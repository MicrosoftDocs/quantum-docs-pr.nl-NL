---
title: Broombridge-schema specificatie (ver 0,1)
description: Details van de specificaties voor de Broombridge quantum chemie schema v 0.1 voor de micro soft quantum chemie-bibliotheek.
author: cgranade
ms.author: chgranad@microsoft.com
ms.date: 10/17/2018
ms.topic: article
uid: microsoft.quantum.libraries.chemistry.schema.spec_v_0_1
ms.openlocfilehash: 618892b6cb01855d17522b06e47f72f68595ab38
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/23/2020
ms.locfileid: "85275154"
---
# <a name="broombridge-specification-v01"></a><span data-ttu-id="2af80-103">Broombridge-specificatie v 0.1</span><span class="sxs-lookup"><span data-stu-id="2af80-103">Broombridge Specification v0.1</span></span> #

<span data-ttu-id="2af80-104">De sleutel woorden ' moet ', ' mag niet ', ' vereist ', ' moet ', ' mag niet ', ' moet ', ' mogen ', ' is ', ' mag ' niet ', ' Aanbevolen ' en ' optioneel ' in dit document moeten worden geïnterpreteerd zoals beschreven in [RFC 2119](https://tools.ietf.org/html/rfc2119).</span><span class="sxs-lookup"><span data-stu-id="2af80-104">The key words "MUST", "MUST NOT", "REQUIRED", "SHALL", "SHALL NOT", "SHOULD", "SHOULD NOT", "RECOMMENDED",  "MAY", and "OPTIONAL" in this document are to be interpreted as described in [RFC 2119](https://tools.ietf.org/html/rfc2119).</span></span>

<span data-ttu-id="2af80-105">Een terzijde met de koppen ' NOTE ', ' informatie ' of ' waarschuwing ' is informatieve.</span><span class="sxs-lookup"><span data-stu-id="2af80-105">Any sidebar with the headings "NOTE," "INFORMATION," or "WARNING" is informative.</span></span>

## <a name="introduction"></a><span data-ttu-id="2af80-106">Inleiding</span><span class="sxs-lookup"><span data-stu-id="2af80-106">Introduction</span></span> ##

<span data-ttu-id="2af80-107">Deze sectie is informatieve.</span><span class="sxs-lookup"><span data-stu-id="2af80-107">This section is informative.</span></span>

<span data-ttu-id="2af80-108">Broombridge documenten zijn bedoeld voor het communiceren van exemplaren van simulatie problemen in quantum chemie voor verwerking met de Quantum simulatie en programmeer toolchains.</span><span class="sxs-lookup"><span data-stu-id="2af80-108">Broombridge documents are intended to communicate instances of simulation problems in quantum chemistry for processing using quantum simulation and programming toolchains.</span></span>

## <a name="serialization"></a><span data-ttu-id="2af80-109">Serialisatie</span><span class="sxs-lookup"><span data-stu-id="2af80-109">Serialization</span></span> ##

<span data-ttu-id="2af80-110">Deze sectie is normatieve.</span><span class="sxs-lookup"><span data-stu-id="2af80-110">This section is normative.</span></span>

