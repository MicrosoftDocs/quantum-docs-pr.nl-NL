---
title: Quantum dynamiek
description: Meer informatie over de overeenkomsten en verschillen tussen de Quantum dynamiek en de klassieke dynamiek.
author: nathanwiebe2
ms.author: nawiebe@microsoft.com
ms.date: 10/09/2017
ms.topic: article-type-from-white-list
uid: microsoft.quantum.chemistry.concepts.quantumdynamics
ms.openlocfilehash: 9cb74ccd4b7806a90c0701300860d777fa8e5d75
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/23/2020
ms.locfileid: "85275090"
---
# <a name="quantum-dynamics"></a>Quantum dynamiek

Quantum mechanismen zijn in het algemeen het onderzoek van de Quantum dynamiek, waarmee wordt uitgelegd hoe een initiële Quantum status $ \ket{\psi (0)} $ in de loop van de tijd varieert (Zie de [conceptuele documenten](xref:microsoft.quantum.concepts.dirac) op quantum computing voor meer informatie over de Dirac-notatie).
In het bijzonder, gezien deze voor waarde, een Quantum status, een ontwikkelings tijd en een specificatie van het dynamische systeem van de Quantum, wordt een Quantum status $ \ket{\psi (t)} $ gezocht.
Voordat u doorgaat met de uitleg van Quantum Dynamics, is het handig om een stap terug te nemen en te denken over klassieke dynamiek, omdat het inzicht biedt in hoe Quantum monteurs zich eigenlijk niet afwijkt van de klassieke dynamiek.

In de klassieke dynamiek weten we van het tweede recht van Newton dat de positie van een partikel wordt gegroeid op basis van $F (x, t) = ma = m\frac {\ dd ^ 2} {\dd t ^ 2} {x} (t) $, waarbij $F (x, t) $ $a $m de versnelling is.
Op basis van een begin positie $x (0) $, ontwikkelings tijd $t $ en een beschrijving van de krachten die op het partikel reageren, kunnen we $x (t) $ vinden door de differentiële vergelijking te verhelpen die wordt gegeven door de vergelijkingen van Newton voor $x (t) $.
Het opgeven van de krachten op deze manier is een beetje van een pijn.
Daarom geven we de oorzaken van de mogelijke energie van het systeem vaak door. Dit geeft ons $-\ partial_x V (x, t) = m \frac{\dd ^ 2} {\dd t ^ 2} {x} (t) $.
Voor een partikel moet de dynamiek van het systeem dus alleen worden opgegeven door de mogelijke energie functie, de massa van het partikel en de ontwikkelings tijd.

