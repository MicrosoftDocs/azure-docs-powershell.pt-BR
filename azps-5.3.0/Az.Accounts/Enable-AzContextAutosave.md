---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azcontextautosave
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
ms.openlocfilehash: 6d80ee2ee2072bd31e96f4daa5706cba5f1c8dab
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98432837"
---
# <span data-ttu-id="739c5-101">Enable-AzContextAutosave</span><span class="sxs-lookup"><span data-stu-id="739c5-101">Enable-AzContextAutosave</span></span>

## <span data-ttu-id="739c5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="739c5-102">SYNOPSIS</span></span>
<span data-ttu-id="739c5-103">Os contextos do Azure são objetos do PowerShell que representam a sua assinatura ativa para executar comandos e as informações de autenticação necessárias para se conectar a uma nuvem do Azure.</span><span class="sxs-lookup"><span data-stu-id="739c5-103">Azure contexts are PowerShell objects representing your active subscription to run commands against, and the authentication information needed to connect to an Azure cloud.</span></span> <span data-ttu-id="739c5-104">Com os contextos do Azure, o PowerShell do Azure não precisa autenticar sua conta sempre que você alternar entre assinaturas.</span><span class="sxs-lookup"><span data-stu-id="739c5-104">With Azure contexts, Azure PowerShell doesn't need to reauthenticate your account each time you switch subscriptions.</span></span> <span data-ttu-id="739c5-105">Para obter mais informações, consulte [objetos de contexto do PowerShell do PowerShell](https://docs.microsoft.com/powershell/azure/context-persistence).</span><span class="sxs-lookup"><span data-stu-id="739c5-105">For more information, see [Azure PowerShell context objects](https://docs.microsoft.com/powershell/azure/context-persistence).</span></span>

<span data-ttu-id="739c5-106">Esse cmdlet permite que as informações de contexto do Azure sejam salvas e carregadas automaticamente quando você inicia um processo do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="739c5-106">This cmdlet allows the Azure context information to be saved and automatically loaded when you start a PowerShell process.</span></span> <span data-ttu-id="739c5-107">Por exemplo, ao abrir uma nova janela.</span><span class="sxs-lookup"><span data-stu-id="739c5-107">For example, when opening a new window.</span></span>

## <span data-ttu-id="739c5-108">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="739c5-108">SYNTAX</span></span>

```
Enable-AzContextAutosave [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="739c5-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="739c5-109">DESCRIPTION</span></span>

<span data-ttu-id="739c5-110">Permite que as informações de contexto do Azure sejam salvas e carregadas automaticamente quando um processo do PowerShell é iniciado.</span><span class="sxs-lookup"><span data-stu-id="739c5-110">Allows the Azure context information to be saved and automatically loaded when a PowerShell process starts.</span></span> <span data-ttu-id="739c5-111">O contexto é salvo no final da execução de qualquer cmdlet que afete o contexto.</span><span class="sxs-lookup"><span data-stu-id="739c5-111">The context is saved at the end of the execution of any cmdlet that affects the context.</span></span> <span data-ttu-id="739c5-112">Por exemplo, qualquer cmdlet de perfil.</span><span class="sxs-lookup"><span data-stu-id="739c5-112">For example, any profile cmdlet.</span></span> <span data-ttu-id="739c5-113">Se você estiver usando a autenticação de usuário, os tokens podem ser atualizados durante o curso da execução de qualquer cmdlet.</span><span class="sxs-lookup"><span data-stu-id="739c5-113">If you're using user authentication, then tokens can be updated during the course of running any cmdlet.</span></span>

## <span data-ttu-id="739c5-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="739c5-114">EXAMPLES</span></span>

### <span data-ttu-id="739c5-115">Exemplo 1: habilitar a gravação de credenciais para o usuário atual</span><span class="sxs-lookup"><span data-stu-id="739c5-115">Example 1: Enable autosaving credentials for the current user</span></span>

<span data-ttu-id="739c5-116">Ative o salvamento automático de credenciais para o usuário atual.</span><span class="sxs-lookup"><span data-stu-id="739c5-116">Turn on credential autosave for the current user.</span></span> <span data-ttu-id="739c5-117">Sempre que uma janela do PowerShell é aberta, seu contexto atual é lembrado sem fazer logon.</span><span class="sxs-lookup"><span data-stu-id="739c5-117">Whenever a PowerShell window is opened, your current context is remembered without logging in.</span></span>

```powershell
Enable-AzContextAutosave
```

### <span data-ttu-id="739c5-118">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="739c5-118">Example 2</span></span>

<span data-ttu-id="739c5-119">Permitir que a credencial do Azure, a conta e as informações de assinatura sejam salvas e carregadas automaticamente quando você abrir uma janela do PowerShell nesta sessão do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="739c5-119">Allow the Azure credential, account, and subscription information, to be saved and automatically loaded when you open a PowerShell window in this PowerShell session.</span></span> <span data-ttu-id="739c5-120">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="739c5-120">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example -->
Enable-AzContextAutosave -Scope Process
```

