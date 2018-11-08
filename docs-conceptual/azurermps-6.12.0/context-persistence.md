---
title: Manter credenciais do usuário entre as sessões do PowerShell
description: Aprenda a reutilizar as credenciais do Azure e outras informações em várias sessões do PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/09/2018
ms.openlocfilehash: a07b5fe8cd532f99038d7f0ce10b3b891c896da1
ms.sourcegitcommit: 06f9206e025afa7207d4657c8f57c94ddb74817a
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/07/2018
ms.locfileid: "51212545"
---
# <a name="persist-user-credentials-across-powershell-sessions"></a><span data-ttu-id="35b3f-103">Manter credenciais do usuário entre as sessões do PowerShell</span><span class="sxs-lookup"><span data-stu-id="35b3f-103">Persist user credentials across PowerShell sessions</span></span>

<span data-ttu-id="35b3f-104">O Azure PowerShell oferece um recurso chamado **Salvamento Automático do contexto do Azure**, que oferece os seguintes recursos:</span><span class="sxs-lookup"><span data-stu-id="35b3f-104">Azure PowerShell offers a feature called **Azure Context Autosave**, which gives the following features:</span></span>

- <span data-ttu-id="35b3f-105">Retenção das informações de conexão para a reutilização em novas sessões do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="35b3f-105">Retention of sign-in information for reuse in new PowerShell sessions.</span></span>
- <span data-ttu-id="35b3f-106">Facilitar o uso de tarefas em segundo plano para executar os cmdlets de execução longa.</span><span class="sxs-lookup"><span data-stu-id="35b3f-106">Easier use of background tasks for executing long-running cmdlets.</span></span>
- <span data-ttu-id="35b3f-107">Alterne contas, assinaturas e ambientes sem usar credenciais separadas.</span><span class="sxs-lookup"><span data-stu-id="35b3f-107">Switch between accounts, subscriptions, and environments without a separate sign-in.</span></span>
- <span data-ttu-id="35b3f-108">Execução de tarefas usando credenciais e assinaturas diferentes, simultaneamente, a partir da mesma sessão do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="35b3f-108">Execution of tasks using different credentials and subscriptions, simultaneously, from the same PowerShell session.</span></span>

## <a name="azure-contexts-defined"></a><span data-ttu-id="35b3f-109">Contextos do Azure definidos</span><span class="sxs-lookup"><span data-stu-id="35b3f-109">Azure contexts defined</span></span>

<span data-ttu-id="35b3f-110">Um *contexto do Azure* é um conjunto de informações que define o destino de cmdlets do Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="35b3f-110">An *Azure context* is a set of information that defines the target of Azure PowerShell cmdlets.</span></span> <span data-ttu-id="35b3f-111">O contexto consiste em cinco partes:</span><span class="sxs-lookup"><span data-stu-id="35b3f-111">The context consists of five parts:</span></span>

- <span data-ttu-id="35b3f-112">Uma *Conta* - a entidade de serviço ou o nome de usuário usado para autenticar a comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="35b3f-112">An *Account* - the UserName or Service Principal used to authenticate communications with Azure</span></span>
- <span data-ttu-id="35b3f-113">Uma *Assinatura* - a assinatura do Azure com os recursos que estão sendo tratados.</span><span class="sxs-lookup"><span data-stu-id="35b3f-113">A *Subscription* - The Azure Subscription with the Resources being acted upon.</span></span>
- <span data-ttu-id="35b3f-114">Um *Locatário* - o locatário do Azure Active Directory que contém sua assinatura.</span><span class="sxs-lookup"><span data-stu-id="35b3f-114">A *Tenant* - The Azure Active Directory tenant that contains your subscription.</span></span> <span data-ttu-id="35b3f-115">Os Locatários são mais importantes para a autenticação ServicePrincipal.</span><span class="sxs-lookup"><span data-stu-id="35b3f-115">Tenants are more important to ServicePrincipal authentication.</span></span>
- <span data-ttu-id="35b3f-116">Um *Ambiente* - a nuvem de destino específica do Azure, normalmente a nuvem global do Azure.</span><span class="sxs-lookup"><span data-stu-id="35b3f-116">An *Environment* - The particular Azure Cloud being targeted, usually the Azure global Cloud.</span></span>
  <span data-ttu-id="35b3f-117">No entanto, a configuração do ambiente também permite usar nuvens nacionais, governamentais e locais (Azure Stack) como destino.</span><span class="sxs-lookup"><span data-stu-id="35b3f-117">However, the environment setting allows you to target National, Government, and on-premises (Azure Stack) clouds as well.</span></span>
