---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/set-azdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzDefault.md
ms.openlocfilehash: 25fd0e1cd651f70fa0900c528f9e5297a8eaf2df
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941996"
---
# <span data-ttu-id="4a10f-101">Set-AzDefault</span><span class="sxs-lookup"><span data-stu-id="4a10f-101">Set-AzDefault</span></span>

## <span data-ttu-id="4a10f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4a10f-102">SYNOPSIS</span></span>
<span data-ttu-id="4a10f-103">Define um padrão no contexto atual</span><span class="sxs-lookup"><span data-stu-id="4a10f-103">Sets a default in the current context</span></span>

## <span data-ttu-id="4a10f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4a10f-104">SYNTAX</span></span>

```
Set-AzDefault [-ResourceGroupName <String>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a10f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4a10f-105">DESCRIPTION</span></span>
<span data-ttu-id="4a10f-106">O cmdlet Set-AzDefault adiciona ou altera os padrões no contexto atual.</span><span class="sxs-lookup"><span data-stu-id="4a10f-106">The Set-AzDefault cmdlet adds or changes the defaults in the current context.</span></span>

## <span data-ttu-id="4a10f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4a10f-107">EXAMPLES</span></span>

### <span data-ttu-id="4a10f-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4a10f-108">Example 1</span></span>
```
PS C:\> Set-AzDefault -ResourceGroupName myResourceGroup

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="4a10f-109">Este comando define o grupo de recursos padrão para o grupo de recursos especificado pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="4a10f-109">This command sets the default resource group to the resource group specified by the user.</span></span>

## <span data-ttu-id="4a10f-110">OS</span><span class="sxs-lookup"><span data-stu-id="4a10f-110">PARAMETERS</span></span>

### <span data-ttu-id="4a10f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a10f-111">-DefaultProfile</span></span>
<span data-ttu-id="4a10f-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4a10f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4a10f-113">-Force</span><span class="sxs-lookup"><span data-stu-id="4a10f-113">-Force</span></span>
<span data-ttu-id="4a10f-114">Criar um novo grupo de recursos se o padrão especificado não existir</span><span class="sxs-lookup"><span data-stu-id="4a10f-114">Create a new resource group if specified default does not exist</span></span>

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

### <span data-ttu-id="4a10f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a10f-115">-ResourceGroupName</span></span>
<span data-ttu-id="4a10f-116">Nome do grupo de recursos sendo definido como padrão</span><span class="sxs-lookup"><span data-stu-id="4a10f-116">Name of the resource group being set as default</span></span>

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

### <span data-ttu-id="4a10f-117">-Escopo</span><span class="sxs-lookup"><span data-stu-id="4a10f-117">-Scope</span></span>
<span data-ttu-id="4a10f-118">Determina o escopo das alterações de contexto, por exemplo, se as alterações se aplicam somente ao processo atual ou a todas as sessões iniciadas por esse usuário.</span><span class="sxs-lookup"><span data-stu-id="4a10f-118">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="4a10f-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4a10f-119">-Confirm</span></span>
<span data-ttu-id="4a10f-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4a10f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a10f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a10f-121">-WhatIf</span></span>
<span data-ttu-id="4a10f-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4a10f-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a10f-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4a10f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a10f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a10f-124">CommonParameters</span></span>
<span data-ttu-id="4a10f-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a10f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a10f-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a10f-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a10f-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4a10f-127">INPUTS</span></span>

### <span data-ttu-id="4a10f-128">System. String</span><span class="sxs-lookup"><span data-stu-id="4a10f-128">System.String</span></span>

## <span data-ttu-id="4a10f-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4a10f-129">OUTPUTS</span></span>

### <span data-ttu-id="4a10f-130">Microsoft. Azure. Commands. Profile. Models. PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4a10f-130">Microsoft.Azure.Commands.Profile.Models.PSResourceGroup</span></span>

## <span data-ttu-id="4a10f-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4a10f-131">NOTES</span></span>

## <span data-ttu-id="4a10f-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4a10f-132">RELATED LINKS</span></span>
