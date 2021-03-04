---
external help file: ''
Module Name: Az.HealthBot
online version: https://docs.microsoft.com/powershell/module/az.healthbot/new-azhealthbot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/New-AzHealthBot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/New-AzHealthBot.md
ms.openlocfilehash: b9c4e4cd55f81449497b0d397574c3eeec64d2d2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893305"
---
# <span data-ttu-id="ef913-101">New-AzHealthBot</span><span class="sxs-lookup"><span data-stu-id="ef913-101">New-AzHealthBot</span></span>

## <span data-ttu-id="ef913-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef913-102">SYNOPSIS</span></span>
<span data-ttu-id="ef913-103">Crie um novo HealthBot.</span><span class="sxs-lookup"><span data-stu-id="ef913-103">Create a new HealthBot.</span></span>

## <span data-ttu-id="ef913-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ef913-104">SYNTAX</span></span>

```
New-AzHealthBot -Name <String> -ResourceGroupName <String> -Location <String> -Sku <SkuName>
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ef913-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ef913-105">DESCRIPTION</span></span>
<span data-ttu-id="ef913-106">Crie um novo HealthBot.</span><span class="sxs-lookup"><span data-stu-id="ef913-106">Create a new HealthBot.</span></span>

## <span data-ttu-id="ef913-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ef913-107">EXAMPLES</span></span>

### <span data-ttu-id="ef913-108">Exemplo 1: Criar novo HealthBot</span><span class="sxs-lookup"><span data-stu-id="ef913-108">Example 1: Create new HealthBot</span></span>
```powershell
PS C:\> New-AzHealthBot -Name yourihealthbot1 -ResourceGroupName youriTest -Location eastus -Sku F0

Location Name           SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy             SystemDataLastModifiedByType Type
-------- ----           ------------------- -------------------   ----------------------- ------------------------ ------------------------             ---------------------------- ----
eastus   yourihealthbot 2020/12/29 8:19:10  test@microsoft.com User                    2020/12/29 8:19:14       6db4d6bb-6649-4dc2-84b7-0b5c6894031e Application                  Microsoft.Heal…
```

<span data-ttu-id="ef913-109">Criar novo HealthBot por padrão</span><span class="sxs-lookup"><span data-stu-id="ef913-109">Create new HealthBot By default</span></span>

## <span data-ttu-id="ef913-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ef913-110">PARAMETERS</span></span>

### <span data-ttu-id="ef913-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ef913-111">-AsJob</span></span>
<span data-ttu-id="ef913-112">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="ef913-112">Run the command as a job</span></span>

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

### <span data-ttu-id="ef913-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef913-113">-DefaultProfile</span></span>
<span data-ttu-id="ef913-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ef913-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef913-115">-Location</span><span class="sxs-lookup"><span data-stu-id="ef913-115">-Location</span></span>
<span data-ttu-id="ef913-116">A localização geográfica onde o recurso mora</span><span class="sxs-lookup"><span data-stu-id="ef913-116">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="ef913-117">-Name</span><span class="sxs-lookup"><span data-stu-id="ef913-117">-Name</span></span>
<span data-ttu-id="ef913-118">O nome do recurso Bot.</span><span class="sxs-lookup"><span data-stu-id="ef913-118">The name of the Bot resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BotName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef913-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ef913-119">-NoWait</span></span>
<span data-ttu-id="ef913-120">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="ef913-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ef913-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef913-121">-ResourceGroupName</span></span>
<span data-ttu-id="ef913-122">O nome do grupo de recursos Bot na assinatura do usuário.</span><span class="sxs-lookup"><span data-stu-id="ef913-122">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="ef913-123">-Sku</span><span class="sxs-lookup"><span data-stu-id="ef913-123">-Sku</span></span>
<span data-ttu-id="ef913-124">O nome do SKU HealthBot</span><span class="sxs-lookup"><span data-stu-id="ef913-124">The name of the HealthBot SKU</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Support.SkuName
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef913-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ef913-125">-SubscriptionId</span></span>
<span data-ttu-id="ef913-126">ID da Assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="ef913-126">Azure Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef913-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="ef913-127">-Tag</span></span>
<span data-ttu-id="ef913-128">Marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="ef913-128">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef913-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ef913-129">-Confirm</span></span>
<span data-ttu-id="ef913-130">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ef913-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef913-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef913-131">-WhatIf</span></span>
<span data-ttu-id="ef913-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ef913-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef913-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ef913-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef913-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef913-134">CommonParameters</span></span>
<span data-ttu-id="ef913-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef913-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef913-136">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ef913-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef913-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ef913-137">INPUTS</span></span>

## <span data-ttu-id="ef913-138">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ef913-138">OUTPUTS</span></span>

### <span data-ttu-id="ef913-139">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.Api20201208.IHealthBot</span><span class="sxs-lookup"><span data-stu-id="ef913-139">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.Api20201208.IHealthBot</span></span>

## <span data-ttu-id="ef913-140">NOTES</span><span class="sxs-lookup"><span data-stu-id="ef913-140">NOTES</span></span>

<span data-ttu-id="ef913-141">ALIASES</span><span class="sxs-lookup"><span data-stu-id="ef913-141">ALIASES</span></span>

## <span data-ttu-id="ef913-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ef913-142">RELATED LINKS</span></span>