## <span data-ttu-id="739c5-121">OS</span><span class="sxs-lookup"><span data-stu-id="739c5-121">PARAMETERS</span></span>

### <span data-ttu-id="739c5-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="739c5-122">-DefaultProfile</span></span>

<span data-ttu-id="739c5-123">As credenciais, o locatário e a assinatura usados para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="739c5-123">The credentials, tenant, and subscription used for communication with Azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="739c5-124">-Escopo</span><span class="sxs-lookup"><span data-stu-id="739c5-124">-Scope</span></span>

<span data-ttu-id="739c5-125">Determina o escopo das alterações de contexto.</span><span class="sxs-lookup"><span data-stu-id="739c5-125">Determines the scope of context changes.</span></span> <span data-ttu-id="739c5-126">Por exemplo, se as alterações se aplicam somente ao processo atual ou a todas as sessões iniciadas por esse usuário.</span><span class="sxs-lookup"><span data-stu-id="739c5-126">For example, whether changes apply only to the current process, or to all sessions started by this user.</span></span> <span data-ttu-id="739c5-127">As alterações feitas com o escopo `CurrentUser` afetarão todas as sessões do PowerShell iniciadas pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="739c5-127">Changes made with the scope `CurrentUser` will affect all PowerShell sessions started by the user.</span></span> <span data-ttu-id="739c5-128">Se uma sessão específica precisa ter configurações diferentes, use o escopo `Process` .</span><span class="sxs-lookup"><span data-stu-id="739c5-128">If a particular session needs to have different settings, use the scope `Process`.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: CurrentUser
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="739c5-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="739c5-129">-Confirm</span></span>

<span data-ttu-id="739c5-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="739c5-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="739c5-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="739c5-131">-WhatIf</span></span>

<span data-ttu-id="739c5-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="739c5-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="739c5-133">O cmdlet não está em execução.</span><span class="sxs-lookup"><span data-stu-id="739c5-133">The cmdlet isn't run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="739c5-134">Parâmetros comuns</span><span class="sxs-lookup"><span data-stu-id="739c5-134">Common Parameters</span></span>

<span data-ttu-id="739c5-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="739c5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="739c5-136">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="739c5-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="739c5-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="739c5-137">INPUTS</span></span>

### <span data-ttu-id="739c5-138">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="739c5-138">None</span></span>

## <span data-ttu-id="739c5-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="739c5-139">OUTPUTS</span></span>

### <span data-ttu-id="739c5-140">Microsoft. Azure. Commands. Common. Authentication. ContextAutosaveSettings</span><span class="sxs-lookup"><span data-stu-id="739c5-140">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>

## <span data-ttu-id="739c5-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="739c5-141">NOTES</span></span>

## <span data-ttu-id="739c5-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="739c5-142">RELATED LINKS</span></span>
