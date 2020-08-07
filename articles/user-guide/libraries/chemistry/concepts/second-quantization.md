---
title: Tweede Kwantisatiefouten
description: Meer informatie over de tweede Kwantisatiefouten-benadering voor het model leren van elektronische structuren in kwantum programmering.
author: nathanwiebe2
ms.author: nawiebe@microsoft.com
ms.date: 10/09/2017
ms.topic: article-type-from-white-list
uid: microsoft.quantum.chemistry.concepts.secondquantization
no-loc:
- Q#
- $$v
ms.openlocfilehash: ba77c499d6830b1f78bba39e20b15c4ebe9433fc
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/06/2020
ms.locfileid: "87869457"
---
# <a name="second-quantization"></a>Tweede Kwantisatiefouten

Tweede kwantisatiefouten kijkt naar het probleem van de elektronische structuur via een andere lens.
In plaats van elke $N _e $ electrons toe te wijzen aan een specifieke staat (of Orbital), houdt tweede kwantisatiefouten elke Orbital bij en slaat het op of er in elk van deze elektron aanwezig zijn en tegelijkertijd de symmetrie-eigenschappen van de overeenkomstige functie van Wave worden gegarandeerd.
Dit is belang rijk omdat het mogelijk is dat er quantum chemie-modellen worden opgegeven zonder dat u zich zorgen hoeft te maken over anti-symmetrizing de invoer status (zoals vereist voor fermions) en dat dergelijke modellen door de tweede kwantisatiefouten kunnen worden gesimuleerd met behulp van kleine quantum computers.

Als voor beeld van een tweede kwantisatiefouten in actie gaan we ervan uit dat $ \ psi_0 \cdots \ psi_ {N-1} $ een orthonormal-verzameling van ruimtelijke banen is.
Deze banen worden zo gekozen dat het systeem zo nauw keurig mogelijk kan worden weer gegeven binnen de beperkte basis die wordt overwogen.
Een gemeen schappelijk voor beeld van deze banen is een Atomic-baan die een eigenbasis vormt voor de water stof Atom.
Omdat electrons twee statussen hebben, kan twee electrons worden Crammed in elk van deze ruimtelijke Orbital.
Dat wil zeggen dat de geldige basis statussen de volgende notatie hebben: $ \ psi_ {0, \uparrow}, \ldots, \ psi_ {N-1, \uparrow}, \ psi_ {0, \downarrow}, \ldots, \ psi_ {N-1, \downarrow} $, waarbij $ \uparrow $ en $ \downarrow $ de labels zijn die de twee eigenstates van de mate van vrijheid van de draaiing bepalen.
Deze gecombineerde index van $ (j, \sigma) $ voor $ \sigma \in \{ \uparrow, \downarrow \} $ wordt ' spin-Orbital ' genoemd, omdat deze zowel de ruimtelijke als de mate van vrijheid van het niveau van de kring waarde bevat.
In de Library chemie worden spin-banen opgeslagen in een `SpinOrbital` gegevens structuur en als volgt gemaakt.

```csharp
    // First, we load the namespace containing spin-orbital objects.
    using Microsoft.Quantum.Chemistry.OrbitalIntegrals;

    // First, we assign an orbital index, say `5`. Note that we use 0-indexing,
    // so this is the 6th orbital.
    var orbitalIdx = 5;

    // Second, we assign a spin index, say `Spin.u` for spin up or `Spin.d` for spin down.
    var spin = Spin.d;

    // the spin-orbital (5, ↓) is then
    var spinOrbital = new SpinOrbital(orbitalIdx, spin);

    // A tuple `(int, Spin)` is also implicitly recognized as a spin-orbital.
    (int, Spin) tuple = (orbitalIdx, spin);

    // We explicitly specify the type of `spinOrbital1` to demonstrate
    // the implicit cast to `SpinOrbital`.
    SpinOrbital spinOrbital1 = tuple;
```

