---
title: Pauli metingen
description: Meer informatie over het werken met single-en multi-Qubit Pauli-meet bewerkingen.
author: QuantumWriter
uid: microsoft.quantum.concepts.pauli
ms.author: nawiebe@microsoft.com
ms.date: 12/11/2017
ms.topic: article
no-loc:
- $
- $
- '\cdots'
- bmatrix
- '\ddots'
- '\equiv'
- '\sum'
- '\begin'
- '\end'
- '\sqrt'
- '\otimes'
- '{'
- '}'
- '\text'
- '\phi'
- '\kappa'
- '\psi'
- '\alpha'
- '\beta'
- '\gamma'
- '\delta'
- '\omega'
- '\bra'
- '\ket'
- '\boldone'
- '\\\\'
- '\\'
- =
- '\frac'
- '\text'
- '\mapsto'
- '\dagger'
- '\to'
- "\begin{cases}"
- "\end{cases}"
- '\operatorname'
- '\braket'
- '\id'
- '\expect'
- '\defeq'
- '\variance'
- '\dd'
- '&'
- "\begin{align}"
- "\end{align}"
- '\Lambda'
- '\lambda'
- '\Omega'
- '\mathrm'
- '\left'
- '\right'
- '\qquad'
- '\times'
- '\big'
- '\langle'
- '\rangle'
- '\bigg'
- '\Big'
- '|'
- '\mathbb'
- '\vec'
- '\in'
- '\texttt'
- '\ne'
- <
- '>'
- '\leq'
- '\geq'
- ~~
- "~"
ms.openlocfilehash: 115c1703e433f24930e4be61b545048c95da28d1
ms.sourcegitcommit: e23178d32b316d05784a02ba3cd6166dad177e89
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/09/2020
ms.locfileid: "84630305"
---
# <a name="pauli-measurements"></a><span data-ttu-id="91a90-103">Pauli metingen</span><span class="sxs-lookup"><span data-stu-id="91a90-103">Pauli Measurements</span></span>

<span data-ttu-id="91a90-104">In de vorige discussies hebben we gestreefd naar reken kundige basis metingen.</span><span class="sxs-lookup"><span data-stu-id="91a90-104">In the previous discussions, we have focused on computational basis measurements.</span></span>
<span data-ttu-id="91a90-105">Er zijn ook andere algemene metingen die zich voordoen bij Quantum Computing en die, vanuit een notatie perspectief, handig zijn om te worden uitgedrukt in termen van reken kundige basis metingen.</span><span class="sxs-lookup"><span data-stu-id="91a90-105">In fact, there are other common measurements that occur in quantum computing that, from a notational perspective, are convenient to express in terms of computational basis measurements.</span></span>
<span data-ttu-id="91a90-106">Terwijl u met Q # werkt, zijn de meest voorkomende maat eenheden die u in de hand hebt, waarschijnlijk *Paulie metingen*, waarmee reken kundige basis metingen kunnen worden gemeten in andere bases en van de pariteit tussen verschillende qubits.</span><span class="sxs-lookup"><span data-stu-id="91a90-106">As you work with Q#, the most common kind of measurements that you'll run into will likely be *Pauli measurements*, which generalize computational basis measurements to include measurements in other bases, and of parity between different qubits.</span></span>
<span data-ttu-id="91a90-107">In dergelijke gevallen is het gebruikelijk om de meting van een Pauli-operator te bespreken, in het algemeen een operator zoals $X, Y, Z $ of $Z \otimes Z, x \otimes x, x \otimes Y enzovoort $ .</span><span class="sxs-lookup"><span data-stu-id="91a90-107">In such cases, it is common to discuss measuring a Pauli operator, in general an operator such as $X,Y,Z$ or $Z\otimes Z, X\otimes X, X\otimes Y$, and so forth.</span></span>

> [!TIP]
> <span data-ttu-id="91a90-108">In Q # worden Opera tors met meerdere Qubit Pauli doorgaans vertegenwoordigd door matrixen van het type `Pauli[]` .</span><span class="sxs-lookup"><span data-stu-id="91a90-108">In Q#, multi-qubit Pauli operators are generally represented by arrays of type `Pauli[]`.</span></span>
> <span data-ttu-id="91a90-109">Als u bijvoorbeeld $X \otimes Z \otimes Y wilt weer geven $ , kunt u de matrix gebruiken `[PauliX, PauliZ, PauliY]` .</span><span class="sxs-lookup"><span data-stu-id="91a90-109">For example, to represent $X \otimes Z \otimes Y$, you can use the array `[PauliX, PauliZ, PauliY]`.</span></span>

<span data-ttu-id="91a90-110">Het bespreken van metingen in termen van Pauli-Opera Tors is vooral gebruikelijk in het subveld van Quantum fout correctie.</span><span class="sxs-lookup"><span data-stu-id="91a90-110">Discussing measurement in terms of Pauli operators is especially common in the subfield of quantum error correction.</span></span>
<span data-ttu-id="91a90-111">In Q # volgen we een vergelijk bare Conventie; We verklaren nu deze alternatieve weer gave van metingen.</span><span class="sxs-lookup"><span data-stu-id="91a90-111">In Q#, we follow a similar convention; we now explain this alternative view of measurements.</span></span>

<span data-ttu-id="91a90-112">Voordat u meer informatie krijgt over hoe u een Pauli meting kunt zien, is het handig om te zien wat het meten van één Qubit in een quantum computer met de Quantum status is.</span><span class="sxs-lookup"><span data-stu-id="91a90-112">Before delving into the details of how to think of a Pauli measurement, it is useful to think about what measuring a single qubit inside a quantum computer does to the quantum state.</span></span>
<span data-ttu-id="91a90-113">Stel dat er sprake is $ van een $n Quantum-Qubit. vervolgens wordt een Qubit voor de helft van de $2 ^ n $ mogelijkheden waarvan de status mogelijk is, weer gemeten.</span><span class="sxs-lookup"><span data-stu-id="91a90-113">Imagine that we have an $n$-qubit quantum state; then measuring one qubit immediately rules out half of the $2^n$ possibilities that state could be in.</span></span>
<span data-ttu-id="91a90-114">Met andere woorden, de meting projecteert de Quantum status op een van de twee halve ruimtes.</span><span class="sxs-lookup"><span data-stu-id="91a90-114">In other words, the measurement projects the quantum state onto one of two half-spaces.</span></span>
<span data-ttu-id="91a90-115">We kunnen het beste bepalen hoe de meting wordt toegepast op deze intuition.</span><span class="sxs-lookup"><span data-stu-id="91a90-115">We can generalize the way we think about measurement to reflect this intuition.</span></span>

