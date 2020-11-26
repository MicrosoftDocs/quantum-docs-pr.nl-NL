---
uid: Microsoft.Quantum.Canon.Angle
title: Functie Angle
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Angle
qsharp.summary: Returns 1, if `index` has an odd number of 1s and -1, if `index` has an even number of 1s.
ms.openlocfilehash: 1d8a9c2c19469e4949f043edd1ba91021fa42e78
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96219410"
---
# <a name="angle-function"></a>Functie Angle

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Retourneert 1, als `index` heeft een oneven aantal enen en-1, als `index` een even aantal enen heeft.

```qsharp
function Angle (index : Int) : Int
```


## <a name="description"></a>Beschrijving

De waarde komt overeen met het teken van de coëfficiënt van het Rademacher-Walsh spectrum van de n-variabele en de functie voor een bepaalde toewijzing die de hoek van de draaiing bepaalt.

## <a name="input"></a>Invoer

### <a name="index--int"></a>index: [int](xref:microsoft.quantum.lang-ref.int)

Invoer toewijzing als geheel getal (tussen 0 en 2 ^ n-1)



## <a name="output--int"></a>Uitvoer: [int](xref:microsoft.quantum.lang-ref.int)