Dit betekent dat we formeel kunnen nadenken over het spin en ruimtelijke deel van de functie Wave als $ \ psi_ {0} \cdots \ psi_ {2n-1} $, waarbij elk van de indices nu een opsomming is van een $ (j, \sigma) $.
Een mogelijke opsomming is $g (j, \sigma) = j + N\sigma ' $.
Een andere mogelijke opsomming is $h (j, \sigma) = 2 * j + \sigma $.
De quantum chemie-bibliotheek kan gebruikmaken van deze conventies en de spin-banen in een dergelijke code ring kunnen als volgt worden geïnstantieerd.

```csharp
    // Let us use the spin orbital created in the previous snippet.
   var spinOrbital = new SpinOrbital(5, Spin.d);

   // Let us set the total number of orbitals to be say, `7`.
   var nOrbitals = 7;

    // This converts a spin-orbital index to a unique integer, in this case `12`,
    // using the formula `g(j,σ)`.
    var integerIndexHalfUp = spinOrbital.ToInt(IndexConvention.HalfUp);

    // This converts a spin-orbital index to a unique integer, in this case `11`,
    // using the formula `h(j,σ)`.
    var integerIndexUpDown = spinOrbital.ToInt(IndexConvention.UpDown);

    // The default conversion uses the formula `h(j,σ)`, in this case `11`.
    var integerIndexDefault = spinOrbital.ToInt();
```

Voor fermionic-systemen wordt voor komen dat er meer dan één elektro uren aanwezig zijn in een spin-Orbital tegelijk.
Dit betekent dat we de twee juridische Staten kunnen schrijven voor $ \ psi_1 $ als \begin{Equation} \ psi_1 \rightarrow \begin{cases} \ket {0} _1 & \Text{if $ \ psi_1 $ niet bezet is,}\\\
\ket {1} _1 & \Text{if $ \ psi_1 $ is bezet.} \end{cases} \end{Equation} deze code ring is ideaal voor quantum computers, omdat het elektronische beroep als één Quantum bit kan worden opgeslagen.

De beroeps statussen voor de $2N $ spin-banen kunnen op dezelfde manier worden opgeslagen in $2N $ qubits.
Als $N bijvoorbeeld = $2, is de status $ $ \ket {0} \ket {1} \ket {1} \ket {0} , $ $

komt overeen met de kring velden $1 $ en $2 $ die worden ingen Omen met de rest lege.
Op dezelfde manier is de status $ $ \ket {0} \equiv \ket {0} _ {0} {0} \cdots \ket_{N-1}, $ $

heeft geen electrons en wordt aangeduid als ' vacuüm status '.

Een prachtige kant van het tweede kwantisatiefouten is dat we de anti-symmetrie van de Quantum status niet langer hoeven te volgen.
Dit komt omdat de anti-symmetrie van de staat zichzelf voordoet, in plaats van de anti-werk regels van de Opera tors die elektronische beroepen van een spin Orbital maken en vernietigen.

## <a name="fermionic-operators"></a>Fermionic-Opera tors

De twee fundamentele Opera tors die op de secundaire basis vectoren handelen, worden het maken en Annihilation Opera tors genoemd.
Deze opera tors invoegen of vernietigen electrons op een bepaalde locatie.
Deze worden aangeduid $a ^ \ dagger_j $ en $a _j $ respectievelijk.

