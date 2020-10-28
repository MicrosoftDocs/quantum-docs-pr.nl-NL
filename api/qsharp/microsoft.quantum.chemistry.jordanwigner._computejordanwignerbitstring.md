---
uid: Microsoft.Quantum.Chemistry.JordanWigner._ComputeJordanWignerBitString
title: Functie _ComputeJordanWignerBitString
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _ComputeJordanWignerBitString
qsharp.summary: Computes Z component of Jordan–Wigner string between fermion indices in a fermionic operator with an even number of creation / annihilation operators.
ms.openlocfilehash: 31b957a435c3f578bc03d432609cde14c2ef5ced
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703496"
---
# <a name="_computejordanwignerbitstring-function"></a>Functie _ComputeJordanWignerBitString

Naam ruimte: [micro soft. Quantum. chemie. JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)

Pakket [](https://nuget.org/packages/)


Berekent Z-onderdeel van Jordanië – Wigner teken reeks tussen fermion indices in een fermionic-operator met een even aantal aanmaak/Annihilation-Opera tors.

```qsharp
function _ComputeJordanWignerBitString (nFermions : Int, idxFermions : Int[]) : Bool[]
```


## <a name="input"></a>Invoer

### <a name="nfermions--int"></a>nFermions: [int](xref:microsoft.quantum.lang-ref.int)

Het aantal fermions in het systeem.


### <a name="idxfermions--int"></a>idxFermions: [int](xref:microsoft.quantum.lang-ref.int)[]

indices van fermionic-Opera tors.



## <a name="output--bool"></a>Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)[]

Bitstring `Bool[]` waarop `true` een `PauliZ` moet worden toegepast.