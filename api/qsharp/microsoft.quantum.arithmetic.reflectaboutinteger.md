---
uid: Microsoft.Quantum.Arithmetic.ReflectAboutInteger
title: Bewerking ReflectAboutInteger
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ReflectAboutInteger
qsharp.summary: Reflects a quantum register about a given classical integer.
ms.openlocfilehash: e034f0a24d5c2f0465ebd1914b28cb8c695d978c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706340"
---
# <a name="reflectaboutinteger-operation"></a>Bewerking ReflectAboutInteger

Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)

Pakket [](https://nuget.org/packages/)


Weerspiegelt een Quantum register over een gegeven klassiek geheel getal.

```qsharp
operation ReflectAboutInteger (index : Int, reg : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
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