<span data-ttu-id="91a90-116">Om deze subruimten te kunnen identificeren, hebben we een taal nodig om ze te beschrijven.</span><span class="sxs-lookup"><span data-stu-id="91a90-116">In order to concisely identify these subspaces, we need a language for describing them.</span></span>
<span data-ttu-id="91a90-117">Een manier om de twee subruimten te beschrijven, is door ze op te geven via een matrix die slechts twee unieke eigenvalues heeft, die door de conventies voor $ \pm 1 worden gebruikt $ .</span><span class="sxs-lookup"><span data-stu-id="91a90-117">One way to describe the two subspaces is by specifying them through a matrix that just has two unique eigenvalues, taken by convention to be $\pm 1$.</span></span>
<span data-ttu-id="91a90-118">Voor een eenvoudig voor beeld van het beschrijven van subruimten op deze manier kunt u $Z $ :</span><span class="sxs-lookup"><span data-stu-id="91a90-118">For a simple example of describing subspaces in this way, consider $Z$:</span></span>

<span data-ttu-id="91a90-119">$ $ \begin{align}</span><span class="sxs-lookup"><span data-stu-id="91a90-119">$$ \begin{align}</span></span>
  <span data-ttu-id="91a90-120">Z & = \begin{ bmatrix } 1 & 0 \\ \\ 0 &-1 \end{ bmatrix } .</span><span class="sxs-lookup"><span data-stu-id="91a90-120">Z & = \begin{bmatrix} 1 & 0 \\\\ 0 & -1 \end{bmatrix}.</span></span>
<span data-ttu-id="91a90-121">\end{align}</span><span class="sxs-lookup"><span data-stu-id="91a90-121">\end{align}</span></span>
$$

<span data-ttu-id="91a90-122">Door de diagonale elementen van de matrix met Pauli-$Z te lezen $ , kunnen we zien dat $Z $ twee eigenvectors heeft, $ \ket{0 } $ en $ \ket{1 } $, met bijbehorende eigenvalues $ \pm 1 $ .</span><span class="sxs-lookup"><span data-stu-id="91a90-122">By reading the diagonal elements of the Pauli-$Z$ matrix, we can see that $Z$ has two eigenvectors, $\ket{0}$ and $\ket{1}$, with corresponding eigenvalues $\pm 1$.</span></span>
<span data-ttu-id="91a90-123">Als we de Qubit meten en `Zero` (overeenkomen met de status $ \ket{0 } $), weten we dat de status van onze Qubit een $ + 1- $ eigenstate van de operator $Z is $ .</span><span class="sxs-lookup"><span data-stu-id="91a90-123">Thus, if we measure the qubit and obtain `Zero` (corresponding to the state $\ket{0}$), we know that the state of our qubit is a $+1$ eigenstate of the $Z$ operator.</span></span>
<span data-ttu-id="91a90-124">Op dezelfde manier `One` weten we dat de status van onze Qubit een $-1- $ eigenstate van $Z is $ .</span><span class="sxs-lookup"><span data-stu-id="91a90-124">Similarly, if we obtain `One`, we know that the state of our qubit is a $-1$ eigenstate of $Z$.</span></span>
<span data-ttu-id="91a90-125">Dit proces wordt aangeduid met de taal van Pauli-metingen als ' meet Pauli $Z $ ' en is volledig gelijk aan het uitvoeren van een reken kundige basis meting.</span><span class="sxs-lookup"><span data-stu-id="91a90-125">This process is referred to in the language of Pauli measurements as "measuring Pauli $Z$," and is entirely equivalent to performing a computational basis measurement.</span></span>

<span data-ttu-id="91a90-126">Een \times $ matrix van $2 2 die een unitary-trans formatie van $Z $ ook voldoet aan deze criteria.</span><span class="sxs-lookup"><span data-stu-id="91a90-126">Any $2\times 2$ matrix that is a unitary transformation of $Z$ also satisfies this criteria.</span></span>
<span data-ttu-id="91a90-127">Dat wil zeggen dat we ook een matrix $A = U ^ \dagger Z U gebruiken $ , waarbij $U een $ andere unitary-matrix is, om een matrix te geven waarin de twee uitkomsten van een meting in de $ \pm 1-eigenvectors worden gedefinieerd $ .</span><span class="sxs-lookup"><span data-stu-id="91a90-127">That is, we could also use a matrix $A=U^\dagger Z U$, where $U$ is any other unitary matrix, to give a matrix that defines the two outcomes of a measurement in its $\pm 1$ eigenvectors.</span></span>
<span data-ttu-id="91a90-128">De notatie van Pauli metingen verwijst naar deze unitary-equivalentie door $X, Y, Z- $ metingen als gelijkwaardige waarden te identificeren die een kan doen om informatie van een Qubit te verkrijgen.</span><span class="sxs-lookup"><span data-stu-id="91a90-128">The notation of Pauli measurements references this unitary equivalence by identifying $X,Y,Z$ measurements as equivalent measurements that one could do to gain information from a qubit.</span></span>
<span data-ttu-id="91a90-129">Deze metingen worden hieronder vermeld voor het gemak.</span><span class="sxs-lookup"><span data-stu-id="91a90-129">These measurements are given below for convenience.</span></span>


|<span data-ttu-id="91a90-130">Pauli meting</span><span class="sxs-lookup"><span data-stu-id="91a90-130">Pauli Measurement</span></span>  |<span data-ttu-id="91a90-131">Unitary-trans formatie</span><span class="sxs-lookup"><span data-stu-id="91a90-131">Unitary transformation</span></span>  |
|-------------------|------------------------|
| <span data-ttu-id="91a90-132">$Z$</span><span class="sxs-lookup"><span data-stu-id="91a90-132">$Z$</span></span>               | <span data-ttu-id="91a90-133">$ \boldone$</span><span class="sxs-lookup"><span data-stu-id="91a90-133">$\boldone$</span></span>             |
| <span data-ttu-id="91a90-134">$X$</span><span class="sxs-lookup"><span data-stu-id="91a90-134">$X$</span></span>               | <span data-ttu-id="91a90-135">$H$</span><span class="sxs-lookup"><span data-stu-id="91a90-135">$H$</span></span>                    |
| <span data-ttu-id="91a90-136">$Y$</span><span class="sxs-lookup"><span data-stu-id="91a90-136">$Y$</span></span>               | <span data-ttu-id="91a90-137">$HS ^ {\dagger}$</span><span class="sxs-lookup"><span data-stu-id="91a90-137">$HS^{\dagger}$</span></span>         |

