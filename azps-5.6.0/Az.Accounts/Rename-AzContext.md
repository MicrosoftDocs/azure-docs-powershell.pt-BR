---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/rename-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Rename-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Rename-AzContext.md
ms.openlocfilehash: 2ff8297ff04f18a903cca3a262d5232ace7c6ef1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887078"
---
# <span data-ttu-id="098d5-101">Rename-AzContext</span><span class="sxs-lookup"><span data-stu-id="098d5-101">Rename-AzContext</span></span>

## <span data-ttu-id="098d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="098d5-102">SYNOPSIS</span></span>
<span data-ttu-id="098d5-103">Renomeie um contexto do Azure.</span><span class="sxs-lookup"><span data-stu-id="098d5-103">Rename an Azure context.</span></span>  <span data-ttu-id="098d5-104">Por padrão, os contextos são nomeados por conta de usuário e assinatura.</span><span class="sxs-lookup"><span data-stu-id="098d5-104">By default contexts are named by user account and subscription.</span></span>

## <span data-ttu-id="098d5-105">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="098d5-105">SYNTAX</span></span>

### <span data-ttu-id="098d5-106">RenameByInputObject (Padrão)</span><span class="sxs-lookup"><span data-stu-id="098d5-106">RenameByInputObject (Default)</span></span>
```
Rename-AzContext -InputObject <PSAzureContext> [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-TargetName] <String> [<CommonParameters>]
```

### <span data-ttu-id="098d5-107">RenameByName</span><span class="sxs-lookup"><span data-stu-id="098d5-107">RenameByName</span></span>
```
Rename-AzContext [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-SourceName] <String> [-TargetName] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="098d5-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="098d5-108">DESCRIPTION</span></span>
<span data-ttu-id="098d5-109">Renomeie um contexto do Azure.</span><span class="sxs-lookup"><span data-stu-id="098d5-109">Rename an Azure context.</span></span>  <span data-ttu-id="098d5-110">Por padrão, os contextos são nomeados por conta de usuário e assinatura.</span><span class="sxs-lookup"><span data-stu-id="098d5-110">By default contexts are named by user account and subscription.</span></span>

## <span data-ttu-id="098d5-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="098d5-111">EXAMPLES</span></span>

### <span data-ttu-id="098d5-112">Exemplo 1: Renomear um contexto usando parâmetros nomeados</span><span class="sxs-lookup"><span data-stu-id="098d5-112">Example 1: Rename a context using named parameters</span></span>
```powershell
PS C:\> Rename-AzContext -SourceName "[user1@contoso.org; 12345-6789-2345-3567890]" -TargetName "Work"
```

<span data-ttu-id="098d5-113">Renomeie o contexto para ' ' com a assinatura user1@contoso.org '12345-6789-2345-3567890' para 'Work'.</span><span class="sxs-lookup"><span data-stu-id="098d5-113">Rename the context for 'user1@contoso.org' with subscription '12345-6789-2345-3567890' to 'Work'.</span></span>  <span data-ttu-id="098d5-114">Após esse comando, você poderá direcionar o contexto usando 'Select-AzContext Work'.</span><span class="sxs-lookup"><span data-stu-id="098d5-114">After this command, you will be able to target the context using 'Select-AzContext Work'.</span></span>  <span data-ttu-id="098d5-115">Observe que você pode tabular os valores de 'SourceName' usando a conclusão da guia.</span><span class="sxs-lookup"><span data-stu-id="098d5-115">Note that you can tab through the values for 'SourceName' using tab completion.</span></span>

### <span data-ttu-id="098d5-116">Exemplo 2: Renomear um contexto usando parâmetros posicionais</span><span class="sxs-lookup"><span data-stu-id="098d5-116">Example 2: Rename a context using positional parameters</span></span>
```powershell
PS C:\> Rename-AzContext "My context" "Work"
```

<span data-ttu-id="098d5-117">Renomeie o contexto chamado "Meu contexto" para "Trabalho".</span><span class="sxs-lookup"><span data-stu-id="098d5-117">Rename the context named "My context" to "Work".</span></span>  <span data-ttu-id="098d5-118">Após esse comando, você poderá direcionar o contexto usando o Select-AzContext Work</span><span class="sxs-lookup"><span data-stu-id="098d5-118">After this command, you will be able to target the context using Select-AzContext Work</span></span>

## <span data-ttu-id="098d5-119">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="098d5-119">PARAMETERS</span></span>

### <span data-ttu-id="098d5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="098d5-120">-DefaultProfile</span></span>
<span data-ttu-id="098d5-121">As credenciais, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="098d5-121">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="098d5-122">-Force</span><span class="sxs-lookup"><span data-stu-id="098d5-122">-Force</span></span>
<span data-ttu-id="098d5-123">Renomeie o contexto mesmo que o contexto de destino já exista</span><span class="sxs-lookup"><span data-stu-id="098d5-123">Rename the context even if the target context already exists</span></span>

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

### <span data-ttu-id="098d5-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="098d5-124">-InputObject</span></span>
<span data-ttu-id="098d5-125">Um objeto de contexto, normalmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="098d5-125">A context object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="098d5-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="098d5-126">-PassThru</span></span>
<span data-ttu-id="098d5-127">Retornar o contexto renomeado.</span><span class="sxs-lookup"><span data-stu-id="098d5-127">Return the renamed context.</span></span>

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

### <span data-ttu-id="098d5-128">-Scope</span><span class="sxs-lookup"><span data-stu-id="098d5-128">-Scope</span></span>
<span data-ttu-id="098d5-129">Determina o escopo das alterações de contexto, por exemplo, se as alterações se aplicam apenas ao processo atual ou a todas as sessões iniciadas por esse usuário</span><span class="sxs-lookup"><span data-stu-id="098d5-129">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="098d5-130">-SourceName</span><span class="sxs-lookup"><span data-stu-id="098d5-130">-SourceName</span></span>
<span data-ttu-id="098d5-131">O nome do contexto</span><span class="sxs-lookup"><span data-stu-id="098d5-131">The name of the context</span></span>

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

### <span data-ttu-id="098d5-132">-TargetName</span><span class="sxs-lookup"><span data-stu-id="098d5-132">-TargetName</span></span>
<span data-ttu-id="098d5-133">O novo nome do contexto</span><span class="sxs-lookup"><span data-stu-id="098d5-133">The new name of the context</span></span>

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

### <span data-ttu-id="098d5-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="098d5-134">-Confirm</span></span>
<span data-ttu-id="098d5-135">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="098d5-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="098d5-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="098d5-136">-WhatIf</span></span>
<span data-ttu-id="098d5-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="098d5-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="098d5-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="098d5-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="098d5-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="098d5-139">CommonParameters</span></span>
<span data-ttu-id="098d5-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="098d5-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="098d5-141">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="098d5-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="098d5-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="098d5-142">INPUTS</span></span>

### <span data-ttu-id="098d5-143">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="098d5-143">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="098d5-144">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="098d5-144">OUTPUTS</span></span>

### <span data-ttu-id="098d5-145">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="098d5-145">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="098d5-146">NOTES</span><span class="sxs-lookup"><span data-stu-id="098d5-146">NOTES</span></span>

## <span data-ttu-id="098d5-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="098d5-147">RELATED LINKS</span></span>
