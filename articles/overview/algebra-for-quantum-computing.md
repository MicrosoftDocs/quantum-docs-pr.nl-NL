---
title: Lineaire algebra voor kwantumcomputing
description: Meer informatie over de basisprincipes van lineaire algebra om kwantumcomputing beter te begrijpen
author: bradben
ms.author: bradben
ms.date: 5/5/2020
ms.topic: overview
uid: microsoft.quantum.overview.algebra
no-loc:
- Q#
- $$v
ms.openlocfilehash: d7a8dff8d491a9ce6451148d2d27121f1c190ed0
ms.sourcegitcommit: 8256ff463eb9319f1933820a36c0838cf1e024e8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/17/2020
ms.locfileid: "90759319"
---
# <a name="linear-algebra-for-quantum-computing"></a>Lineaire algebra voor kwantumcomputing

Lineaire algebra is de taal van kwantumcomputing. Hoewel u deze niet hoeft te kennen om kwantumprogramma's te implementeren of schrijven, wordt deze taal veel gebruikt voor het beschrijven van qubittoestanden, kwantumbewerkingen en voor het voorspellen van het gedrag van een kwantumcomputer in reactie op een reeks instructies.

Net zoals u kwantumcomputing beter kunt begrijpen als u bekend bent met de [basisconcepten van kwantumfysica](xref:microsoft.quantum.overview.understanding), kunt u beter begrijpen hoe kwantumalgoritmen werken als u enige basiskennis hebt van lineaire algebra. U dient op zijn minst bekend te zijn met **vectoren** en **matrixvermenigvuldiging**. U kunt uw kennis van deze algebraconcepten zo nodig opfrissen met de volgende zelfstudies over de basisbeginselen:

