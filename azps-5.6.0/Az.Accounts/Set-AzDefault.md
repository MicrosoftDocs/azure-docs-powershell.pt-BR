---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/set-azdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzDefault.md
ms.openlocfilehash: 98e7877ba075aacc1da00291bb557c2e94e276e6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892914"
---
# <span data-ttu-id="00137-101">Set-AzDefault</span><span class="sxs-lookup"><span data-stu-id="00137-101">Set-AzDefault</span></span>

## <span data-ttu-id="00137-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00137-102">SYNOPSIS</span></span>
<span data-ttu-id="00137-103">Define um padrão no contexto atual</span><span class="sxs-lookup"><span data-stu-id="00137-103">Sets a default in the current context</span></span>

## <span data-ttu-id="00137-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="00137-104">SYNTAX</span></span>

```
Set-AzDefault [-ResourceGroupName <String>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00137-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="00137-105">DESCRIPTION</span></span>
<span data-ttu-id="00137-106">O Set-AzDefault cmdlet adiciona ou altera os padrões no contexto atual.</span><span class="sxs-lookup"><span data-stu-id="00137-106">The Set-AzDefault cmdlet adds or changes the defaults in the current context.</span></span>

## <span data-ttu-id="00137-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="00137-107">EXAMPLES</span></span>

### <span data-ttu-id="00137-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="00137-108">Example 1</span></span>
```
PS C:\> Set-AzDefault -ResourceGroupName myResourceGroup

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="00137-109">Este comando define o grupo de recursos padrão para o grupo de recursos especificado pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="00137-109">This command sets the default resource group to the resource group specified by the user.</span></span>

## <span data-ttu-id="00137-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="00137-110">PARAMETERS</span></span>

### <span data-ttu-id="00137-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00137-111">-DefaultProfile</span></span>
<span data-ttu-id="00137-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="00137-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="00137-113">-Force</span><span class="sxs-lookup"><span data-stu-id="00137-113">-Force</span></span>
<span data-ttu-id="00137-114">Criar um novo grupo de recursos se o padrão especificado não existir</span><span class="sxs-lookup"><span data-stu-id="00137-114">Create a new resource group if specified default does not exist</span></span>

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

### <span data-ttu-id="00137-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00137-115">-ResourceGroupName</span></span>
<span data-ttu-id="00137-116">Nome do grupo de recursos que está sendo definido como padrão</span><span class="sxs-lookup"><span data-stu-id="00137-116">Name of the resource group being set as default</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00137-117">-Scope</span><span class="sxs-lookup"><span data-stu-id="00137-117">-Scope</span></span>
<span data-ttu-id="00137-118">Determina o escopo das alterações de contexto, por exemplo, se as alterações se aplicam apenas ao processo atual ou a todas as sessões iniciadas por esse usuário.</span><span class="sxs-lookup"><span data-stu-id="00137-118">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="00137-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="00137-119">-Confirm</span></span>
<span data-ttu-id="00137-120">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="00137-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00137-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00137-121">-WhatIf</span></span>
<span data-ttu-id="00137-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="00137-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00137-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="00137-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00137-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00137-124">CommonParameters</span></span>
<span data-ttu-id="00137-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00137-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00137-126">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="00137-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00137-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="00137-127">INPUTS</span></span>

### <span data-ttu-id="00137-128">System.String</span><span class="sxs-lookup"><span data-stu-id="00137-128">System.String</span></span>

## <span data-ttu-id="00137-129">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="00137-129">OUTPUTS</span></span>

### <span data-ttu-id="00137-130">Microsoft.Azure.Commands.Profile.Models.PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="00137-130">Microsoft.Azure.Commands.Profile.Models.PSResourceGroup</span></span>

## <span data-ttu-id="00137-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="00137-131">NOTES</span></span>

## <span data-ttu-id="00137-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="00137-132">RELATED LINKS</span></span>
