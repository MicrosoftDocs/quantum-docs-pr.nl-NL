---
title: Voor beelden die bijdragen aan de micro soft-QDK
description: Meer informatie over hoe u voorbeeld code bijdraagt aan de Microsoft Quantum Development Kit (QDK).
author: cgranade
ms.author: chgranad
ms.date: 10/12/2018
ms.topic: article
uid: microsoft.quantum.contributing.samples
ms.openlocfilehash: 3bd0de04a448c74eea6c3e8e3a15dcbb19f9d705
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/23/2020
ms.locfileid: "85274513"
---
# <a name="contributing-samples-to-the-quantum-development-kit"></a>Voor beelden die bijdragen aan de Quantum Development Kit

Als u geïnteresseerd bent in het verzenden van code naar de [opslag plaats voor beelden](https://github.com/Microsoft/Quantum), hartelijk dank dat u de Quantum Development Community een betere plaats wilt maken.

## <a name="the-quantum-development-kit-samples-repository"></a>De voor beelden van de Quantum Development Kit-opslag plaats

Om u te helpen uw bijdrage voor te bereiden om zo veel mogelijk te helpen, is het handig om snel te kijken hoe de voor beelden van de opslag plaats worden opgesteld:

```plaintext
microsoft/Quantum
📁 samples/
  📁 algorithms/
    📁 chsh-game/
      📝 CHSHGame.csproj
      📝 Game.qs
      📝 Host.cs
      📝 host.py
      📝 README.md
     ⋮
  📁 arithmetic/
  📁 characterization/
  📁 chemistry/
   ⋮
```

Dat wil zeggen dat de voor beelden in de [micro soft/Quantum-opslag plaats](https://github.com/microsoft/Quantum) worden onderverdeeld op onderwerpgebied in andere mappen, zoals `algorithms/` , `arithmetic/` of `characterization/` .
In de map voor elk onderwerp, bestaat elk voor beeld uit één map waarin alles wordt verzameld voor een gebruiker die het voor beeld moet verkennen en gebruiken.

## <a name="how-samples-are-structured"></a>Hoe steek proeven worden gestructureerd

Wanneer u de bestanden waaruit elke map bestaat, bekijkt, gaan we naar het voor [`algorithms/chsh-game/`](https://github.com/microsoft/Quantum/tree/master/samples/algorithms/chsh-game) beeld.

| File              | Description                                                |
|-------------------|------------------------------------------------------------|
| `CHSHGame.csproj` | Q #-project gebruikt om het voor beeld samen te stellen met de .NET Core SDK |
| `Game.qs`         | Q # bewerkingen en functies voor het voor beeld                 |
| `Host.cs`         | C#-hostprogramma waarmee het voor beeld wordt uitgevoerd                     |
| `host.py`         | Python-hostcluster dat wordt gebruikt om het voor beeld uit te voeren                 |
| `README.md`       | Documentatie over wat het voor beeld doet en hoe u het kunt gebruiken    |

Niet alle voor beelden hebben precies dezelfde set bestanden (bijvoorbeeld: sommige voor beelden kunnen alleen C# zijn, andere hebben mogelijk geen python-host, of voor sommige voor beelden zijn mogelijk auxillary-gegevens bestanden nodig).

## <a name="anatomy-of-a-helpful-readme-file"></a>Anatomie van een handig Leesmij-bestand

Een bijzonder belang rijk bestand is het bestand, maar het is `README.md` wat gebruikers nodig hebben om aan de slag te gaan met uw voor beeld.

Elk `README.md` van deze moet beginnen met een aantal meta gegevens waarmee docs.Microsoft.com/samples uw bijdrage kunt vinden.

> [!div class="nextstepaction"]
> [Bekijk hoe het chsh-game-voor beeld wordt weer gegeven](https://docs.microsoft.com/samples/microsoft/quantum/validating-quantum-mechanics/)

Deze meta gegevens worden weer gegeven als een [yaml-header](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html#yaml-header) die aangeeft in welke talen uw steek proef betrekking heeft (doorgaans is dit `qsharp` , `csharp` en `python` ) en op welke producten uw voor beeld betrekking heeft (doorgaans gewoon `qdk` ).

:::code language="markdown" source="~/quantum/samples/algorithms/chsh-game/README.md" range="1-11":::

> [!IMPORTANT]
> De `page_type: sample` sleutel in de header is vereist om uw steek proef weer te geven op docs.Microsoft.com/samples.
> Op dezelfde manier `product` zijn de en- `language` sleutels essentieel om gebruikers te helpen bij het zoeken en uitvoeren van uw voor beeld.

Daarna is het handig om een korte inleiding te geven die aangeeft wat het nieuwe voor beeld doet:

:::code language="markdown" source="~/quantum/samples/algorithms/chsh-game/README.md" range="13-21":::

Het is ook belang rijk dat gebruikers van uw voor beeld weten wat ze nodig hebben om het uit te voeren (bijvoorbeeld: gebruikers hebben alleen de Quantum Development Kit zelf nodig of hebben ze extra software, zoals node.js?):

:::code language="markdown" source="~/quantum/samples/algorithms/chsh-game/README.md" range="23-25":::

Zo kunt u gebruikers vertellen hoe uw voor beeld moet worden uitgevoerd:

:::code language="markdown" source="~/quantum/samples/algorithms/chsh-game/README.md" range="27-50":::

Ten slotte is het handig om gebruikers te vertellen wat elk bestand in uw voor beeld doet en waar ze meer informatie kunnen vinden:

:::code language="markdown" source="~/quantum/samples/algorithms/chsh-game/README.md" range="52-61":::

> [!WARNING]
> Zorg ervoor dat u absolute Url's hier gebruikt, omdat uw voor beeld wordt weer gegeven op een andere URL wanneer het wordt gerenderd op docs.microsoft.com/samples!
