---
title: Vectoren en matrices in kwantumcomputing
description: Leer de basis beginselen van het werken met vectoren en matrices.
author: QuantumWriter
uid: microsoft.quantum.concepts.vectors
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
ms.openlocfilehash: 6c09531cd8bee8f5efb472c95c575daed04d3040
ms.sourcegitcommit: e23178d32b316d05784a02ba3cd6166dad177e89
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/09/2020
ms.locfileid: "84630193"
---
# <a name="vectors-and-matrices"></a><span data-ttu-id="97d25-103">Vectoren en matrices</span><span class="sxs-lookup"><span data-stu-id="97d25-103">Vectors and Matrices</span></span>

<span data-ttu-id="97d25-104">Enige kennis met vectoren en matrices is essentieel voor het begrijpen van Quantum Computing.</span><span class="sxs-lookup"><span data-stu-id="97d25-104">Some familiarity with vectors and matrices is essential to understand quantum computing.</span></span> <span data-ttu-id="97d25-105">Hieronder vindt u een korte inleiding en geïnteresseerde lezers worden aanbevolen om een standaard referentie te lezen op lineaire algebra zoals *Strang, G. (1993). Inleiding tot lineaire algebra (vol. 3). Wellesley, MA: Wellesley-Cambridge Press* of een online verwijzing zoals [lineair algebra](http://joshua.smcvt.edu/linearalgebra/).</span><span class="sxs-lookup"><span data-stu-id="97d25-105">We provide a brief introduction below and interested readers are recommended to read a standard reference on linear algebra such as *Strang, G. (1993). Introduction to linear algebra (Vol. 3). Wellesley, MA: Wellesley-Cambridge Press* or an online reference such as [Linear Algebra](http://joshua.smcvt.edu/linearalgebra/).</span></span>

<span data-ttu-id="97d25-106">Een kolom vector (of alleen [*Vector*](https://en.wikipedia.org/wiki/Vector_(mathematics_and_physics))) $v $ van een dimensie (of grootte) $n $ is een verzameling van $n $ complexe getallen $ (v_1, v_2, \ldots, v_n) $ gerangschikt als een kolom:</span><span class="sxs-lookup"><span data-stu-id="97d25-106">A column vector (or simply [*vector*](https://en.wikipedia.org/wiki/Vector_(mathematics_and_physics))) $v$ of dimension (or size) $n$ is a collection of $n$ complex numbers $(v_1,v_2,\ldots,v_n)$ arranged as a column:</span></span>

<span data-ttu-id="97d25-107">$ $v = \begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="97d25-107">$$v =\begin{bmatrix}</span></span>
<span data-ttu-id="97d25-108">v_1\\\\</span><span class="sxs-lookup"><span data-stu-id="97d25-108">v_1\\\\</span></span>
<span data-ttu-id="97d25-109">v_2\\\\</span><span class="sxs-lookup"><span data-stu-id="97d25-109">v_2\\\\</span></span>
<span data-ttu-id="97d25-110">\vdots\\\\</span><span class="sxs-lookup"><span data-stu-id="97d25-110">\vdots\\\\</span></span>
<span data-ttu-id="97d25-111">v_n \end{bmatrix}$$</span><span class="sxs-lookup"><span data-stu-id="97d25-111">v_n \end{bmatrix}$$</span></span>

<span data-ttu-id="97d25-112">De norm van een vector $v $ is gedefinieerd als $ \sqrt { \sum \_ i | v \_ i | ^ 2 } $.</span><span class="sxs-lookup"><span data-stu-id="97d25-112">The norm of a vector $v$ is defined as $\sqrt{\sum\_i |v\_i|^2}$.</span></span> <span data-ttu-id="97d25-113">Een vector is bedoeld als eenheids norm (of ook wel een [*eenheids vector*](https://en.wikipedia.org/wiki/Unit_vector)genoemd) als de norm $1 is $ .</span><span class="sxs-lookup"><span data-stu-id="97d25-113">A vector is said to be of unit norm (or alternatively it is called a [*unit vector*](https://en.wikipedia.org/wiki/Unit_vector)) if its norm is $1$.</span></span> <span data-ttu-id="97d25-114">De [*adjoint van een vector*](https://en.wikipedia.org/wiki/Adjoint_matrix) $v $ wordt aangegeven $v ^ \dagger $ en is gedefinieerd als de volgende rijke vector waarbij $ \* $ de complex geconjugeerde aanduidt,</span><span class="sxs-lookup"><span data-stu-id="97d25-114">The [*adjoint of a vector*](https://en.wikipedia.org/wiki/Adjoint_matrix) $v$ is denoted $v^\dagger$ and is defined to be the following row vector where $\*$ denotes the complex conjugate,</span></span>

<span data-ttu-id="97d25-115">$ $ \begin{ bmatrix } v_1 \\ \\ \vdots \\ \\ v_n \end{ bmatrix } ^ \dagger = \begin{ bmatrix } v_1 ^ \* & \cdots & v_n ^ \* \end{bmatrix}$$</span><span class="sxs-lookup"><span data-stu-id="97d25-115">$$\begin{bmatrix}v_1 \\\\ \vdots \\\\ v_n \end{bmatrix}^\dagger = \begin{bmatrix}v_1^\* & \cdots & v_n^\* \end{bmatrix}$$</span></span>

<span data-ttu-id="97d25-116">De meest voorkomende manier om twee vectoren samen te vermenigvuldigen is via het [*binnenste product*](https://en.wikipedia.org/wiki/Inner_product_space), ook wel een punt product genoemd.</span><span class="sxs-lookup"><span data-stu-id="97d25-116">The most common way to multiply two vectors together is through the [*inner product*](https://en.wikipedia.org/wiki/Inner_product_space), also known as a dot product.</span></span>  <span data-ttu-id="97d25-117">Het binnenste product geeft de projectie van één vector op een andere en is inwaardevol bij het beschrijven hoe u een vector kunt uitdrukken als een som van andere eenvoudiger vectoren.</span><span class="sxs-lookup"><span data-stu-id="97d25-117">The inner product gives the projection of one vector onto another and is invaluable in describing how to express one vector as a sum of other simpler vectors.</span></span>  <span data-ttu-id="97d25-118">Het binnenste product tussen $u $ en $v $ , aangegeven $ \left \langle u, v \right \rangle $ is gedefinieerd als</span><span class="sxs-lookup"><span data-stu-id="97d25-118">The inner product between $u$ and $v$, denoted $\left\langle u, v\right\rangle$ is defined as</span></span>

<span data-ttu-id="97d25-119">$ $ \langle u, v \rangle = u ^ \dagger v = u \_ 1 ^ { \* } v_1 + \cdots + u \_ n ^ { \* } v \_ n.</span><span class="sxs-lookup"><span data-stu-id="97d25-119">$$ \langle u, v\rangle = u^\dagger v=u\_1^{\*} v_1 + \cdots + u\_n^{\*} v\_n.</span></span>
$$

<span data-ttu-id="97d25-120">Met deze notatie kan ook de norm van een vector $v $ worden geschreven als $ \sqrt { \langle v, v \rangle } $.</span><span class="sxs-lookup"><span data-stu-id="97d25-120">This notation also allows the norm of a vector $v$ to be written as $\sqrt{\langle v, v\rangle}$.</span></span>

<span data-ttu-id="97d25-121">We kunnen een vector vermenigvuldigen met een getal $c $ om een nieuwe vector te vormen waarvan de items door $c worden vermenigvuldigd $ .</span><span class="sxs-lookup"><span data-stu-id="97d25-121">We can multiply a vector with a number $c$ to form a new vector whose entries are multiplied by $c$.</span></span> <span data-ttu-id="97d25-122">We kunnen ook twee vectoren $u $ en $v toevoegen $ om een nieuwe vector te vormen waarvan de gegevens de som van de vermeldingen van $u $ en $v zijn $ .</span><span class="sxs-lookup"><span data-stu-id="97d25-122">We can also add two vectors $u$ and $v$ to form a new vector whose entries are the sum of the entries of $u$ and $v$.</span></span> <span data-ttu-id="97d25-123">Deze bewerkingen worden hieronder weer gegeven:</span><span class="sxs-lookup"><span data-stu-id="97d25-123">These operations are depicted below:</span></span>

<span data-ttu-id="97d25-124">$ $ \mathrm{If } ~ u = \begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="97d25-124">$$\mathrm{If}~u =\begin{bmatrix}</span></span>
<span data-ttu-id="97d25-125">u_1\\\\</span><span class="sxs-lookup"><span data-stu-id="97d25-125">u_1\\\\</span></span>
<span data-ttu-id="97d25-126">u_2\\\\</span><span class="sxs-lookup"><span data-stu-id="97d25-126">u_2\\\\</span></span>
<span data-ttu-id="97d25-127">\vdots\\\\</span><span class="sxs-lookup"><span data-stu-id="97d25-127">\vdots\\\\</span></span>
<span data-ttu-id="97d25-128">u_n \end{ bmatrix } ~ \mathrm{and } ~ v = \begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="97d25-128">u_n \end{bmatrix}~\mathrm{and}~ v =\begin{bmatrix}</span></span>
    <span data-ttu-id="97d25-129">v_1\\\\</span><span class="sxs-lookup"><span data-stu-id="97d25-129">v_1\\\\</span></span>
    <span data-ttu-id="97d25-130">v_2\\\\</span><span class="sxs-lookup"><span data-stu-id="97d25-130">v_2\\\\</span></span>
    <span data-ttu-id="97d25-131">\vdots\\\\</span><span class="sxs-lookup"><span data-stu-id="97d25-131">\vdots\\\\</span></span>
    <span data-ttu-id="97d25-132">v_n \end{ bmatrix } , ~ \mathrm{then } ~ au + BW = \begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="97d25-132">v_n \end{bmatrix},~\mathrm{then}~ au+bv =\begin{bmatrix}</span></span>
<span data-ttu-id="97d25-133">au_1 + bv_1\\\\</span><span class="sxs-lookup"><span data-stu-id="97d25-133">au_1+bv_1\\\\</span></span>
<span data-ttu-id="97d25-134">au_2 + bv_2\\\\</span><span class="sxs-lookup"><span data-stu-id="97d25-134">au_2+bv_2\\\\</span></span>
<span data-ttu-id="97d25-135">\vdots\\\\</span><span class="sxs-lookup"><span data-stu-id="97d25-135">\vdots\\\\</span></span>
<span data-ttu-id="97d25-136">au_n + bv_n \end{ bmatrix } .</span><span class="sxs-lookup"><span data-stu-id="97d25-136">au_n+bv_n \end{bmatrix}.</span></span>
$$

<span data-ttu-id="97d25-137">Een [*matrix*](https://en.wikipedia.org/wiki/Matrix_(mathematics)) van grootte $m \times n $ is een verzameling van $Mn $ complexe getallen die zijn ingedeeld in $m $ rijen en $n $ kolommen, zoals hieronder wordt weer gegeven:</span><span class="sxs-lookup"><span data-stu-id="97d25-137">A [*matrix*](https://en.wikipedia.org/wiki/Matrix_(mathematics)) of size $m \times n$ is a collection of $mn$ complex numbers arranged in $m$ rows and $n$ columns as shown below:</span></span>

<span data-ttu-id="97d25-138">$ $M = \begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="97d25-138">$$M = \begin{bmatrix}</span></span>
<span data-ttu-id="97d25-139">M_ {11 } ~ ~ M_ {12 } ~ ~ \cdots ~ ~ M_ {1N } \\ \\ M_ {21 } ~ ~ M_ {22 } ~ ~ \cdots ~ ~ M_ {2n } \\ \\ \ddots\\\\</span><span class="sxs-lookup"><span data-stu-id="97d25-139">M_{11} ~~ M_{12} ~~ \cdots ~~ M_{1n}\\\\ M_{21} ~~ M_{22} ~~ \cdots ~~ M_{2n}\\\\ \ddots\\\\</span></span>
<span data-ttu-id="97d25-140">M_ {M1 } ~ ~ M_ {m2 } ~ ~ \cdots ~ ~ M_ {MN } \\ \\ \end{ bmatrix } . $ $</span><span class="sxs-lookup"><span data-stu-id="97d25-140">M_{m1} ~~ M_{m2} ~~ \cdots ~~ M_{mn}\\\\ \end{bmatrix}.$$</span></span>

<span data-ttu-id="97d25-141">Houd er rekening mee dat een vector van dimensie $n $ een matrix van grootte is $n \times 1 $ .</span><span class="sxs-lookup"><span data-stu-id="97d25-141">Note that a vector of dimension $n$ is simply a matrix of size $n \times 1$.</span></span> <span data-ttu-id="97d25-142">Net als bij vectoren kunnen we een matrix vermenigvuldigen met een getal $c $ om een nieuwe matrix te verkrijgen waarin elk item wordt vermenigvuldigd met $c $ , en we kunnen twee matrices van dezelfde grootte toevoegen om een nieuwe matrix te maken waarvan de gegevens de som van de respectieve vermeldingen van de twee matrices zijn.</span><span class="sxs-lookup"><span data-stu-id="97d25-142">As with vectors, we can multiply a matrix with a number $c$ to obtain a new matrix where every entry is multiplied with $c$, and we can add two matrices of the same size to produce a new matrix whose entries are the sum of the respective entries of the two matrices.</span></span> 

## <a name="matrix-multiplication-and-tensor-products"></a><span data-ttu-id="97d25-143">Matrix vermenigvuldiging en tensor-producten</span><span class="sxs-lookup"><span data-stu-id="97d25-143">Matrix Multiplication and Tensor Products</span></span>

<span data-ttu-id="97d25-144">We kunnen ook twee matrices vermenigvuldigen $M $ van dimensie $m \times n $ en $N $ dimensie $n \times p $ om als volgt een nieuwe matrix $P $ van dimensie $m \times p te krijgen $ :</span><span class="sxs-lookup"><span data-stu-id="97d25-144">We can also multiply two matrices $M$ of dimension $m\times n$ and $N$ of dimension $n \times p$ to get a new matrix $P$ of dimension $m \times p$ as follows:</span></span>

<span data-ttu-id="97d25-145">\begin{align}</span><span class="sxs-lookup"><span data-stu-id="97d25-145">\begin{align}</span></span>
<span data-ttu-id="97d25-146">& \begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="97d25-146">&\begin{bmatrix}</span></span>
    <span data-ttu-id="97d25-147">M_ {11 } ~ ~ M_ {12 } ~ ~ \cdots ~ ~ M_ {1N } \\ \\ M_ {21 } ~ ~ M_ {22 } ~ ~ \cdots ~ ~ M_ {2n } \\ \\ \ddots\\\\</span><span class="sxs-lookup"><span data-stu-id="97d25-147">M_{11} ~~ M_{12} ~~ \cdots ~~ M_{1n}\\\\ M_{21} ~~ M_{22} ~~ \cdots ~~ M_{2n}\\\\ \ddots\\\\</span></span>
    <span data-ttu-id="97d25-148">M_ {M1 } ~ ~ M_ {m2 } ~ ~ \cdots ~ ~ M_ {mn}</span><span class="sxs-lookup"><span data-stu-id="97d25-148">M_{m1} ~~ M_{m2} ~~ \cdots ~~ M_{mn}</span></span>
<span data-ttu-id="97d25-149">endsystemenbmatrix}</span><span class="sxs-lookup"><span data-stu-id="97d25-149">\end{bmatrix}</span></span>
<span data-ttu-id="97d25-150">neemtbmatrix}</span><span class="sxs-lookup"><span data-stu-id="97d25-150">\begin{bmatrix}</span></span>
<span data-ttu-id="97d25-151">N_ {11 } ~ ~ N_ {\cdots ~ ~ } N_ {1p } \\ \\ N_ {21 } ~ ~ N_ {22 } ~ ~ \cdots ~ ~ N_ {2p } \\ \\ \ddots\\\\</span><span class="sxs-lookup"><span data-stu-id="97d25-151">N_{11} ~~ N_{12} ~~ \cdots ~~ N_{1p}\\\\ N_{21} ~~ N_{22} ~~ \cdots ~~ N_{2p}\\\\ \ddots\\\\</span></span>
<span data-ttu-id="97d25-152">N_ {N1 } ~ ~ N_ {N2 } ~ ~ \cdots ~ ~ N_ {NP}</span><span class="sxs-lookup"><span data-stu-id="97d25-152">N_{n1} ~~ N_{n2} ~~ \cdots ~~ N_{np}</span></span>
<span data-ttu-id="97d25-153">\end{ bmatrix } = \begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="97d25-153">\end{bmatrix}=\begin{bmatrix}</span></span>
<span data-ttu-id="97d25-154">P_ {11 } ~ ~ P_ {\cdots ~ ~ } P_ {1p } \\ \\ P_ {21 } ~ ~ P_ {22 } ~ ~ \cdots ~ ~ P_ {2p } \\ \\ \ddots\\\\</span><span class="sxs-lookup"><span data-stu-id="97d25-154">P_{11} ~~ P_{12} ~~ \cdots ~~ P_{1p}\\\\ P_{21} ~~ P_{22} ~~ \cdots ~~ P_{2p}\\\\ \ddots\\\\</span></span>
<span data-ttu-id="97d25-155">P_ {M1 } ~ ~ P_ {m2 } ~ ~ \cdots ~ ~ P_ {MP}</span><span class="sxs-lookup"><span data-stu-id="97d25-155">P_{m1} ~~ P_{m2} ~~ \cdots ~~ P_{mp}</span></span>
<span data-ttu-id="97d25-156">endsystemenbmatrix}</span><span class="sxs-lookup"><span data-stu-id="97d25-156">\end{bmatrix}</span></span>
<span data-ttu-id="97d25-157">\end{align}</span><span class="sxs-lookup"><span data-stu-id="97d25-157">\end{align}</span></span>

<span data-ttu-id="97d25-158">de vermeldingen van $P $ zijn $P _ {ik } = \ sum_j M_ {ij} N_ {JK } $.</span><span class="sxs-lookup"><span data-stu-id="97d25-158">where the entries of $P$ are $P_{ik} = \sum_j M_{ij}N_{jk}$.</span></span> <span data-ttu-id="97d25-159">De invoer $P _ {11 } $ is bijvoorbeeld het binnenste product van de eerste rij van $M $ met de eerste kolom van $N $ .</span><span class="sxs-lookup"><span data-stu-id="97d25-159">For example, the entry $P_{11}$ is the inner product of the first row of $M$ with the first column of $N$.</span></span> <span data-ttu-id="97d25-160">Houd er rekening mee dat omdat een vector gewoon een speciaal geval van een matrix is, de definitie wordt uitgebreid naar matrix-vector vermenigvuldigen.</span><span class="sxs-lookup"><span data-stu-id="97d25-160">Note that since a vector is simply a special case of a matrix, this definition extends to matrix-vector multiplication.</span></span> 

<span data-ttu-id="97d25-161">Alle matrices die we overwegen, zijn vier Kante matrices, waarbij het aantal rijen en kolommen gelijk is, of vectoren, die overeenkomen met een kolom van $1 $ .</span><span class="sxs-lookup"><span data-stu-id="97d25-161">All the matrices we consider will either be square matrices, where the number of rows and columns are equal, or vectors, which corresponds to only $1$ column.</span></span> <span data-ttu-id="97d25-162">Een speciale vier Kante matrix is de [*identiteits matrix*](https://en.wikipedia.org/wiki/Identity_matrix), aangeduid met $ \boldone $ , die alle diagonale elementen heeft die gelijk zijn aan $1 $ en de resterende elementen gelijk zijn aan $0 $ :</span><span class="sxs-lookup"><span data-stu-id="97d25-162">One special square matrix is the [*identity matrix*](https://en.wikipedia.org/wiki/Identity_matrix), denoted $\boldone$, which has all its diagonal elements equal to $1$ and the remaining elements equal to $0$:</span></span>

<span data-ttu-id="97d25-163">$ $ \boldone = \begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="97d25-163">$$\boldone=\begin{bmatrix}</span></span>
<span data-ttu-id="97d25-164">1 ~ ~ 0 ~ ~ \cdots ~ ~ 0\\\\</span><span class="sxs-lookup"><span data-stu-id="97d25-164">1 ~~ 0 ~~ \cdots ~~ 0\\\\</span></span>
<span data-ttu-id="97d25-165">0 ~ ~ 1 ~ ~ \cdots ~ ~ 0\\\\</span><span class="sxs-lookup"><span data-stu-id="97d25-165">0 ~~ 1 ~~ \cdots ~~ 0\\\\</span></span>
<span data-ttu-id="97d25-166">~ ~ \ddots\\\\</span><span class="sxs-lookup"><span data-stu-id="97d25-166">~~ \ddots\\\\</span></span>
<span data-ttu-id="97d25-167">0 ~ ~ 0 ~ ~ \cdots ~ ~ 1 \end{ bmatrix } . $ $</span><span class="sxs-lookup"><span data-stu-id="97d25-167">0 ~~ 0 ~~ \cdots ~~ 1 \end{bmatrix}.$$</span></span>

<span data-ttu-id="97d25-168">Voor een vier Kante matrix $A $ zeggen we dat een matrix $B $ de [*inverse*](https://en.wikipedia.org/wiki/Invertible_matrix) is als $AB = BA = \boldone $ .</span><span class="sxs-lookup"><span data-stu-id="97d25-168">For a square matrix $A$, we say a matrix $B$ is its [*inverse*](https://en.wikipedia.org/wiki/Invertible_matrix) if $AB = BA = \boldone$.</span></span> <span data-ttu-id="97d25-169">De inverse van een matrix hoeft niet te bestaan, maar wanneer deze bestaat, is deze uniek en wordt deze $A ^ {-1 } $ aangegeven.</span><span class="sxs-lookup"><span data-stu-id="97d25-169">The inverse of a matrix need not exist, but when it exists it is unique and we denote it $A^{-1}$.</span></span> 

<span data-ttu-id="97d25-170">Voor elke matrix $M $ is de adjoint of de geconjugeerde van $M $ een matrix $N $ dat $N _ {IJ } = M_ {Ji } ^ \* $.</span><span class="sxs-lookup"><span data-stu-id="97d25-170">For any matrix $M$, the adjoint or conjugate transpose of $M$ is a matrix $N$ such that $N_{ij} = M_{ji}^\*$.</span></span> <span data-ttu-id="97d25-171">De adjoint van $M $ wordt gewoonlijk aangegeven $M ^ \dagger $ .</span><span class="sxs-lookup"><span data-stu-id="97d25-171">The adjoint of $M$ is usually denoted $M^\dagger$.</span></span> <span data-ttu-id="97d25-172">We zeggen dat een matrix $ $U [*unitary*](https://en.wikipedia.org/wiki/Unitary_matrix) is als $uu ^ \dagger = U ^ \dagger U = \boldone $ of een vergelijk bare $U ^ {-1 } = u ^ \dagger $ .</span><span class="sxs-lookup"><span data-stu-id="97d25-172">We say a matrix $U$ is [*unitary*](https://en.wikipedia.org/wiki/Unitary_matrix) if $UU^\dagger = U^\dagger U = \boldone$ or equivalently, $U^{-1} = U^\dagger$.</span></span>  <span data-ttu-id="97d25-173">Misschien is de belangrijkste eigenschap van unitary-matrices dat ze de norm van een vector behouden.</span><span class="sxs-lookup"><span data-stu-id="97d25-173">Perhaps the most important property of unitary matrices is that they preserve the norm of a vector.</span></span>  <span data-ttu-id="97d25-174">Dit gebeurt omdat</span><span class="sxs-lookup"><span data-stu-id="97d25-174">This happens because</span></span> 

<span data-ttu-id="97d25-175">$ $ \langle v, v \rangle = v ^ \dagger v = v ^ \dagger U ^ {-1 } U v = v ^ \Dagger u ^ \Dagger u v = \Langle U v, u v \rangle . $ $</span><span class="sxs-lookup"><span data-stu-id="97d25-175">$$\langle v,v \rangle=v^\dagger v = v^\dagger U^{-1} U v = v^\dagger U^\dagger U v = \langle U v, U v\rangle.$$</span></span>  

<span data-ttu-id="97d25-176">Een matrix $M $ wordt aangeduid als [*Hermitian*](https://en.wikipedia.org/wiki/Hermitian_matrix) als $M = M ^ \dagger $ .</span><span class="sxs-lookup"><span data-stu-id="97d25-176">A matrix $M$ is said to be [*Hermitian*](https://en.wikipedia.org/wiki/Hermitian_matrix) if $M=M^\dagger$.</span></span>

<span data-ttu-id="97d25-177">Ten slotte is het [*tensor-product*](https://en.wikipedia.org/wiki/Tensor_product) (of het Kronecker-product) van twee matrices $M $ van grootte $m \times n $ en $N $ van grootte $p \times q $ een grotere matrix $P = M \otimes n $ van grootte $MP \times NQ $ , en wordt als volgt verkregen van $M $ en $N $ :</span><span class="sxs-lookup"><span data-stu-id="97d25-177">Finally, the [*tensor product*](https://en.wikipedia.org/wiki/Tensor_product) (or Kronecker product) of two matrices $M$ of size $m\times n$ and $N$ of size $p \times q$ is a larger matrix $P=M\otimes N$ of size $mp \times nq$, and is obtained from $M$ and $N$ as follows:</span></span>

<span data-ttu-id="97d25-178">\begin{align}</span><span class="sxs-lookup"><span data-stu-id="97d25-178">\begin{align}</span></span>
    <span data-ttu-id="97d25-179">M \otimes N &= \begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="97d25-179">M \otimes N &= \begin{bmatrix}</span></span>
        <span data-ttu-id="97d25-180">M_ {11 } ~ ~ \cdots ~ ~ M_ {1N } \\ \\ \ddots\\\\</span><span class="sxs-lookup"><span data-stu-id="97d25-180">M_{11} ~~ \cdots ~~ M_{1n} \\\\ \ddots\\\\</span></span>
        <span data-ttu-id="97d25-181">M_ {M1 } ~ ~ \cdots ~ ~ M_ {mn}</span><span class="sxs-lookup"><span data-stu-id="97d25-181">M_{m1}  ~~ \cdots ~~ M_{mn}</span></span>
    <span data-ttu-id="97d25-182">endsystemenbmatrix}</span><span class="sxs-lookup"><span data-stu-id="97d25-182">\end{bmatrix}</span></span>
    <span data-ttu-id="97d25-183">\otimes \begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="97d25-183">\otimes \begin{bmatrix}</span></span>
        <span data-ttu-id="97d25-184">N_ {11 } ~ ~ \cdots ~ ~ N_ {1k } \\ \\ \ddots\\\\</span><span class="sxs-lookup"><span data-stu-id="97d25-184">N_{11}  ~~ \cdots ~~ N_{1q}\\\\ \ddots\\\\</span></span>
        <span data-ttu-id="97d25-185">N_ {P1 } ~ ~ \cdots ~ ~ N_ {pq}</span><span class="sxs-lookup"><span data-stu-id="97d25-185">N_{p1} ~~ \cdots ~~ N_{pq}</span></span>
    <span data-ttu-id="97d25-186">\end{ bmatrix } \\ \\ &= \begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="97d25-186">\end{bmatrix}\\\\ &= \begin{bmatrix}</span></span>
        <span data-ttu-id="97d25-187">M_ {11 } \begin{ bmatrix } N_ {11 } ~ ~ \cdots ~ ~ N_ {1k } \\ \\ \ddots \\\\ N_ {P1 } ~ ~ \cdots ~ ~ N_ {pq } \end{ bmatrix } ~ ~ \cdots ~ ~ M_ {1N } \begin{ bmatrix } N_ {11 } ~ ~ \cdots ~ ~ N_ {1k } \\ \\ \ddots \\\\ N_ {P1 } ~ ~ \cdots ~ ~ N_ {pq } \end{ bmatrix } \\ \\ \ddots\\\\</span><span class="sxs-lookup"><span data-stu-id="97d25-187">M_{11} \begin{bmatrix} N_{11}  ~~ \cdots ~~ N_{1q}\\\\ \ddots\\\\ N_{p1} ~~ \cdots ~~ N_{pq} \end{bmatrix}~~ \cdots ~~ M_{1n} \begin{bmatrix} N_{11}  ~~ \cdots ~~ N_{1q}\\\\ \ddots\\\\ N_{p1} ~~ \cdots ~~ N_{pq} \end{bmatrix}\\\\ \ddots\\\\</span></span>
        <span data-ttu-id="97d25-188">M_ {M1 } \begin{ bmatrix } N_ {11 } ~ ~ \cdots ~ ~ N_ {1k } \\ \\ \ddots \\\\ N_ {P1 } ~ ~ \cdots ~ ~ N_ {pq } \end{ bmatrix } ~ ~ \cdots ~ ~ M_ {MN } \begin{ bmatrix } N_ {11 } ~ ~ \cdots ~ ~ N_ {1k } \\ \\ \ddots \\\\ N_ {P1 } ~ ~ \cdots ~ ~ N_ {pq } \end{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="97d25-188">M_{m1} \begin{bmatrix} N_{11}  ~~ \cdots ~~ N_{1q}\\\\ \ddots\\\\ N_{p1} ~~ \cdots ~~ N_{pq} \end{bmatrix}~~ \cdots ~~ M_{mn} \begin{bmatrix} N_{11}  ~~ \cdots ~~ N_{1q}\\\\ \ddots\\\\ N_{p1} ~~ \cdots ~~ N_{pq} \end{bmatrix}</span></span>
    <span data-ttu-id="97d25-189">\end{ bmatrix } .</span><span class="sxs-lookup"><span data-stu-id="97d25-189">\end{bmatrix}.</span></span>
<span data-ttu-id="97d25-190">\end{align}</span><span class="sxs-lookup"><span data-stu-id="97d25-190">\end{align}</span></span>

<span data-ttu-id="97d25-191">Dit is beter te demonstreren met enkele voor beelden:</span><span class="sxs-lookup"><span data-stu-id="97d25-191">This is better demonstrated with some examples:</span></span>

<span data-ttu-id="97d25-192">$ $ \begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="97d25-192">$$ \begin{bmatrix}</span></span>
        <span data-ttu-id="97d25-193">a \\ \\ b \end{ bmatrix } \otimes \begin{ bmatrix } c \\ \\ d \\ \\ e \end{ bmatrix } = \begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="97d25-193">a \\\\ b  \end{bmatrix} \otimes \begin{bmatrix} c \\\\ d \\\\ e \end{bmatrix} = \begin{bmatrix}</span></span>
        <span data-ttu-id="97d25-194">een \begin{ bmatrix } c \\ \\ d \\ \\ e \end{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="97d25-194">a \begin{bmatrix} c \\\\ d \\\\ e \end{bmatrix}</span></span>
        <span data-ttu-id="97d25-195">\\\\[1.5 em] b \begin{ bmatrix } c \\ \\ d \\ \\ e \end {bmatrix}</span><span class="sxs-lookup"><span data-stu-id="97d25-195">\\\\[1.5em] b \begin{bmatrix} c \\\\ d \\\\ e\end{bmatrix}</span></span>
    <span data-ttu-id="97d25-196">endsystemenbmatrix}</span><span class="sxs-lookup"><span data-stu-id="97d25-196">\end{bmatrix}</span></span>
    <span data-ttu-id="97d25-197">= \begin{ bmatrix } a a c \\ \\ a d \\ \\ a e \\ \\ b c \\ \\ b d \\ \\ \end {bmatrix}</span><span class="sxs-lookup"><span data-stu-id="97d25-197">= \begin{bmatrix} a c \\\\ a d \\\\ a e \\\\ b c \\\\ b d \\\\ be\end{bmatrix}</span></span>
$$

<span data-ttu-id="97d25-198">en</span><span class="sxs-lookup"><span data-stu-id="97d25-198">and</span></span>

<span data-ttu-id="97d25-199">$ $ \begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="97d25-199">$$ \begin{bmatrix}</span></span>
        <span data-ttu-id="97d25-200">een \ b \\ \\ c \ d \end{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="97d25-200">a\ b \\\\ c\ d \end{bmatrix}</span></span>
    <span data-ttu-id="97d25-201">\otimes \begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="97d25-201">\otimes \begin{bmatrix}</span></span>
        <span data-ttu-id="97d25-202">e \ f \\ \\ g \ h \end{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="97d25-202">e\ f\\\\g\ h \end{bmatrix}</span></span>
     <span data-ttu-id="97d25-203">= \begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="97d25-203">= \begin{bmatrix}</span></span>
    <span data-ttu-id="97d25-204">een \begin {bmatrix}</span><span class="sxs-lookup"><span data-stu-id="97d25-204">a\begin{bmatrix}</span></span>
    <span data-ttu-id="97d25-205">e \ f \\\\ g \ h \end{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="97d25-205">e\ f\\\\ g\ h \end{bmatrix}</span></span>
    <span data-ttu-id="97d25-206">b \begin {bmatrix}</span><span class="sxs-lookup"><span data-stu-id="97d25-206">b\begin{bmatrix}</span></span>
    <span data-ttu-id="97d25-207">e \ f \\\\ g \ h \end{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="97d25-207">e\ f\\\\ g\ h \end{bmatrix}</span></span>
    <span data-ttu-id="97d25-208">\\\\[1em] c \begin {bmatrix}</span><span class="sxs-lookup"><span data-stu-id="97d25-208">\\\\[1em] c\begin{bmatrix}</span></span>
    <span data-ttu-id="97d25-209">e \ f \\\\ g \ h \end{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="97d25-209">e\ f\\\\ g\ h \end{bmatrix}</span></span>
    <span data-ttu-id="97d25-210">d \begin {bmatrix}</span><span class="sxs-lookup"><span data-stu-id="97d25-210">d\begin{bmatrix}</span></span>
    <span data-ttu-id="97d25-211">e \ f \\\\ g \ h \end{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="97d25-211">e\ f\\\\ g\ h \end{bmatrix}</span></span>
    <span data-ttu-id="97d25-212">endsystemenbmatrix}</span><span class="sxs-lookup"><span data-stu-id="97d25-212">\end{bmatrix}</span></span>
    <span data-ttu-id="97d25-213">= \begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="97d25-213">= \begin{bmatrix}</span></span>
    <span data-ttu-id="97d25-214">AE \ af. \ BF \\ \\ AG \ ah \ BG \ BH \\ \\ CE \ CF \ de \ DF \\ \\ cg \ CH \ DG \ DH \end{ bmatrix } .</span><span class="sxs-lookup"><span data-stu-id="97d25-214">ae\ af\ be\ bf \\\\ ag\ ah\ bg\ bh \\\\ ce\ cf\ de\ df \\\\ cg\ ch\ dg\ dh \end{bmatrix}.</span></span>
$$

<span data-ttu-id="97d25-215">Een laatste nuttige notatie Conventie rondom tensor-producten is dat voor elke vector $v $ of matrix $M $ $v ^ {\otimes n } $ of $M ^ {\otimes n } $ een korte hand is voor een $n voor $ herhaald tensor-product.</span><span class="sxs-lookup"><span data-stu-id="97d25-215">A final useful notational convention surrounding tensor products is that, for any vector $v$ or matrix $M$, $v^{\otimes n}$ or $M^{\otimes n}$ is short hand for an $n$-fold repeated tensor product.</span></span>  <span data-ttu-id="97d25-216">Bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="97d25-216">For example:</span></span>

<span data-ttu-id="97d25-217">\begin{align}</span><span class="sxs-lookup"><span data-stu-id="97d25-217">\begin{align}</span></span>
<span data-ttu-id="97d25-218">& \begin{ bmatrix } 1 \\ \\ 0 \end{ bmatrix } ^ {\otimes 1 } = \begin{ bmatrix } 1 \\ \\ 0 \end{ bmatrix } , \qquad \begin { bmatrix } 1 \\ \\ 0 \end{ bmatrix } ^ {\otimes 2 } = \begin{ bmatrix } 1 \\ \\ 0 \\ \\ 0 0 \\ \\ \end{ bmatrix } , \qquad \begin { bmatrix } 1 \\ \\ -1 \end{ bmatrix } ^ {\otimes 2 } = \begin{ bmatrix } 1 \\ \\ -1 \\ \\ -1 \\ \\ 1 \end{ bmatrix } , \\ \\ & \begin{ bmatrix } 0 & 1 \\ \\ 1 & 0 \end{ bmatrix } ^ {\otimes 1 } = \begin{ bmatrix } 0 & 1 \\ \\ 1 & 0 \end{ bmatrix } , \qquad \begin { bmatrix } 0 & 1 \\ \\ 1 & 0 \end{ bmatrix } ^ {\otimes 2 } = \begin{ bmatrix } 0 &0&0&1 \\ \\ 0 &0&1&0 \\ \\ 0 &1&0&0 \\\\ 1 &0&0&0 \end { bmatrix } .</span><span class="sxs-lookup"><span data-stu-id="97d25-218">&\begin{bmatrix} 1 \\\\ 0 \end{bmatrix}^{\otimes 1} = \begin{bmatrix} 1 \\\\ 0 \end{bmatrix}, \qquad\begin{bmatrix} 1 \\\\ 0 \end{bmatrix}^{\otimes 2} = \begin{bmatrix} 1 \\\\ 0 \\\\0 \\\\0 \end{bmatrix}, \qquad\begin{bmatrix} 1 \\\\ -1 \end{bmatrix}^{\otimes 2} = \begin{bmatrix} 1 \\\\ -1 \\\\-1 \\\\1 \end{bmatrix}, \\\\ &\begin{bmatrix}  0 & 1 \\\\ 1& 0   \end{bmatrix}^{\otimes 1}= \begin{bmatrix}    0& 1 \\\\ 1& 0  \end{bmatrix},  \qquad\begin{bmatrix} 0 & 1 \\\\ 1& 0   \end{bmatrix}^{\otimes 2}= \begin{bmatrix} 0 &0&0&1 \\\\ 0 &0&1&0 \\\\ 0 &1&0&0\\\\ 1 &0&0&0\end{bmatrix}.</span></span>
<span data-ttu-id="97d25-219">\end{align}</span><span class="sxs-lookup"><span data-stu-id="97d25-219">\end{align}</span></span>
