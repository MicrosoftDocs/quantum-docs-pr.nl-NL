---
uid: Microsoft.Quantum.ErrorCorrection._ExtractLogicalQubitFromSteaneCode
title: _ExtractLogicalQubitFromSteaneCode bewerking
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: _ExtractLogicalQubitFromSteaneCode
qsharp.summary: >-
  Syndrome measurement and the inverse of embedding.

  $X$- and $Z$-stabilizers are not treated equally, which is due to the particular choice of the encoding circuit. This asymmetry leads to a different syndrome extraction routine. One could measure the syndrome by measuring multi-qubit Pauli operator directly on the code state, but for the distillation purpose the logical qubit is returned into a single qubit, in course of which the syndrome measurements can be done without further ancillas.
ms.openlocfilehash: fe64343e30a0a3f0d05382e7812d37d5b13133d3
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853219"
---
# <a name="_extractlogicalqubitfromsteanecode-operation"></a>_ExtractLogicalQubitFromSteaneCode bewerking

Naam ruimte: [micro soft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Syndrome-meting en de inverse van het insluiten.

$X $-en $Z $-stabilisatoren worden niet gelijk behandeld, wat het gevolg is van de specifieke keuze van het coderings circuit.
Deze asymmetrie leidt naar een andere Syndrome-extractie routine.
Eén kan de Syndrome meten door de multi-Qubit Pauli-operator rechtstreeks op de code status te meten, maar voor het doel van de distillatie wordt de logische Qubit geretourneerd in één Qubit, in de periode dat de Syndrome metingen zonder verdere ancillas kunnen worden uitgevoerd.

```qsharp
operation _ExtractLogicalQubitFromSteaneCode (code : Microsoft.Quantum.ErrorCorrection.LogicalRegister) : (Qubit, Int, Int)
```


## <a name="input"></a>Invoer

### <a name="code--logicalregister"></a>code: [LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)





## <a name="output--qubitintint"></a>Uitvoer: ([Qubit](xref:microsoft.quantum.lang-ref.qubit),[int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int))

De logische Qubit en een paar gehele getallen voor $X $-Syndrome en $Z $-Syndrome.
Ze vertegenwoordigen de index van de code Qubit waarop een enkele $X $-of $Z $-error de gemeten Syndrome heeft veroorzaakt.

## <a name="remarks"></a>Opmerkingen

Houd er rekening mee dat deze bewerking niet is gemarkeerd als `internal` , omdat eenheids tests rechtstreeks afhankelijk zijn van deze bewerking. Als toekomstige verbetering moeten eenheids testen worden herstructureeerd om alleen rechtstreeks op open bare callables te zijn.

> [!WARNING]
> Deze routine is afgestemd op een bepaald coderings circuit voor de 7 Qubit-code van Steane. Als het coderings circuit is gewijzigd, moet het Syndrome-resultaat mogelijk anders worden geïnterpreteerd.