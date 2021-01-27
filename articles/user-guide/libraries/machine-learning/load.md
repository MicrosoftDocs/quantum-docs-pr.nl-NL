---
title: Klassieke gegevens laden
description: Meer informatie over het laden van uw eigen gegevensset voor het trainen van een classificatie model met de Microsoft Quantum Development Kit (QDK).
author: geduardo
ms.author: v-edsanc
ms.date: 02/16/2020
ms.topic: conceptual
uid: microsoft.quantum.libraries.machine-learning.load
no-loc:
- Q#
- $$v
ms.openlocfilehash: 7ebfe085e50d4647fdb1027250cf3134f8d8f8c2
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98856461"
---
# <a name="load-and-classify-your-own-datasets"></a>Uw eigen gegevens sets laden en classificeren

In deze korte zelf studie leert u hoe u uw eigen gegevensset kunt laden om een classificatie model te trainen met de Quantum Development Kit (QDK).

Het is raadzaam om een gestandaardiseerde serialisatie-indeling te gebruiken, zoals [json-bestanden](https://en.wikipedia.org/wiki/JSON) , om uw gegevens op te slaan.
Dergelijke indelingen bieden hoge compatibiliteit met verschillende frameworks zoals python en het .NET-ecosysteem.
We raden u met name aan om onze sjabloon te gebruiken voor het laden van de gegevens, zodat u de code rechtstreeks vanuit de voor beelden kunt plakken.

## <a name="template-for-loading-your-datasets"></a>Sjabloon voor het laden van uw gegevens sets

Stel dat we een training-gegevensset $ (x, y) $ van grootte $N = $2 waarbij elk exemplaar $x _i $ van $x $ drie functies heeft: $x _ {I1} $, $x _ {I2} $ en $x _ {i3} $.
De validatie gegevensset heeft dezelfde structuur.
Deze datsets kunnen worden aangeduid met een `data.json` bestand dat vergelijkbaar is met het volgende:

```json
{
    "TrainingData": {
        "Features": [
            [
                x_11,
                x_12,
                x_13
            ],
            [
                x_21,
                x_22,
                x_23
            ]
        ],
        "Labels": [
            y_1,
            y_2
        ]
    },
    "ValidationData": {
        "Features": [
            [
                xv_11,
                xv_12,
                xv_13
            ],
            [
                xv_11,
                xv_12,
                xv_13
            ]
        ],
        "Labels": [
            yv_1,
            yv_2
        ]
    }
}
```

### <a name="example-using-the-template"></a>Voor beeld met behulp van de sjabloon

Stel dat er een kleine gegevensset is met de hoogten en het gewicht van verschillende katten en honden. Deze gegevensset is zeer klein om een model te trainen, maar is voldoende om het proces van het laden van een gegevensset weer te geven.

| Hoogte (m) | Gewicht (kg) | Voeding |
|-----------|------------|--------|
| 0,54      | 30         | Honden    |
| 0,30      | 8          | Kat    |
| 0,91      | 44         | Honden    |
| 0,86      | 31          | Honden    |
| 0,32      | 5         | Kat    |
| 0,25      | 4          | Kat    |

Het proces is:

- Eerst moet u de gegevensset scheiden in training en validatie. In dit geval kunnen we alleen de eerste drie voor beelden voor de training en de rest van voor beelden voor validatie nemen. Over het algemeen is het een goed idee om wille keurig de training en validatie gegevensset te samplen om ongewenste BIASS in de trainings gegevens te voor komen.
- Ten tweede moeten we een numeriek label toewijzen aan elke klasse. Houd er rekening mee dat de QML-bibliotheek alleen tijdelijke classificatie problemen heeft. Daarom zullen we het label 0 toewijzen aan de klasse `Dog` en het nummer 1 aan de klasse `Cat` .
- Ten slotte vullen we de sjabloon in met behulp van de gegevens uit de gegevensset. Houd er rekening mee dat voor Big gegevens sets een klein script moet worden gemaakt om de sjabloon automatisch te genereren op basis van uw specifieke gegevensset. Dit script is afhankelijk van de oorspronkelijke indeling van uw gegevensset.

Voor onze gegevensset `data.json` is het bestand:

```json
{
    "TrainingData": {
        "Features": [
            [
                0.54,
                30
            ],
            [
                0.30,
                8
            ],
            [
                0.91,
                44
            ]
        ],
        "Labels": [
            0,
            1,
            0
        ]
    },
    "ValidationData": {
        "Features": [
            [
                0.86,
                31
            ],
            [
                0.32,
                5
            ]
            [
                0.25,
                4
            ]
        ],
        "Labels": [
            0,
            1,
            1
        ]
    }
}

```

## <a name="loading-the-data"></a>De gegevens laden

Zodra u uw gegevens hebt geserialiseerd als een JSON-bestand, kunt u deze laden met behulp van JSON-bibliotheken die zijn opgenomen in de door u gewenste taal.

### <a name="python"></a>[Python](#tab/tabid-python)

Python biedt het [ingebouwde `json` pakket](https://docs.python.org/3.7/library/json.html) voor het werken met JSON-geserialiseerde gegevens:

:::code language="python" source="~/quantum/samples/machine-learning/half-moons/host.py" range="4-5,20-22":::

### <a name="c"></a>[C#](#tab/tabid-csharp)

Het .NET Core-platform biedt het [ `System.Text.Json` pakket](https://www.nuget.org/packages/System.Text.Json) voor het werken met JSON-geserialiseerde gegevens:

:::code language="csharp" source="~/quantum/samples/machine-learning/half-moons/Host.cs" range="10,64-82":::

***

## <a name="next-steps"></a>Volgende stappen

Nu bent u klaar om uw eigen experimenten uit te voeren met uw eigen gegevens sets. Probeer verschillende classificaties en gegevensset uit en draagt bij aan de community om uw resultaten te delen.
