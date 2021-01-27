---
uid: Microsoft.Quantum.Simulation.BlockEncodingToReflection
title: De functie BlockEncodingToReflection
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: BlockEncodingToReflection
qsharp.summary: >-
  Converts a `BlockEncoding` into an equivalent `BLockEncodingReflection`.

  That is, given a `BlockEncoding` unitary $U$ that encodes some operator $H$ of interest, converts it into a `BlockEncodingReflection` $U'$ that encodes the same operator, but also satisfies $U'^\dagger = U'$. This increases the size of the auxiliary register of $U$ by one qubit.
ms.openlocfilehash: bada0dcc54d2a8d67cf7383d7153c7f46a4a8415
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847261"
---
# <a name="blockencodingtoreflection-function"></a>De functie BlockEncodingToReflection

Naam ruimte: [micro soft. Quantum. simulatie](xref:Microsoft.Quantum.Simulation)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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

## <a name="references"></a>Verwijzingen

- Hamiltonian simulatie door Qubitization Guang Hao laag, Isaac L. Chuang https://arxiv.org/abs/1610.06546

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. simulatie. BlockEncoding](xref:Microsoft.Quantum.Simulation.BlockEncoding)
- [Micro soft. Quantum. simulatie. BlockEncodingReflection](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection)