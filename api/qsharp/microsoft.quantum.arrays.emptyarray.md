---
uid: Microsoft.Quantum.Arrays.EmptyArray
title: De functie EmptyArray
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: EmptyArray
qsharp.summary: Returns the empty array of a given type.
ms.openlocfilehash: cf15e61862bb64fb3408db2318fafb56d532b365
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846180"
---
# <a name="emptyarray-function"></a><span data-ttu-id="6c1f1-102">De functie EmptyArray</span><span class="sxs-lookup"><span data-stu-id="6c1f1-102">EmptyArray function</span></span>

<span data-ttu-id="6c1f1-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="6c1f1-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="6c1f1-104">Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="6c1f1-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="6c1f1-105">Retourneert de lege matrix van een bepaald type.</span><span class="sxs-lookup"><span data-stu-id="6c1f1-105">Returns the empty array of a given type.</span></span>

```qsharp
function EmptyArray<'TElement> () : 'TElement[]
```


## <a name="output--telement"></a><span data-ttu-id="6c1f1-106">Output: ' TEle []</span><span class="sxs-lookup"><span data-stu-id="6c1f1-106">Output : 'TElement[]</span></span>

<span data-ttu-id="6c1f1-107">De lege matrix.</span><span class="sxs-lookup"><span data-stu-id="6c1f1-107">The empty array.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="6c1f1-108">Type parameters</span><span class="sxs-lookup"><span data-stu-id="6c1f1-108">Type Parameters</span></span>

### <a name="telement"></a><span data-ttu-id="6c1f1-109">-TEle</span><span class="sxs-lookup"><span data-stu-id="6c1f1-109">'TElement</span></span>

<span data-ttu-id="6c1f1-110">Het type elementen van de matrix.</span><span class="sxs-lookup"><span data-stu-id="6c1f1-110">The type of elements of the array.</span></span>

## <a name="example"></a><span data-ttu-id="6c1f1-111">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="6c1f1-111">Example</span></span>

```qsharp
let empty = EmptyArray<Int>();
```