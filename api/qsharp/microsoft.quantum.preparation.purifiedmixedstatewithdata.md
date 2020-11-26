---
uid: Microsoft.Quantum.Preparation.PurifiedMixedStateWithData
title: De functie PurifiedMixedStateWithData
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PurifiedMixedStateWithData
qsharp.summary: "Returns an operation that prepares a a purification of a given mixed\rstate, entangled with a register representing a given collection of data.\rA \"purified mixed state with data\" refers to a state of the form Σᵢ √\U0001D45Dᵢ |\U0001D456⟩ |\U0001D465ᵢ⟩ |garbageᵢ⟩,\rwhere each \U0001D465ᵢ is a bitstring encoding additional data associated with the register |\U0001D456⟩.\r\rSee https://arxiv.org/pdf/1805.03662.pdf?page=15 for further discussion."
ms.openlocfilehash: c89ee8f5df58e5d6b154b67d2b39db208bc8a215
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96229950"
---
# <a name="purifiedmixedstatewithdata-function"></a>De functie PurifiedMixedStateWithData

Naam ruimte: [micro soft. Quantum. prepare](xref:Microsoft.Quantum.Preparation)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Retourneert een bewerking die een zuivering van een bepaalde gemengde status voorbereidt, Entangled met een REGI ster dat een bepaalde verzameling gegevens vertegenwoordigt.
Een ' zuivere gemengde status met gegevens ' verwijst naar een status van de vorm σi √ Pi | i ⟩ | XI ⟩ | garbagei ⟩, waarbij elke XI een bitstring is voor het coderen van extra gegevens die zijn gekoppeld aan de kassa | i ⟩.

Zie https://arxiv.org/pdf/1805.03662.pdf?page=15 voor meer discussie.

```qsharp
function PurifiedMixedStateWithData (targetError : Double, coefficients : (Double, Bool[])[]) : Microsoft.Quantum.Preparation.MixedStatePreparation
```


## <a name="description"></a>Beschrijving

Maakt gebruik van de Quantum ROM-techniek om een opgegeven dichtheids matrix weer te geven. deze representatie wordt geretourneerd als een status voorbereidings bewerking.

Met name een lijst van $N $ coëfficiënten $ \ alpha_j $ en een bitstring $ \vec{x}_j $ die is gekoppeld aan elke coëfficiënt, deze functie retourneert een bewerking die gebruikmaakt van de Quantum rom-techniek om een benadering voor te bereiden $ $ \begin{align} \tilde\rho = \sum_{j = 0} ^ {N-1} p_j \ket{j}\bra{j} \otimes \ket{\vec{x} _J} \bra{\vec{x}_j} \end{align} $ $ van de gemengde status $ $ \begin{align} \rho = \sum_{j = 0} ^ {N-1} \ FRAC {| alpha_j |} {\ sum_k | \ alpha_k |} \ket{j}\bra{j} \otimes \ket{\vec{x} _j} \bra{\vec{x} _j}, \end{align} $ $ waarbij elke $p _j $ een benadering is van de gegeven coëfficiënt $ \ alpha_j $, zoals $ $ \begin{align} \left | p_j-\frac{| \ alpha_j |} {\ sum_k | \ alpha_k |} \le \frac{\epsilon}{N} \end{align} $ $ voor elke $j $.

Bij het door gegeven van een index register en een REGI ster van garbage qubits, in eerste instantie in de status $ \ket {0} \ket{00\cdots 0}, met de geretourneerde bewerking worden beide registers voor bereid op de zuivering van $ \tilde \rho $, $ $ \begin{align} \ sum_ {j = 0} ^ {N-1} \sqrt{p_j} \ket{j} \ket{\vec{x} _J} \ket{\text{garbage} _J}, \end{align} $ $, waardoor het opnieuw instellen en ongedaan maken van de garbagecollection de gewenste voor bereiding krijgt in de doel fout $ \epsilon $.

## <a name="input"></a>Invoer

### <a name="targeterror--double"></a>targetError: [dubbel](xref:microsoft.quantum.lang-ref.double)

De doel fout $ \epsilon $.


### <a name="coefficients--doublebool"></a>coëfficiënten: ([dubbel](xref:microsoft.quantum.lang-ref.double),[BOOL](xref:microsoft.quantum.lang-ref.bool)[]) []

Matrix van $N $ coëfficiënten waarmee de kans van basis status wordt opgegeven, samen met de bitstring $ \vec{x} _j $ die aan elke coëfficiënt is gekoppeld.
Negatieve getallen $-\ alpha_j $ worden behandeld als positieve waarde $ | \ alpha_j | $.



## <a name="output--mixedstatepreparation"></a>Uitvoer: [MixedStatePreparation](xref:Microsoft.Quantum.Preparation.MixedStatePreparation)

Een bewerking waarbij $ \tilde \rho $ als zuivering wordt voor bereid op een gemeen schappelijke index en een schone registratie.

## <a name="remarks"></a>Opmerkingen

De coëfficiënten die aan deze bewerking worden gegeven, worden genormaliseerd volgens de 1-norm, zodat de coëfficiënten altijd worden beschouwd als een geldige categorische-kans-distributie.

## <a name="references"></a>Referenties

- Versleutelen van elektronische spectra in Quantum circuits met lineaire T complexiteit Ryan Babbush, Craig Gidney, Dominic W. Berry, Nathan Wiebe, Jarrod McClean, Alexandru pastel, Austin Fowler, Hartmut neven https://arxiv.org/abs/1805.03662

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. prepare. PurifiedMixedState](xref:Microsoft.Quantum.Preparation.PurifiedMixedState)