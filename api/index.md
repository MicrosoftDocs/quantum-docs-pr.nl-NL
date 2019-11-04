---
uid: microsoft.quantum.standardlibsintro
title: Q#-standaardbibliotheek voor Microsoft Quantum
description: Referentiedocumentatie voor de Q#-standaardbibliotheek voor Microsoft Quantum
author: natke
ms.author: nakersha
ms.date: 09/04/2019
ms.topic: landing-page
ms.openlocfilehash: 25a53e1cb8577761ef89cdcf2cfcddc509093f86
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/29/2019
ms.locfileid: "73056970"
---
# <a name="q-standard-libraries"></a><span data-ttu-id="d6692-103">Q#-standaardbibliotheken</span><span class="sxs-lookup"><span data-stu-id="d6692-103">Q# standard libraries</span></span> #

<span data-ttu-id="d6692-104">Q# wordt ondersteund door allerlei verschillende nuttige bewerkingen, functies en door de gebruiker gedefinieerde typen waaruit de Q#-*standaardbibliotheek* bestaat.</span><span class="sxs-lookup"><span data-stu-id="d6692-104">Q# is supported by a range of different useful operations, functions, and user-defined types that comprise the Q# *standard library*.</span></span>
<span data-ttu-id="d6692-105">De Q#-standaardbibliotheek is onderverdeeld in twee hoofdonderdelen:</span><span class="sxs-lookup"><span data-stu-id="d6692-105">The Q# standard library is split into two main parts:</span></span>

- <span data-ttu-id="d6692-106">**De prelude**: bewerkingen en functies die zijn gedefinieerd als onderdeel van de doelcomputer en compiler, doorgaans in klassieke systeemeigen .NET-code.</span><span class="sxs-lookup"><span data-stu-id="d6692-106">**The prelude**: operations and functions defined as a part of the target machine and compiler, typically in classical native .NET code.</span></span>
  <span data-ttu-id="d6692-107">Over het algemeen kan de prelude op verschillende doelcomputers verschillend zijn geïmplementeerd zodat deze geschikt is het betreffende systeem.</span><span class="sxs-lookup"><span data-stu-id="d6692-107">In general, different target machines may have different implementations of the prelude appropriate to each system.</span></span>
- <span data-ttu-id="d6692-108">**De canon**: bewerkingen en functies die zijn gedefinieerd in Q# en voortbouwen op de logica die is gedefinieerd in de prelude.</span><span class="sxs-lookup"><span data-stu-id="d6692-108">**The canon**: operations and functions defined in Q# building on the logic defined in the prelude.</span></span>
  <span data-ttu-id="d6692-109">De implementatie van de canon is agnostisch met betrekking tot doelcomputers.</span><span class="sxs-lookup"><span data-stu-id="d6692-109">The canon implementation is agnostic with respect to target machines.</span></span>
<span data-ttu-id="d6692-110">&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;</span><span class="sxs-lookup"><span data-stu-id="d6692-110">&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;</span></span>