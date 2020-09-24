---
title: Contextos e credenciais de entrada do Azure
description: Aprenda a reutilizar as credenciais do Azure e outras informações em várias sessões do PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/21/2019
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: b6ac8b821f2d88431be67fd5fe1d50fc640d2b8f
ms.sourcegitcommit: 15f21c40dcb7610e2fbaaabf264ad925e4224500
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/22/2020
ms.locfileid: "90927903"
---
# <a name="azure-powershell-context-objects"></a><span data-ttu-id="6500c-103">Objetos de contexto do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="6500c-103">Azure PowerShell context objects</span></span>

<span data-ttu-id="6500c-104">O Azure PowerShell usa _objetos de contexto do Azure PowerShell_ (contextos do Azure) para armazenar as informações de assinatura e autenticação.</span><span class="sxs-lookup"><span data-stu-id="6500c-104">Azure PowerShell uses _Azure PowerShell context objects_ (Azure contexts) to hold subscription and authentication information.</span></span> <span data-ttu-id="6500c-105">Se tiver mais de uma assinatura, os contextos do Azure permitirão que você selecione a assinatura na qual executar os cmdlets do Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6500c-105">If you have more than one subscription, Azure contexts let you select the subscription to run Azure PowerShell cmdlets on.</span></span> <span data-ttu-id="6500c-106">Os contextos do Azure também são usados para armazenar informações de conexão em várias sessões do PowerShell e executar tarefas em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="6500c-106">Azure contexts are also used to store sign-in information across multiple PowerShell sessions and run background tasks.</span></span>

<span data-ttu-id="6500c-107">Este artigo aborda o gerenciamento de contextos do Azure, não o gerenciamento de assinaturas ou contas.</span><span class="sxs-lookup"><span data-stu-id="6500c-107">This article covers managing Azure contexts, not the management of subscriptions or accounts.</span></span> <span data-ttu-id="6500c-108">Se você estiver procurando gerenciar usuários, assinaturas, locatários ou outras informações de conta, confira a documentação do [Azure Active Directory](/azure/active-directory).</span><span class="sxs-lookup"><span data-stu-id="6500c-108">If you're looking to manage users, subscriptions, tenants, or other account information, see the [Azure Active Directory](/azure/active-directory) documentation.</span></span> <span data-ttu-id="6500c-109">Para saber mais sobre como usar contextos para executar tarefas em segundo plano ou em paralelo, confira [Usar cmdlets do Azure PowerShell em trabalhos do PowerShell](using-psjobs.md) depois de se familiarizar com os contextos do Azure.</span><span class="sxs-lookup"><span data-stu-id="6500c-109">To learn about using contexts for running background or parallel tasks, see [Use Azure PowerShell cmdlets in PowerShell jobs](using-psjobs.md) after becoming familiar with Azure contexts.</span></span>

## <a name="overview-of-azure-context-objects"></a><span data-ttu-id="6500c-110">Visão geral de objetos de contexto do Azure</span><span class="sxs-lookup"><span data-stu-id="6500c-110">Overview of Azure context objects</span></span>

<span data-ttu-id="6500c-111">Os contextos do Azure são objetos do PowerShell que representam sua assinatura ativa na qual executar comandos e as informações de autenticação necessárias para se conectar a uma nuvem do Azure.</span><span class="sxs-lookup"><span data-stu-id="6500c-111">Azure contexts are PowerShell objects representing your active subscription to run commands against, and the authentication information needed to connect to an Azure cloud.</span></span> <span data-ttu-id="6500c-112">Com os contextos do Azure, o Azure PowerShell não precisa autenticar novamente sua conta sempre que você mudar de assinaturas.</span><span class="sxs-lookup"><span data-stu-id="6500c-112">With Azure contexts, Azure PowerShell doesn't need to reauthenticate your account each time you switch subscriptions.</span></span> <span data-ttu-id="6500c-113">Um contexto do Azure é composto:</span><span class="sxs-lookup"><span data-stu-id="6500c-113">An Azure context consists of:</span></span>

