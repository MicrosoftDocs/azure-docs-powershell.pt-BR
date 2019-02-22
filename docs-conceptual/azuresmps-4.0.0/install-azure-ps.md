---
title: Instalar e configurar o módulo Gerenciamento de Serviços do Azure PowerShell | Microsoft Docs
description: Como instalar e configurar o Azure PowerShell para o primeiro uso.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/06/2017
ms.openlocfilehash: b7283e4a54cd423282141c07750630050799d59c
ms.sourcegitcommit: 2054a8f74cd9bf5a50ea7fdfddccaa632c842934
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/12/2019
ms.locfileid: "56152946"
---
# <a name="installing-the-azure-powershell-service-management-module"></a><span data-ttu-id="cb377-103">Instalação do módulo de Gerenciamento de Serviços do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="cb377-103">Installing the Azure PowerShell Service Management module</span></span>

<span data-ttu-id="cb377-104">Instalar o Azure PowerShell a partir da [Galeria do PowerShell](https://www.powershellgallery.com/) é o método preferido de instalação.</span><span class="sxs-lookup"><span data-stu-id="cb377-104">Installing Azure PowerShell from the [PowerShell Gallery](https://www.powershellgallery.com/) is the preferred method of installation.</span></span>

## <a name="step-1-install-powershellget"></a><span data-ttu-id="cb377-105">Etapa 1: Instalar o PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="cb377-105">Step 1: Install PowerShellGet</span></span>

<span data-ttu-id="cb377-106">Instalar os itens da Galeria do PowerShell requer o módulo PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="cb377-106">Installing items from the PowerShell Gallery requires the PowerShellGet module.</span></span> <span data-ttu-id="cb377-107">Verifique se que você tem a versão apropriada do PowerShellGet e outros requisitos do sistema.</span><span class="sxs-lookup"><span data-stu-id="cb377-107">Make sure you have the appropriate version of PowerShellGet and other system requirements.</span></span> <span data-ttu-id="cb377-108">Execute o seguinte comando para ver se você tem o PowerShellGet instalado em seu sistema.</span><span class="sxs-lookup"><span data-stu-id="cb377-108">Run the following command to see if you have PowerShellGet installed on your system.</span></span>

```powershell
Get-InstalledModule PowerShellGet -AllVersions | Select-Object Name,Version,Path
```

<span data-ttu-id="cb377-109">Você deverá ver algo semelhante à seguinte saída:</span><span class="sxs-lookup"><span data-stu-id="cb377-109">You should see something similar to the following output:</span></span>

```output
Name          Version Path
----          ------- ----
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

<span data-ttu-id="cb377-110">Se você não tiver o PowerShellGet instalado, consulte [Como obter o PowerShellGet](#how-to-get-powershellget).</span><span class="sxs-lookup"><span data-stu-id="cb377-110">If you do not have PowerShellGet installed, see the [How to get PowerShellGet](#how-to-get-powershellget).</span></span>

## <a name="step-2-install-azure-powershell"></a><span data-ttu-id="cb377-111">Etapa 2: Instalar o Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="cb377-111">Step 2: Install Azure PowerShell</span></span>

<span data-ttu-id="cb377-112">Execute o seguinte comando no console do Windows PowerShell como Administrador:</span><span class="sxs-lookup"><span data-stu-id="cb377-112">Run the following command from the Windows PowerShell console running as Administrator:</span></span>

```powershell
Install-Module Azure
```

<span data-ttu-id="cb377-113">O Azure é um módulo do pacote cumulativo de atualizações para os cmdlets do Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="cb377-113">The Azure module is a rollup module for the Azure Resource Manager cmdlets.</span></span> <span data-ttu-id="cb377-114">Ao instalar o módulo AzureRM, qualquer outro módulo do Azure que não tiver sido instalado anteriormente será baixado e instalado usando a Galeria do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="cb377-114">When you install the AzureRM module, any other Azure modules that have not previously been installed will be downloaded and installed from the PowerShell Gallery.</span></span>

<span data-ttu-id="cb377-115">O módulo Gerenciamento de Serviços do Azure compartilha dependências com os módulos Azure PowerShell Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="cb377-115">The Azure Service Management module shares dependencies with the Azure PowerShell Resource Manager modules.</span></span> <span data-ttu-id="cb377-116">Se você instalou os módulos do Azure PowerShell Resource Manager, será necessário adicionar o parâmetro `-AllowClobber` ao comando de instalação.</span><span class="sxs-lookup"><span data-stu-id="cb377-116">If you have installed the Azure PowerShell Resource Manager modules, you will need to add the `-AllowClobber` parameter to the install command.</span></span> <span data-ttu-id="cb377-117">Isso permite a atualização dessas dependências compartilhadas existentes.</span><span class="sxs-lookup"><span data-stu-id="cb377-117">This allows this existing shared dependencies to be updated.</span></span> <span data-ttu-id="cb377-118">Sem esse parâmetro, a instalação do módulo falha.</span><span class="sxs-lookup"><span data-stu-id="cb377-118">Without this parameter, installation of the module fails.</span></span>

```powershell
Install-Module Azure -AllowClobber
```

<span data-ttu-id="cb377-119">Depois de instalar esse módulo, você pode importar o módulo executando o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="cb377-119">After you install this module, you can import the module by running the following command:</span></span>

```powershell
Import-Module Azure
```

## <a name="to-use-the-cmdlets"></a><span data-ttu-id="cb377-120">Para usar os cmdlets</span><span class="sxs-lookup"><span data-stu-id="cb377-120">To use the cmdlets</span></span>

<span data-ttu-id="cb377-121">Para começar a trabalhar com os cmdlets de Gerenciamento de Serviços do Azure, primeiro faça logon em sua conta do Azure.</span><span class="sxs-lookup"><span data-stu-id="cb377-121">To start working with the Azure Service Management cmdlets, first log on to your Azure account.</span></span> <span data-ttu-id="cb377-122">Para fazer logon em sua conta, execute o comando a seguir:</span><span class="sxs-lookup"><span data-stu-id="cb377-122">To log on to your account, run the following command:</span></span>

```powershell
Add-AzureAccount
```

<span data-ttu-id="cb377-123">Após fazer logon no Azure, o Azure PowerShell cria um contexto para a sessão específica.</span><span class="sxs-lookup"><span data-stu-id="cb377-123">After logging into Azure, Azure PowerShell creates a context for the given session.</span></span> <span data-ttu-id="cb377-124">Esse contexto contém o ambiente, a conta, o locatário e a assinatura do Azure PowerShell que será usada para todos os cmdlets dentro dessa sessão.</span><span class="sxs-lookup"><span data-stu-id="cb377-124">That context contains the Azure PowerShell environment, account, tenant, and subscription that will be used for all cmdlets within that session.</span></span> <span data-ttu-id="cb377-125">Agora você está pronto para usar os módulos abaixo.</span><span class="sxs-lookup"><span data-stu-id="cb377-125">Now you are ready to use the modules below.</span></span>

## <a name="azure-service-management-cmdlets"></a><span data-ttu-id="cb377-126">Cmdlets do Azure Service Management</span><span class="sxs-lookup"><span data-stu-id="cb377-126">Azure Service Management cmdlets</span></span>

<span data-ttu-id="cb377-127">Módulos do Azure PowerShell são atualizados com frequência.</span><span class="sxs-lookup"><span data-stu-id="cb377-127">Azure PowerShell modules are updated frequently.</span></span> <span data-ttu-id="cb377-128">Se você perceber que a ajuda online do cmdlet inclui cmdlets ou parâmetros que não estão em seu módulo, baixe e instale a versão mais recente do módulo.</span><span class="sxs-lookup"><span data-stu-id="cb377-128">If you notice that the online cmdlet help includes cmdlets or parameters that are not in your module, download and install the latest version of the module.</span></span> <span data-ttu-id="cb377-129">Para localizar a versão de seu módulo, digite: `(Get-InstalledModule Azure).Version`.</span><span class="sxs-lookup"><span data-stu-id="cb377-129">To find the version of your module, type: `(Get-InstalledModule Azure).Version`.</span></span>

<span data-ttu-id="cb377-130">Para obter exemplos de scripts que podem ajudar você a automatizar algumas tarefas comuns no Azure, consulte o [Centro de Script do Windows Azure](http://www.windowsazure.com/documentation/scripts/).</span><span class="sxs-lookup"><span data-stu-id="cb377-130">For sample scripts that can help you automate some of the common tasks in Azure, see the [Windows Azure Script Center](http://www.windowsazure.com/documentation/scripts/).</span></span>

<span data-ttu-id="cb377-131">Para obter informações gerais sobre como instalar, aprender, usar e personalizar o Windows PowerShell, consulte [Criar scripts com o Windows PowerShell](http://go.microsoft.com/fwlink/p/?linkid=320210).</span><span class="sxs-lookup"><span data-stu-id="cb377-131">For general information about installing, learning, using, and customizing Windows PowerShell, see [Scripting with Windows PowerShell](http://go.microsoft.com/fwlink/p/?linkid=320210).</span></span>

### <a name="how-to-get-powershellget"></a><span data-ttu-id="cb377-132">Como obter o PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="cb377-132">How to get PowerShellGet</span></span>

|<span data-ttu-id="cb377-133">Versão do SO</span><span class="sxs-lookup"><span data-stu-id="cb377-133">OS Version</span></span>|<span data-ttu-id="cb377-134">Instalar instruções</span><span class="sxs-lookup"><span data-stu-id="cb377-134">Install instructions</span></span>|
|---|---|
|<span data-ttu-id="cb377-135">Tenho o Windows 10 ou o Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="cb377-135">I have Windows 10 or Windows Server 2016</span></span>|<span data-ttu-id="cb377-136">Compilado no Windows Management Framework (WMF) 5.0 incluído no SO</span><span class="sxs-lookup"><span data-stu-id="cb377-136">Built into Windows Management Framework (WMF) 5.0 included in the OS</span></span>|
|<span data-ttu-id="cb377-137">Desejo fazer uma atualização para o PowerShell 5</span><span class="sxs-lookup"><span data-stu-id="cb377-137">I want to upgrade to PowerShell 5</span></span>|[<span data-ttu-id="cb377-138">Instalar a versão mais recente do WMF</span><span class="sxs-lookup"><span data-stu-id="cb377-138">Install the latest version of WMF</span></span>](https://www.microsoft.com/en-us/download/details.aspx?id=54616)|
|<span data-ttu-id="cb377-139">Estou executando uma versão do Windows com o PowerShell 3 ou 4</span><span class="sxs-lookup"><span data-stu-id="cb377-139">I am running on a version of Windows with PowerShell 3 or PowerShell 4</span></span>|[<span data-ttu-id="cb377-140">Obter os módulos PackageManagement</span><span class="sxs-lookup"><span data-stu-id="cb377-140">Get the PackageManagement modules</span></span>](http://go.microsoft.com/fwlink/?LinkID=746217)|

<div id="helpmechoose"/>

### <a name="checking-the-version-of-azure-powershell"></a><span data-ttu-id="cb377-141">Verificando a versão do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="cb377-141">Checking the version of Azure PowerShell</span></span>

<span data-ttu-id="cb377-142">Embora recomendemos que você atualize para a última versão o mais cedo possível, várias versões do Azure PowerShell são suportadas.</span><span class="sxs-lookup"><span data-stu-id="cb377-142">Although we encourage you to upgrade to the latest version as early as possible, several versions of Azure PowerShell are support.</span></span> <span data-ttu-id="cb377-143">Para determinar a versão do Azure PowerShell instalada, execute `Get-InstalledModule Azure` na linha de comando.</span><span class="sxs-lookup"><span data-stu-id="cb377-143">To determine the version of Azure PowerShell you have installed, run `Get-InstalledModule Azure` from your command line.</span></span>

```powershell
Get-InstalledModule Azure -AllVersions | Select-Object Name,Version,Path
```
