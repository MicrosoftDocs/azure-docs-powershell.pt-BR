---
title: Introdução ao Azure PowerShell
description: ''
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: get-started-article
ms.date: 01/14/2019
ms.openlocfilehash: 0c3b749cb2ac7f11dacafca76b65944f523f727d
ms.sourcegitcommit: 0c012450805bef75472f48c74fe488baf6ba53bb
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2019
ms.locfileid: "66498147"
---
# <a name="get-started-with-azure-powershell"></a><span data-ttu-id="7afd8-102">Introdução ao Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="7afd8-102">Get started with Azure PowerShell</span></span>

<span data-ttu-id="7afd8-103">O Azure PowerShell foi projetado para gerenciar e administrar recursos do Azure na linha de comando.</span><span class="sxs-lookup"><span data-stu-id="7afd8-103">Azure PowerShell is designed for managing and administering Azure resources from the command line.</span></span> <span data-ttu-id="7afd8-104">Use o Azure PowerShell quando quiser compilar ferramentas automatizadas que usam o modelo do Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="7afd8-104">Use Azure PowerShell when you want to build automated tools that use the Azure Resource Manager model.</span></span>
<span data-ttu-id="7afd8-105">Teste-o em seu navegador com o [Azure Cloud Shell](/azure/cloud-shell/overview) ou instale-o em seu computador local.</span><span class="sxs-lookup"><span data-stu-id="7afd8-105">Try it out in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview), or install on your local machine.</span></span>

<span data-ttu-id="7afd8-106">Este artigo ajuda você a começar a usar o Azure PowerShell, além de ensinar os conceitos básicos por trás dele.</span><span class="sxs-lookup"><span data-stu-id="7afd8-106">This article helps you get started with Azure PowerShell and teaches the core concepts behind it.</span></span>

## <a name="install-or-run-in-azure-cloud-shell"></a><span data-ttu-id="7afd8-107">Instalar ou executar no Azure Cloud Shell</span><span class="sxs-lookup"><span data-stu-id="7afd8-107">Install or run in Azure Cloud Shell</span></span>

<span data-ttu-id="7afd8-108">A maneira mais fácil para começar a usar o Azure PowerShell é testando-o em um ambiente do Azure Cloud Shell.</span><span class="sxs-lookup"><span data-stu-id="7afd8-108">The easiest way to get started with Azure PowerShell is by trying it out in an Azure Cloud Shell environment.</span></span>
<span data-ttu-id="7afd8-109">Para começar a usar o Cloud Shell, confira [Início Rápido do PowerShell no Azure Cloud Shell](/azure/cloud-shell/quickstart-powershell).</span><span class="sxs-lookup"><span data-stu-id="7afd8-109">To get up and running with Cloud Shell, see [Quickstart for PowerShell in Azure Cloud Shell](/azure/cloud-shell/quickstart-powershell).</span></span>
<span data-ttu-id="7afd8-110">O Cloud Shell executa o PowerShell 6 em um contêiner do Linux, portanto, uma funcionalidade específica do Windows não está disponível.</span><span class="sxs-lookup"><span data-stu-id="7afd8-110">Cloud Shell runs PowerShell 6 on a Linux container, so Windows-specific functionality isn't available.</span></span>

