---
title: 'Q #-technieken-lokale variabelen | Microsoft Docs'
description: 'Q #-technieken-lokale variabelen'
author: QuantumWriter
ms.author: Christopher.Granade@microsoft.com
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: 4f5eff1ee8482fa5e5fee9dff421efab93fc0c5a
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/26/2019
ms.locfileid: "73183281"
---
# <a name="local-variables"></a><span data-ttu-id="d756d-103">Lokale variabelen</span><span class="sxs-lookup"><span data-stu-id="d756d-103">Local Variables</span></span> #

<span data-ttu-id="d756d-104">Een waarde van elk type in Q # kan worden toegewezen aan een variabele voor hergebruik in een bewerking of functie met behulp van het sleutel woord `let`.</span><span class="sxs-lookup"><span data-stu-id="d756d-104">A value of any type in Q# can be assigned to a variable for reuse within an operation or function by using the `let` keyword.</span></span>
<span data-ttu-id="d756d-105">Bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="d756d-105">For instance:</span></span>

```qsharp
let measurementOperator = [PauliX, PauliZ, PauliZ, PauliX, PauliI];
```

<span data-ttu-id="d756d-106">Hiermee wijst u een bepaalde matrix van Pauli-Opera tors toe aan een variabele met de naam `measurementOperator`.</span><span class="sxs-lookup"><span data-stu-id="d756d-106">This assigns a particular array of Pauli operators to a variable called `measurementOperator`.</span></span>

> [!TIP]
> <span data-ttu-id="d756d-107">Houd er rekening mee dat het type van de nieuwe variabele niet expliciet moet worden opgegeven, omdat de expressie aan de rechter kant van de `let` instructie ondubbelzinnig is en het type wordt afgeleid door de compiler.</span><span class="sxs-lookup"><span data-stu-id="d756d-107">Note that we did not need to explicitly specify the type of our new variable, as the expression on the right-hand side of the `let` statement is unambiguous and the type is inferred by the compiler.</span></span> 

<span data-ttu-id="d756d-108">Variabelen in Q # kunnen *onveranderbaar*zijn, wat betekent dat wanneer een variabele op deze manier is gedefinieerd, deze niet meer op een wille keurige manier kan worden gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="d756d-108">Variables in Q# are *immutable*, meaning that once a variable has been defined in this way, it can no longer be changed in any way.</span></span>
<span data-ttu-id="d756d-109">Dit maakt een aantal gunstige optimalisaties mogelijk, waaronder de optimalisatie van de klassieke logica die op variabelen moet worden gerangschikt om de `Adjoint` variant van een bewerking toe te passen.</span><span class="sxs-lookup"><span data-stu-id="d756d-109">This allows for several beneficial optimizations, including optimization of the classical logic acting on variables to be reordered for applying the `Adjoint` variant of an operation.</span></span>

<span data-ttu-id="d756d-110">Variabelen die zijn gedefinieerd met behulp van de `let` binding als hierboven, zijn lokaal voor een bepaald bereik, zoals de hoofd tekst van een bewerking of de inhoud van een `for`-lus.</span><span class="sxs-lookup"><span data-stu-id="d756d-110">Variables defined using the `let` binding as above are local to a particular scope, such as the body of an operation or the contents of a `for` loop.</span></span>


## <a name="mutability"></a><span data-ttu-id="d756d-111">Veranderlijkheid</span><span class="sxs-lookup"><span data-stu-id="d756d-111">Mutability</span></span> ##

<span data-ttu-id="d756d-112">Als alternatief voor het maken van een variabele met `let`wordt met het sleutel woord `mutable` een speciale onveranderlijke variabele gemaakt die opnieuw kan worden gebonden nadat deze in eerste instantie is gemaakt met behulp van het sleutel woord `set`.</span><span class="sxs-lookup"><span data-stu-id="d756d-112">As an alternative to creating a variable with `let`, the `mutable` keyword will create a special mutable variable that can be re-bound after it is initially created by using the `set` keyword.</span></span>

```qsharp
operation RandomInts(maxInt : Int, nrSamples : Int) : Int[] {
    mutable samples = new Int[0];
    for (i in 1 .. nrSamples) {
        set samples += [RandomInt(maxInt)];
    }
    return samples;
}
```

<span data-ttu-id="d756d-113">Alle typen in Q #, inclusief matrices, volgen de waarde semantiek.</span><span class="sxs-lookup"><span data-stu-id="d756d-113">All types in Q#, including arrays, follow value semantics.</span></span> <span data-ttu-id="d756d-114">Met name het is niet mogelijk om matrix items bij te werken.</span><span class="sxs-lookup"><span data-stu-id="d756d-114">In particular, it is not possible to update array items.</span></span> <span data-ttu-id="d756d-115">Als u een bestaande matrix wilt wijzigen, moet u een methode voor kopiëren en bijwerken gebruiken die vergelijkbaar is met F#die voor records in.</span><span class="sxs-lookup"><span data-stu-id="d756d-115">To modify an existing array requires leveraging a copy-and-update mechanism much like the one for records in F#.</span></span> <span data-ttu-id="d756d-116">Met de bibliotheek hulpprogramma's voor matrices die zijn opgegeven in [`Microsoft.Quantum.Arrays`](xref:microsoft.quantum.arrays), kunt u bijvoorbeeld eenvoudig een functie definiëren die een matrix van PAULIS retourneert waarbij de Pauli bij index `i` de gegeven waarde heeft en alle andere vermeldingen de identiteit zijn:</span><span class="sxs-lookup"><span data-stu-id="d756d-116">Using the library tools for arrays provided in [`Microsoft.Quantum.Arrays`](xref:microsoft.quantum.arrays), we can e.g. easily define a function that returns an array of Paulis where the Pauli at index `i` takes the given value and all other entries are the identity:</span></span> 

