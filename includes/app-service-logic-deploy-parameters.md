---
author: cephalin
ms.service: app-service
ms.topic: include
ms.date: 11/03/2016
ms.author: cephalin
ms.openlocfilehash: f188f2c7bea511f1109d37ef49563e0f745a770e
ms.sourcegitcommit: 9d7391e11d69af521a112ca886488caff5808ad6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2018
ms.locfileid: "50133245"
---
Con Azure Resource Manager, puede definir los parámetros de los valores que se usan al implementar la plantilla. La plantilla incluye una sección `parameters` que contiene todos los valores de los parámetros. La plantilla usa cada uno de estos valores de los parámetros para definir los recursos que se desea implementar.

> [!NOTE]
> No defina parámetros para valores que siempre permanezcan igual. Defina parámetros solo para los valores que varíen, en función del proyecto que vaya a implementar o del entorno en el que vaya a realizar la implementación.

Cuando defina los parámetros:

* Para especificar los valores que un usuario puede proporcionar durante la implementación, use el campo **allowedValues**.

* Para asignar los valores predeterminados a un parámetro cuando no se proporcionan valores durante la implementación, use el campo **defaultValue**. 