<span data-ttu-id="91a90-138">Dat wil zeggen, het gebruik van deze taal, ' Measure $Y $ ' is gelijk aan het Toep assen van $HS ^ \dagger $ en het meten van de reken kracht, waarbij [`S`](xref:microsoft.quantum.intrinsic.s) een intrinsieke Quantum bewerking ook wel ' fase Gate ' wordt genoemd en kan worden gesimuleerd door de unitary-matrix</span><span class="sxs-lookup"><span data-stu-id="91a90-138">That is, using this language, "measure $Y$" is equivalent to applying $HS^\dagger$ and then measuring in the computational basis, where [`S`](xref:microsoft.quantum.intrinsic.s) is an intrinsic quantum operation sometimes called the "phase gate," and can be simulated by the unitary matrix</span></span>

<span data-ttu-id="91a90-139">$ $ \begin{align}</span><span class="sxs-lookup"><span data-stu-id="91a90-139">$$ \begin{align}</span></span>
    <span data-ttu-id="91a90-140">S = \begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="91a90-140">S = \begin{bmatrix}</span></span>
        <span data-ttu-id="91a90-141">1 & 0 \\ \\ 0 & ik \end{ bmatrix } .</span><span class="sxs-lookup"><span data-stu-id="91a90-141">1 & 0 \\\\ 0 & i \end{bmatrix}.</span></span>
<span data-ttu-id="91a90-142">\end{align}</span><span class="sxs-lookup"><span data-stu-id="91a90-142">\end{align}</span></span>
$$

<span data-ttu-id="91a90-143">Het is ook gelijk aan het Toep assen van $HS ^ \dagger $ aan de Quantum status vector en vervolgens het meten van $Z $ , zodat de volgende bewerking overeenkomt met `Measure([PauliY], [q])` :</span><span class="sxs-lookup"><span data-stu-id="91a90-143">It is also equivalent to applying $HS^\dagger$ to the quantum state vector and then measuring $Z$, such that the following operation is equivalent to `Measure([PauliY], [q])`:</span></span>

```Q#
operation MeasureY(qubit : Qubit) : Result {
    mutable result = Zero;
    within {
        H(q);
        Adjoint S(q);
    } apply {
        set result = M(q);
    }
    return result;
}
```

<span data-ttu-id="91a90-144">Vervolgens wordt de juiste status gevonden door terug te zetten naar de reken kundige basis, die bedragen om $SH toe $ te passen op de Quantum status vector; in het bovenstaande code fragment wordt de trans formatie teruggeleid naar de reken kracht automatisch door het gebruik van het `within … apply` blok.</span><span class="sxs-lookup"><span data-stu-id="91a90-144">The correct state would then be found by transforming back to the computational basis, which amounts to applying $SH$ to the quantum state vector; in the above snippet, the transformation back to the computational basis is handled automatically by the use of the `within … apply` block.</span></span>

<span data-ttu-id="91a90-145">In Q # zeggen we het resultaat---dat wil zeggen dat de klassieke informatie die is geëxtraheerd uit interactie met de status---wordt gegeven met een `Result` waarde $j \in \\ {\Texttt{Zero } , \texttt{One } \\ } $ die aangeeft of het resultaat zich in $ (-1) ^ j $ eigenspace van de Pauli-operator gemeten.</span><span class="sxs-lookup"><span data-stu-id="91a90-145">In Q#, we say the outcome---that is, the classical information extracted from interacting with the state---is given by a `Result` value $j \in \\{\texttt{Zero}, \texttt{One}\\}$ indicating if the result is in the $(-1)^j$ eigenspace of the Pauli operator measured.</span></span>


## <a name="multiple-qubit-measurements"></a><span data-ttu-id="91a90-146">Metingen met meerdere Qubit</span><span class="sxs-lookup"><span data-stu-id="91a90-146">Multiple-qubit measurements</span></span>

<span data-ttu-id="91a90-147">Metingen van Qubit Pauli-Opera tors worden op dezelfde manier gedefinieerd, zoals u kunt zien van:</span><span class="sxs-lookup"><span data-stu-id="91a90-147">Measurements of multi-qubit Pauli operators are defined similarly, as seen from:</span></span>

<span data-ttu-id="91a90-148">$ $ Z \otimes z = \begin{ bmatrix } 1 &0 &0&0 \\\\ 0 & -1&0&0 \\\\ 0&0 & -1&0 \\\\ 0&0&0&1 \end { bmatrix } .</span><span class="sxs-lookup"><span data-stu-id="91a90-148">$$ Z\otimes Z = \begin{bmatrix}1 &0 &0&0\\\\  0&-1&0&0\\\\ 0&0&-1&0\\\\ 0&0&0&1\end{bmatrix}.</span></span>
$$

<span data-ttu-id="91a90-149">Daarom vormen de tensor-producten van twee Pauli-$Z- $ Opera tors een matrix die bestaat uit twee ruimten die bestaan uit $ + 1 $ en $-1 $ eigenvalues.</span><span class="sxs-lookup"><span data-stu-id="91a90-149">Thus the tensor products of two Pauli-$Z$ operators forms a matrix composed of two spaces consisting of $+1$ and $-1$ eigenvalues.</span></span>
<span data-ttu-id="91a90-150">Net als bij de single-Qubit geldt een halve spatie dat de helft van de toegankelijke vector ruimte deel uitmaakt van de eigenspace $ + 1 $ en de resterende helft naar $1 $ eigenspace.</span><span class="sxs-lookup"><span data-stu-id="91a90-150">As with the single-qubit case, both constitute a half-space meaning that half of the accessible vector space belongs to the $+1$ eigenspace and the remaining half to the $-1$ eigenspace.</span></span>
<span data-ttu-id="91a90-151">Over het algemeen is het eenvoudig om te zien uit de definitie van het tensor-product dat een tensor product van Pauli $Z- $ Opera tors en de identiteit dit ook volgt.</span><span class="sxs-lookup"><span data-stu-id="91a90-151">In general, it is easy to see from the definition of the tensor product that any tensor product of Pauli-$Z$ operators and the identity also obeys this.</span></span>
<span data-ttu-id="91a90-152">Bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="91a90-152">For example,</span></span>

<span data-ttu-id="91a90-153">$ $ \begin{align}</span><span class="sxs-lookup"><span data-stu-id="91a90-153">$$ \begin{align}</span></span>
    <span data-ttu-id="91a90-154">Z \otimes \boldone = \begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="91a90-154">Z \otimes \boldone = \begin{bmatrix}</span></span>
        <span data-ttu-id="91a90-155">1 & 0 & 0 & 0 \\ \\ 0 & 1 & 0 & 0 \\ \\ 0 & 0 &-1 & 0 \\ \\ 0 & 0 & 0 &-1 \end{ bmatrix } .</span><span class="sxs-lookup"><span data-stu-id="91a90-155">1 &  0 &  0 &  0 \\\\ 0 &  1 &  0 &  0 \\\\ 0 &  0 & -1 &  0 \\\\ 0 &  0 &  0 & -1 \end{bmatrix}.</span></span>
<span data-ttu-id="91a90-156">\end{align}</span><span class="sxs-lookup"><span data-stu-id="91a90-156">\end{align}</span></span>
$$

<span data-ttu-id="91a90-157">Net als voorheen worden door elke unitary-trans formatie van dergelijke matrices ook twee halve ruimten beschreven die worden gelabeld door $ \pm 1 $ eigenvalues.</span><span class="sxs-lookup"><span data-stu-id="91a90-157">As before, any unitary transformation of such matrices also describes two half-spaces labeled by $\pm 1$ eigenvalues.</span></span>
<span data-ttu-id="91a90-158">Bijvoorbeeld $X \otimes X = h \otimes h (z \otimes z) h h \otimes $ van de identiteit die $Z = HXH $ .</span><span class="sxs-lookup"><span data-stu-id="91a90-158">For example, $X\otimes X = H\otimes H(Z\otimes Z)H\otimes H$  from the identity that $Z=HXH$.</span></span>
<span data-ttu-id="91a90-159">Net als bij de één-qubite-case kunnen alle twee Qubit Pauli-metingen worden geschreven als $U ^ \dagger (Z \otimes \id) U $ voor $4 \times 4 unitary- $ matrices $U $ .</span><span class="sxs-lookup"><span data-stu-id="91a90-159">Similar to the one-qubit case, all two-qubit Pauli-measurements can be written as $U^\dagger (Z\otimes \id) U$ for $4\times 4$ unitary matrices $U$.</span></span> <span data-ttu-id="91a90-160">De trans formaties in de volgende tabel worden opgesomd.</span><span class="sxs-lookup"><span data-stu-id="91a90-160">We enumerate the transformations in the following table.</span></span>

> [!NOTE]
> <span data-ttu-id="91a90-161">In de onderstaande tabel gebruiken we $ \operatorname{SWAP } $ om aan te geven dat de matrix $ $ \begin{align}</span><span class="sxs-lookup"><span data-stu-id="91a90-161">In the table below, we use $\operatorname{SWAP}$ to indicate the matrix $$ \begin{align}</span></span>
>     <span data-ttu-id="91a90-162">\operatorname{SWAP } & = \left (\begin{matrix}</span><span class="sxs-lookup"><span data-stu-id="91a90-162">\operatorname{SWAP} & = \left(\begin{matrix}</span></span>
>         <span data-ttu-id="91a90-163">1 & 0 & 0 & 0 \\ \\ 0 & 0 & 1 & 0 \\ \\ 0 & 1 & 0 & 0 \\ \\ 0 & 0 & 0 & 1 \end{matrix } \right) \end{align}</span><span class="sxs-lookup"><span data-stu-id="91a90-163">1 & 0 & 0 & 0 \\\\ 0 & 0 & 1 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & 1 \end{matrix}\right) \end{align}</span></span>
> <span data-ttu-id="91a90-164">$ $ wordt gebruikt om de intrinsieke bewerking te simuleren [`SWAP`](xref:microsoft.quantum.intrinsic) .</span><span class="sxs-lookup"><span data-stu-id="91a90-164">$$ used to simulate the intrinsic operation [`SWAP`](xref:microsoft.quantum.intrinsic).</span></span>

