---
title: 'Fout correctie in de Q # standaard-bibliotheken'
description: "Meer informatie over het gebruik van fout correctie codes in uw Q #-Program ma's terwijl u de status van de qubits beveiligt."
author: QuantumWriter
uid: microsoft.quantum.libraries.error-correction
ms.author: martinro@microsoft.com
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: 514fe68f603b9a3a0b4607390719b08a43fe4967
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/28/2020
ms.locfileid: "77907763"
---
# <a name="error-correction"></a>Fout correctie #

## <a name="introduction"></a>Inleiding ##

Als er in klassieke computing een beetje op fouten wil beveiligen, kan het vaak voldoende zijn om die bit te vertegenwoordigen door een *logische bit* door de gegevensbits te herhalen.
Laat bijvoorbeeld $ \overline{0} = $0 de code ring van de gegevensbit 0 zijn, waarbij we de regel boven het label 0 gebruiken om aan te geven dat het een code ring van een bit in de status 0 is.
Als we op dezelfde manier $ \overline{1} = $111, hebben we een eenvoudige herhalings code die kan worden beveiligd tegen een fout bij het spie gelen van een bit.
Als een van de drie bits is gespiegeld, kunnen we de status van de logische bit herstellen door een meerderheids stem te nemen.
Hoewel de klassieke fout correctie een veel rijker onderwerp is dat dit specifieke voor beeld wordt aangeraden, wordt de [inleidende](https://www.springer.com/us/book/9783540641339)code hierboven al verwezen naar een mogelijk probleem bij het beveiligen van Quantum gegevens.
Het [no-klonen van theorema](xref:microsoft.quantum.concepts.pauli#the-no-cloning-theorem) impliceert dat als we elke afzonderlijke Qubit meten en een meerderheids stem hebben ondergaand op basis van de hierboven vermelde code, de nauw keurige informatie die we proberen te beveiligen, verloren is gegaan.

In de Quantum instelling zien we dat de meting problemen heeft. De bovenstaande code ring kan nog steeds worden geïmplementeerd.
Het is handig om dit te doen om te zien hoe de fout correctie voor de Quantum case kan worden gegeneraliseerd.
Laat bijvoorbeeld $ \ket{\overline{0}} = \ket{000} = \ket{0} \otimes \ket{0} \otimes \ket{0}$, en laat $ \ket{\overline{1}} = \ket{111}$.
Op basis van lineariteit hebben we de herhalings code voor alle invoer gedefinieerd. bijvoorbeeld: $ \ket{\overline{+}} = (\ket{\overline{0}} + \ket{\overline{1}})/\sqrt{2} = (\ket{000} + \ket{111})/\sqrt{2}$.
Met name als u een bit spiegel fout $X _1 $ Act op de middelste Qubit, zien we dat de benodigde correctie in beide filialen precies $X _1 $: $ $ \begin{align} X_1 \ket{\overline{+}} & = \frac{1}{\sqrt{2}} \left (X_1 \ket{000} + X_1 \ket{111} \right) \\\\ & = \frac{1}{\sqrt{2}} \left (\ket{010} + \ket{101} \right).
\end{align} $ $

Om te zien hoe we kunnen vaststellen dat dit het geval is, zonder dat u de enige status die we proberen te bemeten, is het handig om te schrijven wat elke andere bit voor het spie gelen van fouten aan de logische status heeft:

| Fout $E $ | $E \ket{\overline{0}} $ | $E \ket{\overline{1}} $ |
| --- | --- | --- |
| $ \boldone $ | $ \ket{000}$ | $ \ket{111}$ |
| $X _0 $ | $ \ket{100}$ | $ \ket{011}$ |
| $X _1 $ | $ \ket{010}$ | $ \ket{101}$ |
| $X _2 $ | $ \ket{001}$ | $ \ket{110}$ |

Ter bescherming van de status die we coderen, moeten we de drie fouten van elkaar en uit de identiteit $ \boldone $ onderscheiden, zonder onderscheid te maken tussen $ \ket{\overline{0}} $ en $ \ket{\overline{1}} $.
Als we bijvoorbeeld $Z _0 $ meten, krijgen we een ander resultaat voor $ \ket{\overline{0}} $ en $ \ket{\overline{1}} $ in het geval geen fout, waardoor de gecodeerde status wordt samengevouwen.
In het andere geval kunt u overwegen om $Z _0 Z_1 $ te meten, de pariteit van de eerste twee bits in elke reken status.
U kunt er ook voor zorgen dat elke meting van een Pauli-operator controleert welke eigenvalue de status wordt gemeten overeenkomt met, dus voor elke staat $ \ket{\psi} $ in de bovenstaande tabel, kunnen we $Z _0 Z_1 \ket{\psi} $ berekenen om te zien of $ \pm\ket{\psi} $ wordt ontvangen.
Houd er rekening mee dat $Z _0 Z_1 \ket{000} = \ket{000}$ en dat $Z _0 Z_1 \ket{111} = \ket{111}$, zodat we kunnen concluderen dat deze meting hetzelfde is voor beide gecodeerde statussen.
Aan de andere kant, $Z _0 Z_1 \ket{100} =-\ket{100}$ en $Z _0 Z_1 \ket{011} =-\ket{011}$, dus het resultaat van de meting $Z _0 Z_1 $ onthult nuttige informatie over welke fout is opgetreden.

Als u dit wilt benadrukken, herhaalt u de bovenstaande tabel, maar voegt u de resultaten van meting $Z _0 Z_1 $ en $Z _1 Z_2 $ toe aan elke rij.
De resultaten van elke meting worden aangegeven door het teken van de eigenvalue die wordt waargenomen, ofwel $ + $ of $-$, die overeenkomt met de Q # `Result` waarden van `Zero` en `One`respectievelijk.

| Fout $E $ | $E \ket{\overline{0}} $ | $E \ket{\overline{1}} $ | Resultaat van $Z _0 Z_1 $ | Resultaat van $Z _1 Z_2 $ |
| --- | --- | --- | --- | --- |
| $ \boldone $ | $ \ket{000}$ | $ \ket{111}$ | $+$ | $+$ |
| $X _0 $ | $ \ket{100}$ | $ \ket{011}$ | $-$ | $+$ |
| $X _1 $ | $ \ket{010}$ | $ \ket{101}$ | $-$ | $-$ |
| $X _2 $ | $ \ket{001}$ | $ \ket{110}$ | $+$ | $-$ |

De resultaten van de twee metingen bepalen daarom op unieke wijze welke bit-Flip-fout is opgetreden, maar zonder dat er informatie wordt onthuld over welke status er is gecodeerd.
We noemen deze resultaten een *Syndrome*en verwijzen naar het proces van het toewijzen van een Syndrome terug naar de fout die de *bewerking*heeft veroorzaakt.
In het bijzonder benadrukken we dat herstel een *klassieke* methode voor het afwijzen van de interferentie is, waarbij de Syndrome wordt ingevoerd, en er een recept wordt geretourneerd voor het oplossen van eventuele fouten die zich hebben voorgedaan.

> [!NOTE]
> De bit-Flip code hierboven kan alleen worden gecorrigeerd ten opzichte van enkele bits-Flip-fouten; dat wil zeggen een `X` bewerking die wordt uitgevoerd op één Qubit.
> Als `X` op meer dan één Qubit wordt toegepast, wordt $ \ket{\overline{0}} $ toegewezen aan $ \ket{\overline{1}} $ na herstel.
> Op dezelfde manier wordt bij het Toep assen van een Phase-`Z` bewerking voor het spie gelen van een fase $ \ket{\overline{1}} $ aan $-\ket{\overline{1}} $ toegewezen, en wordt dus $ \ket{\overline{+}} $ toegewezen aan $ \ket{\overline{-}} $.
> Meer in het algemeen kunnen codes worden gemaakt voor het verwerken van een groter aantal fouten en voor het afhandelen van $Z $-fouten, evenals $X $-fouten.

Het inzicht dat we meten in een Quantum fout correctie die op dezelfde manier op alle code Staten reageert, is de essentie van de *stabilisatie formaliteit*.
De Q # Canon biedt een framework voor het beschrijven van code ring en het decoderen van stabilisator-codes, en voor het beschrijven van het herstel van fouten.
In deze sectie beschrijven we dit kader en de toepassing ervan tot een paar eenvoudige Quantum fout codes.

> [!TIP]
> Een volledige inleiding tot de stabilisatie formaliteit valt buiten het bereik van deze sectie.
> We verwijzen naar lezers die meer willen weten over [Gottesman 2009](https://arxiv.org/abs/0904.2557).

## <a name="representing-error-correcting-codes-in-q"></a>Geeft aan dat fouten zijn gecorrigeerd codes in Q # ##

Om u te helpen bij het opgeven van fouten corrigerende codes, biedt Q # Canon verschillende door de gebruiker gedefinieerde typen:

- <xref:microsoft.quantum.errorcorrection.logicalregister> `= Qubit[]`: Hiermee wordt aangegeven dat een REGI ster van qubits moet worden geïnterpreteerd als het code blok van een code voor fout correctie.
- <xref:microsoft.quantum.errorcorrection.syndrome> `= Result[]`: Hiermee wordt aangegeven dat een matrix met meet resultaten moet worden geïnterpreteerd als de Syndrome die wordt gemeten in een code blok.
- <xref:microsoft.quantum.errorcorrection.recoveryfn> `= (Syndrome -> Pauli[])`: Hiermee wordt aangegeven dat een *klassieke* functie moet worden gebruikt om een Syndrome te interpreteren en een correctie te retour neren die moet worden toegepast.
- <xref:microsoft.quantum.errorcorrection.encodeop> `= ((Qubit[], Qubit[]) => LogicalRegister)`: Hiermee wordt aangegeven dat bij een bewerking qubits gegevens worden gebruikt in combi natie met een nieuwe ancilla qubits om een code blok te maken van een fout code.
- <xref:microsoft.quantum.errorcorrection.decodeop> `= (LogicalRegister => (Qubit[], Qubit[]))`: Hiermee wordt aangegeven dat een bewerking een code blok van een fout bij het corrigeren van code in de gegevens qubits en de ancilla qubits gebruikt om Syndrome-informatie weer te geven.
- <xref:microsoft.quantum.errorcorrection.syndromemeasop> `= (LogicalRegister => Syndrome)`: geeft een bewerking aan die moet worden gebruikt voor het extra heren van Syndrome-informatie uit een code blok zonder dat de status wordt verstoord die wordt beveiligd door de code.

Ten slotte biedt Canon het <xref:microsoft.quantum.errorcorrection.qecc> type voor het verzamelen van de andere typen die vereist zijn voor het definiëren van een Quantum fout-juiste code. Voor elke stabilisatore Quantum code is de lengte van de code $n $, het aantal $k $ logische qubits en de minimale afstand $d $, vaak gezamenlijk gegroepeerd in de notatie ⟦ $n $, $k $ $d $ ⟧. De functie <xref:microsoft.quantum.errorcorrection.bitflipcode> definieert bijvoorbeeld de ⟦ 3, 1, 1 ⟧ bit voor spie gelen:

```qsharp
let encodeOp = EncodeOp(BitFlipEncoder);
let decodeOp = DecodeOp(BitFlipDecoder);
let syndMeasOp = SyndromeMeasOp(MeasureStabilizerGenerators([
    [PauliZ, PauliZ, PauliI],
    [PauliI, PauliZ, PauliZ]
], _, MeasureWithScratch));
let code = QECC(encodeOp, decodeOp, syndMeasOp);
```

U ziet dat het type `QECC` *geen herstel functie bevat.*
Hierdoor kunnen we de herstel functie wijzigen die wordt gebruikt bij het corrigeren van fouten zonder de definitie van de code zelf te wijzigen. deze mogelijkheid is vooral nuttig bij het opnemen van feedback van karakte maten in het model dat wordt gebruikt door herstel.

Zodra een code op deze manier is gedefinieerd, kunnen we de bewerking <xref:microsoft.quantum.errorcorrection.recover> gebruiken om fouten op te lossen:

```qsharp
let code = BitFlipCode();
let fn = BitFlipRecoveryFn();
let X0 = ApplyPauli([PauliX, PauliI, PauliI], _);
using (scratch = Qubit[nScratch]) {
    let logicalRegister = encode(data, scratch);
    // Cause an error.
    X0(logicalRegister);
    Recover(code, fn, logicalRegister);
    let (decodedData, decodedScratch) = decode(logicalRegister);
    ApplyToEach(Reset, decodedScratch);
}
```

We verkennen dit gedetailleerder in het bits-voor beeld voor het [spie gelen van code](https://github.com/microsoft/Quantum/tree/master/samples/error-correction/bit-flip-code).

Afgezien van de code voor het spie gelen van bits, wordt Q # Canon gegeven met implementaties van de code van [vijf Qubit perfect](https://arxiv.org/abs/quant-ph/9602019)en de [code van zeven Qubit](https://arxiv.org/abs/quant-ph/9705052), die beide een wille keurige fout met één qubit kan oplossen.
