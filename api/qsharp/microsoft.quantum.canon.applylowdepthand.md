---
uid: Microsoft.Quantum.Canon.ApplyLowDepthAnd
title: Bewerking ApplyLowDepthAnd
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyLowDepthAnd
qsharp.summary: Inverts a given target qubit if and only if both control qubits are in the 1 state, with T-depth 1, using measurement to perform the adjoint operation.
ms.openlocfilehash: 4c5e381227bf82415121add38d0c0d2959fb529d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96209312"
---
# <a name="applylowdepthand-operation"></a>Bewerking ApplyLowDepthAnd

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Hiermee wordt een bepaalde doel-Qubit als en alleen als beide Control qubits zich in de status 1 bevinden, met T-diepte 1, met behulp van meting om de adjoint-bewerking uit te voeren.

```qsharp
operation ApplyLowDepthAnd (control1 : Qubit, control2 : Qubit, target : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a>Beschrijving

Keert `target` alleen als beide besturings elementen 1 zijn, maar er wordt van uitgegaan dat de `target` status 0 is.  De bewerking heeft T-Count 4, T-diepte 1 en vereist een helper-Qubit en kan daarom de voor keur geven aan een CCNOT-bewerking, als `target` bekend is dat deze 0 is.  De adjoint van deze bewerking wordt gemeten op basis van de meting en vereist geen T-poorten en geen helper-Qubit.

## <a name="input"></a>Invoer

### <a name="control1--qubit"></a>control1: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Eerste besturings element Qubit


### <a name="control2--qubit"></a>control2: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Qubit voor het tweede besturings element


### <a name="target--qubit"></a>doel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Doel hulp Qubit; moet de status 0 hebben



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="references"></a>Referenties

- Cody Jones: ' nieuwe constructies voor de fout tolerante Toffoli-Gate ', fysiek. Rev. A 87, 022328, 2013 [arXiv: 1212.5069](https://arxiv.org/abs/1212.5069) DOI: 10.1103/PhysRevA. 87.022328
- Peter Selinger: ' Quantum circuits One ', fysiek. Rev. A 87, 042302, 2013 [arXiv: 1210.0974](https://arxiv.org/abs/1210.0974) DOI: 10.1103/PhysRevA. 87.042302