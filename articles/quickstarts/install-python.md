---
title: Ontwikkelen met Q# en Python
author: bradben
ms.author: bradben
ms.date: 5/30/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.python
ms.openlocfilehash: 6513acd5b9cdce15ce61ed2c0454f46e6a6d9bd0
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/23/2020
ms.locfileid: "85274048"
---
# <a name="develop-with-q-and-python"></a><span data-ttu-id="66868-102">Ontwikkelen met Q# en Python</span><span class="sxs-lookup"><span data-stu-id="66868-102">Develop with Q# and Python</span></span>

<span data-ttu-id="66868-103">Installeer de QDK om Python-hostprogramma's te ontwikkelen waarmee Q#-bewerkingen kunnen worden aangeroepen.</span><span class="sxs-lookup"><span data-stu-id="66868-103">Install the QDK to develop Python host programs to call Q# operations.</span></span>

1. <span data-ttu-id="66868-104">Vereisten</span><span class="sxs-lookup"><span data-stu-id="66868-104">Prerequisites</span></span>

    - <span data-ttu-id="66868-105">[Python](https://www.python.org/downloads/) 3.6 of hoger</span><span class="sxs-lookup"><span data-stu-id="66868-105">[Python](https://www.python.org/downloads/) 3.6 or later</span></span>
    - <span data-ttu-id="66868-106">Python-pakketbeheer voor [PIP](https://pip.pypa.io/en/stable/installing)</span><span class="sxs-lookup"><span data-stu-id="66868-106">The [PIP](https://pip.pypa.io/en/stable/installing) Python package manager</span></span>
    - [<span data-ttu-id="66868-107">.NET Core SDK 3.1</span><span class="sxs-lookup"><span data-stu-id="66868-107">.NET Core SDK 3.1</span></span>](https://dotnet.microsoft.com/download/dotnet-core/3.1)


1. <span data-ttu-id="66868-108">Installeer het `qsharp`-pakket, een Python-pakket dat interoperabiliteit mogelijk maakt tussen Q# en Python.</span><span class="sxs-lookup"><span data-stu-id="66868-108">Install the `qsharp` package, a Python package that enables interop between Q# and Python.</span></span>

    ```
    pip install qsharp
    ```

1. <span data-ttu-id="66868-109">Installeer IQ#, een kernel die hoofdzakelijk wordt gebruikt door Jupyter en Python, en die de kernfunctionaliteit biedt voor het compileren en uitvoeren van Q#-bewerkingen.</span><span class="sxs-lookup"><span data-stu-id="66868-109">Install IQ#, a kernel used by Jupyter and Python that provides the core functionality for compiling and executing Q# operations.</span></span>

    ```dotnetcli
    dotnet tool install -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

    > [!NOTE]
    > <span data-ttu-id="66868-110">Als er tijdens de `dotnet iqsharp install`-stap een fout optreedt, moet u een nieuw terminalvenster openen en het nogmaals proberen.</span><span class="sxs-lookup"><span data-stu-id="66868-110">If you get an error during the `dotnet iqsharp install` step, open a new terminal window and try again.</span></span>
    > <span data-ttu-id="66868-111">Als het daarna nog steeds niet werkt, zoekt u het geïnstalleerde `dotnet-iqsharp`-hulpprogramma (in Windows, `dotnet-iqsharp.exe`) en voert u dit uit:</span><span class="sxs-lookup"><span data-stu-id="66868-111">If this still doesn't work, try locating the installed `dotnet-iqsharp` tool (on Windows, `dotnet-iqsharp.exe`) and running:</span></span>
    > ```
    > /path/to/dotnet-iqsharp install --user --path-to-tool="/path/to/dotnet-iqsharp"
    > ```
    > <span data-ttu-id="66868-112">waarbij `/path/to/dotnet-iqsharp` moet worden vervangen door het absolute pad naar het `dotnet-iqsharp`-hulpprogramma in uw bestandssysteem.</span><span class="sxs-lookup"><span data-stu-id="66868-112">where `/path/to/dotnet-iqsharp` should be replaced by the absolute path to the `dotnet-iqsharp` tool in your file system.</span></span>
    > <span data-ttu-id="66868-113">Dit is meestal bij `.dotnet/tools` in de map van uw gebruikersprofiel.</span><span class="sxs-lookup"><span data-stu-id="66868-113">Typically this will be under `.dotnet/tools` in your user profile folder.</span></span>
  
1. <span data-ttu-id="66868-114">Hoewel u Q# met Python in elke IDE kunt gebruiken, raden we u ten zeerste aan om de IDE van Visual Studio Code (VS Code) voor uw Q# + Python-toepassingen te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="66868-114">While you can use Q# with Python in any IDE, we highly recommend using Visual Studio Code (VS Code) IDE for your Q# + Python applications.</span></span> <span data-ttu-id="66868-115">Met Visual Studio Code en de QDK Visual Studio Code-extensie krijgt u toegang tot meer functies.</span><span class="sxs-lookup"><span data-stu-id="66868-115">By using Visual Studio Code and the QDK Visual Studio Code extension you gain access to richer functionality.</span></span>

    - <span data-ttu-id="66868-116">Installeer [VS Code](https://code.visualstudio.com/download) (Windows, Linux en Mac)</span><span class="sxs-lookup"><span data-stu-id="66868-116">Install [VS Code](https://code.visualstudio.com/download) (Windows, Linux and Mac)</span></span>
    - <span data-ttu-id="66868-117">Installeer de [QDK-extensie voor VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).</span><span class="sxs-lookup"><span data-stu-id="66868-117">Install the [QDK extension for VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).</span></span>

1. <span data-ttu-id="66868-118">Controleer de installatie door een `Hello World`-toepassing te maken</span><span class="sxs-lookup"><span data-stu-id="66868-118">Verify the installation by creating a `Hello World` application</span></span>

    - <span data-ttu-id="66868-119">Maak een minimale Q#-bewerking door een bestand met de naam `Operation.qs` te maken en er de volgende code aan toe te voegen:</span><span class="sxs-lookup"><span data-stu-id="66868-119">Create a minimal Q# operation, by creating a file called `Operation.qs`, and adding the following code to it:</span></span>

        ```qsharp
        namespace HelloWorld {
            open Microsoft.Quantum.Intrinsic;
            open Microsoft.Quantum.Canon;

            operation SayHello() : Unit {
                Message("Hello from quantum world!");
            }
        }
        ```

    - <span data-ttu-id="66868-120">Maak een Python-programma met de naam `hello_world.py` om de Q#-bewerking `SayHello()` aan te roepen:</span><span class="sxs-lookup"><span data-stu-id="66868-120">Create a Python program called `hello_world.py` to call the Q# `SayHello()` operation:</span></span>

        ```python
        import qsharp

        from HelloWorld import SayHello

        SayHello.simulate()
        ```

    - <span data-ttu-id="66868-121">Voer het programma uit:</span><span class="sxs-lookup"><span data-stu-id="66868-121">Run the program:</span></span>

        ```
        python hello_world.py
        ```

    - <span data-ttu-id="66868-122">Controleer de uitvoer.</span><span class="sxs-lookup"><span data-stu-id="66868-122">Verify the output.</span></span> <span data-ttu-id="66868-123">Met het programma worden de volgende regels uitgevoerd:</span><span class="sxs-lookup"><span data-stu-id="66868-123">Your program should output the following lines:</span></span>

        ```
        Hello from quantum world!
        ```


> [!NOTE]
> * <span data-ttu-id="66868-124">U kunt Python Jupyter Notebooks ook gebruiken om het klassieke Python-programma te schrijven en Q#-bewerkingen vanuit de cellen aan te roepen.</span><span class="sxs-lookup"><span data-stu-id="66868-124">You can also use Python Jupyter notebooks to write the classical Python program and call Q# operations from the cells.</span></span> <span data-ttu-id="66868-125">De Python-code is een regulier Python-programma.</span><span class="sxs-lookup"><span data-stu-id="66868-125">The Python code is just a normal Python program.</span></span>

## <a name="next-steps"></a><span data-ttu-id="66868-126">Volgende stappen</span><span class="sxs-lookup"><span data-stu-id="66868-126">Next steps</span></span>

<span data-ttu-id="66868-127">Nu u de Quantum development kit hebt geïnstalleerd in de omgeving van uw voorkeur, kunt u [uw eerste kwantumprogramma](xref:microsoft.quantum.quickstarts.qrng) schrijven en uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="66868-127">Now that you have installed the Quantum Development Kit in your preferred environment, you can write and run [your first quantum program](xref:microsoft.quantum.quickstarts.qrng).</span></span>