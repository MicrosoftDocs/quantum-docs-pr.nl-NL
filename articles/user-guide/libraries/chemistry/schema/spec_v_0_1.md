---
title: Broombridge-schema specificatie (ver 0,1)
description: Details van de specificaties voor de Broombridge quantum chemie schema v 0.1 voor de micro soft quantum chemie-bibliotheek.
author: cgranade
ms.author: chgranad
ms.date: 10/17/2018
ms.topic: article
uid: microsoft.quantum.libraries.chemistry.schema.spec_v_0_1
no-loc:
- Q#
- $$v
ms.openlocfilehash: b99c90c434958f7b04712580789b203766cd084d
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/21/2020
ms.locfileid: "90835737"
---
# <a name="broombridge-specification-v01"></a>Broombridge-specificatie v 0.1 #

De sleutel woorden ' moet ', ' mag niet ', ' vereist ', ' moet ', ' mag niet ', ' moet ', ' mogen ', ' is ', ' mag ' niet ', ' Aanbevolen ' en ' optioneel ' in dit document moeten worden geïnterpreteerd zoals beschreven in [RFC 2119](https://tools.ietf.org/html/rfc2119).

Een terzijde met de koppen ' NOTE ', ' informatie ' of ' waarschuwing ' is informatieve.

## <a name="introduction"></a>Inleiding ##

Deze sectie is informatieve.

Broombridge documenten zijn bedoeld voor het communiceren van exemplaren van simulatie problemen in quantum chemie voor verwerking met de Quantum simulatie en programmeer toolchains.

## <a name="serialization"></a>Serialisatie ##

Deze sectie is normatieve.

