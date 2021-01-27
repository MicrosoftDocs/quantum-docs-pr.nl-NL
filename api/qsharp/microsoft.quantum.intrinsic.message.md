---
uid: Microsoft.Quantum.Intrinsic.Message
title: Bericht functie
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: Message
qsharp.summary: Logs a message.
ms.openlocfilehash: 652e33de69ffb725f117db3beeffa66558776f49
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98849363"
---
# <a name="message-function"></a>Bericht functie

Naam ruimte: [micro soft. Quantum. intrinsiek](xref:Microsoft.Quantum.Intrinsic)

Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Een bericht wordt geregistreerd.

```qsharp
function Message (msg : String) : Unit
```


## <a name="input"></a>Invoer

### <a name="msg--string"></a>bericht: [teken reeks](xref:microsoft.quantum.lang-ref.string)

Het bericht dat moet worden gerapporteerd.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Opmerkingen

Het specifieke gedrag van deze functie is van Simulator afhankelijk, maar in de meeste gevallen wordt het gegeven bericht naar de-console geschreven.