<span data-ttu-id="2af80-111">Een Broombridge-document moet worden geserialiseerd als een [YAML 1,2-document](http://yaml.org/spec/) dat een JSON-object vertegenwoordigt, zoals beschreven in sectie 2,2 van [RFC 4627](https://tools.ietf.org/html/rfc4627) .</span><span class="sxs-lookup"><span data-stu-id="2af80-111">A Broombridge document MUST be serialized as a [YAML 1.2 document](http://yaml.org/spec/) representing a JSON object as described in [RFC 4627](https://tools.ietf.org/html/rfc4627) section 2.2.</span></span>
<span data-ttu-id="2af80-112">Het object dat is geserialiseerd naar YAML moet een eigenschap hebben `"$schema"` waarvan de waarde is `"https://raw.githubusercontent.com/Microsoft/Quantum/master/Chemistry/Schema/qchem-0.1.schema.json"` , en moet geldig zijn volgens de specificatie van het JSON-schema Draft-06 [[1](https://tools.ietf.org/html/draft-wright-json-schema-01), [2](https://tools.ietf.org/html/draft-wright-json-schema-validation-01)].</span><span class="sxs-lookup"><span data-stu-id="2af80-112">The object serialized to YAML MUST have a property `"$schema"` whose value is `"https://raw.githubusercontent.com/Microsoft/Quantum/master/Chemistry/Schema/qchem-0.1.schema.json"`, and MUST be valid according to the JSON Schema draft-06 specifications [[1](https://tools.ietf.org/html/draft-wright-json-schema-01), [2](https://tools.ietf.org/html/draft-wright-json-schema-validation-01)].</span></span>

<span data-ttu-id="2af80-113">Voor de rest van deze specificatie verwijst het object Broombridge naar het JSON-object dat is gedeserialiseerd van een Broombridge YAML-document.</span><span class="sxs-lookup"><span data-stu-id="2af80-113">For the remainder of this specification, "the Broombridge object" will refer to the JSON object deserialized from a Broombridge YAML document.</span></span>

<span data-ttu-id="2af80-114">Tenzij anders uitdrukkelijk aangegeven, moeten objecten geen aanvullende eigenschappen hebben die niet expliciet in dit document zijn opgegeven.</span><span class="sxs-lookup"><span data-stu-id="2af80-114">Unless otherwise explicitly noted, objects MUST NOT have additional properties beyond those specified explicitly in this document.</span></span>

## <a name="additional-definitions"></a><span data-ttu-id="2af80-115">Aanvullende definities</span><span class="sxs-lookup"><span data-stu-id="2af80-115">Additional Definitions</span></span> ##

<span data-ttu-id="2af80-116">Deze sectie is normatieve.</span><span class="sxs-lookup"><span data-stu-id="2af80-116">This section is normative.</span></span>

### <a name="quantity-objects"></a><span data-ttu-id="2af80-117">Hoeveelheids objecten</span><span class="sxs-lookup"><span data-stu-id="2af80-117">Quantity Objects</span></span> ###

<span data-ttu-id="2af80-118">Deze sectie is normatieve.</span><span class="sxs-lookup"><span data-stu-id="2af80-118">This section is normative.</span></span>

<span data-ttu-id="2af80-119">Een _hoeveelheids object_ is een JSON-object en moet een eigenschap hebben `units` waarvan de waarde een van de toegestane waarden is die worden vermeld in tabel 1.</span><span class="sxs-lookup"><span data-stu-id="2af80-119">A _quantity object_ is a JSON object, and MUST have a property `units` whose value is one of the allowed values listed in Table 1.</span></span>

<span data-ttu-id="2af80-120">Een hoeveelheids object is een _eenvoudig hoeveelheids object_ als het een enkele eigenschap heeft `value` naast de bijbehorende `units` eigenschap.</span><span class="sxs-lookup"><span data-stu-id="2af80-120">A quantity object is a _simple quantity object_ if it has a single property `value` in addition to its `units` property.</span></span>
<span data-ttu-id="2af80-121">De waarde van de `value` eigenschap moet een getal zijn.</span><span class="sxs-lookup"><span data-stu-id="2af80-121">The value of the `value` property MUST be a number.</span></span>

<span data-ttu-id="2af80-122">Een hoeveelheids object is een _begrensd hoeveelheids object_ als dit de eigenschappen bevat `lower` en `upper` naast de `units` eigenschap.</span><span class="sxs-lookup"><span data-stu-id="2af80-122">A quantity object is a _bounded quantity object_ if it has the properties `lower` and `upper` in addition to its `units` property.</span></span>
<span data-ttu-id="2af80-123">De waarden van de `lower` `upper` Eigenschappen en moeten getallen zijn.</span><span class="sxs-lookup"><span data-stu-id="2af80-123">The values of the `lower` and `upper` properties MUST be numbers.</span></span>
<span data-ttu-id="2af80-124">Een begrensd hoeveelheids object kan een eigenschap hebben `value` waarvan de waarde een getal is.</span><span class="sxs-lookup"><span data-stu-id="2af80-124">A bounded quantity object MAY have a property `value` whose value is a number.</span></span>

<span data-ttu-id="2af80-125">Een hoeveelheids object is een object met een _Sparse matrix_ als het de eigenschap `format` en een eigenschap bevat `values` naast de `units` eigenschap.</span><span class="sxs-lookup"><span data-stu-id="2af80-125">A quantity object is a _sparse array quantity object_ if it has the property `format` and a property `values` in addition to its `units` property.</span></span>
<span data-ttu-id="2af80-126">De waarde van `format` moet de teken reeks zijn `sparse` .</span><span class="sxs-lookup"><span data-stu-id="2af80-126">The value of `format` MUST be the string `sparse`.</span></span>
<span data-ttu-id="2af80-127">De waarde van de `values` eigenschap moet een matrix zijn.</span><span class="sxs-lookup"><span data-stu-id="2af80-127">The value of the `values` property MUST be an array.</span></span>
<span data-ttu-id="2af80-128">Elk element van `values` moet een matrix zijn die de indices en waarde van de Sparse matrix vertegenwoordigt.</span><span class="sxs-lookup"><span data-stu-id="2af80-128">Each element of `values` MUST be an array representing the indices and value of the sparse array quantity.</span></span>

<span data-ttu-id="2af80-129">De indexen voor elk element van een object met een Sparse matrix moeten uniek zijn binnen het gehele object voor de Sparse matrix.</span><span class="sxs-lookup"><span data-stu-id="2af80-129">The indices for each element of a sparse array quantity object MUST be unique across the entire sparse array quantity object.</span></span>
<span data-ttu-id="2af80-130">Als een index aanwezig is met een waarde van `0` , moet een parser het object van de Sparse matrix op dezelfde manier behandelen aan een object met een Sparse matrix, waarin de index niet aanwezig is.</span><span class="sxs-lookup"><span data-stu-id="2af80-130">If an index is present with a value of `0`, a parser MUST treat the sparse array quantity object identically to a sparse array quantity object in which that index is not present at all.</span></span>


<span data-ttu-id="2af80-131">Een hoeveelheids object moet</span><span class="sxs-lookup"><span data-stu-id="2af80-131">A quantity object MUST either be</span></span>

- <span data-ttu-id="2af80-132">een eenvoudig hoeveelheids object,</span><span class="sxs-lookup"><span data-stu-id="2af80-132">a simple quantity object,</span></span>
- <span data-ttu-id="2af80-133">een begrensd hoeveelheids object, of</span><span class="sxs-lookup"><span data-stu-id="2af80-133">a bounded quantity object, or</span></span>
- <span data-ttu-id="2af80-134">een object met een Sparse matrix.</span><span class="sxs-lookup"><span data-stu-id="2af80-134">a sparse array quantity object.</span></span>


### <a name="examples"></a><span data-ttu-id="2af80-135">Voorbeelden</span><span class="sxs-lookup"><span data-stu-id="2af80-135">Examples</span></span> ###

<span data-ttu-id="2af80-136">Deze sectie is informatieve.</span><span class="sxs-lookup"><span data-stu-id="2af80-136">This section is informative.</span></span>

<span data-ttu-id="2af80-137">Een eenvoudige hoeveelheid voor $1.9844146837 \, \mathrm{ha} $:</span><span class="sxs-lookup"><span data-stu-id="2af80-137">A simple quantity representing $1.9844146837\,\mathrm{Ha}$:</span></span>

```yaml
coulomb_repulsion:
    value: 1.9844146837
    units: hartree
```

<span data-ttu-id="2af80-138">Een grens hoeveelheid die een uniforme distributie vertegenwoordigt voor het interval $ [-7,-6] \, \mathrm{ha} $:</span><span class="sxs-lookup"><span data-stu-id="2af80-138">A bounded quantity representing a uniform distribution over the interval $[-7, -6]\,\mathrm{Ha}$:</span></span>

```yaml
fci_energy:
    upper: -6
    lower: -7
    units: hartree
```

<span data-ttu-id="2af80-139">Hier volgt een Sparse matrix hoeveelheid met een element `[1, 2]` gelijk aan `hello` en een element `[3, 4]` gelijk aan `world` :</span><span class="sxs-lookup"><span data-stu-id="2af80-139">The following is a sparse array quantity with an element `[1, 2]` equal to `hello` and an element `[3, 4]` equal to `world`:</span></span>

```yaml
sparse_example:
    format: sparse
    units: hartree
    values:
    - [1, 2, "hello"]
    - [3, 4, "world"]
```

## <a name="format-section"></a><span data-ttu-id="2af80-140">Indelings sectie</span><span class="sxs-lookup"><span data-stu-id="2af80-140">Format Section</span></span> ##

<span data-ttu-id="2af80-141">Deze sectie is normatieve.</span><span class="sxs-lookup"><span data-stu-id="2af80-141">This section is normative.</span></span>

<span data-ttu-id="2af80-142">Het Broombridge-object moet een eigenschap hebben `format` waarvan de waarde een JSON-object is met een eigenschap met de naam `version` .</span><span class="sxs-lookup"><span data-stu-id="2af80-142">The Broombridge object MUST have a property `format` whose value is a JSON object with one property called `version`.</span></span>
<span data-ttu-id="2af80-143">De `version` eigenschap moet de waarde hebben `"0.1"` .</span><span class="sxs-lookup"><span data-stu-id="2af80-143">The `version` property MUST have the value `"0.1"`.</span></span>

### <a name="example"></a><span data-ttu-id="2af80-144">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="2af80-144">Example</span></span> ###

<span data-ttu-id="2af80-145">Deze sectie is informatieve.</span><span class="sxs-lookup"><span data-stu-id="2af80-145">This section is informative.</span></span>

```yaml
format:                        # required
    version: "0.1"             # must match exactly
```

## <a name="integral-sets-section"></a><span data-ttu-id="2af80-146">Sectie integrale sets</span><span class="sxs-lookup"><span data-stu-id="2af80-146">Integral Sets Section</span></span> ##

<span data-ttu-id="2af80-147">Deze sectie is normatieve.</span><span class="sxs-lookup"><span data-stu-id="2af80-147">This section is normative.</span></span>

<span data-ttu-id="2af80-148">Het Broombridge-object moet een eigenschap hebben `integral_sets` waarvan de waarde een JSON-matrix is.</span><span class="sxs-lookup"><span data-stu-id="2af80-148">The Broombridge object MUST have a property `integral_sets` whose value is a JSON array.</span></span>
<span data-ttu-id="2af80-149">Elk item in de waarde van de `integral_sets` eigenschap moet een JSON-object zijn dat een set integralen beschrijft, zoals beschreven in de rest van deze sectie.</span><span class="sxs-lookup"><span data-stu-id="2af80-149">Each item in the value of the `integral_sets` property MUST be a JSON object describing one set of integrals, as described in the remainder of this section.</span></span>
<span data-ttu-id="2af80-150">In de rest van deze sectie verwijst de term ' integraal set object ' naar een item in de waarde van de `integral_sets` eigenschap van het Broombridge-object.</span><span class="sxs-lookup"><span data-stu-id="2af80-150">In the remainder of this section, the term "integral set object" will refer to an item in the value of the `integral_sets` property of the Broombridge object.</span></span>

<span data-ttu-id="2af80-151">Elk integraal set-object moet een eigenschap hebben `metadata` waarvan de waarde een JSON-object is.</span><span class="sxs-lookup"><span data-stu-id="2af80-151">Each integral set object MUST have a property `metadata` whose value is a JSON object.</span></span>
<span data-ttu-id="2af80-152">De waarde van `metadata` kan het lege JSON-object zijn (dat wil zeggen `{}` ) of kan extra eigenschappen bevatten die zijn gedefinieerd door de implementatie functie.</span><span class="sxs-lookup"><span data-stu-id="2af80-152">The value of `metadata` MAY be the empty JSON object (that is, `{}`), or MAY contain additional properties defined by the implementor.</span></span>

### <a name="hamiltonian-section"></a><span data-ttu-id="2af80-153">De sectie Hamiltonian</span><span class="sxs-lookup"><span data-stu-id="2af80-153">Hamiltonian Section</span></span> ###

#### <a name="overview"></a><span data-ttu-id="2af80-154">Overzicht</span><span class="sxs-lookup"><span data-stu-id="2af80-154">Overview</span></span> ####

<span data-ttu-id="2af80-155">Deze sectie is informatieve.</span><span class="sxs-lookup"><span data-stu-id="2af80-155">This section is informative.</span></span>

<span data-ttu-id="2af80-156">De `hamiltonian` eigenschap van elk integraal set-object beschrijft de Hamiltonian voor een bepaald probleem met de quantum chemie door de termen met één en twee hoofd tekst te vermelden als Sparse matrix met reële getallen.</span><span class="sxs-lookup"><span data-stu-id="2af80-156">The `hamiltonian` property of each integral set object describes the Hamiltonian for a particular quantum chemistry problem by listing out its one- and two-body terms as sparse arrays of real numbers.</span></span>
<span data-ttu-id="2af80-157">De Hamiltonian-Opera tors die door elk integraal set-object worden beschreven, hebben het formulier</span><span class="sxs-lookup"><span data-stu-id="2af80-157">The Hamiltonian operators described by each integral set object take the form</span></span>

<span data-ttu-id="2af80-158">$ $ H = \sum \_ \{ i, j \} \sum \_ {\sigma\in \\ {\uparrow, \downarrow \\ }} H \_ \{ ij \} a ^ \{ \dagger \} \_ {i, \sigma} a \_ {j, \sigma} + \frac {1} {2} \sum \_ \{ i, j, k, l \} \sum \_ {\sigma, \rho\in \\ {\uparrow, \downarrow \\ }} H \_ {ijkl} a ^ \dagger \_ {i, \sigma} a ^ \dagger \_ {k, \rho} a \_ {l, \rho} a \_ {j, \sigma}, $ $</span><span class="sxs-lookup"><span data-stu-id="2af80-158">$$ H = \sum\_\{i,j\}\sum\_{\sigma\in\\{\uparrow,\downarrow\\}} h\_\{ij\} a^\{\dagger\}\_{i,\sigma} a\_{j,\sigma} + \frac{1}{2}\sum\_\{i,j,k,l\}\sum\_{\sigma,\rho\in\\{\uparrow,\downarrow\\}} h\_{ijkl} a^\dagger\_{i,\sigma} a^\dagger\_{k,\rho} a\_{l,\rho} a\_{j,\sigma}, $$</span></span>

<span data-ttu-id="2af80-159">hier $h _ {ijkl} = (IJ | KL) $ in Mulliken Convention.</span><span class="sxs-lookup"><span data-stu-id="2af80-159">here $h_{ijkl}= (ij|kl)$ in Mulliken convention.</span></span>

<span data-ttu-id="2af80-160">Ter duidelijkheid is de term één-elektro periode</span><span class="sxs-lookup"><span data-stu-id="2af80-160">For clarity, the one-electron term is</span></span>

<span data-ttu-id="2af80-161">$ $ h_ {IJ} = \int {\mathrm d} x \psi ^ \* \_ i (x) \left (\frac {1} {2} \nabla ^ 2 + \sum \_ {A} \frac{Z \_ A} {| x-x \_ a |}  \right) \psi \_ j (x), $ $</span><span class="sxs-lookup"><span data-stu-id="2af80-161">$$ h_{ij} = \int {\mathrm d}x \psi^\*\_i(x) \left(\frac{1}{2}\nabla^2 + \sum\_{A}\frac{Z\_A}{|x-x\_A|}  \right) \psi\_j(x), $$</span></span>

<span data-ttu-id="2af80-162">en de twee-elektro periode is</span><span class="sxs-lookup"><span data-stu-id="2af80-162">and the two-electron term is</span></span>

<span data-ttu-id="2af80-163">$ $ h \_ \{ ijkl \} = \iint \{ \mathrm d \} x ^ 2 \psi ^ \{ \* \} \_ i (x \_ 1) \psi \_ j (x \_ 1) \frac \{ 1 \} \{ \| x \_ 1 x \_ 2 \| \} \psi \_ k ^ \{ \* \} (x \_ 2) \psi \_ l (x \_ 2).</span><span class="sxs-lookup"><span data-stu-id="2af80-163">$$ h\_\{ijkl\} = \iint \{\mathrm d\}x^2 \psi^\{\*\}\_i(x\_1)\psi\_j(x\_1) \frac\{1\}\{\|x\_1 -x\_2\|\}\psi\_k^\{\*\}(x\_2) \psi\_l(x\_2).</span></span>
$$

<span data-ttu-id="2af80-164">Zoals vermeld in de beschrijving van de [ `basis_set` eigenschap](#basis-set-object) van elk element van de `integral_sets` eigenschap, gaan we er verder vanuit dat de basis functies worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="2af80-164">As noted in our description of the [`basis_set` property](#basis-set-object) of each element of the `integral_sets` property, we further explicitly assume that the basis functions used are real-valued.</span></span>
<span data-ttu-id="2af80-165">Hierdoor kunnen we de volgende Symmetries gebruiken tussen de voor waarden om de weer gave van de Hamiltonian te comprimeren.</span><span class="sxs-lookup"><span data-stu-id="2af80-165">This allows us to use the following symmetries between the terms to compress the representation of the Hamiltonian.</span></span>

<span data-ttu-id="2af80-166">$ $ h_ {ijkl} = h_ {ijlk} = h_ {jikl} = h_ {jilk} = h_ {klij} = h_ {klji} = h_ {lkij} = h_ {lkji}.</span><span class="sxs-lookup"><span data-stu-id="2af80-166">$$ h_{ijkl} = h_{ijlk}=h_{jikl}=h_{jilk}=h_{klij}=h_{klji}=h_{lkij}=h_{lkji}.</span></span>
$$


#### <a name="contents"></a><span data-ttu-id="2af80-167">Inhoud</span><span class="sxs-lookup"><span data-stu-id="2af80-167">Contents</span></span> ####

<span data-ttu-id="2af80-168">Deze sectie is normatieve.</span><span class="sxs-lookup"><span data-stu-id="2af80-168">This section is normative.</span></span>

<span data-ttu-id="2af80-169">Elke integrale set moet een eigenschap hebben `hamiltonian` waarvan de waarde een JSON-object is.</span><span class="sxs-lookup"><span data-stu-id="2af80-169">Each integral set MUST have a property `hamiltonian` whose value is a JSON object.</span></span>
<span data-ttu-id="2af80-170">De waarde van de `hamiltonian` eigenschap wordt een Hamiltonian-object genoemd en moet de eigenschappen hebben, `one_electron_integrals` `two_electron_integrals` zoals beschreven in de rest van deze sectie.</span><span class="sxs-lookup"><span data-stu-id="2af80-170">The value of the `hamiltonian` property is known as a Hamiltonian object, and MUST have the properties `one_electron_integrals` and `two_electron_integrals` as described in the remainder of this section.</span></span>
<span data-ttu-id="2af80-171">Een Hamiltonian-object kan ook een eigenschap hebben `particle_hole_representation` .</span><span class="sxs-lookup"><span data-stu-id="2af80-171">A Hamiltonian object MAY also have a property `particle_hole_representation`.</span></span>
<span data-ttu-id="2af80-172">Indien aanwezig, de waarde van `particle_hole_representation` moet volgen op de notatie die in de rest van deze sectie wordt beschreven.</span><span class="sxs-lookup"><span data-stu-id="2af80-172">If present, the value of `particle_hole_representation` MUST follow the format described in the remainder of this section.</span></span>

##### <a name="one-electron-integrals-object"></a><span data-ttu-id="2af80-173">Object met één elektron integraal</span><span class="sxs-lookup"><span data-stu-id="2af80-173">One-Electron Integrals Object</span></span> #####

<span data-ttu-id="2af80-174">Deze sectie is normatieve.</span><span class="sxs-lookup"><span data-stu-id="2af80-174">This section is normative.</span></span>

<span data-ttu-id="2af80-175">De `one_electron_integrals` eigenschap van het Hamiltonian-object moet een Sparse matrix zijn waarvan de indices twee gehele getallen zijn en waarvan de waarden getallen zijn.</span><span class="sxs-lookup"><span data-stu-id="2af80-175">The `one_electron_integrals` property of the Hamiltonian object MUST be a sparse array quantity whose indices are two integers and whose values are numbers.</span></span>
<span data-ttu-id="2af80-176">Elke term moet indices bevatten `[i, j]` waarbij `i >= j` .</span><span class="sxs-lookup"><span data-stu-id="2af80-176">Every term MUST have indices `[i, j]` where `i >= j`.</span></span>

> <span data-ttu-id="2af80-177">ERAAN Dit weerspiegelt de symmetrie die $h _ {IJ} = h_ {Ji} $, wat het gevolg is van het feit dat de Hamiltonian Hermitian is.</span><span class="sxs-lookup"><span data-stu-id="2af80-177">[NOTE] This reflects the symmetry that $h_{ij} = h_{ji}$ which is a consequence of the fact that the Hamiltonian is Hermitian.</span></span>


###### <a name="example"></a><span data-ttu-id="2af80-178">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="2af80-178">Example</span></span> ######

<span data-ttu-id="2af80-179">Deze sectie is informatieve.</span><span class="sxs-lookup"><span data-stu-id="2af80-179">This section is informative.</span></span>

<span data-ttu-id="2af80-180">De volgende Sparse matrix vertegenwoordigt de Hamiltonian $ $ H = \left (-5,0 (a ^ \{ \dagger \} \_ {1, \uparrow} a \_ {1, \uparrow} + a ^ \{ \dagger \} \_ {1, \downarrow} a \_ {1, \downarrow}) + 0,17 (a ^ \{ \dagger \} \_ {2, \uparrow} a \_ {1, \uparrow} + a ^ \{ \dagger \} \_ {1, \uparrow} a \_ {2, \uparrow} + a ^ \{ \dagger \} \_ {2, \downarrow} a \_ {1, \downarrow} + a ^ \{ \dagger \} \_ {1, \downarrow} a \_ {2, \downarrow}) \right) \\ , \mathrm{ha}.</span><span class="sxs-lookup"><span data-stu-id="2af80-180">The following sparse array quantity represents the Hamiltonian $$ H = \left(-5.0  (a^\{\dagger\}\_{1,\uparrow} a\_{1,\uparrow}+a^\{\dagger\}\_{1,\downarrow} a\_{1,\downarrow})+ 0.17 (a^\{\dagger\}\_{2,\uparrow} a\_{1,\uparrow}+ a^\{\dagger\}\_{1,\uparrow} a\_{2,\uparrow}+a^\{\dagger\}\_{2,\downarrow} a\_{1,\downarrow}+ a^\{\dagger\}\_{1,\downarrow} a\_{2,\downarrow})\right)\\,\mathrm{Ha}.</span></span>
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
> <span data-ttu-id="2af80-181">Broombridge maakt gebruik van op 1 gebaseerde indexering.</span><span class="sxs-lookup"><span data-stu-id="2af80-181">Broombridge uses 1-based indexing.</span></span>


##### <a name="two-electron-integrals-object"></a><span data-ttu-id="2af80-182">Twee-elektroden integraal object</span><span class="sxs-lookup"><span data-stu-id="2af80-182">Two-Electron Integrals Object</span></span> #####

<span data-ttu-id="2af80-183">Deze sectie is normatieve.</span><span class="sxs-lookup"><span data-stu-id="2af80-183">This section is normative.</span></span>

<span data-ttu-id="2af80-184">De `two_electron_integrals` eigenschap van het Hamiltonian-object moet een Sparse matrix zijn met een extra eigenschap met de naam `index_convention` .</span><span class="sxs-lookup"><span data-stu-id="2af80-184">The `two_electron_integrals` property of the Hamiltonian object MUST be a sparse array quantity with one additional property called `index_convention`.</span></span>
<span data-ttu-id="2af80-185">Elk element van de waarde van `two_electron_integrals` moet vier indexen hebben.</span><span class="sxs-lookup"><span data-stu-id="2af80-185">Each element of the value of `two_electron_integrals` MUST have four indices.</span></span>

<span data-ttu-id="2af80-186">Elke `two_electron_integrals` eigenschap moet een `index_convention` eigenschap hebben.</span><span class="sxs-lookup"><span data-stu-id="2af80-186">Each `two_electron_integrals` property MUST have a `index_convention` property.</span></span>
<span data-ttu-id="2af80-187">De waarde van de `index_convention` eigenschap moet een van de toegestane waarden zijn die worden vermeld in tabel 1.</span><span class="sxs-lookup"><span data-stu-id="2af80-187">The value of the `index_convention` property MUST be one of the allowed values listed in Table 1.</span></span>
<span data-ttu-id="2af80-188">Als de waarde van `index_convention` is `mulliken` , voor elk element van de `two_electron_integrals` Sparse matrix, moet een parser die een Broombridge-document laadt een Hamiltonian-term instantiëren die gelijk is aan de twee-elektroden operator $h _ {i, j, k, l} a ^ \ dagger_i een ^ \ dagger_j a_k a_l $, waarbij $i $, $j $, $k $ en $l $ moet een geheel getal zijn in het inclusieve bereik van 1 tot het aantal electrons dat is opgegeven door de `n_electrons` eigenschap van het set-object Integral en waarbij $h _ {i, j, k, l} $ het element `[i, j, k, l, h(i, j, k, l)]` van de Sparse matrix is.</span><span class="sxs-lookup"><span data-stu-id="2af80-188">If the value of `index_convention` is `mulliken`, then for each element of the `two_electron_integrals` sparse array quantity, a parser loading a Broombridge document MUST instantiate a Hamiltonian term equal to the two-electron operator $h_{i, j, k, l} a^\dagger_i a^\dagger_j a_k a_l$, where $i$, $j$, $k$, and $l$ MUST be integers in the inclusive range from 1 to the number of electrons specified by the `n_electrons` property of the integral set object, and where $h_{i, j, k, l}$ is the element `[i, j, k, l, h(i, j, k, l)]` of the sparse array quantity.</span></span>

###### <a name="symmetries"></a><span data-ttu-id="2af80-189">Symmetries</span><span class="sxs-lookup"><span data-stu-id="2af80-189">Symmetries</span></span> ######

<span data-ttu-id="2af80-190">Deze sectie is normatieve.</span><span class="sxs-lookup"><span data-stu-id="2af80-190">This section is normative.</span></span>

<span data-ttu-id="2af80-191">Als de `index_convention` eigenschap van een `two_electron_integrals` object gelijk is aan `mulliken` en als er een element met indices `[i, j, k, l]` aanwezig is, moeten de volgende indexen niet aanwezig zijn, tenzij ze gelijk zijn aan `[i, j, k, l]` :</span><span class="sxs-lookup"><span data-stu-id="2af80-191">If the `index_convention` property of a `two_electron_integrals` object is equal to `mulliken`, then if an element with indices `[i, j, k, l]` is present, the following indices MUST NOT be present unless they are equal to `[i, j, k, l]`:</span></span>

- `[i, j, l, k]`
- `[j, i, k, l]`
- `[j, i, l, k]`
- `[k, l, i, j]`
- `[k, l, j, i]`
- `[l, k, j, i]`

> [!NOTE]
> <span data-ttu-id="2af80-192">Omdat de `index_convention` eigenschap een object met een sparse hoeveelheid is, kunnen er geen indices worden herhaald op verschillende elementen.</span><span class="sxs-lookup"><span data-stu-id="2af80-192">Because the `index_convention` property is a sparse quantity object, no indices may be repeated on different elements.</span></span>
> <span data-ttu-id="2af80-193">Met name als er een element met indices `[i, j, k, l]` aanwezig is, kan geen ander element deze indexen bevatten.</span><span class="sxs-lookup"><span data-stu-id="2af80-193">In particular, if an element with indices `[i, j, k, l]` is present, no other element may have those indices.</span></span>


<!-- h_{ijkl} = h_{ijlk}=h_{jikl}=h_{jilk}=h_{klij}=h_{klji}=h_{lkji}. -->

###### <a name="example"></a><span data-ttu-id="2af80-194">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="2af80-194">Example</span></span> #######

<span data-ttu-id="2af80-195">Deze sectie is informatieve.</span><span class="sxs-lookup"><span data-stu-id="2af80-195">This section is informative.</span></span>

<span data-ttu-id="2af80-196">Het volgende object geeft de Hamiltonian</span><span class="sxs-lookup"><span data-stu-id="2af80-196">The following object specifies the Hamiltonian</span></span>

<span data-ttu-id="2af80-197">$ $ H = \frac12 \sum \_ {\sigma, \rho\in \\ {\uparrow, \downarrow \\ }} \Biggr (1,6 a ^ {\dagger} \_ {1, \sigma} a ^ {\dagger} \_ {1, \rho} a \_ {1, \rho} a \_ {1, \sigma}-0,1 a ^ {\dagger} \_ {6, \sigma} a ^ {\dagger} \_ {1, \rho} a \_ {3, \rho} a \_ {2, \sigma}-0,1 a ^ {\dagger} \_ {6, \sigma} a ^ {\dagger} \_ {1, \rho} a \_ {2, \rho} a \_ {3, \sigma}-0,1 a ^ {\dagger} \_ {1, \sigma} a ^ {\dagger} \_ {6, \rho} a \_ {3, \rho} a \_ {2, \sigma}-0,1 a ^ {\dagger} \_ {1, \sigma} a ^ {\dagger} \_ {6, \rho} a \_ {2, \rho} a \_ {3, \sigma} $ $ $ $-0,1 a ^ {\dagger} \_ {3, \sigma} a ^ {\dagger} \_ {2, \rho} a \_ {6, \rho} a \_ {1, \sigma}-0,1 a ^ {\dagger} \_ {3, \sigma} a ^ {\dagger} \_ {2, \rho} a \_ {1, \rho} a \_ {6, \sigma}-0,1 a ^ {\dagger} \_ {2, \sigma} a ^ {\dagger} \_ {3 , \rho} a \_ {6, \rho} a \_ {1, \sigma}-0,1 a ^ {\dagger} \_ {2, \sigma} a ^ {\dagger} \_ {3, \rho} a \_ {1, \Rho} a \_ {6, \sigma}\Biggr) \\ , \textrm{ha}.</span><span class="sxs-lookup"><span data-stu-id="2af80-197">$$ H = \frac12 \sum\_{\sigma,\rho\in\\{\uparrow,\downarrow\\}}\Biggr( 1.6 a^{\dagger}\_{1,\sigma} a^{\dagger}\_{1,\rho} a\_{1,\rho} a\_{1,\sigma}- 0.1 a^{\dagger}\_{6,\sigma} a^{\dagger}\_{1,\rho} a\_{3,\rho} a\_{2,\sigma}- 0.1 a^{\dagger}\_{6,\sigma} a^{\dagger}\_{1,\rho} a\_{2,\rho} a\_{3,\sigma}- 0.1 a^{\dagger}\_{1,\sigma} a^{\dagger}\_{6,\rho} a\_{3,\rho} a\_{2,\sigma}- 0.1 a^{\dagger}\_{1,\sigma} a^{\dagger}\_{6,\rho} a\_{2,\rho} a\_{3,\sigma} $$ $$- 0.1 a^{\dagger}\_{3,\sigma} a^{\dagger}\_{2,\rho} a\_{6,\rho} a\_{1,\sigma}- 0.1 a^{\dagger}\_{3,\sigma} a^{\dagger}\_{2,\rho} a\_{1,\rho} a\_{6,\sigma}- 0.1 a^{\dagger}\_{2,\sigma} a^{\dagger}\_{3,\rho} a\_{6,\rho} a\_{1,\sigma}- 0.1 a^{\dagger}\_{2,\sigma} a^{\dagger}\_{3,\rho} a\_{1,\rho} a\_{6,\sigma}\Biggr)\\,\textrm{Ha}.</span></span>
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

##### <a name="particlehole-representation-object"></a><span data-ttu-id="2af80-198">Partikel-object: gat weer geven</span><span class="sxs-lookup"><span data-stu-id="2af80-198">Particle–Hole Representation Object</span></span> #####

<span data-ttu-id="2af80-199">Deze sectie is normatieve.</span><span class="sxs-lookup"><span data-stu-id="2af80-199">This section is normative.</span></span>

<span data-ttu-id="2af80-200">Met het object partikel-gat geeft u op dat de opgeslagen integralen worden gedefinieerd met betrekking tot de weer gave van de opening en Annihilation Opera tors waarin de berekenings operatoren worden beschreven, zoals een Hartree-Fock-status.</span><span class="sxs-lookup"><span data-stu-id="2af80-200">The particle–hole representation object specifies that the integrals stored are defined with respect to particle hole representation wherein the creation and annihilation operators describe excitations away from the reference state used, such as a Hartree–Fock state.</span></span>
<span data-ttu-id="2af80-201">Het object is optioneel.</span><span class="sxs-lookup"><span data-stu-id="2af80-201">The object is OPTIONAL.</span></span>
<span data-ttu-id="2af80-202">Als het object niet is opgegeven, wordt de Hamiltonian geïnterpreteerd als niet gegeven in partikel-hole-weer gave.</span><span class="sxs-lookup"><span data-stu-id="2af80-202">If the object is not specified then the Hamiltonian is to be interpreted as not given in particle-hole representation.</span></span>
<span data-ttu-id="2af80-203">Indien aanwezig, moet de waarde van `particle_hole_representation` een sparse array-hoeveelheid object zijn waarvan de indexen vier gehele getallen zijn en waarvan de waarden een getal en een teken reeks zijn.</span><span class="sxs-lookup"><span data-stu-id="2af80-203">If present, the value of `particle_hole_representation` MUST be a sparse array quantity object whose indices are four integers, and whose values are a number and a string.</span></span>
<span data-ttu-id="2af80-204">Het teken reeks gedeelte van de waarde van elk element mag alleen de tekens bevatten `'+'` en `'-'` geeft aan of een bepaalde factor in de term een aanmaak-of Annihilation-operator is in de weer gave partikel-gat.</span><span class="sxs-lookup"><span data-stu-id="2af80-204">The string portion of the value of each element MUST contain only the characters `'+'` and `'-'` which specifies whether a given factor in the term is a creation or annihilation operator in the particle–hole representation.</span></span>  <span data-ttu-id="2af80-205">Er wordt bijvoorbeeld `"-+++"` gereageerd op een gat dat wordt gemaakt op de site $i $ en de partikels die worden gemaakt op sites $j, k $ en $l $.</span><span class="sxs-lookup"><span data-stu-id="2af80-205">For example `"-+++"` coresponds to a hole being created at site $i$ and particles being created at sites $j,k$ and $l$.</span></span>

> [!NOTE]
> <span data-ttu-id="2af80-206">Als de waarde van het `particle_hole_representation` object een Sparse matrix is, `unit` moeten de `format` Eigenschappen en worden opgegeven.</span><span class="sxs-lookup"><span data-stu-id="2af80-206">As the value of the `particle_hole_representation` is a sparse array quantity object, the `unit` and `format` properties must be specified.</span></span>
> <span data-ttu-id="2af80-207">Acceptabele eenheden zijn opgenomen in tabel 1.</span><span class="sxs-lookup"><span data-stu-id="2af80-207">Acceptable units include are listed in Table 1.</span></span>
> <span data-ttu-id="2af80-208">De `format` eigenschap is vereist en geeft aan of de Hamiltonian coëfficiënten zijn opgegeven als een compacte of Sparse matrix.</span><span class="sxs-lookup"><span data-stu-id="2af80-208">The `format` property is required, and indicates whether the Hamiltonian coefficients are specified as a dense or sparse array.</span></span>
> <span data-ttu-id="2af80-209">In de huidige versie worden alleen sparse matrices ondersteund, met uitleg dat alle niet-opgegeven elementen $0 $ zijn, maar toekomstige versies kunnen ondersteuning toevoegen voor aanvullende waarden van de `format` eigenschap.</span><span class="sxs-lookup"><span data-stu-id="2af80-209">In the current version, only sparse arrays are supported, with interpretation that all unspecified elements are $0$, but future versions may add support for additional values of the `format` property.</span></span>

### <a name="initial-state-section"></a><span data-ttu-id="2af80-210">Eerste status sectie</span><span class="sxs-lookup"><span data-stu-id="2af80-210">Initial State Section</span></span> ###

<span data-ttu-id="2af80-211">Het initial_state_suggestion-object geeft initiële Quantum statussen aan die relevant zijn voor de opgegeven Hamiltonian.</span><span class="sxs-lookup"><span data-stu-id="2af80-211">The initial_state_suggestion object specifies initial quantum states of interest to the specified Hamiltonian.</span></span> <span data-ttu-id="2af80-212">Dit object moet een matrix zijn van JSON- `state` objecten.</span><span class="sxs-lookup"><span data-stu-id="2af80-212">This object must be an array of JSON `state` objects.</span></span>

#### <a name="state-object"></a><span data-ttu-id="2af80-213">Status object</span><span class="sxs-lookup"><span data-stu-id="2af80-213">State object</span></span> ####

<span data-ttu-id="2af80-214">Elke status vertegenwoordigt een superpositie van bezette banen.</span><span class="sxs-lookup"><span data-stu-id="2af80-214">Each states represents a superposition of occupied orbitals.</span></span> <span data-ttu-id="2af80-215">Elk status-object moet een `label` eigenschap hebben die een teken reeks bevat.</span><span class="sxs-lookup"><span data-stu-id="2af80-215">Each state object MUST have a `label` property containing a string.</span></span> <span data-ttu-id="2af80-216">Elk status-object moet een `superposition` eigenschap hebben die een matrix met basis statussen en hun ongebruikelijke amplitudes bevat.</span><span class="sxs-lookup"><span data-stu-id="2af80-216">Each state object MUST have a `superposition` property containing an array of basis states and their unnormalized amplitudes.</span></span>

<span data-ttu-id="2af80-217">Bijvoorbeeld: de initiële statussen $ $ \ket{G0} = \ket{G1} = \ket{G2} = (a ^ {\dagger} \_ {1, \uparrow}a ^ {\dagger} \_ {2, \uparrow}a ^ {\dagger} \_ {2, \downarrow}) \ket {0} $ $ $ $ \ket{E} = \frac{0.1 (a ^ {\dagger} \_ {1, \uparrow}a ^ {\dagger} \_ {2, \uparrow}a ^ {\dagger} \_ {2, \downarrow}) + 0,2 (a ^ {\dagger} \_ {1, \uparrow}a ^ {\dagger} \_ {3, \uparrow}a ^ {\dagger} \_ {2, \downarrow})} {\sqrt{| 0,1 | ^ 2 + | 0,2 | ^ 2}} \ket {0} $ $ worden vertegenwoordigd door</span><span class="sxs-lookup"><span data-stu-id="2af80-217">For example, the initial states $$ \ket{G0}=\ket{G1}=\ket{G2}=(a^{\dagger}\_{1,\uparrow}a^{\dagger}\_{2,\uparrow}a^{\dagger}\_{2,\downarrow})\ket{0} $$ $$ \ket{E}=\frac{0.1 (a^{\dagger}\_{1,\uparrow}a^{\dagger}\_{2,\uparrow}a^{\dagger}\_{2,\downarrow})+0.2 (a^{\dagger}\_{1,\uparrow}a^{\dagger}\_{3,\uparrow}a^{\dagger}\_{2,\downarrow})}{\sqrt{|0.1|^2+|0.2|^2}}\ket{0} $$ are represented by</span></span>
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

#### <a name="basis-set-object"></a><span data-ttu-id="2af80-218">Object basis instellen</span><span class="sxs-lookup"><span data-stu-id="2af80-218">Basis Set Object</span></span> ####

<span data-ttu-id="2af80-219">Deze sectie is normatieve.</span><span class="sxs-lookup"><span data-stu-id="2af80-219">This section is normative.</span></span>

<span data-ttu-id="2af80-220">Elk integraal set-object kan een `basis_set` eigenschap hebben.</span><span class="sxs-lookup"><span data-stu-id="2af80-220">Each integral set object MAY have a `basis_set` property.</span></span>
<span data-ttu-id="2af80-221">Indien aanwezig moet de waarde van de `basis_set` eigenschap een object zijn met twee eigenschappen, `type` en `name` .</span><span class="sxs-lookup"><span data-stu-id="2af80-221">If present, the value of the `basis_set` property MUST be an object with two properties, `type` and `name`.</span></span>

<span data-ttu-id="2af80-222">De basis functies die door de waarde van de `basis_set` eigenschap worden aangegeven, moeten waarden met een echte naam hebben.</span><span class="sxs-lookup"><span data-stu-id="2af80-222">The basis functions identified by the value of the `basis_set` property MUST be real-valued.</span></span>

> [!NOTE]
> <span data-ttu-id="2af80-223">De veronderstelling dat alle basis functies worden gerealiseerd, kan in toekomstige versies van deze specificatie worden versoepeld.</span><span class="sxs-lookup"><span data-stu-id="2af80-223">The assumption that all basis functions are real-valued may be relaxed in future versions of this specification.</span></span>

## <a name="tables-and-lists"></a><span data-ttu-id="2af80-224">Tabellen en lijsten</span><span class="sxs-lookup"><span data-stu-id="2af80-224">Tables and Lists</span></span> ##

### <a name="table-1-allowed-physical-units"></a><span data-ttu-id="2af80-225">Tabel 1.</span><span class="sxs-lookup"><span data-stu-id="2af80-225">Table 1.</span></span> <span data-ttu-id="2af80-226">Toegestane fysieke eenheden</span><span class="sxs-lookup"><span data-stu-id="2af80-226">Allowed Physical Units</span></span> ###

<span data-ttu-id="2af80-227">Deze sectie is normatieve.</span><span class="sxs-lookup"><span data-stu-id="2af80-227">This section is normative.</span></span>

<span data-ttu-id="2af80-228">Een wille keurige teken reeks die een eenheid opgeeft, moet een van de volgende zijn:</span><span class="sxs-lookup"><span data-stu-id="2af80-228">Any string specifying a unit MUST be one of the following:</span></span>

- `hartree`
- `ev`

<span data-ttu-id="2af80-229">Parsers en producenten moeten de volgende eenvoudige hoeveelheids objecten behandelen als gelijkwaardig:</span><span class="sxs-lookup"><span data-stu-id="2af80-229">Parsers and producers MUST treat the following simple quantity objects as equivalent:</span></span>

```yaml
- {"units": "hartree", "value": 1}
- {"units": "ev", "value": 27.2113831301723}
```

### <a name="table-2-allowed-index-conventions"></a><span data-ttu-id="2af80-230">Tabel 2.</span><span class="sxs-lookup"><span data-stu-id="2af80-230">Table 2.</span></span> <span data-ttu-id="2af80-231">Toegestane index conventies</span><span class="sxs-lookup"><span data-stu-id="2af80-231">Allowed Index Conventions</span></span> ###

<span data-ttu-id="2af80-232">Deze sectie is normatieve.</span><span class="sxs-lookup"><span data-stu-id="2af80-232">This section is normative.</span></span>

<span data-ttu-id="2af80-233">Een wille keurige teken reeks die een index Conventie opgeeft, moet een van de volgende zijn:</span><span class="sxs-lookup"><span data-stu-id="2af80-233">Any string specifying an index convention MUST be one of the following:</span></span>

- `mulliken`

<span data-ttu-id="2af80-234">Deze sectie is informatieve.</span><span class="sxs-lookup"><span data-stu-id="2af80-234">This section is informative.</span></span>

<span data-ttu-id="2af80-235">In toekomstige versies van deze specificatie kunnen aanvullende index conventies worden geïntroduceerd.</span><span class="sxs-lookup"><span data-stu-id="2af80-235">Additional index conventions may be introduced in future versions of this specification.</span></span>

#### <a name="interpretation-of-index-conventions"></a><span data-ttu-id="2af80-236">Interpretatie van index conventies</span><span class="sxs-lookup"><span data-stu-id="2af80-236">Interpretation of Index Conventions</span></span> ####

<span data-ttu-id="2af80-237">Deze sectie is informatieve.</span><span class="sxs-lookup"><span data-stu-id="2af80-237">This section is informative.</span></span>
