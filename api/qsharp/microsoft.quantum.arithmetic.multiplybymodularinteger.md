---
uid: Microsoft.Quantum.Arithmetic.MultiplyByModularInteger
title: Bewerking MultiplyByModularInteger
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MultiplyByModularInteger
qsharp.summary: Performs modular multiplication by an integer constant on a qubit register.
ms.openlocfilehash: 6deced7862ab4cb74315219eaaab97380cdf0f92
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706389"
---
# <a name="multiplybymodularinteger-operation"></a>Bewerking MultiplyByModularInteger

Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)

Pakket [](https://nuget.org/packages/)


Voert modulaire vermenigvuldiging uit met een gehele constante in een Qubit-REGI ster.

```qsharp
operation MultiplyByModularInteger (constMultiplier : Int, modulus : Int, multiplier : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="description"></a>Beschrijving

Laat het ons weten `modulus` door $N $ en `constMultiplier` door $a $.
Met deze bewerking wordt een unitary-bewerking geïmplementeerd die is gedefinieerd door de volgende kaart op basis van de berekening: $ $ \begin{align} \ket{y} \mapsto \ket{(a \cdot y) \operatorname{mod} N} \end{align} $ $ voor alle $y $ tussen $0 $ en $N-$1.

## <a name="input"></a>Invoer

### <a name="constmultiplier--int"></a>constMultiplier: [int](xref:microsoft.quantum.lang-ref.int)

De constante waarmee vermenigvuldiger wordt vermenigvuldigd. Moet een combi natie zijn van de modulus.


### <a name="modulus--int"></a>modulus: [int](xref:microsoft.quantum.lang-ref.int)

De vermenigvuldigings bewerking wordt modulo uitgevoerd `modulus` .


### <a name="multiplier--littleendian"></a>vermenigvuldiger: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Het getal dat door een constante wordt vermenigvuldigd.
Dit is een matrix met qubits-code ring: een geheel getal in de indeling little-endian.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Opmerkingen

- Zie afbeelding 7 op [pagina 8 van arXiv: Quant-pH/0205095v3](https://arxiv.org/pdf/quant-ph/0205095v3.pdf#page=8) voor het circuit diagram en de uitleg.
- Deze bewerking komt overeen met U ₐ in [arXiv: Quant-pH/0205095v3](https://arxiv.org/pdf/quant-ph/0205095v3.pdf)