---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/remove-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Remove-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Remove-AzContext.md
ms.openlocfilehash: d5c31519ba55babb79e3e902a01e46746c5b70f1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114327"
---
# <span data-ttu-id="74d5f-101">Remove-AzContext</span><span class="sxs-lookup"><span data-stu-id="74d5f-101">Remove-AzContext</span></span>

## <span data-ttu-id="74d5f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="74d5f-102">SYNOPSIS</span></span>
<span data-ttu-id="74d5f-103">Remover um contexto do conjunto de contextos disponíveis</span><span class="sxs-lookup"><span data-stu-id="74d5f-103">Remove a context from the set of available contexts</span></span>

## <span data-ttu-id="74d5f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="74d5f-104">SYNTAX</span></span>

### <span data-ttu-id="74d5f-105">RemoveByInputObject (Padrão)</span><span class="sxs-lookup"><span data-stu-id="74d5f-105">RemoveByInputObject (Default)</span></span>
```
Remove-AzContext -InputObject <PSAzureContext> [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74d5f-106">RemoveByName</span><span class="sxs-lookup"><span data-stu-id="74d5f-106">RemoveByName</span></span>
```
Remove-AzContext [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="74d5f-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="74d5f-107">DESCRIPTION</span></span>
<span data-ttu-id="74d5f-108">Remover um contexto do azure do conjunto de contextos</span><span class="sxs-lookup"><span data-stu-id="74d5f-108">Remove an azure context from the set of contexts</span></span>

## <span data-ttu-id="74d5f-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="74d5f-109">EXAMPLES</span></span>

### <span data-ttu-id="74d5f-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="74d5f-110">Example 1</span></span>
```
PS C:\> Remove-AzContext -Name Default
```

<span data-ttu-id="74d5f-111">Remover o contexto nomeado como padrão</span><span class="sxs-lookup"><span data-stu-id="74d5f-111">Remove the context named default</span></span>

## <span data-ttu-id="74d5f-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="74d5f-112">PARAMETERS</span></span>

### <span data-ttu-id="74d5f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74d5f-113">-DefaultProfile</span></span>
<span data-ttu-id="74d5f-114">As credenciais, locatário e assinatura usados para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="74d5f-114">The credentials, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="74d5f-115">-Forçar</span><span class="sxs-lookup"><span data-stu-id="74d5f-115">-Force</span></span>
<span data-ttu-id="74d5f-116">Remover contexto mesmo que seja o padrão</span><span class="sxs-lookup"><span data-stu-id="74d5f-116">Remove context even if it is the default</span></span>

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

### <span data-ttu-id="74d5f-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="74d5f-117">-InputObject</span></span>
<span data-ttu-id="74d5f-118">Um objeto de contexto, normalmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="74d5f-118">A context object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="74d5f-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="74d5f-119">-Name</span></span>
<span data-ttu-id="74d5f-120">O nome do contexto</span><span class="sxs-lookup"><span data-stu-id="74d5f-120">The name of the context</span></span>

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

### <span data-ttu-id="74d5f-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="74d5f-121">-PassThru</span></span>
<span data-ttu-id="74d5f-122">Retornar o contexto removido</span><span class="sxs-lookup"><span data-stu-id="74d5f-122">Return the removed context</span></span>

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

### <span data-ttu-id="74d5f-123">-Escopo</span><span class="sxs-lookup"><span data-stu-id="74d5f-123">-Scope</span></span>
<span data-ttu-id="74d5f-124">Determina o escopo das alterações de contexto, por exemplo, se as alterações se aplicam apenas ao processo atual ou a todas as sessões iniciadas por esse usuário</span><span class="sxs-lookup"><span data-stu-id="74d5f-124">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="74d5f-125">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="74d5f-125">-Confirm</span></span>
<span data-ttu-id="74d5f-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74d5f-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74d5f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74d5f-127">-WhatIf</span></span>
<span data-ttu-id="74d5f-128">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="74d5f-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74d5f-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="74d5f-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74d5f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74d5f-130">CommonParameters</span></span>
<span data-ttu-id="74d5f-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74d5f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74d5f-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74d5f-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74d5f-133">Entradas</span><span class="sxs-lookup"><span data-stu-id="74d5f-133">INPUTS</span></span>

### <span data-ttu-id="74d5f-134">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="74d5f-134">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="74d5f-135">Saídas</span><span class="sxs-lookup"><span data-stu-id="74d5f-135">OUTPUTS</span></span>

### <span data-ttu-id="74d5f-136">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="74d5f-136">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="74d5f-137">Notas</span><span class="sxs-lookup"><span data-stu-id="74d5f-137">NOTES</span></span>

## <span data-ttu-id="74d5f-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="74d5f-138">RELATED LINKS</span></span>
