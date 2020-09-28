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
# <a name="develop-with-no-locq-and-binder"></a>Ontwikkelen met Q# en Binder

U kunt Binder gebruiken om uw Jupyter Notebooks online uit te voeren en te delen.

## <a name="use-binder-with-the-microsoft-qdk-samples"></a>Binder gebruiken met de Microsoft QDK-voorbeelden

Binder configureren om automatisch gebruik te maken van de Microsoft QDK-voorbeelden:

1. Open een browser en voer https://aka.ms/try-qsharp uit.
1. Klik op de landingspagina **Quantum Development Kit-voorbeelden** op **Q#-notebook** voor meer informatie over hoe u IQ# gebruikt om uw eigen kwantumtoepassingsnotebooks te schrijven.

![QDK-landingspagina](~/media/binder-install.png)

## <a name="use-binder-with-your-own-notebooks-and-repository"></a>Binder gebruiken met uw eigen notebooks en opslagplaats

Als u al notebooks in een GitHub-opslagplaats hebt, kunt u Binder configureren om te werken met uw opslagplaats:

1. Zorg ervoor dat er zich een bestand met de naam *Dockerfile* bevindt in de hoofdmap van uw opslagplaats. Het bestand moet minstens de volgende regels bevatten:

    ```bash
    FROM mcr.microsoft.com/quantum/iqsharp-base:0.12.20082513
    
    USER root
    COPY . ${HOME}
    RUN chown -R ${USER} ${HOME}
    
    USER ${USER}
    ```

    > [!NOTE]
    > U kunt de actueelste versie van IQ# verifiëren in de [releaseopmerkingen](xref:microsoft.quantum.relnotes).

    Raadpleeg voor meer informatie over het maken van een Dockerfile de [Dockerfile-referentie](https://docs.docker.com/engine/reference/builder/).

2. Open een browser in [mybinder.org](https://mybinder.org).
3. Voer uw opslagplaatsnaam in als de **GitHub-URL** (bijvoorbeeld *MijnNaam/MijnOpslag*) en klik op **Starten**.

![MyBinder-formulier](~/media/mybinder.png)
    
## <a name="next-steps"></a>Volgende stappen

Nu u uw Binder-omgeving hebt ingesteld, kunt u uw [eerste kwantumprogramma](xref:microsoft.quantum.quickstarts.qrng) schrijven en uitvoeren.
