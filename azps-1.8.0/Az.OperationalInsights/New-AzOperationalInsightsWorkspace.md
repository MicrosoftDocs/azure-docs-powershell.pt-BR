---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 4682807D-34E8-4057-8894-36820447067B
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 863b83cbab64d791e55f8cfc2719d66be64fcac6
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93785075"
---
# <span data-ttu-id="7d2be-101">New-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="7d2be-101">New-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="7d2be-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7d2be-102">SYNOPSIS</span></span>
<span data-ttu-id="7d2be-103">Cria um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="7d2be-103">Creates a workspace.</span></span>

## <span data-ttu-id="7d2be-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7d2be-104">SYNTAX</span></span>

```
New-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Sku] <String>] [[-CustomerId] <Guid>] [[-Tag] <Hashtable>] [[-RetentionInDays] <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d2be-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7d2be-105">DESCRIPTION</span></span>
<span data-ttu-id="7d2be-106">O cmdlet **New-AzOperationalInsightsWorkspace** cria um espaço de trabalho no grupo de recursos e na localização especificados.</span><span class="sxs-lookup"><span data-stu-id="7d2be-106">The **New-AzOperationalInsightsWorkspace** cmdlet creates a workspace in the specified resource group and location.</span></span>

## <span data-ttu-id="7d2be-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7d2be-107">EXAMPLES</span></span>

### <span data-ttu-id="7d2be-108">Exemplo 1: criar um espaço de trabalho por nome</span><span class="sxs-lookup"><span data-stu-id="7d2be-108">Example 1: Create a workspace by name</span></span>
```
PS C:\>New-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Location "East US" -Sku "Standard"
```

<span data-ttu-id="7d2be-109">Esse comando cria um espaço de trabalho de SKU padrão chamado MyWorkspace no grupo de recursos chamado ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="7d2be-109">This command creates a standard SKU workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="7d2be-110">Exemplo 2: criar um espaço de trabalho e vinculá-lo a uma conta existente</span><span class="sxs-lookup"><span data-stu-id="7d2be-110">Example 2: Create a workspace and link it to an existing account</span></span>
```
PS C:\>$OILinkTargets = Get-AzOperationalInsightsLinkTargets

