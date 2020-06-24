---
title: Geavanceerde matrixconcepten
description: Meer informatie over eigenvectors, eigenvalues en matrix exponentiëles, de belangrijkste hulpprogram ma's voor het beschrijven en simuleren van Quantum algoritmen.
author: QuantumWriter
uid: microsoft.quantum.concepts.matrix-advanced
ms.author: nawiebe@microsoft.com
ms.date: 12/11/2017
ms.topic: article
no-loc:
- $
- $
- $
- $
- $
- $
- $$
- $$
- $$
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
- "\begin{bmatrix}"
- "\end{bmatrix}"
- '\_'
ms.openlocfilehash: 71923247121eae6a1d4e26d2664d8e547370ba3a
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/23/2020
ms.locfileid: "85269453"
---
# <a name="advanced-matrix-concepts"></a><span data-ttu-id="ecf51-103">Geavanceerde matrix concepten</span><span class="sxs-lookup"><span data-stu-id="ecf51-103">Advanced Matrix Concepts</span></span> #

<span data-ttu-id="ecf51-104">We gaan nu onze manipulatie van matrices uitbreiden naar [*eigenvalues, Eigenvectors*](https://en.wikipedia.org/wiki/Eigenvalues_and_eigenvectors) en [*exponenten*](https://en.wikipedia.org/wiki/Matrix_exponential) die een fundamentele set hulpprogram ma's vormen die we Quantum algoritmen moeten beschrijven en implementeren.</span><span class="sxs-lookup"><span data-stu-id="ecf51-104">We now extend our manipulation of Matrices to [*Eigenvalues, Eigenvectors*](https://en.wikipedia.org/wiki/Eigenvalues_and_eigenvectors) and [*Exponentials*](https://en.wikipedia.org/wiki/Matrix_exponential) which form a fundamental set of tools we need to describe and implement quantum algorithms.</span></span>

## <a name="eigenvalues-and-eigenvectors"></a><span data-ttu-id="ecf51-105">Eigenvalues en Eigenvectors</span><span class="sxs-lookup"><span data-stu-id="ecf51-105">Eigenvalues and Eigenvectors</span></span> ##

<span data-ttu-id="ecf51-106">Laat $M $ een vier Kante matrix zijn en $v $ een vector is die niet de enige 0-vector is (dat wil zeggen, de vector met alle vermeldingen die gelijk zijn aan $0 $ ).</span><span class="sxs-lookup"><span data-stu-id="ecf51-106">Let $M$ be a square matrix and $v$ be a vector that is not the all zeros vector (i.e., the vector with all entries equal to $0$).</span></span>

<span data-ttu-id="ecf51-107">We zeggen $ dat $v een [*eigenvector*](https://en.wikipedia.org/wiki/Eigenvalues_and_eigenvectors) is van $M $ als $MV = avk $ voor een aantal $c $ .</span><span class="sxs-lookup"><span data-stu-id="ecf51-107">We say $v$ is an [*eigenvector*](https://en.wikipedia.org/wiki/Eigenvalues_and_eigenvectors) of  $M$ if $Mv = cv$ for some number $c$.</span></span> <span data-ttu-id="ecf51-108">We zeggen dat $c $ de [*eigenvalue*](https://en.wikipedia.org/wiki/Eigenvalues_and_eigenvectors) is die overeenkomt met de eigenvector $v $ .</span><span class="sxs-lookup"><span data-stu-id="ecf51-108">We say $c$ is the [*eigenvalue*](https://en.wikipedia.org/wiki/Eigenvalues_and_eigenvectors) corresponding to the eigenvector $v$.</span></span> <span data-ttu-id="ecf51-109">In het algemeen een matrix $M $ kan een vector omzetten in een andere vector, maar een eigenvector is een speciale waarde omdat deze ongewijzigd blijft, behalve als vermenigvuldigd met een getal.</span><span class="sxs-lookup"><span data-stu-id="ecf51-109">In general a matrix $M$ may transform a vector into any other vector, but an eigenvector is special because it is left unchanged except for being multiplied by a number.</span></span> <span data-ttu-id="ecf51-110">Houd er rekening mee dat als $v $ een eigenvector is met eigenvalue $c $ , $AV $ ook een eigenvector (voor elke niet-nul $a $ ) met dezelfde eigenvalue.</span><span class="sxs-lookup"><span data-stu-id="ecf51-110">Note that if $v$ is an eigenvector with eigenvalue $c$, then $av$ is also an eigenvector (for any nonzero $a$) with the same eigenvalue.</span></span>

<span data-ttu-id="ecf51-111">Voor de ID-matrix is bijvoorbeeld elke vector $v $ een eigenvector met eigenvalue $1 $ .</span><span class="sxs-lookup"><span data-stu-id="ecf51-111">For example, for the identity matrix, every vector $v$ is an eigenvector with eigenvalue $1$.</span></span>

<span data-ttu-id="ecf51-112">Een ander voor beeld is dat u een [*diagonale matrix*](https://en.wikipedia.org/wiki/Diagonal_matrix) $D $ die alleen niet-nul vermeldingen bevat op de diagonaal:</span><span class="sxs-lookup"><span data-stu-id="ecf51-112">As another example, consider a [*diagonal matrix*](https://en.wikipedia.org/wiki/Diagonal_matrix) $D$ which only has nonzero entries on the diagonal:</span></span>

<span data-ttu-id="ecf51-113">$ $ \begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="ecf51-113">$$ \begin{bmatrix}</span></span>
<span data-ttu-id="ecf51-114">d_1 & 0 & 0 \\ \\ 0 & d_2 & 0 \\ \\ 0 & 0 & D_3 \end{ bmatrix } .</span><span class="sxs-lookup"><span data-stu-id="ecf51-114">d_1 & 0 & 0 \\\\ 0 & d_2 & 0 \\\\ 0 & 0 & d_3 \end{bmatrix}.</span></span>
$$

<span data-ttu-id="ecf51-115">De vectoren</span><span class="sxs-lookup"><span data-stu-id="ecf51-115">The vectors</span></span>

<span data-ttu-id="ecf51-116">$ $ \begin{ bmatrix } 1 \\ \\ 0 \\ \\ 0 \end{ bmatrix } , \begin{ bmatrix } 0 \\ \\ 1 \\ \\ 0 \end{bmatrix} en \begin{ bmatrix } 0 \\ \\ 0 \\ \\ 1\end{bmatrix}$$</span><span class="sxs-lookup"><span data-stu-id="ecf51-116">$$\begin{bmatrix}1 \\\\ 0 \\\\ 0 \end{bmatrix}, \begin{bmatrix}0 \\\\ 1 \\\\ 0\end{bmatrix} and \begin{bmatrix}0 \\\\ 0 \\\\ 1\end{bmatrix}$$</span></span>

<span data-ttu-id="ecf51-117">zijn eigenvectors van deze matrix met respectievelijk eigenvalues $d _1 $ , $d _2 $ en $d _3 $ .</span><span class="sxs-lookup"><span data-stu-id="ecf51-117">are eigenvectors of this matrix with eigenvalues  $d_1$, $d_2$, and $d_3$, respectively.</span></span> <span data-ttu-id="ecf51-118">Als $d _1 $ , $d _2 $ en $d _3 $ afzonderlijke getallen zijn, zijn deze vectoren (en hun veelvouden) de enige eigenvectors van de matrix $D $ .</span><span class="sxs-lookup"><span data-stu-id="ecf51-118">If $d_1$, $d_2$, and $d_3$ are distinct numbers, then these vectors (and their multiples) are the only eigenvectors of the matrix $D$.</span></span> <span data-ttu-id="ecf51-119">Over het algemeen kunt u voor een diagonale matrix eenvoudig de eigenvalues en eigenvectors lezen.</span><span class="sxs-lookup"><span data-stu-id="ecf51-119">In general, for a diagonal matrix it is easy to read off the eigenvalues and eigenvectors.</span></span> <span data-ttu-id="ecf51-120">De eigenvalues zijn alle getallen die worden weer gegeven op de diagonaal en hun respectieve eigenvectors zijn de eenheids vectoren met één vermelding gelijk aan $1 $ en de resterende vermeldingen gelijk zijn aan $0 $ .</span><span class="sxs-lookup"><span data-stu-id="ecf51-120">The eigenvalues are all the numbers appearing on the diagonal, and their respective eigenvectors are the unit vectors with one entry equal to $1$ and the remaining entries equal to $0$.</span></span>

<span data-ttu-id="ecf51-121">In het bovenstaande voor beeld ziet u dat de eigenvectors van $D $ een basis vormt voor $3 $ -dimensionale vectoren.</span><span class="sxs-lookup"><span data-stu-id="ecf51-121">Note in the above example that the eigenvectors of $D$ form a basis for $3$-dimensional vectors.</span></span> <span data-ttu-id="ecf51-122">Een basis is een set vectoren waarmee elke vector als een lineaire combi natie ervan kan worden geschreven.</span><span class="sxs-lookup"><span data-stu-id="ecf51-122">A basis is a set of vectors such that any vector can be written as a linear combination of them.</span></span> <span data-ttu-id="ecf51-123">Meer expliciet, $v _1 $ , $v _2 $ en $v _3 $ vormen een basis als een vector $v $ kan worden geschreven als $v = a_1 v_1 + a_2 v_2 + a_3 v_3 $ voor sommige cijfers $a _1 $ , $a _2 $ en $a _3 $ .</span><span class="sxs-lookup"><span data-stu-id="ecf51-123">More explicitly, $v_1$, $v_2$, and $v_3$ form a basis if any vector $v$ can be written as $v=a_1 v_1 + a_2 v_2 + a_3 v_3$ for some numbers $a_1$, $a_2$, and $a_3$.</span></span>

<span data-ttu-id="ecf51-124">Terughalen dat een Hermitian-matrix (ook wel Self-adjoint genoemd) een complexe vier Kante matrix is die gelijk is aan zijn eigen complexe geconjugeerde, terwijl een unitary-matrix een complexe vier Kante matrix is waarvan de inverse is gelijk aan de complex geconjugeerde.</span><span class="sxs-lookup"><span data-stu-id="ecf51-124">Recall that a Hermitian matrix (also called self-adjoint) is a complex square matrix equal to its own complex conjugate, while a unitary matrix is a complex square matrix whose inverse is equal to its complex conjugate.</span></span>
<span data-ttu-id="ecf51-125">Voor Hermitian-en unitary-matrices, die in feite de enige matrices zijn die zich voordoen bij Quantum Computing, is er een algemeen resultaat bekend als de [*Spectral theorema*](https://en.wikipedia.org/wiki/Spectral_theorem), waarbij het volgende wordt door berekend: voor elke Hermitian-of unitary matrix $M $ , bestaat er een unitary $U, $ zodat $M = U ^ \dagger D u $ voor sommige diagonale matrix $D $ .</span><span class="sxs-lookup"><span data-stu-id="ecf51-125">For Hermitian and unitary matrices, which are essentially the only matrices encountered in quantum computing, there is a general result known as the [*spectral theorem*](https://en.wikipedia.org/wiki/Spectral_theorem), which asserts the following: For any Hermitian or unitary matrix $M$, there exists a unitary $U$ such that $M=U^\dagger D U$ for some diagonal matrix $D$.</span></span> <span data-ttu-id="ecf51-126">Bovendien zijn de diagonale items van $D $ de eigenvalues van $M $ .</span><span class="sxs-lookup"><span data-stu-id="ecf51-126">Furthermore, the diagonal entries of $D$ will be the eigenvalues of $M$.</span></span>

<span data-ttu-id="ecf51-127">U weet al hoe u de eigenvalues en eigenvectors van een matrix met diagonale $D wilt berekenen $ .</span><span class="sxs-lookup"><span data-stu-id="ecf51-127">We already know how to compute the eigenvalues and eigenvectors of a diagonal matrix $D$.</span></span> <span data-ttu-id="ecf51-128">Met deze theorema weten we dat als $v $ een eigenvector is van $D $ met eigenvalue $c $ , dat wil zeggen $DV = avk $ , en $U ^ \dagger v $ een eigenvector is van $M $ met eigenvalue $c $ .</span><span class="sxs-lookup"><span data-stu-id="ecf51-128">Using this theorem we know that if $v$ is an eigenvector of $D$ with eigenvalue $c$, i.e., $Dv = cv$, then $U^\dagger v$ will be an eigenvector of $M$ with eigenvalue $c$.</span></span> <span data-ttu-id="ecf51-129">Dit komt doordat</span><span class="sxs-lookup"><span data-stu-id="ecf51-129">This is because</span></span>

<span data-ttu-id="ecf51-130">$ $M (U ^ \dagger v) = U ^ \dagger D U (U ^ \dagger v) = U ^ \dagger D (U U ^ \dagger) v = U ^ \dagger D v = c U ^ \dagger v. $ $</span><span class="sxs-lookup"><span data-stu-id="ecf51-130">$$M(U^\dagger v) = U^\dagger D U  (U^\dagger v) =U^\dagger D (U  U^\dagger) v = U^\dagger D v = c U^\dagger v.$$</span></span>

## <a name="matrix-exponentials"></a><span data-ttu-id="ecf51-131">Matrix exponentiële waarde</span><span class="sxs-lookup"><span data-stu-id="ecf51-131">Matrix Exponentials</span></span>
<span data-ttu-id="ecf51-132">Een [*exponentiële matrix*](https://en.wikipedia.org/wiki/Matrix_exponential) kan ook worden gedefinieerd in exacte analoge waarde naar de exponentiële functie.</span><span class="sxs-lookup"><span data-stu-id="ecf51-132">A [*matrix exponential*](https://en.wikipedia.org/wiki/Matrix_exponential) can also be defined in exact analogy to the exponential function.</span></span>  <span data-ttu-id="ecf51-133">De matrix exponentiële waarde van een matrix $A $ kan worden uitgedrukt als</span><span class="sxs-lookup"><span data-stu-id="ecf51-133">The matrix exponential of a matrix $A$ can be expressed as</span></span>

<span data-ttu-id="ecf51-134">$ $ e ^ A = \boldone + a + \frac{A ^ 2 } {2!} + \frac{A ^ 3 } {3!} + \cdots $ $</span><span class="sxs-lookup"><span data-stu-id="ecf51-134">$$ e^A=\boldone + A + \frac{A^2}{2!}+\frac{A^3}{3!}+\cdots $$</span></span>

<span data-ttu-id="ecf51-135">Dit is belang rijk omdat quantum-mechanische tijd wordt beschreven in een unitary matrix van het formulier $e ^ {iB } $ voor Hermitian matrix $B $ .</span><span class="sxs-lookup"><span data-stu-id="ecf51-135">This is important because quantum mechanical time evolution is described by a unitary matrix of the form $e^{iB}$ for Hermitian matrix $B$.</span></span>  <span data-ttu-id="ecf51-136">Daarom is het uitvoeren van matrix exponentiëlen een fundamenteel onderdeel van Quantum Computing, en biedt dit Q # intrinsieke routines voor het beschrijven van deze bewerkingen.</span><span class="sxs-lookup"><span data-stu-id="ecf51-136">For this reason, performing matrix exponentials is a fundamental part of quantum computing and as such Q# offers intrinsic routines for describing these operations.</span></span>
<span data-ttu-id="ecf51-137">Er zijn veel manieren in de praktijk om een matrix exponentiële waarde te berekenen op een klassieke computer, en in het algemeen is een dergelijke exponentiële benadering fraught met Peril.</span><span class="sxs-lookup"><span data-stu-id="ecf51-137">There are many ways in practice to compute a matrix exponential on a classical computer, and in general numerically approximating such an exponential is fraught with peril.</span></span>  <span data-ttu-id="ecf51-138">Zie [*Cleve moler en Jeroen van bruikleen. "19 dubious manieren om de exponentiële waarde van een matrix te berekenen." SIAM beoordeling 20,4 (1978): 801-836*](https://doi.org/10.1137/S00361445024180) voor meer informatie over de betrokken uitdagingen.</span><span class="sxs-lookup"><span data-stu-id="ecf51-138">See [*Cleve Moler and Charles Van Loan. "Nineteen dubious ways to compute the exponential of a matrix." SIAM review 20.4 (1978): 801-836*](https://doi.org/10.1137/S00361445024180) for more information about the challenges involved.</span></span>

<span data-ttu-id="ecf51-139">De eenvoudigste manier om inzicht te krijgen in het berekenen van de exponentiële waarde van een matrix is via de eigenvalues en eigenvectors van die matrix.</span><span class="sxs-lookup"><span data-stu-id="ecf51-139">The easiest way to understand how to compute the exponential of a matrix is through the eigenvalues and eigenvectors of that matrix.</span></span>  <span data-ttu-id="ecf51-140">Met name de hierboven besproken Spectral theorema geeft aan dat voor elke Hermitian of unitary matrix $A $ er een unitary matrix $U $ en een diagonale matrix $D $ dat $A = U ^ \dagger D u $ .  Vanwege de eigenschappen van unitarity hebben we dat $A ^ 2 = U ^ \dagger D ^ 2 U $ en ook voor alle power $p $ $A ^ p = U ^ \dagger D ^ p U $ .  Als we dit vervangen door de operator definitie van de operator exponentiële, krijgen we het volgende:</span><span class="sxs-lookup"><span data-stu-id="ecf51-140">Specifically, the spectral theorem discussed above says that for every Hermitian or unitary matrix $A$ there exists a unitary matrix $U$ and a diagonal matrix $D$ such that $A=U^\dagger D U$.  Because of the properties of unitarity we have that $A^2 = U^\dagger D^2 U$ and similarly for any power $p$ $A^p = U^\dagger D^p U$.  If we substitute this into the operator definition of the operator exponential we obtain:</span></span>

<span data-ttu-id="ecf51-141">$ $ e ^ A = U ^ \dagger \left (\boldone + D + \frac{D ^ 2 } {2!} + \cdots \right) U = u ^ \dagger \begin{ bmatrix } \exp (D_ {11 } ) & 0 & \cdots &0 \\\\ 0 & \exp (D_ {22 } ) & \cdots & 0 \\\\ \vdots & \vdots & \ddots & \vdots \\\\ 0&0 & \cdots & \exp (D_ {nn } ) \end{ bmatrix } U. $ $</span><span class="sxs-lookup"><span data-stu-id="ecf51-141">$$ e^A= U^\dagger \left(\boldone +D +\frac{D^2}{2!}+\cdots \right)U= U^\dagger \begin{bmatrix}\exp(D_{11}) & 0 &\cdots &0\\\\ 0 & \exp(D_{22})&\cdots& 0\\\\ \vdots &\vdots &\ddots &\vdots\\\\ 0&0&\cdots&\exp(D_{NN}) \end{bmatrix} U. $$</span></span>

<span data-ttu-id="ecf51-142">Met andere woorden, als u overschakelt naar de eigenbasis van de matrix $A $ wordt de matrix exponentiële waarde gelijk aan het berekenen van de normale exponentieel van de eigenvalues van de matrix.</span><span class="sxs-lookup"><span data-stu-id="ecf51-142">In other words, if you transform to the eigenbasis of the matrix $A$ then computing the matrix exponential is equivalent to computing the ordinary exponential of the eigenvalues of the matrix.</span></span>  <span data-ttu-id="ecf51-143">Net als veel bewerkingen in Quantum Computing moeten matrix-exponentiële waarden worden uitgevoerd, wordt deze truc omgezet in de eigenbasis van een matrix om het uitvoeren van de operator exponentieel te vereenvoudigen, en dit is de basis achter veel Quantum algoritmen, zoals Trotter – Suzuki-stijl, verderop in deze hand leiding besproken.</span><span class="sxs-lookup"><span data-stu-id="ecf51-143">As many operations in quantum computing involve performing matrix exponentials, this trick of transforming into the eigenbasis of a matrix to simplify performing the operator exponential appears frequently and is the basis behind many quantum algorithms such as Trotter–Suzuki-style quantum simulation methods discussed later in this guide.</span></span>

<span data-ttu-id="ecf51-144">Een andere nuttige eigenschap is als $B $ zowel unitary als Hermitian is, dat wil zeggen $B = b ^ {-1 } = B ^ \dagger $ $B ^ 2 = \boldone $ .</span><span class="sxs-lookup"><span data-stu-id="ecf51-144">Another useful property is if $B$ is both unitary and Hermitian, i.e., $B=B^{-1}=B^\dagger$ then $B^2=\boldone$.</span></span> <span data-ttu-id="ecf51-145">Door deze regel toe te passen op de bovenstaande uitbrei ding van de matrix exponentiële en door het groeperen van de $ \boldone $ en de voor waarden van de $B $ , kan het worden weer geven dat voor elke feitelijke waarde $x $ de identiteit</span><span class="sxs-lookup"><span data-stu-id="ecf51-145">By applying this rule to the above expansion of the matrix exponential and by grouping the $\boldone$ and the $B$ terms together, it can be see that for any real value $x$ the identity</span></span>

<span data-ttu-id="ecf51-146">$ $e ^ {iBx } = \boldone \cos (x) + iB\sin (x) $ $</span><span class="sxs-lookup"><span data-stu-id="ecf51-146">$$e^{iBx}=\boldone \cos(x)+ iB\sin(x)$$</span></span>


<span data-ttu-id="ecf51-147">keringen.</span><span class="sxs-lookup"><span data-stu-id="ecf51-147">holds.</span></span> <span data-ttu-id="ecf51-148">Dit is met name nuttig omdat het de oorzaak is van de exponentiële waarde van de acties matrix, zelfs als de dimensie van $B $ exponentieel groot is, voor het speciale geval wanneer $B $ zowel unitary als Hermitian is.</span><span class="sxs-lookup"><span data-stu-id="ecf51-148">This trick is especially useful because it allows to reason about the actions matrix exponentials have, even if the dimension of $B$ is exponentially large, for the special case when $B$ is both unitary and Hermitian.</span></span>