Bijvoorbeeld \begin{align} a ^ \ dagger_1 \ket {0} _1 = \ket {1} _1, \quad a ^ \ dagger_1 \ket {1} _1 = 0, \quad a_1 \ket {0} _1 = 0, \quad a_1 \ket {1} _1 = \ket {0} _1.
in \end{align} ziet u dat hier $a ^ \ dagger_1 \ket {1} _1 = 0 $ en $a _1 \ket {0} _1 $ resulteert in de nul-vector, niet $ \ket {0} _1 $.
Dergelijke Opera tors zijn daarom noch Hermitian noch unitary.
De Opera tors voor algemeen maken en Annihilation worden aangeduid met het <xref:Microsoft.Quantum.Chemistry.LadderOperators.LadderOperator`1> type.
Een enkele operator voor maken wordt bijvoorbeeld als volgt weer gegeven.

```csharp
    // We load the namespace containing ladder operator objects.
    using Microsoft.Quantum.Chemistry.LadderOperators;

    // Let us use the spin orbital created in the previous snippet.
    var spinOrbitalInteger = new SpinOrbital(5, Spin.d).ToInt();

    // We specify either a creation or annihilation operator using 
    // the enumerable type `RaisingLowering.u` or `RaisingLowering.d`
    // respectively;
    var creationEnum = RaisingLowering.u;

    // The type representing a creation operator is then initialized 
    // as follows. Here, we index these operators with integers.
    // Hence we initialize the generic ladder operator with an
    // integer index type.
    var ladderOperator0 = new LadderOperator<int>(creationEnum, spinOrbitalInteger);

    // An alternate constructor for a LadderOperator instead uses
    // a tuple.
    var ladderOperator1 = new LadderOperator<int>((creationEnum, spinOrbitalInteger));
```

Met behulp van dergelijke Opera tors kunnen we ook \ket {0} \ket {1} \ket {1} \ket {0} = a ^ \ dagger_1 een ^ \ dagger_2 \ket {0} ^ {\otimes 4}.
$ $ Deze volg orde van Opera tors wordt in de Hamiltonian-simulatie bibliotheek gemaakt met behulp van C#-code die vergelijkbaar is met de Orbital-situatie met één spin die hierboven wordt behandeld:
```csharp
    // We load the namespace containing fermion-related objects.
    using Microsoft.Quantum.Chemistry.Fermion;

    // Let us initialize an array of tuples representing the
    // desired sequence of creation operators.
    var indices = new[] { (RaisingLowering.u, 1), (RaisingLowering.u, 2) };

    // We can convert this array of tuples to a sequence of ladder
    // operators using the `ToLadderSequence()` methods.
    var ladderSequences = indices.ToLadderSequence();

    // Sequences of ladder operators are quite general. For instance,
    // they could be bosonic operators, instead of fermionic operators.
    // We specialize them by constructing a `FermionTerm` representing 
    // a fermion creation operator on the index `2` followed by `1`.
    var fermionTerm = new FermionTerm(ladderSequences);
```

Voor een systeem van $k $ Fermions, in de tweede kwantisatiefouten is de actie van de operator maken $a ^ \ dagger_i $ gegeven door $ $ a ^ \ dagger_i \ket{n_1, n_2, \ldots, 0_i, \ldots, n_k} = (-1) ^ {S_i} \ket{n_1, n_2, \ldots, 1_i, \ldots, n_k}, $ $ en $ $ a ^ \ dagger_i \ket{n_1, n_2, \ldots, 1_i, \ldots, n_k} = 0, $ $ waar $S _i = \ sum_ {j<i} a ^ \ dagger_j a_j $ meet het totale aantal Fermions dat in de staat van één partikel is en die een index heeft $j < i $.

Een derde operator wordt ook vaak gebruikt in tweede verdeelde representaties.
Deze operator staat bekend als de operator Number en wordt gedefinieerd door \begin{Equation} n_i = a ^ \ dagger_i a_i.
\end{Equation} deze operator telt het beroep van een gegeven Orbital, wat wil zeggen \begin{align} n_i \ket {0} _i &= 0 \ geen getal\\\
n_i \ket {1} _i &= \ket {1} _I.
\end{align} die vergelijkbaar zijn met de bovenstaande `FermionTerm` voor beelden, is deze nummer operator als volgt samengesteld.
```csharp
    // Let us use a new method to compactly create a sequence of ladder
    // operators. Note that we have omitted specifying whether the 
    // operators are raising or lowering. In this case, the first half
    // will be raising operators, and the second half will be lowering 
    // operators.
    var indices = new[] { 1, 1 }.ToLadderSequence();

    // We now construct a `FermionTerm` representing an annihilation operator
    // on the index 1 followed by the creation operator on the index 1.
    var fermionTerm0 = new FermionTerm(indices);
