---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/set-azdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzDefault.md
ms.openlocfilehash: 25fd0e1cd651f70fa0900c528f9e5297a8eaf2df
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110698"
---
# <span data-ttu-id="bb434-101">Set-AzDefault</span><span class="sxs-lookup"><span data-stu-id="bb434-101">Set-AzDefault</span></span>

## <span data-ttu-id="bb434-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bb434-102">SYNOPSIS</span></span>
<span data-ttu-id="bb434-103">Define um padrão no contexto atual</span><span class="sxs-lookup"><span data-stu-id="bb434-103">Sets a default in the current context</span></span>

## <span data-ttu-id="bb434-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bb434-104">SYNTAX</span></span>

```
Set-AzDefault [-ResourceGroupName <String>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb434-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bb434-105">DESCRIPTION</span></span>
<span data-ttu-id="bb434-106">O cmdlet Set-AzDefault adiciona ou altera os padrões no contexto atual.</span><span class="sxs-lookup"><span data-stu-id="bb434-106">The Set-AzDefault cmdlet adds or changes the defaults in the current context.</span></span>

## <span data-ttu-id="bb434-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bb434-107">EXAMPLES</span></span>

### <span data-ttu-id="bb434-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bb434-108">Example 1</span></span>
```
PS C:\> Set-AzDefault -ResourceGroupName myResourceGroup

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="bb434-109">Este comando define o grupo de recursos padrão para o grupo de recursos especificado pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="bb434-109">This command sets the default resource group to the resource group specified by the user.</span></span>

## <span data-ttu-id="bb434-110">OS</span><span class="sxs-lookup"><span data-stu-id="bb434-110">PARAMETERS</span></span>

### <span data-ttu-id="bb434-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb434-111">-DefaultProfile</span></span>
<span data-ttu-id="bb434-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bb434-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bb434-113">-Force</span><span class="sxs-lookup"><span data-stu-id="bb434-113">-Force</span></span>
<span data-ttu-id="bb434-114">Criar um novo grupo de recursos se o padrão especificado não existir</span><span class="sxs-lookup"><span data-stu-id="bb434-114">Create a new resource group if specified default does not exist</span></span>

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

### <span data-ttu-id="bb434-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb434-115">-ResourceGroupName</span></span>
<span data-ttu-id="bb434-116">Nome do grupo de recursos sendo definido como padrão</span><span class="sxs-lookup"><span data-stu-id="bb434-116">Name of the resource group being set as default</span></span>

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

### <span data-ttu-id="bb434-117">-Escopo</span><span class="sxs-lookup"><span data-stu-id="bb434-117">-Scope</span></span>
<span data-ttu-id="bb434-118">Determina o escopo das alterações de contexto, por exemplo, se as alterações se aplicam somente ao processo atual ou a todas as sessões iniciadas por esse usuário.</span><span class="sxs-lookup"><span data-stu-id="bb434-118">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="bb434-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="bb434-119">-Confirm</span></span>
<span data-ttu-id="bb434-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb434-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb434-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb434-121">-WhatIf</span></span>
<span data-ttu-id="bb434-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bb434-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb434-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bb434-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb434-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb434-124">CommonParameters</span></span>
<span data-ttu-id="bb434-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb434-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb434-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb434-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb434-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bb434-127">INPUTS</span></span>

### <span data-ttu-id="bb434-128">System. String</span><span class="sxs-lookup"><span data-stu-id="bb434-128">System.String</span></span>

## <span data-ttu-id="bb434-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bb434-129">OUTPUTS</span></span>

### <span data-ttu-id="bb434-130">Microsoft. Azure. Commands. Profile. Models. PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="bb434-130">Microsoft.Azure.Commands.Profile.Models.PSResourceGroup</span></span>

## <span data-ttu-id="bb434-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bb434-131">NOTES</span></span>

## <span data-ttu-id="bb434-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bb434-132">RELATED LINKS</span></span>
