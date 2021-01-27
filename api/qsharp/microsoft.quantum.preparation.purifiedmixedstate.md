---
uid: Microsoft.Quantum.Preparation.PurifiedMixedState
title: De functie PurifiedMixedState
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PurifiedMixedState
qsharp.summary: "Returns an operation that prepares a a purification of a given mixed state.\rA \"purified mixed state\" refers to states of the form |ψ⟩ = Σᵢ √\U0001D45Dᵢ |\U0001D456⟩ |garbageᵢ⟩ specified by a vector of\rcoefficients {\U0001D45Dᵢ}. States of this form can be reduced to mixed states ρ ≔ \U0001D45Dᵢ |\U0001D456⟩⟨\U0001D456| by tracing over the \"garbage\"\rregister (that is, a mixed state that is diagonal in the computational basis).\r\rSee https://arxiv.org/pdf/1805.03662.pdf?page=15 for further discussion."
ms.openlocfilehash: 594a1d9fa674e457ab88072ade4198283b677af6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854293"
---
# <a name="purifiedmixedstate-function"></a>De functie PurifiedMixedState

Naam ruimte: [micro soft. Quantum. prepare](xref:Microsoft.Quantum.Preparation)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Retourneert een bewerking die een zuivering van een bepaalde gemengde status voorbereidt.
Een ' zuivere gemengde status ' verwijst naar de statussen van het formulier | ψ ⟩ = σi √ Pi | i ⟩ | garbagei ⟩, opgegeven door een vector van coëfficiënten {pi}. De statussen van dit formulier kunnen worden verkleind tot gemengde statussen ρ ≔ Pi | i ⟩ ⟨ i | door over te trekken van de registratie van ' garbage ' (dat wil zeggen, een gemengde status die diagonaal is in de berekening).

Zie https://arxiv.org/pdf/1805.03662.pdf?page=15 voor meer discussie.

```qsharp
function PurifiedMixedState (targetError : Double, coefficients : Double[]) : Microsoft.Quantum.Preparation.MixedStatePreparation
```


## <a name="description"></a>Beschrijving

Maakt gebruik van de Quantum ROM-techniek om een opgegeven dichtheids matrix weer te geven. deze representatie wordt geretourneerd als een status voorbereidings bewerking.

Met name een lijst van $N $-coëfficiënten $ \ alpha_j $, deze functie retourneert een bewerking die gebruikmaakt van de Quantum ROM-techniek om een benadering voor te bereiden $ $ \begin{align} \tilde\rho = \ sum_ {j = 0} ^ {N-1} p_j \ket{j}\bra{j} \end{align} $ $ van de gemengde status $ $ \begin{align} \rho = \ sum_ {j = 0} ^ {N-1} \ FRAC {| alpha_j |} {\ sum_k | \ alpha_k |} \ket{j}\bra{j}, \end{align} $ $ waarbij elke $p _j $ een benadering is van de gegeven coëfficiënt $ \ alpha_j $, \begin{align} \left | p_j-\frac{| \ alpha_j |} {\ sum_k | \ alpha_k |} \le \frac{\epsilon}{N} \end{align} $ $ voor elke $j $.

Bij het door gegeven van een index register en een REGI ster van garbage qubits, in eerste instantie van de status $ \ket {0} \ket{00\cdots 0} bereidt de geretourneerde bewerking beide registers voor op de zuivering van $ \tilde \rho $, $ $ \begin{align} \ sum_ {j = 0} ^ {N-1} \sqrt{p_j} \ket{j}\ket{\text{garbage} _J}, \end{align} $ $, waardoor het opnieuw instellen en ongedaan maken van de garbage collector de gewenste voor bereiding krijgt in de doel fout

## <a name="input"></a>Invoer

### <a name="targeterror--double"></a>targetError: [dubbel](xref:microsoft.quantum.lang-ref.double)

De doel fout $ \epsilon $.


### <a name="coefficients--double"></a>coëfficiënten: [dubbel](xref:microsoft.quantum.lang-ref.double)[]

Matrix van $N $-coëfficiënten waarmee de kans op basis status wordt opgegeven.
Negatieve getallen $-\ alpha_j $ worden behandeld als positieve waarde $ | \ alpha_j | $.



## <a name="output--mixedstatepreparation"></a>Uitvoer: [MixedStatePreparation](xref:Microsoft.Quantum.Preparation.MixedStatePreparation)

Een bewerking waarbij $ \tilde \rho $ als zuivering wordt voor bereid op een gemeen schappelijke index en een schone registratie.

## <a name="example"></a>Voorbeeld

Het volgende code fragment bereidt een zuivering van de $3 $-Qubit-status $ \rho = \ sum_ {j = 0} ^ {4} \frac{| alpha_j |} {\ sum_k | \ alpha_k |} \ket{j}\bra{j} $, waarbij $ \vec\alpha = (1.0, 2,0, 3,0, 4,0, 5,0) $, en de doel fout is $10 ^ {-3} $:

```qsharp
let coefficients = [1.0, 2.0, 3.0, 4.0, 5.0];
let targetError = 1e-3;
let purifiedState = PurifiedMixedState(targetError, coefficients);
using (indexRegister = Qubit[purifiedState::Requirements::NIndexQubits]) {
    using (garbageRegister = Qubit[purifiedState::Requirements::NGarbageQubits]) {
        purifiedState::Prepare(LittleEndian(indexRegister), new Qubit[0], garbageRegister);
    }
}
```

## <a name="remarks"></a>Opmerkingen

De coëfficiënten die aan deze bewerking worden gegeven, worden genormaliseerd volgens de 1-norm, zodat de coëfficiënten altijd worden beschouwd als een geldige categorische-kans-distributie.

## <a name="references"></a>Verwijzingen

- Versleutelen van elektronische spectra in Quantum circuits met lineaire T complexiteit Ryan Babbush, Craig Gidney, Dominic W. Berry, Nathan Wiebe, Jarrod McClean, Alexandru pastel, Austin Fowler, Hartmut neven https://arxiv.org/abs/1805.03662

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. prepare. PurifiedMixedStateWithData](xref:Microsoft.Quantum.Preparation.PurifiedMixedStateWithData)