|<span data-ttu-id="91a90-165">Pauli meting</span><span class="sxs-lookup"><span data-stu-id="91a90-165">Pauli Measurement</span></span>     |<span data-ttu-id="91a90-166">Unitary-trans formatie</span><span class="sxs-lookup"><span data-stu-id="91a90-166">Unitary transformation</span></span>  |
|----------------------|------------------------|
| <span data-ttu-id="91a90-167">$Z \otimes \boldone$</span><span class="sxs-lookup"><span data-stu-id="91a90-167">$Z \otimes \boldone$</span></span> | <span data-ttu-id="91a90-168">$ \boldone \otimes \boldone$</span><span class="sxs-lookup"><span data-stu-id="91a90-168">$\boldone \otimes \boldone$</span></span> |
| <span data-ttu-id="91a90-169">$Z \otimes \boldone$</span><span class="sxs-lookup"><span data-stu-id="91a90-169">$Z\otimes \boldone$</span></span> | <span data-ttu-id="91a90-170">$ \boldone \otimes \boldone$</span><span class="sxs-lookup"><span data-stu-id="91a90-170">$\boldone\otimes \boldone$</span></span> |
| <span data-ttu-id="91a90-171">$X \otimes \boldone$</span><span class="sxs-lookup"><span data-stu-id="91a90-171">$X\otimes \boldone$</span></span> | <span data-ttu-id="91a90-172">$H \otimes \boldone$</span><span class="sxs-lookup"><span data-stu-id="91a90-172">$H\otimes \boldone$</span></span> |
| <span data-ttu-id="91a90-173">$Y \otimes \boldone$</span><span class="sxs-lookup"><span data-stu-id="91a90-173">$Y\otimes \boldone$</span></span> | <span data-ttu-id="91a90-174">$HS ^ \dagger \otimes \boldone$</span><span class="sxs-lookup"><span data-stu-id="91a90-174">$HS^\dagger\otimes \boldone$</span></span> |
| <span data-ttu-id="91a90-175">$ \boldone \otimes Z$</span><span class="sxs-lookup"><span data-stu-id="91a90-175">$\boldone \otimes Z$</span></span> | <span data-ttu-id="91a90-176">$ \operatorname{SWAP}$</span><span class="sxs-lookup"><span data-stu-id="91a90-176">$\operatorname{SWAP}$</span></span> |
| <span data-ttu-id="91a90-177">$ \boldone \otimes X$</span><span class="sxs-lookup"><span data-stu-id="91a90-177">$\boldone \otimes X$</span></span> | <span data-ttu-id="91a90-178">$ (H \otimes \boldone) \operatorname{swap}$</span><span class="sxs-lookup"><span data-stu-id="91a90-178">$(H\otimes \boldone)\operatorname{SWAP}$</span></span> |
| <span data-ttu-id="91a90-179">$ \boldone \otimes Y$</span><span class="sxs-lookup"><span data-stu-id="91a90-179">$\boldone \otimes Y$</span></span> | <span data-ttu-id="91a90-180">$ (HS ^ \dagger \otimes \boldone) \operatorname{swap}$</span><span class="sxs-lookup"><span data-stu-id="91a90-180">$(HS^\dagger\otimes \boldone)\operatorname{SWAP}$</span></span> |
| <span data-ttu-id="91a90-181">$Z \otimes Z$</span><span class="sxs-lookup"><span data-stu-id="91a90-181">$Z\otimes Z$</span></span> | <span data-ttu-id="91a90-182">$ \operatorname{CNOT } \_ {10}$</span><span class="sxs-lookup"><span data-stu-id="91a90-182">$\operatorname{CNOT}\_{10}$</span></span> |
| <span data-ttu-id="91a90-183">$X \otimes Z$</span><span class="sxs-lookup"><span data-stu-id="91a90-183">$X\otimes Z$</span></span> | <span data-ttu-id="91a90-184">$ \operatorname{CNOT } \_ {10 } (H \otimes \boldone) $</span><span class="sxs-lookup"><span data-stu-id="91a90-184">$\operatorname{CNOT}\_{10}(H\otimes \boldone)$</span></span> |
| <span data-ttu-id="91a90-185">$Y \otimes Z$</span><span class="sxs-lookup"><span data-stu-id="91a90-185">$Y\otimes Z$</span></span> | <span data-ttu-id="91a90-186">$ \operatorname{CNOT } \_ {10 } (HS ^ \dagger \otimes \boldone) $</span><span class="sxs-lookup"><span data-stu-id="91a90-186">$\operatorname{CNOT}\_{10}(HS^\dagger\otimes \boldone)$</span></span> |
| <span data-ttu-id="91a90-187">$Z \otimes X$</span><span class="sxs-lookup"><span data-stu-id="91a90-187">$Z\otimes X$</span></span> | <span data-ttu-id="91a90-188">$ \operatorname{CNOT } \_ {10 } (\boldone \otimes H) $</span><span class="sxs-lookup"><span data-stu-id="91a90-188">$\operatorname{CNOT}\_{10}(\boldone\otimes H)$</span></span> |
| <span data-ttu-id="91a90-189">$X \otimes X$</span><span class="sxs-lookup"><span data-stu-id="91a90-189">$X\otimes X$</span></span> | <span data-ttu-id="91a90-190">$ \operatorname{CNOT } \_ {10 } (h \otimes h) $</span><span class="sxs-lookup"><span data-stu-id="91a90-190">$\operatorname{CNOT}\_{10}(H\otimes H)$</span></span> |
| <span data-ttu-id="91a90-191">$Y \otimes X$</span><span class="sxs-lookup"><span data-stu-id="91a90-191">$Y\otimes X$</span></span> | <span data-ttu-id="91a90-192">$ \operatorname{CNOT } \_ {10 } (HS ^ \dagger \otimes H) $</span><span class="sxs-lookup"><span data-stu-id="91a90-192">$\operatorname{CNOT}\_{10}(HS^\dagger\otimes H)$</span></span> |
| <span data-ttu-id="91a90-193">$Z \otimes Y$</span><span class="sxs-lookup"><span data-stu-id="91a90-193">$Z\otimes Y$</span></span> | <span data-ttu-id="91a90-194">$ \operatorname{CNOT } \_ {10 } (\boldone \otimes HS ^ \dagger) $</span><span class="sxs-lookup"><span data-stu-id="91a90-194">$\operatorname{CNOT}\_{10}(\boldone \otimes HS^\dagger)$</span></span> |
| <span data-ttu-id="91a90-195">$X \otimes Y$</span><span class="sxs-lookup"><span data-stu-id="91a90-195">$X\otimes Y$</span></span> | <span data-ttu-id="91a90-196">$ \operatorname{CNOT } \_ {10 } (H \otimes HS ^ \dagger) $</span><span class="sxs-lookup"><span data-stu-id="91a90-196">$\operatorname{CNOT}\_{10}(H\otimes HS^\dagger)$</span></span> |
| <span data-ttu-id="91a90-197">$Y \otimes Y$</span><span class="sxs-lookup"><span data-stu-id="91a90-197">$Y\otimes Y$</span></span> | <span data-ttu-id="91a90-198">$ \operatorname{CNOT } \_ {10 } (HS ^ \dagger \otimes HS ^ \dagger) $</span><span class="sxs-lookup"><span data-stu-id="91a90-198">$\operatorname{CNOT}\_{10}(HS^\dagger\otimes HS^\dagger)$</span></span> |

<span data-ttu-id="91a90-199">Hier wordt de [`CNOT`](xref:microsoft.quantum.intrinsic.cnot) bewerking weer gegeven om de volgende reden.</span><span class="sxs-lookup"><span data-stu-id="91a90-199">Here, the [`CNOT`](xref:microsoft.quantum.intrinsic.cnot) operation appears for the following reason.</span></span>
<span data-ttu-id="91a90-200">Elke Pauli-meting die geen \boldone-matrix bevat, $ is gelijk aan een unitary om Z te \otimes $Z $ door de bovenstaande reden.</span><span class="sxs-lookup"><span data-stu-id="91a90-200">Each Pauli measurement that does not include the $\boldone$ matrix is equivalent up to a unitary to $Z\otimes Z$ by the above reasoning.</span></span>
<span data-ttu-id="91a90-201">De eigenvalues van $Z \otimes Z $ is alleen afhankelijk van de pariteit van de qubits die alle reken kundige basis vector vormen, en de beheerde-not-bewerkingen dienen deze pariteit te berekenen en op te slaan in de eerste bit.</span><span class="sxs-lookup"><span data-stu-id="91a90-201">The eigenvalues of $Z\otimes Z$ only depend on the parity of the qubits that comprise each computational basis vector, and the controlled-not operations serve to compute this parity and store it in the first bit.</span></span>
<span data-ttu-id="91a90-202">Zodra de eerste bit wordt gemeten, kunnen we de identiteit van de resulterende halve ruimte herstellen, die overeenkomt met het meten van de Pauli-operator.</span><span class="sxs-lookup"><span data-stu-id="91a90-202">Then once the first bit is measured, we can recover the identity of the resultant half-space, which is equivalent to measuring the Pauli operator.</span></span>

