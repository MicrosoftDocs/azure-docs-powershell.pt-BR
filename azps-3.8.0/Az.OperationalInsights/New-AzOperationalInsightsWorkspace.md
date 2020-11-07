---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 4682807D-34E8-4057-8894-36820447067B
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 22cc5c18e2c3cf21472426160d667c7890f04d4f
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93947295"
---
# <span data-ttu-id="bd9d6-101">New-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="bd9d6-101">New-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="bd9d6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bd9d6-102">SYNOPSIS</span></span>
<span data-ttu-id="bd9d6-103">Cria um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="bd9d6-103">Creates a workspace.</span></span>

## <span data-ttu-id="bd9d6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bd9d6-104">SYNTAX</span></span>

```
New-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Sku] <String>] [[-CustomerId] <Guid>] [[-Tag] <Hashtable>] [[-RetentionInDays] <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd9d6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bd9d6-105">DESCRIPTION</span></span>
<span data-ttu-id="bd9d6-106">O cmdlet **New-AzOperationalInsightsWorkspace** cria um espaço de trabalho no grupo de recursos e na localização especificados.</span><span class="sxs-lookup"><span data-stu-id="bd9d6-106">The **New-AzOperationalInsightsWorkspace** cmdlet creates a workspace in the specified resource group and location.</span></span>

## <span data-ttu-id="bd9d6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bd9d6-107">EXAMPLES</span></span>

### <span data-ttu-id="bd9d6-108">Exemplo 1: criar um espaço de trabalho por nome</span><span class="sxs-lookup"><span data-stu-id="bd9d6-108">Example 1: Create a workspace by name</span></span>
```
PS C:\>New-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Location "East US" -Sku "Standard"
```

<span data-ttu-id="bd9d6-109">Esse comando cria um espaço de trabalho de SKU padrão chamado MyWorkspace no grupo de recursos chamado ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="bd9d6-109">This command creates a standard SKU workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="bd9d6-110">Exemplo 2: criar um espaço de trabalho e vinculá-lo a uma conta existente</span><span class="sxs-lookup"><span data-stu-id="bd9d6-110">Example 2: Create a workspace and link it to an existing account</span></span>
```
PS C:\>$OILinkTargets = Get-AzOperationalInsightsLinkTargets

