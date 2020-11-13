---
title: Introdução ao Azure PowerShell
description: Introdução ao Azure PowerShell
ms.devlang: powershell
ms.topic: get-started-article
ms.date: 01/17/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 8958570285e3db264b3e0bb654acb7f38526354c
ms.sourcegitcommit: 2036538797dd088728aee5ac5021472454d82eb2
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2020
ms.locfileid: "93409798"
---
# <a name="get-started-with-azure-powershell"></a><span data-ttu-id="b1bf3-103">Introdução ao Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="b1bf3-103">Get started with Azure PowerShell</span></span>

<span data-ttu-id="b1bf3-104">O Azure PowerShell foi projetado para gerenciar e administrar recursos do Azure na linha de comando.</span><span class="sxs-lookup"><span data-stu-id="b1bf3-104">Azure PowerShell is designed for managing and administering Azure resources from the command line.</span></span> <span data-ttu-id="b1bf3-105">Use o Azure PowerShell quando quiser compilar ferramentas automatizadas que usam o modelo do Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="b1bf3-105">Use Azure PowerShell when you want to build automated tools that use the Azure Resource Manager model.</span></span>
<span data-ttu-id="b1bf3-106">Teste-o em seu navegador com o [Azure Cloud Shell](/azure/cloud-shell/overview) ou instale-o em seu computador local.</span><span class="sxs-lookup"><span data-stu-id="b1bf3-106">Try it out in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview), or install on your local machine.</span></span>

<span data-ttu-id="b1bf3-107">Este artigo ajuda você a começar a usar o Azure PowerShell, além de ensinar os conceitos básicos por trás dele.</span><span class="sxs-lookup"><span data-stu-id="b1bf3-107">This article helps you get started with Azure PowerShell and teaches the core concepts behind it.</span></span>

## <a name="install-or-run-in-azure-cloud-shell"></a><span data-ttu-id="b1bf3-108">Instalar ou executar no Azure Cloud Shell</span><span class="sxs-lookup"><span data-stu-id="b1bf3-108">Install or run in Azure Cloud Shell</span></span>

<span data-ttu-id="b1bf3-109">A maneira mais fácil para começar a usar o Azure PowerShell é testando-o em um ambiente do Azure Cloud Shell.</span><span class="sxs-lookup"><span data-stu-id="b1bf3-109">The easiest way to get started with Azure PowerShell is by trying it out in an Azure Cloud Shell environment.</span></span>
<span data-ttu-id="b1bf3-110">Para começar a usar o Cloud Shell, confira [Início Rápido do PowerShell no Azure Cloud Shell](/azure/cloud-shell/quickstart-powershell).</span><span class="sxs-lookup"><span data-stu-id="b1bf3-110">To get up and running with Cloud Shell, see [Quickstart for PowerShell in Azure Cloud Shell](/azure/cloud-shell/quickstart-powershell).</span></span>
<span data-ttu-id="b1bf3-111">O Cloud Shell executa o PowerShell 6 em um contêiner do Linux, portanto, uma funcionalidade específica do Windows não está disponível.</span><span class="sxs-lookup"><span data-stu-id="b1bf3-111">Cloud Shell runs PowerShell 6 on a Linux container, so Windows-specific functionality isn't available.</span></span>

