---
uid: Microsoft.Quantum.Arithmetic.ReflectAboutInteger
title: Bewerking ReflectAboutInteger
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ReflectAboutInteger
qsharp.summary: Reflects a quantum register about a given classical integer.
ms.openlocfilehash: 4d451c4e8e002f86c892b394f58ea2d7e9dd6a48
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842983"
---
# <a name="reflectaboutinteger-operation"></a>Bewerking ReflectAboutInteger

Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Weerspiegelt een Quantum register over een gegeven klassiek geheel getal.

```qsharp
operation ReflectAboutInteger (index : Int, reg : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a>Beschrijving

Gezien een Quantum register in eerste instantie in de staat $ \ sum_i \ alpha_i \ket{i} $, waarbij elke $ \ket{i} $ een basis status is van een geheel getal $i $, weerspiegelt de status van de kassa over de basis status voor een bepaald geheel getal $ \ket{j} $, $ $ \ sum_i (-1) ^ {\ delta_ {IJ}} \ alpha_i \ket{i} $ $

## <a name="input"></a>Invoer

### <a name="index--int"></a>index: [int](xref:microsoft.quantum.lang-ref.int)

Het klassieke geheel getal waarmee de basis status wordt geïndexeerd die moet worden weer gegeven.


### <a name="reg--littleendian"></a>reg: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)





## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Opmerkingen

Deze bewerking wordt in-place geïmplementeerd zonder uitdrukkelijke toewijzing van aanvullende hulp qubits.