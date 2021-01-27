---
uid: Microsoft.Quantum.Characterization.EstimateFrequency
title: Bewerking EstimateFrequency
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: EstimateFrequency
qsharp.summary: Given a preparation and measurement, estimates the frequency with which that measurement succeeds (returns `Zero`) by performing a given number of trials.
ms.openlocfilehash: 1e044a08718e02d673edab1d6b9d16d7f09618dc
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851886"
---
# <a name="estimatefrequency-operation"></a><span data-ttu-id="8195e-102">Bewerking EstimateFrequency</span><span class="sxs-lookup"><span data-stu-id="8195e-102">EstimateFrequency operation</span></span>

<span data-ttu-id="8195e-103">Naam ruimte: [micro soft. Quantum. karakte Rise](xref:Microsoft.Quantum.Characterization) ring</span><span class="sxs-lookup"><span data-stu-id="8195e-103">Namespace: [Microsoft.Quantum.Characterization](xref:Microsoft.Quantum.Characterization)</span></span>

<span data-ttu-id="8195e-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="8195e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="8195e-105">Op basis van een voor bereiding en meting, schat de frequentie waarmee deze meting slaagt (retourneert `Zero` ) door een bepaald aantal experimenten uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="8195e-105">Given a preparation and measurement, estimates the frequency with which that measurement succeeds (returns `Zero`) by performing a given number of trials.</span></span>

```qsharp
operation EstimateFrequency (preparation : (Qubit[] => Unit), measurement : (Qubit[] => Result), nQubits : Int, nMeasurements : Int) : Double
```


## <a name="input"></a><span data-ttu-id="8195e-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="8195e-106">Input</span></span>

### <a name="preparation--qubit--unit"></a><span data-ttu-id="8195e-107">voor bereiding: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] =>- [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="8195e-107">preparation : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="8195e-108">Een bewerking $P $ die een bepaalde status $ \rho $ voorbereidt op de invoer register.</span><span class="sxs-lookup"><span data-stu-id="8195e-108">An operation $P$ that prepares a given state $\rho$ on its input register.</span></span>


### <a name="measurement--qubit--__invalidresult__"></a><span data-ttu-id="8195e-109">meting: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => __ongeldig <Result>__</span><span class="sxs-lookup"><span data-stu-id="8195e-109">measurement : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => __invalid<Result>__</span></span> 

<span data-ttu-id="8195e-110">Een bewerking $M $ die de afmeting van de interesse vertegenwoordigt.</span><span class="sxs-lookup"><span data-stu-id="8195e-110">An operation $M$ representing the measurement of interest.</span></span>


### <a name="nqubits--int"></a><span data-ttu-id="8195e-111">nQubits: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="8195e-111">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="8195e-112">Het aantal qubits waarop de voor bereiding en meting elke handeling uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="8195e-112">The number of qubits on which the preparation and measurement each act.</span></span>


### <a name="nmeasurements--int"></a><span data-ttu-id="8195e-113">nMeasurements: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="8195e-113">nMeasurements : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="8195e-114">Het aantal keren dat de meting moet worden uitgevoerd om de frequentie van de interesse te schatten.</span><span class="sxs-lookup"><span data-stu-id="8195e-114">The number of times that the measurement should be performed in order to estimate the frequency of interest.</span></span>



## <a name="output--double"></a><span data-ttu-id="8195e-115">Uitvoer: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="8195e-115">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="8195e-116">Een schatting $ \hat{p} $ van de frequentie waarmee $M (P (\ket{00 \cdots 0} \bra{00 \cdots 0})) $ retourneert `Zero` , verkregen met behulp van de niet-verwerkte binomiale Estimator $ \hat{p} = n \_ {\uparrow}/n \_ {\Text{measurements}} $, waarbij $n \_ {\uparrow} $ het aantal `Zero` waargenomen resultaten is.</span><span class="sxs-lookup"><span data-stu-id="8195e-116">An estimate $\hat{p}$ of the frequency with which $M(P(\ket{00 \cdots 0}\bra{00 \cdots 0}))$ returns `Zero`, obtained using the unbiased binomial estimator $\hat{p} = n\_{\uparrow} / n\_{\text{measurements}}$, where $n\_{\uparrow}$ is the number of `Zero` results observed.</span></span>

<span data-ttu-id="8195e-117">Dit is met name belang rijk voor doel computers die fysieke beperkingen eerbiedigen, zodat er waarschijnlijk niet kan worden gemeten.</span><span class="sxs-lookup"><span data-stu-id="8195e-117">This is particularly important on target machines which respect physical limitations, such that probabilities cannot be measured.</span></span>