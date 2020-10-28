---
uid: Microsoft.Quantum.Canon.Angle
title: Functie Angle
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Angle
qsharp.summary: Returns 1, if `index` has an odd number of 1s and -1, if `index` has an even number of 1s.
ms.openlocfilehash: da3ecdaf1b2c88180bd2a660fac0b6e87b2cafa1
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705524"
---
# <a name="angle-function"></a>Functie Angle

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket [](https://nuget.org/packages/)


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

