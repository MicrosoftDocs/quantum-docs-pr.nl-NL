---
title: Ontwikkelen met Q# en Binder
description: Meer informatie over hoe u een Q#-toepassing maakt met Binder.
author: bradben
ms.author: v-benbra
ms.date: 9/03/2020
ms.topic: quickstart
uid: microsoft.quantum.install.binder
no-loc:
- Q#
- $$v
ms.openlocfilehash: f7e9b1ae67d6275ec7ba39ea411842dc537536c5
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98856716"
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
