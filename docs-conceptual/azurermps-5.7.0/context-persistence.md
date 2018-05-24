---
title: Persistência de logons de usuário nas sessões do PowerShell
description: Este artigo explica os novos recursos no Azure PowerShell que permitem a reutilização de credenciais e outras informações do usuário em várias sessões do PowerShell.
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 08/31/2017
ms.openlocfilehash: e086ce919b4cdd14a8cc7527aa62bfd9ce09628a
ms.sourcegitcommit: 5971c92cb023bdd1d71fa2ad0a3b378abfbd092a
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/23/2018
---
# <a name="persisting-user-logins-across-powershell-sessions"></a><span data-ttu-id="debe1-103">Persistência de logons de usuário nas sessões do PowerShell</span><span class="sxs-lookup"><span data-stu-id="debe1-103">Persisting user logins across PowerShell sessions</span></span>

<span data-ttu-id="debe1-104">Na versão de setembro de 2017 do Azure PowerShell, os cmdlets do Azure Resource Manager apresentam um novo recurso, **Salvamento Automático de Contexto do Azure**.</span><span class="sxs-lookup"><span data-stu-id="debe1-104">In the September 2017 release of Azure PowerShell, Azure Resource Manager cmdlets introduce a new feature, **Azure Context Autosave**.</span></span> <span data-ttu-id="debe1-105">Esse recurso permite vários novos cenários de usuário, incluindo:</span><span class="sxs-lookup"><span data-stu-id="debe1-105">This feature enables several new user scenarios, including:</span></span>

- <span data-ttu-id="debe1-106">Retenção de informações de logon para reutilização em novas sessões do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="debe1-106">Retention of login information for reuse in new PowerShell sessions.</span></span>
- <span data-ttu-id="debe1-107">Facilitar o uso de tarefas em segundo plano para executar os cmdlets de execução longa.</span><span class="sxs-lookup"><span data-stu-id="debe1-107">Easier use of background tasks for executing long-running cmdlets.</span></span>
- <span data-ttu-id="debe1-108">Alternar entre contas, assinaturas e ambientes sem um logon separado.</span><span class="sxs-lookup"><span data-stu-id="debe1-108">Switch between accounts, subscriptions, and environments without a separate login.</span></span>
- <span data-ttu-id="debe1-109">Execução de tarefas usando credenciais e assinaturas diferentes, simultaneamente, a partir da mesma sessão do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="debe1-109">Execution of tasks using different credentials and subscriptions, simultaneously, from the same PowerShell session.</span></span>

## <a name="azure-contexts-defined"></a><span data-ttu-id="debe1-110">Contextos do Azure definidos</span><span class="sxs-lookup"><span data-stu-id="debe1-110">Azure contexts defined</span></span>

<span data-ttu-id="debe1-111">Um *contexto do Azure* é um conjunto de informações que define o destino de cmdlets do Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="debe1-111">An *Azure context* is a set of information that defines the target of Azure PowerShell cmdlets.</span></span> <span data-ttu-id="debe1-112">O contexto consiste em cinco partes:</span><span class="sxs-lookup"><span data-stu-id="debe1-112">The context consists of five parts:</span></span>