<span data-ttu-id="91a90-203">Een aanvullend Opmerking: Hoewel het mogelijk is dat de meting $Z \otimes z $ hetzelfde is als opeenvolgend meet $Z \otimes \mathbb{1 } $ en vervolgens $ \mathbb{1 } \otimes Z $ , zou deze veronderstelling onwaar zijn.</span><span class="sxs-lookup"><span data-stu-id="91a90-203">One additional note: while it may be tempting to assume that measuring $Z\otimes Z$ is the same as sequentially measuring $Z\otimes \mathbb{1}$ and then $\mathbb{1} \otimes Z$, this assumption would be false.</span></span>
<span data-ttu-id="91a90-204">Het meten \otimes van $Z Z $ projecteert de Quantum status in de $ + 1- $ of $-1- $ eigenstate van deze opera tors.</span><span class="sxs-lookup"><span data-stu-id="91a90-204">The reason is that measuring $Z\otimes Z$ projects the quantum state into either the $+1$ or $-1$ eigenstate of these operators.</span></span>
<span data-ttu-id="91a90-205">Meting $Z \otimes \mathbb{1 } $ en vervolgens $ \Mathbb{1 } \otimes z $ projecteert de Quantum status vector eerst op een halve ruimte van $Z \otimes \mathbb{1 } $ en vervolgens op een halve spatie van $ \mathbb{1 } \otimes Z $ . Omdat er vier reken kundige basis vectoren zijn, vermindert het uitvoeren van beide metingen de status naar een vierde spatie en vermindert deze in een enkele reken kundige basis vector.</span><span class="sxs-lookup"><span data-stu-id="91a90-205">Measuring $Z\otimes \mathbb{1}$ and then $\mathbb{1} \otimes Z$ projects the quantum state vector first onto a half space of $Z\otimes \mathbb{1}$ and then onto a half space of $\mathbb{1} \otimes Z$. As there are four computational basis vectors, performing both measurements reduces the state to a quarter-space and hence reduces it to a single computational basis vector.</span></span>

## <a name="correlations-between-qubits"></a><span data-ttu-id="91a90-206">Correlaties tussen qubits</span><span class="sxs-lookup"><span data-stu-id="91a90-206">Correlations between qubits</span></span>
<span data-ttu-id="91a90-207">Een andere manier om te kijken naar het meten van tensor-producten van Pauli-matrices, zoals $X \otimes X $ of $Z \otimes Z $ , is dat met deze metingen u de informatie kunt bekijken die is opgeslagen in de correlaties tussen de twee qubits.</span><span class="sxs-lookup"><span data-stu-id="91a90-207">Another way of looking at measuring tensor products of Pauli matrices such as $X\otimes X$ or $Z\otimes Z$ is that these measurements let you look at information stored in the correlations between the two qubits.</span></span>
<span data-ttu-id="91a90-208">Door $X \otimes \id $ te meten, kunt u zien welke gegevens lokaal zijn opgeslagen in de eerste Qubit.</span><span class="sxs-lookup"><span data-stu-id="91a90-208">Measuring $X\otimes \id$ lets you look at information that is locally stored in the first qubit.</span></span>
<span data-ttu-id="91a90-209">Hoewel beide soorten metingen even waardevol zijn voor Quantum Computing, licht de eerste maal de kracht van Quantum Computing.</span><span class="sxs-lookup"><span data-stu-id="91a90-209">While both types of measurements are equally valuable in quantum computing, the former illuminates the power of quantum computing.</span></span>
<span data-ttu-id="91a90-210">In het geval van Quantum Computing is het vaak dat de informatie die u wilt leren, niet is opgeslagen in een enkele Qubit, maar niet lokaal is opgeslagen in alle qubits en daarom alleen door te kijken door een gemeen schappelijke meting (bijvoorbeeld $Z \otimes Z $ ).</span><span class="sxs-lookup"><span data-stu-id="91a90-210">It reveals that in quantum computing, often the information you wish to learn is not stored in any single qubit but rather stored non-locally in all the qubits at once, and therefore only by looking at it through a joint measurement (e.g. $Z\otimes Z$) does this information become manifest.</span></span>

