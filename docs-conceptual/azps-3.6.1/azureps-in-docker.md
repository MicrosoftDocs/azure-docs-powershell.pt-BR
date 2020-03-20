---
title: Como usar o Azure PowerShell no Docker
description: Como usar o Azure PowerShell que é pré-instalado em uma imagem do Docker.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.openlocfilehash: a5746b71cfc41f7c6283b0e95b0940ca4b594ec7
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2020
ms.locfileid: "79402673"
---
# <a name="using-azure-powershell-in-docker"></a><span data-ttu-id="63b73-103">Como usar o Azure PowerShell no Docker</span><span class="sxs-lookup"><span data-stu-id="63b73-103">Using Azure PowerShell in Docker</span></span>

<span data-ttu-id="63b73-104">Estamos publicando imagens do Docker com o Azure PowerShell pré-instalado.</span><span class="sxs-lookup"><span data-stu-id="63b73-104">We are publishing Docker images with Azure PowerShell preinstalled.</span></span> <span data-ttu-id="63b73-105">Este artigo mostra como começar a usar o Azure PowerShell no contêiner do Docker.</span><span class="sxs-lookup"><span data-stu-id="63b73-105">This article shows you how to get started using Azure PowerShell in the Docker container.</span></span>

## <a name="finding-available-images"></a><span data-ttu-id="63b73-106">Localizar imagens disponíveis</span><span class="sxs-lookup"><span data-stu-id="63b73-106">Finding available images</span></span>

<span data-ttu-id="63b73-107">As imagens liberadas exigem o Docker 17.05 ou mais recente.</span><span class="sxs-lookup"><span data-stu-id="63b73-107">The released images require Docker 17.05 or newer.</span></span> <span data-ttu-id="63b73-108">Também é esperado que você possa executar o Docker sem `sudo` ou direitos administrativos locais.</span><span class="sxs-lookup"><span data-stu-id="63b73-108">It is also expected that you are able to run Docker without `sudo` or local administrative rights.</span></span> <span data-ttu-id="63b73-109">Siga as [instruções][install] oficiais do Docker para instalar o `docker` corretamente.</span><span class="sxs-lookup"><span data-stu-id="63b73-109">Please follow Docker's official [instructions][install] to install `docker` correctly.</span></span>

<span data-ttu-id="63b73-110">Os contêineres liberados são criados com base nos contêineres oficiais do PowerShell e, em seguida, o módulo Az é adicionado como uma camada.</span><span class="sxs-lookup"><span data-stu-id="63b73-110">The released containers are built from the official PowerShell containers, then the Az module added as a layer.</span></span>

<span data-ttu-id="63b73-111">A imagem estável mais recente inclui:</span><span class="sxs-lookup"><span data-stu-id="63b73-111">The latest stable image includes:</span></span>

- <span data-ttu-id="63b73-112">Ubuntu 18.04</span><span class="sxs-lookup"><span data-stu-id="63b73-112">Ubuntu 18.04</span></span>
- <span data-ttu-id="63b73-113">PowerShell versão 6.2.4</span><span class="sxs-lookup"><span data-stu-id="63b73-113">PowerShell version 6.2.4</span></span>
- <span data-ttu-id="63b73-114">Módulo Az mais atual do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="63b73-114">Azure PowerShell most current Az module</span></span>

<span data-ttu-id="63b73-115">Uma lista completa de imagens disponíveis pode ser encontrada em nossa página de [imagem do Docker][az image].</span><span class="sxs-lookup"><span data-stu-id="63b73-115">A full list of available images can be found on our [Docker image][az image] page.</span></span>

## <a name="using-azure-powershell-in-a-container"></a><span data-ttu-id="63b73-116">Usar o Azure PowerShell em um contêiner</span><span class="sxs-lookup"><span data-stu-id="63b73-116">Using Azure PowerShell in a container</span></span>

<span data-ttu-id="63b73-117">As etapas a seguir mostram os comandos do Docker necessários para baixar a imagem e iniciar uma sessão interativa do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="63b73-117">The following steps show the Docker commands required to download the image and start an interactive PowerShell session.</span></span>

