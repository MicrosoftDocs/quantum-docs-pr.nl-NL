---
title: Ontwikkelen met Q# en Binder
description: Meer informatie over hoe u een Q#-toepassing maakt met Binder.
author: bradben
ms.author: v-benbra
ms.date: 9/03/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.binder
no-loc:
- Q#
- $$v
ms.openlocfilehash: f993a1145dd8c01045d4cc7cfd0c98efd574ea78
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/21/2020
ms.locfileid: "90836536"
---
# <a name="develop-with-no-locq-and-binder"></a><span data-ttu-id="fd2a8-103">Ontwikkelen met Q# en Binder</span><span class="sxs-lookup"><span data-stu-id="fd2a8-103">Develop with Q# and Binder</span></span>

<span data-ttu-id="fd2a8-104">U kunt Binder gebruiken om uw Jupyter Notebooks online uit te voeren en te delen.</span><span class="sxs-lookup"><span data-stu-id="fd2a8-104">You can use Binder to run and share your Jupyter Notebooks online.</span></span>

## <a name="use-binder-with-the-microsoft-qdk-samples"></a><span data-ttu-id="fd2a8-105">Binder gebruiken met de Microsoft QDK-voorbeelden</span><span class="sxs-lookup"><span data-stu-id="fd2a8-105">Use Binder with the Microsoft QDK samples</span></span>

<span data-ttu-id="fd2a8-106">Binder configureren om automatisch gebruik te maken van de Microsoft QDK-voorbeelden:</span><span class="sxs-lookup"><span data-stu-id="fd2a8-106">To configure Binder automatically to use the Microsoft QDK samples:</span></span>

1. <span data-ttu-id="fd2a8-107">Open een browser en voer https://aka.ms/try-qsharp uit.</span><span class="sxs-lookup"><span data-stu-id="fd2a8-107">Open a browser and run https://aka.ms/try-qsharp.</span></span>
1. <span data-ttu-id="fd2a8-108">Klik op de landingspagina **Quantum Development Kit-voorbeelden** op **Q#-notebook** voor meer informatie over hoe u IQ# gebruikt om uw eigen kwantumtoepassingsnotebooks te schrijven.</span><span class="sxs-lookup"><span data-stu-id="fd2a8-108">On the **Quantum Development Kit Samples** landing page, click **Q# notebook** to learn how to use IQ# to write your own quantum application notebooks.</span></span>

![QDK-landingspagina](~/media/binder-install.png)

## <a name="use-binder-with-your-own-notebooks-and-repository"></a><span data-ttu-id="fd2a8-110">Binder gebruiken met uw eigen notebooks en opslagplaats</span><span class="sxs-lookup"><span data-stu-id="fd2a8-110">Use Binder with your own notebooks and repository</span></span>

<span data-ttu-id="fd2a8-111">Als u al notebooks in een GitHub-opslagplaats hebt, kunt u Binder configureren om te werken met uw opslagplaats:</span><span class="sxs-lookup"><span data-stu-id="fd2a8-111">If you already have notebooks in a GitHub repository, you can configure Binder to work with your repo:</span></span>

1. <span data-ttu-id="fd2a8-112">Zorg ervoor dat er zich een bestand met de naam *Dockerfile* bevindt in de hoofdmap van uw opslagplaats.</span><span class="sxs-lookup"><span data-stu-id="fd2a8-112">Ensure that there is a file named *Dockerfile* in the root of your repository.</span></span> <span data-ttu-id="fd2a8-113">Het bestand moet minstens de volgende regels bevatten:</span><span class="sxs-lookup"><span data-stu-id="fd2a8-113">The file must contain at least the following lines:</span></span>

    ```bash
    FROM mcr.microsoft.com/quantum/iqsharp-base:0.12.20082513
    
    USER root
    COPY . ${HOME}
    RUN chown -R ${USER} ${HOME}
    
    USER ${USER}
    ```

    > [!NOTE]
    > <span data-ttu-id="fd2a8-114">U kunt de actueelste versie van IQ# verifiëren in de [releaseopmerkingen](xref:microsoft.quantum.relnotes).</span><span class="sxs-lookup"><span data-stu-id="fd2a8-114">You can verify the most current version of IQ# in the [Release Notes](xref:microsoft.quantum.relnotes).</span></span>

    <span data-ttu-id="fd2a8-115">Raadpleeg voor meer informatie over het maken van een Dockerfile de [Dockerfile-referentie](https://docs.docker.com/engine/reference/builder/).</span><span class="sxs-lookup"><span data-stu-id="fd2a8-115">For more information about creating a Dockerfile, see the [Dockerfile reference](https://docs.docker.com/engine/reference/builder/).</span></span>

2. <span data-ttu-id="fd2a8-116">Open een browser in [mybinder.org](https://mybinder.org).</span><span class="sxs-lookup"><span data-stu-id="fd2a8-116">Open a browser to [mybinder.org](https://mybinder.org).</span></span>
3. <span data-ttu-id="fd2a8-117">Voer uw opslagplaatsnaam in als de **GitHub-URL** (bijvoorbeeld *MijnNaam/MijnOpslag*) en klik op **Starten**.</span><span class="sxs-lookup"><span data-stu-id="fd2a8-117">Enter your repository name as the **GitHub URL** (for example *MyName/MyRepo*), and click **launch**.</span></span>

![MyBinder-formulier](~/media/mybinder.png)
    
## <a name="next-steps"></a><span data-ttu-id="fd2a8-119">Volgende stappen</span><span class="sxs-lookup"><span data-stu-id="fd2a8-119">Next steps</span></span>

<span data-ttu-id="fd2a8-120">Nu u uw Binder-omgeving hebt ingesteld, kunt u uw [eerste kwantumprogramma](xref:microsoft.quantum.quickstarts.qrng) schrijven en uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="fd2a8-120">Now that you have set up your Binder environment, you can write and run [your first quantum program](xref:microsoft.quantum.quickstarts.qrng).</span></span>
