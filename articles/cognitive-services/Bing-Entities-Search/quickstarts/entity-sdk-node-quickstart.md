---
title: 'Inicio rápido: Envío de una solicitud de búsqueda el SDK de Bing Entity Search para Node.js'
titleSuffix: Azure Cognitive Services
description: Use este inicio rápido para buscar entidades con el SDK de Bing Entity Search para Node.js
services: cognitive-services
author: mikedodaro
manager: nitinme
ms.service: cognitive-services
ms.subservice: bing-entity-search
ms.topic: quickstart
ms.date: 02/01/2019
ms.author: v-gedod
ms.openlocfilehash: 04ec95e891b4e9333949a3a0f40dcc9df88e49e7
ms.sourcegitcommit: 90cec6cccf303ad4767a343ce00befba020a10f6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/07/2019
ms.locfileid: "55865869"
---
# <a name="quickstart-send-a-search-request-with-the-bing-entity-search-sdk-for-nodejs"></a>Inicio rápido: Envío de una solicitud de búsqueda el SDK de Bing Entity Search para Node.js

Use este inicio rápido para empezar a buscar entidades con el SDK de Bing Entity Search para Node.js. Aunque Bing Entity Search tiene una API REST compatible con la mayoría de los lenguajes de programación, el SDK proporciona una forma sencilla de integrar el servicio en sus aplicaciones. El código fuente de este ejemplo está disponible en [GitHub](https://github.com/Azure-Samples/cognitive-services-node-sdk-samples/blob/master/Samples/entitySearch.js).

## <a name="prerequisites"></a>Requisitos previos

* La última versión de [Node.js](https://nodejs.org/en/download/).

* El SDK de [Bing Entity Search SDK para Node.js](https://www.npmjs.com/package/azure-cognitiveservices-entitysearch)

Para instalar el SDK de Bing Entity Search:

1. Ejecute `npm install ms-rest-azure` en el entorno de desarrollo.
2. Ejecute `npm install azure-cognitiveservices-entitysearch` en el entorno de desarrollo.

[!INCLUDE [cognitive-services-bing-news-search-signup-requirements](../../../../includes/cognitive-services-bing-entity-search-signup-requirements.md)]


## <a name="create-and-initialize-the-application"></a>Creación e inicialización de la aplicación

1. Cree un archivo JavaScript en el editor o el IDE que prefiera y agregue los siguientes requisitos. 
    
    ```javascript
    const CognitiveServicesCredentials = require('ms-rest-azure').CognitiveServicesCredentials;
    const EntitySearchAPIClient = require('azure-cognitiveservices-entitysearch');
    ```

2. Cree una instancia de `CognitiveServicesCredentials` mediante su clave de suscripción. Luego, cree una instancia del cliente de búsqueda con ella.

    ```javascript
    let credentials = new CognitiveServicesCredentials('YOUR-ACCESS-KEY');
    let entitySearchApiClient = new EntitySearchAPIClient(credentials);
    ```

## <a name="send-a-request-and-receive-a-response"></a>Envío de una solicitud y recepción de la respuesta

2. Envíe una solicitud de búsqueda de entidades con `entitiesOperations.search()`. Después de recibir una respuesta, imprima el `queryContext`, el número de resultados devueltos y la descripción del primer resultado.
      
    ```javascript
    entitySearchApiClient.entitiesOperations.search('seahawks').then((result) => {
        console.log(result.queryContext);
        console.log(result.entities.value);
        console.log(result.entities.value[0].description);
    }).catch((err) => {
        throw err;
    });
    ```

<!-- Removing until we can replace with a sanitized version.
![Entity results](media/entity-search-sdk-node-quickstart-results.png)
-->

## <a name="next-steps"></a>Pasos siguientes

> [!div class="nextstepaction"]
> [Creación de una aplicación web de una sola página](../tutorial-bing-entities-search-single-page-app.md)

* [¿Qué es Bing Entity Search API?](../overview.md )