```

Er komt een subtlety bij het gebruik van de Opera tors maken of Annihilation in fermionic-systemen.
Een geldige Quantum staat is niet-symmetrisch onder uitwisseling van labels.
Dit betekent dat $ $ a ^ \ dagger_2 een ^ \ dagger_1 \ket {0} =-a ^ \ dagger_1 een ^ \ dagger_2 \ket {0} .
$ $ Dergelijke Opera tors zijn "antiwerkend" en in het algemeen voor elke $i, j $ we hebben dat \begin{align} een ^ \ dagger_i een ^ \ dagger_j =-(1-\ delta_ {i, j}) een ^ \ dagger_j een ^ \ dagger_i, \quad a ^ \ dagger_i a_j = \ delta_ {i, j}-a_j een ^ \ dagger_i.
\end{align} dus de volgende twee <xref:Microsoft.Quantum.Chemistry.LadderOperators.LadderSequence`1> instanties worden beschouwd als een gelijkwaardige waarde
```csharp
    // Let us initialize an array of tuples representing the
    // desired sequence of creation operators.
    var indices = new[] { (RaisingLowering.u, 1), (RaisingLowering.u, 2) };

    // We now construct a `LadderSequence` representing a creation operator
    // on the index 1 followed by 2, then a term with the reverse ordering.
    var laddderSeqeunce = indices.ToLadderSequence();
    var laddderSeqeunceReversed = indices.Reverse().ToLadderSequence();

    // The following Boolean is `false`.
    var equal = laddderSeqeunce == laddderSeqeunceReversed;
```

De vereiste dat elk van de verwerkings exploitanten antiwerkers betekent dat het gebruik van een tweede gevormde vertegenwoordiging verstrekken de uitdagingen van de anti-symmetrie van Fermions.
In plaats daarvan wordt de uitdaging in de definitie van de Opera tors voor maken hersteld. 

Bij het gebruik van de regels voor anti-werkingen `LadderSequence` komen sommige instanties in werkelijkheid overeen met dezelfde volg orde van fermionic-Opera Tors, soms met een minteken.
Denk bijvoorbeeld aan de Hamiltonian $a _0 ^ \dagger a_1 ^ \dagger a_1 a_0 =-a_1 ^ \dagger a_0 ^ \dagger a_1 a_0 $.
Hiermee wordt ons gemotiveren een canonieke ordening voor elke te definiëren `FermionTerm` .
Elk `FermionTerm` wordt automatisch als volgt in canonieke volg orde geplaatst.
```csharp
    // We now construct two `FermionTerms` that are equivalent with respect to
    // anti-commutation up to a sign change.
    var fermionTerm0 = new FermionTerm(new[] { 0, 1, 1, 0 }.ToLadderSequence());
    var fermionTerm1 = new FermionTerm(new[] { 1, 0, 1, 0 }.ToLadderSequence());

    // The following Boolean is `true`.
    var sequenceEqual = fermionTerm0 == fermionTerm1;

    // The change in sign is not compared above, but is an internally tracked
    // property of `FermionTerm`.
    int sign0 = fermionTerm0.Coefficient;
    var sign1 = fermionTerm1.Coefficient;

    // The following Boolean is `false`.
    var signEqual = sign0 == sign1;
```

## <a name="second-quantized-fermionic-hamiltonian"></a>Fermionic Hamiltonian met de tweede gequanteerde