<span data-ttu-id="7afd8-111">Quando você estiver pronto para instalar o Azure PowerShell em seu computador local, siga as instruções em [Instalar o módulo do Azure PowerShell](install-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="7afd8-111">When you're ready to install Azure PowerShell on your local machine, follow the instructions in [Install the Azure PowerShell module](install-az-ps.md).</span></span>

## <a name="sign-in-to-azure"></a><span data-ttu-id="7afd8-112">Entrar no Azure</span><span class="sxs-lookup"><span data-stu-id="7afd8-112">Sign in to Azure</span></span>

<span data-ttu-id="7afd8-113">Entre interativamente com o cmdlet `Connect-AzAccount`.</span><span class="sxs-lookup"><span data-stu-id="7afd8-113">Sign in interactively with the `Connect-AzAccount` cmdlet.</span></span> <span data-ttu-id="7afd8-114">Caso use o Cloud Shell, ignore esta etapa: Sua sessão do Azure Cloud Shell já está autenticada para o ambiente, a assinatura e o locatário que iniciaram a sessão do Cloud Shell.</span><span class="sxs-lookup"><span data-stu-id="7afd8-114">Skip this step if you use Cloud Shell: Your Azure Cloud Shell session is already authenticated for the environment, subscription, and tenant that launched the Cloud Shell session.</span></span>

```azurepowershell-interactive
Connect-AzAccount
```

<span data-ttu-id="7afd8-115">Se você estiver em uma região fora dos EUA, use o parâmetro `-Environment` para entrar.</span><span class="sxs-lookup"><span data-stu-id="7afd8-115">If you're in a non-US region, use the `-Environment` parameter to sign in.</span></span> <span data-ttu-id="7afd8-116">Obtenha o nome do ambiente para sua região usando o cmdlet [Get-AzEnvironment](/powershell/module/Az.Accounts/Get-AzEnvironment).</span><span class="sxs-lookup"><span data-stu-id="7afd8-116">Get the name of the environment for your region by using the [Get-AzEnvironment](/powershell/module/Az.Accounts/Get-AzEnvironment) cmdlet.</span></span> <span data-ttu-id="7afd8-117">Por exemplo, para entrar no Azure China 21Vianet:</span><span class="sxs-lookup"><span data-stu-id="7afd8-117">For example, to sign in to Azure China 21Vianet:</span></span>

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

<span data-ttu-id="7afd8-118">você receberá um token a ser usado em https://microsoft.com/devicelogin.</span><span class="sxs-lookup"><span data-stu-id="7afd8-118">You'll get a token to use on https://microsoft.com/devicelogin.</span></span> <span data-ttu-id="7afd8-119">Abra essa página no seu navegador e insira o token, depois entre com suas credenciais da conta do Azure e autorize o Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="7afd8-119">Open this page in your browser and enter the token, then sign in with your Azure account credentials and authorize Azure PowerShell.</span></span> 

<span data-ttu-id="7afd8-120">Depois de entrar, você verá informações indicando qual das suas assinaturas do Azure está ativa.</span><span class="sxs-lookup"><span data-stu-id="7afd8-120">After signing in, you'll see information indicating which of your Azure subscriptions is active.</span></span> <span data-ttu-id="7afd8-121">Caso você tenha várias assinaturas do Azure em sua conta e queira selecionar uma diferente, obtenha suas assinaturas disponíveis com o [Get-AzSubscription](/powershell/module/az.accounts/get-azsubscription) e use o cmdlet [Set-AzContext](/powershell/module/az.accounts/set-azcontext) com sua ID da assinatura.</span><span class="sxs-lookup"><span data-stu-id="7afd8-121">If you have multiple Azure subscriptions in your account and want to select a different one, get your available subscriptions with [Get-AzSubscription](/powershell/module/az.accounts/get-azsubscription) and use the [Set-AzContext](/powershell/module/az.accounts/set-azcontext) cmdlet with your subscription ID.</span></span>
<span data-ttu-id="7afd8-122">Para obter mais informações sobre como gerenciar suas assinaturas do Azure no Azure PowerShell, confira [Usar várias assinaturas do Azure](manage-subscriptions-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="7afd8-122">For more information about managing your Azure subscriptions in Azure PowerShell, see [Use multiple Azure subscriptions](manage-subscriptions-azureps.md).</span></span>

<span data-ttu-id="7afd8-123">Depois de entrar, use os cmdlets do Azure PowerShell para acessar e gerenciar os recursos em sua assinatura.</span><span class="sxs-lookup"><span data-stu-id="7afd8-123">Once signed in, use the Azure PowerShell cmdlets to access and manage resources in your subscription.</span></span> <span data-ttu-id="7afd8-124">Para saber mais sobre o processo de entrada e os métodos de autenticação, confira [Entrar com o Azure PowerShell](authenticate-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="7afd8-124">To learn more about the sign-in process and authentication methods, see [Sign in with Azure PowerShell](authenticate-azureps.md).</span></span>

## <a name="find-commands"></a><span data-ttu-id="7afd8-125">Localizar comandos</span><span class="sxs-lookup"><span data-stu-id="7afd8-125">Find commands</span></span>

<span data-ttu-id="7afd8-126">Os cmdlets do Azure PowerShell seguem uma convenção de nomenclatura padrão para o PowerShell, `VERB-NOUN`.</span><span class="sxs-lookup"><span data-stu-id="7afd8-126">Azure PowerShell cmdlets follow a standard naming convention for PowerShell, `VERB-NOUN`.</span></span> <span data-ttu-id="7afd8-127">O verbo descreve a ação (por exemplo, `Create`, `Get`, `Set`, `Delete`) e o substantivo descreve o tipo de recurso (por exemplo, `AzVM`, `AzKeyVaultCertificate`, `AzFirewall`, `AzVirtualNetworkGateway`).</span><span class="sxs-lookup"><span data-stu-id="7afd8-127">The verb describes the action (examples include `Create`, `Get`, `Set`, `Delete`) and the noun describes the resource type (examples include `AzVM`, `AzKeyVaultCertificate`, `AzFirewall`, `AzVirtualNetworkGateway`).</span></span> <span data-ttu-id="7afd8-128">Os substantivos no Azure PowerShell sempre começam com o prefixo `Az`.</span><span class="sxs-lookup"><span data-stu-id="7afd8-128">Nouns in Azure PowerShell always start with the prefix `Az`.</span></span> <span data-ttu-id="7afd8-129">Para obter a lista completa de verbos padrão, confira [Verbos aprovados para comandos do PowerShell](/powershell/developer/cmdlet/approved-verbs-for-windows-powershell-commands).</span><span class="sxs-lookup"><span data-stu-id="7afd8-129">For the full list of standard verbs, see [Approved verbs for PowerShell Commands](/powershell/developer/cmdlet/approved-verbs-for-windows-powershell-commands).</span></span>

<span data-ttu-id="7afd8-130">Conhecer os substantivos, verbos e os módulos disponíveis do Azure PowerShell ajudará você a localizar os comandos com o cmdlet [Get-Command](/powershell/module/microsoft.powershell.core/get-command).</span><span class="sxs-lookup"><span data-stu-id="7afd8-130">Knowing the nouns, verbs, and the Azure PowerShell modules available help you find commands with the [Get-Command](/powershell/module/microsoft.powershell.core/get-command) cmdlet.</span></span> <span data-ttu-id="7afd8-131">Por exemplo, para localizar todos os comandos relacionados à VM que usam o verbo `Get`:</span><span class="sxs-lookup"><span data-stu-id="7afd8-131">For example, to find all VM-related commands that use the `Get` verb:</span></span>

```powershell-interactive
Get-Command -Verb Get -Noun AzVM* -Module Az.Compute
```

<span data-ttu-id="7afd8-132">Para ajudar você a localizar os comandos comuns, esta tabela lista o tipo de recurso, o módulo correspondente do Azure PowerShell e o prefixo do substantivo para usar com `Get-Command`:</span><span class="sxs-lookup"><span data-stu-id="7afd8-132">To help you find common commands, this table lists the resource type, corresponding Azure PowerShell module, and noun prefix to use with `Get-Command`:</span></span>

| <span data-ttu-id="7afd8-133">Tipo de recurso</span><span class="sxs-lookup"><span data-stu-id="7afd8-133">Resource type</span></span> | <span data-ttu-id="7afd8-134">Módulo do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="7afd8-134">Azure PowerShell module</span></span> | <span data-ttu-id="7afd8-135">Prefixo do substantivo</span><span class="sxs-lookup"><span data-stu-id="7afd8-135">Noun prefix</span></span> |
|---------------|-------------------------|----------------|
| [<span data-ttu-id="7afd8-136">Grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="7afd8-136">Resource group</span></span>](/azure/azure-resource-manager/resource-group-overview) | [<span data-ttu-id="7afd8-137">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7afd8-137">Az.Resources</span></span>](/powershell/module/az.resources#resources) | `AzResourceGroup` |
| [<span data-ttu-id="7afd8-138">Máquinas virtuais</span><span class="sxs-lookup"><span data-stu-id="7afd8-138">Virtual machines</span></span>](/azure/virtual-machines) | [<span data-ttu-id="7afd8-139">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7afd8-139">Az.Compute</span></span>](/powershell/module/az.compute#virtual_machines) | `AzVM` |
| [<span data-ttu-id="7afd8-140">Contas de armazenamento</span><span class="sxs-lookup"><span data-stu-id="7afd8-140">Storage accounts</span></span>](/azure/storage/common/storage-introduction) | [<span data-ttu-id="7afd8-141">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7afd8-141">Az.Storage</span></span>](/powershell/module/az.storage/) | `AzStorageAccount` |
| [<span data-ttu-id="7afd8-142">Key Vault</span><span class="sxs-lookup"><span data-stu-id="7afd8-142">Key Vault</span></span>](/azure/key-vault/key-vault-whatis) | [<span data-ttu-id="7afd8-143">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7afd8-143">Az.KeyVault</span></span>](/powershell/module/az.keyvault) | `AzKeyVault` |
| [<span data-ttu-id="7afd8-144">Aplicativos Web</span><span class="sxs-lookup"><span data-stu-id="7afd8-144">Web applications</span></span>](/azure/app-service) | [<span data-ttu-id="7afd8-145">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7afd8-145">Az.Websites</span></span>](/powershell/module/az.websites) | `AzWebApp` |
| [<span data-ttu-id="7afd8-146">Bancos de dados SQL</span><span class="sxs-lookup"><span data-stu-id="7afd8-146">SQL databases</span></span>](/azure/sql-database) | [<span data-ttu-id="7afd8-147">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7afd8-147">Az.Sql</span></span>](/powershell/module/az.sql) | `AzSqlDatabase` |

<span data-ttu-id="7afd8-148">Para obter uma lista completa dos módulos do Azure PowerShell, confira a [lista de módulos do PowerShell do Azure](https://github.com/Azure/azure-powershell/blob/master/documentation/azure-powershell-modules.md) hospedada no GitHub.</span><span class="sxs-lookup"><span data-stu-id="7afd8-148">For a full list of the modules in Azure PowerShell, see the [Azure PowerShell modules list](https://github.com/Azure/azure-powershell/blob/master/documentation/azure-powershell-modules.md) hosted on GitHub.</span></span>

## <a name="learn-azure-powershell-basics-with-quickstarts-and-tutorials"></a><span data-ttu-id="7afd8-149">Aprenda as noções básicas do Azure PowerShell com guias de início rápido e tutoriais</span><span class="sxs-lookup"><span data-stu-id="7afd8-149">Learn Azure PowerShell basics with quickstarts and tutorials</span></span>

<span data-ttu-id="7afd8-150">Para começar a usar o Azure PowerShell, teste um tutorial aprofundado para configurar máquinas virtuais e aprender como consultá-las.</span><span class="sxs-lookup"><span data-stu-id="7afd8-150">To get started with Azure PowerShell, try an in-depth tutorial for setting up virtual machines and learning how to query them.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="7afd8-151">Criar máquinas virtuais com o Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="7afd8-151">Create virtual machines with Azure PowerShell</span></span>](azureps-vm-tutorial.yml)

<span data-ttu-id="7afd8-152">Também há guias de início rápido do Azure PowerShell para outros serviços populares do Azure:</span><span class="sxs-lookup"><span data-stu-id="7afd8-152">There are also Azure PowerShell quickstarts for other popular Azure services:</span></span>

* [<span data-ttu-id="7afd8-153">Criar uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="7afd8-153">Create a storage account</span></span>](/azure/storage/common/storage-quickstart-create-account?tabs=azure-powershell)
* [<span data-ttu-id="7afd8-154">Transferir objetos de/para o armazenamento de Blobs do Azure</span><span class="sxs-lookup"><span data-stu-id="7afd8-154">Transfer objects to/from Azure Blob storage</span></span>](/azure/storage/blobs/storage-quickstart-blobs-powershell)
* [<span data-ttu-id="7afd8-155">Criar e recuperar segredos do Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="7afd8-155">Create and retrieve secrets from Azure Key Vault</span></span>](/azure/key-vault/quick-create-powershell)
* [<span data-ttu-id="7afd8-156">Criar um firewall e um banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="7afd8-156">Create an Azure SQL database and firewall</span></span>](/azure/sql-database/scripts/sql-database-create-and-configure-database-powershell)
* [<span data-ttu-id="7afd8-157">Executar um contêiner em Instâncias de Contêiner do Azure</span><span class="sxs-lookup"><span data-stu-id="7afd8-157">Run a container in Azure Container Instances</span></span>](/azure/container-instances/container-instances-quickstart-powershell)
* [<span data-ttu-id="7afd8-158">Criar um VMSS (Conjunto de Dimensionamento de Máquina Virtual)</span><span class="sxs-lookup"><span data-stu-id="7afd8-158">Create a Virtual Machine Scale Set (VMSS)</span></span>](/azure/virtual-machine-scale-sets/quick-create-powershell)
* [<span data-ttu-id="7afd8-159">Criar um balanceador de carga padrão</span><span class="sxs-lookup"><span data-stu-id="7afd8-159">Create a standard load balancer</span></span>](/azure/load-balancer/quickstart-create-standard-load-balancer-powershell)

## <a name="next-steps"></a><span data-ttu-id="7afd8-160">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="7afd8-160">Next steps</span></span>

* [<span data-ttu-id="7afd8-161">Entrar com o Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="7afd8-161">Sign in with Azure PowerShell</span></span>](authenticate-azureps.md)
* [<span data-ttu-id="7afd8-162">Gerenciar as assinaturas do Azure com o Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="7afd8-162">Manage Azure subscriptions with Azure PowerShell</span></span>](manage-subscriptions-azureps.md)
* [<span data-ttu-id="7afd8-163">Criar entidades de serviço com o Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="7afd8-163">Create service principals with Azure PowerShell</span></span>](create-azure-service-principal-azureps.md)
* <span data-ttu-id="7afd8-164">Obtenha ajuda da comunidade:</span><span class="sxs-lookup"><span data-stu-id="7afd8-164">Get help from the community:</span></span>
  * [<span data-ttu-id="7afd8-165">Fórum do Azure no MSDN</span><span class="sxs-lookup"><span data-stu-id="7afd8-165">Azure forum on MSDN</span></span>](http://go.microsoft.com/fwlink/p/?LinkId=320212)
  * [<span data-ttu-id="7afd8-166">Stack Overflow</span><span class="sxs-lookup"><span data-stu-id="7afd8-166">Stack Overflow</span></span>](http://go.microsoft.com/fwlink/?LinkId=320213)