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
ms.sourcegitcommit: a749eb729f583c9d0dd86141bbd04984d77ae9ab
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/11/2018
ms.locfileid: "48882037"
---
# <a name="run-azure-powershell-in-a-docker-container"></a><span data-ttu-id="7ddae-103">Executar o Azure PowerShell em um contêiner do Docker</span><span class="sxs-lookup"><span data-stu-id="7ddae-103">Run Azure PowerShell in a Docker container</span></span>

<span data-ttu-id="7ddae-104">A Microsoft publica as imagens do Docker com o Azure PowerShell pré-instalado.</span><span class="sxs-lookup"><span data-stu-id="7ddae-104">Microsoft publishes Docker images with Azure PowerShell pre-installed.</span></span> <span data-ttu-id="7ddae-105">Essas imagens permitem experimentar o Azure PowerShell ou executá-lo em um ambiente isolado.</span><span class="sxs-lookup"><span data-stu-id="7ddae-105">These images allow for experimenting with Azure PowerShell or running it in an isolated environment.</span></span> <span data-ttu-id="7ddae-106">Existem imagens em execução no PowerShell Core e no PowerShell 5.</span><span class="sxs-lookup"><span data-stu-id="7ddae-106">There are images running both PowerShell Core and PowerShell 5.</span></span> 

| <span data-ttu-id="7ddae-107">Ambiente</span><span class="sxs-lookup"><span data-stu-id="7ddae-107">Environment</span></span> | <span data-ttu-id="7ddae-108">Imagem do Docker</span><span class="sxs-lookup"><span data-stu-id="7ddae-108">Docker image</span></span> |
|-------------|--------------|
| <span data-ttu-id="7ddae-109">PowerShell no Windows</span><span class="sxs-lookup"><span data-stu-id="7ddae-109">PowerShell on Windows</span></span> | [<span data-ttu-id="7ddae-110">azuresdk/azure-powershell</span><span class="sxs-lookup"><span data-stu-id="7ddae-110">azuresdk/azure-powershell</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell/) |
| <span data-ttu-id="7ddae-111">PowerShell Core no Windows</span><span class="sxs-lookup"><span data-stu-id="7ddae-111">PowerShell Core on Windows</span></span> | [<span data-ttu-id="7ddae-112">azuresdk/azure-powershell-core:nanoserver</span><span class="sxs-lookup"><span data-stu-id="7ddae-112">azuresdk/azure-powershell-core:nanoserver</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |
| <span data-ttu-id="7ddae-113">PowerShell Core no Linux</span><span class="sxs-lookup"><span data-stu-id="7ddae-113">PowerShell Core on Linux</span></span> | [<span data-ttu-id="7ddae-114">azuresdk/azure-powershell-core:latest</span><span class="sxs-lookup"><span data-stu-id="7ddae-114">azuresdk/azure-powershell-core:latest</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |

<span data-ttu-id="7ddae-115">Para executar qualquer um desses contêineres, use `docker run -it $ImageName` para obter um terminal interativo.</span><span class="sxs-lookup"><span data-stu-id="7ddae-115">To run any of these containers, use `docker run -it $ImageName` to get an interactive terminal.</span></span> <span data-ttu-id="7ddae-116">Por exemplo, para executar um contêiner do Linux com o PowerShell Core:</span><span class="sxs-lookup"><span data-stu-id="7ddae-116">For example, to run a Linux container with PowerShell Core:</span></span>

```powershell
docker run -it azuresdk/azure-powershell-core:latest
```

> [!NOTE]
> <span data-ttu-id="7ddae-117">Para executar um contêiner do Windows no Docker, o sistema operacional do host deve ser Windows e o Docker deve ser definido para executar contêineres do Windows.</span><span class="sxs-lookup"><span data-stu-id="7ddae-117">To run a Windows container in Docker, your host OS must be Windows and Docker must be set to run Windows containers.</span></span> <span data-ttu-id="7ddae-118">Para obter informações sobre como alternar entre ambientes Windows e Linux no Docker, confira a documentação do Docker [Alternar entre contêineres do Windows e do Linux](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers).</span><span class="sxs-lookup"><span data-stu-id="7ddae-118">To learn about switching between Windows and Linux environments in Docker, see the Docker documentation [Switch between Windows and Linux containers](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers).</span></span>

## <a name="use-a-powershell-core-container"></a><span data-ttu-id="7ddae-119">Usar um contêiner do PowerShell Core</span><span class="sxs-lookup"><span data-stu-id="7ddae-119">Use a PowerShell Core container</span></span>

<span data-ttu-id="7ddae-120">Os contêineres do PowerShell Core vêm com o PowerShell Core v6 e o módulo `AzureRM.NetCore` pré-instalados.</span><span class="sxs-lookup"><span data-stu-id="7ddae-120">The PowerShell Core containers come with PowerShell Core v6 and the `AzureRM.NetCore` module pre-installed.</span></span> <span data-ttu-id="7ddae-121">Execute o cmdlet [Import-Module](/powershell/module/microsoft.powershell.core/import-module), em seguida, entre com sua conta do Azure:</span><span class="sxs-lookup"><span data-stu-id="7ddae-121">Run the [Import-Module](/powershell/module/microsoft.powershell.core/import-module) cmdlet and then sign in with your Azure account:</span></span>

```powershell
Import-Module AzureRM.NetCore
Connect-AzureRmAccount
```

## <a name="use-the-windows-container-with-powershell"></a><span data-ttu-id="7ddae-122">Usar o contêiner do Windows com o PowerShell</span><span class="sxs-lookup"><span data-stu-id="7ddae-122">Use the Windows container with PowerShell</span></span>

<span data-ttu-id="7ddae-123">O contêiner do Windows tem o módulo `AzureRM` pré-instalado.</span><span class="sxs-lookup"><span data-stu-id="7ddae-123">The Windows container has the `AzureRM` module pre-installed.</span></span> <span data-ttu-id="7ddae-124">Execute o cmdlet [Import-Module](/powershell/module/microsoft.powershell.core/import-module), em seguida, entre com sua conta do Azure:</span><span class="sxs-lookup"><span data-stu-id="7ddae-124">Run the [Import-Module](/powershell/module/microsoft.powershell.core/import-module) cmdlet and then sign in with your Azure account:</span></span>

```powershell
Import-Module AzureRM
Connect-AzureRmAccount
```
