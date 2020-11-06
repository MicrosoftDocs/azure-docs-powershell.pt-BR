---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/remove-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Remove-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Remove-AzContext.md
ms.openlocfilehash: a2fc63409f36215d40fcf1e2e17c48b4dbe89e11
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93595785"
---
# <span data-ttu-id="de29c-101">Remove-AzContext</span><span class="sxs-lookup"><span data-stu-id="de29c-101">Remove-AzContext</span></span>

## <span data-ttu-id="de29c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="de29c-102">SYNOPSIS</span></span>
<span data-ttu-id="de29c-103">Remover um contexto do conjunto de contextos disponíveis</span><span class="sxs-lookup"><span data-stu-id="de29c-103">Remove a context from the set of available contexts</span></span>

## <span data-ttu-id="de29c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="de29c-104">SYNTAX</span></span>

### <span data-ttu-id="de29c-105">RemoveByInputObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="de29c-105">RemoveByInputObject (Default)</span></span>
```
Remove-AzContext -InputObject <PSAzureContext> [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de29c-106">RemoveByName</span><span class="sxs-lookup"><span data-stu-id="de29c-106">RemoveByName</span></span>
```
Remove-AzContext [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="de29c-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="de29c-107">DESCRIPTION</span></span>
<span data-ttu-id="de29c-108">Remover um contexto do Azure do conjunto de contextos</span><span class="sxs-lookup"><span data-stu-id="de29c-108">Remove an azure context from the set of contexts</span></span>

## <span data-ttu-id="de29c-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="de29c-109">EXAMPLES</span></span>

### <span data-ttu-id="de29c-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="de29c-110">Example 1</span></span>
```
PS C:\> Remove-AzContext -Name Default
```

<span data-ttu-id="de29c-111">Remover o contexto chamado padrão</span><span class="sxs-lookup"><span data-stu-id="de29c-111">Remove the context named default</span></span>

## <span data-ttu-id="de29c-112">OS</span><span class="sxs-lookup"><span data-stu-id="de29c-112">PARAMETERS</span></span>

### <span data-ttu-id="de29c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de29c-113">-DefaultProfile</span></span>
<span data-ttu-id="de29c-114">As credenciais, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="de29c-114">The credentials, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="de29c-115">-Force</span><span class="sxs-lookup"><span data-stu-id="de29c-115">-Force</span></span>
<span data-ttu-id="de29c-116">Remover contexto mesmo que seja o</span><span class="sxs-lookup"><span data-stu-id="de29c-116">Remove context even if it is the defualt</span></span>

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

### <span data-ttu-id="de29c-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="de29c-117">-InputObject</span></span>
<span data-ttu-id="de29c-118">Um objeto Context, normalmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="de29c-118">A context object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="de29c-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="de29c-119">-Name</span></span>
<span data-ttu-id="de29c-120">O nome do contexto</span><span class="sxs-lookup"><span data-stu-id="de29c-120">The name of the context</span></span>

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

### <span data-ttu-id="de29c-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="de29c-121">-PassThru</span></span>
<span data-ttu-id="de29c-122">Retornar o contexto removido</span><span class="sxs-lookup"><span data-stu-id="de29c-122">Return the removed context</span></span>

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

### <span data-ttu-id="de29c-123">-Escopo</span><span class="sxs-lookup"><span data-stu-id="de29c-123">-Scope</span></span>
<span data-ttu-id="de29c-124">Determina o escopo das alterações de contexto, por exemplo, se as alterações se aplicam somente ao processo atual ou a todas as sessões iniciadas por este usuário</span><span class="sxs-lookup"><span data-stu-id="de29c-124">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="de29c-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="de29c-125">-Confirm</span></span>
<span data-ttu-id="de29c-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de29c-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de29c-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de29c-127">-WhatIf</span></span>
<span data-ttu-id="de29c-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="de29c-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de29c-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="de29c-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de29c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de29c-130">CommonParameters</span></span>
<span data-ttu-id="de29c-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de29c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de29c-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de29c-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de29c-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="de29c-133">INPUTS</span></span>

### <span data-ttu-id="de29c-134">Microsoft. Azure. Commands. Profile. Models. Core. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="de29c-134">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="de29c-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="de29c-135">OUTPUTS</span></span>

### <span data-ttu-id="de29c-136">Microsoft. Azure. Commands. Profile. Models. Core. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="de29c-136">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="de29c-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="de29c-137">NOTES</span></span>

## <span data-ttu-id="de29c-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="de29c-138">RELATED LINKS</span></span>