* <span data-ttu-id="6500c-114">Pela _conta_ que foi usada para entrar no Azure com [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount).</span><span class="sxs-lookup"><span data-stu-id="6500c-114">The _account_ that was used to sign in to Azure with [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount).</span></span> <span data-ttu-id="6500c-115">Os contextos do Azure tratam usuários, IDs de aplicativo e entidades de serviço da mesma maneira de uma perspectiva de conta.</span><span class="sxs-lookup"><span data-stu-id="6500c-115">Azure contexts treat users, application IDs, and service principals the same from an account perspective.</span></span>
* <span data-ttu-id="6500c-116">Pela _assinatura_ ativa, um contrato de serviço com a Microsoft para criar e executar recursos do Azure, que estão associados a um _locatário_.</span><span class="sxs-lookup"><span data-stu-id="6500c-116">The active _subscription_, a service agreement with Microsoft to create and run Azure resources, which are associated with a _tenant_.</span></span> <span data-ttu-id="6500c-117">Os locatários costumam ser chamados de _organizações_ na documentação ou ao trabalhar com o Active Directory.</span><span class="sxs-lookup"><span data-stu-id="6500c-117">Tenants are often referred to as _organizations_ in documentation or when working with Active Directory.</span></span>
* <span data-ttu-id="6500c-118">Por uma referência a um _cache de token_, um token de autenticação armazenado para acessar uma nuvem do Azure.</span><span class="sxs-lookup"><span data-stu-id="6500c-118">A reference to a _token cache_, a stored authentication token for accessing an Azure cloud.</span></span> <span data-ttu-id="6500c-119">O local em que esse token é armazenado e por quanto tempo ele persiste é determinado pelas [configurações de salvamento automático de contexto](#save-azure-contexts-across-powershell-sessions).</span><span class="sxs-lookup"><span data-stu-id="6500c-119">Where this token is stored and how long it persists for is determined by the [context autosave settings](#save-azure-contexts-across-powershell-sessions).</span></span>

<span data-ttu-id="6500c-120">Para obter mais informações sobre esses termos, confira [Terminologia do Azure Active Directory](/azure/active-directory/fundamentals/active-directory-whatis#terminology).</span><span class="sxs-lookup"><span data-stu-id="6500c-120">For more information on these terms, see [Azure Active Directory Terminology](/azure/active-directory/fundamentals/active-directory-whatis#terminology).</span></span> <span data-ttu-id="6500c-121">Os tokens de autenticação usados por contextos do Azure são os mesmos que outros tokens armazenados que fazem parte de uma sessão persistente.</span><span class="sxs-lookup"><span data-stu-id="6500c-121">Authentication tokens used by Azure contexts are the same as other stored tokens that are part of a persistent session.</span></span> 

<span data-ttu-id="6500c-122">Quando você entra com `Connect-AzAccount`, pelo menos um contexto do Azure é criado para sua assinatura padrão.</span><span class="sxs-lookup"><span data-stu-id="6500c-122">When you sign in with `Connect-AzAccount`, at least one Azure context is created for your default subscription.</span></span> <span data-ttu-id="6500c-123">O objeto retornado por `Connect-AzAccount` é o contexto padrão do Azure usado para o restante da sessão do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6500c-123">The object returned by `Connect-AzAccount` is the default Azure context used for the rest of the PowerShell session.</span></span>

## <a name="get-azure-contexts"></a><span data-ttu-id="6500c-124">Obter contextos do Azure</span><span class="sxs-lookup"><span data-stu-id="6500c-124">Get Azure contexts</span></span>

<span data-ttu-id="6500c-125">Os contextos do Azure disponíveis são recuperados com o cmdlet [Get-AzContext](/powershell/module/az.accounts/get-azcontext).</span><span class="sxs-lookup"><span data-stu-id="6500c-125">Available Azure contexts are retrieved with the [Get-AzContext](/powershell/module/az.accounts/get-azcontext) cmdlet.</span></span> <span data-ttu-id="6500c-126">Liste todos os contextos disponíveis com `-ListAvailable`:</span><span class="sxs-lookup"><span data-stu-id="6500c-126">List all of the available contexts with `-ListAvailable`:</span></span>

```azurepowershell-interactive
Get-AzContext -ListAvailable
```

<span data-ttu-id="6500c-127">Ou obtenha um contexto por nome:</span><span class="sxs-lookup"><span data-stu-id="6500c-127">Or get a context by name:</span></span>

```azurepowershell-interactive
$context = Get-AzContext -Name "mycontext"
```

<span data-ttu-id="6500c-128">Os nomes de contexto podem ser diferentes do nome da assinatura associada.</span><span class="sxs-lookup"><span data-stu-id="6500c-128">Context names may be different from the name of the associated subscription.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6500c-129">Os contextos do Azure disponíveis __nem__ sempre são suas assinaturas disponíveis.</span><span class="sxs-lookup"><span data-stu-id="6500c-129">The available Azure contexts __aren't__ always your available subscriptions.</span></span> <span data-ttu-id="6500c-130">Os contextos do Azure representam apenas informações armazenadas localmente.</span><span class="sxs-lookup"><span data-stu-id="6500c-130">Azure contexts only represent locally-stored information.</span></span> <span data-ttu-id="6500c-131">Você pode obter suas assinaturas com o cmdlet [Get-AzSubscription](/powershell/module/Az.Accounts/Get-AzSubscription?view=azps-1.8.0).</span><span class="sxs-lookup"><span data-stu-id="6500c-131">You can get your subscriptions with the [Get-AzSubscription](/powershell/module/Az.Accounts/Get-AzSubscription?view=azps-1.8.0) cmdlet.</span></span>

## <a name="create-a-new-azure-context-from-subscription-information"></a><span data-ttu-id="6500c-132">Criar um contexto do Azure com base em informações de assinatura</span><span class="sxs-lookup"><span data-stu-id="6500c-132">Create a new Azure context from subscription information</span></span>

<span data-ttu-id="6500c-133">O cmdlet [Set-AzContext](/powershell/module/Az.Accounts/Set-AzContext) é usado para criar contextos do Azure e defini-los como o contexto ativo.</span><span class="sxs-lookup"><span data-stu-id="6500c-133">The [Set-AzContext](/powershell/module/Az.Accounts/Set-AzContext) cmdlet is used to both create new Azure contexts and set them as the active context.</span></span>
<span data-ttu-id="6500c-134">A maneira mais fácil de criar um contexto do Azure é usar informações de assinatura existentes.</span><span class="sxs-lookup"><span data-stu-id="6500c-134">The easiest way to create a new Azure context is to use existing subscription information.</span></span> <span data-ttu-id="6500c-135">O cmdlet é criado para usar o objeto de saída de `Get-AzSubscription` como um valor de pipe e configurar um novo contexto do Azure:</span><span class="sxs-lookup"><span data-stu-id="6500c-135">The cmdlet is designed to take the output object from `Get-AzSubscription` as a piped value and configure a new Azure context:</span></span>

```azurepowershell-interactive
Get-AzSubscription -SubscriptionName 'MySubscriptionName' | Set-AzContext -Name 'MyContextName'
```

<span data-ttu-id="6500c-136">Ou forneça o nome ou a ID da assinatura e a ID de locatário, se necessário:</span><span class="sxs-lookup"><span data-stu-id="6500c-136">Or give the subscription name or ID and the tenant ID if necessary:</span></span>

```azurepowershell-interactive
Set-AzContext -Name 'MyContextName' -Subscription 'MySubscriptionName' -Tenant '.......'
```

<span data-ttu-id="6500c-137">Se o argumento `-Name` for omitido, o nome e a ID da assinatura serão usados como o nome do contexto no formato `Subscription Name (subscription-id)`.</span><span class="sxs-lookup"><span data-stu-id="6500c-137">If the `-Name` argument is omitted, then the subscription's name and ID are used as the context name in the format `Subscription Name (subscription-id)`.</span></span>

## <a name="change-the-active-azure-context"></a><span data-ttu-id="6500c-138">Alterar o contexto do Azure ativo</span><span class="sxs-lookup"><span data-stu-id="6500c-138">Change the active Azure context</span></span>

<span data-ttu-id="6500c-139">Tanto `Set-AzContext` quanto [Select-AzContext](/powershell/module/az.accounts/set-azcontext) podem ser usados para alterar o contexto do Azure ativo.</span><span class="sxs-lookup"><span data-stu-id="6500c-139">Both `Set-AzContext` and [Select-AzContext](/powershell/module/az.accounts/set-azcontext) can be used to change the active Azure context.</span></span> <span data-ttu-id="6500c-140">Conforme descrito em [Criar um contexto do Azure](#create-a-new-azure-context-from-subscription-information), `Set-AzContext` criará um contexto do Azure para uma assinatura se não existir um e alternará para usar esse contexto como o ativo.</span><span class="sxs-lookup"><span data-stu-id="6500c-140">As described in [Create a new Azure context](#create-a-new-azure-context-from-subscription-information), `Set-AzContext` creates a new Azure context for a subscription if one doesn't exist, and then switches to use that context as the active one.</span></span>

<span data-ttu-id="6500c-141">O `Select-AzContext` destina-se a ser usado somente com contextos existentes do Azure e funciona de forma semelhante ao uso de `Set-AzContext -Context`, mas foi projetado para uso com o redirecionamento:</span><span class="sxs-lookup"><span data-stu-id="6500c-141">`Select-AzContext` is meant to be used with existing Azure contexts only and works similarly to using `Set-AzContext -Context`, but is designed for use with piping:</span></span>

```azurepowershell-interactive
Set-AzContext -Context $(Get-AzContext -Name "mycontext") # Set a context with an inline Azure context object
Get-AzContext -Name "mycontext" | Select-AzContext # Set a context with a piped Azure context object
```

<span data-ttu-id="6500c-142">Como muitos outros comandos de gerenciamento de conta e de contexto no Azure PowerShell, `Set-AzContext` e `Select-AzContext` dão suporte ao argumento `-Scope` para que você possa controlar por quanto tempo o contexto está ativo.</span><span class="sxs-lookup"><span data-stu-id="6500c-142">Like many other account and context management commands in Azure PowerShell, `Set-AzContext` and `Select-AzContext` support the `-Scope` argument so that you can control how long the context is active.</span></span> <span data-ttu-id="6500c-143">`-Scope` permite que você altere o contexto ativo de uma única sessão sem alterar o padrão:</span><span class="sxs-lookup"><span data-stu-id="6500c-143">`-Scope` lets you change a single session's active context without changing the default:</span></span>

```azurepowershell-interactive
Get-AzContext -Name "mycontext" | Select-AzContext -Scope Process
```

<span data-ttu-id="6500c-144">Para evitar alternar contextos para uma sessão inteira do PowerShell, todos os comandos do Azure PowerShell podem ser executados em um contexto determinado com o argumento `-AzContext`:</span><span class="sxs-lookup"><span data-stu-id="6500c-144">To avoid switching contexts for a whole PowerShell session, all Azure PowerShell commands can be run against a given context with the `-AzContext` argument:</span></span>

```azurepowershell-interactive
$context = Get-AzContext -Name "mycontext"
New-AzVM -Name ExampleVM -AzContext $context
```

<span data-ttu-id="6500c-145">O outro uso principal de contextos com cmdlets do Azure PowerShell é executar comandos em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="6500c-145">The other main use of contexts with Azure PowerShell cmdlets is to run background commands.</span></span> <span data-ttu-id="6500c-146">Para saber mais sobre como executar Trabalhos do PowerShell usando o Azure PowerShell, confira [Executar cmdlets do Azure PowerShell nos Trabalhos do PowerShell](using-psjobs.md).</span><span class="sxs-lookup"><span data-stu-id="6500c-146">To learn more about running PowerShell Jobs using Azure PowerShell, see [Run Azure PowerShell cmdlets in PowerShell Jobs](using-psjobs.md).</span></span>

## <a name="save-azure-contexts-across-powershell-sessions"></a><span data-ttu-id="6500c-147">Salvar contextos do Azure em sessões do PowerShell</span><span class="sxs-lookup"><span data-stu-id="6500c-147">Save Azure contexts across PowerShell sessions</span></span>

<span data-ttu-id="6500c-148">Por padrão, os contextos do Azure são salvos para uso entre sessões do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6500c-148">By default, Azure contexts are saved for use between PowerShell sessions.</span></span> <span data-ttu-id="6500c-149">Você muda esse comportamento das seguintes maneiras:</span><span class="sxs-lookup"><span data-stu-id="6500c-149">You change this behavior in the following ways:</span></span>

* <span data-ttu-id="6500c-150">Entre usando o `-Scope Process` com o `Connect-AzAccount`.</span><span class="sxs-lookup"><span data-stu-id="6500c-150">Sign in using `-Scope Process` with `Connect-AzAccount`.</span></span>

  ```azurepowershell
  Connect-AzAccount -Scope Process
  ```

  <span data-ttu-id="6500c-151">O contexto do Azure retornado como parte dessa entrada é válido _apenas_ para a sessão atual e não será salvo automaticamente, independentemente da configuração de salvamento automático do contexto do Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6500c-151">The Azure context returned as part of this sign in is valid for the current session _only_ and will not be automatically saved, regardless of the Azure PowerShell context autosave setting.</span></span>
* <span data-ttu-id="6500c-152">Desabilite o salvamento automático do contexto do AzurePowershell com o cmdlet [Disable-AzContextAutosave](/powershell/module/az.accounts/disable-azcontextautosave).</span><span class="sxs-lookup"><span data-stu-id="6500c-152">Disable AzurePowershell's context autosave with the [Disable-AzContextAutosave](/powershell/module/az.accounts/disable-azcontextautosave) cmdlet.</span></span>
  <span data-ttu-id="6500c-153">Desabilitar o salvamento automático de contexto __não__ limpa os tokens armazenados.</span><span class="sxs-lookup"><span data-stu-id="6500c-153">Disabling context autosave __doesn't__ clear any stored tokens.</span></span> <span data-ttu-id="6500c-154">Para saber como limpar informações de contexto do Azure armazenadas, confira [Remover contextos e credenciais do Azure](#remove-azure-contexts-and-stored-credentials).</span><span class="sxs-lookup"><span data-stu-id="6500c-154">To learn how to clear stored Azure context information, see [Remove Azure contexts and credentials](#remove-azure-contexts-and-stored-credentials).</span></span>
* <span data-ttu-id="6500c-155">Habilitar explicitamente o salvamento automático de contexto do Azure pode ser habilitado com o cmdlet [Disable-AzContextAutosave](/powershell/module/az.accounts/enable-azcontextautosave).</span><span class="sxs-lookup"><span data-stu-id="6500c-155">Explicitly enable Azure context autosave can be enabled with the [Enable-AzContextAutosave](/powershell/module/az.accounts/enable-azcontextautosave) cmdlet.</span></span> <span data-ttu-id="6500c-156">Com o salvamento automático habilitado, todos os contextos de um usuário são armazenados localmente para sessões posteriores do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6500c-156">With autosave enabled, all of a user's contexts are stored locally for later PowerShell sessions.</span></span>
* <span data-ttu-id="6500c-157">Salve manualmente contextos com [Save-AzContext](/powershell/module/az.accounts/save-azcontext) para serem usados em sessões futuras do PowerShell, em que eles podem ser carregados com [Import-AzContext](/powershell/module/az.accounts/import-azcontext):</span><span class="sxs-lookup"><span data-stu-id="6500c-157">Manually save contexts with [Save-AzContext](/powershell/module/az.accounts/save-azcontext) to be used in future PowerShell sessions, where they can be loaded with [Import-AzContext](/powershell/module/az.accounts/import-azcontext):</span></span>

  ```azurepowershell
  Save-AzContext -Path current-context.json # Save the current context
  Save-AzContext -Profile $profileObject -Path other-context.json # Save a context object
  Import-AzContext -Path other-context.json # Load the context from a file and set it to the current context
  ```

> [!WARNING]
> <span data-ttu-id="6500c-158">Desabilitar o salvamento automático de contexto __não__ limpa as informações de contexto armazenadas que foram salvas.</span><span class="sxs-lookup"><span data-stu-id="6500c-158">Disabling context autosave __doesn't__ clear any stored context information that was saved.</span></span> <span data-ttu-id="6500c-159">Para remover informações armazenadas, use o cmdlet [Clear-AzContext](/powershell/module/az.accounts/Clear-AzContext).</span><span class="sxs-lookup"><span data-stu-id="6500c-159">To remove stored information, use the [Clear-AzContext](/powershell/module/az.accounts/Clear-AzContext) cmdlet.</span></span> <span data-ttu-id="6500c-160">Para saber mais sobre como remover contextos salvos, confira [Remover contextos e credenciais](#remove-azure-contexts-and-stored-credentials).</span><span class="sxs-lookup"><span data-stu-id="6500c-160">For more on removing saved contexts, see [Remove contexts and credentials](#remove-azure-contexts-and-stored-credentials).</span></span>

<span data-ttu-id="6500c-161">Cada um desses comandos dá suporte ao parâmetro `-Scope`, que pode usar um valor de `Process` a ser aplicado apenas ao processo de execução atual.</span><span class="sxs-lookup"><span data-stu-id="6500c-161">Each of these commands supports the `-Scope` parameter, which can take a value of `Process` to only apply to the current running process.</span></span> <span data-ttu-id="6500c-162">Por exemplo, para garantir que contextos recém-criados não sejam salvos após sair de uma sessão do PowerShell:</span><span class="sxs-lookup"><span data-stu-id="6500c-162">For example, to ensure that newly created contexts aren't saved after exiting a PowerShell session:</span></span>

```azurepowershell-interactive
Disable-AzContextAutosave -Scope Process
$context2 = Set-AzContext -Subscription "sub-id" -Tenant "other-tenant"
```

<span data-ttu-id="6500c-163">As informações de contexto e tokens são armazenados no diretório `$env:USERPROFILE\.Azure` no Windows e no `$HOME/.Azure` em outras plataformas.</span><span class="sxs-lookup"><span data-stu-id="6500c-163">Context information and tokens are stored in the `$env:USERPROFILE\.Azure` directory on Windows, and on `$HOME/.Azure` on other platforms.</span></span> <span data-ttu-id="6500c-164">Informações confidenciais, como IDs de assinatura e IDs de locatário, ainda podem ser expostas em informações armazenadas, por meio de logs ou contextos salvos.</span><span class="sxs-lookup"><span data-stu-id="6500c-164">Sensitive information such as subscription IDs and tenant IDs may still be exposed in stored information, through logs or saved contexts.</span></span> <span data-ttu-id="6500c-165">Para saber como limpar informações armazenadas, confira a seção [Remover contextos e credenciais](#remove-azure-contexts-and-stored-credentials).</span><span class="sxs-lookup"><span data-stu-id="6500c-165">To learn how to clear stored information, see the [Remove contexts and credentials](#remove-azure-contexts-and-stored-credentials) section.</span></span>

## <a name="remove-azure-contexts-and-stored-credentials"></a><span data-ttu-id="6500c-166">Remover contextos e credenciais armazenadas do Azure</span><span class="sxs-lookup"><span data-stu-id="6500c-166">Remove Azure contexts and stored credentials</span></span>

<span data-ttu-id="6500c-167">Para limpar contextos e credenciais do Azure:</span><span class="sxs-lookup"><span data-stu-id="6500c-167">To clear Azure contexts and credentials:</span></span>

* <span data-ttu-id="6500c-168">Saia de uma conta com [Disconnect-AzAccount](/powershell/module/az.accounts/disconnect-azaccount).</span><span class="sxs-lookup"><span data-stu-id="6500c-168">Sign out of an account with [Disconnect-AzAccount](/powershell/module/az.accounts/disconnect-azaccount).</span></span>
  <span data-ttu-id="6500c-169">Você pode sair de qualquer conta por conta ou contexto:</span><span class="sxs-lookup"><span data-stu-id="6500c-169">You can sign out of any account either by account or context:</span></span>

  ```azurepowershell-interactive
  Disconnect-AzAccount # Disconnect active account 
  Disconnect-AzAccount -Username "user@contoso.com" # Disconnect by account name

  Disconnect-AzAccount -ContextName "subscription2" # Disconnect by context name
  Disconnect-AzAccount -AzureContext $contextObject # Disconnect using context object information
  ```

  <span data-ttu-id="6500c-170">A desconexão sempre remove tokens de autenticação armazenados e limpa contextos salvos associados ao usuário desconectado ou ao contexto.</span><span class="sxs-lookup"><span data-stu-id="6500c-170">Disconnecting always removes stored authentication tokens and clears saved contexts associated with the disconnected user or context.</span></span>
* <span data-ttu-id="6500c-171">Use [Clear-AzContext](/powershell/module/az.accounts/Clear-AzContext).</span><span class="sxs-lookup"><span data-stu-id="6500c-171">Use [Clear-AzContext](/powershell/module/az.accounts/Clear-AzContext).</span></span> <span data-ttu-id="6500c-172">Esse cmdlet tem a garantia de sempre remover contextos armazenados e tokens de autenticação e também desconectará você.</span><span class="sxs-lookup"><span data-stu-id="6500c-172">This cmdlet is guaranteed to always remove stored contexts and authentication tokens, and will also sign you out.</span></span>
* <span data-ttu-id="6500c-173">Remova um contexto com [Remove-AzContext](/powershell/module/az.accounts/remove-azcontext):</span><span class="sxs-lookup"><span data-stu-id="6500c-173">Remove a context with [Remove-AzContext](/powershell/module/az.accounts/remove-azcontext):</span></span>
  
  ```azurepowershell-interactive
  Remove-AzContext -Name "mycontext" # Remove by name
  Get-AzContext -Name "mycontext" | Remove-AzContext # Remove by piping Azure context object
  ```

  <span data-ttu-id="6500c-174">Se remover o contexto ativo, você será desconectado do Azure e precisará autenticar-se novamente com `Connect-AzAccount`.</span><span class="sxs-lookup"><span data-stu-id="6500c-174">If you remove the active context, you will be disconnected from Azure and need to reauthenticate with `Connect-AzAccount`.</span></span>

## <a name="see-also"></a><span data-ttu-id="6500c-175">Confira também</span><span class="sxs-lookup"><span data-stu-id="6500c-175">See also</span></span>

* [<span data-ttu-id="6500c-176">Executar cmdlets do Azure PowerShell nos Trabalhos do PowerShell</span><span class="sxs-lookup"><span data-stu-id="6500c-176">Run Azure PowerShell cmdlets in PowerShell Jobs</span></span>](using-psjobs.md)
* [<span data-ttu-id="6500c-177">Terminologia do Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="6500c-177">Azure Active Directory Terminology</span></span>](/azure/active-directory/fundamentals/active-directory-whatis#terminology)
* [<span data-ttu-id="6500c-178">Referência Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6500c-178">Az.Accounts reference</span></span>](/powershell/module/az.accounts)
