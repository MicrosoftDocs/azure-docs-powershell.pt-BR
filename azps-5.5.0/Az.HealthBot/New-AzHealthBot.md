---
external help file: ''
Module Name: Az.HealthBot
online version: https://docs.microsoft.com/en-us/powershell/module/az.healthbot/new-azhealthbot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/New-AzHealthBot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/New-AzHealthBot.md
ms.openlocfilehash: dc39a7324f89e0a45efd4b631fb24a2e000d5e72
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111861"
---
# <span data-ttu-id="ee355-101">New-AzHealthBot</span><span class="sxs-lookup"><span data-stu-id="ee355-101">New-AzHealthBot</span></span>

## <span data-ttu-id="ee355-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ee355-102">SYNOPSIS</span></span>
<span data-ttu-id="ee355-103">Crie um novo HealthBot.</span><span class="sxs-lookup"><span data-stu-id="ee355-103">Create a new HealthBot.</span></span>

## <span data-ttu-id="ee355-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ee355-104">SYNTAX</span></span>

```
New-AzHealthBot -Name <String> -ResourceGroupName <String> -Location <String> -Sku <SkuName>
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ee355-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="ee355-105">DESCRIPTION</span></span>
<span data-ttu-id="ee355-106">Crie um novo HealthBot.</span><span class="sxs-lookup"><span data-stu-id="ee355-106">Create a new HealthBot.</span></span>

## <span data-ttu-id="ee355-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ee355-107">EXAMPLES</span></span>

### <span data-ttu-id="ee355-108">Exemplo 1: Criar novo HealthBot</span><span class="sxs-lookup"><span data-stu-id="ee355-108">Example 1: Create new HealthBot</span></span>
```powershell
PS C:\> New-AzHealthBot -Name yourihealthbot1 -ResourceGroupName youriTest -Location eastus -Sku F0

Location Name           SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy             SystemDataLastModifiedByType Type
-------- ----           ------------------- -------------------   ----------------------- ------------------------ ------------------------             ---------------------------- ----
eastus   yourihealthbot 2020/12/29 8:19:10  test@microsoft.com User                    2020/12/29 8:19:14       6db4d6bb-6649-4dc2-84b7-0b5c6894031e Application                  Microsoft.Heal…
```

<span data-ttu-id="ee355-109">Criar novo HealthBot por padrão</span><span class="sxs-lookup"><span data-stu-id="ee355-109">Create new HealthBot By default</span></span>

## <span data-ttu-id="ee355-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ee355-110">PARAMETERS</span></span>

### <span data-ttu-id="ee355-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ee355-111">-AsJob</span></span>
<span data-ttu-id="ee355-112">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="ee355-112">Run the command as a job</span></span>

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

### <span data-ttu-id="ee355-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee355-113">-DefaultProfile</span></span>
<span data-ttu-id="ee355-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ee355-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee355-115">-Local</span><span class="sxs-lookup"><span data-stu-id="ee355-115">-Location</span></span>
<span data-ttu-id="ee355-116">A localização geográfica onde o recurso reside</span><span class="sxs-lookup"><span data-stu-id="ee355-116">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="ee355-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="ee355-117">-Name</span></span>
<span data-ttu-id="ee355-118">O nome do recurso bot.</span><span class="sxs-lookup"><span data-stu-id="ee355-118">The name of the Bot resource.</span></span>

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

### <span data-ttu-id="ee355-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ee355-119">-NoWait</span></span>
<span data-ttu-id="ee355-120">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="ee355-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ee355-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee355-121">-ResourceGroupName</span></span>
<span data-ttu-id="ee355-122">O nome do grupo de recursos do Bot na assinatura do usuário.</span><span class="sxs-lookup"><span data-stu-id="ee355-122">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="ee355-123">-SKU</span><span class="sxs-lookup"><span data-stu-id="ee355-123">-Sku</span></span>
<span data-ttu-id="ee355-124">O nome da SKU do HealthBot</span><span class="sxs-lookup"><span data-stu-id="ee355-124">The name of the HealthBot SKU</span></span>

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

### <span data-ttu-id="ee355-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ee355-125">-SubscriptionId</span></span>
<span data-ttu-id="ee355-126">ID de Assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="ee355-126">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="ee355-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="ee355-127">-Tag</span></span>
<span data-ttu-id="ee355-128">Marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="ee355-128">Resource tags.</span></span>

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

### <span data-ttu-id="ee355-129">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="ee355-129">-Confirm</span></span>
<span data-ttu-id="ee355-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee355-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee355-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee355-131">-WhatIf</span></span>
<span data-ttu-id="ee355-132">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="ee355-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee355-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ee355-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee355-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee355-134">CommonParameters</span></span>
<span data-ttu-id="ee355-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee355-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee355-136">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ee355-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee355-137">Entradas</span><span class="sxs-lookup"><span data-stu-id="ee355-137">INPUTS</span></span>

## <span data-ttu-id="ee355-138">Saídas</span><span class="sxs-lookup"><span data-stu-id="ee355-138">OUTPUTS</span></span>

### <span data-ttu-id="ee355-139">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.Api20201208.IHealthBot</span><span class="sxs-lookup"><span data-stu-id="ee355-139">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.Api20201208.IHealthBot</span></span>

## <span data-ttu-id="ee355-140">Notas</span><span class="sxs-lookup"><span data-stu-id="ee355-140">NOTES</span></span>

<span data-ttu-id="ee355-141">Aliases</span><span class="sxs-lookup"><span data-stu-id="ee355-141">ALIASES</span></span>

## <span data-ttu-id="ee355-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ee355-142">RELATED LINKS</span></span>