Een bredere taal wordt vaak geïntroduceerd voor de klassieke dynamiek die verder gaat dan $F = ma $.
Een formulering, die bijzonder nuttig is voor Quantum-garages, is Hamiltonian-garages.
In Hamiltonian-mechanismen geven de totale energie van een systeem en de (gegeneraliseerde) posities en tijdstippen alle informatie die nodig is om de beweging van een wille keurig klassiek object te beschrijven.
Laat $f (x, p, t) $ een deel van de gegeneraliseerde posities $x $ en Momenta $p $ van een systeem en laat $H (x, p, t) $ de functie Hamiltonian.
Als we bijvoorbeeld $f (x, p, t) = x (t) $ en $H (x, p, t) = p ^ 2 (t)/2m-V (x, t) $, zouden we het bovenstaande geval van Newtonian Dynamics herstellen.
In het algemeen hebben we dat \begin{align} \frac{d}{DT} f &= \ partial_t f-(\ partial_x H \ partial_p f + \ partial_p H \ partial_x f) \\ \\ & \defeq \ partial_t f + \\ {f, H \\ }.
\end{align} hier $ \\ {f, H \\ } $ wordt de [Poisson-haak](https://en.wikipedia.org/wiki/Poisson_bracket) genoemd en wordt weer gegeven in de klassieke dynamiek vanwege de centrale rol die wordt afgespeeld bij het definiëren van Dynamics.

Kwantum dynamiek kan worden beschreven in exact dezelfde taal.
De Hamiltonian, of totale energie, geeft volledig de dynamiek van een gesloten Quantum systeem op.
Er zijn echter enkele belang rijke verschillen tussen de twee theories.
In klassieke mechanismen $x $ en $p $ zijn alleen cijfers, terwijl ze in Quantum-mechanismen niet zijn.
Ze werken niet zelfs niet als werkend: $xp \ne px $.

Het juiste wiskundige concept om deze niet-werk objecten te beschrijven, is een operator, in gevallen waarin $x $ en $p $ alleen een afzonderlijke set waarden kan hebben die samen vallen met het concept van een matrix.
Ter vereenvoudiging gaan we ervan uit dat ons Quantum systeem eindig is zodat het kan worden beschreven met behulp van [vectoren en matrices](xref:microsoft.quantum.concepts.vectors).
Deze matrices moeten verder worden Hermitian (wat betekent dat de conjugaat van de matrix hetzelfde is als de oorspronkelijke matrix).
Dit zorgt ervoor dat de eigenvalues van de matrices reële waarde heeft. een voor waarde die wordt opgelegd om ervoor te zorgen dat er een hoeveelheid wordt gemeten op basis van een positie, waarbij we een imaginair nummer niet ophalen.

Net zoals de analogen van de positie en het momentum in de Quantum-garages moeten worden vervangen door Opera Tors, moet de functie Hamiltonian ook worden vervangen door een operator.
Bijvoorbeeld: voor een partikel in vrije ruimte hebben we dat $H (x, p) = p ^ 2/2 min. $, terwijl in de Quantum-mechanismen de Hamiltonian-operator $ \hat{H} $ $ \hat{H} = \hat{p} ^ 2/2 min. $, waarbij $ \hat{p} $ de momentum-operator is.
Vanuit dit perspectief is het niet meer nodig om de variabelen die worden gebruikt in de normale dynamiek te vervangen door Opera tors van klassiek naar Quantum Dynamics.
Zodra we de Hamiltonian-operator hebben gebouwd door de gewone klassieke Hamiltonian te vertalen naar de Quantum taal, kunnen we de dynamiek van een wille keurige Quantum hoeveelheid (d.w.z. quantum mechanisch-operator) uitdrukken. $ \hat{f} (t) $ via \begin{align} \frac{d}{DT} \hat{f} = \ partial_t \hat{f} + [\hat{f}, \hat{H}], \end{align}, waarbij $ [f, H]
Deze expressie is precies hetzelfde als de klassieke expressie hierboven met het verschil dat de Poisson-haak $ \\ {f, H \\ } $ wordt vervangen door de commutator tussen $f $ en $H $.
Dit proces van het nemen van een klassieke Hamiltonian en het gebruik ervan om een Quantum Hamiltonian te vinden, is bekend als canonieke waarde voor kwantisatiefouten.

Welke Opera tors $f $ zijn het meest geïnteresseerd in?  Het antwoord hierop is afhankelijk van het probleem dat u wilt oplossen.
Misschien is het meest bruikbare aantal dat u kunt vinden, de Quantum State-operator, zoals beschreven in de eerdere conceptuele documentatie, waarmee alles kan worden geëxtraheerd over de dynamiek.
Nadat u dit hebt gedaan (en het resultaat te vereenvoudigen in geval van een pure staat), wordt de Schrödinger-vergelijking voor de Quantum status gevonden \begin{align} i \ partial_t \ket{\psi (t)} = \hat{H} (t) \ket{\psi (t)}.
\end{align}

Deze vergelijking kan echter minder intuïtief zijn dan hierboven vermeld, maar kan ook de eenvoudigste expressie opleveren voor het simuleren van Quantum dynamiek op een Quantum of klassieke computer.
Dit komt doordat de oplossing voor de differentiële vergelijking kan worden weer gegeven in de volgende vorm (voor het geval waarin de Hamiltonian constant is in $t $) \begin{align} \ket{\psi (t)} = e ^ {-iHt} \ket{\psi (0)}.
\end{align} hier $e ^ {-iHt} $ een unitary-matrix is.
Dit betekent dat er een Quantum circuit is dat kan worden ontworpen om het uit te voeren, omdat quantum computers de unitary matrix nauw keurig kunnen benaderen.
Deze handeling van het vinden van een Quantum circuit voor het implementeren van de Quantum time evolutie operator $e ^ {-iHt} $ is wat vaak Quantum simulatie wordt genoemd, of met name een dynamische Quantum simulatie.
