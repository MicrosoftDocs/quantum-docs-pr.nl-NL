---
uid: Microsoft.Quantum.Characterization.SingleQubitProcessTomographyMeasurement
title: Bewerking SingleQubitProcessTomographyMeasurement
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: SingleQubitProcessTomographyMeasurement
qsharp.summary: Performs a single-qubit process tomography measurement in the Pauli basis, given a particular channel of interest.
ms.openlocfilehash: 3756040df8e34ecee1e968428b08387e0096ab7b
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96204195"
---
# <a name="singlequbitprocesstomographymeasurement-operation"></a><span data-ttu-id="ad61e-102">Bewerking SingleQubitProcessTomographyMeasurement</span><span class="sxs-lookup"><span data-stu-id="ad61e-102">SingleQubitProcessTomographyMeasurement operation</span></span>

<span data-ttu-id="ad61e-103">Naam ruimte: [micro soft. Quantum. karakte Rise](xref:Microsoft.Quantum.Characterization) ring</span><span class="sxs-lookup"><span data-stu-id="ad61e-103">Namespace: [Microsoft.Quantum.Characterization](xref:Microsoft.Quantum.Characterization)</span></span>

<span data-ttu-id="ad61e-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ad61e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ad61e-105">Hiermee wordt een Qubit-proces tomography meting uitgevoerd in de Pauli, op basis van een bepaald kanaal van belang.</span><span class="sxs-lookup"><span data-stu-id="ad61e-105">Performs a single-qubit process tomography measurement in the Pauli basis, given a particular channel of interest.</span></span>

```qsharp
operation SingleQubitProcessTomographyMeasurement (preparation : Pauli, measurement : Pauli, channel : (Qubit => Unit)) : Result
```


## <a name="input"></a><span data-ttu-id="ad61e-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="ad61e-106">Input</span></span>

### <a name="preparation--pauli"></a><span data-ttu-id="ad61e-107">voor bereiding: [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="ad61e-107">preparation : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="ad61e-108">Het Pauli basis element $P $ waarin een Qubit moet worden voor bereid.</span><span class="sxs-lookup"><span data-stu-id="ad61e-108">The Pauli basis element $P$ in which a qubit is to be prepared.</span></span>


### <a name="measurement--pauli"></a><span data-ttu-id="ad61e-109">meting: [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="ad61e-109">measurement : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="ad61e-110">Het Pauli basis element $Q $ waarin een Qubit moet worden gemeten.</span><span class="sxs-lookup"><span data-stu-id="ad61e-110">The Pauli basis element $Q$ in which a qubit is to be measured.</span></span>


### <a name="channel--qubit--unit"></a><span data-ttu-id="ad61e-111">kanaal: [Qubit](xref:microsoft.quantum.lang-ref.qubit) - => [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ad61e-111">channel : [Qubit](xref:microsoft.quantum.lang-ref.qubit) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="ad61e-112">Eén Qubit-kanaal $ \Lambda $ waarvan het gedrag wordt geschat met Process tomography.</span><span class="sxs-lookup"><span data-stu-id="ad61e-112">A single qubit channel $\Lambda$ whose behavior is being estimated with process tomography.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="ad61e-113">Uitvoer: __ongeldig <Result>__</span><span class="sxs-lookup"><span data-stu-id="ad61e-113">Output : __invalid<Result>__</span></span>

<span data-ttu-id="ad61e-114">Het resultaat `Zero` met kans $ $ \Begin{align} \Pr (\texttt{Zero} | \Lambda; P, Q) = \operatorname{Tr}\left (\frac{\boldone + Q} {2} \Lambda\left [\frac{\boldone + P} {2} \right] \right).</span><span class="sxs-lookup"><span data-stu-id="ad61e-114">The Result `Zero` with probability $$ \begin{align} \Pr(\texttt{Zero} | \Lambda; P, Q) = \operatorname{Tr}\left( \frac{\boldone + Q}{2} \Lambda\left[ \frac{\boldone + P}{2} \right] \right).</span></span>
<span data-ttu-id="ad61e-115">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="ad61e-115">\end{align} $$</span></span>

## <a name="remarks"></a><span data-ttu-id="ad61e-116">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="ad61e-116">Remarks</span></span>

<span data-ttu-id="ad61e-117">De verdeling over de resultaten die door deze bewerking worden geretourneerd, is een speciaal geval van een tomography-status van twee Qubit.</span><span class="sxs-lookup"><span data-stu-id="ad61e-117">The distribution over results returned by this operation is a special case of two-qubit state tomography.</span></span> <span data-ttu-id="ad61e-118">Laat $ \rho = J (\Lambda)/$2 de status Choi-Jamiłkowski voor $ \Lambda $ zijn.</span><span class="sxs-lookup"><span data-stu-id="ad61e-118">Let $\rho = J(\Lambda) / 2$ be the Choi–Jamiłkowski state for $\Lambda$.</span></span> <span data-ttu-id="ad61e-119">De bovenstaande distributie is dan identiek aan $ $ \begin{align} \Pr (\texttt{Zero} | \rho; M) = \operatorname{Tr} (M \rho), \end{align} $ $ waarbij $M = 2 (\boldone + P) ^ \mathrm{T}/2 \cdot (\boldone + Q)/$2 de daad werkelijke meting is die overeenkomt met $P $ en $Q $.</span><span class="sxs-lookup"><span data-stu-id="ad61e-119">Then, the distribution above is identical to $$ \begin{align} \Pr(\texttt{Zero} | \rho; M) = \operatorname{Tr}(M \rho), \end{align} $$ where $M = 2 (\boldone + P)^\mathrm{T} / 2 \cdot (\boldone + Q) / 2$ is the effective measurement corresponding to $P$ and $Q$.</span></span>