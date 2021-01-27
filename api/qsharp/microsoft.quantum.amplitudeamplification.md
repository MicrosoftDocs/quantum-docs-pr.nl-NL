---
uid: Microsoft.Quantum.AmplitudeAmplification
title: Micro soft. Quantum. AmplitudeAmplification-naam ruimte
ms.date: 1/23/2021 12:00:00 AM
ms.topic: managed-reference
qsharp.kind: namespace
qsharp.name: Microsoft.Quantum.AmplitudeAmplification
qsharp.summary: This namespace contains functions and operations for performing amplitude amplification.
ms.openlocfilehash: a014f923de62c5e660c1c0fc839fbe60e80f8ba9
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845834"
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