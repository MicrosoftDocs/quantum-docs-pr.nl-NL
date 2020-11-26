---
uid: Microsoft.Quantum.ErrorCorrection.KnillDistill
title: Bewerking KnillDistill
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: KnillDistill
qsharp.summary: Implements the Knill magic state distillation algorithm.
ms.openlocfilehash: df00c7572d909a67ec658bc8dccaf0e338afe5c5
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96200744"
---
# <a name="knilldistill-operation"></a>Bewerking KnillDistill

Naam ruimte: [micro soft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Implementeert het distillatie algoritme Knill Magic State.

```qsharp
operation KnillDistill (roughMagic : Qubit[]) : Bool
```


## <a name="description"></a>Beschrijving

Gegeven op 15 geschatte kopieën van een magische status $ $ \begin{align} \cos\frac{\pi} {8} \ket {0} + \sin \frac{\pi} {8} \ket {1} \end{align}, $ $ levert een kopie van een hogere kwaliteit.

## <a name="input"></a>Invoer

### <a name="roughmagic--qubit"></a>roughMagic: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Een REGI ster van vijf tien qubits die geschatte kopieën van een magische status bevatten. De volgende toepassing van deze destillatie procedure `roughMagic[0]` bevat één kopie van een hogere kwaliteit en de rest van het REGI ster wordt opnieuw ingesteld op de status $ \ket{00\cdots 0} $.



## <a name="output--bool"></a>Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)

Als `true` de procedure is geslaagd en de kopie van de hogere kwaliteit moet worden geaccepteerd. Als `false` de procedure is mislukt en de status van het REGI ster moet worden beschouwd als niet-gedefinieerd.

## <a name="remarks"></a>Opmerkingen

We volgen het algoritme van Knill.
De huidige implementatie is echter veel van optimaal, omdat er te veel qubits worden gebruikt.
De magische statussen worden in deze routine geïnjecteerd, in welk geval er betere protocollen zijn.

## <a name="references"></a>Referenties

- [Knill](https://arxiv.org/abs/quant-ph/0402171)