---
uid: Microsoft.Quantum.Chemistry.JordanWigner.PrepareSparseMultiConfigurationalState
title: Bewerking PrepareSparseMultiConfigurationalState
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: PrepareSparseMultiConfigurationalState
qsharp.summary: Sparse multi-configurational state preparation of trial state by adding excitations to initial trial state.
ms.openlocfilehash: 1182f79a33784cdb49cb13db5cc97a0a45e59f9f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703130"
---
# <a name="preparesparsemulticonfigurationalstate-operation"></a><span data-ttu-id="2904b-102">Bewerking PrepareSparseMultiConfigurationalState</span><span class="sxs-lookup"><span data-stu-id="2904b-102">PrepareSparseMultiConfigurationalState operation</span></span>

<span data-ttu-id="2904b-103">Naam ruimte: [micro soft. Quantum. chemie. JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="2904b-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="2904b-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="2904b-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="2904b-105">Sparse status van de proef versie van de evaluatie periode voor meerdere configuraties door aanstellingen toe te voegen aan de status van de eerste proef versie.</span><span class="sxs-lookup"><span data-stu-id="2904b-105">Sparse multi-configurational state preparation of trial state by adding excitations to initial trial state.</span></span>

```qsharp
operation PrepareSparseMultiConfigurationalState (initialStatePreparation : (Qubit[] => Unit), excitations : Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerInputState[], qubits : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="2904b-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="2904b-106">Input</span></span>

### <a name="initialstatepreparation--qubit--unit"></a><span data-ttu-id="2904b-107">initialStatePreparation: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] =>- [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="2904b-107">initialStatePreparation : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="2904b-108">Unitary om de status van de eerste proef versie voor te bereiden.</span><span class="sxs-lookup"><span data-stu-id="2904b-108">Unitary to prepare initial trial state.</span></span>


### <a name="excitations--jordanwignerinputstate"></a><span data-ttu-id="2904b-109">bekrachtigingen: [JordanWignerInputState](xref:Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerInputState)[]</span><span class="sxs-lookup"><span data-stu-id="2904b-109">excitations : [JordanWignerInputState](xref:Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerInputState)[]</span></span>

<span data-ttu-id="2904b-110">Door de amplitude van de aandrijf acties gestarte statussen van de eerste proef versie en Qubit indices worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="2904b-110">Excitations of initial trial state represented by the amplitude of the excitation and the qubit indices the excitation acts on.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="2904b-111">qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="2904b-111">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="2904b-112">Qubits van Hamiltonian.</span><span class="sxs-lookup"><span data-stu-id="2904b-112">Qubits of Hamiltonian.</span></span>



## <a name="output--unit"></a><span data-ttu-id="2904b-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="2904b-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>
