---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azcontextautosave
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
ms.openlocfilehash: 6d80ee2ee2072bd31e96f4daa5706cba5f1c8dab
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115578"
---
# <span data-ttu-id="039de-101">Enable-AzContextAutosave</span><span class="sxs-lookup"><span data-stu-id="039de-101">Enable-AzContextAutosave</span></span>

## <span data-ttu-id="039de-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="039de-102">SYNOPSIS</span></span>
<span data-ttu-id="039de-103">Os contextos do Azure são objetos do PowerShell que representam sua assinatura ativa para executar comandos e as informações de autenticação necessárias para se conectar a uma nuvem do Azure.</span><span class="sxs-lookup"><span data-stu-id="039de-103">Azure contexts are PowerShell objects representing your active subscription to run commands against, and the authentication information needed to connect to an Azure cloud.</span></span> <span data-ttu-id="039de-104">Com contextos do Azure, o Azure PowerShell não precisa re autenticar sua conta sempre que você mudar de assinatura.</span><span class="sxs-lookup"><span data-stu-id="039de-104">With Azure contexts, Azure PowerShell doesn't need to reauthenticate your account each time you switch subscriptions.</span></span> <span data-ttu-id="039de-105">Para obter mais informações, consulte objetos [de contexto do PowerShell do Azure.](https://docs.microsoft.com/powershell/azure/context-persistence)</span><span class="sxs-lookup"><span data-stu-id="039de-105">For more information, see [Azure PowerShell context objects](https://docs.microsoft.com/powershell/azure/context-persistence).</span></span>

<span data-ttu-id="039de-106">Esse cmdlet permite que as informações de contexto do Azure sejam salvas e carregadas automaticamente quando você inicia um processo do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="039de-106">This cmdlet allows the Azure context information to be saved and automatically loaded when you start a PowerShell process.</span></span> <span data-ttu-id="039de-107">Por exemplo, ao abrir uma nova janela.</span><span class="sxs-lookup"><span data-stu-id="039de-107">For example, when opening a new window.</span></span>

## <span data-ttu-id="039de-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="039de-108">SYNTAX</span></span>

```
Enable-AzContextAutosave [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="039de-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="039de-109">DESCRIPTION</span></span>

<span data-ttu-id="039de-110">Permite que as informações de contexto do Azure sejam salvas e carregadas automaticamente quando um processo do PowerShell é iniciado.</span><span class="sxs-lookup"><span data-stu-id="039de-110">Allows the Azure context information to be saved and automatically loaded when a PowerShell process starts.</span></span> <span data-ttu-id="039de-111">O contexto é salvo no final da execução de qualquer cmdlet que afete o contexto.</span><span class="sxs-lookup"><span data-stu-id="039de-111">The context is saved at the end of the execution of any cmdlet that affects the context.</span></span> <span data-ttu-id="039de-112">Por exemplo, qualquer cmdlet de perfil.</span><span class="sxs-lookup"><span data-stu-id="039de-112">For example, any profile cmdlet.</span></span> <span data-ttu-id="039de-113">Se você estiver usando a autenticação do usuário, os tokens poderão ser atualizados durante a execução de qualquer cmdlet.</span><span class="sxs-lookup"><span data-stu-id="039de-113">If you're using user authentication, then tokens can be updated during the course of running any cmdlet.</span></span>

## <span data-ttu-id="039de-114">Exemplos</span><span class="sxs-lookup"><span data-stu-id="039de-114">EXAMPLES</span></span>

### <span data-ttu-id="039de-115">Exemplo 1: Habilitar as credenciais de autoslagem para o usuário atual</span><span class="sxs-lookup"><span data-stu-id="039de-115">Example 1: Enable autosaving credentials for the current user</span></span>

<span data-ttu-id="039de-116">Ativar o autosave de credenciais para o usuário atual.</span><span class="sxs-lookup"><span data-stu-id="039de-116">Turn on credential autosave for the current user.</span></span> <span data-ttu-id="039de-117">Sempre que uma janela do PowerShell é aberta, seu contexto atual é lembrado sem fazer logo login.</span><span class="sxs-lookup"><span data-stu-id="039de-117">Whenever a PowerShell window is opened, your current context is remembered without logging in.</span></span>

```powershell
Enable-AzContextAutosave
```

### <span data-ttu-id="039de-118">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="039de-118">Example 2</span></span>

<span data-ttu-id="039de-119">Permita que as informações da credencial, da conta e da assinatura do Azure sejam salvas e carregadas automaticamente quando você abrir uma janela do PowerShell nesta sessão do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="039de-119">Allow the Azure credential, account, and subscription information, to be saved and automatically loaded when you open a PowerShell window in this PowerShell session.</span></span> <span data-ttu-id="039de-120">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="039de-120">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example -->
Enable-AzContextAutosave -Scope Process
```

## <span data-ttu-id="039de-121">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="039de-121">PARAMETERS</span></span>

### <span data-ttu-id="039de-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="039de-122">-DefaultProfile</span></span>

<span data-ttu-id="039de-123">As credenciais, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="039de-123">The credentials, tenant, and subscription used for communication with Azure</span></span>

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

### <span data-ttu-id="039de-124">-Escopo</span><span class="sxs-lookup"><span data-stu-id="039de-124">-Scope</span></span>

<span data-ttu-id="039de-125">Determina o escopo das alterações de contexto.</span><span class="sxs-lookup"><span data-stu-id="039de-125">Determines the scope of context changes.</span></span> <span data-ttu-id="039de-126">Por exemplo, se as alterações se aplicam apenas ao processo atual ou a todas as sessões iniciadas por esse usuário.</span><span class="sxs-lookup"><span data-stu-id="039de-126">For example, whether changes apply only to the current process, or to all sessions started by this user.</span></span> <span data-ttu-id="039de-127">As alterações feitas com o escopo `CurrentUser` afetarão todas as sessões do PowerShell iniciadas pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="039de-127">Changes made with the scope `CurrentUser` will affect all PowerShell sessions started by the user.</span></span> <span data-ttu-id="039de-128">Se uma sessão específica precisar ter configurações diferentes, use o `Process` escopo.</span><span class="sxs-lookup"><span data-stu-id="039de-128">If a particular session needs to have different settings, use the scope `Process`.</span></span>

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

### <span data-ttu-id="039de-129">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="039de-129">-Confirm</span></span>

<span data-ttu-id="039de-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="039de-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="039de-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="039de-131">-WhatIf</span></span>

<span data-ttu-id="039de-132">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="039de-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="039de-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="039de-133">The cmdlet isn't run.</span></span>

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

### <span data-ttu-id="039de-134">Parâmetros Comuns</span><span class="sxs-lookup"><span data-stu-id="039de-134">Common Parameters</span></span>

<span data-ttu-id="039de-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="039de-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="039de-136">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="039de-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="039de-137">Entradas</span><span class="sxs-lookup"><span data-stu-id="039de-137">INPUTS</span></span>

### <span data-ttu-id="039de-138">Nenhum</span><span class="sxs-lookup"><span data-stu-id="039de-138">None</span></span>

## <span data-ttu-id="039de-139">Saídas</span><span class="sxs-lookup"><span data-stu-id="039de-139">OUTPUTS</span></span>

### <span data-ttu-id="039de-140">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span><span class="sxs-lookup"><span data-stu-id="039de-140">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>

## <span data-ttu-id="039de-141">Notas</span><span class="sxs-lookup"><span data-stu-id="039de-141">NOTES</span></span>

## <span data-ttu-id="039de-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="039de-142">RELATED LINKS</span></span>
