---
uid: Microsoft.Quantum.Characterization.EstimateFrequencyA
title: Bewerking EstimateFrequencyA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: EstimateFrequencyA
qsharp.summary: Given a preparation that is adjointable and measurement, estimates the frequency with which that measurement succeeds (returns `Zero`) by performing a given number of trials.
ms.openlocfilehash: 6cca8dff70283e0d69441db8a5b31fb5bfb3082a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98839916"
---
# <a name="estimatefrequencya-operation"></a><span data-ttu-id="6fde0-102">Bewerking EstimateFrequencyA</span><span class="sxs-lookup"><span data-stu-id="6fde0-102">EstimateFrequencyA operation</span></span>

<span data-ttu-id="6fde0-103">Naam ruimte: [micro soft. Quantum. karakte Rise](xref:Microsoft.Quantum.Characterization) ring</span><span class="sxs-lookup"><span data-stu-id="6fde0-103">Namespace: [Microsoft.Quantum.Characterization](xref:Microsoft.Quantum.Characterization)</span></span>

<span data-ttu-id="6fde0-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="6fde0-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="6fde0-105">Op basis van een voor bereiding die adjointable en meting levert, wordt een schatting gemaakt van de frequentie waarmee deze meting slaagt (retourneert `Zero` ) door een bepaald aantal experimenten uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="6fde0-105">Given a preparation that is adjointable and measurement, estimates the frequency with which that measurement succeeds (returns `Zero`) by performing a given number of trials.</span></span>

```qsharp
operation EstimateFrequencyA (preparation : (Qubit[] => Unit is Adj), measurement : (Qubit[] => Result), nQubits : Int, nMeasurements : Int) : Double
```


## <a name="input"></a><span data-ttu-id="6fde0-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="6fde0-106">Input</span></span>

### <a name="preparation--qubit--unit--is-adj"></a><span data-ttu-id="6fde0-107">voor bereiding: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ</span><span class="sxs-lookup"><span data-stu-id="6fde0-107">preparation : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="6fde0-108">Een adjointable-bewerking $P $ die een bepaalde status $ \rho $ voorbereidt op de invoer register.</span><span class="sxs-lookup"><span data-stu-id="6fde0-108">An adjointable operation $P$ that prepares a given state $\rho$ on its input register.</span></span>


### <a name="measurement--qubit--__invalidresult__"></a><span data-ttu-id="6fde0-109">meting: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => __ongeldig <Result>__</span><span class="sxs-lookup"><span data-stu-id="6fde0-109">measurement : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => __invalid<Result>__</span></span> 

<span data-ttu-id="6fde0-110">Een bewerking $M $ die de afmeting van de interesse vertegenwoordigt.</span><span class="sxs-lookup"><span data-stu-id="6fde0-110">An operation $M$ representing the measurement of interest.</span></span>


### <a name="nqubits--int"></a><span data-ttu-id="6fde0-111">nQubits: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="6fde0-111">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="6fde0-112">Het aantal qubits waarop de voor bereiding en meting elke handeling uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="6fde0-112">The number of qubits on which the preparation and measurement each act.</span></span>


### <a name="nmeasurements--int"></a><span data-ttu-id="6fde0-113">nMeasurements: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="6fde0-113">nMeasurements : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="6fde0-114">Het aantal keren dat de meting moet worden uitgevoerd om de frequentie van de interesse te schatten.</span><span class="sxs-lookup"><span data-stu-id="6fde0-114">The number of times that the measurement should be performed in order to estimate the frequency of interest.</span></span>



## <a name="output--double"></a><span data-ttu-id="6fde0-115">Uitvoer: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="6fde0-115">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="6fde0-116">Een schatting $ \hat{p} $ van de frequentie waarmee $M (P (\ket{00 \cdots 0} \bra{00 \cdots 0})) $ retourneert `Zero` , verkregen met behulp van de niet-verwerkte binomiale Estimator $ \hat{p} = n \_ {\uparrow}/n \_ {\Text{measurements}} $, waarbij $n \_ {\uparrow} $ het aantal `Zero` waargenomen resultaten is.</span><span class="sxs-lookup"><span data-stu-id="6fde0-116">An estimate $\hat{p}$ of the frequency with which $M(P(\ket{00 \cdots 0}\bra{00 \cdots 0}))$ returns `Zero`, obtained using the unbiased binomial estimator $\hat{p} = n\_{\uparrow} / n\_{\text{measurements}}$, where $n\_{\uparrow}$ is the number of `Zero` results observed.</span></span>

## <a name="remarks"></a><span data-ttu-id="6fde0-117">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="6fde0-117">Remarks</span></span>

<span data-ttu-id="6fde0-118">Voor adjointable-bewerkingen kunnen bepaalde hypo Thesen worden gemaakt, zoals het aanroepen van de bewerking, wordt de qubits voor bereid op exact dezelfde staat, zodat doel machines een aantal prestatie optimalisaties mogelijk maken.</span><span class="sxs-lookup"><span data-stu-id="6fde0-118">For adjointable operations, certain assumptions can be made such like calling the operation will prepare the qubits to exactly the same state, which allow target machines to make some performance optimizations.</span></span>