<span data-ttu-id="b1bf3-112">Quando você estiver pronto para instalar o Azure PowerShell em seu computador local, siga as instruções em [Instalar o módulo do Azure PowerShell](install-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="b1bf3-112">When you're ready to install Azure PowerShell on your local machine, follow the instructions in [Install the Azure PowerShell module](install-az-ps.md).</span></span>

## <a name="sign-in-to-azure"></a><span data-ttu-id="b1bf3-113">Entrar no Azure</span><span class="sxs-lookup"><span data-stu-id="b1bf3-113">Sign in to Azure</span></span>

<span data-ttu-id="b1bf3-114">Entre interativamente com o cmdlet `Connect-AzAccount`.</span><span class="sxs-lookup"><span data-stu-id="b1bf3-114">Sign in interactively with the `Connect-AzAccount` cmdlet.</span></span> <span data-ttu-id="b1bf3-115">Caso use o Cloud Shell, ignore esta etapa: Sua sessão do Azure Cloud Shell já está autenticada para o ambiente, a assinatura e o locatário que iniciaram a sessão do Cloud Shell.</span><span class="sxs-lookup"><span data-stu-id="b1bf3-115">Skip this step if you use Cloud Shell: Your Azure Cloud Shell session is already authenticated for the environment, subscription, and tenant that launched the Cloud Shell session.</span></span>

```azurepowershell-interactive
Connect-AzAccount
```

<span data-ttu-id="b1bf3-116">Se você estiver em uma região fora dos EUA, use o parâmetro `-Environment` para entrar.</span><span class="sxs-lookup"><span data-stu-id="b1bf3-116">If you're in a non-US region, use the `-Environment` parameter to sign in.</span></span> <span data-ttu-id="b1bf3-117">Obtenha o nome do ambiente para sua região usando o cmdlet [Get-AzEnvironment](/powershell/module/Az.Accounts/Get-AzEnvironment).</span><span class="sxs-lookup"><span data-stu-id="b1bf3-117">Get the name of the environment for your region by using the [Get-AzEnvironment](/powershell/module/Az.Accounts/Get-AzEnvironment) cmdlet.</span></span> <span data-ttu-id="b1bf3-118">Por exemplo, para entrar no Azure China 21Vianet:</span><span class="sxs-lookup"><span data-stu-id="b1bf3-118">For example, to sign in to Azure China 21Vianet:</span></span>

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

<span data-ttu-id="b1bf3-119">Em ambientes do PowerShell 5.1, você receberá uma caixa de diálogo de entrada para fornecer um nome de usuário e uma senha de sua conta do Azure.</span><span class="sxs-lookup"><span data-stu-id="b1bf3-119">In PowerShell 5.1 environments, you'll get a sign-in dialog to provide a username and password for your Azure account.</span></span> <span data-ttu-id="b1bf3-120">Em todas as outras versões do PowerShell, você receberá um token para usá-lo em [https://microsoft.com/devicelogin ].</span><span class="sxs-lookup"><span data-stu-id="b1bf3-120">On every other version of PowerShell, you'll get a token to use on [https://microsoft.com/devicelogin].</span></span>
<span data-ttu-id="b1bf3-121">Abra essa página no seu navegador e insira o token, depois entre com suas credenciais da conta do Azure e autorize o Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b1bf3-121">Open this page in your browser and enter the token, then sign in with your Azure account credentials and authorize Azure PowerShell.</span></span>

<span data-ttu-id="b1bf3-122">Depois de entrar, você verá informações indicando qual das suas assinaturas do Azure está ativa.</span><span class="sxs-lookup"><span data-stu-id="b1bf3-122">After signing in, you'll see information indicating which of your Azure subscriptions is active.</span></span> <span data-ttu-id="b1bf3-123">Caso você tenha várias assinaturas do Azure em sua conta e queira selecionar uma diferente, obtenha suas assinaturas disponíveis com o [Get-AzSubscription](/powershell/module/az.accounts/get-azsubscription) e use o cmdlet [Set-AzContext](/powershell/module/az.accounts/set-azcontext) com sua ID da assinatura.</span><span class="sxs-lookup"><span data-stu-id="b1bf3-123">If you have multiple Azure subscriptions in your account and want to select a different one, get your available subscriptions with [Get-AzSubscription](/powershell/module/az.accounts/get-azsubscription) and use the [Set-AzContext](/powershell/module/az.accounts/set-azcontext) cmdlet with your subscription ID.</span></span>
<span data-ttu-id="b1bf3-124">Para obter mais informações sobre como gerenciar suas assinaturas do Azure no Azure PowerShell, confira [Usar várias assinaturas do Azure](manage-subscriptions-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="b1bf3-124">For more information about managing your Azure subscriptions in Azure PowerShell, see [Use multiple Azure subscriptions](manage-subscriptions-azureps.md).</span></span>

<span data-ttu-id="b1bf3-125">Depois de entrar, use os cmdlets do Azure PowerShell para acessar e gerenciar os recursos em sua assinatura.</span><span class="sxs-lookup"><span data-stu-id="b1bf3-125">Once signed in, use the Azure PowerShell cmdlets to access and manage resources in your subscription.</span></span> <span data-ttu-id="b1bf3-126">Para saber mais sobre o processo de entrada e os métodos de autenticação, confira [Entrar com o Azure PowerShell](authenticate-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="b1bf3-126">To learn more about the sign-in process and authentication methods, see [Sign in with Azure PowerShell](authenticate-azureps.md).</span></span>

## <a name="find-commands"></a><span data-ttu-id="b1bf3-127">Localizar comandos</span><span class="sxs-lookup"><span data-stu-id="b1bf3-127">Find commands</span></span>

<span data-ttu-id="b1bf3-128">Os cmdlets do Azure PowerShell seguem uma convenção de nomenclatura padrão para o PowerShell, `VERB-NOUN`.</span><span class="sxs-lookup"><span data-stu-id="b1bf3-128">Azure PowerShell cmdlets follow a standard naming convention for PowerShell, `VERB-NOUN`.</span></span> <span data-ttu-id="b1bf3-129">O verbo descreve a ação (por exemplo, `New`, `Get`, `Set`, `Remove`) e o substantivo descreve o tipo de recurso (por exemplo, `AzVM`, `AzKeyVaultCertificate`, `AzFirewall`, `AzVirtualNetworkGateway`).</span><span class="sxs-lookup"><span data-stu-id="b1bf3-129">The verb describes the action (examples include `New`, `Get`, `Set`, `Remove`) and the noun describes the resource type (examples include `AzVM`, `AzKeyVaultCertificate`, `AzFirewall`, `AzVirtualNetworkGateway`).</span></span> <span data-ttu-id="b1bf3-130">Os substantivos no Azure PowerShell sempre começam com o prefixo `Az`.</span><span class="sxs-lookup"><span data-stu-id="b1bf3-130">Nouns in Azure PowerShell always start with the prefix `Az`.</span></span> <span data-ttu-id="b1bf3-131">Para obter a lista completa de verbos padrão, confira [Verbos aprovados para comandos do PowerShell](/powershell/scripting/developer/cmdlet/approved-verbs-for-windows-powershell-commands).</span><span class="sxs-lookup"><span data-stu-id="b1bf3-131">For the full list of standard verbs, see [Approved verbs for PowerShell Commands](/powershell/scripting/developer/cmdlet/approved-verbs-for-windows-powershell-commands).</span></span>

<span data-ttu-id="b1bf3-132">Conhecer os substantivos, verbos e os módulos disponíveis do Azure PowerShell ajudará você a localizar os comandos com o cmdlet [Get-Command](/powershell/module/microsoft.powershell.core/get-command).</span><span class="sxs-lookup"><span data-stu-id="b1bf3-132">Knowing the nouns, verbs, and the Azure PowerShell modules available help you find commands with the [Get-Command](/powershell/module/microsoft.powershell.core/get-command) cmdlet.</span></span> <span data-ttu-id="b1bf3-133">Por exemplo, para localizar todos os comandos relacionados à VM que usam o verbo `Get`:</span><span class="sxs-lookup"><span data-stu-id="b1bf3-133">For example, to find all VM-related commands that use the `Get` verb:</span></span>

```powershell-interactive
Get-Command -Verb Get -Noun AzVM* -Module Az.Compute
```

<span data-ttu-id="b1bf3-134">Para ajudar você a localizar os comandos comuns, esta tabela lista o tipo de recurso, o módulo correspondente do Azure PowerShell e o prefixo do substantivo para usar com `Get-Command`:</span><span class="sxs-lookup"><span data-stu-id="b1bf3-134">To help you find common commands, this table lists the resource type, corresponding Azure PowerShell module, and noun prefix to use with `Get-Command`:</span></span>

| <span data-ttu-id="b1bf3-135">Tipo de recurso</span><span class="sxs-lookup"><span data-stu-id="b1bf3-135">Resource type</span></span> | <span data-ttu-id="b1bf3-136">Módulo do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="b1bf3-136">Azure PowerShell module</span></span> | <span data-ttu-id="b1bf3-137">Prefixo do substantivo</span><span class="sxs-lookup"><span data-stu-id="b1bf3-137">Noun prefix</span></span> |
|---------------|-------------------------|----------------|
| [<span data-ttu-id="b1bf3-138">Grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="b1bf3-138">Resource group</span></span>](/azure/azure-resource-manager/resource-group-overview) | [<span data-ttu-id="b1bf3-139">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b1bf3-139">Az.Resources</span></span>](/powershell/module/az.resources#resources) | `AzResourceGroup` |
| [<span data-ttu-id="b1bf3-140">Máquinas virtuais</span><span class="sxs-lookup"><span data-stu-id="b1bf3-140">Virtual machines</span></span>](/azure/virtual-machines) | [<span data-ttu-id="b1bf3-141">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b1bf3-141">Az.Compute</span></span>](/powershell/module/az.compute#virtual_machines) | `AzVM` |
| [<span data-ttu-id="b1bf3-142">Contas de armazenamento</span><span class="sxs-lookup"><span data-stu-id="b1bf3-142">Storage accounts</span></span>](/azure/storage/common/storage-introduction) | [<span data-ttu-id="b1bf3-143">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b1bf3-143">Az.Storage</span></span>](/powershell/module/az.storage/) | `AzStorageAccount` |
| [<span data-ttu-id="b1bf3-144">Key Vault</span><span class="sxs-lookup"><span data-stu-id="b1bf3-144">Key Vault</span></span>](/azure/key-vault/key-vault-whatis) | [<span data-ttu-id="b1bf3-145">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b1bf3-145">Az.KeyVault</span></span>](/powershell/module/az.keyvault) | `AzKeyVault` |
| [<span data-ttu-id="b1bf3-146">Aplicativos Web</span><span class="sxs-lookup"><span data-stu-id="b1bf3-146">Web applications</span></span>](/azure/app-service) | [<span data-ttu-id="b1bf3-147">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b1bf3-147">Az.Websites</span></span>](/powershell/module/az.websites) | `AzWebApp` |
| [<span data-ttu-id="b1bf3-148">Bancos de dados SQL</span><span class="sxs-lookup"><span data-stu-id="b1bf3-148">SQL databases</span></span>](/azure/sql-database) | [<span data-ttu-id="b1bf3-149">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b1bf3-149">Az.Sql</span></span>](/powershell/module/az.sql) | `AzSqlDatabase` |

<span data-ttu-id="b1bf3-150">Para obter uma lista completa dos módulos do Azure PowerShell, confira a [lista de módulos do PowerShell do Azure](https://github.com/Azure/azure-powershell/blob/master/documentation/azure-powershell-modules.md) hospedada no GitHub.</span><span class="sxs-lookup"><span data-stu-id="b1bf3-150">For a full list of the modules in Azure PowerShell, see the [Azure PowerShell modules list](https://github.com/Azure/azure-powershell/blob/master/documentation/azure-powershell-modules.md) hosted on GitHub.</span></span>

## <a name="learn-azure-powershell-basics-with-quickstarts-and-tutorials"></a><span data-ttu-id="b1bf3-151">Aprenda as noções básicas do Azure PowerShell com guias de início rápido e tutoriais</span><span class="sxs-lookup"><span data-stu-id="b1bf3-151">Learn Azure PowerShell basics with quickstarts and tutorials</span></span>

<span data-ttu-id="b1bf3-152">Para começar a usar o Azure PowerShell, teste um tutorial aprofundado para configurar máquinas virtuais e aprender como consultá-las.</span><span class="sxs-lookup"><span data-stu-id="b1bf3-152">To get started with Azure PowerShell, try an in-depth tutorial for setting up virtual machines and learning how to query them.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="b1bf3-153">Criar máquinas virtuais com o Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="b1bf3-153">Create virtual machines with Azure PowerShell</span></span>](azureps-vm-tutorial.yml)

<span data-ttu-id="b1bf3-154">Também há guias de início rápido do Azure PowerShell para outros serviços populares do Azure:</span><span class="sxs-lookup"><span data-stu-id="b1bf3-154">There are also Azure PowerShell quickstarts for other popular Azure services:</span></span>

* [<span data-ttu-id="b1bf3-155">Criar uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="b1bf3-155">Create a storage account</span></span>](/azure/storage/common/storage-quickstart-create-account?tabs=azure-powershell)
* [<span data-ttu-id="b1bf3-156">Transferir objetos de/para o armazenamento de Blobs do Azure</span><span class="sxs-lookup"><span data-stu-id="b1bf3-156">Transfer objects to/from Azure Blob storage</span></span>](/azure/storage/blobs/storage-quickstart-blobs-powershell)
* [<span data-ttu-id="b1bf3-157">Criar e recuperar segredos do Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="b1bf3-157">Create and retrieve secrets from Azure Key Vault</span></span>](/azure/key-vault/quick-create-powershell)
* [<span data-ttu-id="b1bf3-158">Criar um firewall e um banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="b1bf3-158">Create an Azure SQL database and firewall</span></span>](/azure/sql-database/scripts/sql-database-create-and-configure-database-powershell)
* [<span data-ttu-id="b1bf3-159">Executar um contêiner em Instâncias de Contêiner do Azure</span><span class="sxs-lookup"><span data-stu-id="b1bf3-159">Run a container in Azure Container Instances</span></span>](/azure/container-instances/container-instances-quickstart-powershell)
* [<span data-ttu-id="b1bf3-160">Criar um VMSS (Conjunto de Dimensionamento de Máquina Virtual)</span><span class="sxs-lookup"><span data-stu-id="b1bf3-160">Create a Virtual Machine Scale Set (VMSS)</span></span>](/azure/virtual-machine-scale-sets/quick-create-powershell)
* [<span data-ttu-id="b1bf3-161">Criar um balanceador de carga padrão</span><span class="sxs-lookup"><span data-stu-id="b1bf3-161">Create a standard load balancer</span></span>](/azure/load-balancer/quickstart-create-standard-load-balancer-powershell)

## <a name="next-steps"></a><span data-ttu-id="b1bf3-162">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="b1bf3-162">Next steps</span></span>

* [<span data-ttu-id="b1bf3-163">Entrar com o Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="b1bf3-163">Sign in with Azure PowerShell</span></span>](authenticate-azureps.md)
* [<span data-ttu-id="b1bf3-164">Gerenciar as assinaturas do Azure com o Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="b1bf3-164">Manage Azure subscriptions with Azure PowerShell</span></span>](manage-subscriptions-azureps.md)
* [<span data-ttu-id="b1bf3-165">Criar entidades de serviço com o Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="b1bf3-165">Create service principals with Azure PowerShell</span></span>](create-azure-service-principal-azureps.md)
* <span data-ttu-id="b1bf3-166">Obtenha ajuda da comunidade:</span><span class="sxs-lookup"><span data-stu-id="b1bf3-166">Get help from the community:</span></span>
  * [<span data-ttu-id="b1bf3-167">Fórum do Azure no MSDN</span><span class="sxs-lookup"><span data-stu-id="b1bf3-167">Azure forum on MSDN</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=320212)
  * [<span data-ttu-id="b1bf3-168">Stack Overflow</span><span class="sxs-lookup"><span data-stu-id="b1bf3-168">Stack Overflow</span></span>](https://go.microsoft.com/fwlink/?LinkId=320213)
