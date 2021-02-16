---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 4682807D-34E8-4057-8894-36820447067B
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: a2e0bc21546dad414ee8782acd0a1505ed1e5489
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399117"
---
# <span data-ttu-id="22bb0-101">New-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="22bb0-101">New-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="22bb0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="22bb0-102">SYNOPSIS</span></span>
<span data-ttu-id="22bb0-103">Cria um espaço de trabalho ou restaura um espaço de trabalho excluído suavemente.</span><span class="sxs-lookup"><span data-stu-id="22bb0-103">Creates a workspace, or restore a soft-deleted workspace.</span></span>

## <span data-ttu-id="22bb0-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="22bb0-104">SYNTAX</span></span>

```
New-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Sku] <String>] [[-Tag] <Hashtable>] [[-RetentionInDays] <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [[-PublicNetworkAccessForIngestion] <String>]
 [[-PublicNetworkAccessForQuery] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22bb0-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="22bb0-105">DESCRIPTION</span></span>
<span data-ttu-id="22bb0-106">O cmdlet **New-AzOperationalInsightsWorkspace** cria um espaço de trabalho no grupo de recursos e no local especificados.</span><span class="sxs-lookup"><span data-stu-id="22bb0-106">The **New-AzOperationalInsightsWorkspace** cmdlet creates a workspace in the specified resource group and location.</span></span> <span data-ttu-id="22bb0-107">Ou restaure um espaço de trabalho excluído suavemente.</span><span class="sxs-lookup"><span data-stu-id="22bb0-107">Or restore a soft-deleted workspace.</span></span>

## <span data-ttu-id="22bb0-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="22bb0-108">EXAMPLES</span></span>

### <span data-ttu-id="22bb0-109">Exemplo 1: Criar um espaço de trabalho por nome</span><span class="sxs-lookup"><span data-stu-id="22bb0-109">Example 1: Create a workspace by name</span></span>
```
PS C:\>New-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Location "East US" -Sku "Standard"
```

<span data-ttu-id="22bb0-110">Esse comando cria um espaço de trabalho SKU padrão chamado MyWorkspace no grupo de recursos chamado ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="22bb0-110">This command creates a standard SKU workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="22bb0-111">Exemplo 2: Criar um espaço de trabalho e vinculá-lo a uma conta existente</span><span class="sxs-lookup"><span data-stu-id="22bb0-111">Example 2: Create a workspace and link it to an existing account</span></span>
```
PS C:\>$OILinkTargets = Get-AzOperationalInsightsLinkTargets