Een Broombridge-document moet worden geserialiseerd als een [YAML 1,2-document](http://yaml.org/spec/) dat een JSON-object vertegenwoordigt, zoals beschreven in sectie 2,2 van [RFC 4627](https://tools.ietf.org/html/rfc4627) .
Het object dat is geserialiseerd naar YAML moet een eigenschap hebben `"$schema"` waarvan de waarde is `"https://raw.githubusercontent.com/Microsoft/Quantum/master/Chemistry/Schema/qchem-0.1.schema.json"` , en moet geldig zijn volgens de specificatie van het JSON-schema Draft-06 [[1](https://tools.ietf.org/html/draft-wright-json-schema-01), [2](https://tools.ietf.org/html/draft-wright-json-schema-validation-01)].

Voor de rest van deze specificatie verwijst het object Broombridge naar het JSON-object dat is gedeserialiseerd van een Broombridge YAML-document.

Tenzij anders uitdrukkelijk aangegeven, moeten objecten geen aanvullende eigenschappen hebben die niet expliciet in dit document zijn opgegeven.

## <a name="additional-definitions"></a>Aanvullende definities ##

Deze sectie is normatieve.

### <a name="quantity-objects"></a>Hoeveelheids objecten ###

Deze sectie is normatieve.

Een _hoeveelheids object_ is een JSON-object en moet een eigenschap hebben `units` waarvan de waarde een van de toegestane waarden is die worden vermeld in tabel 1.

Een hoeveelheids object is een _eenvoudig hoeveelheids object_ als het een enkele eigenschap heeft `value` naast de bijbehorende `units` eigenschap.
De waarde van de `value` eigenschap moet een getal zijn.

Een hoeveelheids object is een _begrensd hoeveelheids object_ als dit de eigenschappen bevat `lower` en `upper` naast de `units` eigenschap.
De waarden van de `lower` `upper` Eigenschappen en moeten getallen zijn.
Een begrensd hoeveelheids object kan een eigenschap hebben `value` waarvan de waarde een getal is.

Een hoeveelheids object is een object met een _Sparse matrix_ als het de eigenschap `format` en een eigenschap bevat `values` naast de `units` eigenschap.
De waarde van `format` moet de teken reeks zijn `sparse` .
De waarde van de `values` eigenschap moet een matrix zijn.
Elk element van `values` moet een matrix zijn die de indices en waarde van de Sparse matrix vertegenwoordigt.

De indexen voor elk element van een object met een Sparse matrix moeten uniek zijn binnen het gehele object voor de Sparse matrix.
Als een index aanwezig is met een waarde van `0` , moet een parser het object van de Sparse matrix op dezelfde manier behandelen aan een object met een Sparse matrix, waarin de index niet aanwezig is.


Een hoeveelheids object moet

- een eenvoudig hoeveelheids object,
- een begrensd hoeveelheids object, of
- een object met een Sparse matrix.


### <a name="examples"></a>Voorbeelden ###

Deze sectie is informatieve.

Een eenvoudige hoeveelheid voor $1.9844146837 \, \mathrm{ha} $:

```yaml
coulomb_repulsion:
    value: 1.9844146837
    units: hartree
```

Een grens hoeveelheid die een uniforme distributie vertegenwoordigt voor het interval $ [-7,-6] \, \mathrm{ha} $:

```yaml
fci_energy:
    upper: -6
    lower: -7
    units: hartree
```

Hier volgt een Sparse matrix hoeveelheid met een element `[1, 2]` gelijk aan `hello` en een element `[3, 4]` gelijk aan `world` :

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

Het Broombridge-object moet een eigenschap hebben `format` waarvan de waarde een JSON-object is met een eigenschap met de naam `version` .
De `version` eigenschap moet de waarde hebben `"0.1"` .

### <a name="example"></a>Voorbeeld ###

Deze sectie is informatieve.

```yaml
format:                        # required
    version: "0.1"             # must match exactly
```

## <a name="integral-sets-section"></a>Sectie integrale sets ##

Deze sectie is normatieve.

Het Broombridge-object moet een eigenschap hebben `integral_sets` waarvan de waarde een JSON-matrix is.
Elk item in de waarde van de `integral_sets` eigenschap moet een JSON-object zijn dat een set integralen beschrijft, zoals beschreven in de rest van deze sectie.
In de rest van deze sectie verwijst de term ' integraal set object ' naar een item in de waarde van de `integral_sets` eigenschap van het Broombridge-object.

Elk integraal set-object moet een eigenschap hebben `metadata` waarvan de waarde een JSON-object is.
De waarde van `metadata` kan het lege JSON-object zijn (dat wil zeggen `{}` ) of kan extra eigenschappen bevatten die zijn gedefinieerd door de implementatie functie.

### <a name="hamiltonian-section"></a>De sectie Hamiltonian ###

#### <a name="overview"></a>Overzicht ####

Deze sectie is informatieve.

De `hamiltonian` eigenschap van elk integraal set-object beschrijft de Hamiltonian voor een bepaald probleem met de quantum chemie door de termen met één en twee hoofd tekst te vermelden als Sparse matrix met reële getallen.
De Hamiltonian-Opera tors die door elk integraal set-object worden beschreven, hebben het formulier

$ $ H = \sum \_ \{ i, j \} \sum \_ {\sigma\in \\ {\uparrow, \downarrow \\ }} H \_ \{ ij \} a ^ \{ \dagger \} \_ {i, \sigma} a \_ {j, \sigma} + \frac {1} {2} \sum \_ \{ i, j, k, l \} \sum \_ {\sigma, \rho\in \\ {\uparrow, \downarrow \\ }} H \_ {ijkl} a ^ \dagger \_ {i, \sigma} a ^ \dagger \_ {k, \rho} a \_ {l, \rho} a \_ {j, \sigma}, $ $

hier $h _ {ijkl} = (IJ | KL) $ in Mulliken Convention.

Ter duidelijkheid is de term één-elektro periode

$ $ h_ {IJ} = \int {\mathrm d} x \psi ^ * \_ i (x) \left (\frac {1} {2} \nabla ^ 2 + \sum \_ {A} \frac{Z \_ A} {| x-x \_ a |}  \right) \psi \_ j (x), $ $

en de twee-elektro periode is

$ $ h \_ \{ ijkl \} = \iint \{ \mathrm d \} x ^ 2 \psi ^ \{ \* \} \_ i (x \_ 1) \psi \_ j (x \_ 1) \frac \{ 1 \} \{ \| x \_ 1 x \_ 2 \| \} \psi \_ k ^ \{ \* \} (x \_ 2) \psi \_ l (x \_ 2).
$$

Zoals vermeld in de beschrijving van de [ `basis_set` eigenschap](#basis-set-object) van elk element van de `integral_sets` eigenschap, gaan we er verder vanuit dat de basis functies worden gebruikt.
Hierdoor kunnen we de volgende Symmetries gebruiken tussen de voor waarden om de weer gave van de Hamiltonian te comprimeren.

$ $ h_ {ijkl} = h_ {ijlk} = h_ {jikl} = h_ {jilk} = h_ {klij} = h_ {klji} = h_ {lkij} = h_ {lkji}.
$$


#### <a name="contents"></a>Inhoud ####

Deze sectie is normatieve.

Elke integrale set moet een eigenschap hebben `hamiltonian` waarvan de waarde een JSON-object is.
De waarde van de `hamiltonian` eigenschap wordt een Hamiltonian-object genoemd en moet de eigenschappen hebben, `one_electron_integrals` `two_electron_integrals` zoals beschreven in de rest van deze sectie.
Een Hamiltonian-object kan ook een eigenschap hebben `particle_hole_representation` .
Indien aanwezig, de waarde van `particle_hole_representation` moet volgen op de notatie die in de rest van deze sectie wordt beschreven.

##### <a name="one-electron-integrals-object"></a>Object met één elektron integraal #####

Deze sectie is normatieve.

De `one_electron_integrals` eigenschap van het Hamiltonian-object moet een Sparse matrix zijn waarvan de indices twee gehele getallen zijn en waarvan de waarden getallen zijn.
Elke term moet indices bevatten `[i, j]` waarbij `i >= j` .

> ERAAN Dit weerspiegelt de symmetrie die $h _ {IJ} = h_ {Ji} $, wat het gevolg is van het feit dat de Hamiltonian Hermitian is.


###### <a name="example"></a>Voorbeeld ######

Deze sectie is informatieve.

De volgende Sparse matrix vertegenwoordigt de Hamiltonian $ $ H = \left (-5,0 (a ^ \{ \dagger \} \_ {1, \uparrow} a \_ {1, \uparrow} + a ^ \{ \dagger \} \_ {1, \downarrow} a \_ {1, \downarrow}) + 0,17 (a ^ \{ \dagger \} \_ {2, \uparrow} a \_ {1, \uparrow} + a ^ \{ \dagger \} \_ {1, \uparrow} a \_ {2, \uparrow} + a ^ \{ \dagger \} \_ {2, \downarrow} a \_ {1, \downarrow} + a ^ \{ \dagger \} \_ {1, \downarrow} a \_ {2, \downarrow}) \right) \\ , \mathrm{ha}.
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

De `two_electron_integrals` eigenschap van het Hamiltonian-object moet een Sparse matrix zijn met een extra eigenschap met de naam `index_convention` .
Elk element van de waarde van `two_electron_integrals` moet vier indexen hebben.

Elke `two_electron_integrals` eigenschap moet een `index_convention` eigenschap hebben.
De waarde van de `index_convention` eigenschap moet een van de toegestane waarden zijn die worden vermeld in tabel 1.
Als de waarde van `index_convention` is `mulliken` , voor elk element van de `two_electron_integrals` Sparse matrix, moet een parser die een Broombridge-document laadt een Hamiltonian-term instantiëren die gelijk is aan de twee-elektroden operator $h _ {i, j, k, l} a ^ \ dagger_i een ^ \ dagger_j a_k a_l $, waarbij $i $, $j $, $k $ en $l $ moet een geheel getal zijn in het inclusieve bereik van 1 tot het aantal electrons dat is opgegeven door de `n_electrons` eigenschap van het set-object Integral en waarbij $h _ {i, j, k, l} $ het element `[i, j, k, l, h(i, j, k, l)]` van de Sparse matrix is.

###### <a name="symmetries"></a>Symmetries ######

Deze sectie is normatieve.

Als de `index_convention` eigenschap van een `two_electron_integrals` object gelijk is aan `mulliken` en als er een element met indices `[i, j, k, l]` aanwezig is, moeten de volgende indexen niet aanwezig zijn, tenzij ze gelijk zijn aan `[i, j, k, l]` :

- `[i, j, l, k]`
- `[j, i, k, l]`
- `[j, i, l, k]`
- `[k, l, i, j]`
- `[k, l, j, i]`
- `[l, k, j, i]`

> [!NOTE]
> Omdat de `index_convention` eigenschap een object met een sparse hoeveelheid is, kunnen er geen indices worden herhaald op verschillende elementen.
> Met name als er een element met indices `[i, j, k, l]` aanwezig is, kan geen ander element deze indexen bevatten.


<!-- h_{ijkl} = h_{ijlk}=h_{jikl}=h_{jilk}=h_{klij}=h_{klji}=h_{lkji}. -->

###### <a name="example"></a>Voorbeeld #######

Deze sectie is informatieve.

Het volgende object geeft de Hamiltonian

$ $ H = \frac12 \sum \_ {\sigma, \rho\in \\ {\uparrow, \downarrow \\ }} \Biggr (1,6 a ^ {\dagger} \_ {1, \sigma} a ^ {\dagger} \_ {1, \rho} a \_ {1, \rho} a \_ {1, \sigma}-0,1 a ^ {\dagger} \_ {6, \sigma} a ^ {\dagger} \_ {1, \rho} a \_ {3, \rho} a \_ {2, \sigma}-0,1 a ^ {\dagger} \_ {6, \sigma} a ^ {\dagger} \_ {1, \rho} a \_ {2, \rho} a \_ {3, \sigma}-0,1 a ^ {\dagger} \_ {1, \sigma} a ^ {\dagger} \_ {6, \rho} a \_ {3, \rho} a \_ {2, \sigma}-0,1 a ^ {\dagger} \_ {1, \sigma} a ^ {\dagger} \_ {6, \rho} a \_ {2, \rho} a \_ {3, \sigma} $ $ $ $-0,1 a ^ {\dagger} \_ {3, \sigma} a ^ {\dagger} \_ {2, \rho} a \_ {6, \rho} a \_ {1, \sigma}-0,1 a ^ {\dagger} \_ {3, \sigma} a ^ {\dagger} \_ {2, \rho} a \_ {1, \rho} a \_ {6, \sigma}-0,1 a ^ {\dagger} \_ {2, \sigma} a ^ {\dagger} \_ {3 , \rho} a \_ {6, \rho} a \_ {1, \sigma}-0,1 a ^ {\dagger} \_ {2, \sigma} a ^ {\dagger} \_ {3, \rho} a \_ {1, \Rho} a \_ {6, \sigma}\Biggr) \\ , \textrm{ha}.
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

##### <a name="particlehole-representation-object"></a>Partikel-object: gat weer geven #####

Deze sectie is normatieve.

Met het object partikel-gat geeft u op dat de opgeslagen integralen worden gedefinieerd met betrekking tot de weer gave van de opening en Annihilation Opera tors waarin de berekenings operatoren worden beschreven, zoals een Hartree-Fock-status.
Het object is optioneel.
Als het object niet is opgegeven, wordt de Hamiltonian geïnterpreteerd als niet gegeven in partikel-hole-weer gave.
Indien aanwezig, moet de waarde van `particle_hole_representation` een sparse array-hoeveelheid object zijn waarvan de indexen vier gehele getallen zijn en waarvan de waarden een getal en een teken reeks zijn.
Het teken reeks gedeelte van de waarde van elk element mag alleen de tekens bevatten `'+'` en `'-'` geeft aan of een bepaalde factor in de term een aanmaak-of Annihilation-operator is in de weer gave partikel-gat.  Er wordt bijvoorbeeld `"-+++"` gereageerd op een gat dat wordt gemaakt op de site $i $ en de partikels die worden gemaakt op sites $j, k $ en $l $.

> [!NOTE]
> Als de waarde van het `particle_hole_representation` object een Sparse matrix is, `unit` moeten de `format` Eigenschappen en worden opgegeven.
> Acceptabele eenheden zijn opgenomen in tabel 1.
> De `format` eigenschap is vereist en geeft aan of de Hamiltonian coëfficiënten zijn opgegeven als een compacte of Sparse matrix.
> In de huidige versie worden alleen sparse matrices ondersteund, met uitleg dat alle niet-opgegeven elementen $0 $ zijn, maar toekomstige versies kunnen ondersteuning toevoegen voor aanvullende waarden van de `format` eigenschap.

### <a name="initial-state-section"></a>Eerste status sectie ###

Het initial_state_suggestion-object geeft initiële Quantum statussen aan die relevant zijn voor de opgegeven Hamiltonian. Dit object moet een matrix zijn van JSON- `state` objecten.

#### <a name="state-object"></a>Status object ####

Elke status vertegenwoordigt een superpositie van bezette banen. Elk status-object moet een `label` eigenschap hebben die een teken reeks bevat. Elk status-object moet een `superposition` eigenschap hebben die een matrix met basis statussen en hun ongebruikelijke amplitudes bevat.

Bijvoorbeeld: de initiële statussen $ $ \ket{G0} = \ket{G1} = \ket{G2} = (a ^ {\dagger} \_ {1, \uparrow}a ^ {\dagger} \_ {2, \uparrow}a ^ {\dagger} \_ {2, \downarrow}) \ket {0} $ $ $ $ \ket{E} = \frac{0.1 (a ^ {\dagger} \_ {1, \uparrow}a ^ {\dagger} \_ {2, \uparrow}a ^ {\dagger} \_ {2, \downarrow}) + 0,2 (a ^ {\dagger} \_ {1, \uparrow}a ^ {\dagger} \_ {3, \uparrow}a ^ {\dagger} \_ {2, \downarrow})} {\sqrt{| 0,1 | ^ 2 + | 0,2 | ^ 2}} \ket {0} $ $ worden vertegenwoordigd door
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

#### <a name="basis-set-object"></a>Object basis instellen ####

Deze sectie is normatieve.

Elk integraal set-object kan een `basis_set` eigenschap hebben.
Indien aanwezig moet de waarde van de `basis_set` eigenschap een object zijn met twee eigenschappen, `type` en `name` .

De basis functies die door de waarde van de `basis_set` eigenschap worden aangegeven, moeten waarden met een echte naam hebben.

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
