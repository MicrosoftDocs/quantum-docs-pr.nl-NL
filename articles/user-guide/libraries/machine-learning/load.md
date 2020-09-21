---
title: Klassieke gegevens laden
description: Meer informatie over het laden van uw eigen gegevensset voor het trainen van een classificatie model met de Microsoft Quantum Development Kit (QDK).
author: geduardo
ms.author: v-edsanc
ms.date: 02/16/2020
ms.topic: article
uid: microsoft.quantum.libraries.machine-learning.load
no-loc:
- Q#
- $$v
ms.openlocfilehash: cd6fdb6bb33a65ee02ac8c43f40df9abeff9c841
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/21/2020
ms.locfileid: "90833708"
---
# <a name="load-and-classify-your-own-datasets"></a><span data-ttu-id="3eedb-103">Uw eigen gegevens sets laden en classificeren</span><span class="sxs-lookup"><span data-stu-id="3eedb-103">Load and classify your own datasets</span></span>

<span data-ttu-id="3eedb-104">In deze korte zelf studie leert u hoe u uw eigen gegevensset kunt laden om een classificatie model te trainen met de Quantum Development Kit (QDK).</span><span class="sxs-lookup"><span data-stu-id="3eedb-104">In this short tutorial, we are going to learn how to load your own dataset to train a classifier model with the Quantum Development Kit (QDK).</span></span>

