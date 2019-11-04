---
title: 'Q #-technieken-lokale variabelen | Microsoft Docs'
description: 'Q #-technieken-lokale variabelen'
author: QuantumWriter
ms.author: Christopher.Granade@microsoft.com
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: 4f5eff1ee8482fa5e5fee9dff421efab93fc0c5a
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/26/2019
ms.locfileid: "73183281"
---
# <a name="local-variables"></a>Lokale variabelen #

Een waarde van elk type in Q # kan worden toegewezen aan een variabele voor hergebruik in een bewerking of functie met behulp van het sleutel woord `let`.
Bijvoorbeeld:

```qsharp
let measurementOperator = [PauliX, PauliZ, PauliZ, PauliX, PauliI];
```

Hiermee wijst u een bepaalde matrix van Pauli-Opera tors toe aan een variabele met de naam `measurementOperator`.

> [!TIP]
> Houd er rekening mee dat het type van de nieuwe variabele niet expliciet moet worden opgegeven, omdat de expressie aan de rechter kant van de `let` instructie ondubbelzinnig is en het type wordt afgeleid door de compiler. 

Variabelen in Q # kunnen *onveranderbaar*zijn, wat betekent dat wanneer een variabele op deze manier is gedefinieerd, deze niet meer op een wille keurige manier kan worden gewijzigd.
Dit maakt een aantal gunstige optimalisaties mogelijk, waaronder de optimalisatie van de klassieke logica die op variabelen moet worden gerangschikt om de `Adjoint` variant van een bewerking toe te passen.

Variabelen die zijn gedefinieerd met behulp van de `let` binding als hierboven, zijn lokaal voor een bepaald bereik, zoals de hoofd tekst van een bewerking of de inhoud van een `for`-lus.


## <a name="mutability"></a>Veranderlijkheid ##

Als alternatief voor het maken van een variabele met `let`wordt met het sleutel woord `mutable` een speciale onveranderlijke variabele gemaakt die opnieuw kan worden gebonden nadat deze in eerste instantie is gemaakt met behulp van het sleutel woord `set`.

```qsharp
operation RandomInts(maxInt : Int, nrSamples : Int) : Int[] {
    mutable samples = new Int[0];
    for (i in 1 .. nrSamples) {
        set samples += [RandomInt(maxInt)];
    }
    return samples;
}
```

Alle typen in Q #, inclusief matrices, volgen de waarde semantiek. Met name het is niet mogelijk om matrix items bij te werken. Als u een bestaande matrix wilt wijzigen, moet u een methode voor kopiëren en bijwerken gebruiken die vergelijkbaar is met F#die voor records in. Met de bibliotheek hulpprogramma's voor matrices die zijn opgegeven in [`Microsoft.Quantum.Arrays`](xref:microsoft.quantum.arrays), kunt u bijvoorbeeld eenvoudig een functie definiëren die een matrix van PAULIS retourneert waarbij de Pauli bij index `i` de gegeven waarde heeft en alle andere vermeldingen de identiteit zijn: 

```qsharp
function EmbedPauli (pauli : Pauli, i : Int, n : Int) : Pauli[] {
    
    let arr = ConstantArray(n, PauliI); // creates an array of filled with PauliI
    return arr w/ i <- pauli; // constructs a new array based on arr except that entry i is set to pauli
}
```

Meer informatie over het werken met matrices vindt u in het bespreken van Q #-instructies en expressies. 

Veranderlijkheid binnen Q # is een concept dat van toepassing is op een *symbool* in plaats van een type of waarde. In het bijzonder heeft het geen representatie in het type systeem, impliciet of expliciet, en of een binding wordt gewijzigd (zoals aangegeven door het sleutel woord `mutable`) of dat onveranderbaar is (zoals aangegeven door `let`) het type van de afhankelijke variabele (n) niet wijzigt. Dit biedt een belang rijke manier om veranderlijkheid te isoleren in gespecialiseerde functies en bewerkingen.
Met name hoewel een adjoint specialisatie voor een bewerking die gebruikmaakt van een onveranderlijke variabele niet automatisch kan worden gegenereerd, werkt automatisch genereren prima voor een bewerking die een functie aanroept die gebruikmaakt van veranderlijkheid.
Daarom is het een goed idee om functies en bewerkingen te maken waarbij veranderlijkheid zo kort mogelijk en compact worden gebruikt, zodat de rest van het Quantum programma kan worden geschreven met behulp van gewone onveranderlijke variabelen.


## <a name="deconstruction"></a>Ontbouwing ##

Naast het toewijzen van één variabele, de sleutel woorden `let` en `mutable`, of in feite een andere bindings constructie, kunt u ook de inhoud van een tuple- [type](xref:microsoft.quantum.language.type-model#tuple-types)uitpakken.
Een toewijzing van dit formulier wordt genoemd om de elementen van die tuple te *ontconstrueren* .
Als we bijvoorbeeld een term in een Hamiltonian door een tuple model leren, kunnen we de ontbouwing gebruiken om toegang te krijgen tot de verschillende gegevens die we moeten simuleren onder deze term:

```qsharp
// Represents H = 3.1 X_0 Z_1.
let (_, (paulis, idxQubits)) = ((3.1, 1.0), ([PauliX, PauliZ], [0, 1])); // paulis and idxQubits are both immutable variables
mutable ((c1, c2), _) = ((3.1, 1.0), ([PauliX, PauliZ], [0, 1])); // c1 and c2 are both mutable variables
```