Het is misschien unsurprising dat de Hamiltonian in [Quantum modellen voor elektronische systemen](xref:microsoft.quantum.chemistry.concepts.quantummodels) kan worden geschreven in termen van maken en Annihilation-Opera tors.
Met name als $ \psi \_ j $ de kring banen zijn die de basis vormen, dan

\begin{Equation} \hat{H} = \sum \_ {pq} H \_ {pq} a ^ \dagger \_ p a \_ q + \frac {1} {2} \sum \_ {pqrs} H \_ {pqrs} a ^ \dagger \_ p a ^ \dagger \_ q a \_ Ra \_ s + H \_ {\textrm NUC}, \label{EQ: totalHam} \end{Equation}, waarbij $h \_ {\textrm NUC} $ de kern energie is (een constante onder de door aankomende Oppenheimer benadering) en

\begin{align} h \_ {pq} &= \int \_ {-\infty} ^ \infty \psi ^ \* \_ p (x \_ 1) \left (-\Frac{\nabla ^ 2} {2} + V (x \_ 1) \right) \psi \_ q (x \_ 1) \mathrm{d} ^ 3x \_ 1, \end{align}

waarbij $V (x) $ het potentieel veld is, en

\begin{align} h \_ {pqrs} &= \int \_ {-\infty} ^ \infty \int \_ {-\infty} ^ \infty\psi \_ p ^ \* (x \_ 1) \psi \_ q ^ \* (x \_ 2) \left (\frac {1} {| x_1-x_2 |} \right) \psi \_ r (x \_ 2) \psi \_ s (x \_ 1) \mathrm{d} ^ 3x \_ 1 \ mathrm {d} ^ 3x \_ 2. \ label {EQ: integralen} \end{align}

De voor waarden $h \_ {pq} $ worden aangeduid als een-, integrale integraal, omdat al deze voor waarden slechts één electrons omvatten en ook $h \_ {pqrs} $ de twee-elektroden integraal zijn.
Ze worden integralen genoemd, omdat het berekenen van de waarden van deze coëfficiënten een integraal vereist.
De één elektroon-term beschrijft de kinetische energie van de afzonderlijke electrons en hun interacties met de elektrische velden van de kernen.
De twee-elektroden integralen anderzijds beschrijven de interacties tussen de electrons.

Een Intuition voor wat deze termen betekenen, kan afgelezen zijn van de Opera tors maken en Annihilation die elk daarvan bestaan.
Bijvoorbeeld, $h _ {pq} a ^ \ dagger_p a_q $ beschrijft de elektron verspringen van Orbital $q $ om Orbital $p $ te draaien.
Op dezelfde manier worden met de term $h _ {pqrs} a ^ \ dagger_p een ^ \ dagger_q a_r a_s $ (voor DISTINCT $p, q, r, s $) twee electrons in kring velden $r $ en $s $-sprei ding van elkaar beschreven en eindigend op spin banen $p $ en $q $.
Als $r = q $ en $p = s $ then $h _ {prrp} a ^ \ dagger_p een ^ \ dagger_r a_r a_p = h_ {prrp} n_p n_r $ de energie boete van de twee electrons bijna op elkaar lijkt, maar beschrijft geen dynamisch proces.

We kunnen dergelijke Hamiltonians met behulp van de `FermionHamiltonian` -klasse vertegenwoordigen. Dit is in feite een lijst die alle gewenste `FermionTerm` instanties bevat.
Als Hamiltonians worden Hermitian per definitie, indexeren we termen met het complexere type `HermitianFermionTerm` dat ook Hermitian symmetrie gebruikt bij het controleren of de voor waarden gelijk zijn.

