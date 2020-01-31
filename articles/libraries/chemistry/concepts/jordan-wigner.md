---
title: Jordanië-Wigner representatie | Microsoft Docs
description: Jordanië-Wigner-weer gave conceptuele docs
author: nathanwiebe2
ms.author: nawiebe@microsoft.com
ms.date: 10/09/2017
ms.topic: article-type-from-white-list
uid: microsoft.quantum.chemistry.concepts.jordanwigner
ms.openlocfilehash: 5d9038e440a2022547395e889e149a531a7ef818
ms.sourcegitcommit: f8d6d32d16c3e758046337fb4b16a8c42fb04c39
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2020
ms.locfileid: "76820535"
---
# <a name="jordan-wigner-representation"></a>Jordanië-Wignere representatie

Hoewel het tweede aantal geHamiltonianseerde taken handig is weer gegeven in termen van $a ^ \dagger $ (maken) en $a $ (Annihilation), zijn deze bewerkingen geen fundamentele bewerkingen op quantum computers.
Als u deze wilt implementeren op een quantum computer, moeten de Opera tors worden toegewezen aan unitary-matrices die op een quantum computer kunnen worden geïmplementeerd.
De Wigner-weer gave van Jordanië bevat een dergelijke kaart.
Andere, zoals de Bravyi – Kitaev-vertegenwoordiging bestaan echter ook en hebben hun eigen relatieve voor delen en nadelen.
Het belangrijkste voor deel van de Wignere weer gave van Jordanië is de eenvoud.

De Wigner-representatie van Jordanië is direct voorwaarts om te kunnen afleiden.
U herinnert dat een status $ \ket{0}_j $ impliceert dat Orbital $j $ leeg is en $ \ket{1}_j $ impliceert dat deze bezet is.
Dit betekent dat qubits natuurlijk het beroep van een bepaalde spin Orbital kan opslaan.
We hebben dat $a ^ \ dagger_j \ket{0}_j = \ket{1}_j $ en $a ^ \ dagger_j \ket{1}_j = $0.
Het is eenvoudig om te controleren of \begin{align} een ^ \ dagger_j & = \begin{bmatrix}0 & 0 \\\ 1 & 0 \end{bmatrix} = \frac{X_j-iY_j}{2}, \nonumber\\\\ a_j & = \begin{bmatrix}0 & 1 \\\ 0 & 0 \end{bmatrix} = \frac{X_j + iY_j}{2}, \end{align} waarbij $X _j $ en $Y _J $ het Pauli-$X $ en-$Y $ Opera tors op Qubit $j $.

>[!NOTE]
> In Q # geeft de $ \ket{0}$ status de + 1 eigenstate van de operator $Z $ aan. In sommige gebieden van fysieke fysica ${0}\ket is de status van de laag-energie toestand en dus de-1 eigenstate van de operator van de $Z $ vertegenwoordigd. Sommige formules kunnen daarom verschillen van populaire literatuur.

In de Library chemie gebruiken we $ \ket{0}$ om een onbezette spin-Orbital aan te duiden.
Dit laat zien dat voor een enkele spin Orbital het gemakkelijk is om de Opera tors voor maken en Annihilation te vertegenwoordigen in termen van unitary-matrices die quantum computers begrijpen.
Houd er rekening mee dat $X $ en $Y $ unitary $a ^ \dagger $ en $a $ niet zijn.
We zullen later zien dat dit geen uitdaging voor simulatie vormt.

Een probleem dat zich blijft voordoen, is dat hoewel de bovenstaande constructie voor een enkele spin Orbital werkt, het mislukt voor systemen met twee of meer draaiende banen.
Omdat Fermions antisymmetic zijn, weten we dat $a ^ \ dagger_j een ^ \ dagger_k =-a ^ \ dagger_k een ^ \ dagger_j $ voor $j $ en $k $.
$ $ \Left (\frac{X_j-iY_j}{2}\right) \left (\frac{X_k-iY_k}{2}\right) = \left (\frac{X_k-iY_k}{2}\right) \left (\frac{X_j-iY_j}{2}\right).
$ $ Met andere woorden, de twee maken-Opera tors werken niet zoals vereist.
Dit kan zelfs op een eenvoudige, op een onelegante manier worden verholpen.
De oplossing is te weten dat Paulie opera toren op natuurlijke wijze worden gewerkt.
Met name $XZ =-ZX $ en $YZ =-ZY $.
Daarom kunnen we met $Z $-Opera tors in de bouw van de operator de juiste anti-werkzaamheden emuleren.
De volledige constructie is als volgt: 

