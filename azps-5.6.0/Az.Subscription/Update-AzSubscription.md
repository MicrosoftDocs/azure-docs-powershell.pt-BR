---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/powershell/module/az.subscription/update-azsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Update-AzSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Update-AzSubscription.md
ms.openlocfilehash: 0fe030e3ef4dfcb8e43ba436d37d582871e55a5b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888403"
---
# <span data-ttu-id="54eba-101">Update-AzSubscription</span><span class="sxs-lookup"><span data-stu-id="54eba-101">Update-AzSubscription</span></span>

## <span data-ttu-id="54eba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54eba-102">SYNOPSIS</span></span>
<span data-ttu-id="54eba-103">Atualiza uma assinatura do Azure</span><span class="sxs-lookup"><span data-stu-id="54eba-103">Updates an Azure Subscription</span></span>

## <span data-ttu-id="54eba-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="54eba-104">SYNTAX</span></span>

```
Update-AzSubscription -SubscriptionId <String> -Action <String> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54eba-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="54eba-105">DESCRIPTION</span></span>
<span data-ttu-id="54eba-106">O cmdlet **Update-AzSubscription** atualiza uma assinatura do Azure</span><span class="sxs-lookup"><span data-stu-id="54eba-106">The **Update-AzSubscription** cmdlet updates an Azure subscription</span></span>

## <span data-ttu-id="54eba-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="54eba-107">EXAMPLES</span></span>

### <span data-ttu-id="54eba-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="54eba-108">Example 1</span></span>
```powershell
PS C:\> Update-AzSubscription -SubscriptionId "86869d42-1782-4337-98b0-c905fb937d46" -Action "Cancel"

Name        : My Subscription
Id          : 86869d42-1782-4337-98b0-c905fb937d46
TenantId    : a5dcb057-fd83-4384-9d49-5198004d33a5
State       : Enabled
```

<span data-ttu-id="54eba-109">Atualiza a assinatura</span><span class="sxs-lookup"><span data-stu-id="54eba-109">Updates the subscription</span></span>

## <span data-ttu-id="54eba-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="54eba-110">PARAMETERS</span></span>

### <span data-ttu-id="54eba-111">-Action</span><span class="sxs-lookup"><span data-stu-id="54eba-111">-Action</span></span>
<span data-ttu-id="54eba-112">Ação a executar na assinatura</span><span class="sxs-lookup"><span data-stu-id="54eba-112">Action to perform on subscription</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54eba-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="54eba-113">-AsJob</span></span>
<span data-ttu-id="54eba-114">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="54eba-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="54eba-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54eba-115">-DefaultProfile</span></span>
<span data-ttu-id="54eba-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="54eba-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54eba-117">-Name</span><span class="sxs-lookup"><span data-stu-id="54eba-117">-Name</span></span>
<span data-ttu-id="54eba-118">Nome da assinatura</span><span class="sxs-lookup"><span data-stu-id="54eba-118">Name of the subscription</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54eba-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="54eba-119">-SubscriptionId</span></span>
<span data-ttu-id="54eba-120">ID da assinatura para atualização</span><span class="sxs-lookup"><span data-stu-id="54eba-120">Subscription Id to update</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54eba-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="54eba-121">-Confirm</span></span>
<span data-ttu-id="54eba-122">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="54eba-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54eba-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54eba-123">-WhatIf</span></span>
<span data-ttu-id="54eba-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="54eba-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54eba-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="54eba-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54eba-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54eba-126">CommonParameters</span></span>
<span data-ttu-id="54eba-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54eba-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54eba-128">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="54eba-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54eba-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="54eba-129">INPUTS</span></span>

### <span data-ttu-id="54eba-130">Nenhum</span><span class="sxs-lookup"><span data-stu-id="54eba-130">None</span></span>

## <span data-ttu-id="54eba-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="54eba-131">OUTPUTS</span></span>

### <span data-ttu-id="54eba-132">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="54eba-132">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="54eba-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="54eba-133">NOTES</span></span>

## <span data-ttu-id="54eba-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="54eba-134">RELATED LINKS</span></span>