Laat ons enkele voor beelden van een voor beeld maken.
Bekijk de Hamiltonian $ \hat{H} = a_0 ^ \dagger a_1 + a_1 ^ \dagger a_0 $.
```csharp
    // We create a `FermionHamiltonian` instance to store the fermion terms.
    var hamiltonian = new FermionHamiltonian();

    // We construct the terms to be added.
    var fermionTerm0 = new FermionTerm(new[] { 1, 0 }.ToLadderSequence());
    var fermionTerm1 = new FermionTerm(new[] { 0, 1 }.ToLadderSequence());

    // These fermion terms are not equal. The following Boolean is `false`.
    var sequenceEqual = fermionTerm0 == fermionTerm1;

    // However, these terms are equal under Hermitian symmetry.
    // We also take the opportunity to demonstrate equivalent constructors
    // for hermitian fermion terms
    var hermitianFermionTerm0 = new HermitianFermionTerm(fermionTerm0);
    var hermitianFermionTerm1 = new HermitianFermionTerm(new[] { 0, 1 });

    // These Hermitian fermion terms are equal. The following Boolean is `true`.
    var hermitianSequenceEqual = hermitianFermionTerm0 == hermitianFermionTerm1;

    // We add the terms to the Hamiltonian with the appropriate coefficient.
    // Note that these terms are identical.
    hamiltonian.Add(hermitianFermionTerm0, 1.0);
    hamiltonian.Add(hermitianFermionTerm1, 1.0);
```
We kunnen deze constructie vereenvoudigen met het feit dat Hamiltonian Opera tors van Hermitian zijn.
Wanneer u voor waarden toevoegt aan de Hamiltonian met `Add` , wordt ervan uitgegaan dat de niet-Hermitian-term bijvoorbeeld `fermionTerm0` wordt gekoppeld aan de bijbehorende Hermitian geconjugeerde.
Het volgende code fragment bevat dus ook dezelfde Hamiltonian:
```csharp
    // We create a `FermionHamiltonian` instance to store the fermion terms.
    var hamiltonian = new FermionHamiltonian();

    // We construct the term to be added -- note the doubled coefficient.
    hamiltonian.Add(new HermitianFermionTerm(new[] { 1, 0 }), 2.0);
```

Door gebruik te maken van de regels voor anti-werkingen, `FermionTerm` komen sommige instanties in de Hamiltonian in werkelijkheid overeen met dezelfde volg orde van fermionic-Opera Tors, soms met een minteken.
Denk bijvoorbeeld aan de Hamiltonian $H = a_0 ^ \dagger a_1 ^ \dagger a_1 a_0-a_1 ^ \dagger a_0 ^ \dagger a_1 a_0 = 2a_0 ^ \dagger a_1 ^ \dagger a_1 a_0 $. Dit is een som van de bovenstaande voor waarden.
Het is niet altijd duidelijk voor de gebruiker dat deze gelijkwaardige voor waarden zijn, zodat ze afzonderlijk kunnen worden toegevoegd aan de Hamiltonian.
Het is ook mogelijk dat een van de bestaande voor waarden in de Hamiltonian wordt gewijzigd.
In deze gevallen kunnen we gelijkwaardige voor waarden als volgt combi neren.
```csharp
    // We create a `FermionHamiltonian` instance to store the fermion terms.
    var hamiltonian = new FermionHamiltonian();

    // We now create two Hermitian fermion terms that are equivalent with respect to
    // anti-commutation and Hermitian symmetry.
    var terms = new[] {
        (new[] { 0, 1, 1, 0 }, 1.0),
        (new[] { 1, 0, 1, 0 }, 1.0) }
    .Select(o => (new HermitianFermionTerm(o.Item1.ToLadderSequence()), o.Item2.ToDoubleCoeff()));

    // Now add `terms` to the Hamiltonian.
    hamiltonian.AddRange(terms);

    // There is only one unique term. `nTerms == 1` is `true`.
    var nTerms = hamiltonian.CountTerms();
```
Door coefficienten van gelijkwaardige termen te combi neren, verlagen we het totale aantal voor waarden in de Hamiltonian.
Later vermindert dit het aantal Quantum-Gates dat nodig is voor het simuleren van de Hamiltonian.

