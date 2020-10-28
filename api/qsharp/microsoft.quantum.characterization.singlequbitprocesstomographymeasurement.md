---
uid: Microsoft.Quantum.Characterization.SingleQubitProcessTomographyMeasurement
title: Bewerking SingleQubitProcessTomographyMeasurement
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: SingleQubitProcessTomographyMeasurement
qsharp.summary: Performs a single-qubit process tomography measurement in the Pauli basis, given a particular channel of interest.
ms.openlocfilehash: 34e5143d5be316ee42a63124d35475949db0a692
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703592"
---
# <a name="singlequbitprocesstomographymeasurement-operation"></a><span data-ttu-id="892cd-102">Bewerking SingleQubitProcessTomographyMeasurement</span><span class="sxs-lookup"><span data-stu-id="892cd-102">SingleQubitProcessTomographyMeasurement operation</span></span>

<span data-ttu-id="892cd-103">Naam ruimte: [micro soft. Quantum. karakte Rise](xref:Microsoft.Quantum.Characterization) ring</span><span class="sxs-lookup"><span data-stu-id="892cd-103">Namespace: [Microsoft.Quantum.Characterization](xref:Microsoft.Quantum.Characterization)</span></span>

<span data-ttu-id="892cd-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="892cd-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="892cd-105">Hiermee wordt een Qubit-proces tomography meting uitgevoerd in de Pauli, op basis van een bepaald kanaal van belang.</span><span class="sxs-lookup"><span data-stu-id="892cd-105">Performs a single-qubit process tomography measurement in the Pauli basis, given a particular channel of interest.</span></span>

```qsharp
operation SingleQubitProcessTomographyMeasurement (preparation : Pauli, measurement : Pauli, channel : (Qubit => Unit)) : Result
```


## <a name="input"></a><span data-ttu-id="892cd-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="892cd-106">Input</span></span>

### <a name="preparation--pauli"></a><span data-ttu-id="892cd-107">voor bereiding: [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="892cd-107">preparation : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="892cd-108">Het Pauli basis element $P $ waarin een Qubit moet worden voor bereid.</span><span class="sxs-lookup"><span data-stu-id="892cd-108">The Pauli basis element $P$ in which a qubit is to be prepared.</span></span>


### <a name="measurement--pauli"></a><span data-ttu-id="892cd-109">meting: [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="892cd-109">measurement : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="892cd-110">Het Pauli basis element $Q $ waarin een Qubit moet worden gemeten.</span><span class="sxs-lookup"><span data-stu-id="892cd-110">The Pauli basis element $Q$ in which a qubit is to be measured.</span></span>


### <a name="channel--qubit--unit"></a><span data-ttu-id="892cd-111">kanaal: [Qubit](xref:microsoft.quantum.lang-ref.qubit) - => [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="892cd-111">channel : [Qubit](xref:microsoft.quantum.lang-ref.qubit) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="892cd-112">Eén Qubit-kanaal $ \Lambda $ waarvan het gedrag wordt geschat met Process tomography.</span><span class="sxs-lookup"><span data-stu-id="892cd-112">A single qubit channel $\Lambda$ whose behavior is being estimated with process tomography.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="892cd-113">Uitvoer: __ongeldig <Result>__</span><span class="sxs-lookup"><span data-stu-id="892cd-113">Output : __invalid<Result>__</span></span>

<span data-ttu-id="892cd-114">Het resultaat `Zero` met kans $ $ \Begin{align} \Pr (\texttt{Zero} | \Lambda; P, Q) = \operatorname{Tr}\left (\frac{\boldone + Q} {2} \Lambda\left [\frac{\boldone + P} {2} \right] \right).</span><span class="sxs-lookup"><span data-stu-id="892cd-114">The Result `Zero` with probability $$ \begin{align} \Pr(\texttt{Zero} | \Lambda; P, Q) = \operatorname{Tr}\left( \frac{\boldone + Q}{2} \Lambda\left[ \frac{\boldone + P}{2} \right] \right).</span></span>
<span data-ttu-id="892cd-115">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="892cd-115">\end{align} $$</span></span>

## <a name="remarks"></a><span data-ttu-id="892cd-116">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="892cd-116">Remarks</span></span>

<span data-ttu-id="892cd-117">De verdeling over de resultaten die door deze bewerking worden geretourneerd, is een speciaal geval van een tomography-status van twee Qubit.</span><span class="sxs-lookup"><span data-stu-id="892cd-117">The distribution over results returned by this operation is a special case of two-qubit state tomography.</span></span> <span data-ttu-id="892cd-118">Laat $ \rho = J (\Lambda)/$2 de status Choi-Jamiłkowski voor $ \Lambda $ zijn.</span><span class="sxs-lookup"><span data-stu-id="892cd-118">Let $\rho = J(\Lambda) / 2$ be the Choi–Jamiłkowski state for $\Lambda$.</span></span> <span data-ttu-id="892cd-119">De bovenstaande distributie is dan identiek aan $ $ \begin{align} \Pr (\texttt{Zero} | \rho; M) = \operatorname{Tr} (M \rho), \end{align} $ $ waarbij $M = 2 (\boldone + P) ^ \mathrm{T}/2 \cdot (\boldone + Q)/$2 de daad werkelijke meting is die overeenkomt met $P $ en $Q $.</span><span class="sxs-lookup"><span data-stu-id="892cd-119">Then, the distribution above is identical to $$ \begin{align} \Pr(\texttt{Zero} | \rho; M) = \operatorname{Tr}(M \rho), \end{align} $$ where $M = 2 (\boldone + P)^\mathrm{T} / 2 \cdot (\boldone + Q) / 2$ is the effective measurement corresponding to $P$ and $Q$.</span></span>