- <span data-ttu-id="35b3f-118">*Credenciais* - as informações usadas pelo Azure para verificar sua identidade e confirmar sua autorização para acessar recursos no Azure</span><span class="sxs-lookup"><span data-stu-id="35b3f-118">*Credentials* - The information used by Azure to verify your identity and confirm your authorization to access resources in Azure</span></span>

<span data-ttu-id="35b3f-119">Em versões anteriores, um Contexto do Azure precisava ser criado sempre que você abria uma nova sessão do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="35b3f-119">In previous releases, an Azure Context had to be created each time you opened a new PowerShell session.</span></span> <span data-ttu-id="35b3f-120">A partir do Azure PowerShell v4.4.0, os Contextos do Azure podem ser salvos automaticamente sempre que uma nova sessão do PowerShell for aberta.</span><span class="sxs-lookup"><span data-stu-id="35b3f-120">Beginning with Azure PowerShell v4.4.0, Azure Contexts can automatically be saved whenever opening a new PowerShell session.</span></span>

## <a name="automatically-save-the-context-for-the-next-sign-in"></a><span data-ttu-id="35b3f-121">Salvar automaticamente o contexto para a próxima conexão</span><span class="sxs-lookup"><span data-stu-id="35b3f-121">Automatically save the context for the next sign-in</span></span>

<span data-ttu-id="35b3f-122">Nas versões 6.3.0 e posteriores, o Azure PowerShell retém suas informações do contexto automaticamente entre as sessões.</span><span class="sxs-lookup"><span data-stu-id="35b3f-122">In versions 6.3.0 and later, Azure PowerShell retains your context information automatically between sessions.</span></span> <span data-ttu-id="35b3f-123">Para configurar o PowerShell para esquecer o contexto e as credenciais, use `Disable-AzureRmContextAutoSave`.</span><span class="sxs-lookup"><span data-stu-id="35b3f-123">To set PowerShell to forget your context and credentials, use `Disable-AzureRmContextAutoSave`.</span></span> <span data-ttu-id="35b3f-124">Você precisará entrar no Azure sempre que abrir uma sessão do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="35b3f-124">You'll need to sign in to Azure every time you open a PowerShell session.</span></span>

<span data-ttu-id="35b3f-125">Para permitir que o Azure PowerShell se lembre do seu contexto depois que a sessão do PowerShell for fechada, use `Enable-AzureRmContextAutosave`.</span><span class="sxs-lookup"><span data-stu-id="35b3f-125">To allow Azure PowerShell to remember your context after the PowerShell session is closed, use `Enable-AzureRmContextAutosave`.</span></span> <span data-ttu-id="35b3f-126">As informações de contexto e as credenciais são salvas automaticamente em uma pasta oculta especial no diretório de usuário (`%AppData%\Roaming\Windows Azure PowerShell`).</span><span class="sxs-lookup"><span data-stu-id="35b3f-126">Context and credential information are automatically saved in a special hidden folder in your user directory (`%AppData%\Roaming\Windows Azure PowerShell`).</span></span>
<span data-ttu-id="35b3f-127">Cada nova sessão do PowerShell terá como alvo o contexto usado na última sessão.</span><span class="sxs-lookup"><span data-stu-id="35b3f-127">Each new PowerShell session targets the context used in your last session.</span></span>

