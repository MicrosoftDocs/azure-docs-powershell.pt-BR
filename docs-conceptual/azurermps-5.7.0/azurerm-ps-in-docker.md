---
title: Executar o Azure PowerShell em um contêiner do Docker
description: Como executar o Azure PowerShell em um contêiner do Docker.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/20/2018
ms.openlocfilehash: b224beb95809d0e48c6f1dd5985de45b3b4df816
ms.sourcegitcommit: 4c775721461210431bd913f28d1f1e6f1976880a
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/28/2018
ms.locfileid: "37091565"
---
## <a name="run-azure-powershell-in-a-docker-container"></a><span data-ttu-id="bb28d-103">Executar o Azure PowerShell em um contêiner do Docker</span><span class="sxs-lookup"><span data-stu-id="bb28d-103">Run Azure PowerShell in a Docker container</span></span>

<span data-ttu-id="bb28d-104">Há um conjunto de imagens do Docker pré-configuradas com o Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="bb28d-104">There are a set of Docker images preconfigured with Azure PowerShell.</span></span> <span data-ttu-id="bb28d-105">Há dois tipos de contêineres disponíveis: os que estão executando o PowerShell tradicional no Windows, e um contêiner executando o PowerShell Core no Windows ou no Linux.</span><span class="sxs-lookup"><span data-stu-id="bb28d-105">Two types of containers are available: Those running traditional PowerShell on Windows, and a container running PowerShell Core on either Windows or Linux.</span></span>

| <span data-ttu-id="bb28d-106">Ambiente</span><span class="sxs-lookup"><span data-stu-id="bb28d-106">Environment</span></span> | <span data-ttu-id="bb28d-107">Imagem do Docker</span><span class="sxs-lookup"><span data-stu-id="bb28d-107">Docker image</span></span> |
|-------------|--------------|
| <span data-ttu-id="bb28d-108">PowerShell no Windows</span><span class="sxs-lookup"><span data-stu-id="bb28d-108">PowerShell on Windows</span></span> | [<span data-ttu-id="bb28d-109">azuresdk/azure-powershell</span><span class="sxs-lookup"><span data-stu-id="bb28d-109">azuresdk/azure-powershell</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell/) |
| <span data-ttu-id="bb28d-110">PowerShell Core no Windows</span><span class="sxs-lookup"><span data-stu-id="bb28d-110">PowerShell Core on Windows</span></span> | [<span data-ttu-id="bb28d-111">azuresdk/azure-powershell-core:nanoserver</span><span class="sxs-lookup"><span data-stu-id="bb28d-111">azuresdk/azure-powershell-core:nanoserver</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |
| <span data-ttu-id="bb28d-112">PowerShell Core no Linux</span><span class="sxs-lookup"><span data-stu-id="bb28d-112">PowerShell Core on Linux</span></span> | [<span data-ttu-id="bb28d-113">azuresdk/azure-powershell-core:latest</span><span class="sxs-lookup"><span data-stu-id="bb28d-113">azuresdk/azure-powershell-core:latest</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |

<span data-ttu-id="bb28d-114">Para executar qualquer um desses contêineres, você deve usar `docker run -it $ImageName` para obter um terminal interativo.</span><span class="sxs-lookup"><span data-stu-id="bb28d-114">To run any of these containers, you use `docker run -it $ImageName` to get an interactive terminal.</span></span> <span data-ttu-id="bb28d-115">Por exemplo, para executar o PowerShell Core no contêiner do Linux, use:</span><span class="sxs-lookup"><span data-stu-id="bb28d-115">For example, to run the PowerShell Core on Linux container, use:</span></span>

```powershell
docker run -it azuresdk/azure-powershell-core:latest
```

> [!NOTE]
> <span data-ttu-id="bb28d-116">Para executar um contêiner do Windows no Docker, o sistema operacional do host deve ser Windows e o Docker deve ser definido para executar contêineres do Windows.</span><span class="sxs-lookup"><span data-stu-id="bb28d-116">To run a Windows container in Docker, your host OS must be Windows and Docker must be set to run Windows containers.</span></span> <span data-ttu-id="bb28d-117">Para obter informações sobre como alternar entre ambientes Windows e Linux no Docker, confira a documentação do Docker [Alternar entre contêineres do Windows e do Linux](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers).</span><span class="sxs-lookup"><span data-stu-id="bb28d-117">To learn about switching between Windows and Linux environments in Docker, see the Docker documentation [Switch between Windows and Linux containers](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers).</span></span>

## <a name="use-a-powershell-core-container"></a><span data-ttu-id="bb28d-118">Usar um contêiner do PowerShell Core</span><span class="sxs-lookup"><span data-stu-id="bb28d-118">Use a PowerShell Core container</span></span>

<span data-ttu-id="bb28d-119">Os contêineres do PowerShell Core vêm com o PowerShell Core v6 e o módulo `AzureRM.NetCore` pré-instalados.</span><span class="sxs-lookup"><span data-stu-id="bb28d-119">The PowerShell Core containers come with PowerShell Core v6 and the `AzureRM.NetCore` module pre-installed.</span></span> <span data-ttu-id="bb28d-120">Execute o cmdlet [Import-Module](/powershell/module/microsoft.powershell.core/import-module) e, em seguida, entre com sua conta do Azure:</span><span class="sxs-lookup"><span data-stu-id="bb28d-120">Run the [Import-Module](/powershell/module/microsoft.powershell.core/import-module) cmdlet and then sign in with your Azure account:</span></span>

```powershell
Import-Module AzureRM.NetCore
Connect-AzureRmAccount
```

## <a name="use-the-windows-container-with-powershell"></a><span data-ttu-id="bb28d-121">Usar o contêiner do Windows com o PowerShell</span><span class="sxs-lookup"><span data-stu-id="bb28d-121">Use the Windows container with PowerShell</span></span>

<span data-ttu-id="bb28d-122">O contêiner do Windows tem o módulo `AzureRM` pré-instalado.</span><span class="sxs-lookup"><span data-stu-id="bb28d-122">The Windows container has the `AzureRM` module pre-installed.</span></span> <span data-ttu-id="bb28d-123">Execute o cmdlet [Import-Module](/powershell/module/microsoft.powershell.core/import-module) e, em seguida, entre com sua conta do Azure:</span><span class="sxs-lookup"><span data-stu-id="bb28d-123">Run the [Import-Module](/powershell/module/microsoft.powershell.core/import-module) cmdlet and then sign in with your Azure account:</span></span>

```powershell
Import-Module AzureRM
Connect-AzureRmAccount
```