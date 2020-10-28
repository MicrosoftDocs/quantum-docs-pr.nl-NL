---
uid: Microsoft.Quantum.AmplitudeAmplification
title: Micro soft. Quantum. AmplitudeAmplification-naam ruimte
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: namespace
qsharp.name: Microsoft.Quantum.AmplitudeAmplification
qsharp.summary: This namespace contains functions and operations for performing amplitude amplification.
ms.openlocfilehash: 09c29bd9d0648bb8652051ad97ceca6ef6557df3
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707728"
---
# <a name="microsoftquantumamplitudeamplification-namespace"></a>Micro soft. Quantum. AmplitudeAmplification-naam ruimte

Deze naam ruimte bevat functies en bewerkingen voor het uitvoeren van amplitude versterking.



## <a name="description"></a>Beschrijving

Obliviouse amplitude versterking met gedeeltelijke reflecties is de meest algemene vorm van amplitude versterking die hier wordt geïmplementeerd.

Dit wordt aangeroepen via de bewerking AmpAmpObliviousByReflectionPhases.

Dit heeft twee registers: `ancillaRegister` en `systemRegister` .

Dit accepteert twee Oracle voor deze reflecties van het type `ReflectionOracle` dat alleen op de kassa kan worden toegepast `ancillaRegister` .

Dit aanvaardt een specifiek Oracle-obliviouse amplitude versterking van het type `ObliviousOracle` dat gezamenlijk op beide registraties reageert.

De invoer status `ancillaRegister` wordt aangenomen dat het unieke $-$1-eigenstate van de eerste reflectie operator $I-2 \ Ket {s} \ Bra {s} $ is.

Reflecties over een doel Quantum status worden vaak geïmplementeerd door de toegang tot een Oracle die de status voorbereidt op basis van de reken kracht $ \ket{0\cdots 0} $.

Voor onze conventies voor deze Oracle zijn twee kassa's vereist: een single-Qubit `flagQubit` registratie en een REGI ster voor alle andere zaken op het ancillaRegister-REGI ster.

Het Oracle van het type `StateOracle` oefent gezamenlijk uit op beide kassa's om de doel status te maken die door $ \ket {1} $ in het `flagQubit` REGI ster is gemarkeerd met een echte amplitude.

De reflectie `ReflectionOracle` over de status van deze vlag wordt gegenereerd door de bewerking `TargetStateReflectionOracle` .

De reflectie `ReflectionOracle` over de invoer status naar `ancillaRegister` wordt gegenereerd door het omkeren van StateOracle en vervolgens weer spie gelen over $ \ket{0\cdots 0} $ met ReflectionStart ().

Het Oracle van `DeterministicStateOracle` het type reageert op de `qubitState` kassa's om de doel status precies zonder vlag te maken.

`AmpAmpObliviousByOraclePhases` is een versie van de Oblivious-amplitude versterking waarmee Oracle `StateOracle` en `ObliviousOracle` in plaats van reflecties worden geaccepteerd.

Houd er rekening mee dat de versterking van de amplitude een speciaal geval is voor een obliviouse amplitude versterking waarbij `ObliviousOracle` de identiteits operator is en er geen systeem-qubits `systemRegister` is.

Dit wordt aangeroepen door de bewerking `AmpAmByReflectionPhases` en `AmpAmpByOraclePhases` .

De fasen voor gedeeltelijke reflecties in het standaard geval van een Grover-zoek opdracht worden gegeven door de functie AmpAmpPhasesStandard.

We hebben bijvoorbeeld de volgende afhankelijkheden: AmpAmpByOracle-> AmpAmpByOraclePhases-> AmpAmpObliviousByOraclePhases-> AmpAmpObliviousByReflectionPhases.