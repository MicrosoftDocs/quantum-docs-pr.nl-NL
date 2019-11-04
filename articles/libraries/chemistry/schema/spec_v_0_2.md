---
title: Broombridge-schema specificatie
author: guanghaolow
ms.author: gulow@microsoft.com
ms.date: 05/28/2019
ms.topic: article
uid: microsoft.quantum.libraries.chemistry.schema.spec_v_0_2
ms.openlocfilehash: 2f4be96bc6f1e8e6fe21b93bc0d9ab2aa367fd53
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/29/2019
ms.locfileid: "73185304"
---
# <a name="broombridge-specification-v02"></a><span data-ttu-id="2e030-102">Broombridge-specificatie v 0,2</span><span class="sxs-lookup"><span data-stu-id="2e030-102">Broombridge Specification v0.2</span></span> #

<span data-ttu-id="2e030-103">De sleutel woorden ' moet ', ' mag niet ', ' vereist ', ' moet ', ' mag niet ', ' moet ', ' mogen ', ' is ', ' mag ' niet ', ' Aanbevolen ' en ' optioneel ' in dit document moeten worden geïnterpreteerd zoals beschreven in [RFC 2119](https://tools.ietf.org/html/rfc2119).</span><span class="sxs-lookup"><span data-stu-id="2e030-103">The key words "MUST", "MUST NOT", "REQUIRED", "SHALL", "SHALL NOT", "SHOULD", "SHOULD NOT", "RECOMMENDED",  "MAY", and "OPTIONAL" in this document are to be interpreted as described in [RFC 2119](https://tools.ietf.org/html/rfc2119).</span></span>

<span data-ttu-id="2e030-104">Een terzijde met de koppen ' NOTE ', ' informatie ' of ' waarschuwing ' is informatieve.</span><span class="sxs-lookup"><span data-stu-id="2e030-104">Any sidebar with the headings "NOTE," "INFORMATION," or "WARNING" is informative.</span></span>

## <a name="introduction"></a><span data-ttu-id="2e030-105">Inleiding</span><span class="sxs-lookup"><span data-stu-id="2e030-105">Introduction</span></span> ##

<span data-ttu-id="2e030-106">Deze sectie is informatieve.</span><span class="sxs-lookup"><span data-stu-id="2e030-106">This section is informative.</span></span>

<span data-ttu-id="2e030-107">Broombridge documenten zijn bedoeld voor het communiceren van exemplaren van simulatie problemen in quantum chemie voor verwerking met de Quantum simulatie en programmeer toolchains.</span><span class="sxs-lookup"><span data-stu-id="2e030-107">Broombridge documents are intended to communicate instances of simulation problems in quantum chemistry for processing using quantum simulation and programming toolchains.</span></span>

## <a name="serialization"></a><span data-ttu-id="2e030-108">Serialisatie</span><span class="sxs-lookup"><span data-stu-id="2e030-108">Serialization</span></span> ##

<span data-ttu-id="2e030-109">Deze sectie is normatieve.</span><span class="sxs-lookup"><span data-stu-id="2e030-109">This section is normative.</span></span>

