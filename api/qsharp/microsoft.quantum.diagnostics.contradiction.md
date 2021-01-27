---
uid: Microsoft.Quantum.Diagnostics.Contradiction
title: Functie tegen strijdigheid
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: Contradiction
qsharp.summary: Declares that a classical condition is false.
ms.openlocfilehash: 7d62c9341b768dfdfbfbf8e73e64748f04317595
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98829369"
---
# <a name="contradiction-function"></a><span data-ttu-id="09d90-102">Functie tegen strijdigheid</span><span class="sxs-lookup"><span data-stu-id="09d90-102">Contradiction function</span></span>

<span data-ttu-id="09d90-103">Naam ruimte: [micro soft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="09d90-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="09d90-104">Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="09d90-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="09d90-105">Declareert dat een klassieke voor waarde ONWAAR is.</span><span class="sxs-lookup"><span data-stu-id="09d90-105">Declares that a classical condition is false.</span></span>

```qsharp
function Contradiction (actual : Bool, message : String) : Unit
```


## <a name="input"></a><span data-ttu-id="09d90-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="09d90-106">Input</span></span>

### <a name="actual--bool"></a><span data-ttu-id="09d90-107">werkelijk: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="09d90-107">actual : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="09d90-108">De voor waarde die moet worden gedeclareerd.</span><span class="sxs-lookup"><span data-stu-id="09d90-108">The condition to be declared.</span></span>


### <a name="message--string"></a><span data-ttu-id="09d90-109">bericht: [teken reeks](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="09d90-109">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="09d90-110">Fout bericht teken reeks die moet worden afgedrukt in het geval dat de klassieke voor waarde waar is.</span><span class="sxs-lookup"><span data-stu-id="09d90-110">Failure message string to be printed in the case that the classical condition is true.</span></span>



## <a name="output--unit"></a><span data-ttu-id="09d90-111">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="09d90-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="example"></a><span data-ttu-id="09d90-112">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="09d90-112">Example</span></span>

<span data-ttu-id="09d90-113">Met de volgende Q #-code wordt "Hallo, wereld" afgedrukt:</span><span class="sxs-lookup"><span data-stu-id="09d90-113">The following Q# code will print "Hello, world":</span></span>

```qsharp
Contradiction(2 == 3, "2 is not equal to 3.");
Message("Hello, world.");
```

## <a name="see-also"></a><span data-ttu-id="09d90-114">Zie ook</span><span class="sxs-lookup"><span data-stu-id="09d90-114">See Also</span></span>

- [<span data-ttu-id="09d90-115">Micro soft. Quantum. Diagnostics. fact</span><span class="sxs-lookup"><span data-stu-id="09d90-115">Microsoft.Quantum.Diagnostics.Fact</span></span>](xref:Microsoft.Quantum.Diagnostics.Fact)