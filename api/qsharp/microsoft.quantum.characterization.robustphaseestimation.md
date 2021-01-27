---
uid: Microsoft.Quantum.Characterization.RobustPhaseEstimation
title: Bewerking RobustPhaseEstimation
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: RobustPhaseEstimation
qsharp.summary: Performs the robust non-iterative quantum phase estimation algorithm for a given oracle `U` and eigenstate, and provides a single real-valued estimate of the phase with variance scaling at the Heisenberg limit.
ms.openlocfilehash: 4b37c8275a5b2aee8534bacc5831281aa498b57d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851804"
---
# <a name="robustphaseestimation-operation"></a><span data-ttu-id="af655-102">Bewerking RobustPhaseEstimation</span><span class="sxs-lookup"><span data-stu-id="af655-102">RobustPhaseEstimation operation</span></span>

<span data-ttu-id="af655-103">Naam ruimte: [micro soft. Quantum. karakte Rise](xref:Microsoft.Quantum.Characterization) ring</span><span class="sxs-lookup"><span data-stu-id="af655-103">Namespace: [Microsoft.Quantum.Characterization](xref:Microsoft.Quantum.Characterization)</span></span>

<span data-ttu-id="af655-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="af655-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="af655-105">Voert het robuuste algoritme voor het schatten van de niet-iteratieve Quantum fase voor een bepaalde Oracle `U` -en eigenstate en biedt een enkele geschatte schatting van de fase met variantie schaaling bij de Heisenberg-limiet.</span><span class="sxs-lookup"><span data-stu-id="af655-105">Performs the robust non-iterative quantum phase estimation algorithm for a given oracle `U` and eigenstate, and provides a single real-valued estimate of the phase with variance scaling at the Heisenberg limit.</span></span>

```qsharp
operation RobustPhaseEstimation (bitsPrecision : Int, oracle : Microsoft.Quantum.Oracles.DiscreteOracle, targetState : Qubit[]) : Double
```


## <a name="input"></a><span data-ttu-id="af655-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="af655-106">Input</span></span>

### <a name="bitsprecision--int"></a><span data-ttu-id="af655-107">bitsPrecision: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="af655-107">bitsPrecision : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="af655-108">Dit biedt een schatting van $ \phi $ met de standaard afwijking $ \sigma \le 2 \ pi/2 ^ \text{bitsPrecision} $ met behulp van een aantal query's dat kan worden geschaald zoals $ \sigma \le 10,7 \pi/\Text{# van query's} $.</span><span class="sxs-lookup"><span data-stu-id="af655-108">This provides an estimate of $\phi$ with standard deviation $\sigma \le 2\pi / 2^\text{bitsPrecision}$ using a number of queries scaling like $\sigma \le 10.7 \pi / \text{# of queries}$.</span></span>


### <a name="oracle--discreteoracle"></a><span data-ttu-id="af655-109">Oracle: [DiscreteOracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle)</span><span class="sxs-lookup"><span data-stu-id="af655-109">oracle : [DiscreteOracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle)</span></span>

<span data-ttu-id="af655-110">Een bewerking die $U ^ m $ implementeert voor gegeven geheeltallige maat regelen, $m $.</span><span class="sxs-lookup"><span data-stu-id="af655-110">An operation implementing $U^m$ for given integer powers $m$.</span></span>


### <a name="targetstate--qubit"></a><span data-ttu-id="af655-111">targetState: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="af655-111">targetState : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="af655-112">Een Quantum registratie waarmee $ wordt $U.</span><span class="sxs-lookup"><span data-stu-id="af655-112">A quantum register that $U$ acts on.</span></span> <span data-ttu-id="af655-113">Als er een eigenstate $ \ket{\phi} $ van $U $ wordt opgeslagen, wordt $U \ket{\phi} = e ^ {i\phi} \ket{\phi} $ voor $ \phi\in (-\pi, \pi] $ een onbekende fase.</span><span class="sxs-lookup"><span data-stu-id="af655-113">If it stores an eigenstate $\ket{\phi}$ of $U$, then $U\ket{\phi} = e^{i\phi} \ket{\phi}$ for $\phi\in(-\pi,\pi]$ an unknown phase.</span></span>



## <a name="output--double"></a><span data-ttu-id="af655-114">Uitvoer: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="af655-114">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>



## <a name="remarks"></a><span data-ttu-id="af655-115">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="af655-115">Remarks</span></span>

<span data-ttu-id="af655-116">In de limiet van een groot aantal query's Cramer-Rao lagere grenzen voor de standaard afwijking van de schatting van $ \phi $ voldoen aan $ \sigma \ge 2 \pi/\Text{# van query's} $.</span><span class="sxs-lookup"><span data-stu-id="af655-116">In the limit of a large number of queries, Cramer-Rao lower bounds for the standard deviation of the estimate of $\phi$ satisfy $\sigma \ge 2 \pi / \text{# of queries}$.</span></span>

## <a name="references"></a><span data-ttu-id="af655-117">Verwijzingen</span><span class="sxs-lookup"><span data-stu-id="af655-117">References</span></span>

- <span data-ttu-id="af655-118">Robuuste kalibratie van een universele Single-Qubit Gate-Set via een robuuste fase schatting Shelby Kimmel, Guang Hao low, Theodore J. Yoder https://arxiv.org/abs/1502.02677</span><span class="sxs-lookup"><span data-stu-id="af655-118">Robust Calibration of a Universal Single-Qubit Gate-Set via Robust Phase Estimation Shelby Kimmel, Guang Hao Low, Theodore J. Yoder https://arxiv.org/abs/1502.02677</span></span>