<span data-ttu-id="35b3f-128">Os cmdlets que permitem gerenciar contextos do Azure também permitem um controle refinado.</span><span class="sxs-lookup"><span data-stu-id="35b3f-128">The cmdlets that allow you to manage Azure contexts also allow you fine grained control.</span></span> <span data-ttu-id="35b3f-129">Se quiser que as alterações sejam aplicadas somente à sessão atual do PowerShell (escopo `Process`) ou em cada sessão do PowerShell (escopo `CurrentUser`).</span><span class="sxs-lookup"><span data-stu-id="35b3f-129">If you want changes to apply only to the current PowerShell session (`Process` scope) or every PowerShell session (`CurrentUser` scope).</span></span> <span data-ttu-id="35b3f-130">Essas opções são discutidas em detalhes em [Usar Escopos de Contexto](#Using-Context-Scopes).</span><span class="sxs-lookup"><span data-stu-id="35b3f-130">These options are discussed in mode detail in [Using Context Scopes](#Using-Context-Scopes).</span></span>

## <a name="running-azure-powershell-cmdlets-as-background-jobs"></a><span data-ttu-id="35b3f-131">Executar os cmdlets do Azure PowerShell como trabalhos em segundo plano</span><span class="sxs-lookup"><span data-stu-id="35b3f-131">Running Azure PowerShell cmdlets as background jobs</span></span>

<span data-ttu-id="35b3f-132">O recurso de **Salvamento Automático de Contexto do Azure** também permite compartilhar seu contexto com trabalhos em segundo plano do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="35b3f-132">The **Azure Context Autosave** feature also allows you to share you context with PowerShell background jobs.</span></span> <span data-ttu-id="35b3f-133">O PowerShell permite iniciar e monitorar tarefas de execução longa como trabalhos em segundo plano sem a necessidade de aguardar a conclusão das tarefas.</span><span class="sxs-lookup"><span data-stu-id="35b3f-133">PowerShell allows you to start and monitor long-executing tasks as background jobs without having to wait for the tasks to complete.</span></span> <span data-ttu-id="35b3f-134">Você pode compartilhar as credenciais com trabalhos em segundo plano de duas maneiras diferentes:</span><span class="sxs-lookup"><span data-stu-id="35b3f-134">You can share credentials with background jobs in two different ways:</span></span>

- <span data-ttu-id="35b3f-135">Transmitir o contexto como um argumento</span><span class="sxs-lookup"><span data-stu-id="35b3f-135">Passing the context as an argument</span></span>

  <span data-ttu-id="35b3f-136">A maioria dos cmdlets do AzureRM permite passar o contexto como um parâmetro para o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35b3f-136">Most AzureRM cmdlets allow you to pass the context as a parameter to the cmdlet.</span></span> <span data-ttu-id="35b3f-137">Você pode passar um contexto para um trabalho em segundo plano, conforme mostrado no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="35b3f-137">You can pass a context to a background job as shown in the following example:</span></span>

  ```powershell-interactive
  PS C:\> $job = Start-Job { param ($ctx) New-AzureRmVm -AzureRmContext $ctx [... Additional parameters ...]} -ArgumentList (Get-AzureRmContext)
  ```

- <span data-ttu-id="35b3f-138">Usando o contexto padrão com Salvamento Automático habilitado</span><span class="sxs-lookup"><span data-stu-id="35b3f-138">Using the default context with Autosave enabled</span></span>

  <span data-ttu-id="35b3f-139">Se você tiver habilitado o **Salvamento Automático de Contexto**, os trabalhos em segundo plano automaticamente usarão o contexto padrão salvo.</span><span class="sxs-lookup"><span data-stu-id="35b3f-139">If you have enabled **Context Autosave**, background jobs automatically use the default saved context.</span></span>

  ```powershell-interactive
  PS C:\> $job = Start-Job { New-AzureRmVm [... Additional parameters ...]}
  ```

<span data-ttu-id="35b3f-140">Quando precisar saber o resultado da tarefa em segundo plano, use `Get-Job` para verificar o status do trabalho e `Wait-Job` para aguardar a conclusão do trabalho.</span><span class="sxs-lookup"><span data-stu-id="35b3f-140">When you need to know the outcome of the background task, use `Get-Job` to check the job status and `Wait-Job` to wait for the Job to complete.</span></span> <span data-ttu-id="35b3f-141">Use `Receive-Job` para capturar ou exibir a saída do trabalho em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="35b3f-141">Use `Receive-Job` to capture or display the output of the background job.</span></span> <span data-ttu-id="35b3f-142">Para obter mais informações, consulte [about_Jobs](/powershell/module/microsoft.powershell.core/about/about_jobs).</span><span class="sxs-lookup"><span data-stu-id="35b3f-142">For more information, see [about_Jobs](/powershell/module/microsoft.powershell.core/about/about_jobs).</span></span>

## <a name="creating-selecting-renaming-and-removing-contexts"></a><span data-ttu-id="35b3f-143">Criando, selecionando, renomeando e removendo contextos</span><span class="sxs-lookup"><span data-stu-id="35b3f-143">Creating, selecting, renaming, and removing contexts</span></span>

<span data-ttu-id="35b3f-144">Para criar um contexto, você deve entrar no Azure.</span><span class="sxs-lookup"><span data-stu-id="35b3f-144">To create a context, you must be signed in to Azure.</span></span> <span data-ttu-id="35b3f-145">O cmdlet `Connect-AzureRmAccount` (ou seu alias, `Login-AzureRmAccount`) define o contexto padrão usado pelos cmdlets do Azure PowerShell e deixa que você acesse qualquer locatário ou assinatura permitida por suas credenciais.</span><span class="sxs-lookup"><span data-stu-id="35b3f-145">The `Connect-AzureRmAccount` cmdlet (or its alias, `Login-AzureRmAccount`) sets the default context used by Azure PowerShell cmdlets, and allows you to access any tenants or subscriptions allowed by your credentials.</span></span>

<span data-ttu-id="35b3f-146">Para adicionar um novo contexto após a conexão, use `Set-AzureRmContext` (ou seu alias, `Select-AzureRmSubscription`).</span><span class="sxs-lookup"><span data-stu-id="35b3f-146">To add a new context after sign-in, use `Set-AzureRmContext` (or its alias, `Select-AzureRmSubscription`).</span></span>

```azurepowershell-interactive
PS C:\> Set-AzureRMContext -Subscription "Contoso Subscription 1" -Name "Contoso1"
```

<span data-ttu-id="35b3f-147">O exemplo anterior adiciona um novo contexto com 'Assinatura Contoso 1' como destino usando suas credenciais atuais.</span><span class="sxs-lookup"><span data-stu-id="35b3f-147">The previous example adds a new context targeting 'Contoso Subscription 1' using your current credentials.</span></span> <span data-ttu-id="35b3f-148">O novo contexto é denominado 'Contoso1'.</span><span class="sxs-lookup"><span data-stu-id="35b3f-148">The new context is named 'Contoso1'.</span></span> <span data-ttu-id="35b3f-149">Se você não fornecer um nome para o contexto, será usado um nome padrão usando a ID da conta e a ID da assinatura.</span><span class="sxs-lookup"><span data-stu-id="35b3f-149">If you don't provide a name for the context, a default name, using the account ID and subscription ID is used.</span></span>

<span data-ttu-id="35b3f-150">Para renomear um contexto já existente, use o cmdlet `Rename-AzureRmContext`.</span><span class="sxs-lookup"><span data-stu-id="35b3f-150">To rename an existing context, use the `Rename-AzureRmContext` cmdlet.</span></span> <span data-ttu-id="35b3f-151">Por exemplo: </span><span class="sxs-lookup"><span data-stu-id="35b3f-151">For example:</span></span>

```azurepowershell-interactive
PS C:\> Rename-AzureRmContext '[user1@contoso.org; 123456-7890-1234-564321]` 'Contoso2'
```

<span data-ttu-id="35b3f-152">Este exemplo renomeia o contexto com o nome automático `[user1@contoso.org; 123456-7890-1234-564321]` por um nome simples nome 'Contoso2'.</span><span class="sxs-lookup"><span data-stu-id="35b3f-152">This example renames the context with automatic name `[user1@contoso.org; 123456-7890-1234-564321]` to the simple name 'Contoso2'.</span></span> <span data-ttu-id="35b3f-153">Os cmdlets que gerenciam contextos também usam o preenchimento de guia e isso permite escolher rapidamente o contexto.</span><span class="sxs-lookup"><span data-stu-id="35b3f-153">Cmdlets that manage contexts also use tab completion, allowing you to quickly select the context.</span></span>

<span data-ttu-id="35b3f-154">E, por último, para remover um contexto, use o cmdlet `Remove-AzureRmContext`.</span><span class="sxs-lookup"><span data-stu-id="35b3f-154">Finally, to remove a context, use the `Remove-AzureRmContext` cmdlet.</span></span>  <span data-ttu-id="35b3f-155">Por exemplo: </span><span class="sxs-lookup"><span data-stu-id="35b3f-155">For example:</span></span>

```azurepowershell-interactive
PS C:\> Remove-AzureRmContext Contoso2
```

<span data-ttu-id="35b3f-156">Você se esquece do contexto que foi nomeado 'Contoso2'.</span><span class="sxs-lookup"><span data-stu-id="35b3f-156">Forgets the context that was named 'Contoso2'.</span></span> <span data-ttu-id="35b3f-157">É possível recriar este contexto usando `Set-AzureRmContext`</span><span class="sxs-lookup"><span data-stu-id="35b3f-157">You can recreate this context using `Set-AzureRmContext`</span></span>

## <a name="removing-credentials"></a><span data-ttu-id="35b3f-158">Removendo credenciais</span><span class="sxs-lookup"><span data-stu-id="35b3f-158">Removing credentials</span></span>

<span data-ttu-id="35b3f-159">Você pode remover todas as credenciais e contextos associados de um usuário ou entidade de serviço usando `Disconnect-AzureRmAccount` (também conhecido como `Logout-AzureRmAccount`).</span><span class="sxs-lookup"><span data-stu-id="35b3f-159">You can remove all credentials and associated contexts for a user or service principal using `Disconnect-AzureRmAccount` (also known as `Logout-AzureRmAccount`).</span></span> <span data-ttu-id="35b3f-160">Quando executado sem parâmetros, o cmdlet `Disconnect-AzureRmAccount` remove todas as credenciais e contextos associados ao usuário ou entidade de serviço no contexto atual.</span><span class="sxs-lookup"><span data-stu-id="35b3f-160">When executed without parameters, the `Disconnect-AzureRmAccount` cmdlet removes all credentials and contexts associated with the User or Service Principal in the current context.</span></span> <span data-ttu-id="35b3f-161">Você pode passar um Nome de Usuário, o Nome da Entidade de Serviço ou o Contexto para uma determinada entidade de destino.</span><span class="sxs-lookup"><span data-stu-id="35b3f-161">You may pass in a Username, Service Principal Name, or context to target a particular principal.</span></span>

```azurepowershell-interactive
Disconnect-AzureRmAccount user1@contoso.org
```

## <a name="using-context-scopes"></a><span data-ttu-id="35b3f-162">Usando escopos de contexto</span><span class="sxs-lookup"><span data-stu-id="35b3f-162">Using context scopes</span></span>

<span data-ttu-id="35b3f-163">Ocasionalmente, convém selecionar, alterar ou remover um contexto em uma sessão do PowerShell sem afetar outras sessões.</span><span class="sxs-lookup"><span data-stu-id="35b3f-163">Occasionally, you may want to select, change, or remove a context in a PowerShell session without impacting other sessions.</span></span> <span data-ttu-id="35b3f-164">Para alterar o comportamento padrão dos cmdlets de contexto, use o parâmetro `Scope`.</span><span class="sxs-lookup"><span data-stu-id="35b3f-164">To change the default behavior of context cmdlets, use the `Scope` parameter.</span></span> <span data-ttu-id="35b3f-165">O escopo `Process` substitui o comportamento padrão aplicando-o apenas à sessão atual.</span><span class="sxs-lookup"><span data-stu-id="35b3f-165">The `Process` scope overrides the default behavior by making it apply only for the current session.</span></span> <span data-ttu-id="35b3f-166">Por outro lado, o escopo `CurrentUser` altera o contexto em todas as sessões, em vez de apenas a sessão atual.</span><span class="sxs-lookup"><span data-stu-id="35b3f-166">Conversely `CurrentUser` scope changes the context in all sessions, instead of just the current session.</span></span>

<span data-ttu-id="35b3f-167">Por exemplo, para alterar o contexto padrão na sessão atual do PowerShell sem afetar outras janelas ou o contexto usado na próxima vez em que uma sessão for aberta, use:</span><span class="sxs-lookup"><span data-stu-id="35b3f-167">As an example, to change the default context in the current PowerShell session without impacting other windows, or the context used the next time a session is opened, use:</span></span>

```azurepowershell-interactive
PS C:\> Select-AzureRmContext Contoso1 -Scope Process
```

## <a name="how-the-context-autosave-setting-is-remembered"></a><span data-ttu-id="35b3f-168">Como a configuração de salvamento automático de contexto é lembrada</span><span class="sxs-lookup"><span data-stu-id="35b3f-168">How the context autosave setting is remembered</span></span>

<span data-ttu-id="35b3f-169">A configuração de Salvamento Automático de contexto é salva no diretório do usuário do Azure PowerShell (`%AppData%\Roaming\Windows Azure PowerShell`).</span><span class="sxs-lookup"><span data-stu-id="35b3f-169">The context AutoSave setting is saved to the user Azure PowerShell directory (`%AppData%\Roaming\Windows Azure PowerShell`).</span></span> <span data-ttu-id="35b3f-170">Alguns tipos de contas de computador podem não ter acesso a esse diretório.</span><span class="sxs-lookup"><span data-stu-id="35b3f-170">Some kinds of computer accounts may not have access to this directory.</span></span> <span data-ttu-id="35b3f-171">Para esses cenários, você pode usar a variável de ambiente</span><span class="sxs-lookup"><span data-stu-id="35b3f-171">For such scenarios, you can use the environment variable</span></span>

```azurepowershell-interactive
$env:AzureRmContextAutoSave="true" | "false"
```

<span data-ttu-id="35b3f-172">Quando definido como “true”, o contexto é salvo automaticamente.</span><span class="sxs-lookup"><span data-stu-id="35b3f-172">When set to 'true', the context is automatically saved.</span></span> <span data-ttu-id="35b3f-173">Se definido como “false”, o contexto não é salvo.</span><span class="sxs-lookup"><span data-stu-id="35b3f-173">If set to 'false', the context isn't saved.</span></span>

## <a name="changes-to-the-azurermprofile-module"></a><span data-ttu-id="35b3f-174">Alterações no módulo AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="35b3f-174">Changes to the AzureRM.Profile module</span></span>

<span data-ttu-id="35b3f-175">Novos cmdlets para gerenciar contextos</span><span class="sxs-lookup"><span data-stu-id="35b3f-175">New cmdlets for managing context</span></span>

- <span data-ttu-id="35b3f-176">[Enable-AzureRmContextAutosave][enable] - Permite salvar o contexto entre sessões do Powershell.</span><span class="sxs-lookup"><span data-stu-id="35b3f-176">[Enable-AzureRmContextAutosave][enable] - Allow saving the context between powershell sessions.</span></span>
  <span data-ttu-id="35b3f-177">Qualquer alteração feita afetará o contexto global.</span><span class="sxs-lookup"><span data-stu-id="35b3f-177">Any changes alter the global context.</span></span>
- <span data-ttu-id="35b3f-178">[Disable-AzureRmContextAutosave][disable] - Desativa o salvamento automático do contexto.</span><span class="sxs-lookup"><span data-stu-id="35b3f-178">[Disable-AzureRmContextAutosave][disable] - Turn off autosaving the context.</span></span> <span data-ttu-id="35b3f-179">É necessário entrar novamente em cada nova sessão do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="35b3f-179">Each new PowerShell session is required to sign in again.</span></span>
- <span data-ttu-id="35b3f-180">[Select-AzureRmContext][select] - Seleciona um contexto como o padrão.</span><span class="sxs-lookup"><span data-stu-id="35b3f-180">[Select-AzureRmContext][select] - Select a context as the default.</span></span> <span data-ttu-id="35b3f-181">Todos os cmdlets usam as credenciais neste contexto para autenticação.</span><span class="sxs-lookup"><span data-stu-id="35b3f-181">All cmdlets use the credentials in this context for authentication.</span></span>
- <span data-ttu-id="35b3f-182">[Disconnect-AzureRmAccount][remove-cred] - Remove todas as credenciais e contextos associados a uma conta.</span><span class="sxs-lookup"><span data-stu-id="35b3f-182">[Disconnect-AzureRmAccount][remove-cred] - Remove all credentials and contexts associated with an account.</span></span>
- <span data-ttu-id="35b3f-183">[Remove-AzureRmContext][remove-context] - Remove um contexto nomeado.</span><span class="sxs-lookup"><span data-stu-id="35b3f-183">[Remove-AzureRmContext][remove-context] - Remove a named context.</span></span>
- <span data-ttu-id="35b3f-184">[Rename-AzureRmContext][rename] - Renomeia um contexto existente.</span><span class="sxs-lookup"><span data-stu-id="35b3f-184">[Rename-AzureRmContext][rename] - Rename an existing context.</span></span>

<span data-ttu-id="35b3f-185">Alterações em cmdlets de perfil existentes</span><span class="sxs-lookup"><span data-stu-id="35b3f-185">Changes to existing profile cmdlets</span></span>

- <span data-ttu-id="35b3f-186">[Add-AzureRmAccount][login] - Permite o escopo da conexão para o processo ou o usuário atual.</span><span class="sxs-lookup"><span data-stu-id="35b3f-186">[Add-AzureRmAccount][login] - Allow scoping of the sign-in to the process or the current user.</span></span>
  <span data-ttu-id="35b3f-187">Permite nomear o contexto padrão após a autenticação.</span><span class="sxs-lookup"><span data-stu-id="35b3f-187">Allow naming the default context after authentication.</span></span>
- <span data-ttu-id="35b3f-188">[Import-AzureRmContext][import] - Permite o escopo da conexão para o processo ou o usuário atual.</span><span class="sxs-lookup"><span data-stu-id="35b3f-188">[Import-AzureRmContext][import] - Allow scoping of the sign-in to the process or the current user.</span></span>
- <span data-ttu-id="35b3f-189">[Set-AzureRmContext][set-context] - Permite a seleção de contextos nomeados existentes e alterações no escopo do processo ou do usuário atual.</span><span class="sxs-lookup"><span data-stu-id="35b3f-189">[Set-AzureRmContext][set-context] - Allow selection of existing named contexts, and scope changes to the process or current user.</span></span>

<!-- Hyperlinks -->
[enable]: /powershell/module/azurerm.profile/Enable-AzureRmContextAutosave
[disable]: /powershell/module/azurerm.profile/Disable-AzureRmContextAutosave
[select]: /powershell/module/azurerm.profile/Select-AzureRmContext
[remove-cred]: /powershell/module/azurerm.profile/Disconnect-AzureRmAccount
[remove-context]: /powershell/module/azurerm.profile/Remove-AzureRmContext
[rename]: /powershell/module/azurerm.profile/Rename-AzureRmContext

<!-- Updated cmdlets -->
[login]: /powershell/module/azurerm.profile/Connect-AzureRmAccount
[import]:  /powershell/module/azurerm.profile/Import-AzureRmContext
[set-context]: /powershell/module/azurerm.profile/Set-AzureRmContext
