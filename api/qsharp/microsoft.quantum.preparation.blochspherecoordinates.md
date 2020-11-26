---
uid: Microsoft.Quantum.Preparation.BlochSphereCoordinates
title: De functie BlochSphereCoordinates
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: BlochSphereCoordinates
qsharp.summary: >-
  Computes the Bloch sphere coordinates for a single-qubit state.

  Given two complex numbers $a0, a1$ that represent the qubit state, computes coordinates on the Bloch sphere such that $a0 \ket{0} + a1 \ket{1} = r e^{it}(e^{-i \phi /2}\cos{(\theta/2)}\ket{0}+e^{i \phi /2}\sin{(\theta/2)}\ket{1})$.
ms.openlocfilehash: 594896a72fe40e5ba994e08500c3ce71b185bfff
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96193553"
---
# <a name="blochspherecoordinates-function"></a>De functie BlochSphereCoordinates

Naam ruimte: [micro soft. Quantum. prepare](xref:Microsoft.Quantum.Preparation)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Berekent de Bloch Sphere-coördinaten voor een status met één Qubit.

Met twee complexe getallen $a 0, a1 $ die de status Qubit vertegenwoordigen, worden de coördinaten van de Bloch-bol berekend, zodat $a 0 \ket {0} + a1 \ket {1} = r e ^ {it} (e ^ {-i \phi/2}\cos{(\ theta/2)} \ket {0} + e ^ {i \phi/2}\sin{(\ theta/2)} \ket {1} ) $.

```qsharp
function BlochSphereCoordinates (a0 : Microsoft.Quantum.Math.ComplexPolar, a1 : Microsoft.Quantum.Math.ComplexPolar) : (Microsoft.Quantum.Math.ComplexPolar, Double, Double)
```


## <a name="input"></a>Invoer

### <a name="a0--complexpolar"></a>a0: [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)

Complexe coëfficiënt van status $ \ket {0} $.


### <a name="a1--complexpolar"></a>a1: [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)

Complexe coëfficiënt van status $ \ket {1} $.



## <a name="output--complexpolardoubledouble"></a>Uitvoer: ([ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar),[Double](xref:microsoft.quantum.lang-ref.double),[Double](xref:microsoft.quantum.lang-ref.double))

Een tupel met `(ComplexPolar(r, t), phi, theta)` .