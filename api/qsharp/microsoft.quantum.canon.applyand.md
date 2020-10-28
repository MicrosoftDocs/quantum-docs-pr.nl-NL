---
uid: Microsoft.Quantum.Canon.ApplyAnd
title: Bewerking ApplyAnd
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyAnd
qsharp.summary: Inverts a given target qubit if and only if both control qubits are in the 1 state, using measurement to perform the adjoint operation.
ms.openlocfilehash: 5a4e18cb0361708e1fc00e8d62c0a6c2415d6bed
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705501"
---
# <a name="applyand-operation"></a>Bewerking ApplyAnd

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket [](https://nuget.org/packages/)


Hiermee wordt een bepaalde doel-Qubit als en alleen als beide besturings qubits de status 1 hebben, met behulp van meting om de adjoint-bewerking uit te voeren.

```qsharp
operation ApplyAnd (control1 : Qubit, control2 : Qubit, target : Qubit) : Unit
```


## <a name="description"></a>Beschrijving

Keert `target` alleen als beide besturings elementen 1 zijn, maar er wordt van uitgegaan dat de `target` status 0 is.  De bewerking heeft T-Count 4, T-diepte 2 en vereist geen helper Qubit. Dit kan daarom de voor keur hebben voor een CCNOT-bewerking, als `target` bekend is dat deze 0 is.  De adjoint van deze bewerking is gebaseerd op metingen en vereist geen T-poorten.

De beheerde toepassing van deze bewerking vereist geen Qubit, `2^c` `Rz` poorten en is niet geoptimaliseerd voor diepte, waarbij `c` het aantal algemene besturings elementen qubits, met inbegrip van de twee controles van de `ApplyAnd` bewerking.  De door adjoint beheerde toepassing vereist `2^c - 1` `Rz` poorten (met een hoek van twee keer de grootte van de niet-adjoint bewerking), geen helper-Qubit en is niet geoptimaliseerd voor diepte.

## <a name="input"></a>Invoer

### <a name="control1--qubit"></a>control1: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Eerste besturings element Qubit


### <a name="control2--qubit"></a>control2: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Qubit voor het tweede besturings element


### <a name="target--qubit"></a>doel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Doel hulp Qubit; moet de status 0 hebben



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="references"></a>Naslaginformatie

- Cody Jones: ' nieuwe constructies voor de fout tolerante Toffoli-Gate ', fysiek. Rev. A 87, 022328, 2013 [arXiv: 1212.5069](https://arxiv.org/abs/1212.5069) DOI: 10.1103/PhysRevA. 87.022328
- Craig Gidney: "de kosten van een Quantum toevoeging", Quantum 2, pagina 74, 2018 [arXiv: 1709.06648](https://arxiv.org/abs/1709.06648) DOI: 10.1103/PhysRevA. 85.044302
- Mathias soeken: "Quantum Oracle-circuits en het patroon voor kerst boom", [blog artikel van 19 December 2019](https://msoeken.github.io/blog_qac.html) (Opmerking: uitleg over de meerdere bewaakte constructie)