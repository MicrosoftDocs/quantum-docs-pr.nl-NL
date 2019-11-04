---
title: Vectoren en matrices | Microsoft Docs
description: Vectoren en matrices
author: QuantumWriter
uid: microsoft.quantum.concepts.vectors
ms.author: nawiebe@microsoft.com
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: 58c96f9cda22b712e1a408e5566e0a8ee987bd6e
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/26/2019
ms.locfileid: "73183740"
---
# <a name="vectors-and-matrices"></a>Vectoren en matrices

Enige kennis met vectoren en matrices is essentieel voor het begrijpen van Quantum Computing. Hieronder vindt u een korte inleiding en geïnteresseerde lezers worden aanbevolen om een standaard referentie te lezen op lineaire algebra zoals *Strang, G. (1993). Inleiding tot lineaire algebra (vol. 3). Wellesley, MA: Wellesley-Cambridge Press* of een online verwijzing zoals [lineair algebra](http://joshua.smcvt.edu/linearalgebra/).

Een kolom vector (of alleen [*Vector*](https://en.wikipedia.org/wiki/Vector_(mathematics_and_physics))) $v $ van dimensie (of grootte) $n $ is een verzameling van $n $ complexe getallen $ (v_1, v_2, \ldots, v_n) $ gerangschikt als een kolom:

$ $v = \begin{bmatrix} v_1\\\\ v_2\\\\ \vdots\\\\ v_n \end{bmatrix} $ $

De norm van een vector $v $ is gedefinieerd als $ \sqrt{\sum\_i | v\_i | ^ 2} $. Een vector is bedoeld als eenheids norm (of ook wel een [*eenheids vector*](https://en.wikipedia.org/wiki/Unit_vector)genoemd) als de norm $1 $ is. De [*adjoint van een vector*](https://en.wikipedia.org/wiki/Adjoint_matrix) $v $ wordt aangegeven $v ^ \dagger $ en is gedefinieerd als de volgende rijkere rij, waarbij $\*$ de complex geconjugeerde aanduidt,

$ $ \begin{bmatrix}v_1 \\\\ \vdots \\\\ v_n \end{bmatrix} ^ \dagger = \begin{bmatrix}v_1 ^ * & \cdots & v_n ^ * \end{bmatrix} $ $

De meest voorkomende manier om twee vectoren samen te vermenigvuldigen is via het [*binnenste product*](https://en.wikipedia.org/wiki/Inner_product_space), ook wel een punt product genoemd.  Het binnenste product geeft de projectie van één vector op een andere en is inwaardevol bij het beschrijven hoe u een vector kunt uitdrukken als een som van andere eenvoudiger vectoren.  Het binnenste product tussen $u $ en $v $, aangegeven $ \left\langle u, v\right\rangle $ is gedefinieerd als

$ $ \langle u, v\rangle = u ^ \dagger v = u\_1 ^ {\*} v_1 + \cdots + u\_n ^ {\*} v\_n.
$$

Met deze notatie kan ook de norm van een vector $v $ worden geschreven als $ \sqrt{\langle v, v\rangle} $.

We kunnen een vector vermenigvuldigen met een getal $c $ om een nieuwe vector te vormen waarvan de items door $c $ worden vermenigvuldigd. We kunnen ook twee vectoren $u $ en $v $ toevoegen om een nieuwe vector te vormen waarvan de invoer de som is van de vermeldingen van $u $ en $v $. Deze bewerkingen worden hieronder weer gegeven:

$ $ \mathrm{If} ~ u = \begin{bmatrix} u_1\\\\ u_2\\\\ \vdots\\\\ u_n \end{bmatrix} ~ \mathrm{and} ~ v = \begin{bmatrix} v_1\\\\ v_2\\\\ \vdots @no__ t_10_ \\ v_n \end{bmatrix}, ~ \mathrm{then} ~ au + BV = \begin{bmatrix} au_1 + bv_1\\\\ au_2 + bv_2\\\\ \vdots\\\\ au_n + bv_n \end{bmatrix}.
$$

Een [*matrix*](https://en.wikipedia.org/wiki/Matrix_(mathematics)) van grootte $m \times n $ is een verzameling van $Mn $ complexe getallen die zijn ingedeeld in $m $ rows en $n $ columns, zoals hieronder wordt weer gegeven:

$ $M = \begin{bmatrix} M_{11} ~ ~ M_{12} ~ ~ \cdots ~ ~ M_ {1N}\\\\ M_{21} ~ ~ M_{22} ~ ~ \cdots ~ ~ M_ {2n}\\\\ \ddots\\\\ M_ {M1} ~ ~ M_ {m2} ~ ~ \cdots ~ ~ M_ {MN}\\@no__ t_11_ \end{bmatrix}. $ $

Houd er rekening mee dat een vector van dimensie $n $ een matrix van grootte is $n \times $1. Net als bij vectoren kunnen we een matrix met een getal $c $ vermenigvuldigen om een nieuwe matrix te verkrijgen waarin elk item wordt vermenigvuldigd met $c $, en kunnen we twee matrices van dezelfde grootte toevoegen om een nieuwe matrix te maken waarvan de gegevens de som van de respectieve vermeldingen van de twee matrices zijn. 

## <a name="matrix-multiplication-and-tensor-products"></a>Matrix vermenigvuldiging en tensor-producten

We kunnen ook twee matrices vermenigvuldigen $M $ van dimensie $m \times n $ en $N $ van Dimension $n \times p $ om een nieuwe matrix te verkrijgen $P $ van dimensie $m \times p $ als volgt:

\begin{align} & \begin{bmatrix} M_{11} ~ ~ M_{12} ~ ~ \cdots ~ ~ M_ {1N}\\\\ M_{21} ~ ~ M_{22} ~ ~ \cdots ~ ~ M_ {2n}\\\\ \ddots\\\\ M_ {M1} ~ ~ M_ {m2} ~ ~ \cdots ~ ~ M_ {MN} \end{bmatrix} \ begin {bmatrix} N_{11} ~ ~ N_{12} ~ ~ \cdots ~ ~ N_ {1p}\\\\ N_{21} ~ ~ N_{22} ~ ~ \cdots ~ ~ N_ {2p}\\\\ \ddots\\\\ N_ {N1} ~ ~ N_ {N2} ~ ~ \cdots ~ ~ N_ {NP} \end{bmatrix} = \begin{bmatrix} P_{11} ~ ~ P_{12} ~ ~ \cdots ~ ~ P_ {1p}\\\\ P_{21} ~ ~ P_{22} ~ ~ \cdots ~ ~ P_ {2p}\\\\ \ddots\\\\ P_ {M1} ~ ~ P_ {m2} ~ ~ \cdots ~ ~ P_ {MP} \end{bmatrix} \end{align}

waarbij de vermeldingen van $P $ $P _ {Ik} = \sum_j M_ {IJ} N_ {JK} $ zijn. De vermelding $P _{11}$ is bijvoorbeeld het binnenste product van de eerste rij van $M $ met de eerste kolom van $N $. Houd er rekening mee dat omdat een vector gewoon een speciaal geval van een matrix is, de definitie wordt uitgebreid naar matrix-vector vermenigvuldigen. 

Alle matrices die we overwegen, zijn vier Kante matrices, waarbij het aantal rijen en kolommen gelijk is, of vectoren, die overeenkomen met slechts $1 $ kolom. Een speciale vier Kante matrix is de [*identiteits matrix*](https://en.wikipedia.org/wiki/Identity_matrix), aangeduid met $ \boldone $, die alle diagonale elementen heeft die gelijk zijn aan $1 $ en de resterende elementen gelijk zijn aan $0 $:

$ $ \boldone = \begin{bmatrix} 1 ~ ~ 0 ~ ~ \cdots ~ ~ 0\\\\ 0 ~ ~ 1 ~ ~ \cdots ~ ~ 0\\\\ ~ ~ \ddots\\\\ 0 ~ ~ 0 ~ ~ \cdots ~ ~ 1 \end{bmatrix}. $ $

Voor een vier Kante matrix $A $ zeggen we een matrix $B $ de [*inverse*](https://en.wikipedia.org/wiki/Invertible_matrix) is als $AB = BA = \boldone $. De inverse van een matrix hoeft niet te bestaan, maar wanneer deze bestaat, is deze uniek en wordt deze $A ^{-1}$ aangegeven. 

Voor elke matrix $M $ is de adjoint of de geconjugeerde van $M $ een matrix $N $ zodanig dat $N _ {IJ} = M_ {Ji} ^\*$. De adjoint van $M $ wordt meestal aangeduid als $M ^ \dagger $. We zeggen een matrix $U $ is [*unitary*](https://en.wikipedia.org/wiki/Unitary_matrix) als $uu ^ \Dagger = u ^ \dagger U = \boldone $ of een vergelijk bare $U ^{-1} = u ^ \dagger $.  Misschien is de belangrijkste eigenschap van unitary-matrices dat ze de norm van een vector behouden.  Dit gebeurt omdat 

$ $ \langle v, v \rangle = v ^ \dagger v = v ^ \dagger U ^{-1} U v = v ^ \dagger U ^ \dagger U v = \langle U v, U v\rangle. $ $  

Een matrix $M $ is aangeduid als [*Hermitian*](https://en.wikipedia.org/wiki/Hermitian_matrix) als $M = M ^ \dagger $.

Ten slotte is het [*tensor-product*](https://en.wikipedia.org/wiki/Tensor_product) (of het Kronecker-product) van twee matrices $M $ van grootte $m \times n $ en $N $ van grootte $p \times q $ een grotere matrix $P = M\otimes n $ van grootte $MP \times NQ $, en wordt als volgt verkregen van $M $ en $N $:

\begin{align} M \otimes N & = \begin{bmatrix} M_{11} ~ ~ \cdots ~ ~ M_ {1N} \\\\ \ddots\\\\ M_ {M1} ~ ~ \cdots ~ ~ M_ {MN} \end{bmatrix} \otimes \begin{bmatrix} N_{11} ~ ~ \cdots ~ ~ N_ {1k}\\\\ \ddots @no__ t_8_ \\ N_ {P1} ~ ~ \cdots ~ ~ N_ {pq} \end{bmatrix}\\\\ & = \begin{bmatrix} M_{11} \begin{bmatrix} N_{11} ~ ~ \cdots ~ ~ N_ {1k}\\\\ \ddots\\\\ N_ {P1} ~ ~ \cdots ~ ~ N_ {pq} \end{bmatrix} ~ ~ \cdots ~ ~ M_ {1N} \begin{bmatrix} N_{11} ~ ~ \cdots ~ ~ N_ {1k}\\\\ \ddots\\\\ N_ {P1} ~ ~ \cdots ~ ~ N_ {pq} \end{bmatrix}\\\\ \ddots\\\\ M_ {M1} \begin{bmatrix} N_{11} ~ ~ \ cdots ~ ~ N_ {1k}\\\\ \ddots\\\\ N_ {P1} ~ ~ \cdots ~ ~ N_ {pq} \end{bmatrix} ~ ~ \cdots ~ ~ M_ {MN} \begin{bmatrix} N_{11} ~ ~ \cdots ~ ~ N_ {1k}\\\\ \ddots\\\\ N_ {P1} ~ ~ \cdots ~ ~ N_ {pq} \end {bmatrix} \end{bmatrix}.
\end{align}

Dit is beter te demonstreren met enkele voor beelden:

$ $ \begin{bmatrix} a \\\\ b \end{bmatrix} \otimes \begin{bmatrix} c \\\\ d \\\\ e \end{bmatrix} = \begin{bmatrix} a \begin{bmatrix} c \\\\ d \\\\ e \end{bmatrix} @no__ t_10_ \\[1.5 em] b \begin{bmatrix} c \\\\ d \\\\ e\end {bmatrix} \end{bmatrix} = \begin{bmatrix} a c \\\\ a d \\een e \\ \\b c \\\\ b d \\\\ be\end {bmatrix} $ $

en de

$ $ \begin{bmatrix} a \ b \\\\ c \ d \end{bmatrix} \otimes \begin{bmatrix} e \ f\\\\g \ h \end{bmatrix} = \begin{bmatrix} a\begin {bmatrix} e \ f\\\\ g \ h \end{bmatrix} b\begin {bmatrix} e \ f\\@no__ t_7_ g \ h \end{bmatrix} \\\\[1em] c\begin {bmatrix} e \ f\\\\ g \ h \end{bmatrix} d\begin {bmatrix} e \ f\\\\ g \ h \end{bmatrix} \end{bmatrix} = \begin{bmatrix} AE \ af \ BF \\@no__ t_15_ AG \ ah \ BG \ BH \\\\ CE \ CF \ de \ DF \\\\ CG \ CH \ DG \ DH \end{bmatrix}.
$$

Een laatste nuttige notatie Conventie rondom tensor-producten is dat voor elke vector $v $ of matrix $M $ $v ^ {\otimes n} $ of $M ^ {\otimes n} $ een korte hand is voor een $n $-fold tensor-product.  Bijvoorbeeld:

\begin{align} & \begin{bmatrix} 1 \\\\ 0 \end{bmatrix} ^ {\otimes 1} = \begin{bmatrix} 1 \\\\ 0 \end{bmatrix}, \qquad\begin{bmatrix} 1 \\\\ 0 \end{bmatrix} ^ {\otimes 2} = \begin{bmatrix} 1 \\\\ 0 \\\\0 \\\\0 \end{bmatrix}, \qquad\begin{bmatrix} 1 \\\\-1 \end{bmatrix} ^ {\otimes 2} = \begin{bmatrix} 1 \\\\-1 \\\\-1 \\\\1 \end{bmatrix}, \\\\ & \begin{bmatrix} 0 & 1 \\\\ 1 & 0 \end{bmatrix} ^ {\otimes 1} = \begin{bmatrix} 0 & 1 \\\\ 1 & 0 \end{bmatrix}, \qquad\begin{bmatrix} 0 & 1 \\@no__ t_27_ 1 & 0 \end{bmatrix} ^ {\otimes 2} = \begin{bmatrix} 0 & 0 & 0 & 1 \\\\ 0 & 0 & 1 & 0 \\\\ 0 & 1 & 0 & 0\\\\ 1 & 0 & 0 & 0 \ end {bmatrix}.
\end{align}

