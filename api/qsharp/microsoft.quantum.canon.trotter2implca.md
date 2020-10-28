---
uid: Microsoft.Quantum.Canon.Trotter2ImplCA
title: Bewerking Trotter2ImplCA
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Trotter2ImplCA
qsharp.summary: Implementation of the second-order Trotter–Suzuki integrator.
ms.openlocfilehash: 98ba4db45fa7b7e8f442ba166929142aac4fa5a4
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703755"
---
# <a name="trotter2implca-operation"></a>Bewerking Trotter2ImplCA

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket [](https://nuget.org/packages/)


Implementatie van de tweede order Trotter – Suzuki integrator.

```qsharp
operation Trotter2ImplCA<'T> ((nSteps : Int, op : ((Int, Double, 'T) => Unit is Adj + Ctl)), stepSize : Double, target : 'T) : Unit
```


## <a name="input"></a>Invoer

### <a name="nsteps--int"></a>nSteps: [int](xref:microsoft.quantum.lang-ref.int)

Het aantal bewerkingen dat moet worden uitgesplitst in tijd stappen.


### <a name="op--intdoublet--unit-adj--ctl"></a>op: ([int](xref:microsoft.quantum.lang-ref.int),[Double](xref:microsoft.quantum.lang-ref.double), 't) => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL

Een bewerking die een index-invoer (type `Int` ) en een tijd-invoer (type `Double` ) en een Quantum register (type `'T` ) voor de ontleding accepteert.


### <a name="stepsize--double"></a>stepSize: [dubbel](xref:microsoft.quantum.lang-ref.double)

Vermenigvuldiger op grootte van elke stap van de simulatie.


### <a name="target--t"></a>doel: 'T

Een Quantum registratie waarop de bewerkingen worden uitgevoerd.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T

Het type waarvoor elke stap moet worden uitgevoerd; normaal gesp roken, ofwel `Qubit[]` of `Qubit` .