```qsharp
function EmbedPauli (pauli : Pauli, i : Int, n : Int) : Pauli[] {
    
    let arr = ConstantArray(n, PauliI); // creates an array of filled with PauliI
    return arr w/ i <- pauli; // constructs a new array based on arr except that entry i is set to pauli
}
```

<span data-ttu-id="d756d-117">Meer informatie over het werken met matrices vindt u in het bespreken van Q #-instructies en expressies.</span><span class="sxs-lookup"><span data-stu-id="d756d-117">We will elaborate more on how to work with arrays when discussing Q# statements and expressions.</span></span> 

<span data-ttu-id="d756d-118">Veranderlijkheid binnen Q # is een concept dat van toepassing is op een *symbool* in plaats van een type of waarde.</span><span class="sxs-lookup"><span data-stu-id="d756d-118">Mutability within Q# is a concept that applies to a *symbol* rather than a type or value.</span></span> <span data-ttu-id="d756d-119">In het bijzonder heeft het geen representatie in het type systeem, impliciet of expliciet, en of een binding wordt gewijzigd (zoals aangegeven door het sleutel woord `mutable`) of dat onveranderbaar is (zoals aangegeven door `let`) het type van de afhankelijke variabele (n) niet wijzigt.</span><span class="sxs-lookup"><span data-stu-id="d756d-119">Specifically, it does not have a representation in the type system, implicitly or explicitly, and whether or not a binding is mutable (as indicated by the `mutable` keyword) or immutable (as indicated by `let`) does not change the type of the bound variable(s).</span></span> <span data-ttu-id="d756d-120">Dit biedt een belang rijke manier om veranderlijkheid te isoleren in gespecialiseerde functies en bewerkingen.</span><span class="sxs-lookup"><span data-stu-id="d756d-120">This provides an important way to isolate mutability inside specialized functions and operations.</span></span>
<span data-ttu-id="d756d-121">Met name hoewel een adjoint specialisatie voor een bewerking die gebruikmaakt van een onveranderlijke variabele niet automatisch kan worden gegenereerd, werkt automatisch genereren prima voor een bewerking die een functie aanroept die gebruikmaakt van veranderlijkheid.</span><span class="sxs-lookup"><span data-stu-id="d756d-121">In particular, even though an adjoint specialization for an operation which uses a mutable variable cannot be auto-generated, auto-generation works fine for an operation calling a function which uses mutability.</span></span>
<span data-ttu-id="d756d-122">Daarom is het een goed idee om functies en bewerkingen te maken waarbij veranderlijkheid zo kort mogelijk en compact worden gebruikt, zodat de rest van het Quantum programma kan worden geschreven met behulp van gewone onveranderlijke variabelen.</span><span class="sxs-lookup"><span data-stu-id="d756d-122">For this reason, it is a good practice to make functions and operations which use mutability as short and compact as possible, so that the rest of the quantum program can be written using ordinary immutable variables.</span></span>


## <a name="deconstruction"></a><span data-ttu-id="d756d-123">Ontbouwing</span><span class="sxs-lookup"><span data-stu-id="d756d-123">Deconstruction</span></span> ##

<span data-ttu-id="d756d-124">Naast het toewijzen van één variabele, de sleutel woorden `let` en `mutable`, of in feite een andere bindings constructie, kunt u ook de inhoud van een tuple- [type](xref:microsoft.quantum.language.type-model#tuple-types)uitpakken.</span><span class="sxs-lookup"><span data-stu-id="d756d-124">In addition to assigning a single variable, the `let` and `mutable` keywords - or in fact any other binding construct - also allow for unpacking the contents of a [tuple type](xref:microsoft.quantum.language.type-model#tuple-types).</span></span>
<span data-ttu-id="d756d-125">Een toewijzing van dit formulier wordt genoemd om de elementen van die tuple te *ontconstrueren* .</span><span class="sxs-lookup"><span data-stu-id="d756d-125">An assignment of this form is said to *deconstruct* the elements of that tuple.</span></span>
<span data-ttu-id="d756d-126">Als we bijvoorbeeld een term in een Hamiltonian door een tuple model leren, kunnen we de ontbouwing gebruiken om toegang te krijgen tot de verschillende gegevens die we moeten simuleren onder deze term:</span><span class="sxs-lookup"><span data-stu-id="d756d-126">For instance, if we model a term in a Hamiltonian by a tuple, then we can use deconstruction to access the different data that we need to simulate under that term:</span></span>

```qsharp
// Represents H = 3.1 X_0 Z_1.
let (_, (paulis, idxQubits)) = ((3.1, 1.0), ([PauliX, PauliZ], [0, 1])); // paulis and idxQubits are both immutable variables
mutable ((c1, c2), _) = ((3.1, 1.0), ([PauliX, PauliZ], [0, 1])); // c1 and c2 are both mutable variables
```


