---
title: Como usar o Azure PowerShell no Docker
description: Como usar o Azure PowerShell que é pré-instalado em uma imagem do Docker.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/20/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 48935f15241ec965adf4c34d2c17aa670110585a
ms.sourcegitcommit: 2036538797dd088728aee5ac5021472454d82eb2
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2020
ms.locfileid: "93410444"
---
# <a name="using-azure-powershell-in-docker"></a><span data-ttu-id="b22b7-103">Como usar o Azure PowerShell no Docker</span><span class="sxs-lookup"><span data-stu-id="b22b7-103">Using Azure PowerShell in Docker</span></span>

<span data-ttu-id="b22b7-104">Estamos publicando imagens do Docker com o Azure PowerShell pré-instalado.</span><span class="sxs-lookup"><span data-stu-id="b22b7-104">We are publishing Docker images with Azure PowerShell preinstalled.</span></span> <span data-ttu-id="b22b7-105">Este artigo mostra como começar a usar o Azure PowerShell no contêiner do Docker.</span><span class="sxs-lookup"><span data-stu-id="b22b7-105">This article shows you how to get started using Azure PowerShell in the Docker container.</span></span>

## <a name="finding-available-images"></a><span data-ttu-id="b22b7-106">Localizar imagens disponíveis</span><span class="sxs-lookup"><span data-stu-id="b22b7-106">Finding available images</span></span>

<span data-ttu-id="b22b7-107">As imagens liberadas exigem o Docker 17.05 ou mais recente.</span><span class="sxs-lookup"><span data-stu-id="b22b7-107">The released images require Docker 17.05 or newer.</span></span> <span data-ttu-id="b22b7-108">Também é esperado que você possa executar o Docker sem `sudo` ou direitos administrativos locais.</span><span class="sxs-lookup"><span data-stu-id="b22b7-108">It is also expected that you are able to run Docker without `sudo` or local administrative rights.</span></span> <span data-ttu-id="b22b7-109">Siga as [instruções][install] oficiais do Docker para instalar o `docker` corretamente.</span><span class="sxs-lookup"><span data-stu-id="b22b7-109">Please follow Docker's official [instructions][install] to install `docker` correctly.</span></span>

<span data-ttu-id="b22b7-110">A imagem de contêiner mais recente contém a versão mais recente do PowerShell e os módulos do Azure PowerShell mais recentes compatíveis com o módulo Az.</span><span class="sxs-lookup"><span data-stu-id="b22b7-110">The latest container image contains the latest version of PowerShell and the latest Azure PowerShell modules supported with the Az module.</span></span>

<span data-ttu-id="b22b7-111">Para cada nova versão do módulo Az, estamos lançando uma imagem para os seguintes sistemas operacionais:</span><span class="sxs-lookup"><span data-stu-id="b22b7-111">For each new release of the Az module we are releasing an image for the following operating systems:</span></span>

- <span data-ttu-id="b22b7-112">Ubuntu 18.04 (padrão)</span><span class="sxs-lookup"><span data-stu-id="b22b7-112">Ubuntu 18.04 (default)</span></span>
- <span data-ttu-id="b22b7-113">Debian 9</span><span class="sxs-lookup"><span data-stu-id="b22b7-113">Debian 9</span></span>
- <span data-ttu-id="b22b7-114">CentOs 7</span><span class="sxs-lookup"><span data-stu-id="b22b7-114">CentOs 7</span></span>

<span data-ttu-id="b22b7-115">Uma lista completa de imagens disponíveis pode ser encontrada em nossa página de [imagem do Docker][az image].</span><span class="sxs-lookup"><span data-stu-id="b22b7-115">A full list of available images can be found on our [Docker image][az image] page.</span></span>

## <a name="using-azure-powershell-in-a-container"></a><span data-ttu-id="b22b7-116">Usar o Azure PowerShell em um contêiner</span><span class="sxs-lookup"><span data-stu-id="b22b7-116">Using Azure PowerShell in a container</span></span>

<span data-ttu-id="b22b7-117">As etapas a seguir mostram os comandos do Docker necessários para baixar a imagem e iniciar uma sessão interativa do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b22b7-117">The following steps show the Docker commands required to download the image and start an interactive PowerShell session.</span></span>

1. <span data-ttu-id="b22b7-118">Baixe a imagem do azure-powershell mais recente.</span><span class="sxs-lookup"><span data-stu-id="b22b7-118">Download the latest azure-powershell image.</span></span>

   ```console
   docker pull mcr.microsoft.com/azure-powershell
   ```

1. <span data-ttu-id="b22b7-119">Execute o contêiner do azure-powershell no modo interativo:</span><span class="sxs-lookup"><span data-stu-id="b22b7-119">Run the azure-powershell container in interactive mode:</span></span>

   ```console
   docker run -it mcr.microsoft.com/azure-powershell pwsh
   ```

<span data-ttu-id="b22b7-120">Para hosts do Windows Docker, é preciso habilitar o compartilhamento de arquivos do Docker para permitir que unidades locais no Windows sejam compartilhadas com contêineres do Linux.</span><span class="sxs-lookup"><span data-stu-id="b22b7-120">For Windows Docker hosts, you must enable Docker File Sharing to allow local drives on Windows to be shared with Linux containers.</span></span> <span data-ttu-id="b22b7-121">Para saber mais, confira [Introdução ao Docker for Windows][file-sharing].</span><span class="sxs-lookup"><span data-stu-id="b22b7-121">For more information see [Get started with Docker for Windows][file-sharing].</span></span>

### <a name="run-the-azure-powershell-container-interactively-using-host-authentication"></a><span data-ttu-id="b22b7-122">Executar o contêiner do azure-powershell interativamente usando a autenticação de host</span><span class="sxs-lookup"><span data-stu-id="b22b7-122">Run the azure-powershell container interactively using host authentication</span></span>

<span data-ttu-id="b22b7-123">Se já tiver o Azure PowerShell instalado no sistema que hospeda o Docker, você poderá ter credenciais do Azure em cache.</span><span class="sxs-lookup"><span data-stu-id="b22b7-123">If you have Azure PowerShell already installed on the system hosting Docker, you may have cached Azure credentials.</span></span> <span data-ttu-id="b22b7-124">Essas credenciais podem ser usadas na sessão do PowerShell em execução no contêiner do Docker.</span><span class="sxs-lookup"><span data-stu-id="b22b7-124">These credentials can be used in the PowerShell session running in the Docker container.</span></span>

<span data-ttu-id="b22b7-125">Por padrão, as credenciais armazenadas em cache ficam no diretório `$HOME/.Azure` no host.</span><span class="sxs-lookup"><span data-stu-id="b22b7-125">By default, the cached credentials are in `$HOME/.Azure` directory on your host.</span></span> <span data-ttu-id="b22b7-126">O serviço do Docker deve ter acesso a esse local para acessar as credenciais.</span><span class="sxs-lookup"><span data-stu-id="b22b7-126">The Docker service must have access to this location to access the credentials.</span></span> <span data-ttu-id="b22b7-127">O comando a seguir inicia o contêiner com o cache de credenciais montado e inicia uma sessão interativa do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b22b7-127">The following command starts the container with the credential cache mounted and starts an interactive PowerShell session.</span></span>

```console
docker run -it -v ~/.Azure/AzureRmContext.json:/root/.Azure/AzureRmContext.json -v ~/.Azure/TokenCache.dat:/root/.Azure/TokenCache.dat mcr.microsoft.com/azure-powershell pwsh
```

### <a name="remove-the-image-when-no-longer-needed"></a><span data-ttu-id="b22b7-128">Remover a imagem quando não for mais necessária</span><span class="sxs-lookup"><span data-stu-id="b22b7-128">Remove the image when no longer needed</span></span>

<span data-ttu-id="b22b7-129">O comando a seguir é usado para excluir o contêiner do Docker quando você não precisar mais dele.</span><span class="sxs-lookup"><span data-stu-id="b22b7-129">The following command is used to delete the Docker container when you no longer need it.</span></span>

```console
docker rmi mcr.microsoft.com/azure-powershell
```

## <a name="next-steps"></a><span data-ttu-id="b22b7-130">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="b22b7-130">Next steps</span></span>

<span data-ttu-id="b22b7-131">Para saber mais sobre os módulos do Azure PowerShell e seus recursos, confira [Introdução ao Azure PowerShell](get-started-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="b22b7-131">To learn more about the Azure PowerShell modules and their features, see [Get Started with Azure PowerShell](get-started-azureps.md).</span></span>

<!-- link references -->
[install]: https://docs.docker.com/engine/installation/
[powershell image]: https://hub.docker.com/_/microsoft-powershell
[az image]: https://hub.docker.com/_/microsoft-azure-powershell
[file-sharing]: https://docs.docker.com/docker-for-windows/#file-sharing
