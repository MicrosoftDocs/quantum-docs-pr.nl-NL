---
uid: Microsoft.Quantum.Synthesis.DecomposedOn
title: De functie DecomposedOn
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: DecomposedOn
qsharp.summary: Decomposes a permutation on a variable
ms.openlocfilehash: fb7aa5af8f3eb07399e0d2dd2d50723f4e6b169a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855516"
---
# <a name="decomposedon-function"></a><span data-ttu-id="7c672-102">De functie DecomposedOn</span><span class="sxs-lookup"><span data-stu-id="7c672-102">DecomposedOn function</span></span>

<span data-ttu-id="7c672-103">Naam ruimte: [micro soft. Quantum. synthese](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="7c672-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="7c672-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="7c672-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="7c672-105">Ontleedt een permutatie op een variabele</span><span class="sxs-lookup"><span data-stu-id="7c672-105">Decomposes a permutation on a variable</span></span>

```qsharp
function DecomposedOn (perm : Int[], index : Int) : ((Int[], Int[]), Int[])
```


## <a name="description"></a><span data-ttu-id="7c672-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="7c672-106">Description</span></span>

<span data-ttu-id="7c672-107">Met een permutatie $ \pi $ ( `perm` ) en een index $i $ ( `index` ), deze methode retourneert drie permutaties $ ((\ pi_l, \ pi_r), \pi ') $ zo dat de installatie kopieën van $ \ pi_l $ en $ \ pi_r $ geen bits in hun eigen elementen wijzigen op andere indexen dan $i $ en installatie kopieën van $ \pi $ in hun eigen elementen.</span><span class="sxs-lookup"><span data-stu-id="7c672-107">Given a permutation $\pi$ (`perm`) and an index $i$ (`index`), this method returns three permutations $((\pi_l, \pi_r), \pi')$ such that the images of $\pi_l$ and $\pi_r$ do not change bits in their elements at indexes other than $i$ and images of $\pi'$ do not change bit $i$ in their elements.</span></span>

## <a name="input"></a><span data-ttu-id="7c672-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="7c672-108">Input</span></span>

### <a name="perm--int"></a><span data-ttu-id="7c672-109">macht: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="7c672-109">perm : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>




### <a name="index--int"></a><span data-ttu-id="7c672-110">index: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="7c672-110">index : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>





## <a name="output--intintint"></a><span data-ttu-id="7c672-111">Output: (([int](xref:microsoft.quantum.lang-ref.int)[],[int](xref:microsoft.quantum.lang-ref.int)[]),[int](xref:microsoft.quantum.lang-ref.int)[])</span><span class="sxs-lookup"><span data-stu-id="7c672-111">Output : (([Int](xref:microsoft.quantum.lang-ref.int)[],[Int](xref:microsoft.quantum.lang-ref.int)[]),[Int](xref:microsoft.quantum.lang-ref.int)[])</span></span>



## <a name="example"></a><span data-ttu-id="7c672-112">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="7c672-112">Example</span></span>

<span data-ttu-id="7c672-113">Stel dat de invoer de volgende macht heeft: [0, 2, 3, 5, 7, 1, 4, 6] en index = 0. deze functie berekent drie permutaties op basis van de onderstaande tabel, waarin de permutatie `perm` in binaire notatie met elementen in groep A en afbeeldingen in groep D wordt weer gegeven.  De kolommen bevatten een lijst met de bits indexen.</span><span class="sxs-lookup"><span data-stu-id="7c672-113">Assume that the input is perm = [0, 2, 3, 5, 7, 1, 4, 6] and index = 0, then this function computes three permutations based on the following table, which lists the permutation `perm` in binary notation with elements in group A and images in group D.  The columns list the bit indices.</span></span>

<span data-ttu-id="7c672-114">|   A |   B |   C |   D |</span><span class="sxs-lookup"><span data-stu-id="7c672-114">|   A   |   B   |   C   |   D   |</span></span>
| <span data-ttu-id="7c672-115">2 1 0</span><span class="sxs-lookup"><span data-stu-id="7c672-115">2 1 0</span></span> | <span data-ttu-id="7c672-116">2 1 0</span><span class="sxs-lookup"><span data-stu-id="7c672-116">2 1 0</span></span> | <span data-ttu-id="7c672-117">2 1 0</span><span class="sxs-lookup"><span data-stu-id="7c672-117">2 1 0</span></span> | <span data-ttu-id="7c672-118">2 1 0</span><span class="sxs-lookup"><span data-stu-id="7c672-118">2 1 0</span></span> |
|-------|-------|-------|-------|
| <span data-ttu-id="7c672-119">0 0 0</span><span class="sxs-lookup"><span data-stu-id="7c672-119">0 0 0</span></span> |       |       | <span data-ttu-id="7c672-120">0 0 0</span><span class="sxs-lookup"><span data-stu-id="7c672-120">0 0 0</span></span> | <span data-ttu-id="7c672-121">0</span><span class="sxs-lookup"><span data-stu-id="7c672-121">0</span></span>
| <span data-ttu-id="7c672-122">0 0 1</span><span class="sxs-lookup"><span data-stu-id="7c672-122">0 0 1</span></span> |       |       | <span data-ttu-id="7c672-123">0 1 0</span><span class="sxs-lookup"><span data-stu-id="7c672-123">0 1 0</span></span> | <span data-ttu-id="7c672-124">2</span><span class="sxs-lookup"><span data-stu-id="7c672-124">2</span></span>
| <span data-ttu-id="7c672-125">0 1 0</span><span class="sxs-lookup"><span data-stu-id="7c672-125">0 1 0</span></span> |       |       | <span data-ttu-id="7c672-126">0 1 1</span><span class="sxs-lookup"><span data-stu-id="7c672-126">0 1 1</span></span> | <span data-ttu-id="7c672-127">3</span><span class="sxs-lookup"><span data-stu-id="7c672-127">3</span></span>
| <span data-ttu-id="7c672-128">0 1 1</span><span class="sxs-lookup"><span data-stu-id="7c672-128">0 1 1</span></span> |       |       | <span data-ttu-id="7c672-129">1 0 1</span><span class="sxs-lookup"><span data-stu-id="7c672-129">1 0 1</span></span> | <span data-ttu-id="7c672-130">5</span><span class="sxs-lookup"><span data-stu-id="7c672-130">5</span></span>
| <span data-ttu-id="7c672-131">1 0 0</span><span class="sxs-lookup"><span data-stu-id="7c672-131">1 0 0</span></span> |       |       | <span data-ttu-id="7c672-132">1 1 1</span><span class="sxs-lookup"><span data-stu-id="7c672-132">1 1 1</span></span> | <span data-ttu-id="7c672-133">7</span><span class="sxs-lookup"><span data-stu-id="7c672-133">7</span></span>
| <span data-ttu-id="7c672-134">1 0 1</span><span class="sxs-lookup"><span data-stu-id="7c672-134">1 0 1</span></span> |       |       | <span data-ttu-id="7c672-135">0 0 1</span><span class="sxs-lookup"><span data-stu-id="7c672-135">0 0 1</span></span> | <span data-ttu-id="7c672-136">1</span><span class="sxs-lookup"><span data-stu-id="7c672-136">1</span></span>
| <span data-ttu-id="7c672-137">1 1 0</span><span class="sxs-lookup"><span data-stu-id="7c672-137">1 1 0</span></span> |       |       | <span data-ttu-id="7c672-138">1 0 0</span><span class="sxs-lookup"><span data-stu-id="7c672-138">1 0 0</span></span> | <span data-ttu-id="7c672-139">4</span><span class="sxs-lookup"><span data-stu-id="7c672-139">4</span></span>
| <span data-ttu-id="7c672-140">1 1 1</span><span class="sxs-lookup"><span data-stu-id="7c672-140">1 1 1</span></span> |       |       | <span data-ttu-id="7c672-141">1 1 0</span><span class="sxs-lookup"><span data-stu-id="7c672-141">1 1 0</span></span> | <span data-ttu-id="7c672-142">6</span><span class="sxs-lookup"><span data-stu-id="7c672-142">6</span></span>

<span data-ttu-id="7c672-143">Alle waarden voor indices die niet gelijk zijn aan 0 (= index) worden gekopieerd van A naar B en van D naar C.</span><span class="sxs-lookup"><span data-stu-id="7c672-143">All values for indices not equal to 0 (= index) are copied from A to B and from D to C.</span></span>

<span data-ttu-id="7c672-144">|   A |   B |   C |   D |</span><span class="sxs-lookup"><span data-stu-id="7c672-144">|   A   |   B   |   C   |   D   |</span></span>
| <span data-ttu-id="7c672-145">2 1 0</span><span class="sxs-lookup"><span data-stu-id="7c672-145">2 1 0</span></span> | <span data-ttu-id="7c672-146">2 1 0</span><span class="sxs-lookup"><span data-stu-id="7c672-146">2 1 0</span></span> | <span data-ttu-id="7c672-147">2 1 0</span><span class="sxs-lookup"><span data-stu-id="7c672-147">2 1 0</span></span> | <span data-ttu-id="7c672-148">2 1 0</span><span class="sxs-lookup"><span data-stu-id="7c672-148">2 1 0</span></span> |
|-------|-------|-------|-------|
| <span data-ttu-id="7c672-149">0 0 0</span><span class="sxs-lookup"><span data-stu-id="7c672-149">0 0 0</span></span> | <span data-ttu-id="7c672-150">0 0</span><span class="sxs-lookup"><span data-stu-id="7c672-150">0 0</span></span>   | <span data-ttu-id="7c672-151">0 0</span><span class="sxs-lookup"><span data-stu-id="7c672-151">0 0</span></span>   | <span data-ttu-id="7c672-152">0 0 0</span><span class="sxs-lookup"><span data-stu-id="7c672-152">0 0 0</span></span> |
| <span data-ttu-id="7c672-153">0 0 1</span><span class="sxs-lookup"><span data-stu-id="7c672-153">0 0 1</span></span> | <span data-ttu-id="7c672-154">0 0</span><span class="sxs-lookup"><span data-stu-id="7c672-154">0 0</span></span>   | <span data-ttu-id="7c672-155">0 1</span><span class="sxs-lookup"><span data-stu-id="7c672-155">0 1</span></span>   | <span data-ttu-id="7c672-156">0 1 0</span><span class="sxs-lookup"><span data-stu-id="7c672-156">0 1 0</span></span> |
| <span data-ttu-id="7c672-157">0 1 0</span><span class="sxs-lookup"><span data-stu-id="7c672-157">0 1 0</span></span> | <span data-ttu-id="7c672-158">0 1</span><span class="sxs-lookup"><span data-stu-id="7c672-158">0 1</span></span>   | <span data-ttu-id="7c672-159">0 1</span><span class="sxs-lookup"><span data-stu-id="7c672-159">0 1</span></span>   | <span data-ttu-id="7c672-160">0 1 1</span><span class="sxs-lookup"><span data-stu-id="7c672-160">0 1 1</span></span> |
| <span data-ttu-id="7c672-161">0 1 1</span><span class="sxs-lookup"><span data-stu-id="7c672-161">0 1 1</span></span> | <span data-ttu-id="7c672-162">0 1</span><span class="sxs-lookup"><span data-stu-id="7c672-162">0 1</span></span>   | <span data-ttu-id="7c672-163">1 0</span><span class="sxs-lookup"><span data-stu-id="7c672-163">1 0</span></span>   | <span data-ttu-id="7c672-164">1 0 1</span><span class="sxs-lookup"><span data-stu-id="7c672-164">1 0 1</span></span> |
| <span data-ttu-id="7c672-165">1 0 0</span><span class="sxs-lookup"><span data-stu-id="7c672-165">1 0 0</span></span> | <span data-ttu-id="7c672-166">1 0</span><span class="sxs-lookup"><span data-stu-id="7c672-166">1 0</span></span>   | <span data-ttu-id="7c672-167">1 1</span><span class="sxs-lookup"><span data-stu-id="7c672-167">1 1</span></span>   | <span data-ttu-id="7c672-168">1 1 1</span><span class="sxs-lookup"><span data-stu-id="7c672-168">1 1 1</span></span> |
| <span data-ttu-id="7c672-169">1 0 1</span><span class="sxs-lookup"><span data-stu-id="7c672-169">1 0 1</span></span> | <span data-ttu-id="7c672-170">1 0</span><span class="sxs-lookup"><span data-stu-id="7c672-170">1 0</span></span>   | <span data-ttu-id="7c672-171">0 0</span><span class="sxs-lookup"><span data-stu-id="7c672-171">0 0</span></span>   | <span data-ttu-id="7c672-172">0 0 1</span><span class="sxs-lookup"><span data-stu-id="7c672-172">0 0 1</span></span> |
| <span data-ttu-id="7c672-173">1 1 0</span><span class="sxs-lookup"><span data-stu-id="7c672-173">1 1 0</span></span> | <span data-ttu-id="7c672-174">1 1</span><span class="sxs-lookup"><span data-stu-id="7c672-174">1 1</span></span>   | <span data-ttu-id="7c672-175">1 0</span><span class="sxs-lookup"><span data-stu-id="7c672-175">1 0</span></span>   | <span data-ttu-id="7c672-176">1 0 0</span><span class="sxs-lookup"><span data-stu-id="7c672-176">1 0 0</span></span> |
| <span data-ttu-id="7c672-177">1 1 1</span><span class="sxs-lookup"><span data-stu-id="7c672-177">1 1 1</span></span> | <span data-ttu-id="7c672-178">1 1</span><span class="sxs-lookup"><span data-stu-id="7c672-178">1 1</span></span>   | <span data-ttu-id="7c672-179">1 1</span><span class="sxs-lookup"><span data-stu-id="7c672-179">1 1</span></span>   | <span data-ttu-id="7c672-180">1 1 0</span><span class="sxs-lookup"><span data-stu-id="7c672-180">1 1 0</span></span> |

<span data-ttu-id="7c672-181">Vervolgens wordt 0 geplaatst voor het eerste element met een lege index op kolom 0 in blok B en wordt er een 1 in B geplaatst waarbij het voor voegsel overeenkomt (in het eerste geval de andere rij met indices 0 0).</span><span class="sxs-lookup"><span data-stu-id="7c672-181">Next a 0 is placed for the first element with an empty index at column 0 in block B and then a 1 is placed in B where the prefix matches (in the first case the other row with indices 0 0).</span></span>
<span data-ttu-id="7c672-182">Daarna wordt er een 1 toegevoegd aan dezelfde rij in blok C en vervolgens een 0 voor het bijbehorende voor voegsel in blok C.  Dit proces wordt herhaald totdat alle indices in kolom 0 in de blokken B en C zijn geplaatst.</span><span class="sxs-lookup"><span data-stu-id="7c672-182">Afterwards, a 1 is added in the same row in block C, and then a 0 for the corresponding prefix in block C.  This process is repeated, until all indices have been placed in column 0 in blocks B and C.</span></span>

<span data-ttu-id="7c672-183">|   A |   B |   C |   D |</span><span class="sxs-lookup"><span data-stu-id="7c672-183">|   A   |   B   |   C   |   D   |</span></span>
| <span data-ttu-id="7c672-184">2 1 0</span><span class="sxs-lookup"><span data-stu-id="7c672-184">2 1 0</span></span> | <span data-ttu-id="7c672-185">2 1 0</span><span class="sxs-lookup"><span data-stu-id="7c672-185">2 1 0</span></span> | <span data-ttu-id="7c672-186">2 1 0</span><span class="sxs-lookup"><span data-stu-id="7c672-186">2 1 0</span></span> | <span data-ttu-id="7c672-187">2 1 0</span><span class="sxs-lookup"><span data-stu-id="7c672-187">2 1 0</span></span> |
|-------|-------|-------|-------|
| <span data-ttu-id="7c672-188">0 0 0</span><span class="sxs-lookup"><span data-stu-id="7c672-188">0 0 0</span></span> | <span data-ttu-id="7c672-189">0 0 0</span><span class="sxs-lookup"><span data-stu-id="7c672-189">0 0 0</span></span> | <span data-ttu-id="7c672-190">0 0 0</span><span class="sxs-lookup"><span data-stu-id="7c672-190">0 0 0</span></span> | <span data-ttu-id="7c672-191">0 0 0</span><span class="sxs-lookup"><span data-stu-id="7c672-191">0 0 0</span></span> |
| <span data-ttu-id="7c672-192">0 0 1</span><span class="sxs-lookup"><span data-stu-id="7c672-192">0 0 1</span></span> | <span data-ttu-id="7c672-193">0 0 1</span><span class="sxs-lookup"><span data-stu-id="7c672-193">0 0 1</span></span> | <span data-ttu-id="7c672-194">0 1 1</span><span class="sxs-lookup"><span data-stu-id="7c672-194">0 1 1</span></span> | <span data-ttu-id="7c672-195">0 1 0</span><span class="sxs-lookup"><span data-stu-id="7c672-195">0 1 0</span></span> |
| <span data-ttu-id="7c672-196">0 1 0</span><span class="sxs-lookup"><span data-stu-id="7c672-196">0 1 0</span></span> | <span data-ttu-id="7c672-197">0 1 0</span><span class="sxs-lookup"><span data-stu-id="7c672-197">0 1 0</span></span> | <span data-ttu-id="7c672-198">0 1 0</span><span class="sxs-lookup"><span data-stu-id="7c672-198">0 1 0</span></span> | <span data-ttu-id="7c672-199">0 1 1</span><span class="sxs-lookup"><span data-stu-id="7c672-199">0 1 1</span></span> |
| <span data-ttu-id="7c672-200">0 1 1</span><span class="sxs-lookup"><span data-stu-id="7c672-200">0 1 1</span></span> | <span data-ttu-id="7c672-201">0 1 1</span><span class="sxs-lookup"><span data-stu-id="7c672-201">0 1 1</span></span> | <span data-ttu-id="7c672-202">1 0 1</span><span class="sxs-lookup"><span data-stu-id="7c672-202">1 0 1</span></span> | <span data-ttu-id="7c672-203">1 0 1</span><span class="sxs-lookup"><span data-stu-id="7c672-203">1 0 1</span></span> |
| <span data-ttu-id="7c672-204">1 0 0</span><span class="sxs-lookup"><span data-stu-id="7c672-204">1 0 0</span></span> | <span data-ttu-id="7c672-205">1 0 0</span><span class="sxs-lookup"><span data-stu-id="7c672-205">1 0 0</span></span> | <span data-ttu-id="7c672-206">1 1 0</span><span class="sxs-lookup"><span data-stu-id="7c672-206">1 1 0</span></span> | <span data-ttu-id="7c672-207">1 1 1</span><span class="sxs-lookup"><span data-stu-id="7c672-207">1 1 1</span></span> |
| <span data-ttu-id="7c672-208">1 0 1</span><span class="sxs-lookup"><span data-stu-id="7c672-208">1 0 1</span></span> | <span data-ttu-id="7c672-209">1 0 1</span><span class="sxs-lookup"><span data-stu-id="7c672-209">1 0 1</span></span> | <span data-ttu-id="7c672-210">0 0 1</span><span class="sxs-lookup"><span data-stu-id="7c672-210">0 0 1</span></span> | <span data-ttu-id="7c672-211">0 0 1</span><span class="sxs-lookup"><span data-stu-id="7c672-211">0 0 1</span></span> |
| <span data-ttu-id="7c672-212">1 1 0</span><span class="sxs-lookup"><span data-stu-id="7c672-212">1 1 0</span></span> | <span data-ttu-id="7c672-213">1 1 0</span><span class="sxs-lookup"><span data-stu-id="7c672-213">1 1 0</span></span> | <span data-ttu-id="7c672-214">1 0 0</span><span class="sxs-lookup"><span data-stu-id="7c672-214">1 0 0</span></span> | <span data-ttu-id="7c672-215">1 0 0</span><span class="sxs-lookup"><span data-stu-id="7c672-215">1 0 0</span></span> |
| <span data-ttu-id="7c672-216">1 1 1</span><span class="sxs-lookup"><span data-stu-id="7c672-216">1 1 1</span></span> | <span data-ttu-id="7c672-217">1 1 1</span><span class="sxs-lookup"><span data-stu-id="7c672-217">1 1 1</span></span> | <span data-ttu-id="7c672-218">1 1 1</span><span class="sxs-lookup"><span data-stu-id="7c672-218">1 1 1</span></span> | <span data-ttu-id="7c672-219">1 1 0</span><span class="sxs-lookup"><span data-stu-id="7c672-219">1 1 0</span></span> |

<span data-ttu-id="7c672-220">We kunnen drie nieuwe permutaties uit de tabel lezen:</span><span class="sxs-lookup"><span data-stu-id="7c672-220">We can read three new permutations from the table:</span></span>

- <span data-ttu-id="7c672-221">$ \ pi_l $ met elementen in A, afbeeldingen in B (links)</span><span class="sxs-lookup"><span data-stu-id="7c672-221">$\pi_l$ with elements in A, images in B (left)</span></span>
- <span data-ttu-id="7c672-222">$ \ pi_r $ met elementen in D, afbeeldingen in C (rechts)</span><span class="sxs-lookup"><span data-stu-id="7c672-222">$\pi_r$ with elements in D, images in C (right)</span></span>
- <span data-ttu-id="7c672-223">$ \pi $ met elementen in B, afbeeldingen in C (rest)</span><span class="sxs-lookup"><span data-stu-id="7c672-223">$\pi'$  with elements in B, images in C (remainder)</span></span>

<span data-ttu-id="7c672-224">Houd er rekening mee dat door de ontwerp-bits waarden niet worden gewijzigd in $ \ pi_l $ en $ \ pi_r $ voor indices 1 en 2, en dat bits-waarden niet worden gewijzigd voor in $ \ pi_ $ voor index 0.</span><span class="sxs-lookup"><span data-stu-id="7c672-224">Note that by design bit values do not change in $\pi_l$ and $\pi_r$ for indices 1 and 2, and bit values do not change for in $\pi_'$ for index 0.</span></span>  <span data-ttu-id="7c672-225">Houd er ook rekening mee dat $ \ pi_l $ en $ \ pi_r $ zelf inverse moet zijn.</span><span class="sxs-lookup"><span data-stu-id="7c672-225">Also note that $\pi_l$ and $\pi_r$ must be self-inverse.</span></span>

<span data-ttu-id="7c672-226">De afgeleide en geretourneerde permutaties zijn: Left = [0, 1, 2, 3, 4, 5, 6, 7] rechts = [0, 1, 3, 2, 4, 5, 7, 6] restant = [0, 3, 2, 5, 6, 1, 4, 7]</span><span class="sxs-lookup"><span data-stu-id="7c672-226">The derived and returned permutations are: left      = [0, 1, 2, 3, 4, 5, 6, 7] right     = [0, 1, 3, 2, 4, 5, 7, 6] remainder = [0, 3, 2, 5, 6, 1, 4, 7]</span></span>