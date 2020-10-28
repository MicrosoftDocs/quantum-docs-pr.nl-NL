---
uid: Microsoft.Quantum.Simulation.BlockEncodingToReflection
title: De functie BlockEncodingToReflection
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: BlockEncodingToReflection
qsharp.summary: >-
  Converts a `BlockEncoding` into an equivalent `BLockEncodingReflection`.

  That is, given a `BlockEncoding` unitary $U$ that encodes some operator $H$ of interest, converts it into a `BlockEncodingReflection` $U'$ that encodes the same operator, but also satisfies $U'^\dagger = U'$. This increases the size of the auxiliary register of $U$ by one qubit.
ms.openlocfilehash: a8b4c65f8c32f7f9185f1dbdacf8fc75fd4573b1
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707824"
---
# <a name="blockencodingtoreflection-function"></a>De functie BlockEncodingToReflection

Naam ruimte: [micro soft. Quantum. simulatie](xref:Microsoft.Quantum.Simulation)

Pakket [](https://nuget.org/packages/)


Converteert een `BlockEncoding` in een gelijkwaardige waarde `BLockEncodingReflection` .

Op basis van een `BlockEncoding` unitary $U $ die een bepaalde operator $H $ van de rente codeert, wordt deze omgezet in een `BlockEncodingReflection` $U $ die dezelfde operator codeert, maar ook voldoet aan $U ^ \Dagger = U ' $ '.
Dit verhoogt de grootte van het hulp register van $U $ door één Qubit.

```qsharp
function BlockEncodingToReflection (blockEncoding : Microsoft.Quantum.Simulation.BlockEncoding) : Microsoft.Quantum.Simulation.BlockEncodingReflection
```


## <a name="input"></a>Invoer

### <a name="blockencoding--blockencoding"></a>blockEncoding: [blockEncoding](xref:Microsoft.Quantum.Simulation.BlockEncoding)

Een `BlockEncoding` unitary $U $ moet worden geconverteerd naar een reflectie.



## <a name="output--blockencodingreflection"></a>Uitvoer: [BlockEncodingReflection](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection)

Een unitary-$U ' $ communiceert gezamenlijk aan registers `a` en `s` die blok-coderings $H $, en voldoet aan $U ^ \Dagger = U ' $.

## <a name="remarks"></a>Opmerkingen

Dit verhoogt de grootte van het hulp register van $U $ door één Qubit.

## <a name="references"></a>Naslaginformatie

- Hamiltonian simulatie door Qubitization Guang Hao laag, Isaac L. Chuang https://arxiv.org/abs/1610.06546

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. simulatie. BlockEncoding](xref:Microsoft.Quantum.Simulation.BlockEncoding)
- [Micro soft. Quantum. simulatie. BlockEncodingReflection](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection)