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
# <a name="broombridge-specification-v02"></a>Broombridge-specificatie v 0,2 #

De sleutel woorden ' moet ', ' mag niet ', ' vereist ', ' moet ', ' mag niet ', ' moet ', ' mogen ', ' is ', ' mag ' niet ', ' Aanbevolen ' en ' optioneel ' in dit document moeten worden geïnterpreteerd zoals beschreven in [RFC 2119](https://tools.ietf.org/html/rfc2119).

Een terzijde met de koppen ' NOTE ', ' informatie ' of ' waarschuwing ' is informatieve.

## <a name="introduction"></a>Inleiding ##

Deze sectie is informatieve.

Broombridge documenten zijn bedoeld voor het communiceren van exemplaren van simulatie problemen in quantum chemie voor verwerking met de Quantum simulatie en programmeer toolchains.

## <a name="serialization"></a>Serialisatie ##

Deze sectie is normatieve.

Een Broombridge-document moet worden geserialiseerd als een [YAML 1,2-document](http://yaml.org/spec/) dat een JSON-object vertegenwoordigt, zoals beschreven in sectie 2,2 van [RFC 4627](https://tools.ietf.org/html/rfc4627) .
Het object dat is geserialiseerd naar YAML moet een eigenschap hebben `"$schema"` waarvan de waarde `"https://raw.githubusercontent.com/Microsoft/Quantum/master/Chemistry/Schema/qchem-0.2.schema.json"`is, en moet geldig zijn volgens de specificaties van het JSON-schema Draft-06 [[1](https://tools.ietf.org/html/draft-wright-json-schema-01), [2](https://tools.ietf.org/html/draft-wright-json-schema-validation-01)].

Voor de rest van deze specificatie verwijst het object Broombridge naar het JSON-object dat is gedeserialiseerd van een Broombridge YAML-document.

Tenzij anders uitdrukkelijk aangegeven, moeten objecten geen aanvullende eigenschappen hebben die niet expliciet in dit document zijn opgegeven.

## <a name="additional-definitions"></a>Aanvullende definities ##

Deze sectie is normatieve.

### <a name="quantity-objects"></a>Hoeveelheids objecten ###

Deze sectie is normatieve.

Een _hoeveelheids object_ is een JSON-object en moet een eigenschap hebben `units` waarvan de waarde een van de toegestane waarden in tabel 1 is.

Een hoeveelheids object is een _eenvoudig hoeveelheids object_ als het een enkele eigenschap heeft `value` naast de eigenschap `units`.
De waarde van de eigenschap `value` moet een getal zijn.

Een hoeveelheids object is een _begrensd hoeveelheids object_ als het de eigenschappen `lower` heeft en `upper` naast de eigenschap `units`.
De waarden van de eigenschappen `lower` en `upper` moeten getallen zijn.
Een gebonden hoeveelheids object kan een eigenschap hebben `value` waarvan de waarde een getal is.

Een hoeveelheids object is een object met een _Sparse matrix_ als het de eigenschap `format` en een eigenschap `values` bevat naast de eigenschap `units`.
De waarde van `format` moet de teken reeks zijn `sparse`.
De waarde van de eigenschap `values` moet een matrix zijn.
Elk element van `values` moet een matrix zijn die de indices en waarde van de Sparse matrix vertegenwoordigt.

De indexen voor elk element van een object met een Sparse matrix moeten uniek zijn binnen het gehele object voor de Sparse matrix.
Als een index aanwezig is met een waarde van `0`, moet een parser het object voor de Sparse matrix op dezelfde manier behandelen aan een object met een Sparse matrix, waarin de index niet aanwezig is.


Een hoeveelheids object moet

- een eenvoudig hoeveelheids object,
- een begrensd hoeveelheids object, of
- een object met een Sparse matrix.


### <a name="examples"></a>Voorbeelden ###

Deze sectie is informatieve.

Een eenvoudige hoeveelheid voor $1.9844146837\,\mathrm{Ha} $:

```yaml
coulomb_repulsion:
    value: 1.9844146837
    units: hartree
```

Een grens hoeveelheid die een uniforme distributie vertegenwoordigt voor het interval $ [-7,-6]\,\mathrm{Ha} $:

```yaml
fci_energy:
    upper: -6
    lower: -7
    units: hartree
```

Hier volgt een Sparse matrix met een element `[1, 2]` gelijk aan `hello` en een element `[3, 4]` gelijk is aan `world`:

```yaml
sparse_example:
    format: sparse
    units: hartree
    values:
    - [1, 2, "hello"]
    - [3, 4, "world"]
```

## <a name="format-section"></a>Indelings sectie ##

Deze sectie is normatieve.

Het Broombridge-object moet een eigenschap hebben `format` waarvan de waarde een JSON-object is met één eigenschap met de naam `version`.
De eigenschap `version` moet de waarde `"0.2"`hebben.

### <a name="example"></a>Voorbeeld ###

Deze sectie is informatieve.

```yaml
format:                        # required
    version: "0.2"             # must match exactly
```

## <a name="problem-description-section"></a>Sectie probleem beschrijving ##

Deze sectie is normatieve.

Het Broombridge-object moet een eigenschap hebben `problem_description` waarvan de waarde een JSON-matrix is.
Elk item in de waarde van de eigenschap `problem_description` moet een JSON-object zijn dat een set integralen beschrijft, zoals wordt beschreven in de rest van deze sectie.
In de rest van deze sectie wordt met de term ' probleem beschrijving object ' verwezen naar een item in de waarde van de eigenschap `problem_description` van het object Broombridge.

Elk probleem beschrijvings object moet een eigenschap hebben `metadata` waarvan de waarde een JSON-object is.
De waarde van `metadata` kan het lege JSON-object zijn (dat wil zeggen, `{}`) of extra eigenschappen bevatten die zijn gedefinieerd door de-implementatie.

### <a name="hamiltonian-section"></a>De sectie Hamiltonian ###

#### <a name="overview"></a>Overzicht ####

Deze sectie is informatieve.

De eigenschap `hamiltonian` van elk probleem beschrijvings object beschrijft de Hamiltonian voor een bepaald probleem van quantum chemie door de termen van één en twee hoofd tekst te vermelden als Sparse matrix met reële getallen.
De Hamiltonian-Opera tors die door elk probleem beschrijvings object worden beschreven, hebben de vorm

$ $ H = \sum\_\{i, j\}\sum\_{\sigma\in\\{\uparrow, \downarrow\\}} H\_\{IJ\} a ^\{\dagger\}\_{i , \sigma} a\_{j, \sigma} + \frac{1}{2}\sum\_\{i, j, k, l\}\sum\_{\sigma, \rho\in\\{\uparrow, \downarrow\\}} h\_{ijkl} a ^ \dagger\_{i , \sigma} a ^ \dagger\_{k, \rho} a\_{l \rho} a\_{j, \sigma}, $ $

hier $h _ {ijkl} = (IJ | KL) $ in Mulliken Convention.

Ter duidelijkheid is de term één-elektro periode

$ $ h_ {IJ} = \int {\mathrm d} x \psi ^ *\_i (x) \left (\frac{1}{2}\nabla ^ 2 + \sum\_{A} \frac{Z\_A} {| x-x\_A |}  \right) \psi\_j (x), $ $

en de twee-elektro periode is

$ $ h\_\{ijkl\} = \iint \{\mathrm d\}x ^ 2 \psi ^\{\*\}\_i (x\_1) \psi\_j (x\_1) \frac\{1\}\{\|x\_1-x\_2\|\}\psi\_k ^\{\*\}(x\_2) \psi\_l (x\_2).
$$

Zoals vermeld in de beschrijving van de [eigenschap`basis_set`](#basis-set-object) van elk element van de eigenschap `integral_sets`, gaan we er verder vanuit dat de gebruikte basis functies echt waard zijn.
Hierdoor kunnen we de volgende Symmetries gebruiken tussen de voor waarden om de weer gave van de Hamiltonian te comprimeren.

$ $ h_ {ijkl} = h_ {ijlk} = h_ {jikl} = h_ {jilk} = h_ {klij} = h_ {klji} = h_ {lkij} = h_ {lkji}.
$$


#### <a name="contents"></a>Inhoud ####

Deze sectie is normatieve.

Elk probleem beschrijvings object moet een eigenschap hebben `hamiltonian` waarvan de waarde een JSON-object is.
De waarde van de eigenschap `hamiltonian` wordt ook wel een Hamiltonian-object genoemd en moet de eigenschappen `one_electron_integrals` en `two_electron_integrals` hebben, zoals wordt beschreven in de rest van deze sectie.

Elk probleem beschrijvings object moet een eigenschap hebben `coulomb_repulsion` waarvan de waarde een eenvoudig hoeveelheids object is.
Elk probleem beschrijvings object moet een eigenschap hebben `energy_offet` waarvan de waarde een eenvoudig hoeveelheids object is.
> ERAAN De waarden van `coulomb_repulsion` en `energy_offet` samen worden toegevoegd, vastleggen de id-term van de Hamiltonian.

##### <a name="one-electron-integrals-object"></a>Object met één elektron integraal #####

Deze sectie is normatieve.

De eigenschap `one_electron_integrals` van het Hamiltonian-object moet een Sparse-matrix hoeveelheid zijn waarvan de indices twee gehele getallen zijn en waarvan de waarden getallen zijn.
Elke term moet indexen bevatten `[i, j]` waar `i >= j`.

> ERAAN Dit weerspiegelt de symmetrie die $h _ {IJ} = h_ {Ji} $, wat het gevolg is van het feit dat de Hamiltonian Hermitian is.


###### <a name="example"></a>Voorbeeld ######

Deze sectie is informatieve.

De volgende Sparse matrix vertegenwoordigt de Hamiltonian $ $ H = \left (-5,0 (a ^\{\dagger\}\_{1, \uparrow} een\_{1, \uparrow} + a ^\{\dagger\}\_{1, \downarrow} a\_{1 , \downarrow}) + 0,17 (a ^\{\dagger\}\_{2, \uparrow} a\_{1, \uparrow} + a ^\{\dagger\}\_{1, \uparrow} a\_{2, \uparrow} + a ^\{\dagger\}\_{2 , \downarrow} a\_{1, \downarrow} + a ^\{\dagger\}\_{1, \downarrow} a\_{2, \downarrow}) \right)\\, \mathrm{Ha}.
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
> Broombridge maakt gebruik van op 1 gebaseerde indexering.


##### <a name="two-electron-integrals-object"></a>Twee-elektroden integraal object #####

Deze sectie is normatieve.

De eigenschap `two_electron_integrals` van het Hamiltonian-object moet een Sparse matrix zijn met een extra eigenschap met de naam `index_convention`.
Elk element van de waarde van `two_electron_integrals` moet vier indexen hebben.

Elke `two_electron_integrals` eigenschap moet een `index_convention` eigenschap hebben.
De waarde van de eigenschap `index_convention` moet een van de toegestane waarden zijn die worden vermeld in tabel 1.
Als de waarde van `index_convention` is `mulliken`en vervolgens voor elk element van de `two_electron_integrals` Sparse matrix, moet een parser die een Broombridge-document laadt een Hamiltonian-term instantiëren die gelijk is aan de twee-elektroden operator $h _ {i, j, k, l} a ^ \dagger_i a ^ \dagger_j a_k a_l $ , waarbij $i $, $j $, $k $ en $l $ moet een geheel getal zijn met een waarde van ten minste 1 en waarbij $h _ {i, j, k, l} $ het element `[i, j, k, l, h(i, j, k, l)]` van de Sparse matrix is.

###### <a name="symmetries"></a>Symmetries ######

Deze sectie is normatieve.

Als de eigenschap `index_convention` van een `two_electron_integrals` object gelijk is aan `mulliken`en als er een element met indexen `[i, j, k, l]` aanwezig is, mogen de volgende indexen niet aanwezig zijn, tenzij ze gelijk zijn aan `[i, j, k, l]`:

- `[i, j, l, k]`
- `[j, i, k, l]`
- `[j, i, l, k]`
- `[k, l, i, j]`
- `[k, l, j, i]`
- `[l, k, j, i]`

> [!NOTE]
> Omdat de eigenschap `index_convention` een object met een sparse hoeveelheid is, kunnen er geen indices worden herhaald op verschillende elementen.
> Met name als er een element met indexen `[i, j, k, l]` aanwezig is, kan geen ander element deze indexen bevatten.


<!-- h_{ijkl} = h_{ijlk}=h_{jikl}=h_{jilk}=h_{klij}=h_{klji}=h_{lkji}. -->

###### <a name="example"></a>Voorbeeld #######

Deze sectie is informatieve.

Het volgende object geeft de Hamiltonian

$ $ H = \frac12 \sum\_{\sigma, \rho\in\\{\uparrow, \downarrow\\}} \Biggr (1,6 a ^ {\dagger}\_{1, \sigma} a ^ {\dagger}\_{1, \rho} a\_{1, \rho} a\_{1, \sigma}-0,1 a ^ {\dagger}\_{6 , \sigma} a ^ {\dagger}\_{1, \rho} a\_{3 \rho} a\_{2, \sigma}-0,1 a ^ {\dagger}\_{6, \sigma} a ^ {\dagger}\_{1, \rho} a\_{2, \rho} a\_{3 , \sigma}-0,1 a ^ {\dagger}\_{1, \sigma} a ^ {\dagger}\_{6, \rho} a\_{3, \rho} a\_{2, \sigma}-0,1 a ^ {\dagger}\_{1, \sigma} a ^ {\dagger}\_6, \rho} a\_{2 , \rho} a\_{3, \sigma} $ $ $ $-0,1 a ^ {\dagger}\_{3, \sigma} a ^ {\dagger}\_{2, \rho} a\_{6, \rho} a\_{1, \sigma}-0,1 a ^ {\dagger}\_{3, \sigma} a ^ {\dagger}\_{2 , \rho} a\_{1, \rho} a\_{6, \sigma}-0,1 a ^ {\dagger}\_{2, \sigma} a ^ {\dagger}\_{3, \rho} a\_{6, \rho} a\_{1, \sigma}-0,1 a ^ {\dagger}\_{2 , \sigma} a ^ {\dagger}\_{3, \rho} a\_{1 \rho} a\_{6, \sigma}\Biggr)\\, \textrm{Ha}.
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

### <a name="initial-state-section"></a>Eerste status sectie ###

Deze sectie is normatieve.

Het `initial_state_suggestion`-object waarvan de waarde een JSON-matrix is, geeft de initiële Quantum statussen van belang voor de opgegeven Hamiltonian. Elk item in de waarde van de eigenschap `initial_state_suggestion` moet een JSON-object zijn dat één Quantum status beschrijft, zoals beschreven in de rest van deze sectie.
In de rest van deze sectie wordt met de term ' State object ' verwezen naar een item in de waarde van de eigenschap `initial_state_suggestion` van het object Broombridge.

#### <a name="state-object"></a>Status object ####

Deze sectie is normatieve.

Elk status-object moet een `label` eigenschap hebben die een teken reeks bevat. Elk status-object moet een `method` eigenschap hebben. De waarde van de eigenschap `method` moet een van de toegestane waarden zijn die worden weer gegeven in tabel 3.
Elk status-object kan een eigenschap hebben `energy` waarvan de waarde een eenvoudig hoeveelheids object moet zijn.

Als de waarde van de eigenschap `method` is `sparse_multi_configurational`, moet het object State een `superposition`-eigenschap hebben die een matrix met basis statussen en hun ongebruikelijke amplitudes bevat.

Bijvoorbeeld: de initiële statussen $ $ \ket{G0} = \ket{G1} = \ket{G2} = (a ^ {\dagger}\_{1, \uparrow}a ^ {\dagger}\_{2, \uparrow}a ^ {\dagger}\_{2, \downarrow}) \ket{0} $ $ $ $ \ket{E} = \frac{0.1 (a ^ {\dagger}\_{1 , \uparrow}a ^ {\dagger}\_{2, \uparrow}a ^ {\dagger}\_{2, \downarrow}) + 0,2 (a ^ {\dagger}\_{1, \uparrow}a ^ {\dagger}\_{3, \uparrow}a ^ {\dagger}\_{2, \downarrow})} {\sqrt{| 0,1 | ^ 2 + | 0,2 | ^ 2}} \ket{0}, $ $ waarbij $ \ket{E} $ energie $0,987 \textrm{Ha} $ heeft, worden vertegenwoordigd door
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

Als de waarde van de eigenschap `method` is `unitary_coupled_cluster`, moet het object State een `cluster_operator` eigenschap hebben waarvan de waarde een JSON-object is.
Het JSON-object moet een `reference_state` eigenschap hebben waarvan de waarde de basis status is.
Het JSON-object kan een `one_body_amplitudes` eigenschap hebben waarvan de waarde een matrix is van de cluster operators met één body en hun amplitudes.
Het JSON-object kan een `two_body_amplitudes` eigenschap hebben waarvan de waarde bestaat uit een matrix met twee hoofd cluster operators en hun amplitudes.
met een matrix met de basis status en de ongebruikelijke amplitudes.

Bijvoorbeeld: de status $ $ \ket{\Text{Reference}} = (a ^ {\dagger}\_{1, \uparrow}a ^ {\dagger}\_{2, \uparrow}a ^ {\dagger}\_{2, \downarrow}) \ket{0}, $ $

$ $ \ket{\text{UCCSD}} = e ^ {T-T ^ \dagger}\ket{\Text{Reference}}, $ $

$ $ T = 0,1 a ^ {\dagger}\_{3, \uparrow}a\_{2, \downarrow} + 0,2 a ^ {\dagger}\_{2, \uparrow}a\_{2, \downarrow}-0,3 a ^ {\dagger}\_{1, \uparrow}a ^ {\dagger}\_{3, \downarrow}a\_{3 , \uparrow}a\_{2, \downarrow} $ $ wordt vertegenwoordigd door
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

#### <a name="basis-set-object"></a>Object basis instellen ####

Deze sectie is normatieve.

Elk probleem beschrijvings object kan een `basis_set` eigenschap hebben.
Indien aanwezig, moet de waarde van de eigenschap `basis_set` een object zijn met twee eigenschappen, `type` en `name`.

De basis functies die door de waarde van de eigenschap `basis_set` worden aangeduid, moeten waarden met een echte naam hebben.

> [!NOTE]
> De veronderstelling dat alle basis functies worden gerealiseerd, kan in toekomstige versies van deze specificatie worden versoepeld.

## <a name="tables-and-lists"></a>Tabellen en lijsten ##

### <a name="table-1-allowed-physical-units"></a>Tabel 1. Toegestane fysieke eenheden ###

Deze sectie is normatieve.

Een wille keurige teken reeks die een eenheid opgeeft, moet een van de volgende zijn:

- `hartree`
- `ev`

Parsers en producenten moeten de volgende eenvoudige hoeveelheids objecten behandelen als gelijkwaardig:

```yaml
- {"units": "hartree", "value": 1}
- {"units": "ev", "value": 27.2113831301723}
```

### <a name="table-2-allowed-index-conventions"></a>Tabel 2. Toegestane index conventies ###

Deze sectie is normatieve.

Een wille keurige teken reeks die een index Conventie opgeeft, moet een van de volgende zijn:

- `mulliken`

Deze sectie is informatieve.

In toekomstige versies van deze specificatie kunnen aanvullende index conventies worden geïntroduceerd.

#### <a name="interpretation-of-index-conventions"></a>Interpretatie van index conventies ####

Deze sectie is informatieve.

### <a name="table-3-allowed-state-methods"></a>Tabel 3. Toegestane status methoden ###

Deze sectie is normatieve.

Een wille keurige teken reeks die een status methode opgeeft, moet een van de volgende zijn:

- `sparse_multi_configurational`
- `unitary_coupled_cluster`

Deze sectie is informatieve.

In toekomstige versies van deze specificatie kunnen aanvullende status methoden worden geïntroduceerd.