PS C:\>$OILinkTargets[0] | New-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku "Standard"
```

<span data-ttu-id="bd9d6-111">O primeiro comando usa o cmdlet Get-AzOperationalInsightsLinkTargets para obter destinos de link de conta de insights operacionais e, em seguida, armazena-os na variável $OILinkTargets.</span><span class="sxs-lookup"><span data-stu-id="bd9d6-111">The first command uses the Get-AzOperationalInsightsLinkTargets cmdlet to get Operational Insights account link targets, and then stores them in the $OILinkTargets variable.</span></span>
<span data-ttu-id="bd9d6-112">O segundo comando passa o destino do link da primeira conta no $OILinkTargets para o cmdlet **New-AzOperationalInsightsWorkspace** usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="bd9d6-112">The second command passes the first account link target in $OILinkTargets to the **New-AzOperationalInsightsWorkspace** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="bd9d6-113">O comando cria um espaço de trabalho de SKU padrão chamado MyWorkspace que está vinculado à primeira conta de insights operacionais em $OILinkTargets.</span><span class="sxs-lookup"><span data-stu-id="bd9d6-113">The command creates a standard SKU workspace named MyWorkspace that is linked to the first Operational Insights account in $OILinkTargets.</span></span>

## <span data-ttu-id="bd9d6-114">OS</span><span class="sxs-lookup"><span data-stu-id="bd9d6-114">PARAMETERS</span></span>

### <span data-ttu-id="bd9d6-115">-CustomerId</span><span class="sxs-lookup"><span data-stu-id="bd9d6-115">-CustomerId</span></span>
<span data-ttu-id="bd9d6-116">Especifica a conta para a qual esse espaço de trabalho será vinculado.</span><span class="sxs-lookup"><span data-stu-id="bd9d6-116">Specifies the account to which this workspace will be linked.</span></span>
<span data-ttu-id="bd9d6-117">O cmdlet Get-AzOperationalInsightsLinkTargets também pode ser usado para listar as contas potenciais.</span><span class="sxs-lookup"><span data-stu-id="bd9d6-117">The Get-AzOperationalInsightsLinkTargets cmdlet can also be used to list the potential accounts.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd9d6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd9d6-118">-DefaultProfile</span></span>
<span data-ttu-id="bd9d6-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="bd9d6-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bd9d6-120">-Force</span><span class="sxs-lookup"><span data-stu-id="bd9d6-120">-Force</span></span>
<span data-ttu-id="bd9d6-121">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="bd9d6-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="bd9d6-122">-Local</span><span class="sxs-lookup"><span data-stu-id="bd9d6-122">-Location</span></span>
<span data-ttu-id="bd9d6-123">Especifica o local no qual criar o espaço de trabalho, por exemplo, leste EUA ou oeste europeu.</span><span class="sxs-lookup"><span data-stu-id="bd9d6-123">Specifies the location in which to create the workspace, for example, East US or West Europe.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd9d6-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="bd9d6-124">-Name</span></span>
<span data-ttu-id="bd9d6-125">Especifica o nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="bd9d6-125">Specifies the name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd9d6-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd9d6-126">-ResourceGroupName</span></span>
<span data-ttu-id="bd9d6-127">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="bd9d6-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="bd9d6-128">O espaço de trabalho é criado neste grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="bd9d6-128">The workspace is created in this resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd9d6-129">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="bd9d6-129">-RetentionInDays</span></span>
<span data-ttu-id="bd9d6-130">A retenção de dados do espaço de trabalho em dias.</span><span class="sxs-lookup"><span data-stu-id="bd9d6-130">The workspace data retention in days.</span></span> <span data-ttu-id="bd9d6-131">730 dias é o máximo permitido para todas as outras SKUs</span><span class="sxs-lookup"><span data-stu-id="bd9d6-131">730 days is the maximum allowed for all other Skus</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd9d6-132">-SKU</span><span class="sxs-lookup"><span data-stu-id="bd9d6-132">-Sku</span></span>
<span data-ttu-id="bd9d6-133">Especifica a camada de serviço do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="bd9d6-133">Specifies the service tier of the workspace.</span></span> <span data-ttu-id="bd9d6-134">Para obter mais informações sobre qual valor usar, verifique https://docs.microsoft.com/en-us/azure/azure-monitor/platform/manage-cost-storage#legacy-pricing-tiers .</span><span class="sxs-lookup"><span data-stu-id="bd9d6-134">For more information regarding which value to use please check https://docs.microsoft.com/en-us/azure/azure-monitor/platform/manage-cost-storage#legacy-pricing-tiers.</span></span>
<span data-ttu-id="bd9d6-135">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="bd9d6-135">Valid values are:</span></span>
- <span data-ttu-id="bd9d6-136">gratuito</span><span class="sxs-lookup"><span data-stu-id="bd9d6-136">free</span></span>
- <span data-ttu-id="bd9d6-137">pergb2018</span><span class="sxs-lookup"><span data-stu-id="bd9d6-137">pergb2018</span></span>
- <span data-ttu-id="bd9d6-138">PerNode</span><span class="sxs-lookup"><span data-stu-id="bd9d6-138">pernode</span></span>
- <span data-ttu-id="bd9d6-139">gratifica</span><span class="sxs-lookup"><span data-stu-id="bd9d6-139">premium</span></span>
- <span data-ttu-id="bd9d6-140">autônoma</span><span class="sxs-lookup"><span data-stu-id="bd9d6-140">standalone</span></span>
- <span data-ttu-id="bd9d6-141">oficial</span><span class="sxs-lookup"><span data-stu-id="bd9d6-141">standard</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: free, pergb2018, pernode, premium, standalone, standard

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd9d6-142">-Marca</span><span class="sxs-lookup"><span data-stu-id="bd9d6-142">-Tag</span></span>
<span data-ttu-id="bd9d6-143">As marcas de recurso do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="bd9d6-143">The resource tags for the workspace.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd9d6-144">-Confirme</span><span class="sxs-lookup"><span data-stu-id="bd9d6-144">-Confirm</span></span>
<span data-ttu-id="bd9d6-145">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd9d6-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd9d6-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd9d6-146">-WhatIf</span></span>
<span data-ttu-id="bd9d6-147">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bd9d6-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd9d6-148">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bd9d6-148">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd9d6-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd9d6-149">CommonParameters</span></span>
<span data-ttu-id="bd9d6-150">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd9d6-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd9d6-151">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd9d6-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd9d6-152">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bd9d6-152">INPUTS</span></span>

### <span data-ttu-id="bd9d6-153">System. String</span><span class="sxs-lookup"><span data-stu-id="bd9d6-153">System.String</span></span>

### <span data-ttu-id="bd9d6-154">System. Nullable ' 1 [[System. GUID, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="bd9d6-154">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="bd9d6-155">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="bd9d6-155">System.Collections.Hashtable</span></span>

### <span data-ttu-id="bd9d6-156">System. Nullable ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="bd9d6-156">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="bd9d6-157">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bd9d6-157">OUTPUTS</span></span>

### <span data-ttu-id="bd9d6-158">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="bd9d6-158">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="bd9d6-159">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bd9d6-159">NOTES</span></span>

<span data-ttu-id="bd9d6-160">Um novo modelo de preços foi lançado.</span><span class="sxs-lookup"><span data-stu-id="bd9d6-160">A new pricing model has been released.</span></span> <span data-ttu-id="bd9d6-161">Se você for um CSP que significa que precisa usar "autônomo" para a SKU.</span><span class="sxs-lookup"><span data-stu-id="bd9d6-161">If you are a CSP that means that you have to use "standalone" for the sku.</span></span> <span data-ttu-id="bd9d6-162">Em segundo plano, a SKU será alterada para pergb2018.</span><span class="sxs-lookup"><span data-stu-id="bd9d6-162">Behind the scenes, the sku will be changed to pergb2018.</span></span> <span data-ttu-id="bd9d6-163">Para obter mais informações, confira o seguinte: https://docs.microsoft.com/en-us/azure/monitoring-and-diagnostics/monitoring-usage-and-estimated-costs#new-pricing-model</span><span class="sxs-lookup"><span data-stu-id="bd9d6-163">For more information, please see the following: https://docs.microsoft.com/en-us/azure/monitoring-and-diagnostics/monitoring-usage-and-estimated-costs#new-pricing-model</span></span>

## <span data-ttu-id="bd9d6-164">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bd9d6-164">RELATED LINKS</span></span>

[<span data-ttu-id="bd9d6-165">Cmdlets do Azure Operational insights</span><span class="sxs-lookup"><span data-stu-id="bd9d6-165">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)
