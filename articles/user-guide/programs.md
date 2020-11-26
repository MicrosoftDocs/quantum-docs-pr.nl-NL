---
title: 'Q # introdution'
description: "Snel Inleiding tot Quantum Program ma's in Q #"
author: beheim
ms.author: beheim
ms.date: 11/08/2020
ms.topic: article
uid: microsoft.quantum.guide.programs
ms.openlocfilehash: 975bcda5e0042406b465a83f17f1d2d3f5a1ec4f
ms.sourcegitcommit: b930bb59a1ba8f41d2edc9ed98197109aa8c7f1b
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96233485"
---
# <a name="q-quantum-programming-language"></a>Q # Quantum-programmeer taal

Alles wat u moet weten over de Q # programmeer taal wordt beschreven in de [taal gids q #](xref:microsoft.quantum.qsharp.index). Net als bij iets anders is het [ontwerp proces](https://github.com/microsoft/qsharp-language#q-language-and-core-libraries-design) voor de open source en onze bijdragen.
Zie [Waarom hebben we q # nodig](https://devblogs.microsoft.com/qsharp/why-do-we-need-q/)voor meer achtergrond informatie over de stichtingen en motivaties achter Q #.  
Q # wordt geleverd als onderdeel van de Quantum Development Kit (QDK) voor een kort overzicht, [Wat is de QDK?](xref:microsoft.quantum.overview.q-sharp). 

## <a name="what-is-a-quantum-program"></a>Wat is een Quantum programma?

Een Quantum programma kan worden gezien als een bepaalde set klassieke subroutines die, indien aangeroepen, een berekening uitvoeren door interactie met een Quantum systeem; een programma geschreven in Q # maakt niet rechtstreeks een model van de Quantum status, maar in plaats daarvan wordt beschreven hoe een klassieke controle computer communiceert met qubits.
Op deze manier kunnen we volledig neutraal over wat een Quantum staat, *zelfs op elke* doel computer, die verschillende interpretaties kan hebben, afhankelijk van de computer. 

Een belang rijk gevolg hiervan is dat Q # geen mogelijkheid heeft om rechtstreeks introspect te maken van een Qubit of andere eigenschappen van Quantum monteurs, wat garandeert dat een Q #-programma fysiek kan worden uitgevoerd op een quantum computer.
Een programma kan in plaats daarvan bewerkingen aanroepen zoals [`Measure`](xref:Microsoft.Quantum.Intrinsic.Measure) om klassieke informatie uit een Qubit te halen.

Zodra de toewijzing is toegewezen, kan een Qubit worden door gegeven aan bewerkingen en functies, ook wel *callables* genoemd. In sommige zin is dit alles wat een Q #-programma kan doen met een Qubit. Alle directe acties op de status van een Qubit zijn allemaal gedefinieerd door *intrinsieke* callables, zoals [`X`](xref:Microsoft.Quantum.Intrinsic.X) en [`H`](xref:Microsoft.Quantum.Intrinsic.H) -callables waarvan de implementaties niet zijn gedefinieerd in Q #, maar die in plaats daarvan worden gedefinieerd door de doel computer. Wat deze bewerkingen eigenlijk *doen* , worden alleen concreet gemaakt door de doel computer die we gebruiken om het specifieke Q #-programma uit te voeren.

Als bijvoorbeeld het programma wordt uitgevoerd op onze [volle Simulator](xref:microsoft.quantum.machines.full-state-simulator), voert de Simulator de bijbehorende wiskundige bewerkingen uit op het gesimuleerde Quantum systeem.
Maar in de toekomst kijken, wanneer de doel computer een echte quantum computer is, leidt het aanroepen van dergelijke bewerkingen in Q # ervoor dat de quantum computer de overeenkomstige *real* -bewerkingen op het *echte* Quantum systeem kan uitvoeren (bijvoorbeeld nauw keurig verlopen Laser pulsen).

Een Q #-programma recombineert deze bewerkingen, zoals gedefinieerd door een doel machine, om nieuwe bewerkingen op een hoger niveau te maken voor een snelle Quantum berekening.
Op deze manier maakt Q # het eenvoudig om de logische en hybride Quantum-algoritmen van de logica te expresseren, en is deze ook algemeen wat betreft de structuur van een doel machine of Simulator.

Een eenvoudig voor beeld is het volgende programma, dat één Qubit toewijst in de $ \ket {0} $-status, waarna een Hadamard-bewerking wordt toegepast op het `H` bestand en het resultaat op basis hiervan wordt gemeten `PauliZ` .

```qsharp
@EntryPoint()
operation MeasureOneQubit() : Result {
    // The following using block creates a fresh qubit and initializes it
    // in the |0〉 state.
    using (qubit = Qubit()) {
        // We apply a Hadamard operation H to the state, thereby preparing the
        // state 1 / sqrt(2) (|0〉 + |1〉).
        H(qubit);
        // Now we measure the qubit in Z-basis.
        let result = M(qubit);
        // As the qubit is now in an eigenstate of the measurement operator,
        // we reset the qubit before releasing it.
        if (result == One) { X(qubit); }
        // Finally, we return the result of the measurement.
        return result;
    }
}
```

Onze [Quantum Katas](https://github.com/microsoft/QuantumKatas#introduction) biedt een goede inleiding in de [quantum computing-concepten](https://github.com/microsoft/QuantumKatas#quantum-computing-concepts-qubits-and-gates) , zoals algemene Quantum bewerkingen en het manipuleren van qubits. Meer voor beelden zijn ook te vinden in [intrinsieke bewerkingen en functies](xref:microsoft.quantum.libraries.standard.prelude).



