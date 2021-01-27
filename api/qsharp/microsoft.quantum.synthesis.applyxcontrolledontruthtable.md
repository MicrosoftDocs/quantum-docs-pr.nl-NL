---
uid: Microsoft.Quantum.Synthesis.ApplyXControlledOnTruthTable
title: Bewerking ApplyXControlledOnTruthTable
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: ApplyXControlledOnTruthTable
qsharp.summary: Applies the @"microsoft.quantum.intrinsic.x" operation on `target`, if the Boolean function `func` evaluates to true for the classical assignment in `controlRegister`.
ms.openlocfilehash: 6e956038f7cd15db7348ff830da8bc9eae53aa61
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855566"
---
# <a name="applyxcontrolledontruthtable-operation"></a>Bewerking ApplyXControlledOnTruthTable

Naam ruimte: [micro soft. Quantum. synthese](xref:Microsoft.Quantum.Synthesis)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


De bewerking wordt toegepast @"microsoft.quantum.intrinsic.x" op `target` als de Boole-functie `func` resulteert in waar voor de klassieke toewijzing in `controlRegister` .

```qsharp
operation ApplyXControlledOnTruthTable (func : BigInt, controlRegister : Qubit[], target : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a>Beschrijving

Met deze bewerking wordt de unitary-bewerking geïmplementeerd \begin{align} U\ket {x} \ Ket {y} = \ket{x}\ket{y \oplus f (x)} \end{align} waarbij respectievelijk $x $ en $y $ representeren `controlRegister` `target` .

De Booleaanse functie $f $ wordt weer gegeven als een waarheids tabel in termen van een groot geheel getal.
De functie meerderheid op drie invoer wordt bijvoorbeeld vertegenwoordigd door de bitstring `11101000` , waarbij de meest significante bit `1` overeenkomt met de invoer toewijzing `(1, 1, 1)` en de minst significante bit `0` overeenkomt met de invoer toewijzing `(0, 0, 0)` .
De waarde kan worden weer gegeven met het grote gehele getal `0xE8L` in hexadecimale notatie of als `232L` in de decimale notatie.  Het `L` achtervoegsel geeft aan dat de constante van het type is `BigInt` .
Meer informatie over deze representatie vindt u ook in de [waarheids tabellen Kata](https://github.com/microsoft/QuantumKatas/tree/main/TruthTables).

De implementatie maakt gebruik van @"microsoft.quantum.intrinsic.cnot" en @"microsoft.quantum.intrinsic.r1" poorten.

## <a name="input"></a>Invoer

### <a name="func--bigint"></a>FUNC: [BigInt](xref:microsoft.quantum.lang-ref.bigint)

Tabel met Boole-waarheid wordt weer gegeven als Big-geheel getal


### <a name="controlregister--qubit"></a>controlRegister: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

REGI ster van controle qubits


### <a name="target--qubit"></a>doel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Doel-Qubit



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="references"></a>Verwijzingen

- [*N. Schuch*, *J. Siewert*, PRL 91, no. 027902, 2003, arXiv: Quant-pH/0303063](https://arxiv.org/abs/quant-ph/0303063)
- [*Mathias soeken*, *Martin Roetteler*, arXiv: 2005.12310](https://arxiv.org/abs/2005.12310)

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. synthese. ApplyXControlledOnTruthTableWithCleanTarget](xref:Microsoft.Quantum.Synthesis.ApplyXControlledOnTruthTableWithCleanTarget)