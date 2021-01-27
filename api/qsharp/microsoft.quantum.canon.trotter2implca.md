---
uid: Microsoft.Quantum.Canon.Trotter2ImplCA
title: Bewerking Trotter2ImplCA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Trotter2ImplCA
qsharp.summary: Implementation of the second-order Trotter–Suzuki integrator.
ms.openlocfilehash: 34b60934b67c19b2d1d718d68b85a2f0fffeab5d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852020"
---
# <a name="trotter2implca-operation"></a>Bewerking Trotter2ImplCA

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Implementatie van de tweede order Trotter – Suzuki integrator.

```qsharp
operation Trotter2ImplCA<'T> ((nSteps : Int, op : ((Int, Double, 'T) => Unit is Adj + Ctl)), stepSize : Double, target : 'T) : Unit is Adj + Ctl
```


## <a name="input"></a>Invoer

### <a name="nsteps--int"></a>nSteps: [int](xref:microsoft.quantum.lang-ref.int)

Het aantal bewerkingen dat moet worden uitgesplitst in tijd stappen.


### <a name="op--intdoublet--unit--is-adj--ctl"></a>op: ([int](xref:microsoft.quantum.lang-ref.int),[Double](xref:microsoft.quantum.lang-ref.double), 't) => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL

Een bewerking die een index-invoer (type `Int` ) en een tijd-invoer (type `Double` ) en een Quantum register (type `'T` ) voor de ontleding accepteert.


### <a name="stepsize--double"></a>stepSize: [dubbel](xref:microsoft.quantum.lang-ref.double)

Vermenigvuldiger op grootte van elke stap van de simulatie.


### <a name="target--t"></a>doel: 'T

Een Quantum registratie waarop de bewerkingen worden uitgevoerd.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T

Het type waarvoor elke stap moet worden uitgevoerd; normaal gesp roken, ofwel `Qubit[]` of `Qubit` .

## <a name="example"></a>Voorbeeld

De volgende zijn gelijkwaardig:

```qsharp
op(0, deltaT / 2.0, target);
op(1, deltaT / 2.0, target);
op(1, deltaT / 2.0, target);
op(0, deltaT / 2.0, target);
```

en

```qsharp
Trotter2ImplCA((2, op), deltaT, target);
```