<span data-ttu-id="91a90-211">In het geval van een fout correctie willen we vaak weten welke fout is opgetreden tijdens het leren over de status die we proberen te beveiligen.</span><span class="sxs-lookup"><span data-stu-id="91a90-211">For example, in error correction, we often wish to learn what error occurred while learning nothing about the state that we're trying to protect.</span></span>
<span data-ttu-id="91a90-212">Het [bit-Flip-code voorbeeld](https://github.com/microsoft/Quantum/tree/master/samples/error-correction/bit-flip-code) toont een voor beeld van hoe u dit kunt doen met behulp van metingen zoals $Z \otimes Z \otimes \id $ en $ \id \Otimes z \otimes z $ .</span><span class="sxs-lookup"><span data-stu-id="91a90-212">The [bit-flip code sample](https://github.com/microsoft/Quantum/tree/master/samples/error-correction/bit-flip-code) shows an example of how you can do that using measurements like $Z \otimes Z \otimes \id$ and $\id \otimes Z \otimes Z$.</span></span>
<!-- TODO: change this to a link to the samples browser as soon as the bit-flip code sample is on-boarded. -->

<span data-ttu-id="91a90-213">Wille keurige Pauli-Opera Tors, zoals $X \otimes Y \Otimes Z \otimes \boldone, $ kunnen ook worden gemeten.</span><span class="sxs-lookup"><span data-stu-id="91a90-213">Arbitrary Pauli operators such as $X\otimes Y \otimes Z \otimes \boldone$ can also be measured.</span></span>
<span data-ttu-id="91a90-214">Al deze tensor-producten van Pauli-Opera tors hebben slechts twee eigenvalues $ \pm 1 $ en beide eigenspaces vormen een halve ruimte van de hele vector ruimte.</span><span class="sxs-lookup"><span data-stu-id="91a90-214">All such tensor products of Pauli operators have only two eigenvalues $\pm 1$ and both eigenspaces constitute half-spaces of the entire vector space.</span></span>
<span data-ttu-id="91a90-215">Daarom vallen ze samen met de hierboven vermelde vereisten.</span><span class="sxs-lookup"><span data-stu-id="91a90-215">Thus they coincide with the requirements stated above.</span></span>

<span data-ttu-id="91a90-216">In Q # retourneert deze metingen $j $ als de meting resulteert in een resultaat in de eigenspace van Sign $ (-1) ^ j $ .</span><span class="sxs-lookup"><span data-stu-id="91a90-216">In Q#, such measurements return $j$ if the measurement yields a result in the eigenspace of sign $(-1)^j$.</span></span>
<span data-ttu-id="91a90-217">Het gebruik van Pauli-metingen als een ingebouwde functie in Q # is nuttig omdat het meten van dergelijke Opera tors lange ketens van besturings-en basis transformaties vereist om de diagonalizing $U Gate te beschrijven $ die nodig is om de bewerking als een tensor product van $Z $ en $ \id te geven $ . Doordat u kunt opgeven dat u een van deze vooraf gedefinieerde metingen wilt uitvoeren, hoeft u zich geen zorgen te maken over het transformeren van de basis, zodat een reken kundige basis meting de benodigde informatie bevat.</span><span class="sxs-lookup"><span data-stu-id="91a90-217">Having Pauli measurements as a built-in feature in Q# is helpful because measuring such operators requires long chains of controlled-NOT gates and basis transformations to describe the diagonalizing $U$ gate needed to express the operation as a tensor product of $Z$ and $\id$. By being able to specify that you wish to do one of these pre-defined measurements, you don't need to worry about how to transform your basis such that a computational basis measurement provides the necessary information.</span></span>
<span data-ttu-id="91a90-218">Q # Hiermee worden alle nood zakelijke trans formaties automatisch voor u verwerkt.</span><span class="sxs-lookup"><span data-stu-id="91a90-218">Q# handles all the necessary basis transformations for you automatically.</span></span>
<span data-ttu-id="91a90-219">Zie de en-bewerkingen voor meer informatie [`Measure`](xref:microsoft.quantum.intrinsic.measure) [`MeasurePaulis`](xref:microsoft.quantum.measurement.measurepaulis) .</span><span class="sxs-lookup"><span data-stu-id="91a90-219">For more information, see the [`Measure`](xref:microsoft.quantum.intrinsic.measure) and [`MeasurePaulis`](xref:microsoft.quantum.measurement.measurepaulis) operations.</span></span>

## <a name="the-no-cloning-theorem"></a><span data-ttu-id="91a90-220">De theorema zonder klonen</span><span class="sxs-lookup"><span data-stu-id="91a90-220">The No-Cloning Theorem</span></span>

<span data-ttu-id="91a90-221">De quantum informatie is krachtig.</span><span class="sxs-lookup"><span data-stu-id="91a90-221">Quantum information is powerful.</span></span>
<span data-ttu-id="91a90-222">Hierdoor kunnen we fantastische dingen doen, zoals factor nummers exponentieel sneller dan de best bekende klassieke algoritmen, of op efficiënte wijze simuleren van gecorreleerde elektroden systemen die klassieke kosten in de praktijk nodig hebben om nauw keurig te simuleren.</span><span class="sxs-lookup"><span data-stu-id="91a90-222">It enables us to do amazing things such as factor numbers exponentially faster than the best known classical algorithms, or efficiently simulate correlated electron systems that classically require exponential cost to simulate accurately.</span></span>
<span data-ttu-id="91a90-223">Er zijn echter beperkingen ten aanzien van de kracht van Quantum Computing.</span><span class="sxs-lookup"><span data-stu-id="91a90-223">However, there are limitations to the power of quantum computing.</span></span>
<span data-ttu-id="91a90-224">Een dergelijke beperking wordt gegeven door de *theorema die niet klonen*.</span><span class="sxs-lookup"><span data-stu-id="91a90-224">One such limitation is given by the *No-Cloning Theorem*.</span></span>

<span data-ttu-id="91a90-225">De theorema zonder klonen is aptly met de naam.</span><span class="sxs-lookup"><span data-stu-id="91a90-225">The No-Cloning Theorem is aptly named.</span></span>
<span data-ttu-id="91a90-226">Het klonen van generieke Quantum Staten door een quantum computer wordt niet toegestaan.</span><span class="sxs-lookup"><span data-stu-id="91a90-226">It disallows cloning of generic quantum states by a quantum computer.</span></span>
<span data-ttu-id="91a90-227">Het bewijs van de theorema is onduidelijker.</span><span class="sxs-lookup"><span data-stu-id="91a90-227">The proof of the theorem is remarkably straightforward.</span></span>
<span data-ttu-id="91a90-228">Hoewel een volledig bewijs van het no-klonen van theorema iets te technisch is voor onze discussie, is de proef in het geval van geen extra hulp qubits binnen onze Scope (hulp qubits worden qubits gebruikt voor Scratch ruimte tijdens een berekening en worden ze eenvoudig gebruikt en beheerd in Q #, Zie [geleed qubits](xref:microsoft.quantum.guide.qubits#borrowed-qubits)).</span><span class="sxs-lookup"><span data-stu-id="91a90-228">While a full proof of the no-cloning theorem is a little too technical for our discussion here, the proof in the case of no additional auxiliary qubits is within our scope (auxiliary qubits are qubits used for scratch space during a computation and are easily used and managed in Q#, see [borrowed qubits](xref:microsoft.quantum.guide.qubits#borrowed-qubits)).</span></span>

<span data-ttu-id="91a90-229">Voor een dergelijke quantum computer moet de kloon bewerking worden beschreven in een unitary-matrix.</span><span class="sxs-lookup"><span data-stu-id="91a90-229">For such a quantum computer, the cloning operation must be described by a unitary matrix.</span></span>
<span data-ttu-id="91a90-230">De meting is niet toegestaan omdat de Quantum status die we proberen te klonen, is beschadigd.</span><span class="sxs-lookup"><span data-stu-id="91a90-230">We disallow measurement, since it would corrupt the quantum state we are trying to clone.</span></span>
<span data-ttu-id="91a90-231">Voor het simuleren van de kloon bewerking willen we de unitary-matrix gebruiken om de eigenschap te hebben die $ $ U \ket { \psi } \ket{0 } = \ket { \psi } \ket { \psi}</span><span class="sxs-lookup"><span data-stu-id="91a90-231">To simulate the cloning operation, we want the unitary matrix used to have the property that $$ U \ket{\psi} \ket{0} = \ket{\psi} \ket{\psi}</span></span>
<span data-ttu-id="91a90-232">$ $ voor een wille keurige status $ \ket { \psi } $.</span><span class="sxs-lookup"><span data-stu-id="91a90-232">$$ for any state $\ket{\psi}$.</span></span>
<span data-ttu-id="91a90-233">De eigenschap Linearity van matrix vermenigvuldiging impliceert dat voor elke tweede Quantum status $ \ket { \phi } $,</span><span class="sxs-lookup"><span data-stu-id="91a90-233">The linearity property of matrix multiplication then implies that for any second quantum state $\ket{\phi}$,</span></span>

<span data-ttu-id="91a90-234">$ $ \begin{align}</span><span class="sxs-lookup"><span data-stu-id="91a90-234">$$ \begin{align}</span></span>
    <span data-ttu-id="91a90-235">U \left [\frac{1 } {\sqrt{2 } } \left (\ket { \phi } + \ket { \psi } \right) \right] \ket{0}</span><span class="sxs-lookup"><span data-stu-id="91a90-235">U \left[ \frac{1}{\sqrt{2}}\left(\ket{\phi}+\ket{\psi} \right) \right] \ket{0}</span></span>
    <span data-ttu-id="91a90-236">& = \frac{1 } {\sqrt{2 } } U \ket { \phi } \ket{0}</span><span class="sxs-lookup"><span data-stu-id="91a90-236">& = \frac{1}{\sqrt{2}} U\ket{\phi}\ket{0}</span></span>
      <span data-ttu-id="91a90-237">+ \frac{1 } {\sqrt{2 } } U \ket { \psi } \ket{0 } \\ \\ & = \frac{1 } {\sqrt{2 } } \left (\ket \phi \ket { } { \phi } + \ket { \psi } \ket { \psi}</span><span class="sxs-lookup"><span data-stu-id="91a90-237">+ \frac{1}{\sqrt{2}} U\ket{\psi}\ket{0} \\\\ & = \frac{1}{\sqrt{2}} \left( \ket{\phi} \ket{\phi} + \ket{\psi} \ket{\psi}</span></span>
        <span data-ttu-id="91a90-238">\right) \\ \\ & \ne \left (\frac{1 } {\sqrt{2 } } \left (\ket { \phi } + \ket { \psi } \right) \right) \otimes \left (\frac{1 } {\sqrt{2 } } \left (\ket { \phi } + \ket { \psi } \right) \right).</span><span class="sxs-lookup"><span data-stu-id="91a90-238">\right) \\\\ & \ne \left( \frac{1}{\sqrt{2}}\left(\ket{\phi}+\ket{\psi} \right) \right) \otimes \left( \frac{1}{\sqrt{2}}\left(\ket{\phi}+\ket{\psi} \right) \right).</span></span>
<span data-ttu-id="91a90-239">\end{align}</span><span class="sxs-lookup"><span data-stu-id="91a90-239">\end{align}</span></span>
$$

<span data-ttu-id="91a90-240">Dit voorziet in de fundamentele Intuition achter het no-klonen theorema: elk apparaat dat een onbekende Quantum status kopieert, moet fouten veroorzaken op ten minste een van de statussen die worden gekopieerd.</span><span class="sxs-lookup"><span data-stu-id="91a90-240">This provides the fundamental intuition behind the No-Cloning Theorem: any device that copies an unknown quantum state must induce errors on at least some of the states it copies.</span></span>
<span data-ttu-id="91a90-241">Hoewel de sleutel veronderstelling dat de kloon van de gegevens in de invoer status lineair is, kan dit worden geschonden door de toevoeging en meting van de hulp qubits. dergelijke interacties lekken ook bij het verwerken van informatie over het systeem door middel van de meting statistieken en voor komen dat dergelijke gevallen precies worden gekloond.</span><span class="sxs-lookup"><span data-stu-id="91a90-241">While the key assumption that the cloner acts linearly on the input state can be violated through the addition and measurement of auxiliary qubits, such interactions also leak information about the system through the measurement statistics and prevent exact cloning in such cases as well.</span></span>
<span data-ttu-id="91a90-242">Zie [voor meer informatie](xref:microsoft.quantum.more-information)over de theorema die u niet klonen.</span><span class="sxs-lookup"><span data-stu-id="91a90-242">For a more complete proof of the No-Cloning Theorem see [For more information](xref:microsoft.quantum.more-information).</span></span>

<span data-ttu-id="91a90-243">Het niet-klonen van theorema is belang rijk voor de kwalitatieve kennis van Quantum Computing omdat als u de Quantum toestanden in de buurt zou kunnen klonen, dan krijgt u een Magical-mogelijkheid om te leren van Quantum Staten.</span><span class="sxs-lookup"><span data-stu-id="91a90-243">The No-Cloning Theorem is important for qualitative understanding of quantum computing because if you could clone quantum states inexpensively then you would be granted a near-magical ability to learn from quantum states.</span></span>
<span data-ttu-id="91a90-244">Het is ook mogelijk dat u het Heisenberg van vaunted onzekerheid schendt.</span><span class="sxs-lookup"><span data-stu-id="91a90-244">Indeed, you could violate Heisenberg's vaunted uncertainty principle.</span></span>
<span data-ttu-id="91a90-245">U kunt ook een optimale kloon gebruiken om één voor beeld van een complexe Quantum distributie te maken en alles te leren over die distributie, van slechts één voor beeld.</span><span class="sxs-lookup"><span data-stu-id="91a90-245">Alternatively, you could use an optimal cloner to take a single sample from a complex quantum distribution and learn everything you could possibly learn about that distribution from just one sample.</span></span>
<span data-ttu-id="91a90-246">Dit is een manier om een munten te spie gelen en op de hoogte te houden en vervolgens een vriend te vertellen over het resultaat van de reactie "Ah de verdeling van die munten moet worden gebernoulli met $p = 0.512643 \ ldots $ !"</span><span class="sxs-lookup"><span data-stu-id="91a90-246">This would be like you flipping a coin and observing heads and then upon telling a friend about the result having them respond "Ah the distribution of that coin must be Bernoulli with $p=0.512643\ldots$!"</span></span>  <span data-ttu-id="91a90-247">Een dergelijke instructie zou niet-sensical zijn, omdat een stukje informatie (het resultaat van de kop) simpelweg de vele informatie die nodig is om de distributie te coderen zonder belang rijke eerdere informatie, niet kan leveren.</span><span class="sxs-lookup"><span data-stu-id="91a90-247">Such a statement would be non-sensical because one bit of information (the heads outcome) simply cannot provide the many bits of information needed to encode the distribution without substantial prior information.</span></span>
<span data-ttu-id="91a90-248">Op dezelfde manier kunnen we zonder voorafgaande informatie niet perfect een Quantum status klonen, net zoals we geen ensemble van deze munten kunnen voorbereiden zonder dat $p $ .</span><span class="sxs-lookup"><span data-stu-id="91a90-248">Similarly, without prior information we cannot perfectly clone a quantum state just as we cannot prepare an ensemble of such coins without knowing $p$.</span></span>

<span data-ttu-id="91a90-249">Informatie is niet gratis in Quantum Computing.</span><span class="sxs-lookup"><span data-stu-id="91a90-249">Information is not free in quantum computing.</span></span>
<span data-ttu-id="91a90-250">Elk Qubit dat wordt gemeten, geeft één stukje informatie en het theorema zonder klonen laat zien dat er geen beschik over is die kunnen worden misbruikt om de fundamentele berekenings verhouding te verkrijgen tussen informatie over het systeem en de verstoringen die erop worden opgeroepen.</span><span class="sxs-lookup"><span data-stu-id="91a90-250">Each qubit measured gives a single bit of information, and the No-Cloning Theorem shows that there is no backdoor that can be exploited to get around the fundamental tradeoff between information gained about the system and the disturbance invoked upon it.</span></span>