<span data-ttu-id="3eedb-105">Het is raadzaam om een gestandaardiseerde serialisatie-indeling te gebruiken, zoals [json-bestanden](https://en.wikipedia.org/wiki/JSON) , om uw gegevens op te slaan.</span><span class="sxs-lookup"><span data-stu-id="3eedb-105">We highly recommend the use of a standardized serialization format such as [JSON files](https://en.wikipedia.org/wiki/JSON) to store your data.</span></span>
<span data-ttu-id="3eedb-106">Dergelijke indelingen bieden hoge compatibiliteit met verschillende frameworks zoals python en het .NET-ecosysteem.</span><span class="sxs-lookup"><span data-stu-id="3eedb-106">Such formats offer high compatibility with different frameworks like Python and the .NET ecosystem.</span></span>
<span data-ttu-id="3eedb-107">We raden u met name aan om onze sjabloon te gebruiken voor het laden van de gegevens, zodat u de code rechtstreeks vanuit de voor beelden kunt plakken.</span><span class="sxs-lookup"><span data-stu-id="3eedb-107">In particular, we recommend using our template for loading the data, so that you can copy-paste the code directly from the samples.</span></span>

## <a name="template-for-loading-your-datasets"></a><span data-ttu-id="3eedb-108">Sjabloon voor het laden van uw gegevens sets</span><span class="sxs-lookup"><span data-stu-id="3eedb-108">Template for loading your datasets</span></span>

<span data-ttu-id="3eedb-109">Stel dat we een training-gegevensset $ (x, y) $ van grootte $N = $2 waarbij elk exemplaar $x _i $ van $x $ drie functies heeft: $x _ {I1} $, $x _ {I2} $ en $x _ {i3} $.</span><span class="sxs-lookup"><span data-stu-id="3eedb-109">Suppose we have a training dataset $(x, y)$ of size $N=2$ where each instance $x_i$ of $x$ has three features: $x_{i1}$, $x_{i2}$ and $x_{i3}$.</span></span>
<span data-ttu-id="3eedb-110">De validatie gegevensset heeft dezelfde structuur.</span><span class="sxs-lookup"><span data-stu-id="3eedb-110">The validation dataset has the same structure.</span></span>
<span data-ttu-id="3eedb-111">Deze datsets kunnen worden aangeduid met een `data.json` bestand dat vergelijkbaar is met het volgende:</span><span class="sxs-lookup"><span data-stu-id="3eedb-111">These datsets can be represented by a `data.json` file similar to the following:</span></span>

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

### <a name="example-using-the-template"></a><span data-ttu-id="3eedb-112">Voor beeld met behulp van de sjabloon</span><span class="sxs-lookup"><span data-stu-id="3eedb-112">Example using the template</span></span>

<span data-ttu-id="3eedb-113">Stel dat er een kleine gegevensset is met de hoogten en het gewicht van verschillende katten en honden.</span><span class="sxs-lookup"><span data-stu-id="3eedb-113">Suppose we have a small dataset with the heights and weights of different cats and dogs.</span></span> <span data-ttu-id="3eedb-114">Deze gegevensset is zeer klein om een model te trainen, maar is voldoende om het proces van het laden van een gegevensset weer te geven.</span><span class="sxs-lookup"><span data-stu-id="3eedb-114">This dataset is very small to train a model but will be enough to show the process of loading a dataset.</span></span>

| <span data-ttu-id="3eedb-115">Hoogte (m)</span><span class="sxs-lookup"><span data-stu-id="3eedb-115">Height (m)</span></span> | <span data-ttu-id="3eedb-116">Gewicht (kg)</span><span class="sxs-lookup"><span data-stu-id="3eedb-116">Weight (kg)</span></span> | <span data-ttu-id="3eedb-117">Voeding</span><span class="sxs-lookup"><span data-stu-id="3eedb-117">Animal</span></span> |
|-----------|------------|--------|
| <span data-ttu-id="3eedb-118">0,54</span><span class="sxs-lookup"><span data-stu-id="3eedb-118">0.54</span></span>      | <span data-ttu-id="3eedb-119">30</span><span class="sxs-lookup"><span data-stu-id="3eedb-119">30</span></span>         | <span data-ttu-id="3eedb-120">Honden</span><span class="sxs-lookup"><span data-stu-id="3eedb-120">Dog</span></span>    |
| <span data-ttu-id="3eedb-121">0,30</span><span class="sxs-lookup"><span data-stu-id="3eedb-121">0.30</span></span>      | <span data-ttu-id="3eedb-122">8</span><span class="sxs-lookup"><span data-stu-id="3eedb-122">8</span></span>          | <span data-ttu-id="3eedb-123">Cat5</span><span class="sxs-lookup"><span data-stu-id="3eedb-123">Cat</span></span>    |
| <span data-ttu-id="3eedb-124">0,91</span><span class="sxs-lookup"><span data-stu-id="3eedb-124">0.91</span></span>      | <span data-ttu-id="3eedb-125">44</span><span class="sxs-lookup"><span data-stu-id="3eedb-125">44</span></span>         | <span data-ttu-id="3eedb-126">Honden</span><span class="sxs-lookup"><span data-stu-id="3eedb-126">Dog</span></span>    |
| <span data-ttu-id="3eedb-127">0,86</span><span class="sxs-lookup"><span data-stu-id="3eedb-127">0.86</span></span>      | <span data-ttu-id="3eedb-128">31</span><span class="sxs-lookup"><span data-stu-id="3eedb-128">31</span></span>          | <span data-ttu-id="3eedb-129">Honden</span><span class="sxs-lookup"><span data-stu-id="3eedb-129">Dog</span></span>    |
| <span data-ttu-id="3eedb-130">0,32</span><span class="sxs-lookup"><span data-stu-id="3eedb-130">0.32</span></span>      | <span data-ttu-id="3eedb-131">5</span><span class="sxs-lookup"><span data-stu-id="3eedb-131">5</span></span>         | <span data-ttu-id="3eedb-132">Cat5</span><span class="sxs-lookup"><span data-stu-id="3eedb-132">Cat</span></span>    |
| <span data-ttu-id="3eedb-133">0,25</span><span class="sxs-lookup"><span data-stu-id="3eedb-133">0.25</span></span>      | <span data-ttu-id="3eedb-134">4</span><span class="sxs-lookup"><span data-stu-id="3eedb-134">4</span></span>          | <span data-ttu-id="3eedb-135">Cat5</span><span class="sxs-lookup"><span data-stu-id="3eedb-135">Cat</span></span>    |

<span data-ttu-id="3eedb-136">Het proces is:</span><span class="sxs-lookup"><span data-stu-id="3eedb-136">The process is:</span></span>

- <span data-ttu-id="3eedb-137">Eerst moet u de gegevensset scheiden in training en validatie.</span><span class="sxs-lookup"><span data-stu-id="3eedb-137">First we need to separate the dataset into training and validation.</span></span> <span data-ttu-id="3eedb-138">In dit geval kunnen we alleen de eerste drie voor beelden voor de training en de rest van voor beelden voor validatie nemen.</span><span class="sxs-lookup"><span data-stu-id="3eedb-138">In this case we can just take the first three samples for training and the rest of samples for validation.</span></span> <span data-ttu-id="3eedb-139">Over het algemeen is het een goed idee om wille keurig de training en validatie gegevensset te samplen om ongewenste BIASS in de trainings gegevens te voor komen.</span><span class="sxs-lookup"><span data-stu-id="3eedb-139">In general it is a good practice to sample randomly the training and validation dataset to avoid unwanted biases in the training data.</span></span>
- <span data-ttu-id="3eedb-140">Ten tweede moeten we een numeriek label toewijzen aan elke klasse.</span><span class="sxs-lookup"><span data-stu-id="3eedb-140">Secondly, we need to assign a numeric label to each class.</span></span> <span data-ttu-id="3eedb-141">Houd er rekening mee dat de QML-bibliotheek alleen tijdelijke classificatie problemen heeft.</span><span class="sxs-lookup"><span data-stu-id="3eedb-141">Note that, for the moment, the QML library only admits binary classification problems.</span></span> <span data-ttu-id="3eedb-142">Daarom zullen we het label 0 toewijzen aan de klasse `Dog` en het nummer 1 aan de klasse `Cat` .</span><span class="sxs-lookup"><span data-stu-id="3eedb-142">So we will assign the label 0 to the class `Dog` and the number 1 to the class `Cat`.</span></span>
- <span data-ttu-id="3eedb-143">Ten slotte vullen we de sjabloon in met behulp van de gegevens uit de gegevensset.</span><span class="sxs-lookup"><span data-stu-id="3eedb-143">Finally, we fill the template using the data from our dataset.</span></span> <span data-ttu-id="3eedb-144">Houd er rekening mee dat voor Big gegevens sets een klein script moet worden gemaakt om de sjabloon automatisch te genereren op basis van uw specifieke gegevensset.</span><span class="sxs-lookup"><span data-stu-id="3eedb-144">Note that for big datasets you should build a small script to automatically generate the template from your specific dataset.</span></span> <span data-ttu-id="3eedb-145">Dit script is afhankelijk van de oorspronkelijke indeling van uw gegevensset.</span><span class="sxs-lookup"><span data-stu-id="3eedb-145">This script will depend on the original format of your dataset.</span></span>

<span data-ttu-id="3eedb-146">Voor onze gegevensset `data.json` is het bestand:</span><span class="sxs-lookup"><span data-stu-id="3eedb-146">For our dataset the `data.json` file is:</span></span>

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

## <a name="loading-the-data"></a><span data-ttu-id="3eedb-147">De gegevens laden</span><span class="sxs-lookup"><span data-stu-id="3eedb-147">Loading the data</span></span>

<span data-ttu-id="3eedb-148">Zodra u uw gegevens hebt geserialiseerd als een JSON-bestand, kunt u deze laden met behulp van JSON-bibliotheken die zijn opgenomen in de door u gewenste taal.</span><span class="sxs-lookup"><span data-stu-id="3eedb-148">Once you have your data serialized as a JSON file, you can load it in using JSON libraries provided with your host language of choice.</span></span>

### <a name="python"></a>[<span data-ttu-id="3eedb-149">Python</span><span class="sxs-lookup"><span data-stu-id="3eedb-149">Python</span></span>](#tab/tabid-python)

<span data-ttu-id="3eedb-150">Python biedt het [ingebouwde `json` pakket](https://docs.python.org/3.7/library/json.html) voor het werken met JSON-geserialiseerde gegevens:</span><span class="sxs-lookup"><span data-stu-id="3eedb-150">Python provides the [built-in `json` package](https://docs.python.org/3.7/library/json.html) for working with JSON-serialized data:</span></span>

:::code language="python" source="~/quantum/samples/machine-learning/half-moons/host.py" range="4-5,20-22":::

### <a name="c"></a>[<span data-ttu-id="3eedb-151">C#</span><span class="sxs-lookup"><span data-stu-id="3eedb-151">C#</span></span>](#tab/tabid-csharp)

<span data-ttu-id="3eedb-152">Het .NET Core-platform biedt het [ `System.Text.Json` pakket](https://www.nuget.org/packages/System.Text.Json) voor het werken met JSON-geserialiseerde gegevens:</span><span class="sxs-lookup"><span data-stu-id="3eedb-152">The .NET Core platform provides the [`System.Text.Json` package](https://www.nuget.org/packages/System.Text.Json) for working with JSON-serialized data:</span></span>

:::code language="csharp" source="~/quantum/samples/machine-learning/half-moons/Host.cs" range="10,64-82":::

***

## <a name="next-steps"></a><span data-ttu-id="3eedb-153">Volgende stappen</span><span class="sxs-lookup"><span data-stu-id="3eedb-153">Next steps</span></span>

<span data-ttu-id="3eedb-154">Nu bent u klaar om uw eigen experimenten uit te voeren met uw eigen gegevens sets.</span><span class="sxs-lookup"><span data-stu-id="3eedb-154">Now you are ready to start running your own experiments with your own datasets.</span></span> <span data-ttu-id="3eedb-155">Probeer verschillende classificaties en gegevensset uit en draagt bij aan de community om uw resultaten te delen.</span><span class="sxs-lookup"><span data-stu-id="3eedb-155">Try different classifiers and dataset and contribute to the community sharing your results!</span></span>
