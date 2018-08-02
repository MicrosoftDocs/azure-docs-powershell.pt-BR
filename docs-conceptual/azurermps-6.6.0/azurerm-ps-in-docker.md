---
title: Executar o Azure PowerShell em um contêiner do Docker
description: Como executar o Azure PowerShell em um contêiner do Docker.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/20/2018
ms.openlocfilehash: 656c58fbb7cafb539736a0083d6aed1f46b7b98d
ms.sourcegitcommit: fd11600079ee3844986552bccc4e274a231332b6
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/02/2018
ms.locfileid: "39367898"
---
# <a name="run-azure-powershell-in-a-docker-container"></a>Executar o Azure PowerShell em um contêiner do Docker

Há um conjunto de imagens do Docker pré-configuradas com o Azure PowerShell. Há dois tipos de contêineres disponíveis: os que executam o PowerShell tradicional no Windows e um contêiner que executa o PowerShell Core no Windows ou no Linux.

| Ambiente | Imagem do Docker |
|-------------|--------------|
| PowerShell no Windows | [azuresdk/azure-powershell](https://hub.docker.com/r/azuresdk/azure-powershell/) |
| PowerShell Core no Windows | [azuresdk/azure-powershell-core:nanoserver](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |
| PowerShell Core no Linux | [azuresdk/azure-powershell-core:latest](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |

Para executar qualquer um desses contêineres, você deve usar `docker run -it $ImageName` para obter um terminal interativo. Por exemplo, para executar o PowerShell Core no contêiner do Linux, use:

```powershell
docker run -it azuresdk/azure-powershell-core:latest
```

> [!NOTE]
> Para executar um contêiner do Windows no Docker, o sistema operacional do host deve ser Windows e o Docker deve ser definido para executar contêineres do Windows. Para obter informações sobre como alternar entre ambientes Windows e Linux no Docker, confira a documentação do Docker [Alternar entre contêineres do Windows e do Linux](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers).

## <a name="use-a-powershell-core-container"></a>Usar um contêiner do PowerShell Core

Os contêineres do PowerShell Core vêm com o PowerShell Core v6 e o módulo `AzureRM.NetCore` pré-instalados. Execute o cmdlet [Import-Module](/powershell/module/microsoft.powershell.core/import-module), em seguida, entre com sua conta do Azure:

```powershell
Import-Module AzureRM.NetCore
Connect-AzureRmAccount
```

## <a name="use-the-windows-container-with-powershell"></a>Usar o contêiner do Windows com o PowerShell

O contêiner do Windows tem o módulo `AzureRM` pré-instalado. Execute o cmdlet [Import-Module](/powershell/module/microsoft.powershell.core/import-module), em seguida, entre com sua conta do Azure:

```powershell
Import-Module AzureRM
Connect-AzureRmAccount
```