PS C:\>$OILinkTargets[0] | New-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku "Standard"
```

<span data-ttu-id="22bb0-112">O primeiro comando usa o cmdlet Get-AzOperationalInsightsLinkTargets para obter os destinos de link da conta do Insights Operacionais e, em seguida, os armazena na variável $OILinkTargets dados.</span><span class="sxs-lookup"><span data-stu-id="22bb0-112">The first command uses the Get-AzOperationalInsightsLinkTargets cmdlet to get Operational Insights account link targets, and then stores them in the $OILinkTargets variable.</span></span>
<span data-ttu-id="22bb0-113">O segundo comando passa o primeiro destino de link de conta no $OILinkTargets para o cmdlet **New-AzOperationalInsightsWorkspace** usando o operador de pipeline.</span><span class="sxs-lookup"><span data-stu-id="22bb0-113">The second command passes the first account link target in $OILinkTargets to the **New-AzOperationalInsightsWorkspace** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="22bb0-114">O comando cria um espaço de trabalho SKU padrão chamado MyWorkspace que está vinculado à primeira conta do Insights Operacionais no $OILinkTargets.</span><span class="sxs-lookup"><span data-stu-id="22bb0-114">The command creates a standard SKU workspace named MyWorkspace that is linked to the first Operational Insights account in $OILinkTargets.</span></span>

## <span data-ttu-id="22bb0-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="22bb0-115">PARAMETERS</span></span>

### <span data-ttu-id="22bb0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22bb0-116">-DefaultProfile</span></span>
<span data-ttu-id="22bb0-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="22bb0-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="22bb0-118">-Forçar</span><span class="sxs-lookup"><span data-stu-id="22bb0-118">-Force</span></span>
<span data-ttu-id="22bb0-119">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="22bb0-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="22bb0-120">-Local</span><span class="sxs-lookup"><span data-stu-id="22bb0-120">-Location</span></span>
<span data-ttu-id="22bb0-121">Especifica o local no qual criar o espaço de trabalho, por exemplo, Leste dos EUA ou Europa Ocidental.</span><span class="sxs-lookup"><span data-stu-id="22bb0-121">Specifies the location in which to create the workspace, for example, East US or West Europe.</span></span>

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

### <span data-ttu-id="22bb0-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="22bb0-122">-Name</span></span>
<span data-ttu-id="22bb0-123">Especifica o nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="22bb0-123">Specifies the name of the workspace.</span></span>

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

### <span data-ttu-id="22bb0-124">-PublicNetworkAccessForIngestion</span><span class="sxs-lookup"><span data-stu-id="22bb0-124">-PublicNetworkAccessForIngestion</span></span>
<span data-ttu-id="22bb0-125">O tipo de acesso à rede para acessar a ingestão de espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="22bb0-125">The network access type for accessing workspace ingestion.</span></span> <span data-ttu-id="22bb0-126">O valor deve ser "Habilitado" ou "Desabilitado"</span><span class="sxs-lookup"><span data-stu-id="22bb0-126">Value should be 'Enabled' or 'Disabled'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22bb0-127">-PublicNetworkAccessForQuery</span><span class="sxs-lookup"><span data-stu-id="22bb0-127">-PublicNetworkAccessForQuery</span></span>
<span data-ttu-id="22bb0-128">O tipo de acesso à rede para acessar a consulta de espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="22bb0-128">The network access type for accessing workspace query.</span></span> <span data-ttu-id="22bb0-129">O valor deve ser "Habilitado" ou "Desabilitado"</span><span class="sxs-lookup"><span data-stu-id="22bb0-129">Value should be 'Enabled' or 'Disabled'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22bb0-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22bb0-130">-ResourceGroupName</span></span>
<span data-ttu-id="22bb0-131">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="22bb0-131">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="22bb0-132">O espaço de trabalho é criado neste grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="22bb0-132">The workspace is created in this resource group.</span></span>

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

### <span data-ttu-id="22bb0-133">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="22bb0-133">-RetentionInDays</span></span>
<span data-ttu-id="22bb0-134">A retenção de dados do espaço de trabalho em dias.</span><span class="sxs-lookup"><span data-stu-id="22bb0-134">The workspace data retention in days.</span></span> <span data-ttu-id="22bb0-135">730 dias é o máximo permitido para todas as outras SKUs</span><span class="sxs-lookup"><span data-stu-id="22bb0-135">730 days is the maximum allowed for all other Skus</span></span>

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

### <span data-ttu-id="22bb0-136">-SKU</span><span class="sxs-lookup"><span data-stu-id="22bb0-136">-Sku</span></span>
<span data-ttu-id="22bb0-137">Especifica o nível de serviço do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="22bb0-137">Specifies the service tier of the workspace.</span></span> <span data-ttu-id="22bb0-138">Para obter mais informações sobre qual valor usar, https://docs.microsoft.com/en-us/azure/azure-monitor/platform/manage-cost-storage#legacy-pricing-tiers verifique.</span><span class="sxs-lookup"><span data-stu-id="22bb0-138">For more information regarding which value to use please check https://docs.microsoft.com/en-us/azure/azure-monitor/platform/manage-cost-storage#legacy-pricing-tiers.</span></span>
<span data-ttu-id="22bb0-139">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="22bb0-139">Valid values are:</span></span>
- <span data-ttu-id="22bb0-140">Livre</span><span class="sxs-lookup"><span data-stu-id="22bb0-140">free</span></span>
- <span data-ttu-id="22bb0-141">pergb2018</span><span class="sxs-lookup"><span data-stu-id="22bb0-141">pergb2018</span></span>
- <span data-ttu-id="22bb0-142">pernode</span><span class="sxs-lookup"><span data-stu-id="22bb0-142">pernode</span></span>
- <span data-ttu-id="22bb0-143">Premium</span><span class="sxs-lookup"><span data-stu-id="22bb0-143">premium</span></span>
- <span data-ttu-id="22bb0-144">Autônomo</span><span class="sxs-lookup"><span data-stu-id="22bb0-144">standalone</span></span>
- <span data-ttu-id="22bb0-145">Padrão</span><span class="sxs-lookup"><span data-stu-id="22bb0-145">standard</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22bb0-146">-Tag</span><span class="sxs-lookup"><span data-stu-id="22bb0-146">-Tag</span></span>
<span data-ttu-id="22bb0-147">As marcas de recurso do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="22bb0-147">The resource tags for the workspace.</span></span>

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

### <span data-ttu-id="22bb0-148">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="22bb0-148">-Confirm</span></span>
<span data-ttu-id="22bb0-149">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="22bb0-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22bb0-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22bb0-150">-WhatIf</span></span>
<span data-ttu-id="22bb0-151">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="22bb0-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22bb0-152">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="22bb0-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22bb0-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22bb0-153">CommonParameters</span></span>
<span data-ttu-id="22bb0-154">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22bb0-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22bb0-155">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="22bb0-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22bb0-156">Entradas</span><span class="sxs-lookup"><span data-stu-id="22bb0-156">INPUTS</span></span>

### <span data-ttu-id="22bb0-157">System.String</span><span class="sxs-lookup"><span data-stu-id="22bb0-157">System.String</span></span>

### <span data-ttu-id="22bb0-158">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="22bb0-158">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="22bb0-159">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="22bb0-159">System.Collections.Hashtable</span></span>

### <span data-ttu-id="22bb0-160">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="22bb0-160">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="22bb0-161">Saídas</span><span class="sxs-lookup"><span data-stu-id="22bb0-161">OUTPUTS</span></span>

### <span data-ttu-id="22bb0-162">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="22bb0-162">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="22bb0-163">Notas</span><span class="sxs-lookup"><span data-stu-id="22bb0-163">NOTES</span></span>

<span data-ttu-id="22bb0-164">Um novo modelo de preços foi lançado.</span><span class="sxs-lookup"><span data-stu-id="22bb0-164">A new pricing model has been released.</span></span> <span data-ttu-id="22bb0-165">Se você for um CSP que significa que você precisa usar "autônomo" para a sKU.</span><span class="sxs-lookup"><span data-stu-id="22bb0-165">If you are a CSP that means that you have to use "standalone" for the sku.</span></span> <span data-ttu-id="22bb0-166">Nos bastidores, a SKU será alterada para pergb2018.</span><span class="sxs-lookup"><span data-stu-id="22bb0-166">Behind the scenes, the sku will be changed to pergb2018.</span></span> <span data-ttu-id="22bb0-167">Para obter mais informações, consulte o seguinte: https://docs.microsoft.com/en-us/azure/monitoring-and-diagnostics/monitoring-usage-and-estimated-costs#new-pricing-model</span><span class="sxs-lookup"><span data-stu-id="22bb0-167">For more information, please see the following: https://docs.microsoft.com/en-us/azure/monitoring-and-diagnostics/monitoring-usage-and-estimated-costs#new-pricing-model</span></span>

## <span data-ttu-id="22bb0-168">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="22bb0-168">RELATED LINKS</span></span>

[<span data-ttu-id="22bb0-169">Cmdlets de Insights Operacionais do Azure</span><span class="sxs-lookup"><span data-stu-id="22bb0-169">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)



