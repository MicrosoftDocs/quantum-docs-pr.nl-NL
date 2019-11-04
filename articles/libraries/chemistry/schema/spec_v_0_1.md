---
title: Broombridge-schema specificatie
author: cgranade
ms.author: chgranad@microsoft.com
ms.date: 10/17/2018
ms.topic: article
uid: microsoft.quantum.libraries.chemistry.schema.spec_v_0_1
ms.openlocfilehash: a950e04d44e5de8091b034214258d2c2fa663f58
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/29/2019
ms.locfileid: "73185355"
---
# <a name="broombridge-specification-v01"></a><span data-ttu-id="54116-102">Broombridge-specificatie v 0.1</span><span class="sxs-lookup"><span data-stu-id="54116-102">Broombridge Specification v0.1</span></span> #

<span data-ttu-id="54116-103">De sleutel woorden ' moet ', ' mag niet ', ' vereist ', ' moet ', ' mag niet ', ' moet ', ' mogen ', ' is ', ' mag ' niet ', ' Aanbevolen ' en ' optioneel ' in dit document moeten worden geïnterpreteerd zoals beschreven in [RFC 2119](https://tools.ietf.org/html/rfc2119).</span><span class="sxs-lookup"><span data-stu-id="54116-103">The key words "MUST", "MUST NOT", "REQUIRED", "SHALL", "SHALL NOT", "SHOULD", "SHOULD NOT", "RECOMMENDED",  "MAY", and "OPTIONAL" in this document are to be interpreted as described in [RFC 2119](https://tools.ietf.org/html/rfc2119).</span></span>

<span data-ttu-id="54116-104">Een terzijde met de koppen ' NOTE ', ' informatie ' of ' waarschuwing ' is informatieve.</span><span class="sxs-lookup"><span data-stu-id="54116-104">Any sidebar with the headings "NOTE," "INFORMATION," or "WARNING" is informative.</span></span>

## <a name="introduction"></a><span data-ttu-id="54116-105">Inleiding</span><span class="sxs-lookup"><span data-stu-id="54116-105">Introduction</span></span> ##

<span data-ttu-id="54116-106">Deze sectie is informatieve.</span><span class="sxs-lookup"><span data-stu-id="54116-106">This section is informative.</span></span>

<span data-ttu-id="54116-107">Broombridge documenten zijn bedoeld voor het communiceren van exemplaren van simulatie problemen in quantum chemie voor verwerking met de Quantum simulatie en programmeer toolchains.</span><span class="sxs-lookup"><span data-stu-id="54116-107">Broombridge documents are intended to communicate instances of simulation problems in quantum chemistry for processing using quantum simulation and programming toolchains.</span></span>

## <a name="serialization"></a><span data-ttu-id="54116-108">Serialisatie</span><span class="sxs-lookup"><span data-stu-id="54116-108">Serialization</span></span> ##

<span data-ttu-id="54116-109">Deze sectie is normatieve.</span><span class="sxs-lookup"><span data-stu-id="54116-109">This section is normative.</span></span>

