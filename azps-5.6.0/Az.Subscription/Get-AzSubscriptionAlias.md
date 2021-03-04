---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/powershell/module/az.subscription/get-azsubscriptionalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Get-AzSubscriptionAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Get-AzSubscriptionAlias.md
ms.openlocfilehash: 0cce48f38b669c713f0d3a193deec64cfce649e8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890048"
---
# <span data-ttu-id="750ed-101">Get-AzSubscriptionAlias</span><span class="sxs-lookup"><span data-stu-id="750ed-101">Get-AzSubscriptionAlias</span></span>

## <span data-ttu-id="750ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="750ed-102">SYNOPSIS</span></span>
<span data-ttu-id="750ed-103">Obtém detalhes de alias de assinatura</span><span class="sxs-lookup"><span data-stu-id="750ed-103">Gets subscription alias details</span></span>

## <span data-ttu-id="750ed-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="750ed-104">SYNTAX</span></span>

```
Get-AzSubscriptionAlias [-AliasName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="750ed-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="750ed-105">DESCRIPTION</span></span>
<span data-ttu-id="750ed-106">O cmdlet **Get-AzSubscriptionAlias** obtém detalhes de alias de assinatura.</span><span class="sxs-lookup"><span data-stu-id="750ed-106">The **Get-AzSubscriptionAlias** cmdlet gets subscription alias details.</span></span>

## <span data-ttu-id="750ed-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="750ed-107">EXAMPLES</span></span>

### <span data-ttu-id="750ed-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="750ed-108">Example 1</span></span>
```powershell
PS C:\> Get-AzSubscriptionAlias -AliasName "ExistingAliasName"
```

<span data-ttu-id="750ed-109">Obtém detalhes de alias de assinatura</span><span class="sxs-lookup"><span data-stu-id="750ed-109">Gets subscription alias details</span></span>

## <span data-ttu-id="750ed-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="750ed-110">PARAMETERS</span></span>

### <span data-ttu-id="750ed-111">-AliasName</span><span class="sxs-lookup"><span data-stu-id="750ed-111">-AliasName</span></span>
<span data-ttu-id="750ed-112">Alias para a assinatura</span><span class="sxs-lookup"><span data-stu-id="750ed-112">Alias for the subscription</span></span>

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

### <span data-ttu-id="750ed-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="750ed-113">-AsJob</span></span>
<span data-ttu-id="750ed-114">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="750ed-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="750ed-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="750ed-115">-DefaultProfile</span></span>
<span data-ttu-id="750ed-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="750ed-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="750ed-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="750ed-117">-Confirm</span></span>
<span data-ttu-id="750ed-118">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="750ed-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="750ed-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="750ed-119">-WhatIf</span></span>
<span data-ttu-id="750ed-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="750ed-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="750ed-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="750ed-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="750ed-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="750ed-122">CommonParameters</span></span>
<span data-ttu-id="750ed-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="750ed-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="750ed-124">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="750ed-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="750ed-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="750ed-125">INPUTS</span></span>

### <span data-ttu-id="750ed-126">Nenhum</span><span class="sxs-lookup"><span data-stu-id="750ed-126">None</span></span>

## <span data-ttu-id="750ed-127">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="750ed-127">OUTPUTS</span></span>

### <span data-ttu-id="750ed-128">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="750ed-128">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="750ed-129">NOTES</span><span class="sxs-lookup"><span data-stu-id="750ed-129">NOTES</span></span>

## <span data-ttu-id="750ed-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="750ed-130">RELATED LINKS</span></span>