### <a name="internal-representation"></a>Interne representatie

Een fermionic-Hamiltonian met interacties van één en twee hoofd tekst wordt weer gegeven in de tweede, getekende notatie als

$ $ \begin{align} H = \sum \_ {pq} H \_ {pq} a ^ \dagger \_ {p} a \_ {q} + \frac {1} {2} \sum \_ {pqrs} H \_ {pqrs} a ^ \dagger \_ {p} a ^ \dagger \_ {q} a \_ {r} a \_ {s}.
\end{align} $ $

In deze notatie zijn er Maxi maal $N ^ 2 + N ^ 4 $ coëfficiënten.
Veel van deze coëfficiënten kunnen echter worden verzameld, aangezien ze overeenkomen met dezelfde operator.
Bijvoorbeeld als $p, q, r, s $ zijn afzonderlijke indices. we kunnen de anti-werk regels gebruiken om aan te tonen dat: $ $ a ^ \dagger \_ {p} a ^ \dagger \_ {q} a \_ {r} a \_ {s} =-a ^ \dagger \_ {q} a ^ \dagger \_ {p} a \_ {r} a \_ {s} =-a ^ \dagger \_ {p} a ^ \dagger \_ {q} a {s} a { \_ \_ r} = a ^ \dagger \_ {q} a ^ \dagger \_ {p} a {s} a \_ \_ {r}.
$$

Daarnaast heeft $H $ Hermitian, elke niet-Hermitian fermionic-operator, $h \_ {pqrs} a ^ \dagger \_ {p} a ^ \dagger \_ {q} a \_ {r} a \_ {s} $, een Hermitian geconjugeerde die zich ook bevindt in $H $. Om unieke groepen termen te indexeren die door deze Symmetries worden gekenmerkt, we definiëren een canonieke volg orde op de indices $ (i \_ 1, \cdots, i \_ n, j \_ 1, \cdots, j \_ m) $ van een reeks $n + m $ fermionic Opera tors $a ^ \dagger \_ {i \_ 1} \cdots a ^ \dagger \_ {i \_ n} een \_ {j m} \_ \_ \_ $as volgt:
-   Alle aanmaak operatoren $a ^ \dagger \_ {i \_ \cdot} $ worden geplaatst voordat alle Annihilation-opera tors $a \_ {j \_ \cdot} $.
-   Alle indexen voor het maken van Opera tors worden in oplopende volg orde gesorteerd, die $i \_ 1< i \_ 2< \cdots < i \_ n $.
-   Alle Annihilation-operator indexen zijn in aflopende volg orde gesorteerd, die $j \_ 1> j \_ 2 \cdots > j \_ m $.
-   De meest linkse index is kleiner dan of gelijk aan de meest rechtse index, die $i \_ 1 \ Le j \_ m $ is.

Laat ons deze reeks canonieke bestelde indexen identificeren als $ $ \begin{align} (i \_ 1, \cdots, i n, \_ j \_ 1, \cdots, j \_ m) \in S \_ {n, m}.
\end{align} $ $

Met deze canonieke ordening kan de fermionic-Hamiltonian worden uitgedrukt als $ $ \begin{align} H = \sum \_ {(p, q) \In S \_ {1,1} } H ' \_ {pq} \frac{a ^ \dagger \_ {p} a \_ {q} + a ^ \dagger \_ {q} a \_ {p}} {2} + \sum \_ {(p, q, r, s) \in s \_ {2,2} } H ' \_ {pqrs} \frac{a ^ \dagger \_ {p} a ^ \dagger \_ {q} a \_ {r} a \_ {s} + a ^ \dagger \_ {s} a ^ \dagger \_ {r} a \_ {q} a \_ {p}} {2} , \end{align} $ $ met voldoende aangepaste integraals van één en twee elektroden $h \_ {pq} $ en $h \_ {pqrs} $.

