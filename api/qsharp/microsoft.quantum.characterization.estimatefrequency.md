---
uid: Microsoft.Quantum.Characterization.EstimateFrequency
title: Bewerking EstimateFrequency
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: EstimateFrequency
qsharp.summary: Given a preparation and measurement, estimates the frequency with which that measurement succeeds (returns `Zero`) by performing a given number of trials.
ms.openlocfilehash: 83589637a7bfa328812207271844411f57d42097
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703659"
---
# <a name="estimatefrequency-operation"></a><span data-ttu-id="59e21-102">Bewerking EstimateFrequency</span><span class="sxs-lookup"><span data-stu-id="59e21-102">EstimateFrequency operation</span></span>

<span data-ttu-id="59e21-103">Naam ruimte: [micro soft. Quantum. karakte Rise](xref:Microsoft.Quantum.Characterization) ring</span><span class="sxs-lookup"><span data-stu-id="59e21-103">Namespace: [Microsoft.Quantum.Characterization](xref:Microsoft.Quantum.Characterization)</span></span>

<span data-ttu-id="59e21-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="59e21-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="59e21-105">Op basis van een voor bereiding en meting, schat de frequentie waarmee deze meting slaagt (retourneert `Zero` ) door een bepaald aantal experimenten uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="59e21-105">Given a preparation and measurement, estimates the frequency with which that measurement succeeds (returns `Zero`) by performing a given number of trials.</span></span>

```qsharp
operation EstimateFrequency (preparation : (Qubit[] => Unit), measurement : (Qubit[] => Result), nQubits : Int, nMeasurements : Int) : Double
```


## <a name="input"></a><span data-ttu-id="59e21-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="59e21-106">Input</span></span>

### <a name="preparation--qubit--unit"></a><span data-ttu-id="59e21-107">voor bereiding: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] =>- [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="59e21-107">preparation : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="59e21-108">Een bewerking $P $ die een bepaalde status $ \rho $ voorbereidt op de invoer register.</span><span class="sxs-lookup"><span data-stu-id="59e21-108">An operation $P$ that prepares a given state $\rho$ on its input register.</span></span>


### <a name="measurement--qubit--__invalidresult__"></a><span data-ttu-id="59e21-109">meting: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => __ongeldig <Result>__</span><span class="sxs-lookup"><span data-stu-id="59e21-109">measurement : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => __invalid<Result>__</span></span> 

<span data-ttu-id="59e21-110">Een bewerking $M $ die de afmeting van de interesse vertegenwoordigt.</span><span class="sxs-lookup"><span data-stu-id="59e21-110">An operation $M$ representing the measurement of interest.</span></span>


### <a name="nqubits--int"></a><span data-ttu-id="59e21-111">nQubits: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="59e21-111">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="59e21-112">Het aantal qubits waarop de voor bereiding en meting elke handeling uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="59e21-112">The number of qubits on which the preparation and measurement each act.</span></span>


### <a name="nmeasurements--int"></a><span data-ttu-id="59e21-113">nMeasurements: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="59e21-113">nMeasurements : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="59e21-114">Het aantal keren dat de meting moet worden uitgevoerd om de frequentie van de interesse te schatten.</span><span class="sxs-lookup"><span data-stu-id="59e21-114">The number of times that the measurement should be performed in order to estimate the frequency of interest.</span></span>



## <a name="output--double"></a><span data-ttu-id="59e21-115">Uitvoer: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="59e21-115">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="59e21-116">Een schatting $ \hat{p} $ van de frequentie waarmee $M (P (\ket{00 \cdots 0} \bra{00 \cdots 0})) $ retourneert `Zero` , verkregen met behulp van de niet-verwerkte binomiale Estimator $ \hat{p} = n \_ {\uparrow}/n \_ {\Text{measurements}} $, waarbij $n \_ {\uparrow} $ het aantal `Zero` waargenomen resultaten is.</span><span class="sxs-lookup"><span data-stu-id="59e21-116">An estimate $\hat{p}$ of the frequency with which $M(P(\ket{00 \cdots 0}\bra{00 \cdots 0}))$ returns `Zero`, obtained using the unbiased binomial estimator $\hat{p} = n\_{\uparrow} / n\_{\text{measurements}}$, where $n\_{\uparrow}$ is the number of `Zero` results observed.</span></span>

<span data-ttu-id="59e21-117">Dit is met name belang rijk voor doel computers die fysieke beperkingen eerbiedigen, zodat er waarschijnlijk niet kan worden gemeten.</span><span class="sxs-lookup"><span data-stu-id="59e21-117">This is particularly important on target machines which respect physical limitations, such that probabilities cannot be measured.</span></span>