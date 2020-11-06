---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/rename-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Rename-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Rename-AzContext.md
ms.openlocfilehash: 809ec5bb5388447e5f20fe267598660ac0e49ec8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93595782"
---
# <span data-ttu-id="e8944-101">Rename-AzContext</span><span class="sxs-lookup"><span data-stu-id="e8944-101">Rename-AzContext</span></span>

## <span data-ttu-id="e8944-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e8944-102">SYNOPSIS</span></span>
<span data-ttu-id="e8944-103">Renomear um contexto do Azure.</span><span class="sxs-lookup"><span data-stu-id="e8944-103">Rename an Azure context.</span></span>  <span data-ttu-id="e8944-104">Por contextos padrão são nomeados por conta de usuário e assinatura.</span><span class="sxs-lookup"><span data-stu-id="e8944-104">By default contexts are named by user account and subscription.</span></span>

## <span data-ttu-id="e8944-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e8944-105">SYNTAX</span></span>

### <span data-ttu-id="e8944-106">RenameByInputObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="e8944-106">RenameByInputObject (Default)</span></span>
```
Rename-AzContext -InputObject <PSAzureContext> [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-TargetName] <String> [<CommonParameters>]
```

### <span data-ttu-id="e8944-107">RenameByName</span><span class="sxs-lookup"><span data-stu-id="e8944-107">RenameByName</span></span>
```
Rename-AzContext [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-SourceName] <String> [-TargetName] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="e8944-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e8944-108">DESCRIPTION</span></span>
<span data-ttu-id="e8944-109">Renomear um contexto do Azure.</span><span class="sxs-lookup"><span data-stu-id="e8944-109">Rename an Azure context.</span></span>  <span data-ttu-id="e8944-110">Por contextos padrão são nomeados por conta de usuário e assinatura.</span><span class="sxs-lookup"><span data-stu-id="e8944-110">By default contexts are named by user account and subscription.</span></span>

## <span data-ttu-id="e8944-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e8944-111">EXAMPLES</span></span>

### <span data-ttu-id="e8944-112">Renomear um contexto usando parâmetros nomeados</span><span class="sxs-lookup"><span data-stu-id="e8944-112">Rename a context using named parameters</span></span>
```
PS C:\> Rename-AzContext -SourceName "[user1@contoso.org; 12345-6789-2345-3567890]" -TargetName "Work"
```

<span data-ttu-id="e8944-113">Renomeie o contexto de ' user1@contoso.org ' com a assinatura ' 12345-6789-2345-3567890 ' para ' trabalho '.</span><span class="sxs-lookup"><span data-stu-id="e8944-113">Rename the context for 'user1@contoso.org' with subscription '12345-6789-2345-3567890' to 'Work'.</span></span>  <span data-ttu-id="e8944-114">Após esse comando, você poderá direcionar o contexto usando o ' trabalho de seleção AzContext '.</span><span class="sxs-lookup"><span data-stu-id="e8944-114">After this command, you will be able to target the context using 'Select-AzContext Work'.</span></span>  <span data-ttu-id="e8944-115">Observe que você pode Tab para percorrer os valores de ' SourceName ' usando a conclusão de tabulação.</span><span class="sxs-lookup"><span data-stu-id="e8944-115">Note that you can tab through the values for 'SourceName' using tab completion.</span></span>

### <span data-ttu-id="e8944-116">Renomear um contexto usando parâmetros posicionais</span><span class="sxs-lookup"><span data-stu-id="e8944-116">Rename a context using positional parameters</span></span>
```
PS C:\> Rename-AzContext "My context" "Work"
```

<span data-ttu-id="e8944-117">Renomeie o contexto chamado "My Context" para "Work".</span><span class="sxs-lookup"><span data-stu-id="e8944-117">Rename the context named "My context" to "Work".</span></span>  <span data-ttu-id="e8944-118">Após esse comando, você poderá direcionar o contexto usando Select-AzContext trabalho</span><span class="sxs-lookup"><span data-stu-id="e8944-118">After this command, you will be able to target the context using Select-AzContext Work</span></span>

## <span data-ttu-id="e8944-119">OS</span><span class="sxs-lookup"><span data-stu-id="e8944-119">PARAMETERS</span></span>

### <span data-ttu-id="e8944-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8944-120">-DefaultProfile</span></span>
<span data-ttu-id="e8944-121">As credenciais, o locatário e a assinatura usados para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="e8944-121">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e8944-122">-Force</span><span class="sxs-lookup"><span data-stu-id="e8944-122">-Force</span></span>
<span data-ttu-id="e8944-123">Renomeie o contexto mesmo se o contexto de destino já existir</span><span class="sxs-lookup"><span data-stu-id="e8944-123">Rename the context even if the target context already exists</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8944-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e8944-124">-InputObject</span></span>
<span data-ttu-id="e8944-125">Um objeto Context, normalmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="e8944-125">A context object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext
Parameter Sets: RenameByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e8944-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e8944-126">-PassThru</span></span>
<span data-ttu-id="e8944-127">Retorne o contexto renomeado.</span><span class="sxs-lookup"><span data-stu-id="e8944-127">Return the renamed context.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8944-128">-Escopo</span><span class="sxs-lookup"><span data-stu-id="e8944-128">-Scope</span></span>
<span data-ttu-id="e8944-129">Determina o escopo das alterações de contexto, por exemplo, se as alterações se aplicam somente ao processo atual ou a todas as sessões iniciadas por este usuário</span><span class="sxs-lookup"><span data-stu-id="e8944-129">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8944-130">-SourceName</span><span class="sxs-lookup"><span data-stu-id="e8944-130">-SourceName</span></span>
<span data-ttu-id="e8944-131">O nome do contexto</span><span class="sxs-lookup"><span data-stu-id="e8944-131">The name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: RenameByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8944-132">-TargetName</span><span class="sxs-lookup"><span data-stu-id="e8944-132">-TargetName</span></span>
<span data-ttu-id="e8944-133">O novo nome do contexto</span><span class="sxs-lookup"><span data-stu-id="e8944-133">The new name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8944-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e8944-134">-Confirm</span></span>
<span data-ttu-id="e8944-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8944-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8944-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8944-136">-WhatIf</span></span>
<span data-ttu-id="e8944-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e8944-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8944-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e8944-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8944-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8944-139">CommonParameters</span></span>
<span data-ttu-id="e8944-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8944-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8944-141">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8944-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8944-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e8944-142">INPUTS</span></span>

### <span data-ttu-id="e8944-143">Microsoft. Azure. Commands. Profile. Models. Core. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="e8944-143">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="e8944-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e8944-144">OUTPUTS</span></span>

### <span data-ttu-id="e8944-145">Microsoft. Azure. Commands. Profile. Models. Core. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="e8944-145">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="e8944-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e8944-146">NOTES</span></span>

## <span data-ttu-id="e8944-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e8944-147">RELATED LINKS</span></span>