<span data-ttu-id="2e030-110">Een Broombridge-document moet worden geserialiseerd als een [YAML 1,2-document](http://yaml.org/spec/) dat een JSON-object vertegenwoordigt, zoals beschreven in sectie 2,2 van [RFC 4627](https://tools.ietf.org/html/rfc4627) .</span><span class="sxs-lookup"><span data-stu-id="2e030-110">A Broombridge document MUST be serialized as a [YAML 1.2 document](http://yaml.org/spec/) representing a JSON object as described in [RFC 4627](https://tools.ietf.org/html/rfc4627) section 2.2.</span></span>
<span data-ttu-id="2e030-111">Het object dat is geserialiseerd naar YAML moet een eigenschap hebben `"$schema"` waarvan de waarde `"https://raw.githubusercontent.com/Microsoft/Quantum/master/Chemistry/Schema/qchem-0.2.schema.json"`is, en moet geldig zijn volgens de specificaties van het JSON-schema Draft-06 [[1](https://tools.ietf.org/html/draft-wright-json-schema-01), [2](https://tools.ietf.org/html/draft-wright-json-schema-validation-01)].</span><span class="sxs-lookup"><span data-stu-id="2e030-111">The object serialized to YAML MUST have a property `"$schema"` whose value is `"https://raw.githubusercontent.com/Microsoft/Quantum/master/Chemistry/Schema/qchem-0.2.schema.json"`, and MUST be valid according to the JSON Schema draft-06 specifications [[1](https://tools.ietf.org/html/draft-wright-json-schema-01), [2](https://tools.ietf.org/html/draft-wright-json-schema-validation-01)].</span></span>

<span data-ttu-id="2e030-112">Voor de rest van deze specificatie verwijst het object Broombridge naar het JSON-object dat is gedeserialiseerd van een Broombridge YAML-document.</span><span class="sxs-lookup"><span data-stu-id="2e030-112">For the remainder of this specification, "the Broombridge object" will refer to the JSON object deserialized from a Broombridge YAML document.</span></span>

<span data-ttu-id="2e030-113">Tenzij anders uitdrukkelijk aangegeven, moeten objecten geen aanvullende eigenschappen hebben die niet expliciet in dit document zijn opgegeven.</span><span class="sxs-lookup"><span data-stu-id="2e030-113">Unless otherwise explicitly noted, objects MUST NOT have additional properties beyond those specified explicitly in this document.</span></span>

## <a name="additional-definitions"></a><span data-ttu-id="2e030-114">Aanvullende definities</span><span class="sxs-lookup"><span data-stu-id="2e030-114">Additional Definitions</span></span> ##

<span data-ttu-id="2e030-115">Deze sectie is normatieve.</span><span class="sxs-lookup"><span data-stu-id="2e030-115">This section is normative.</span></span>

### <a name="quantity-objects"></a><span data-ttu-id="2e030-116">Hoeveelheids objecten</span><span class="sxs-lookup"><span data-stu-id="2e030-116">Quantity Objects</span></span> ###

<span data-ttu-id="2e030-117">Deze sectie is normatieve.</span><span class="sxs-lookup"><span data-stu-id="2e030-117">This section is normative.</span></span>

<span data-ttu-id="2e030-118">Een _hoeveelheids object_ is een JSON-object en moet een eigenschap hebben `units` waarvan de waarde een van de toegestane waarden in tabel 1 is.</span><span class="sxs-lookup"><span data-stu-id="2e030-118">A _quantity object_ is a JSON object, and MUST have a property `units` whose value is one of the allowed values listed in Table 1.</span></span>

<span data-ttu-id="2e030-119">Een hoeveelheids object is een _eenvoudig hoeveelheids object_ als het een enkele eigenschap heeft `value` naast de eigenschap `units`.</span><span class="sxs-lookup"><span data-stu-id="2e030-119">A quantity object is a _simple quantity object_ if it has a single property `value` in addition to its `units` property.</span></span>
<span data-ttu-id="2e030-120">De waarde van de eigenschap `value` moet een getal zijn.</span><span class="sxs-lookup"><span data-stu-id="2e030-120">The value of the `value` property MUST be a number.</span></span>

<span data-ttu-id="2e030-121">Een hoeveelheids object is een _begrensd hoeveelheids object_ als het de eigenschappen `lower` heeft en `upper` naast de eigenschap `units`.</span><span class="sxs-lookup"><span data-stu-id="2e030-121">A quantity object is a _bounded quantity object_ if it has the properties `lower` and `upper` in addition to its `units` property.</span></span>
<span data-ttu-id="2e030-122">De waarden van de eigenschappen `lower` en `upper` moeten getallen zijn.</span><span class="sxs-lookup"><span data-stu-id="2e030-122">The values of the `lower` and `upper` properties MUST be numbers.</span></span>
<span data-ttu-id="2e030-123">Een gebonden hoeveelheids object kan een eigenschap hebben `value` waarvan de waarde een getal is.</span><span class="sxs-lookup"><span data-stu-id="2e030-123">A bounded quantity object MAY have a property `value` whose value is a number.</span></span>

<span data-ttu-id="2e030-124">Een hoeveelheids object is een object met een _Sparse matrix_ als het de eigenschap `format` en een eigenschap `values` bevat naast de eigenschap `units`.</span><span class="sxs-lookup"><span data-stu-id="2e030-124">A quantity object is a _sparse array quantity object_ if it has the property `format` and a property `values` in addition to its `units` property.</span></span>
<span data-ttu-id="2e030-125">De waarde van `format` moet de teken reeks zijn `sparse`.</span><span class="sxs-lookup"><span data-stu-id="2e030-125">The value of `format` MUST be the string `sparse`.</span></span>
<span data-ttu-id="2e030-126">De waarde van de eigenschap `values` moet een matrix zijn.</span><span class="sxs-lookup"><span data-stu-id="2e030-126">The value of the `values` property MUST be an array.</span></span>
<span data-ttu-id="2e030-127">Elk element van `values` moet een matrix zijn die de indices en waarde van de Sparse matrix vertegenwoordigt.</span><span class="sxs-lookup"><span data-stu-id="2e030-127">Each element of `values` MUST be an array representing the indices and value of the sparse array quantity.</span></span>

<span data-ttu-id="2e030-128">De indexen voor elk element van een object met een Sparse matrix moeten uniek zijn binnen het gehele object voor de Sparse matrix.</span><span class="sxs-lookup"><span data-stu-id="2e030-128">The indices for each element of a sparse array quantity object MUST be unique across the entire sparse array quantity object.</span></span>
<span data-ttu-id="2e030-129">Als een index aanwezig is met een waarde van `0`, moet een parser het object voor de Sparse matrix op dezelfde manier behandelen aan een object met een Sparse matrix, waarin de index niet aanwezig is.</span><span class="sxs-lookup"><span data-stu-id="2e030-129">If an index is present with a value of `0`, a parser MUST treat the sparse array quantity object identically to a sparse array quantity object in which that index is not present at all.</span></span>


<span data-ttu-id="2e030-130">Een hoeveelheids object moet</span><span class="sxs-lookup"><span data-stu-id="2e030-130">A quantity object MUST either be</span></span>

- <span data-ttu-id="2e030-131">een eenvoudig hoeveelheids object,</span><span class="sxs-lookup"><span data-stu-id="2e030-131">a simple quantity object,</span></span>
- <span data-ttu-id="2e030-132">een begrensd hoeveelheids object, of</span><span class="sxs-lookup"><span data-stu-id="2e030-132">a bounded quantity object, or</span></span>
- <span data-ttu-id="2e030-133">een object met een Sparse matrix.</span><span class="sxs-lookup"><span data-stu-id="2e030-133">a sparse array quantity object.</span></span>


### <a name="examples"></a><span data-ttu-id="2e030-134">Voorbeelden</span><span class="sxs-lookup"><span data-stu-id="2e030-134">Examples</span></span> ###

<span data-ttu-id="2e030-135">Deze sectie is informatieve.</span><span class="sxs-lookup"><span data-stu-id="2e030-135">This section is informative.</span></span>

<span data-ttu-id="2e030-136">Een eenvoudige hoeveelheid voor $1.9844146837\,\mathrm{Ha} $:</span><span class="sxs-lookup"><span data-stu-id="2e030-136">A simple quantity representing $1.9844146837\,\mathrm{Ha}$:</span></span>

```yaml
coulomb_repulsion:
    value: 1.9844146837
    units: hartree
```

<span data-ttu-id="2e030-137">Een grens hoeveelheid die een uniforme distributie vertegenwoordigt voor het interval $ [-7,-6]\,\mathrm{Ha} $:</span><span class="sxs-lookup"><span data-stu-id="2e030-137">A bounded quantity representing a uniform distribution over the interval $[-7, -6]\,\mathrm{Ha}$:</span></span>

```yaml
fci_energy:
    upper: -6
    lower: -7
    units: hartree
```

<span data-ttu-id="2e030-138">Hier volgt een Sparse matrix met een element `[1, 2]` gelijk aan `hello` en een element `[3, 4]` gelijk is aan `world`:</span><span class="sxs-lookup"><span data-stu-id="2e030-138">The following is a sparse array quantity with an element `[1, 2]` equal to `hello` and an element `[3, 4]` equal to `world`:</span></span>

```yaml
sparse_example:
    format: sparse
    units: hartree
    values:
    - [1, 2, "hello"]
    - [3, 4, "world"]
```

## <a name="format-section"></a><span data-ttu-id="2e030-139">Indelings sectie</span><span class="sxs-lookup"><span data-stu-id="2e030-139">Format Section</span></span> ##

<span data-ttu-id="2e030-140">Deze sectie is normatieve.</span><span class="sxs-lookup"><span data-stu-id="2e030-140">This section is normative.</span></span>

<span data-ttu-id="2e030-141">Het Broombridge-object moet een eigenschap hebben `format` waarvan de waarde een JSON-object is met één eigenschap met de naam `version`.</span><span class="sxs-lookup"><span data-stu-id="2e030-141">The Broombridge object MUST have a property `format` whose value is a JSON object with one property called `version`.</span></span>
<span data-ttu-id="2e030-142">De eigenschap `version` moet de waarde `"0.2"`hebben.</span><span class="sxs-lookup"><span data-stu-id="2e030-142">The `version` property MUST have the value `"0.2"`.</span></span>

### <a name="example"></a><span data-ttu-id="2e030-143">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="2e030-143">Example</span></span> ###

<span data-ttu-id="2e030-144">Deze sectie is informatieve.</span><span class="sxs-lookup"><span data-stu-id="2e030-144">This section is informative.</span></span>

```yaml
format:                        # required
    version: "0.2"             # must match exactly
```

## <a name="problem-description-section"></a><span data-ttu-id="2e030-145">Sectie probleem beschrijving</span><span class="sxs-lookup"><span data-stu-id="2e030-145">Problem Description Section</span></span> ##

<span data-ttu-id="2e030-146">Deze sectie is normatieve.</span><span class="sxs-lookup"><span data-stu-id="2e030-146">This section is normative.</span></span>

<span data-ttu-id="2e030-147">Het Broombridge-object moet een eigenschap hebben `problem_description` waarvan de waarde een JSON-matrix is.</span><span class="sxs-lookup"><span data-stu-id="2e030-147">The Broombridge object MUST have a property `problem_description` whose value is a JSON array.</span></span>
<span data-ttu-id="2e030-148">Elk item in de waarde van de eigenschap `problem_description` moet een JSON-object zijn dat een set integralen beschrijft, zoals wordt beschreven in de rest van deze sectie.</span><span class="sxs-lookup"><span data-stu-id="2e030-148">Each item in the value of the `problem_description` property MUST be a JSON object describing one set of integrals, as described in the remainder of this section.</span></span>
<span data-ttu-id="2e030-149">In de rest van deze sectie wordt met de term ' probleem beschrijving object ' verwezen naar een item in de waarde van de eigenschap `problem_description` van het object Broombridge.</span><span class="sxs-lookup"><span data-stu-id="2e030-149">In the remainder of this section, the term "problem description object" will refer to an item in the value of the `problem_description` property of the Broombridge object.</span></span>

<span data-ttu-id="2e030-150">Elk probleem beschrijvings object moet een eigenschap hebben `metadata` waarvan de waarde een JSON-object is.</span><span class="sxs-lookup"><span data-stu-id="2e030-150">Each problem description object MUST have a property `metadata` whose value is a JSON object.</span></span>
<span data-ttu-id="2e030-151">De waarde van `metadata` kan het lege JSON-object zijn (dat wil zeggen, `{}`) of extra eigenschappen bevatten die zijn gedefinieerd door de-implementatie.</span><span class="sxs-lookup"><span data-stu-id="2e030-151">The value of `metadata` MAY be the empty JSON object (that is, `{}`), or MAY contain additional properties defined by the implementor.</span></span>

### <a name="hamiltonian-section"></a><span data-ttu-id="2e030-152">De sectie Hamiltonian</span><span class="sxs-lookup"><span data-stu-id="2e030-152">Hamiltonian Section</span></span> ###

#### <a name="overview"></a><span data-ttu-id="2e030-153">Overzicht</span><span class="sxs-lookup"><span data-stu-id="2e030-153">Overview</span></span> ####

<span data-ttu-id="2e030-154">Deze sectie is informatieve.</span><span class="sxs-lookup"><span data-stu-id="2e030-154">This section is informative.</span></span>

<span data-ttu-id="2e030-155">De eigenschap `hamiltonian` van elk probleem beschrijvings object beschrijft de Hamiltonian voor een bepaald probleem van quantum chemie door de termen van één en twee hoofd tekst te vermelden als Sparse matrix met reële getallen.</span><span class="sxs-lookup"><span data-stu-id="2e030-155">The `hamiltonian` property of each problem description object describes the Hamiltonian for a particular quantum chemistry problem by listing out its one- and two-body terms as sparse arrays of real numbers.</span></span>
<span data-ttu-id="2e030-156">De Hamiltonian-Opera tors die door elk probleem beschrijvings object worden beschreven, hebben de vorm</span><span class="sxs-lookup"><span data-stu-id="2e030-156">The Hamiltonian operators described by each problem description object take the form</span></span>

<span data-ttu-id="2e030-157">$ $ H = \sum\_\{i, j\}\sum\_{\sigma\in\\{\uparrow, \downarrow\\}} H\_\{IJ\} a ^\{\dagger\}\_{i , \sigma} a\_{j, \sigma} + \frac{1}{2}\sum\_\{i, j, k, l\}\sum\_{\sigma, \rho\in\\{\uparrow, \downarrow\\}} h\_{ijkl} a ^ \dagger\_{i , \sigma} a ^ \dagger\_{k, \rho} a\_{l \rho} a\_{j, \sigma}, $ $</span><span class="sxs-lookup"><span data-stu-id="2e030-157">$$ H = \sum\_\{i,j\}\sum\_{\sigma\in\\{\uparrow,\downarrow\\}} h\_\{ij\} a^\{\dagger\}\_{i,\sigma} a\_{j,\sigma} + \frac{1}{2}\sum\_\{i,j,k,l\}\sum\_{\sigma,\rho\in\\{\uparrow,\downarrow\\}} h\_{ijkl} a^\dagger\_{i,\sigma} a^\dagger\_{k,\rho} a\_{l,\rho} a\_{j,\sigma}, $$</span></span>

<span data-ttu-id="2e030-158">hier $h _ {ijkl} = (IJ | KL) $ in Mulliken Convention.</span><span class="sxs-lookup"><span data-stu-id="2e030-158">here $h_{ijkl}= (ij|kl)$ in Mulliken convention.</span></span>

<span data-ttu-id="2e030-159">Ter duidelijkheid is de term één-elektro periode</span><span class="sxs-lookup"><span data-stu-id="2e030-159">For clarity, the one-electron term is</span></span>

<span data-ttu-id="2e030-160">$ $ h_ {IJ} = \int {\mathrm d} x \psi ^ \*\_i (x) \left (\frac{1}{2}\nabla ^ 2 + \sum\_{A} \frac{Z\_A} {| x-x\_A |}  \right) \psi\_j (x), $ $</span><span class="sxs-lookup"><span data-stu-id="2e030-160">$$ h_{ij} = \int {\mathrm d}x \psi^\*\_i(x) \left(\frac{1}{2}\nabla^2 + \sum\_{A}\frac{Z\_A}{|x-x\_A|}  \right) \psi\_j(x), $$</span></span>

<span data-ttu-id="2e030-161">en de twee-elektro periode is</span><span class="sxs-lookup"><span data-stu-id="2e030-161">and the two-electron term is</span></span>

<span data-ttu-id="2e030-162">$ $ h\_\{ijkl\} = \iint \{\mathrm d\}x ^ 2 \psi ^\{\*\}\_i (x\_1) \psi\_j (x\_1) \frac\{1\}\{\|x\_1-x\_2\|\}\psi\_k ^\{\*\}(x\_2) \psi\_l (x\_2).</span><span class="sxs-lookup"><span data-stu-id="2e030-162">$$ h\_\{ijkl\} = \iint \{\mathrm d\}x^2 \psi^\{\*\}\_i(x\_1)\psi\_j(x\_1) \frac\{1\}\{\|x\_1 -x\_2\|\}\psi\_k^\{\*\}(x\_2) \psi\_l(x\_2).</span></span>
$$

<span data-ttu-id="2e030-163">Zoals vermeld in de beschrijving van de [eigenschap`basis_set`](#basis-set-object) van elk element van de eigenschap `integral_sets`, gaan we er verder vanuit dat de gebruikte basis functies echt waard zijn.</span><span class="sxs-lookup"><span data-stu-id="2e030-163">As noted in our description of the [`basis_set` property](#basis-set-object) of each element of the `integral_sets` property, we further explicitly assume that the basis functions used are real-valued.</span></span>
<span data-ttu-id="2e030-164">Hierdoor kunnen we de volgende Symmetries gebruiken tussen de voor waarden om de weer gave van de Hamiltonian te comprimeren.</span><span class="sxs-lookup"><span data-stu-id="2e030-164">This allows us to use the following symmetries between the terms to compress the representation of the Hamiltonian.</span></span>

<span data-ttu-id="2e030-165">$ $ h_ {ijkl} = h_ {ijlk} = h_ {jikl} = h_ {jilk} = h_ {klij} = h_ {klji} = h_ {lkij} = h_ {lkji}.</span><span class="sxs-lookup"><span data-stu-id="2e030-165">$$ h_{ijkl} = h_{ijlk}=h_{jikl}=h_{jilk}=h_{klij}=h_{klji}=h_{lkij}=h_{lkji}.</span></span>
$$


#### <a name="contents"></a><span data-ttu-id="2e030-166">Inhoud</span><span class="sxs-lookup"><span data-stu-id="2e030-166">Contents</span></span> ####

<span data-ttu-id="2e030-167">Deze sectie is normatieve.</span><span class="sxs-lookup"><span data-stu-id="2e030-167">This section is normative.</span></span>

<span data-ttu-id="2e030-168">Elk probleem beschrijvings object moet een eigenschap hebben `hamiltonian` waarvan de waarde een JSON-object is.</span><span class="sxs-lookup"><span data-stu-id="2e030-168">Each problem description object MUST have a property `hamiltonian` whose value is a JSON object.</span></span>
<span data-ttu-id="2e030-169">De waarde van de eigenschap `hamiltonian` wordt ook wel een Hamiltonian-object genoemd en moet de eigenschappen `one_electron_integrals` en `two_electron_integrals` hebben, zoals wordt beschreven in de rest van deze sectie.</span><span class="sxs-lookup"><span data-stu-id="2e030-169">The value of the `hamiltonian` property is known as a Hamiltonian object, and MUST have the properties `one_electron_integrals` and `two_electron_integrals` as described in the remainder of this section.</span></span>

<span data-ttu-id="2e030-170">Elk probleem beschrijvings object moet een eigenschap hebben `coulomb_repulsion` waarvan de waarde een eenvoudig hoeveelheids object is.</span><span class="sxs-lookup"><span data-stu-id="2e030-170">Each problem description object MUST have a property `coulomb_repulsion` whose value is a simple quantity object.</span></span>
<span data-ttu-id="2e030-171">Elk probleem beschrijvings object moet een eigenschap hebben `energy_offet` waarvan de waarde een eenvoudig hoeveelheids object is.</span><span class="sxs-lookup"><span data-stu-id="2e030-171">Each problem description object MUST have a property `energy_offet` whose value is a simple quantity object.</span></span>
> <span data-ttu-id="2e030-172">ERAAN De waarden van `coulomb_repulsion` en `energy_offet` samen worden toegevoegd, vastleggen de id-term van de Hamiltonian.</span><span class="sxs-lookup"><span data-stu-id="2e030-172">[NOTE] The values of `coulomb_repulsion` and `energy_offet` added together capture the identity term of the Hamiltonian.</span></span>

##### <a name="one-electron-integrals-object"></a><span data-ttu-id="2e030-173">Object met één elektron integraal</span><span class="sxs-lookup"><span data-stu-id="2e030-173">One-Electron Integrals Object</span></span> #####

<span data-ttu-id="2e030-174">Deze sectie is normatieve.</span><span class="sxs-lookup"><span data-stu-id="2e030-174">This section is normative.</span></span>

<span data-ttu-id="2e030-175">De eigenschap `one_electron_integrals` van het Hamiltonian-object moet een Sparse-matrix hoeveelheid zijn waarvan de indices twee gehele getallen zijn en waarvan de waarden getallen zijn.</span><span class="sxs-lookup"><span data-stu-id="2e030-175">The `one_electron_integrals` property of the Hamiltonian object MUST be a sparse array quantity whose indices are two integers and whose values are numbers.</span></span>
<span data-ttu-id="2e030-176">Elke term moet indexen bevatten `[i, j]` waar `i >= j`.</span><span class="sxs-lookup"><span data-stu-id="2e030-176">Every term MUST have indices `[i, j]` where `i >= j`.</span></span>

> <span data-ttu-id="2e030-177">ERAAN Dit weerspiegelt de symmetrie die $h _ {IJ} = h_ {Ji} $, wat het gevolg is van het feit dat de Hamiltonian Hermitian is.</span><span class="sxs-lookup"><span data-stu-id="2e030-177">[NOTE] This reflects the symmetry that $h_{ij} = h_{ji}$ which is a consequence of the fact that the Hamiltonian is Hermitian.</span></span>


###### <a name="example"></a><span data-ttu-id="2e030-178">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="2e030-178">Example</span></span> ######

<span data-ttu-id="2e030-179">Deze sectie is informatieve.</span><span class="sxs-lookup"><span data-stu-id="2e030-179">This section is informative.</span></span>

<span data-ttu-id="2e030-180">De volgende Sparse matrix vertegenwoordigt de Hamiltonian $ $ H = \left (-5,0 (a ^\{\dagger\}\_{1, \uparrow} een\_{1, \uparrow} + a ^\{\dagger\}\_{1, \downarrow} a\_{1 , \downarrow}) + 0,17 (a ^\{\dagger\}\_{2, \uparrow} a\_{1, \uparrow} + a ^\{\dagger\}\_{1, \uparrow} a\_{2, \uparrow} + a ^\{\dagger\}\_{2 , \downarrow} a\_{1, \downarrow} + a ^\{\dagger\}\_{1, \downarrow} a\_{2, \downarrow}) \right)\\, \mathrm{Ha}.</span><span class="sxs-lookup"><span data-stu-id="2e030-180">The following sparse array quantity represents the Hamiltonian $$ H = \left(-5.0  (a^\{\dagger\}\_{1,\uparrow} a\_{1,\uparrow}+a^\{\dagger\}\_{1,\downarrow} a\_{1,\downarrow})+ 0.17 (a^\{\dagger\}\_{2,\uparrow} a\_{1,\uparrow}+ a^\{\dagger\}\_{1,\uparrow} a\_{2,\uparrow}+a^\{\dagger\}\_{2,\downarrow} a\_{1,\downarrow}+ a^\{\dagger\}\_{1,\downarrow} a\_{2,\downarrow})\right)\\,\mathrm{Ha}.</span></span>
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
> <span data-ttu-id="2e030-181">Broombridge maakt gebruik van op 1 gebaseerde indexering.</span><span class="sxs-lookup"><span data-stu-id="2e030-181">Broombridge uses 1-based indexing.</span></span>


##### <a name="two-electron-integrals-object"></a><span data-ttu-id="2e030-182">Twee-elektroden integraal object</span><span class="sxs-lookup"><span data-stu-id="2e030-182">Two-Electron Integrals Object</span></span> #####

<span data-ttu-id="2e030-183">Deze sectie is normatieve.</span><span class="sxs-lookup"><span data-stu-id="2e030-183">This section is normative.</span></span>

<span data-ttu-id="2e030-184">De eigenschap `two_electron_integrals` van het Hamiltonian-object moet een Sparse matrix zijn met een extra eigenschap met de naam `index_convention`.</span><span class="sxs-lookup"><span data-stu-id="2e030-184">The `two_electron_integrals` property of the Hamiltonian object MUST be a sparse array quantity with one additional property called `index_convention`.</span></span>
<span data-ttu-id="2e030-185">Elk element van de waarde van `two_electron_integrals` moet vier indexen hebben.</span><span class="sxs-lookup"><span data-stu-id="2e030-185">Each element of the value of `two_electron_integrals` MUST have four indices.</span></span>

<span data-ttu-id="2e030-186">Elke `two_electron_integrals` eigenschap moet een `index_convention` eigenschap hebben.</span><span class="sxs-lookup"><span data-stu-id="2e030-186">Each `two_electron_integrals` property MUST have a `index_convention` property.</span></span>
<span data-ttu-id="2e030-187">De waarde van de eigenschap `index_convention` moet een van de toegestane waarden zijn die worden vermeld in tabel 1.</span><span class="sxs-lookup"><span data-stu-id="2e030-187">The value of the `index_convention` property MUST be one of the allowed values listed in Table 1.</span></span>
<span data-ttu-id="2e030-188">Als de waarde van `index_convention` is `mulliken`en vervolgens voor elk element van de `two_electron_integrals` Sparse matrix, moet een parser die een Broombridge-document laadt een Hamiltonian-term instantiëren die gelijk is aan de twee-elektroden operator $h _ {i, j, k, l} a ^ \dagger_i a ^ \dagger_j a_k a_l $ , waarbij $i $, $j $, $k $ en $l $ moet een geheel getal zijn met een waarde van ten minste 1 en waarbij $h _ {i, j, k, l} $ het element `[i, j, k, l, h(i, j, k, l)]` van de Sparse matrix is.</span><span class="sxs-lookup"><span data-stu-id="2e030-188">If the value of `index_convention` is `mulliken`, then for each element of the `two_electron_integrals` sparse array quantity, a parser loading a Broombridge document MUST instantiate a Hamiltonian term equal to the two-electron operator $h_{i, j, k, l} a^\dagger_i a^\dagger_j a_k a_l$, where $i$, $j$, $k$, and $l$ MUST be integers of value at least 1, and where $h_{i, j, k, l}$ is the element `[i, j, k, l, h(i, j, k, l)]` of the sparse array quantity.</span></span>

###### <a name="symmetries"></a><span data-ttu-id="2e030-189">Symmetries</span><span class="sxs-lookup"><span data-stu-id="2e030-189">Symmetries</span></span> ######

<span data-ttu-id="2e030-190">Deze sectie is normatieve.</span><span class="sxs-lookup"><span data-stu-id="2e030-190">This section is normative.</span></span>

<span data-ttu-id="2e030-191">Als de eigenschap `index_convention` van een `two_electron_integrals` object gelijk is aan `mulliken`en als er een element met indexen `[i, j, k, l]` aanwezig is, mogen de volgende indexen niet aanwezig zijn, tenzij ze gelijk zijn aan `[i, j, k, l]`:</span><span class="sxs-lookup"><span data-stu-id="2e030-191">If the `index_convention` property of a `two_electron_integrals` object is equal to `mulliken`, then if an element with indices `[i, j, k, l]` is present, the following indices MUST NOT be present unless they are equal to `[i, j, k, l]`:</span></span>

- `[i, j, l, k]`
- `[j, i, k, l]`
- `[j, i, l, k]`
- `[k, l, i, j]`
- `[k, l, j, i]`
- `[l, k, j, i]`

> [!NOTE]
> <span data-ttu-id="2e030-192">Omdat de eigenschap `index_convention` een object met een sparse hoeveelheid is, kunnen er geen indices worden herhaald op verschillende elementen.</span><span class="sxs-lookup"><span data-stu-id="2e030-192">Because the `index_convention` property is a sparse quantity object, no indices may be repeated on different elements.</span></span>
> <span data-ttu-id="2e030-193">Met name als er een element met indexen `[i, j, k, l]` aanwezig is, kan geen ander element deze indexen bevatten.</span><span class="sxs-lookup"><span data-stu-id="2e030-193">In particular, if an element with indices `[i, j, k, l]` is present, no other element may have those indices.</span></span>


<!-- h_{ijkl} = h_{ijlk}=h_{jikl}=h_{jilk}=h_{klij}=h_{klji}=h_{lkji}. -->

###### <a name="example"></a><span data-ttu-id="2e030-194">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="2e030-194">Example</span></span> #######

<span data-ttu-id="2e030-195">Deze sectie is informatieve.</span><span class="sxs-lookup"><span data-stu-id="2e030-195">This section is informative.</span></span>

<span data-ttu-id="2e030-196">Het volgende object geeft de Hamiltonian</span><span class="sxs-lookup"><span data-stu-id="2e030-196">The following object specifies the Hamiltonian</span></span>

<span data-ttu-id="2e030-197">$ $ H = \frac12 \sum\_{\sigma, \rho\in\\{\uparrow, \downarrow\\}} \Biggr (1,6 a ^ {\dagger}\_{1, \sigma} a ^ {\dagger}\_{1, \rho} a\_{1, \rho} a\_{1, \sigma}-0,1 a ^ {\dagger}\_{6 , \sigma} a ^ {\dagger}\_{1, \rho} a\_{3 \rho} a\_{2, \sigma}-0,1 a ^ {\dagger}\_{6, \sigma} a ^ {\dagger}\_{1, \rho} a\_{2, \rho} a\_{3 , \sigma}-0,1 a ^ {\dagger}\_{1, \sigma} a ^ {\dagger}\_{6, \rho} a\_{3, \rho} a\_{2, \sigma}-0,1 a ^ {\dagger}\_{1, \sigma} a ^ {\dagger}\_6, \rho} a\_{2 , \rho} a\_{3, \sigma} $ $ $ $-0,1 a ^ {\dagger}\_{3, \sigma} a ^ {\dagger}\_{2, \rho} a\_{6, \rho} a\_{1, \sigma}-0,1 a ^ {\dagger}\_{3, \sigma} a ^ {\dagger}\_{2 , \rho} a\_{1, \rho} a\_{6, \sigma}-0,1 a ^ {\dagger}\_{2, \sigma} a ^ {\dagger}\_{3, \rho} a\_{6, \rho} a\_{1, \sigma}-0,1 a ^ {\dagger}\_{2 , \sigma} a ^ {\dagger}\_{3, \rho} a\_{1 \rho} a\_{6, \sigma}\Biggr)\\, \textrm{Ha}.</span><span class="sxs-lookup"><span data-stu-id="2e030-197">$$ H = \frac12 \sum\_{\sigma,\rho\in\\{\uparrow,\downarrow\\}}\Biggr( 1.6 a^{\dagger}\_{1,\sigma} a^{\dagger}\_{1,\rho} a\_{1,\rho} a\_{1,\sigma}- 0.1 a^{\dagger}\_{6,\sigma} a^{\dagger}\_{1,\rho} a\_{3,\rho} a\_{2,\sigma}- 0.1 a^{\dagger}\_{6,\sigma} a^{\dagger}\_{1,\rho} a\_{2,\rho} a\_{3,\sigma}- 0.1 a^{\dagger}\_{1,\sigma} a^{\dagger}\_{6,\rho} a\_{3,\rho} a\_{2,\sigma}- 0.1 a^{\dagger}\_{1,\sigma} a^{\dagger}\_{6,\rho} a\_{2,\rho} a\_{3,\sigma} $$ $$- 0.1 a^{\dagger}\_{3,\sigma} a^{\dagger}\_{2,\rho} a\_{6,\rho} a\_{1,\sigma}- 0.1 a^{\dagger}\_{3,\sigma} a^{\dagger}\_{2,\rho} a\_{1,\rho} a\_{6,\sigma}- 0.1 a^{\dagger}\_{2,\sigma} a^{\dagger}\_{3,\rho} a\_{6,\rho} a\_{1,\sigma}- 0.1 a^{\dagger}\_{2,\sigma} a^{\dagger}\_{3,\rho} a\_{1,\rho} a\_{6,\sigma}\Biggr)\\,\textrm{Ha}.</span></span>
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

### <a name="initial-state-section"></a><span data-ttu-id="2e030-198">Eerste status sectie</span><span class="sxs-lookup"><span data-stu-id="2e030-198">Initial State Section</span></span> ###

<span data-ttu-id="2e030-199">Deze sectie is normatieve.</span><span class="sxs-lookup"><span data-stu-id="2e030-199">This section is normative.</span></span>

<span data-ttu-id="2e030-200">Het `initial_state_suggestion`-object waarvan de waarde een JSON-matrix is, geeft de initiële Quantum statussen van belang voor de opgegeven Hamiltonian.</span><span class="sxs-lookup"><span data-stu-id="2e030-200">The `initial_state_suggestion` object whose value is a JSON array specifies initial quantum states of interest to the specified Hamiltonian.</span></span> <span data-ttu-id="2e030-201">Elk item in de waarde van de eigenschap `initial_state_suggestion` moet een JSON-object zijn dat één Quantum status beschrijft, zoals beschreven in de rest van deze sectie.</span><span class="sxs-lookup"><span data-stu-id="2e030-201">Each item in the value of the `initial_state_suggestion` property MUST be a JSON object describing one quantum state, as described in the remainder of this section.</span></span>
<span data-ttu-id="2e030-202">In de rest van deze sectie wordt met de term ' State object ' verwezen naar een item in de waarde van de eigenschap `initial_state_suggestion` van het object Broombridge.</span><span class="sxs-lookup"><span data-stu-id="2e030-202">In the remainder of this section, the term "state object" will refer to an item in the value of the `initial_state_suggestion` property of the Broombridge object.</span></span>

#### <a name="state-object"></a><span data-ttu-id="2e030-203">Status object</span><span class="sxs-lookup"><span data-stu-id="2e030-203">State object</span></span> ####

<span data-ttu-id="2e030-204">Deze sectie is normatieve.</span><span class="sxs-lookup"><span data-stu-id="2e030-204">This section is normative.</span></span>

<span data-ttu-id="2e030-205">Elk status-object moet een `label` eigenschap hebben die een teken reeks bevat.</span><span class="sxs-lookup"><span data-stu-id="2e030-205">Each state object MUST have a `label` property containing a string.</span></span> <span data-ttu-id="2e030-206">Elk status-object moet een `method` eigenschap hebben.</span><span class="sxs-lookup"><span data-stu-id="2e030-206">Each state object MUST have a `method` property.</span></span> <span data-ttu-id="2e030-207">De waarde van de eigenschap `method` moet een van de toegestane waarden zijn die worden weer gegeven in tabel 3.</span><span class="sxs-lookup"><span data-stu-id="2e030-207">The value of the `method` property MUST be one of the allowed values listed in Table 3.</span></span>
<span data-ttu-id="2e030-208">Elk status-object kan een eigenschap hebben `energy` waarvan de waarde een eenvoudig hoeveelheids object moet zijn.</span><span class="sxs-lookup"><span data-stu-id="2e030-208">Each state object MAY have a property `energy` whose value MUST be a simple quantity object.</span></span>

<span data-ttu-id="2e030-209">Als de waarde van de eigenschap `method` is `sparse_multi_configurational`, moet het object State een `superposition`-eigenschap hebben die een matrix met basis statussen en hun ongebruikelijke amplitudes bevat.</span><span class="sxs-lookup"><span data-stu-id="2e030-209">If the value of the `method` property is `sparse_multi_configurational`, the state object MUST have a `superposition` property containing an array of basis states and their unnormalized amplitudes.</span></span>

<span data-ttu-id="2e030-210">Bijvoorbeeld: de initiële statussen $ $ \ket{G0} = \ket{G1} = \ket{G2} = (a ^ {\dagger}\_{1, \uparrow}a ^ {\dagger}\_{2, \uparrow}a ^ {\dagger}\_{2, \downarrow}) \ket{0} $ $ $ $ \ket{E} = \frac{0.1 (a ^ {\dagger}\_{1 , \uparrow}a ^ {\dagger}\_{2, \uparrow}a ^ {\dagger}\_{2, \downarrow}) + 0,2 (a ^ {\dagger}\_{1, \uparrow}a ^ {\dagger}\_{3, \uparrow}a ^ {\dagger}\_{2, \downarrow})} {\sqrt{| 0,1 | ^ 2 + | 0,2 | ^ 2}} \ket{0}, $ $ waarbij $ \ket{E} $ energie $0,987 \textrm{Ha} $ heeft, worden vertegenwoordigd door</span><span class="sxs-lookup"><span data-stu-id="2e030-210">For example, the initial states $$ \ket{G0}=\ket{G1}=\ket{G2}=(a^{\dagger}\_{1,\uparrow}a^{\dagger}\_{2,\uparrow}a^{\dagger}\_{2,\downarrow})\ket{0} $$ $$ \ket{E}=\frac{0.1 (a^{\dagger}\_{1,\uparrow}a^{\dagger}\_{2,\uparrow}a^{\dagger}\_{2,\downarrow})+0.2 (a^{\dagger}\_{1,\uparrow}a^{\dagger}\_{3,\uparrow}a^{\dagger}\_{2,\downarrow})}{\sqrt{|0.1|^2+|0.2|^2}}\ket{0}, $$ where $\ket{E}$ has energy $0.987 \textrm{Ha}$, are represented by</span></span>
```yaml
initial_state_suggestions: # optional. If not provided, spin-orbitals will be filled to minimize one-body diagonal term energies.
  - label: "|G0>"
    method: sparse_multi_configurational
    superposition:
      - [1.0, "(1a)+","(2a)+","(2b)+","|vacuum>"]
  - label: "|G1>"
    method: sparse_multi_configurational
    superposition:
      - [-1.0, "(2a)+","(1a)+","(2b)+","|vacuum>"]
  - label: "|G2>"
    method: sparse_multi_configurational
    superposition:
      - [1.0, "(3a)","(1a)+","(2a)+","(3a)+","(2b)+","|vacuum>"]
  - label: "|E>"
    energy: {units: hartree, value: 0.987}
    method: sparse_multi_configurational
    superposition:
      - [0.1, "(1a)+","(2a)+","(2b)+","|vacuum>"]
      - [0.2, "(1a)+","(3a)+","(2b)+","|vacuum>"]
```

<span data-ttu-id="2e030-211">Als de waarde van de eigenschap `method` is `unitary_coupled_cluster`, moet het object State een `cluster_operator` eigenschap hebben waarvan de waarde een JSON-object is.</span><span class="sxs-lookup"><span data-stu-id="2e030-211">If the value of the `method` property is `unitary_coupled_cluster`, the state object MUST have a `cluster_operator` property whose value is a JSON object.</span></span>
<span data-ttu-id="2e030-212">Het JSON-object moet een `reference_state` eigenschap hebben waarvan de waarde de basis status is.</span><span class="sxs-lookup"><span data-stu-id="2e030-212">The JSON object MUST have a `reference_state` property whose value is a basis state.</span></span>
<span data-ttu-id="2e030-213">Het JSON-object kan een `one_body_amplitudes` eigenschap hebben waarvan de waarde een matrix is van de cluster operators met één body en hun amplitudes.</span><span class="sxs-lookup"><span data-stu-id="2e030-213">The JSON object MAY have a `one_body_amplitudes` property whose value is an array of one-body cluster operators and their amplitudes.</span></span>
<span data-ttu-id="2e030-214">Het JSON-object kan een `two_body_amplitudes` eigenschap hebben waarvan de waarde bestaat uit een matrix met twee hoofd cluster operators en hun amplitudes.</span><span class="sxs-lookup"><span data-stu-id="2e030-214">The JSON object MAY have a `two_body_amplitudes` property whose value is an array of two-body cluster operators and their amplitudes.</span></span>
<span data-ttu-id="2e030-215">met een matrix met de basis status en de ongebruikelijke amplitudes.</span><span class="sxs-lookup"><span data-stu-id="2e030-215">containing an array of basis states and their unnormalized amplitudes.</span></span>

<span data-ttu-id="2e030-216">Bijvoorbeeld: de status $ $ \ket{\Text{Reference}} = (a ^ {\dagger}\_{1, \uparrow}a ^ {\dagger}\_{2, \uparrow}a ^ {\dagger}\_{2, \downarrow}) \ket{0}, $ $</span><span class="sxs-lookup"><span data-stu-id="2e030-216">For example, the state $$ \ket{\text{reference}}=(a^{\dagger}\_{1,\uparrow}a^{\dagger}\_{2,\uparrow}a^{\dagger}\_{2,\downarrow})\ket{0}, $$</span></span>

<span data-ttu-id="2e030-217">$ $ \ket{\text{UCCSD}} = e ^ {T-T ^ \dagger}\ket{\Text{Reference}}, $ $</span><span class="sxs-lookup"><span data-stu-id="2e030-217">$$ \ket{\text{UCCSD}}=e^{T-T^\dagger}\ket{\text{reference}}, $$</span></span>

<span data-ttu-id="2e030-218">$ $ T = 0,1 a ^ {\dagger}\_{3, \uparrow}a\_{2, \downarrow} + 0,2 a ^ {\dagger}\_{2, \uparrow}a\_{2, \downarrow}-0,3 a ^ {\dagger}\_{1, \uparrow}a ^ {\dagger}\_{3, \downarrow}a\_{3 , \uparrow}a\_{2, \downarrow} $ $ wordt vertegenwoordigd door</span><span class="sxs-lookup"><span data-stu-id="2e030-218">$$ T = 0.1 a^{\dagger}\_{3,\uparrow}a\_{2,\downarrow} + 0.2 a^{\dagger}\_{2,\uparrow}a\_{2,\downarrow} - 0.3 a^{\dagger}\_{1,\uparrow}a^{\dagger}\_{3,\downarrow}a\_{3,\uparrow}a\_{2,\downarrow} $$ is represented by</span></span>
```yaml
initial_state_suggestions: # optional. If not provided, spin-orbitals will be filled to minimize one-body diagonal term energies.
  - label: "UCCSD"
    method: unitary_coupled_cluster
    cluster_operator: # Initial state that cluster operator is applied to.
        reference_state: 
          [1.0, "(1a)+", "(2a)+", "(2b)+", '|vacuum>']
        one_body_amplitudes: # A one-body cluster term is t^{q}_{p} a^\dag_p a_q   
            - [0.1, "(3a)+", "(2b)"]
            - [-0.2, "(2a)+", "(2b)"]
        two_body_amplitudes: # A two-body unitary cluster term is t^{rs}_{pq} a^\dag_p a^\dag_q a_r a_s
            - [-0.3, "(1a)+", "(3b)+", "(3a)", "(2b)"]
```

#### <a name="basis-set-object"></a><span data-ttu-id="2e030-219">Object basis instellen</span><span class="sxs-lookup"><span data-stu-id="2e030-219">Basis Set Object</span></span> ####

<span data-ttu-id="2e030-220">Deze sectie is normatieve.</span><span class="sxs-lookup"><span data-stu-id="2e030-220">This section is normative.</span></span>

<span data-ttu-id="2e030-221">Elk probleem beschrijvings object kan een `basis_set` eigenschap hebben.</span><span class="sxs-lookup"><span data-stu-id="2e030-221">Each problem description object MAY have a `basis_set` property.</span></span>
<span data-ttu-id="2e030-222">Indien aanwezig, moet de waarde van de eigenschap `basis_set` een object zijn met twee eigenschappen, `type` en `name`.</span><span class="sxs-lookup"><span data-stu-id="2e030-222">If present, the value of the `basis_set` property MUST be an object with two properties, `type` and `name`.</span></span>

<span data-ttu-id="2e030-223">De basis functies die door de waarde van de eigenschap `basis_set` worden aangeduid, moeten waarden met een echte naam hebben.</span><span class="sxs-lookup"><span data-stu-id="2e030-223">The basis functions identified by the value of the `basis_set` property MUST be real-valued.</span></span>

> [!NOTE]
> <span data-ttu-id="2e030-224">De veronderstelling dat alle basis functies worden gerealiseerd, kan in toekomstige versies van deze specificatie worden versoepeld.</span><span class="sxs-lookup"><span data-stu-id="2e030-224">The assumption that all basis functions are real-valued may be relaxed in future versions of this specification.</span></span>

## <a name="tables-and-lists"></a><span data-ttu-id="2e030-225">Tabellen en lijsten</span><span class="sxs-lookup"><span data-stu-id="2e030-225">Tables and Lists</span></span> ##

### <a name="table-1-allowed-physical-units"></a><span data-ttu-id="2e030-226">Tabel 1.</span><span class="sxs-lookup"><span data-stu-id="2e030-226">Table 1.</span></span> <span data-ttu-id="2e030-227">Toegestane fysieke eenheden</span><span class="sxs-lookup"><span data-stu-id="2e030-227">Allowed Physical Units</span></span> ###

<span data-ttu-id="2e030-228">Deze sectie is normatieve.</span><span class="sxs-lookup"><span data-stu-id="2e030-228">This section is normative.</span></span>

<span data-ttu-id="2e030-229">Een wille keurige teken reeks die een eenheid opgeeft, moet een van de volgende zijn:</span><span class="sxs-lookup"><span data-stu-id="2e030-229">Any string specifying a unit MUST be one of the following:</span></span>

- `hartree`
- `ev`

<span data-ttu-id="2e030-230">Parsers en producenten moeten de volgende eenvoudige hoeveelheids objecten behandelen als gelijkwaardig:</span><span class="sxs-lookup"><span data-stu-id="2e030-230">Parsers and producers MUST treat the following simple quantity objects as equivalent:</span></span>

```yaml
- {"units": "hartree", "value": 1}
- {"units": "ev", "value": 27.2113831301723}
```

### <a name="table-2-allowed-index-conventions"></a><span data-ttu-id="2e030-231">Tabel 2.</span><span class="sxs-lookup"><span data-stu-id="2e030-231">Table 2.</span></span> <span data-ttu-id="2e030-232">Toegestane index conventies</span><span class="sxs-lookup"><span data-stu-id="2e030-232">Allowed Index Conventions</span></span> ###

<span data-ttu-id="2e030-233">Deze sectie is normatieve.</span><span class="sxs-lookup"><span data-stu-id="2e030-233">This section is normative.</span></span>

<span data-ttu-id="2e030-234">Een wille keurige teken reeks die een index Conventie opgeeft, moet een van de volgende zijn:</span><span class="sxs-lookup"><span data-stu-id="2e030-234">Any string specifying an index convention MUST be one of the following:</span></span>

- `mulliken`

<span data-ttu-id="2e030-235">Deze sectie is informatieve.</span><span class="sxs-lookup"><span data-stu-id="2e030-235">This section is informative.</span></span>

<span data-ttu-id="2e030-236">In toekomstige versies van deze specificatie kunnen aanvullende index conventies worden geïntroduceerd.</span><span class="sxs-lookup"><span data-stu-id="2e030-236">Additional index conventions may be introduced in future versions of this specification.</span></span>

#### <a name="interpretation-of-index-conventions"></a><span data-ttu-id="2e030-237">Interpretatie van index conventies</span><span class="sxs-lookup"><span data-stu-id="2e030-237">Interpretation of Index Conventions</span></span> ####

<span data-ttu-id="2e030-238">Deze sectie is informatieve.</span><span class="sxs-lookup"><span data-stu-id="2e030-238">This section is informative.</span></span>

### <a name="table-3-allowed-state-methods"></a><span data-ttu-id="2e030-239">Tabel 3.</span><span class="sxs-lookup"><span data-stu-id="2e030-239">Table 3.</span></span> <span data-ttu-id="2e030-240">Toegestane status methoden</span><span class="sxs-lookup"><span data-stu-id="2e030-240">Allowed State methods</span></span> ###

<span data-ttu-id="2e030-241">Deze sectie is normatieve.</span><span class="sxs-lookup"><span data-stu-id="2e030-241">This section is normative.</span></span>

<span data-ttu-id="2e030-242">Een wille keurige teken reeks die een status methode opgeeft, moet een van de volgende zijn:</span><span class="sxs-lookup"><span data-stu-id="2e030-242">Any string specifying a state method MUST be one of the following:</span></span>

- `sparse_multi_configurational`
- `unitary_coupled_cluster`

<span data-ttu-id="2e030-243">Deze sectie is informatieve.</span><span class="sxs-lookup"><span data-stu-id="2e030-243">This section is informative.</span></span>

<span data-ttu-id="2e030-244">In toekomstige versies van deze specificatie kunnen aanvullende status methoden worden geïntroduceerd.</span><span class="sxs-lookup"><span data-stu-id="2e030-244">Additional state methods may be introduced in future versions of this specification.</span></span>