\begin{align} a ^ \ dagger_1 & = \left (\frac{X-iY}{2}\right) \otimes 1 \otimes 1 \otimes 1 \otimes \cdots \otimes 1,\\\\ een ^ \ dagger_2 & = Z\otimes\left (\frac{X-iY}{2}\right) \otimes 1 \ otimes 1 \otimes \cdots \otimes 1,\\\\ een ^ \ dagger_3 & = Z\otimes Z\otimes \left (\frac{X-iY}{2}\right) \otimes 1 \otimes \cdots \otimes 1,\\\\ & \vdots\\\\ een ^ \ dagger_N & = Z\otimes Z\otimes Z\otimes Z \otimes \cdots \otimes Z \ otimes \left (\frac{X-iY}{2}\right). \label{eq:JW} \end{align}

Het is ook handig om de nummer operators, $n _j $, in termen van Pauli-Opera tors uit te drukken.
Gelukkig, de teken reeksen van $Z $-Opera tors (ook wel Jordanië-Wigner teken reeksen genoemd), worden geannuleerd nadat deze vervanging is uitgevoerd.
Nadat u dit hebt uitgevoerd (en terugroept dat $X _jY_j = iZ_j $), hebben we \begin{Equation} n_j = a ^ \ dagger_j a_j = \frac{(1-Z_j)}{2}.
\end{equation}


## <a name="constructing-hamiltonians-in-jordan-wigner-representation"></a>Hamiltonians maken in Jordanië-Wigner-vertegenwoordiging

Zodra we de Wigner-weer gave van Jordanië hebben aangeroepen om de Hamiltonian te vertalen naar een som van Pauli Opera Tors, is dit recht vooruit.
Een van de twee $a ^ \dagger $ en $a $-Opera tors in de Fermionic-Hamiltonian worden vervangen door de teken reeksen van Pauli-Opera tors die hierboven staan vermeld.
Wanneer een van deze vervangingen wordt uitgevoerd, zijn er slechts vijf soorten termen binnen de Hamiltonian.
Deze vijf klassen komen overeen met de verschillende manieren waarop we de $p, q $ en $p, q, r, s $ in de Hamiltonian en de voor waarden van twee hoofd tekst in de-hoofd tekst kunnen kiezen.
Deze vijf klassen, voor het geval waarin $p > q > r > s $ en met de werkelijke waarden.

\begin{align} h_ {PP} a_p ^ \dagger a_p & = \ sum_p \frac{h_ {PP}}{2}(1-Z_p)\\\\ h_ {pq} (a_p ^ \dagger a_q + a ^ \ dagger_q a_p) & = \frac{h_ {pq}}{2}\left (\ prod_ {j = q + 1} ^ {p-1} Z_j \right) \left (X_pX_q + Y_pY_q \right)\\\\ h_ {pqqp} n_p n_q & = \frac{h_ {pqqp}}{4}\left (1-Z_p-Z_q + Z_pZ_q \right)\\\\ H_ {pqqr} & = \frac{h_ {pqqr}}{2}\left (\ prod_ {j = r + 1} ^ {p-1} Z_j \right) \left (X_pX_r + Y_pY_r \right) \left (\frac{1-Z_q}{2}\right)\\\\ H_ {pqrs} & = \frac{h_ {pqrs}}{8}\ prod_ {j = s + 1} ^ {r-1} Z_j \ prod_ {k = q + 1} ^ {p-1} Z_k \Big (XXXX-XXYY + XYXY\nonumber\\\\ & \qquad\qquad\qquad\qquad\qquad + YXXY + YXYX-YYXX\nonumber\\\\ & \qquad\qquad\qquad\qquad\qquad + XYYX + YYYY\Big) \end{align}

Bij het genereren van dergelijke Hamiltonians hoeven deze vervangings regels alleen te worden toegepast. Dit zou niet haalbaar zijn voor grote moleculen die kunnen bestaan uit miljoenen Hamiltonian-voor waarden.
Als alternatief kunnen we automatisch de `JordanWignerEncoding` maken op basis van een `FermionHamiltonian` weer gave van de Hamiltonian.

```csharp
    // We load the namespace containing fermion and Pauli objects. 
    using Microsoft.Quantum.Chemistry.Fermion;
    using Microsoft.Quantum.Chemistry.Pauli;
    
    // We create an example `FermionHamiltonian` instance.
    var fermionHamiltonian = new FermionHamiltonian();

    // We convert this Fermion Hamiltonian to a Jordan-Wigner representation.
    var jordanWignerEncoding = fermionHamiltonian.ToPauliHamiltonian(QubitEncoding.JordanWigner);
```

Zodra de Hamiltonians zijn gemaakt in dit formulier, kunnen we een host van de Quantum-simulatie algoritmen gebruiken om de door $e ^ {-iHt} gegenereerde dynamiek te compileren tot een reeks elementaire Gates (binnen sommige door de gebruiker te definiëren fout tolerantie).
We bespreken de twee populairste methoden voor Quantum simulatie, qubitization-en Trotter-Suzuki-formules in de algoritme-documentatie. We bieden implementaties voor beide methoden in de Hamiltonian-simulatie bibliotheek.
