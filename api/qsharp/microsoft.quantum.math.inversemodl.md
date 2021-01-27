---
uid: Microsoft.Quantum.Math.InverseModL
title: De functie InverseModL
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: InverseModL
qsharp.summary: Returns $b$ such that $a \cdot b = 1 (\operatorname{mod} \texttt{modulus})$.
ms.openlocfilehash: e09c9da500889dfcb514d0a02dec957bfaa70e1c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851393"
---
# <a name="inversemodl-function"></a>De functie InverseModL

Naam ruimte: [micro soft. Quantum. math](xref:Microsoft.Quantum.Math)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Retourneert $b $ zodanig dat $a \cdot b = 1 (\operatorname{mod} \texttt{modulus}) $.

```qsharp
function InverseModL (a : BigInt, modulus : BigInt) : BigInt
```


## <a name="input"></a>Invoer

### <a name="a--bigint"></a>a: [BigInt](xref:microsoft.quantum.lang-ref.bigint)

Het getal wordt omgekeerd


### <a name="modulus--bigint"></a>modulus: [BigInt](xref:microsoft.quantum.lang-ref.bigint)

De modulus op basis waarvan de getallen worden omgekeerd



## <a name="output--bigint"></a>Uitvoer: [BigInt](xref:microsoft.quantum.lang-ref.bigint)

Geheel getal $b $ zodanig dat $a \cdot b = 1 (\operatorname{mod} \texttt{modulus}) $.