- <span data-ttu-id="debe1-113">Uma *Conta* - a entidade de serviço ou o nome de usuário usado para autenticar a comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="debe1-113">An *Account* - the UserName or Service Principal used to authenticate communications with Azure</span></span>
- <span data-ttu-id="debe1-114">Uma *Assinatura* - a assinatura do Azure que contém os recursos que estão sendo tratados.</span><span class="sxs-lookup"><span data-stu-id="debe1-114">A *Subscription* - The Azure Subscription containing the Resources being acted upon.</span></span>
- <span data-ttu-id="debe1-115">Um *Locatário* - o locatário do Azure Active Directory que contém sua assinatura.</span><span class="sxs-lookup"><span data-stu-id="debe1-115">A *Tenant* - The Azure Active Directory tenant that contains your subscription.</span></span> <span data-ttu-id="debe1-116">Os Locatários são mais importantes para a autenticação ServicePrincipal.</span><span class="sxs-lookup"><span data-stu-id="debe1-116">Tenants are more important to ServicePrincipal authentication.</span></span>
- <span data-ttu-id="debe1-117">Um *Ambiente* - a nuvem de destino específica do Azure, normalmente a nuvem global do Azure.</span><span class="sxs-lookup"><span data-stu-id="debe1-117">An *Environment* - The particular Azure Cloud being targeted, usually the Azure global Cloud.</span></span>
  <span data-ttu-id="debe1-118">No entanto, a configuração do ambiente também permite usar nuvens nacionais, governamentais e locais (Azure Stack) como destino.</span><span class="sxs-lookup"><span data-stu-id="debe1-118">However, the environment setting allows you to target National, Government, and on-premises (Azure Stack) clouds as well.</span></span>
- <span data-ttu-id="debe1-119">*Credenciais* - as informações usadas pelo Azure para verificar sua identidade e certificar-se de sua autorização para acessar recursos no Azure</span><span class="sxs-lookup"><span data-stu-id="debe1-119">*Credentials* - The information used by Azure to verify your identity and ensure your authorization to access resources in Azure</span></span>

<span data-ttu-id="debe1-120">Em versões anteriores, o Contexto do Azure precisava ser criado sempre que você abria uma nova sessão do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="debe1-120">In previous releases, your Azure Context had to be created each time you opened a new PowerShell session.</span></span> <span data-ttu-id="debe1-121">A partir do Azure PowerShell v4.4.0, passou a ser possível habilitar o salvamento automático e a reutilização de Contextos do Azure sempre que você abrir uma nova sessão do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="debe1-121">Beginning with Azure PowerShell v4.4.0, you can enable the automatic saving and reuse of Azure Contexts whenever you open a new PowerShell session.</span></span>

## <a name="automatically-saving-the-context-for-the-next-login"></a><span data-ttu-id="debe1-122">Salvar automaticamente o contexto para o próximo logon</span><span class="sxs-lookup"><span data-stu-id="debe1-122">Automatically saving the context for the next login</span></span>

<span data-ttu-id="debe1-123">Por padrão, o Azure PowerShell descarta suas informações de contexto sempre que você fechar a sessão do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="debe1-123">By default, Azure PowerShell discards your context information whenever you close the PowerShell session.</span></span>

<span data-ttu-id="debe1-124">Para permitir que o Azure PowerShell se lembre do seu contexto depois que a sessão do PowerShell for fechada, use `Enable-AzureRmContextAutosave`.</span><span class="sxs-lookup"><span data-stu-id="debe1-124">To allow Azure PowerShell to remember your context after the PowerShell session is closed, use `Enable-AzureRmContextAutosave`.</span></span> <span data-ttu-id="debe1-125">As informações de contexto e as credenciais são salvas automaticamente em uma pasta oculta especial no diretório de usuário (`%AppData%\Roaming\Windows Azure PowerShell`).</span><span class="sxs-lookup"><span data-stu-id="debe1-125">Context and credential information are automatically saved in a special hidden folder in your user directory (`%AppData%\Roaming\Windows Azure PowerShell`).</span></span>
<span data-ttu-id="debe1-126">Posteriormente, cada nova sessão do PowerShell terá como alvo o contexto usado na última sessão.</span><span class="sxs-lookup"><span data-stu-id="debe1-126">Subsequently, each new PowerShell session targets the context used in your last session.</span></span>

<span data-ttu-id="debe1-127">Para configurar o PowerShell para esquecer o contexto e as credenciais, use `Disable-AzureRmContextAutoSave`.</span><span class="sxs-lookup"><span data-stu-id="debe1-127">To set PowerShell to forget your context and credentials, use `Disable-AzureRmContextAutoSave`.</span></span> <span data-ttu-id="debe1-128">Você precisará fazer logon no Azure sempre que abrir uma sessão do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="debe1-128">You will need to log in to Azure every time you open a PowerShell session.</span></span>

