---
title: Woorden lijst voor Quantum Computing
description: Een woorden lijst met algemene termen, acties en objecten die worden gebruikt in Quantum Computing.
author: QuantumWriter
ms.author: Alan.Geller@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.glossary
ms.openlocfilehash: f47d87f5bc9d677baa12a7ac1581af72894e8a4b
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/28/2020
ms.locfileid: "77909888"
---
# <a name="quantum-computing-glossary"></a>Woorden lijst voor Quantum Computing

|Termijn|Definitie|
|-------------|----------|
|Adjoint|De complex geconjugeerde omzetting van de bewerking. Voor bewerkingen waarbij een unitary-operator wordt geïmplementeerd, is de adjoint de inverse van de bewerking.|
|Aanroep bare|Bewerkingen en functies worden gezamenlijk aangeduid als *callables*.|
|Standard|Bewerkingen en functies die zijn gedefinieerd in Q # Voortbouwend op de logica die is gedefinieerd in de prelude. De implementatie van de standaard bibliotheek is neutraal met betrekking tot doel computers.|
|Clifford-groep|De set bewerkingen die de octants van de Bloch-bol innemen. Dit zijn onder andere: `X`, `Y`, `Z`, `H` en `S`|
|Gelijkrichter|Een Quantum bewerking waarbij een of meer qubits als enablers voor de doel bewerking worden gebruikt.|
|Dirac-notatie|Een steno weergave van Quantum status. Zie de sectie [Dirac Notation](xref:microsoft.quantum.concepts.dirac) (Engelstalig) voor meer informatie.|
|Eigenvalues en Eigenvectors|Zie de [sectie geavanceerde matrix](xref:microsoft.quantum.concepts.matrix-advanced) voor meer informatie.|
|EPR paar|Ook wel bekend als [Bell State](https://en.wikipedia.org/wiki/Bell_state)|
|Evolutie|Hoe de status na verloop van tijd verandert. Zie de sectie over <xref:microsoft.quantum.concepts.matrix-advanced#matrix-exponentials> voor een voor beeld. |
|Functie|Louter klassieke routines in de Q #-taal|
| <a id="global-phase"></a>Globale fase | Twee statussen die identiek zijn aan een veelvoud van een complex getal $e ^ {i\phi} $ zijn bedoeld om te variëren tot een globale fase. In tegens telling tot lokale fasen kunnen globale fasen niet worden waargenomen door middel van enige meting. Zie [Pauli-metingen](xref:microsoft.quantum.concepts.pauli) voor meer informatie. |
|Meting|Een klassieke bit verkrijgen van een Qubit (of set van qubits). Zie de sectie met [Qubit-concepten](xref:microsoft.quantum.concepts.qubit) voor meer informatie.|
|Veranderlijk|Een variabele waarvan de waarde kan worden gewijzigd nadat deze is gemaakt.|
|Naamruimte|Een label voor een verzameling verwante namen (doorgaans bewerkingen, functies en typen). Bijvoorbeeld, de naam ruimte [`Microsoft.Quantum.Preparation`](xref:microsoft.quantum.preparation) labels alle symbolen die in de standaard bibliotheek zijn gedefinieerd en die helpen bij het voorbereiden van initiële statussen.|
|Bewerking|De basis eenheid voor het uitvoeren van quantums in Q #. Het is te vergelijken met een functie in C, C++ of Python, of een statische methode in C# of Java.|
|Operator toepassing|Een Quantum bewerking wordt uitgevoerd. Dit past doorgaans een unitary-matrix toe op de huidige status vector. Zie [Inleiding tot Quantum concepten](xref:microsoft.quantum.concepts.intro) voor meer informatie.|
|Oracle|Een subroutine die gegevens afhankelijke informatie levert aan een Quantum algoritme tijdens runtime. Normaal gesp roken is het doel om een superpositie van uitvoer te bieden die overeenkomt met de invoer die zich in superpositie bevindt.   |
|Gedeeltelijke toepassing|Het aanroepen van een functie of bewerking zonder alle vereiste para meters. Het retourneert een nieuwe aanroep die alleen de ontbrekende para meters vereist tijdens een toekomstige toepassing.|
|Pauli-Opera tors|De `X`, `Y` en `Z` Quantum-poorten.|
|Prelude|De set primitieve en klassieke bewerkingen en functies die zijn gedefinieerd door elke afzonderlijke doel machine, in plaats van op het niveau Q #.|
|Quantum circuit|De representatie van een programma voor een quantum computer. Zie de sectie <xref:microsoft.quantum.concepts.circuits> voor meer informatie.|
|Quantum status|Een weer gave van de qubits in het systeem. Dit wordt meestal aangeduid als een complexe kolom vector. Zie <xref:microsoft.quantum.concepts.vectors> voor meer informatie. |
|Qubit|Eenheid van Quantum opslag. Zie de sectie <xref:microsoft.quantum.concepts.qubit> voor meer informatie.|
|Herhalen-tot-geslaagd|Een Quantum algoritme dat probabilistically slaagt. Als het probleem is opgetreden, wordt de routine opnieuw geprobeerd tot geslaagd (of is er een limiet bereikt). |
|Doel computer|Een compilatie doel dat een abstract Quantum programma verlaagt naar hardware of simulatie. Dit omvat doorgaans herschrijf bewerkingen voor veel doelen, waaronder het vervangen van een Gate, code ring voor fout correctie, geometrische indeling en andere.|
|Kaart|Door komma's gescheiden typen, gegroepeerd per haakje. |
|Door de gebruiker gedefinieerd type|Verzameling van ingebouwde of eerder gedefinieerde typen die als één eenheid kunnen worden aangeduid.|

