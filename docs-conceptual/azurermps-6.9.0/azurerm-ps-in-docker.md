---
title: Executar o Azure PowerShell em um contêiner do Docker
description: Como executar o Azure PowerShell em um contêiner do Docker.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/09/2018
ms.openlocfilehash: 0ed8f50abbcb2aa00192196f19004446dc696b5d
ms.sourcegitcommit: 6c38e86e16da99f65cd183c63e34f7176b121ab8
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "47425254"
---
# <a name="run-azure-powershell-in-a-docker-container"></a>Executar o Azure PowerShell em um contêiner do Docker

A Microsoft publica as imagens do Docker com o Azure PowerShell pré-instalado. Essas imagens permitem experimentar o Azure PowerShell ou executá-lo em um ambiente isolado. Existem imagens em execução no PowerShell Core e no PowerShell 5. 

| Ambiente | Imagem do Docker |
|-------------|--------------|
| PowerShell no Windows | [azuresdk/azure-powershell](https://hub.docker.com/r/azuresdk/azure-powershell/) |
| PowerShell Core no Windows | [azuresdk/azure-powershell-core:nanoserver](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |
| PowerShell Core no Linux | [azuresdk/azure-powershell-core:latest](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |

Para executar qualquer um desses contêineres, use `docker run -it $ImageName` para obter um terminal interativo. Por exemplo, para executar um contêiner do Linux com o PowerShell Core:

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
