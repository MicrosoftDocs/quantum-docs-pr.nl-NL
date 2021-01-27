---
title: Inleiding tot het kwantumpakket voor machine learning | Microsoft Docs
description: Inleiding tot het kwantumpakket voor machine learning
author: QuantumWriter
ms.author: alexeib
ms.date: 12/5/2019
ms.topic: conceptual
uid: microsoft.quantum.machine-learning.concepts.intro
no-loc:
- Q#
- $$v
ms.openlocfilehash: 1e36948a216a06d76b99cd451bbfac6f5defd7c8
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98858781"
---
# <a name="introduction-to-the-quantum-machine-learning-library"></a><span data-ttu-id="fb67b-103">Inleiding tot de kwantumbibliotheek voor machine learning</span><span class="sxs-lookup"><span data-stu-id="fb67b-103">Introduction to the Quantum Machine Learning Library</span></span>

<span data-ttu-id="fb67b-104">De kwantumbibliotheek voor machine learning is een API, geschreven in Q#, waarmee u hybride kwantum/klassieke machine learning-experimenten kunt uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="fb67b-104">The Quantum Machine Learning Library is an API, written in Q#, that gives you the ability to run hybrid quantum/classical machine learning experiments.</span></span> <span data-ttu-id="fb67b-105">De bibliotheek biedt u de volgende mogelijkheden:</span><span class="sxs-lookup"><span data-stu-id="fb67b-105">The library gives you the ability to:</span></span>

- <span data-ttu-id="fb67b-106">Uw eigen gegevens laden om te classificeren met kwantumsimulators</span><span class="sxs-lookup"><span data-stu-id="fb67b-106">Load your own data to classify with quantum simulators</span></span>

- <span data-ttu-id="fb67b-107">Voorbeelden en zelfstudies gebruiken om kennis te maken met kwantum machine learning</span><span class="sxs-lookup"><span data-stu-id="fb67b-107">Use samples and tutorials to get introduced to the field of quantum machine learning</span></span>

<span data-ttu-id="fb67b-108">U kunt beperkte prestaties verwachten in vergelijking met de huidige klassieke machine learning-frameworks (houd er rekening mee dat alles wordt uitgevoerd bovenop de technisch veeleisende simulatie van een kwantumapparaat).</span><span class="sxs-lookup"><span data-stu-id="fb67b-108">You can expect low performance compared to current classical machine learning frameworks (remember that everything is running on top of the simulation of a quantum device that is already computationally expensive).</span></span>

<span data-ttu-id="fb67b-109">Het doel van dit document is:</span><span class="sxs-lookup"><span data-stu-id="fb67b-109">The purpose of this documentation is:</span></span>

- <span data-ttu-id="fb67b-110">Een beknopte inleiding bieden voor machine learning-hulpmiddelen (geschreven in Q\#) voor hybride kwantum/klassieke machine learning.</span><span class="sxs-lookup"><span data-stu-id="fb67b-110">A concise introduction to machine learning tools (written in Q\#) for hybrid quantum/classical learning.</span></span>
- <span data-ttu-id="fb67b-111">Een inleiding bieden voor machine learning-concepten en dan vooral voor hoe deze kwantumcircuit-georiënteerde classificaties realiseren (ook wel sequentiële kwantumclassificaties genoemd).</span><span class="sxs-lookup"><span data-stu-id="fb67b-111">Introduce machine learning concepts and specifically their realization in quantum circuit centric classifiers (also known as quantum sequential classifiers).</span></span>
- <span data-ttu-id="fb67b-112">Een aantal zelfstudies bieden over de basisbeginselen, zodat u aan de slag kunt met de hulpprogram ma's in de bibliotheek.</span><span class="sxs-lookup"><span data-stu-id="fb67b-112">Provide a set of tutorials on the basics to start using the tools provided by the library.</span></span>
- <span data-ttu-id="fb67b-113">Bespreek de trainings- en validatiemethoden voor deze classificaties en hoe deze worden omgezet in specifieke Q\#-bewerkingen die de bibliotheek mogelijk maakt.</span><span class="sxs-lookup"><span data-stu-id="fb67b-113">Discuss the training and validation methods for such classifiers and how they translate into specific Q\# operations provided by the library.</span></span>

<span data-ttu-id="fb67b-114">Het in deze bibliotheek geïmplementeerde model is gebaseerd op het kwantum-klassieke trainingsschema dat wordt beschreven in [Circuit-centric quantum classifiers](https://arxiv.org/abs/1804.00633)</span><span class="sxs-lookup"><span data-stu-id="fb67b-114">The model implemented in this library is based on the quantum-classical training scheme presented in [Circuit-centric quantum classifiers](https://arxiv.org/abs/1804.00633)</span></span>
