---
uid: Microsoft.Quantum.Diagnostics.Test
title: Door de gebruiker gedefinieerd type testen
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: Test
qsharp.summary: Compiler-recognized attribute used to mark a unit test.
ms.openlocfilehash: 2f1b521c4ef2bf8e672ca4fe7a5f380d744300b7
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853257"
---
# <a name="test-user-defined-type"></a>Door de gebruiker gedefinieerd type testen

Naam ruimte: [micro soft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Door het compiler herkend kenmerk dat wordt gebruikt om een eenheids test te markeren.

```qsharp

@ Microsoft.Quantum.Core.Attribute()
newtype Test = (ExecutionTarget : String);
```



## <a name="named-items"></a>Benoemde items

### <a name="executiontarget--string"></a>ExecutionTarget: [teken reeks](xref:microsoft.quantum.lang-ref.string)

