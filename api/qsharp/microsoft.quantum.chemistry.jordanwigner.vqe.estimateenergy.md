---
uid: Microsoft.Quantum.Chemistry.JordanWigner.VQE.EstimateEnergy
title: Bewerking EstimateEnergy
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner.VQE
qsharp.name: EstimateEnergy
qsharp.summary: Estimates the energy of the molecule by summing the energy contributed by the individual Jordan-Wigner terms.
ms.openlocfilehash: 52e527a68818c80f93bc177d3563064fd0f2aea3
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703088"
---
# <a name="estimateenergy-operation"></a>Bewerking EstimateEnergy

Naam ruimte: [micro soft. Quantum. chemie. JordanWigner. VQE](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)

Pakket [](https://nuget.org/packages/)


Maakt een schatting van de energie van het molecuul door het opsommen van de energie die door de afzonderlijke Jordan-Wignerings voorwaarden wordt bijgedragen.

```qsharp
operation EstimateEnergy (jwHamiltonian : Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerEncodingData, nSamples : Int) : Double
```


## <a name="description"></a>Beschrijving

Deze bewerking is impliciet afhankelijk van de indexerings Conventie omhoog en omlaag.

## <a name="input"></a>Invoer

### <a name="jwhamiltonian--jordanwignerencodingdata"></a>jwHamiltonian: [JordanWignerEncodingData](xref:Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerEncodingData)

De Jordan-Wigner Hamiltonian.


### <a name="nsamples--int"></a>nSamples: [int](xref:microsoft.quantum.lang-ref.int)

Het aantal steek proeven dat moet worden gebruikt voor de schatting van de verwachtingen van de term.



## <a name="output--double"></a>Uitvoer: [dubbel](xref:microsoft.quantum.lang-ref.double)

De geschatte energie van het molecuul