<span data-ttu-id="debe1-129">Os cmdlets que permitem gerenciar contextos do Azure também permitem um controle refinado.</span><span class="sxs-lookup"><span data-stu-id="debe1-129">The cmdlets that allow you to manage Azure contexts also allow you fine grained control.</span></span> <span data-ttu-id="debe1-130">Se quiser que as alterações sejam aplicadas somente à sessão atual do PowerShell (escopo `Process`) ou em cada sessão do PowerShell (escopo `CurrentUser`).</span><span class="sxs-lookup"><span data-stu-id="debe1-130">If you want changes to apply only to the current PowerShell session (`Process` scope) or every PowerShell session (`CurrentUser` scope).</span></span> <span data-ttu-id="debe1-131">Essas opções são discutidas em detalhes em [Usar Escopos de Contexto](#Using-Context-Scopes).</span><span class="sxs-lookup"><span data-stu-id="debe1-131">These options are discussed in mode detail in [Using Context Scopes](#Using-Context-Scopes).</span></span>

## <a name="running-azure-powershell-cmdlets-as-background-jobs"></a><span data-ttu-id="debe1-132">Executar os cmdlets do Azure PowerShell como trabalhos em segundo plano</span><span class="sxs-lookup"><span data-stu-id="debe1-132">Running Azure PowerShell cmdlets as background jobs</span></span>

<span data-ttu-id="debe1-133">O recurso de **Salvamento Automático de Contexto do Azure** também permite compartilhar seu contexto com trabalhos em segundo plano do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="debe1-133">The **Azure Context Autosave** feature also allows you to share you context with PowerShell background jobs.</span></span> <span data-ttu-id="debe1-134">O PowerShell permite iniciar e monitorar tarefas de execução longa como trabalhos em segundo plano sem a necessidade de aguardar a conclusão das tarefas.</span><span class="sxs-lookup"><span data-stu-id="debe1-134">PowerShell allows you to start and monitor long-executing tasks as background jobs without having to wait for the tasks to complete.</span></span> <span data-ttu-id="debe1-135">Você pode compartilhar as credenciais com trabalhos em segundo plano de duas maneiras diferentes:</span><span class="sxs-lookup"><span data-stu-id="debe1-135">You can share credentials with background jobs in two different ways:</span></span>

- <span data-ttu-id="debe1-136">Transmitir o contexto como um argumento</span><span class="sxs-lookup"><span data-stu-id="debe1-136">Passing the context as an argument</span></span>

  <span data-ttu-id="debe1-137">A maioria dos cmdlets do AzureRM permite passar o contexto como um parâmetro para o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="debe1-137">Most AzureRM cmdlets allow you to pass the context as a parameter to the cmdlet.</span></span> <span data-ttu-id="debe1-138">Você pode passar um contexto para um trabalho em segundo plano, conforme mostrado no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="debe1-138">You can pass a context to a background job as shown in the following example:</span></span>

  ```powershell
  PS C:\> $job = Start-Job { param ($ctx) New-AzureRmVm -AzureRmContext $ctx [... Additional parameters ...]} -ArgumentList (Get-AzureRmContext)
  ```

- <span data-ttu-id="debe1-139">Usando o contexto padrão com Salvamento Automático habilitado</span><span class="sxs-lookup"><span data-stu-id="debe1-139">Using the default context with Autosave enabled</span></span>

  <span data-ttu-id="debe1-140">Se você tiver habilitado o **Salvamento Automático de Contexto**, os trabalhos em segundo plano automaticamente usarão o contexto padrão salvo.</span><span class="sxs-lookup"><span data-stu-id="debe1-140">If you have enabled **Context Autosave**, background jobs automatically use the default saved context.</span></span>

  ```powershell
  PS C:\> $job = Start-Job { New-AzureRmVm [... Additional parameters ...]}
  ```

<span data-ttu-id="debe1-141">Quando precisar saber o resultado da tarefa em segundo plano, use `Get-Job` para verificar o status do trabalho e `Wait-Job` para aguardar a conclusão do trabalho.</span><span class="sxs-lookup"><span data-stu-id="debe1-141">When you need to know the outcome of the background task, use `Get-Job` to check the job status and `Wait-Job` to wait for the Job to complete.</span></span> <span data-ttu-id="debe1-142">Use `Receive-Job` para capturar ou exibir a saída do trabalho em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="debe1-142">Use `Receive-Job` to capture or display the output of the background job.</span></span> <span data-ttu-id="debe1-143">Para obter mais informações, consulte [about_Jobs](/powershell/module/microsoft.powershell.core/about/about_jobs).</span><span class="sxs-lookup"><span data-stu-id="debe1-143">For more information, see [about_Jobs](/powershell/module/microsoft.powershell.core/about/about_jobs).</span></span>

## <a name="creating-selecting-renaming-and-removing-contexts"></a><span data-ttu-id="debe1-144">Criando, selecionando, renomeando e removendo contextos</span><span class="sxs-lookup"><span data-stu-id="debe1-144">Creating, selecting, renaming, and removing contexts</span></span>

<span data-ttu-id="debe1-145">Para criar um contexto, você deve estar conectado ao Azure.</span><span class="sxs-lookup"><span data-stu-id="debe1-145">To create a context, you must be logged in to Azure.</span></span> <span data-ttu-id="debe1-146">O cmdlet `Connect-AzureRmAccount` (ou seu alias, `Login-AzureRmAccount`) define o contexto padrão usado pelos cmdlets do Azure PowerShell posteriores e permite que você acesse qualquer assinatura ou locatário permitido por suas credenciais de logon.</span><span class="sxs-lookup"><span data-stu-id="debe1-146">The `Connect-AzureRmAccount` cmdlet (or its alias, `Login-AzureRmAccount`) sets the default context used by subsequent Azure PowerShell cmdlets, and allows you to access any tenants or subscriptions allowed by your login credentials.</span></span>

<span data-ttu-id="debe1-147">Para adicionar um novo contexto após o logon, use `Set-AzureRmContext` (ou seu alias, `Select-AzureRmSubscription`).</span><span class="sxs-lookup"><span data-stu-id="debe1-147">To add a new context after login, use `Set-AzureRmContext` (or its alias, `Select-AzureRmSubscription`).</span></span>

```powershell
PS C:\> Set-AzureRMContext -Subscription "Contoso Subscription 1" -Name "Contoso1"
```

<span data-ttu-id="debe1-148">O exemplo anterior adiciona um novo contexto com 'Assinatura Contoso 1' como destino usando suas credenciais atuais.</span><span class="sxs-lookup"><span data-stu-id="debe1-148">The previous example adds a new context targeting 'Contoso Subscription 1' using your current credentials.</span></span> <span data-ttu-id="debe1-149">O novo contexto é denominado 'Contoso1'.</span><span class="sxs-lookup"><span data-stu-id="debe1-149">The new context is named 'Contoso1'.</span></span> <span data-ttu-id="debe1-150">Se você não fornecer um nome para o contexto, um nome padrão, usando a ID da conta e a ID da assinatura será usado.</span><span class="sxs-lookup"><span data-stu-id="debe1-150">If you do not provide a name for the context, a default name, using the account ID and subscription ID is used.</span></span>

<span data-ttu-id="debe1-151">Para renomear um contexto já existente, use o cmdlet `Rename-AzureRmContext`.</span><span class="sxs-lookup"><span data-stu-id="debe1-151">To rename an existing context, use the `Rename-AzureRmContext` cmdlet.</span></span> <span data-ttu-id="debe1-152">Por exemplo: </span><span class="sxs-lookup"><span data-stu-id="debe1-152">For example:</span></span>

```powershell
PS C:\> Rename-AzureRmContext '[user1@contoso.org; 123456-7890-1234-564321]` 'Contoso2'
```

<span data-ttu-id="debe1-153">Este exemplo renomeia o contexto com o nome automático `[user1@contoso.org; 123456-7890-1234-564321]` por um nome simples nome 'Contoso2'.</span><span class="sxs-lookup"><span data-stu-id="debe1-153">This example renames the context with automatic name `[user1@contoso.org; 123456-7890-1234-564321]` to the simple name 'Contoso2'.</span></span> <span data-ttu-id="debe1-154">Os cmdlets que gerenciam contextos também usam o preenchimento de guia e isso permite escolher rapidamente o contexto.</span><span class="sxs-lookup"><span data-stu-id="debe1-154">Cmdlets that manage contexts also use tab completion, allowing you to quickly select the context.</span></span>

<span data-ttu-id="debe1-155">E, por último, para remover um contexto, use o cmdlet `Remove-AzureRmContext`.</span><span class="sxs-lookup"><span data-stu-id="debe1-155">Finally, to remove a context, use the `Remove-AzureRmContext` cmdlet.</span></span>  <span data-ttu-id="debe1-156">Por exemplo: </span><span class="sxs-lookup"><span data-stu-id="debe1-156">For example:</span></span>

```powershell
PS C:\> Remove-AzureRmContext Contoso2
```

<span data-ttu-id="debe1-157">Você se esquece do contexto que foi nomeado 'Contoso2'.</span><span class="sxs-lookup"><span data-stu-id="debe1-157">Forgets the context that was named 'Contoso2'.</span></span> <span data-ttu-id="debe1-158">É possível recriar este contexto posteriormente usando `Set-AzureRmContext`</span><span class="sxs-lookup"><span data-stu-id="debe1-158">You can recreate this context subsequently using `Set-AzureRmContext`</span></span>

## <a name="removing-credentials"></a><span data-ttu-id="debe1-159">Removendo credenciais</span><span class="sxs-lookup"><span data-stu-id="debe1-159">Removing credentials</span></span>

<span data-ttu-id="debe1-160">Você pode remover todas as credenciais e contextos associados de um usuário ou entidade de serviço usando `Disconnect-AzureRmAccount` (também conhecido como `Logout-AzureRmAccount`).</span><span class="sxs-lookup"><span data-stu-id="debe1-160">You can remove all credentials and associated contexts for a user or service principal using `Disconnect-AzureRmAccount` (also known as `Logout-AzureRmAccount`).</span></span> <span data-ttu-id="debe1-161">Quando executado sem parâmetros, o cmdlet `Disconnect-AzureRmAccount` remove todas as credenciais e contextos associados ao usuário ou entidade de serviço no contexto atual.</span><span class="sxs-lookup"><span data-stu-id="debe1-161">When executed without parameters, the `Disconnect-AzureRmAccount` cmdlet removes all credentials and contexts associated with the User or Service Principal in the current context.</span></span> <span data-ttu-id="debe1-162">Você pode passar um Nome de Usuário, o Nome da Entidade de Serviço ou o Contexto para uma determinada entidade de destino.</span><span class="sxs-lookup"><span data-stu-id="debe1-162">You may pass in a Username, Service Principal Name, or context to target a particular principal.</span></span>

```powershell
Disconnect-AzureRmAccount user1@contoso.org
```

## <a name="using-context-scopes"></a><span data-ttu-id="debe1-163">Usando escopos de contexto</span><span class="sxs-lookup"><span data-stu-id="debe1-163">Using context scopes</span></span>

<span data-ttu-id="debe1-164">Ocasionalmente, convém selecionar, alterar ou remover um contexto em uma sessão do PowerShell sem afetar outras sessões.</span><span class="sxs-lookup"><span data-stu-id="debe1-164">Occasionally, you may want to select, change, or remove a context in a PowerShell session without impacting other sessions.</span></span> <span data-ttu-id="debe1-165">Para alterar o comportamento padrão dos cmdlets de contexto, use o parâmetro `Scope`.</span><span class="sxs-lookup"><span data-stu-id="debe1-165">To change the default behavior of context cmdlets, use the `Scope` parameter.</span></span> <span data-ttu-id="debe1-166">O escopo `Process` substitui o comportamento padrão aplicando-o apenas à sessão atual.</span><span class="sxs-lookup"><span data-stu-id="debe1-166">The `Process` scope overrides the default behavior by making it apply only for the current session.</span></span> <span data-ttu-id="debe1-167">Por outro lado, o escopo `CurrentUser` altera o contexto em todas as sessões, em vez de apenas a sessão atual.</span><span class="sxs-lookup"><span data-stu-id="debe1-167">Conversely `CurrentUser` scope changes the context in all sessions, instead of just the current session.</span></span>

<span data-ttu-id="debe1-168">Por exemplo, para alterar o contexto padrão na sessão atual do PowerShell sem afetar outras janelas ou o contexto usado na próxima vez em que uma sessão for aberta, use:</span><span class="sxs-lookup"><span data-stu-id="debe1-168">As an example, to change the default context in the current PowerShell session without impacting other windows, or the context used the next time a session is opened, use:</span></span>

```powershell
PS C:\> Select-AzureRmContext Contoso1 -Scope Process
```

## <a name="how-the-context-autosave-setting-is-remembered"></a><span data-ttu-id="debe1-169">Como a configuração de salvamento automático de contexto é lembrada</span><span class="sxs-lookup"><span data-stu-id="debe1-169">How the context autosave setting is remembered</span></span>

<span data-ttu-id="debe1-170">A configuração de Salvamento Automático de contexto é salva no diretório do usuário do Azure PowerShell (`%AppData%\Roaming\Windows Azure PowerShell`).</span><span class="sxs-lookup"><span data-stu-id="debe1-170">The context AutoSave setting is saved to the user Azure PowerShell directory (`%AppData%\Roaming\Windows Azure PowerShell`).</span></span> <span data-ttu-id="debe1-171">Alguns tipos de contas de computador podem não ter acesso a esse diretório.</span><span class="sxs-lookup"><span data-stu-id="debe1-171">Some kinds of computer accounts may not have access to this directory.</span></span> <span data-ttu-id="debe1-172">Para esses cenários, você pode usar a variável de ambiente</span><span class="sxs-lookup"><span data-stu-id="debe1-172">For such scenarios, you can use the environment variable</span></span>

```powershell
$env:AzureRmContextAutoSave="true" | "false"
```

<span data-ttu-id="debe1-173">Se definido como 'true', o contexto é salvo automaticamente.</span><span class="sxs-lookup"><span data-stu-id="debe1-173">If set to 'true', the context is automatically saved.</span></span> <span data-ttu-id="debe1-174">Se definido como 'false', o contexto não é salvo.</span><span class="sxs-lookup"><span data-stu-id="debe1-174">If set to 'false', the context is not saved.</span></span>

## <a name="changes-to-the-azurermprofile-module"></a><span data-ttu-id="debe1-175">Alterações no módulo AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="debe1-175">Changes to the AzureRM.Profile module</span></span>

<span data-ttu-id="debe1-176">Novos cmdlets para gerenciar contextos</span><span class="sxs-lookup"><span data-stu-id="debe1-176">New cmdlets for managing context</span></span>

- <span data-ttu-id="debe1-177">[Enable-AzureRmContextAutosave][enable] - Permite salvar o contexto entre sessões do Powershell.</span><span class="sxs-lookup"><span data-stu-id="debe1-177">[Enable-AzureRmContextAutosave][enable] - Allow saving the context between powershell sessions.</span></span>
  <span data-ttu-id="debe1-178">Qualquer alteração feita afetará o contexto global.</span><span class="sxs-lookup"><span data-stu-id="debe1-178">Any changes alter the global context.</span></span>
- <span data-ttu-id="debe1-179">[Disable-AzureRmContextAutosave][disable] - Desativa o salvamento automático do contexto.</span><span class="sxs-lookup"><span data-stu-id="debe1-179">[Disable-AzureRmContextAutosave][disable] - Turn off autosaving the context.</span></span> <span data-ttu-id="debe1-180">É necessário fazer logon novamente em cada nova sessão do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="debe1-180">Each new PowerShell session is required to log in again.</span></span>
- <span data-ttu-id="debe1-181">[Select-AzureRmContext][select] - Seleciona um contexto como o padrão.</span><span class="sxs-lookup"><span data-stu-id="debe1-181">[Select-AzureRmContext][select] - Select a context as the default.</span></span> <span data-ttu-id="debe1-182">Todos os cmdlets posteriores usam as credenciais neste contexto para autenticação.</span><span class="sxs-lookup"><span data-stu-id="debe1-182">All subsequent cmdlets use the credentials in this context for authentication.</span></span>
- <span data-ttu-id="debe1-183">[Disconnect-AzureRmAccount][remove-cred] - Remove todas as credenciais e contextos associados a uma conta.</span><span class="sxs-lookup"><span data-stu-id="debe1-183">[Disconnect-AzureRmAccount][remove-cred] - Remove all credentials and contexts associated with an account.</span></span>
- <span data-ttu-id="debe1-184">[Remove-AzureRmContext][remove-context] - Remove um contexto nomeado.</span><span class="sxs-lookup"><span data-stu-id="debe1-184">[Remove-AzureRmContext][remove-context] - Remove a named context.</span></span>
- <span data-ttu-id="debe1-185">[Rename-AzureRmContext][rename] - Renomeia um contexto existente.</span><span class="sxs-lookup"><span data-stu-id="debe1-185">[Rename-AzureRmContext][rename] - Rename an existing context.</span></span>

<span data-ttu-id="debe1-186">Alterações em cmdlets de perfil existentes</span><span class="sxs-lookup"><span data-stu-id="debe1-186">Changes to existing profile cmdlets</span></span>

- <span data-ttu-id="debe1-187">[Add-AzureRmAccount][login] - Permite realizar o escopo de logon do processo ou do usuário atual.</span><span class="sxs-lookup"><span data-stu-id="debe1-187">[Add-AzureRmAccount][login] - Allow scoping of the login to the process or the current user.</span></span>
  <span data-ttu-id="debe1-188">Permite nomear o contexto padrão após o logon.</span><span class="sxs-lookup"><span data-stu-id="debe1-188">Allow naming the default context after login.</span></span>
- <span data-ttu-id="debe1-189">[Import-AzureRmContext][import] - Permite realizar o escopo de logon do processo ou do usuário atual.</span><span class="sxs-lookup"><span data-stu-id="debe1-189">[Import-AzureRmContext][import] - Allow scoping of the login to the process or the current user.</span></span>
- <span data-ttu-id="debe1-190">[Set-AzureRmContext][set-context] - Permite a seleção de contextos nomeados existentes e alterações no escopo do processo ou do usuário atual.</span><span class="sxs-lookup"><span data-stu-id="debe1-190">[Set-AzureRmContext][set-context] - Allow selection of existing named contexts, and scope changes to the process or current user.</span></span>

<!-- Hyperlinks -->
[enable]: /powershell/module/azurerm.profile/Enable-AzureRmContextAutosave
[disable]: /powershell/module/azurerm.profile/Disable-AzureRmContextAutosave
[select]: /powershell/module/azurerm.profile/Select-AzureRmContext
[remove-cred]: /powershell/module/azurerm.profile/Disconnect-AzureRmAccount
[remove-context]: /powershell/module/azurerm.profile/Remove-AzureRmContext
[rename]: /powershell/module/azurerm.profile/Rename-AzureRmContext

<!-- Updated cmdlets -->
[login]: /powershell/module/azurerm.profile/Connect-AzureRmAccount
[import]: /powershell/module/azurerm.profile/Import-AzureRmAccount
[set-context]: /powershell/module/azurerm.profile/Import-AzureRmContext
