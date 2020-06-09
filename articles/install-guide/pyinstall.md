---
title: 'Ontwikkelen met Q # en python'
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.python
ms.openlocfilehash: f18d005012dc1c52aab456f1c7b194d182cab786
ms.sourcegitcommit: c8ebc5d7d8581444754f5d7bfaca2f25601f1b14
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/09/2020
ms.locfileid: "84578161"
---
# <a name="develop-with-q-and-python"></a><span data-ttu-id="c88a4-102">Ontwikkelen met Q # en python</span><span class="sxs-lookup"><span data-stu-id="c88a4-102">Develop with Q# and Python</span></span>

<span data-ttu-id="c88a4-103">Installeer de QDK om python-hosttoepassingen te ontwikkelen om Q #-bewerkingen aan te roepen.</span><span class="sxs-lookup"><span data-stu-id="c88a4-103">Install the QDK to develop Python host programs to call Q# operations.</span></span>

1. <span data-ttu-id="c88a4-104">Vereisten</span><span class="sxs-lookup"><span data-stu-id="c88a4-104">Pre-requisites</span></span>

    - <span data-ttu-id="c88a4-105">[Python](https://www.python.org/downloads/) 3.6 of hoger</span><span class="sxs-lookup"><span data-stu-id="c88a4-105">[Python](https://www.python.org/downloads/) 3.6 or later</span></span>
    - <span data-ttu-id="c88a4-106">Python-pakketbeheer voor [PIP](https://pip.pypa.io/en/stable/installing)</span><span class="sxs-lookup"><span data-stu-id="c88a4-106">The [PIP](https://pip.pypa.io/en/stable/installing) Python package manager</span></span>
    - [<span data-ttu-id="c88a4-107">.NET Core SDK 3,1</span><span class="sxs-lookup"><span data-stu-id="c88a4-107">.NET Core SDK 3.1</span></span>](https://dotnet.microsoft.com/download/dotnet-core/3.1)


1. <span data-ttu-id="c88a4-108">Installeer het `qsharp` pakket, een python-pakket dat Interop mogelijk maakt tussen Q # en python.</span><span class="sxs-lookup"><span data-stu-id="c88a4-108">Install the `qsharp` package, a Python package that enables interop between Q# and Python.</span></span>

    ```
    pip install qsharp
    ```

1. <span data-ttu-id="c88a4-109">Installeer IQ #, een kernel die wordt gebruikt door Jupyter en python die de kern functionaliteit biedt voor het compileren en uitvoeren van Q #-bewerkingen.</span><span class="sxs-lookup"><span data-stu-id="c88a4-109">Install IQ#, a kernel used by Jupyter and Python that provides the core functionality for compiling and executing Q# operations.</span></span>

    ```dotnetcli
    dotnet tool install -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```
  
1. <span data-ttu-id="c88a4-110">Hoewel u Q # met python kunt gebruiken in een IDE, raden we u aan om met behulp van de IDE # + python-toepassingen van de Q # code (VS code) te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="c88a4-110">While you can use Q# with Python in any IDE, we highly recommend using Visual Studio Code (VS Code) IDE for your Q# + Python applications.</span></span> <span data-ttu-id="c88a4-111">Met Visual Studio code en de Visual Studio code extension van QDK krijgt u toegang tot uitgebreide functionaliteit.</span><span class="sxs-lookup"><span data-stu-id="c88a4-111">By using Visual Studio Code and the QDK Visual Studio Code extension you gain access to richer functionality.</span></span>

    - <span data-ttu-id="c88a4-112">[VS-code](https://code.visualstudio.com/download) installeren (Windows, Linux en Mac)</span><span class="sxs-lookup"><span data-stu-id="c88a4-112">Install [VS Code](https://code.visualstudio.com/download) (Windows, Linux and Mac)</span></span>
    - <span data-ttu-id="c88a4-113">Installeer de [QDK-uitbrei ding voor VS code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).</span><span class="sxs-lookup"><span data-stu-id="c88a4-113">Install the [QDK extension for VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).</span></span>

1. <span data-ttu-id="c88a4-114">Controleer de installatie door een `Hello World`-toepassing te maken</span><span class="sxs-lookup"><span data-stu-id="c88a4-114">Verify the installation by creating a `Hello World` application</span></span>

    - <span data-ttu-id="c88a4-115">Maak een minimale Q#-bewerking door een bestand met de naam `Operation.qs` te maken en er de volgende code aan toe te voegen:</span><span class="sxs-lookup"><span data-stu-id="c88a4-115">Create a minimal Q# operation, by creating a file called `Operation.qs`, and adding the following code to it:</span></span>

        ```qsharp
        namespace HelloWorld {
            open Microsoft.Quantum.Intrinsic;
            open Microsoft.Quantum.Canon;

            operation SayHello() : Unit {
                Message("Hello from quantum world!");
            }
        }
        ```

    - <span data-ttu-id="c88a4-116">Maak een Python-programma met de naam `hello_world.py` om de Q#-bewerking `SayHello()` aan te roepen:</span><span class="sxs-lookup"><span data-stu-id="c88a4-116">Create a Python program called `hello_world.py` to call the Q# `SayHello()` operation:</span></span>

        ```python
        import qsharp

        from HelloWorld import SayHello

        SayHello.simulate()
        ```

    - <span data-ttu-id="c88a4-117">Voer het programma uit:</span><span class="sxs-lookup"><span data-stu-id="c88a4-117">Run the program:</span></span>

        ```
        python hello_world.py
        ```

    - <span data-ttu-id="c88a4-118">Controleer de uitvoer.</span><span class="sxs-lookup"><span data-stu-id="c88a4-118">Verify the output.</span></span> <span data-ttu-id="c88a4-119">Met het programma worden de volgende regels uitgevoerd:</span><span class="sxs-lookup"><span data-stu-id="c88a4-119">Your program should output the following lines:</span></span>

        ```
        Hello from quantum world!
        ```


> [!NOTE]
> * <span data-ttu-id="c88a4-120">U kunt ook python Jupyter-notebooks gebruiken om het klassieke python-programma te schrijven en Q #-bewerkingen van de cellen aan te roepen.</span><span class="sxs-lookup"><span data-stu-id="c88a4-120">You can also use Python Jupyter notebooks to write the classical Python program and call Q# operations from the cells.</span></span> <span data-ttu-id="c88a4-121">De python-code is slechts een normaal python-programma.</span><span class="sxs-lookup"><span data-stu-id="c88a4-121">The Python code is just a normal Python program.</span></span>

## <a name="next-steps"></a><span data-ttu-id="c88a4-122">Volgende stappen</span><span class="sxs-lookup"><span data-stu-id="c88a4-122">Next steps</span></span>

<span data-ttu-id="c88a4-123">Nu u de Quantum development kit hebt geïnstalleerd in de omgeving van uw voorkeur, kunt u [uw eerste kwantumprogramma](xref:microsoft.quantum.quickstarts.qrng) schrijven en uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="c88a4-123">Now that you have installed the Quantum Development Kit in your preferred environment, you can write and run [your first quantum program](xref:microsoft.quantum.quickstarts.qrng).</span></span>