PS C:\>$OILinkTargets[0] | New-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku "Standard"
```

<span data-ttu-id="7d2be-111">O primeiro comando usa o cmdlet Get-AzOperationalInsightsLinkTargets para obter destinos de link de conta de insights operacionais e, em seguida, armazena-os na variável $OILinkTargets.</span><span class="sxs-lookup"><span data-stu-id="7d2be-111">The first command uses the Get-AzOperationalInsightsLinkTargets cmdlet to get Operational Insights account link targets, and then stores them in the $OILinkTargets variable.</span></span>
<span data-ttu-id="7d2be-112">O segundo comando passa o destino do link da primeira conta no $OILinkTargets para o cmdlet **New-AzOperationalInsightsWorkspace** usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="7d2be-112">The second command passes the first account link target in $OILinkTargets to the **New-AzOperationalInsightsWorkspace** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="7d2be-113">O comando cria um espaço de trabalho de SKU padrão chamado MyWorkspace que está vinculado à primeira conta de insights operacionais em $OILinkTargets.</span><span class="sxs-lookup"><span data-stu-id="7d2be-113">The command creates a standard SKU workspace named MyWorkspace that is linked to the first Operational Insights account in $OILinkTargets.</span></span>

## <span data-ttu-id="7d2be-114">OS</span><span class="sxs-lookup"><span data-stu-id="7d2be-114">PARAMETERS</span></span>

### <span data-ttu-id="7d2be-115">-CustomerId</span><span class="sxs-lookup"><span data-stu-id="7d2be-115">-CustomerId</span></span>
<span data-ttu-id="7d2be-116">Especifica a conta para a qual esse espaço de trabalho será vinculado.</span><span class="sxs-lookup"><span data-stu-id="7d2be-116">Specifies the account to which this workspace will be linked.</span></span>
<span data-ttu-id="7d2be-117">O cmdlet Get-AzOperationalInsightsLinkTargets também pode ser usado para listar as contas potenciais.</span><span class="sxs-lookup"><span data-stu-id="7d2be-117">The Get-AzOperationalInsightsLinkTargets cmdlet can also be used to list the potential accounts.</span></span>

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

### <span data-ttu-id="7d2be-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d2be-118">-DefaultProfile</span></span>
<span data-ttu-id="7d2be-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="7d2be-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7d2be-120">-Force</span><span class="sxs-lookup"><span data-stu-id="7d2be-120">-Force</span></span>
<span data-ttu-id="7d2be-121">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="7d2be-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7d2be-122">-Local</span><span class="sxs-lookup"><span data-stu-id="7d2be-122">-Location</span></span>
<span data-ttu-id="7d2be-123">Especifica o local no qual criar o espaço de trabalho, por exemplo, leste EUA ou oeste europeu.</span><span class="sxs-lookup"><span data-stu-id="7d2be-123">Specifies the location in which to create the workspace, for example, East US or West Europe.</span></span>

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

### <span data-ttu-id="7d2be-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="7d2be-124">-Name</span></span>
<span data-ttu-id="7d2be-125">Especifica o nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="7d2be-125">Specifies the name of the workspace.</span></span>

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

### <span data-ttu-id="7d2be-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d2be-126">-ResourceGroupName</span></span>
<span data-ttu-id="7d2be-127">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="7d2be-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="7d2be-128">O espaço de trabalho é criado neste grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7d2be-128">The workspace is created in this resource group.</span></span>

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

### <span data-ttu-id="7d2be-129">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="7d2be-129">-RetentionInDays</span></span>
<span data-ttu-id="7d2be-130">A retenção de dados do espaço de trabalho em dias.</span><span class="sxs-lookup"><span data-stu-id="7d2be-130">The workspace data retention in days.</span></span> <span data-ttu-id="7d2be-131">730 dias é o máximo permitido para todas as outras SKUs</span><span class="sxs-lookup"><span data-stu-id="7d2be-131">730 days is the maximum allowed for all other Skus</span></span>

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

### <span data-ttu-id="7d2be-132">-SKU</span><span class="sxs-lookup"><span data-stu-id="7d2be-132">-Sku</span></span>
<span data-ttu-id="7d2be-133">Especifica a camada de serviço do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="7d2be-133">Specifies the service tier of the workspace.</span></span>
<span data-ttu-id="7d2be-134">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="7d2be-134">Valid values are:</span></span>
- <span data-ttu-id="7d2be-135">gratuito</span><span class="sxs-lookup"><span data-stu-id="7d2be-135">free</span></span>
- <span data-ttu-id="7d2be-136">oficial</span><span class="sxs-lookup"><span data-stu-id="7d2be-136">standard</span></span>
- <span data-ttu-id="7d2be-137">autônoma</span><span class="sxs-lookup"><span data-stu-id="7d2be-137">standalone</span></span>
- <span data-ttu-id="7d2be-138">gratifica</span><span class="sxs-lookup"><span data-stu-id="7d2be-138">premium</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: free, standard, premium, pernode, standalone

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d2be-139">-Marca</span><span class="sxs-lookup"><span data-stu-id="7d2be-139">-Tag</span></span>
<span data-ttu-id="7d2be-140">As marcas de recurso do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="7d2be-140">The resource tags for the workspace.</span></span>

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

### <span data-ttu-id="7d2be-141">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7d2be-141">-Confirm</span></span>
<span data-ttu-id="7d2be-142">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d2be-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d2be-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d2be-143">-WhatIf</span></span>
<span data-ttu-id="7d2be-144">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7d2be-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d2be-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7d2be-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d2be-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d2be-146">CommonParameters</span></span>
<span data-ttu-id="7d2be-147">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d2be-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d2be-148">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d2be-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d2be-149">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7d2be-149">INPUTS</span></span>

### <span data-ttu-id="7d2be-150">System. String</span><span class="sxs-lookup"><span data-stu-id="7d2be-150">System.String</span></span>

### <span data-ttu-id="7d2be-151">System. Nullable ' 1 [[System. GUID, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="7d2be-151">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="7d2be-152">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="7d2be-152">System.Collections.Hashtable</span></span>

### <span data-ttu-id="7d2be-153">System. Nullable ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="7d2be-153">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="7d2be-154">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7d2be-154">OUTPUTS</span></span>

### <span data-ttu-id="7d2be-155">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="7d2be-155">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="7d2be-156">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7d2be-156">NOTES</span></span>

<span data-ttu-id="7d2be-157">Um novo modelo de preços foi lançado.</span><span class="sxs-lookup"><span data-stu-id="7d2be-157">A new pricing model has been released.</span></span> <span data-ttu-id="7d2be-158">Se você for um CSP que significa que precisa usar "autônomo" para a SKU.</span><span class="sxs-lookup"><span data-stu-id="7d2be-158">If you are a CSP that means that you have to use "standalone" for the sku.</span></span> <span data-ttu-id="7d2be-159">Em segundo plano, a SKU será alterada para pergb2018.</span><span class="sxs-lookup"><span data-stu-id="7d2be-159">Behind the scenes, the sku will be changed to pergb2018.</span></span> <span data-ttu-id="7d2be-160">Para obter mais informações, confira o seguinte: https://docs.microsoft.com/en-us/azure/monitoring-and-diagnostics/monitoring-usage-and-estimated-costs#new-pricing-model</span><span class="sxs-lookup"><span data-stu-id="7d2be-160">For more information, please see the following: https://docs.microsoft.com/en-us/azure/monitoring-and-diagnostics/monitoring-usage-and-estimated-costs#new-pricing-model</span></span>

## <span data-ttu-id="7d2be-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7d2be-161">RELATED LINKS</span></span>

[<span data-ttu-id="7d2be-162">Cmdlets do Azure Operational insights</span><span class="sxs-lookup"><span data-stu-id="7d2be-162">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)
