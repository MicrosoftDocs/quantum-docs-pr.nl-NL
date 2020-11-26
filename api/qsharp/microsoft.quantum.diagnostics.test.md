---
uid: Microsoft.Quantum.Diagnostics.Test
title: Door de gebruiker gedefinieerd type testen
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: Test
qsharp.summary: Compiler-recognized attribute used to mark a unit test.
ms.openlocfilehash: 80821cb46d773d84085838d9ee539a8a45c43e61
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96201492"
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

