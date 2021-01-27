---
uid: Microsoft.Quantum.Canon.Angle
title: Functie Angle
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Angle
qsharp.summary: Returns 1, if `index` has an odd number of 1s and -1, if `index` has an even number of 1s.
ms.openlocfilehash: 0528f21b2d9c98b6497e28741964e6497d4d0fb9
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842040"
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

