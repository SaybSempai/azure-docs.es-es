---
author: cynthn
ms.service: virtual-machines-linux
ms.topic: include
ms.date: 10/26/2018
ms.author: cynthn
ms.openlocfilehash: d93de4ed758afb5e951bb5e19f4f7adb290e461c
ms.sourcegitcommit: 6e09760197a91be564ad60ffd3d6f48a241e083b
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/29/2018
ms.locfileid: "50227110"
---
En la tabla siguiente se enumeran la posibles combinaciones de carga y captura de imágenes del sistema operativo de Linux generalizadas y especializadas. Las combinaciones que se procesarán sin errores se indican mediante una letra Y y las que generarán errores se indican mediante una letra N. En la tabla siguiente, se proporcionan las causas y soluciones para los diferentes errores que se va a encontrar.

| SO | Cargar espec. | Cargar gen. | Capturar espec. | Capturar gen. |
| --- | --- | --- | --- | --- |
| Linux gen. |N<sup>1</sup> |Y |N<sup>3</sup> |Y |
| Linux espec. |Y |N<sup>2</sup> |Y |N<sup>4</sup> |