<span data-ttu-id="54116-110">Een Broombridge-document moet worden geserialiseerd als een [YAML 1,2-document](http://yaml.org/spec/) dat een JSON-object vertegenwoordigt, zoals beschreven in sectie 2,2 van [RFC 4627](https://tools.ietf.org/html/rfc4627) .</span><span class="sxs-lookup"><span data-stu-id="54116-110">A Broombridge document MUST be serialized as a [YAML 1.2 document](http://yaml.org/spec/) representing a JSON object as described in [RFC 4627](https://tools.ietf.org/html/rfc4627) section 2.2.</span></span>
<span data-ttu-id="54116-111">Het object dat is geserialiseerd naar YAML moet een eigenschap hebben `"$schema"` waarvan de waarde `"https://raw.githubusercontent.com/Microsoft/Quantum/master/Chemistry/Schema/qchem-0.1.schema.json"`is, en moet geldig zijn volgens de specificaties van het JSON-schema Draft-06 [[1](https://tools.ietf.org/html/draft-wright-json-schema-01), [2](https://tools.ietf.org/html/draft-wright-json-schema-validation-01)].</span><span class="sxs-lookup"><span data-stu-id="54116-111">The object serialized to YAML MUST have a property `"$schema"` whose value is `"https://raw.githubusercontent.com/Microsoft/Quantum/master/Chemistry/Schema/qchem-0.1.schema.json"`, and MUST be valid according to the JSON Schema draft-06 specifications [[1](https://tools.ietf.org/html/draft-wright-json-schema-01), [2](https://tools.ietf.org/html/draft-wright-json-schema-validation-01)].</span></span>

<span data-ttu-id="54116-112">Voor de rest van deze specificatie verwijst het object Broombridge naar het JSON-object dat is gedeserialiseerd van een Broombridge YAML-document.</span><span class="sxs-lookup"><span data-stu-id="54116-112">For the remainder of this specification, "the Broombridge object" will refer to the JSON object deserialized from a Broombridge YAML document.</span></span>

<span data-ttu-id="54116-113">Tenzij anders uitdrukkelijk aangegeven, moeten objecten geen aanvullende eigenschappen hebben die niet expliciet in dit document zijn opgegeven.</span><span class="sxs-lookup"><span data-stu-id="54116-113">Unless otherwise explicitly noted, objects MUST NOT have additional properties beyond those specified explicitly in this document.</span></span>

## <a name="additional-definitions"></a><span data-ttu-id="54116-114">Aanvullende definities</span><span class="sxs-lookup"><span data-stu-id="54116-114">Additional Definitions</span></span> ##

<span data-ttu-id="54116-115">Deze sectie is normatieve.</span><span class="sxs-lookup"><span data-stu-id="54116-115">This section is normative.</span></span>

### <a name="quantity-objects"></a><span data-ttu-id="54116-116">Hoeveelheids objecten</span><span class="sxs-lookup"><span data-stu-id="54116-116">Quantity Objects</span></span> ###

<span data-ttu-id="54116-117">Deze sectie is normatieve.</span><span class="sxs-lookup"><span data-stu-id="54116-117">This section is normative.</span></span>

<span data-ttu-id="54116-118">Een _hoeveelheids object_ is een JSON-object en moet een eigenschap hebben `units` waarvan de waarde een van de toegestane waarden in tabel 1 is.</span><span class="sxs-lookup"><span data-stu-id="54116-118">A _quantity object_ is a JSON object, and MUST have a property `units` whose value is one of the allowed values listed in Table 1.</span></span>

<span data-ttu-id="54116-119">Een hoeveelheids object is een _eenvoudig hoeveelheids object_ als het een enkele eigenschap heeft `value` naast de eigenschap `units`.</span><span class="sxs-lookup"><span data-stu-id="54116-119">A quantity object is a _simple quantity object_ if it has a single property `value` in addition to its `units` property.</span></span>
<span data-ttu-id="54116-120">De waarde van de eigenschap `value` moet een getal zijn.</span><span class="sxs-lookup"><span data-stu-id="54116-120">The value of the `value` property MUST be a number.</span></span>

<span data-ttu-id="54116-121">Een hoeveelheids object is een _begrensd hoeveelheids object_ als het de eigenschappen `lower` heeft en `upper` naast de eigenschap `units`.</span><span class="sxs-lookup"><span data-stu-id="54116-121">A quantity object is a _bounded quantity object_ if it has the properties `lower` and `upper` in addition to its `units` property.</span></span>
<span data-ttu-id="54116-122">De waarden van de eigenschappen `lower` en `upper` moeten getallen zijn.</span><span class="sxs-lookup"><span data-stu-id="54116-122">The values of the `lower` and `upper` properties MUST be numbers.</span></span>
<span data-ttu-id="54116-123">Een gebonden hoeveelheids object kan een eigenschap hebben `value` waarvan de waarde een getal is.</span><span class="sxs-lookup"><span data-stu-id="54116-123">A bounded quantity object MAY have a property `value` whose value is a number.</span></span>

<span data-ttu-id="54116-124">Een hoeveelheids object is een object met een _Sparse matrix_ als het de eigenschap `format` en een eigenschap `values` bevat naast de eigenschap `units`.</span><span class="sxs-lookup"><span data-stu-id="54116-124">A quantity object is a _sparse array quantity object_ if it has the property `format` and a property `values` in addition to its `units` property.</span></span>
<span data-ttu-id="54116-125">De waarde van `format` moet de teken reeks zijn `sparse`.</span><span class="sxs-lookup"><span data-stu-id="54116-125">The value of `format` MUST be the string `sparse`.</span></span>
<span data-ttu-id="54116-126">De waarde van de eigenschap `values` moet een matrix zijn.</span><span class="sxs-lookup"><span data-stu-id="54116-126">The value of the `values` property MUST be an array.</span></span>
<span data-ttu-id="54116-127">Elk element van `values` moet een matrix zijn die de indices en waarde van de Sparse matrix vertegenwoordigt.</span><span class="sxs-lookup"><span data-stu-id="54116-127">Each element of `values` MUST be an array representing the indices and value of the sparse array quantity.</span></span>

<span data-ttu-id="54116-128">De indexen voor elk element van een object met een Sparse matrix moeten uniek zijn binnen het gehele object voor de Sparse matrix.</span><span class="sxs-lookup"><span data-stu-id="54116-128">The indices for each element of a sparse array quantity object MUST be unique across the entire sparse array quantity object.</span></span>
<span data-ttu-id="54116-129">Als een index aanwezig is met een waarde van `0`, moet een parser het object voor de Sparse matrix op dezelfde manier behandelen aan een object met een Sparse matrix, waarin de index niet aanwezig is.</span><span class="sxs-lookup"><span data-stu-id="54116-129">If an index is present with a value of `0`, a parser MUST treat the sparse array quantity object identically to a sparse array quantity object in which that index is not present at all.</span></span>


<span data-ttu-id="54116-130">Een hoeveelheids object moet</span><span class="sxs-lookup"><span data-stu-id="54116-130">A quantity object MUST either be</span></span>

- <span data-ttu-id="54116-131">een eenvoudig hoeveelheids object,</span><span class="sxs-lookup"><span data-stu-id="54116-131">a simple quantity object,</span></span>
- <span data-ttu-id="54116-132">een begrensd hoeveelheids object, of</span><span class="sxs-lookup"><span data-stu-id="54116-132">a bounded quantity object, or</span></span>
- <span data-ttu-id="54116-133">een object met een Sparse matrix.</span><span class="sxs-lookup"><span data-stu-id="54116-133">a sparse array quantity object.</span></span>


### <a name="examples"></a><span data-ttu-id="54116-134">Voorbeelden</span><span class="sxs-lookup"><span data-stu-id="54116-134">Examples</span></span> ###

<span data-ttu-id="54116-135">Deze sectie is informatieve.</span><span class="sxs-lookup"><span data-stu-id="54116-135">This section is informative.</span></span>

<span data-ttu-id="54116-136">Een eenvoudige hoeveelheid voor $1.9844146837\,\mathrm{Ha} $:</span><span class="sxs-lookup"><span data-stu-id="54116-136">A simple quantity representing $1.9844146837\,\mathrm{Ha}$:</span></span>

```yaml
coulomb_repulsion:
    value: 1.9844146837
    units: hartree
```

<span data-ttu-id="54116-137">Een grens hoeveelheid die een uniforme distributie vertegenwoordigt voor het interval $ [-7,-6]\,\mathrm{Ha} $:</span><span class="sxs-lookup"><span data-stu-id="54116-137">A bounded quantity representing a uniform distribution over the interval $[-7, -6]\,\mathrm{Ha}$:</span></span>

```yaml
fci_energy:
    upper: -6
    lower: -7
    units: hartree
```

<span data-ttu-id="54116-138">Hier volgt een Sparse matrix met een element `[1, 2]` gelijk aan `hello` en een element `[3, 4]` gelijk is aan `world`:</span><span class="sxs-lookup"><span data-stu-id="54116-138">The following is a sparse array quantity with an element `[1, 2]` equal to `hello` and an element `[3, 4]` equal to `world`:</span></span>

```yaml
sparse_example:
    format: sparse
    units: hartree
    values:
    - [1, 2, "hello"]
    - [3, 4, "world"]
```

## <a name="format-section"></a><span data-ttu-id="54116-139">Indelings sectie</span><span class="sxs-lookup"><span data-stu-id="54116-139">Format Section</span></span> ##

<span data-ttu-id="54116-140">Deze sectie is normatieve.</span><span class="sxs-lookup"><span data-stu-id="54116-140">This section is normative.</span></span>

<span data-ttu-id="54116-141">Het Broombridge-object moet een eigenschap hebben `format` waarvan de waarde een JSON-object is met één eigenschap met de naam `version`.</span><span class="sxs-lookup"><span data-stu-id="54116-141">The Broombridge object MUST have a property `format` whose value is a JSON object with one property called `version`.</span></span>
<span data-ttu-id="54116-142">De eigenschap `version` moet de waarde `"0.1"`hebben.</span><span class="sxs-lookup"><span data-stu-id="54116-142">The `version` property MUST have the value `"0.1"`.</span></span>

### <a name="example"></a><span data-ttu-id="54116-143">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="54116-143">Example</span></span> ###

<span data-ttu-id="54116-144">Deze sectie is informatieve.</span><span class="sxs-lookup"><span data-stu-id="54116-144">This section is informative.</span></span>

```yaml
format:                        # required
    version: "0.1"             # must match exactly
```

## <a name="integral-sets-section"></a><span data-ttu-id="54116-145">Sectie integrale sets</span><span class="sxs-lookup"><span data-stu-id="54116-145">Integral Sets Section</span></span> ##

<span data-ttu-id="54116-146">Deze sectie is normatieve.</span><span class="sxs-lookup"><span data-stu-id="54116-146">This section is normative.</span></span>

<span data-ttu-id="54116-147">Het Broombridge-object moet een eigenschap hebben `integral_sets` waarvan de waarde een JSON-matrix is.</span><span class="sxs-lookup"><span data-stu-id="54116-147">The Broombridge object MUST have a property `integral_sets` whose value is a JSON array.</span></span>
<span data-ttu-id="54116-148">Elk item in de waarde van de eigenschap `integral_sets` moet een JSON-object zijn dat een set integralen beschrijft, zoals wordt beschreven in de rest van deze sectie.</span><span class="sxs-lookup"><span data-stu-id="54116-148">Each item in the value of the `integral_sets` property MUST be a JSON object describing one set of integrals, as described in the remainder of this section.</span></span>
<span data-ttu-id="54116-149">In de rest van deze sectie verwijst de term ' integraal set object ' naar een item in de waarde van de eigenschap `integral_sets` van het object Broombridge.</span><span class="sxs-lookup"><span data-stu-id="54116-149">In the remainder of this section, the term "integral set object" will refer to an item in the value of the `integral_sets` property of the Broombridge object.</span></span>

<span data-ttu-id="54116-150">Elk integraal set-object moet een eigenschap hebben `metadata` waarvan de waarde een JSON-object is.</span><span class="sxs-lookup"><span data-stu-id="54116-150">Each integral set object MUST have a property `metadata` whose value is a JSON object.</span></span>
<span data-ttu-id="54116-151">De waarde van `metadata` kan het lege JSON-object zijn (dat wil zeggen, `{}`) of extra eigenschappen bevatten die zijn gedefinieerd door de-implementatie.</span><span class="sxs-lookup"><span data-stu-id="54116-151">The value of `metadata` MAY be the empty JSON object (that is, `{}`), or MAY contain additional properties defined by the implementor.</span></span>

### <a name="hamiltonian-section"></a><span data-ttu-id="54116-152">De sectie Hamiltonian</span><span class="sxs-lookup"><span data-stu-id="54116-152">Hamiltonian Section</span></span> ###

#### <a name="overview"></a><span data-ttu-id="54116-153">Overzicht</span><span class="sxs-lookup"><span data-stu-id="54116-153">Overview</span></span> ####

<span data-ttu-id="54116-154">Deze sectie is informatieve.</span><span class="sxs-lookup"><span data-stu-id="54116-154">This section is informative.</span></span>

<span data-ttu-id="54116-155">De eigenschap `hamiltonian` van elk integraal set-object beschrijft de Hamiltonian voor een bepaald probleem met de quantum chemie door de termen met één en twee hoofd tekst weer te geven als Sparse matrix met reële getallen.</span><span class="sxs-lookup"><span data-stu-id="54116-155">The `hamiltonian` property of each integral set object describes the Hamiltonian for a particular quantum chemistry problem by listing out its one- and two-body terms as sparse arrays of real numbers.</span></span>
<span data-ttu-id="54116-156">De Hamiltonian-Opera tors die door elk integraal set-object worden beschreven, hebben het formulier</span><span class="sxs-lookup"><span data-stu-id="54116-156">The Hamiltonian operators described by each integral set object take the form</span></span>

<span data-ttu-id="54116-157">$ $ H = \sum\_\{i, j\}\sum\_{\sigma\in\\{\uparrow, \downarrow\\}} H\_\{IJ\} a ^\{\dagger\}\_{i , \sigma} a\_{j, \sigma} + \frac{1}{2}\sum\_\{i, j, k, l\}\sum\_{\sigma, \rho\in\\{\uparrow, \downarrow\\}} h\_{ijkl} a ^ \dagger\_{i , \sigma} a ^ \dagger\_{k, \rho} a\_{l \rho} a\_{j, \sigma}, $ $</span><span class="sxs-lookup"><span data-stu-id="54116-157">$$ H = \sum\_\{i,j\}\sum\_{\sigma\in\\{\uparrow,\downarrow\\}} h\_\{ij\} a^\{\dagger\}\_{i,\sigma} a\_{j,\sigma} + \frac{1}{2}\sum\_\{i,j,k,l\}\sum\_{\sigma,\rho\in\\{\uparrow,\downarrow\\}} h\_{ijkl} a^\dagger\_{i,\sigma} a^\dagger\_{k,\rho} a\_{l,\rho} a\_{j,\sigma}, $$</span></span>

<span data-ttu-id="54116-158">hier $h _ {ijkl} = (IJ | KL) $ in Mulliken Convention.</span><span class="sxs-lookup"><span data-stu-id="54116-158">here $h_{ijkl}= (ij|kl)$ in Mulliken convention.</span></span>

<span data-ttu-id="54116-159">Ter duidelijkheid is de term één-elektro periode</span><span class="sxs-lookup"><span data-stu-id="54116-159">For clarity, the one-electron term is</span></span>

<span data-ttu-id="54116-160">$ $ h_ {IJ} = \int {\mathrm d} x \psi ^ \*\_i (x) \left (\frac{1}{2}\nabla ^ 2 + \sum\_{A} \frac{Z\_A} {| x-x\_A |}  \right) \psi\_j (x), $ $</span><span class="sxs-lookup"><span data-stu-id="54116-160">$$ h_{ij} = \int {\mathrm d}x \psi^\*\_i(x) \left(\frac{1}{2}\nabla^2 + \sum\_{A}\frac{Z\_A}{|x-x\_A|}  \right) \psi\_j(x), $$</span></span>

<span data-ttu-id="54116-161">en de twee-elektro periode is</span><span class="sxs-lookup"><span data-stu-id="54116-161">and the two-electron term is</span></span>

<span data-ttu-id="54116-162">$ $ h\_\{ijkl\} = \iint \{\mathrm d\}x ^ 2 \psi ^\{\*\}\_i (x\_1) \psi\_j (x\_1) \frac\{1\}\{\|x\_1-x\_2\|\}\psi\_k ^\{\*\}(x\_2) \psi\_l (x\_2).</span><span class="sxs-lookup"><span data-stu-id="54116-162">$$ h\_\{ijkl\} = \iint \{\mathrm d\}x^2 \psi^\{\*\}\_i(x\_1)\psi\_j(x\_1) \frac\{1\}\{\|x\_1 -x\_2\|\}\psi\_k^\{\*\}(x\_2) \psi\_l(x\_2).</span></span>
$$

<span data-ttu-id="54116-163">Zoals vermeld in de beschrijving van de [eigenschap`basis_set`](#basis-set-object) van elk element van de eigenschap `integral_sets`, gaan we er verder vanuit dat de gebruikte basis functies echt waard zijn.</span><span class="sxs-lookup"><span data-stu-id="54116-163">As noted in our description of the [`basis_set` property](#basis-set-object) of each element of the `integral_sets` property, we further explicitly assume that the basis functions used are real-valued.</span></span>
<span data-ttu-id="54116-164">Hierdoor kunnen we de volgende Symmetries gebruiken tussen de voor waarden om de weer gave van de Hamiltonian te comprimeren.</span><span class="sxs-lookup"><span data-stu-id="54116-164">This allows us to use the following symmetries between the terms to compress the representation of the Hamiltonian.</span></span>

<span data-ttu-id="54116-165">$ $ h_ {ijkl} = h_ {ijlk} = h_ {jikl} = h_ {jilk} = h_ {klij} = h_ {klji} = h_ {lkij} = h_ {lkji}.</span><span class="sxs-lookup"><span data-stu-id="54116-165">$$ h_{ijkl} = h_{ijlk}=h_{jikl}=h_{jilk}=h_{klij}=h_{klji}=h_{lkij}=h_{lkji}.</span></span>
$$


#### <a name="contents"></a><span data-ttu-id="54116-166">Inhoud</span><span class="sxs-lookup"><span data-stu-id="54116-166">Contents</span></span> ####

<span data-ttu-id="54116-167">Deze sectie is normatieve.</span><span class="sxs-lookup"><span data-stu-id="54116-167">This section is normative.</span></span>

<span data-ttu-id="54116-168">Elke integrale set moet een eigenschap hebben `hamiltonian` waarvan de waarde een JSON-object is.</span><span class="sxs-lookup"><span data-stu-id="54116-168">Each integral set MUST have a property `hamiltonian` whose value is a JSON object.</span></span>
<span data-ttu-id="54116-169">De waarde van de eigenschap `hamiltonian` wordt ook wel een Hamiltonian-object genoemd en moet de eigenschappen `one_electron_integrals` en `two_electron_integrals` hebben, zoals wordt beschreven in de rest van deze sectie.</span><span class="sxs-lookup"><span data-stu-id="54116-169">The value of the `hamiltonian` property is known as a Hamiltonian object, and MUST have the properties `one_electron_integrals` and `two_electron_integrals` as described in the remainder of this section.</span></span>
<span data-ttu-id="54116-170">Een Hamiltonian-object kan ook een eigenschap hebben `particle_hole_representation`.</span><span class="sxs-lookup"><span data-stu-id="54116-170">A Hamiltonian object MAY also have a property `particle_hole_representation`.</span></span>
<span data-ttu-id="54116-171">Indien aanwezig moet de waarde van `particle_hole_representation` de notatie volgen die in de rest van deze sectie wordt beschreven.</span><span class="sxs-lookup"><span data-stu-id="54116-171">If present, the value of `particle_hole_representation` MUST follow the format described in the remainder of this section.</span></span>

##### <a name="one-electron-integrals-object"></a><span data-ttu-id="54116-172">Object met één elektron integraal</span><span class="sxs-lookup"><span data-stu-id="54116-172">One-Electron Integrals Object</span></span> #####

<span data-ttu-id="54116-173">Deze sectie is normatieve.</span><span class="sxs-lookup"><span data-stu-id="54116-173">This section is normative.</span></span>

<span data-ttu-id="54116-174">De eigenschap `one_electron_integrals` van het Hamiltonian-object moet een Sparse-matrix hoeveelheid zijn waarvan de indices twee gehele getallen zijn en waarvan de waarden getallen zijn.</span><span class="sxs-lookup"><span data-stu-id="54116-174">The `one_electron_integrals` property of the Hamiltonian object MUST be a sparse array quantity whose indices are two integers and whose values are numbers.</span></span>
<span data-ttu-id="54116-175">Elke term moet indexen bevatten `[i, j]` waar `i >= j`.</span><span class="sxs-lookup"><span data-stu-id="54116-175">Every term MUST have indices `[i, j]` where `i >= j`.</span></span>

> <span data-ttu-id="54116-176">ERAAN Dit weerspiegelt de symmetrie die $h _ {IJ} = h_ {Ji} $, wat het gevolg is van het feit dat de Hamiltonian Hermitian is.</span><span class="sxs-lookup"><span data-stu-id="54116-176">[NOTE] This reflects the symmetry that $h_{ij} = h_{ji}$ which is a consequence of the fact that the Hamiltonian is Hermitian.</span></span>


###### <a name="example"></a><span data-ttu-id="54116-177">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="54116-177">Example</span></span> ######

<span data-ttu-id="54116-178">Deze sectie is informatieve.</span><span class="sxs-lookup"><span data-stu-id="54116-178">This section is informative.</span></span>

<span data-ttu-id="54116-179">De volgende Sparse matrix vertegenwoordigt de Hamiltonian $ $ H = \left (-5,0 (a ^\{\dagger\}\_{1, \uparrow} een\_{1, \uparrow} + a ^\{\dagger\}\_{1, \downarrow} a\_{1 , \downarrow}) + 0,17 (a ^\{\dagger\}\_{2, \uparrow} a\_{1, \uparrow} + a ^\{\dagger\}\_{1, \uparrow} a\_{2, \uparrow} + a ^\{\dagger\}\_{2 , \downarrow} a\_{1, \downarrow} + a ^\{\dagger\}\_{1, \downarrow} a\_{2, \downarrow}) \right)\\, \mathrm{Ha}.</span><span class="sxs-lookup"><span data-stu-id="54116-179">The following sparse array quantity represents the Hamiltonian $$ H = \left(-5.0  (a^\{\dagger\}\_{1,\uparrow} a\_{1,\uparrow}+a^\{\dagger\}\_{1,\downarrow} a\_{1,\downarrow})+ 0.17 (a^\{\dagger\}\_{2,\uparrow} a\_{1,\uparrow}+ a^\{\dagger\}\_{1,\uparrow} a\_{2,\uparrow}+a^\{\dagger\}\_{2,\downarrow} a\_{1,\downarrow}+ a^\{\dagger\}\_{1,\downarrow} a\_{2,\downarrow})\right)\\,\mathrm{Ha}.</span></span>
$$

```yaml
one_electron_integrals:     # required
    units: hartree          # required
    format: sparse          # required
    values:                 # required
        # i j f(i,j)
        - [1, 1, -5.0]
        - [2, 1,  0.17]
```
> [!NOTE]
> <span data-ttu-id="54116-180">Broombridge maakt gebruik van op 1 gebaseerde indexering.</span><span class="sxs-lookup"><span data-stu-id="54116-180">Broombridge uses 1-based indexing.</span></span>


##### <a name="two-electron-integrals-object"></a><span data-ttu-id="54116-181">Twee-elektroden integraal object</span><span class="sxs-lookup"><span data-stu-id="54116-181">Two-Electron Integrals Object</span></span> #####

<span data-ttu-id="54116-182">Deze sectie is normatieve.</span><span class="sxs-lookup"><span data-stu-id="54116-182">This section is normative.</span></span>

<span data-ttu-id="54116-183">De eigenschap `two_electron_integrals` van het Hamiltonian-object moet een Sparse matrix zijn met een extra eigenschap met de naam `index_convention`.</span><span class="sxs-lookup"><span data-stu-id="54116-183">The `two_electron_integrals` property of the Hamiltonian object MUST be a sparse array quantity with one additional property called `index_convention`.</span></span>
<span data-ttu-id="54116-184">Elk element van de waarde van `two_electron_integrals` moet vier indexen hebben.</span><span class="sxs-lookup"><span data-stu-id="54116-184">Each element of the value of `two_electron_integrals` MUST have four indices.</span></span>

<span data-ttu-id="54116-185">Elke `two_electron_integrals` eigenschap moet een `index_convention` eigenschap hebben.</span><span class="sxs-lookup"><span data-stu-id="54116-185">Each `two_electron_integrals` property MUST have a `index_convention` property.</span></span>
<span data-ttu-id="54116-186">De waarde van de eigenschap `index_convention` moet een van de toegestane waarden zijn die worden vermeld in tabel 1.</span><span class="sxs-lookup"><span data-stu-id="54116-186">The value of the `index_convention` property MUST be one of the allowed values listed in Table 1.</span></span>
<span data-ttu-id="54116-187">Als de waarde van `index_convention` is `mulliken`en vervolgens voor elk element van de `two_electron_integrals` Sparse matrix, moet een parser die een Broombridge-document laadt een Hamiltonian-term instantiëren die gelijk is aan de twee-elektroden operator $h _ {i, j, k, l} a ^ \dagger_i a ^ \dagger_j a_k a_l $ , waarbij $i $, $j $, $k $ en $l $ gehele getallen in het inclusieve bereik moeten zijn van 1 tot het aantal electrons dat is opgegeven door de eigenschap `n_electrons` van het object integrale set, en waar $h _ {i, j, k, l} $ het element `[i, j, k, l, h(i, j, k, l)]` van de Sparse matrix is.</span><span class="sxs-lookup"><span data-stu-id="54116-187">If the value of `index_convention` is `mulliken`, then for each element of the `two_electron_integrals` sparse array quantity, a parser loading a Broombridge document MUST instantiate a Hamiltonian term equal to the two-electron operator $h_{i, j, k, l} a^\dagger_i a^\dagger_j a_k a_l$, where $i$, $j$, $k$, and $l$ MUST be integers in the inclusive range from 1 to the number of electrons specified by the `n_electrons` property of the integral set object, and where $h_{i, j, k, l}$ is the element `[i, j, k, l, h(i, j, k, l)]` of the sparse array quantity.</span></span>

###### <a name="symmetries"></a><span data-ttu-id="54116-188">Symmetries</span><span class="sxs-lookup"><span data-stu-id="54116-188">Symmetries</span></span> ######

<span data-ttu-id="54116-189">Deze sectie is normatieve.</span><span class="sxs-lookup"><span data-stu-id="54116-189">This section is normative.</span></span>

<span data-ttu-id="54116-190">Als de eigenschap `index_convention` van een `two_electron_integrals` object gelijk is aan `mulliken`en als er een element met indexen `[i, j, k, l]` aanwezig is, mogen de volgende indexen niet aanwezig zijn, tenzij ze gelijk zijn aan `[i, j, k, l]`:</span><span class="sxs-lookup"><span data-stu-id="54116-190">If the `index_convention` property of a `two_electron_integrals` object is equal to `mulliken`, then if an element with indices `[i, j, k, l]` is present, the following indices MUST NOT be present unless they are equal to `[i, j, k, l]`:</span></span>

- `[i, j, l, k]`
- `[j, i, k, l]`
- `[j, i, l, k]`
- `[k, l, i, j]`
- `[k, l, j, i]`
- `[l, k, j, i]`

> [!NOTE]
> <span data-ttu-id="54116-191">Omdat de eigenschap `index_convention` een object met een sparse hoeveelheid is, kunnen er geen indices worden herhaald op verschillende elementen.</span><span class="sxs-lookup"><span data-stu-id="54116-191">Because the `index_convention` property is a sparse quantity object, no indices may be repeated on different elements.</span></span>
> <span data-ttu-id="54116-192">Met name als er een element met indexen `[i, j, k, l]` aanwezig is, kan geen ander element deze indexen bevatten.</span><span class="sxs-lookup"><span data-stu-id="54116-192">In particular, if an element with indices `[i, j, k, l]` is present, no other element may have those indices.</span></span>


<!-- h_{ijkl} = h_{ijlk}=h_{jikl}=h_{jilk}=h_{klij}=h_{klji}=h_{lkji}. -->

###### <a name="example"></a><span data-ttu-id="54116-193">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="54116-193">Example</span></span> #######

<span data-ttu-id="54116-194">Deze sectie is informatieve.</span><span class="sxs-lookup"><span data-stu-id="54116-194">This section is informative.</span></span>

<span data-ttu-id="54116-195">Het volgende object geeft de Hamiltonian</span><span class="sxs-lookup"><span data-stu-id="54116-195">The following object specifies the Hamiltonian</span></span>

<span data-ttu-id="54116-196">$ $ H = \frac12 \sum\_{\sigma, \rho\in\\{\uparrow, \downarrow\\}} \Biggr (1,6 a ^ {\dagger}\_{1, \sigma} a ^ {\dagger}\_{1, \rho} a\_{1, \rho} a\_{1, \sigma}-0,1 a ^ {\dagger}\_{6 , \sigma} a ^ {\dagger}\_{1, \rho} a\_{3 \rho} a\_{2, \sigma}-0,1 a ^ {\dagger}\_{6, \sigma} a ^ {\dagger}\_{1, \rho} a\_{2, \rho} a\_{3 , \sigma}-0,1 a ^ {\dagger}\_{1, \sigma} a ^ {\dagger}\_{6, \rho} a\_{3, \rho} a\_{2, \sigma}-0,1 a ^ {\dagger}\_{1, \sigma} a ^ {\dagger}\_6, \rho} a\_{2 , \rho} a\_{3, \sigma} $ $ $ $-0,1 a ^ {\dagger}\_{3, \sigma} a ^ {\dagger}\_{2, \rho} a\_{6, \rho} a\_{1, \sigma}-0,1 a ^ {\dagger}\_{3, \sigma} a ^ {\dagger}\_{2 , \rho} a\_{1, \rho} a\_{6, \sigma}-0,1 a ^ {\dagger}\_{2, \sigma} a ^ {\dagger}\_{3, \rho} a\_{6, \rho} a\_{1, \sigma}-0,1 a ^ {\dagger}\_{2 , \sigma} a ^ {\dagger}\_{3, \rho} a\_{1 \rho} a\_{6, \sigma}\Biggr)\\, \textrm{Ha}.</span><span class="sxs-lookup"><span data-stu-id="54116-196">$$ H = \frac12 \sum\_{\sigma,\rho\in\\{\uparrow,\downarrow\\}}\Biggr( 1.6 a^{\dagger}\_{1,\sigma} a^{\dagger}\_{1,\rho} a\_{1,\rho} a\_{1,\sigma}- 0.1 a^{\dagger}\_{6,\sigma} a^{\dagger}\_{1,\rho} a\_{3,\rho} a\_{2,\sigma}- 0.1 a^{\dagger}\_{6,\sigma} a^{\dagger}\_{1,\rho} a\_{2,\rho} a\_{3,\sigma}- 0.1 a^{\dagger}\_{1,\sigma} a^{\dagger}\_{6,\rho} a\_{3,\rho} a\_{2,\sigma}- 0.1 a^{\dagger}\_{1,\sigma} a^{\dagger}\_{6,\rho} a\_{2,\rho} a\_{3,\sigma} $$ $$- 0.1 a^{\dagger}\_{3,\sigma} a^{\dagger}\_{2,\rho} a\_{6,\rho} a\_{1,\sigma}- 0.1 a^{\dagger}\_{3,\sigma} a^{\dagger}\_{2,\rho} a\_{1,\rho} a\_{6,\sigma}- 0.1 a^{\dagger}\_{2,\sigma} a^{\dagger}\_{3,\rho} a\_{6,\rho} a\_{1,\sigma}- 0.1 a^{\dagger}\_{2,\sigma} a^{\dagger}\_{3,\rho} a\_{1,\rho} a\_{6,\sigma}\Biggr)\\,\textrm{Ha}.</span></span>
$$

```yaml
two_electron_integrals:
    index_convention: mulliken
    units: hartree
    format: sparse
    values:
        - [1, 1, 1, 1,  1.6]
        - [6, 1, 3, 2, -0.1]
```

##### <a name="particlehole-representation-object"></a><span data-ttu-id="54116-197">Partikel-object: gat weer geven</span><span class="sxs-lookup"><span data-stu-id="54116-197">Particle–Hole Representation Object</span></span> #####

<span data-ttu-id="54116-198">Deze sectie is normatieve.</span><span class="sxs-lookup"><span data-stu-id="54116-198">This section is normative.</span></span>

<span data-ttu-id="54116-199">Met het object partikel-gat geeft u op dat de opgeslagen integralen worden gedefinieerd met betrekking tot de weer gave van de opening en Annihilation Opera tors waarin de berekenings operatoren worden beschreven die niet van de gebruikte referentie status bestaan, zoals een Hartree – Fock-status.</span><span class="sxs-lookup"><span data-stu-id="54116-199">The particle–hole representation object specifies that the integrals stored are defined with respect to particle hole representation wherein the creation and annihilation operators describe excitations away from the reference state used, such as a Hartree–Fock state.</span></span>
<span data-ttu-id="54116-200">Het object is optioneel.</span><span class="sxs-lookup"><span data-stu-id="54116-200">The object is OPTIONAL.</span></span>
<span data-ttu-id="54116-201">Als het object niet is opgegeven, wordt de Hamiltonian geïnterpreteerd als niet gegeven in partikel-hole-weer gave.</span><span class="sxs-lookup"><span data-stu-id="54116-201">If the object is not specified then the Hamiltonian is to be interpreted as not given in particle-hole representation.</span></span>
<span data-ttu-id="54116-202">Indien aanwezig, moet de waarde van `particle_hole_representation` een Sparse matrix hoeveelheid object zijn waarvan de indexen vier gehele getallen zijn en waarvan de waarden een getal en een teken reeks zijn.</span><span class="sxs-lookup"><span data-stu-id="54116-202">If present, the value of `particle_hole_representation` MUST be a sparse array quantity object whose indices are four integers, and whose values are a number and a string.</span></span>
<span data-ttu-id="54116-203">Het teken reeks gedeelte van de waarde van elk element mag alleen de tekens `'+'` en `'-'` bevatten die aangeeft of een bepaalde factor in de term een aanmaak-of Annihilation-operator is in de weer gave partikel-gat.</span><span class="sxs-lookup"><span data-stu-id="54116-203">The string portion of the value of each element MUST contain only the characters `'+'` and `'-'` which specifies whether a given factor in the term is a creation or annihilation operator in the particle–hole representation.</span></span>  <span data-ttu-id="54116-204">`"-+++"` wordt bijvoorbeeld gereageerd op een gat dat wordt gemaakt op de site $i $ en de partikels die worden gemaakt op sites $j, k $ en $l $.</span><span class="sxs-lookup"><span data-stu-id="54116-204">For example `"-+++"` coresponds to a hole being created at site $i$ and particles being created at sites $j,k$ and $l$.</span></span>

> [!NOTE]
> <span data-ttu-id="54116-205">Als de waarde van de `particle_hole_representation` een Sparse matrix hoeveelheid object is, moeten de `unit` en `format` eigenschappen worden opgegeven.</span><span class="sxs-lookup"><span data-stu-id="54116-205">As the value of the `particle_hole_representation` is a sparse array quantity object, the `unit` and `format` properties must be specified.</span></span>
> <span data-ttu-id="54116-206">Acceptabele eenheden zijn opgenomen in tabel 1.</span><span class="sxs-lookup"><span data-stu-id="54116-206">Acceptable units include are listed in Table 1.</span></span>
> <span data-ttu-id="54116-207">De eigenschap `format` is vereist en geeft aan of de Hamiltonian coëfficiënten zijn opgegeven als een compacte of Sparse matrix.</span><span class="sxs-lookup"><span data-stu-id="54116-207">The `format` property is required, and indicates whether the Hamiltonian coefficients are specified as a dense or sparse array.</span></span>
> <span data-ttu-id="54116-208">In de huidige versie worden alleen sparse matrices ondersteund, met uitleg dat alle niet-opgegeven elementen $0 $ zijn, maar toekomstige versies kunnen ondersteuning toevoegen voor aanvullende waarden van de eigenschap `format`.</span><span class="sxs-lookup"><span data-stu-id="54116-208">In the current version, only sparse arrays are supported, with interpretation that all unspecified elements are $0$, but future versions may add support for additional values of the `format` property.</span></span>

### <a name="initial-state-section"></a><span data-ttu-id="54116-209">Eerste status sectie</span><span class="sxs-lookup"><span data-stu-id="54116-209">Initial State Section</span></span> ###

<span data-ttu-id="54116-210">Het initial_state_suggestion-object geeft de initiële Quantum statussen van belang voor de opgegeven Hamiltonian.</span><span class="sxs-lookup"><span data-stu-id="54116-210">The initial_state_suggestion object specifies initial quantum states of interest to the specified Hamiltonian.</span></span> <span data-ttu-id="54116-211">Dit object moet een matrix van JSON-`state` objecten zijn.</span><span class="sxs-lookup"><span data-stu-id="54116-211">This object must be an array of JSON `state` objects.</span></span>

#### <a name="state-object"></a><span data-ttu-id="54116-212">Status object</span><span class="sxs-lookup"><span data-stu-id="54116-212">State object</span></span> ####

<span data-ttu-id="54116-213">Elke status vertegenwoordigt een superpositie van bezette banen.</span><span class="sxs-lookup"><span data-stu-id="54116-213">Each states represents a superposition of occupied orbitals.</span></span> <span data-ttu-id="54116-214">Elk status-object moet een `label` eigenschap hebben die een teken reeks bevat.</span><span class="sxs-lookup"><span data-stu-id="54116-214">Each state object MUST have a `label` property containing a string.</span></span> <span data-ttu-id="54116-215">Elk status-object moet een `superposition` eigenschap hebben die een matrix met basis statussen en hun ongebruikelijke amplitudes bevat.</span><span class="sxs-lookup"><span data-stu-id="54116-215">Each state object MUST have a `superposition` property containing an array of basis states and their unnormalized amplitudes.</span></span>

<span data-ttu-id="54116-216">Bijvoorbeeld: de initiële statussen $ $ \ket{G0} = \ket{G1} = \ket{G2} = (a ^ {\dagger}\_{1, \uparrow}a ^ {\dagger}\_{2, \uparrow}a ^ {\dagger}\_{2, \downarrow}) \ket{0} $ $ $ $ \ket{E} = \frac{0.1 (a ^ {\dagger}\_{1 , \uparrow}a ^ {\dagger}\_{2, \uparrow}a ^ {\dagger}\_{2, \downarrow}) + 0,2 (a ^ {\dagger}\_{1, \uparrow}a ^ {\dagger}\_{3, \uparrow}a ^ {\dagger}\_{2, \downarrow})} {\sqrt{| 0,1 | ^ 2 + | 0,2 | ^ 2}} \ket{0} $ $ zijn vertegenwoordigd door</span><span class="sxs-lookup"><span data-stu-id="54116-216">For example, the initial states $$ \ket{G0}=\ket{G1}=\ket{G2}=(a^{\dagger}\_{1,\uparrow}a^{\dagger}\_{2,\uparrow}a^{\dagger}\_{2,\downarrow})\ket{0} $$ $$ \ket{E}=\frac{0.1 (a^{\dagger}\_{1,\uparrow}a^{\dagger}\_{2,\uparrow}a^{\dagger}\_{2,\downarrow})+0.2 (a^{\dagger}\_{1,\uparrow}a^{\dagger}\_{3,\uparrow}a^{\dagger}\_{2,\downarrow})}{\sqrt{|0.1|^2+|0.2|^2}}\ket{0} $$ are represented by</span></span>
```yaml
initial_state_suggestions: # optional. If not provided, spin-orbitals will be filled to minimize one-body diagonal term energies.
    - state:
        label: "|G0>"
        superposition:
            - [1.0, "(1a)+","(2a)+","(2b)+","|vacuum>"]
    - state:
        label: "|G1>"
        superposition:
            - [-1.0, "(2a)+","(1a)+","(2b)+","|vacuum>"]
    - state:
        label: "|G2>"
        superposition:
            - [1.0, "(3a)","(1a)+","(2a)+","(3a)+","(2b)+","|vacuum>"]
    - state:
        label: "|E>"
        superposition:
            - [0.1, "(1a)+","(2a)+","(2b)+","|vacuum>"]
            - [0.2, "(1a)+","(3a)+","(2b)+","|vacuum>"]
```

#### <a name="basis-set-object"></a><span data-ttu-id="54116-217">Object basis instellen</span><span class="sxs-lookup"><span data-stu-id="54116-217">Basis Set Object</span></span> ####

<span data-ttu-id="54116-218">Deze sectie is normatieve.</span><span class="sxs-lookup"><span data-stu-id="54116-218">This section is normative.</span></span>

<span data-ttu-id="54116-219">Elk integraal set-object kan een `basis_set` eigenschap hebben.</span><span class="sxs-lookup"><span data-stu-id="54116-219">Each integral set object MAY have a `basis_set` property.</span></span>
<span data-ttu-id="54116-220">Indien aanwezig, moet de waarde van de eigenschap `basis_set` een object zijn met twee eigenschappen, `type` en `name`.</span><span class="sxs-lookup"><span data-stu-id="54116-220">If present, the value of the `basis_set` property MUST be an object with two properties, `type` and `name`.</span></span>

<span data-ttu-id="54116-221">De basis functies die door de waarde van de eigenschap `basis_set` worden aangeduid, moeten waarden met een echte naam hebben.</span><span class="sxs-lookup"><span data-stu-id="54116-221">The basis functions identified by the value of the `basis_set` property MUST be real-valued.</span></span>

> [!NOTE]
> <span data-ttu-id="54116-222">De veronderstelling dat alle basis functies worden gerealiseerd, kan in toekomstige versies van deze specificatie worden versoepeld.</span><span class="sxs-lookup"><span data-stu-id="54116-222">The assumption that all basis functions are real-valued may be relaxed in future versions of this specification.</span></span>

## <a name="tables-and-lists"></a><span data-ttu-id="54116-223">Tabellen en lijsten</span><span class="sxs-lookup"><span data-stu-id="54116-223">Tables and Lists</span></span> ##

### <a name="table-1-allowed-physical-units"></a><span data-ttu-id="54116-224">Tabel 1.</span><span class="sxs-lookup"><span data-stu-id="54116-224">Table 1.</span></span> <span data-ttu-id="54116-225">Toegestane fysieke eenheden</span><span class="sxs-lookup"><span data-stu-id="54116-225">Allowed Physical Units</span></span> ###

<span data-ttu-id="54116-226">Deze sectie is normatieve.</span><span class="sxs-lookup"><span data-stu-id="54116-226">This section is normative.</span></span>

<span data-ttu-id="54116-227">Een wille keurige teken reeks die een eenheid opgeeft, moet een van de volgende zijn:</span><span class="sxs-lookup"><span data-stu-id="54116-227">Any string specifying a unit MUST be one of the following:</span></span>

- `hartree`
- `ev`

<span data-ttu-id="54116-228">Parsers en producenten moeten de volgende eenvoudige hoeveelheids objecten behandelen als gelijkwaardig:</span><span class="sxs-lookup"><span data-stu-id="54116-228">Parsers and producers MUST treat the following simple quantity objects as equivalent:</span></span>

```yaml
- {"units": "hartree", "value": 1}
- {"units": "ev", "value": 27.2113831301723}
```

### <a name="table-2-allowed-index-conventions"></a><span data-ttu-id="54116-229">Tabel 2.</span><span class="sxs-lookup"><span data-stu-id="54116-229">Table 2.</span></span> <span data-ttu-id="54116-230">Toegestane index conventies</span><span class="sxs-lookup"><span data-stu-id="54116-230">Allowed Index Conventions</span></span> ###

<span data-ttu-id="54116-231">Deze sectie is normatieve.</span><span class="sxs-lookup"><span data-stu-id="54116-231">This section is normative.</span></span>

<span data-ttu-id="54116-232">Een wille keurige teken reeks die een index Conventie opgeeft, moet een van de volgende zijn:</span><span class="sxs-lookup"><span data-stu-id="54116-232">Any string specifying an index convention MUST be one of the following:</span></span>

- `mulliken`

<span data-ttu-id="54116-233">Deze sectie is informatieve.</span><span class="sxs-lookup"><span data-stu-id="54116-233">This section is informative.</span></span>

<span data-ttu-id="54116-234">In toekomstige versies van deze specificatie kunnen aanvullende index conventies worden geïntroduceerd.</span><span class="sxs-lookup"><span data-stu-id="54116-234">Additional index conventions may be introduced in future versions of this specification.</span></span>

#### <a name="interpretation-of-index-conventions"></a><span data-ttu-id="54116-235">Interpretatie van index conventies</span><span class="sxs-lookup"><span data-stu-id="54116-235">Interpretation of Index Conventions</span></span> ####

<span data-ttu-id="54116-236">Deze sectie is informatieve.</span><span class="sxs-lookup"><span data-stu-id="54116-236">This section is informative.</span></span>