- [Zelfstudie over een Jupyter-notebook over lineaire algebra](https://github.com/microsoft/QuantumKatas/tree/main/tutorials/LinearAlgebra)
- [Zelfstudie over een Jupyter-notebook over complexe rekenkunde](https://github.com/microsoft/QuantumKatas/tree/main/tutorials/ComplexArithmetic)
- [Lineaire algebra voor kwantumcomputing](https://cds.cern.ch/record/1522001/files/978-1-4614-6336-8_BookBackMatter.pdf)
- [Grondbeginselen van lineaire algebra](https://www.math.ubc.ca/~carrell/NB.pdf)
- [Grondbeginselen van kwantumcomputing](https://www.codeproject.com/Articles/5155638/Quantum-Computation-Primer-Part-1#exploring-quantum-superposition)

## <a name="vectors-and-matrices-in-quantum-computing"></a>Vectoren en matrices in kwantumcomputing

In het onderwerp over [kwantumcomputing](xref:microsoft.quantum.overview.understanding) zag u dat een qubit een toestand van 1 of 0 of een superpositie of beide kan hebben. In lineaire algebra wordt de toestand van een qubit beschreven als een vector en uitgedrukt als één kolom-**matrix** $\begin{bmatrix} a \\\\  b \end{bmatrix}$. Deze wordt ook wel een **kwantumtoestandvector** genoemd en moet voldoen aan de vereiste dat $|a|^2 + |b|^2 = 1$.  

Met de elementen van de matrix wordt de kans uitgedrukt dat de qubit op de ene of de andere manier ineenstort. Hierbij is $|a|^2$ de kans op ineenstorting tot nul en $|b|^2$ de kans op ineenstorting tot één. De volgende matrices zijn allemaal voorbeelden van geldige kwantumtoestandvectoren:

$$\begin{bmatrix} 1 \\\\  0 \end{bmatrix}, \begin{bmatrix} 0 \\\\  1 \end{bmatrix}, \begin{bmatrix} \frac{1}{\sqrt{2}} \\\\  \frac{1}{\sqrt{2}} \end{bmatrix}, \begin{bmatrix} \frac{1}{\sqrt{2}} \\\\  \frac{-1}{\sqrt{2}} \end{bmatrix}, \text{ and }\begin{bmatrix} \frac{1}{\sqrt{2}} \\\\  \frac{i}{\sqrt{2}} \end{bmatrix}.$$

In [Kwantumcomputers en kwantumsimulators](xref:microsoft.quantum.overview.simulators) hebt u ook gezien dat kwantumbewerkingen worden gebruikt om de toestand van een qubit te wijzigen.  Kwantumbewerkingen kunnen ook worden uitgedrukt als een matrix. Wanneer een kwantumbewerking wordt toegepast op een qubit, worden de twee matrices waarmee ze worden uitgedrukt, vermenigvuldigd en vertegenwoordigt het resultaat de nieuwe toestand van de qubit na de bewerking.  

Hier volgen twee veelvoorkomende kwantumbewerkingen die worden uitgedrukt via een matrixvermenigvuldiging.


De [bewerking `X`](xref:microsoft.quantum.intrinsic.x) staat voor de Pauli-matrix $X$,

$$X = \begin{bmatrix} 0 & 1 \\\\ 1 & 0 \end{bmatrix},$$
    
en wordt gebruikt om de toestand van een qubit te wijzigen van 0 in 1 (of omgekeerd), bijvoorbeeld

$$\begin{bmatrix}0 &1\\\\ 1 &0\end{bmatrix}\begin{bmatrix} 1 \\\\  0 \end{bmatrix} = \begin{bmatrix} 0 \\\\  1 \end{bmatrix}.$$

De [bewerking 'H'](xref:microsoft.quantum.intrinsic.h) staat voor de Hadamard-transformatie $H$,

$$H = \dfrac{1}{\sqrt{2}}\begin{bmatrix}1 &1\\\\ 1 &-1\end{bmatrix},$$

 en plaatst een qubit in een toestand van superpositie, waarbij de kans op ineenstorting tot nul even groot is als de kans op ineenstorting tot één, zoals hier wordt weergegeven

$$\frac{1}{\sqrt{2}}\begin{bmatrix}1 &1\\\\ 1 &-1\end{bmatrix}\begin{bmatrix} 1 \\\\  0 \end{bmatrix}=\frac{1}{\sqrt{2}}\begin{bmatrix} 1 \\\\  1 \end{bmatrix}=\left(\frac{1}{\sqrt{2}}\right)^2=\frac{1}{2}.$$

Een matrix die een kwantumbewerking vertegenwoordigt, moet voldoen aan één vereiste: het moet een **unitaire** matrix zijn. Een matrix is unitair als het **omgekeerde** van de matrix gelijk is aan de **geconjugeerde omzetting** van de matrix.

## <a name="representing-two-qubit-states"></a>Toestanden van twee qubits vertegenwoordigen

In de bovenstaande voorbeelden is de toestand van een qubit beschreven als één kolommatrix $\begin{bmatrix} a \\\\  b \end{bmatrix}$, en is het toepassen van een bewerking erop beschreven als een vermenigvuldiging van de twee matrices. In kwantumcomputers worden echter meerdere qubits gebruikt, dus hoe wordt dan de gecombineerde toestand van twee qubits beschreven? 

Elke qubit is immers een vectorruimte, dus u kunt ze niet gewoon vermenigvuldigen. In plaats daarvan gebruikt u een **tensorproduct**. Dat is een gerelateerde bewerking waarmee een nieuwe vectorruimte wordt gemaakt op basis van afzonderlijke vectorruimten. Deze wordt uitgedrukt als $\otimes$. Het tensorproduct van de twee qubittoestanden $\begin{bmatrix} a \\\\  b \end{bmatrix}$ en $\begin{bmatrix} c \\\\  d \end{bmatrix}$ wordt als volgt berekend:

$$ \begin{bmatrix} a \\\\  b \end{bmatrix} \otimes \begin{bmatrix} c \\\\  d \end{bmatrix} =\begin{bmatrix} a \begin{bmatrix} c \\\\  d \end{bmatrix} \\\\ b \begin{bmatrix}c \\\\  d \end{bmatrix} \end{bmatrix} = \begin{bmatrix} ac \\\\  ad \\\\  bc \\\\  bd \end{bmatrix}. $$

Het resultaat is een vierdimensionale matrix, waarbij elk element een waarschijnlijkheid vertegenwoordigt. Bijvoorbeeld: $ac$ is de kans dat de twee qubits ineenstorten tot 0 en 0, $ad$ is de kans op 0 en 1, enzovoort. 

Net zoals de toestand van één qubit $\begin{bmatrix} a \\\\  b \end{bmatrix}$ moet voldoen aan de vereiste $|a|^2 + |b|^2 = 1$ om een kwantumtoestand te vertegenwoordigen, moet de toestand van twee qubits $\begin{bmatrix} ac \\\\  ad \\\\  bc \\\\  bd \end{bmatrix}$ voldoen aan de vereiste $|ac|^2 + |ad|^2 + |bc|^2+ |bd|^2 = 1$.

## <a name="summary"></a>Samenvatting

Lineaire algebra is de standaardtaal voor het beschrijven van kwantumcomputing en kwantumfysica. Hoewel de [bibliotheken](xref:microsoft.quantum.libraries) die in de Microsoft Quantum Development Kit zijn opgenomen, u helpen om geavanceerde kwantumalgoritmen uit te voeren zonder diep in de onderliggende wiskunde te hoeven duiken. Met een begrip van de basisbeginselen kunt u snel aan de slag gaan en hebt u een solide basis om op voort te bouwen.

## <a name="next-steps"></a>Volgende stappen

[De QDK installeren](xref:microsoft.quantum.install)
