---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/remove-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Remove-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Remove-AzContext.md
ms.openlocfilehash: f5307df3a91503f072c8292fe37957ce9af0df49
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885752"
---
# <span data-ttu-id="f6fc6-101">Remove-AzContext</span><span class="sxs-lookup"><span data-stu-id="f6fc6-101">Remove-AzContext</span></span>

## <span data-ttu-id="f6fc6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6fc6-102">SYNOPSIS</span></span>
<span data-ttu-id="f6fc6-103">Remover um contexto do conjunto de contextos disponíveis</span><span class="sxs-lookup"><span data-stu-id="f6fc6-103">Remove a context from the set of available contexts</span></span>

## <span data-ttu-id="f6fc6-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f6fc6-104">SYNTAX</span></span>

### <span data-ttu-id="f6fc6-105">RemoveByInputObject (Padrão)</span><span class="sxs-lookup"><span data-stu-id="f6fc6-105">RemoveByInputObject (Default)</span></span>
```
Remove-AzContext -InputObject <PSAzureContext> [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6fc6-106">RemoveByName</span><span class="sxs-lookup"><span data-stu-id="f6fc6-106">RemoveByName</span></span>
```
Remove-AzContext [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="f6fc6-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f6fc6-107">DESCRIPTION</span></span>
<span data-ttu-id="f6fc6-108">Remover um contexto do azure do conjunto de contextos</span><span class="sxs-lookup"><span data-stu-id="f6fc6-108">Remove an azure context from the set of contexts</span></span>

## <span data-ttu-id="f6fc6-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f6fc6-109">EXAMPLES</span></span>

### <span data-ttu-id="f6fc6-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f6fc6-110">Example 1</span></span>
```
PS C:\> Remove-AzContext -Name Default
```

<span data-ttu-id="f6fc6-111">Remover o contexto denominado padrão</span><span class="sxs-lookup"><span data-stu-id="f6fc6-111">Remove the context named default</span></span>

## <span data-ttu-id="f6fc6-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f6fc6-112">PARAMETERS</span></span>

### <span data-ttu-id="f6fc6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6fc6-113">-DefaultProfile</span></span>
<span data-ttu-id="f6fc6-114">As credenciais, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="f6fc6-114">The credentials, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6fc6-115">-Force</span><span class="sxs-lookup"><span data-stu-id="f6fc6-115">-Force</span></span>
<span data-ttu-id="f6fc6-116">Remover contexto mesmo que seja o padrão</span><span class="sxs-lookup"><span data-stu-id="f6fc6-116">Remove context even if it is the default</span></span>

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

### <span data-ttu-id="f6fc6-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f6fc6-117">-InputObject</span></span>
<span data-ttu-id="f6fc6-118">Um objeto de contexto, normalmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="f6fc6-118">A context object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f6fc6-119">-Name</span><span class="sxs-lookup"><span data-stu-id="f6fc6-119">-Name</span></span>
<span data-ttu-id="f6fc6-120">O nome do contexto</span><span class="sxs-lookup"><span data-stu-id="f6fc6-120">The name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6fc6-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f6fc6-121">-PassThru</span></span>
<span data-ttu-id="f6fc6-122">Retornar o contexto removido</span><span class="sxs-lookup"><span data-stu-id="f6fc6-122">Return the removed context</span></span>

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

### <span data-ttu-id="f6fc6-123">-Scope</span><span class="sxs-lookup"><span data-stu-id="f6fc6-123">-Scope</span></span>
<span data-ttu-id="f6fc6-124">Determina o escopo das alterações de contexto, por exemplo, se as alterações se aplicam apenas ao processo atual ou a todas as sessões iniciadas por esse usuário</span><span class="sxs-lookup"><span data-stu-id="f6fc6-124">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="f6fc6-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f6fc6-125">-Confirm</span></span>
<span data-ttu-id="f6fc6-126">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f6fc6-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6fc6-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6fc6-127">-WhatIf</span></span>
<span data-ttu-id="f6fc6-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f6fc6-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6fc6-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f6fc6-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6fc6-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6fc6-130">CommonParameters</span></span>
<span data-ttu-id="f6fc6-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6fc6-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6fc6-132">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f6fc6-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6fc6-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f6fc6-133">INPUTS</span></span>

### <span data-ttu-id="f6fc6-134">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="f6fc6-134">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="f6fc6-135">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f6fc6-135">OUTPUTS</span></span>

### <span data-ttu-id="f6fc6-136">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="f6fc6-136">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="f6fc6-137">NOTES</span><span class="sxs-lookup"><span data-stu-id="f6fc6-137">NOTES</span></span>

## <span data-ttu-id="f6fc6-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f6fc6-138">RELATED LINKS</span></span>