1. <span data-ttu-id="63b73-118">Baixe a imagem do azure-powershell mais recente.</span><span class="sxs-lookup"><span data-stu-id="63b73-118">Download the latest azure-powershell image.</span></span>

   ```console
   docker pull mcr.microsoft.com/azure-powershell
   ```

1. <span data-ttu-id="63b73-119">Execute o contêiner do azure-powershell no modo interativo:</span><span class="sxs-lookup"><span data-stu-id="63b73-119">Run the azure-powershell container in interactive mode:</span></span>

   ```console
   docker run -it mcr.microsoft.com/azure-powershell pwsh
   ```

### <a name="run-the-azure-powershell-container-interactively-using-host-authentication"></a><span data-ttu-id="63b73-120">Executar o contêiner do azure-powershell interativamente usando a autenticação de host</span><span class="sxs-lookup"><span data-stu-id="63b73-120">Run the azure-powershell container interactively using host authentication</span></span>

<span data-ttu-id="63b73-121">Se já tiver o Azure PowerShell instalado no sistema que hospeda o Docker, você poderá ter credenciais do Azure em cache.</span><span class="sxs-lookup"><span data-stu-id="63b73-121">If you have Azure PowerShell already installed on the system hosting Docker, you may have cached Azure credentials.</span></span> <span data-ttu-id="63b73-122">Essas credenciais podem ser usadas na sessão do PowerShell em execução no contêiner do Docker.</span><span class="sxs-lookup"><span data-stu-id="63b73-122">These credentials can be used in the PowerShell session running in the Docker container.</span></span>

<span data-ttu-id="63b73-123">Por padrão, as credenciais armazenadas em cache ficam no diretório `$HOME/.Azure` no host.</span><span class="sxs-lookup"><span data-stu-id="63b73-123">By default, the cached credentials are in `$HOME/.Azure` directory on your host.</span></span> <span data-ttu-id="63b73-124">O serviço do Docker deve ter acesso a esse local para acessar as credenciais.</span><span class="sxs-lookup"><span data-stu-id="63b73-124">The Docker service must have access to this location to access the credentials.</span></span> <span data-ttu-id="63b73-125">O comando a seguir inicia o contêiner com o cache de credenciais montado e inicia uma sessão interativa do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="63b73-125">The following command starts the container with the credential cache mounted and starts an interactive PowerShell session.</span></span>

```console
docker run -it -v ~/.Azure/AzureRmContext.json:/root/.Azure/AzureRmContext.json -v ~/.Azure/TokenCache.dat:/root/.Azure/TokenCache.dat mcr.microsoft.com/azure-powershell pwsh
```

### <a name="remove-the-image-when-no-longer-needed"></a><span data-ttu-id="63b73-126">Remover a imagem quando não for mais necessária</span><span class="sxs-lookup"><span data-stu-id="63b73-126">Remove the image when no longer needed</span></span>

<span data-ttu-id="63b73-127">O comando a seguir é usado para excluir o contêiner do Docker quando você não precisar mais dele.</span><span class="sxs-lookup"><span data-stu-id="63b73-127">The following command is used to delete the Docker container when you no longer need it.</span></span>

```console
docker rmi mcr.microsoft.com/azure-powershell
```

## <a name="next-steps"></a><span data-ttu-id="63b73-128">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="63b73-128">Next steps</span></span>

<span data-ttu-id="63b73-129">Para saber mais sobre os módulos do Azure PowerShell e seus recursos, confira [Introdução ao Azure PowerShell](get-started-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="63b73-129">To learn more about the Azure PowerShell modules and their features, see [Get Started with Azure PowerShell](get-started-azureps.md).</span></span>

<!-- link references -->
[install]: https://docs.docker.com/engine/installation/
[powershell image]: https://hub.docker.com/_/microsoft-powershell
[az image]: https://hub.docker.com/_/microsoft-azure-powershell