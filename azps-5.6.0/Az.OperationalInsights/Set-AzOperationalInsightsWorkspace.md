---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 54DFBB63-AE8C-4918-870F-19FAD6CC5E4A
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/set-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: ecc68d6f87728f3bccb2d7fe1947c293e6b670d3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890184"
---
# <span data-ttu-id="be43a-101">Set-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="be43a-101">Set-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="be43a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be43a-102">SYNOPSIS</span></span>
<span data-ttu-id="be43a-103">Atualiza um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="be43a-103">Updates a workspace.</span></span>

## <span data-ttu-id="be43a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="be43a-104">SYNTAX</span></span>

### <span data-ttu-id="be43a-105">ByName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="be43a-105">ByName (Default)</span></span>
```
Set-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [[-Sku] <String>]
 [[-Tag] <Hashtable>] [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-PublicNetworkAccessForIngestion <String>] [-PublicNetworkAccessForQuery <String>] [<CommonParameters>]
```

### <span data-ttu-id="be43a-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="be43a-106">ByObject</span></span>
```
Set-AzOperationalInsightsWorkspace [-Workspace] <PSWorkspace> [[-Sku] <String>] [[-Tag] <Hashtable>]
 [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-PublicNetworkAccessForIngestion <String>] [-PublicNetworkAccessForQuery <String>] [<CommonParameters>]
```

## <span data-ttu-id="be43a-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="be43a-107">DESCRIPTION</span></span>
<span data-ttu-id="be43a-108">O cmdlet **Set-AzOperationalInsightsWorkspace** altera a configuração de um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="be43a-108">The **Set-AzOperationalInsightsWorkspace** cmdlet changes the configuration of a workspace.</span></span>

## <span data-ttu-id="be43a-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="be43a-109">EXAMPLES</span></span>

### <span data-ttu-id="be43a-110">Exemplo 1: Modificar um espaço de trabalho pelo nome</span><span class="sxs-lookup"><span data-stu-id="be43a-110">Example 1: Modify a workspace by name</span></span>
```
PS C:\>Set-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku Standard -Tags @{ "Department" = "IT" }
```

<span data-ttu-id="be43a-111">Este comando modifica a SKU e as marcas do espaço de trabalho chamado MyWorkspace no grupo de recursos chamado ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="be43a-111">This command modifies the SKU and tags of the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="be43a-112">Exemplo 2: atualizar um espaço de trabalho usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="be43a-112">Example 2: Update a workspace by using the pipeline</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Set-AzOperationalInsightsWorkspace -Sku "Premium"
```

<span data-ttu-id="be43a-113">Este comando usa o cmdlet Get-AzOperationalInsightsWorkspace para obter o espaço de trabalho chamado MyWorkSpace e, em seguida, passa-o para o cmdlet **Set-AzOperationalInsightsWorkspace** usando o operador de pipeline para definir o SKU como Premium.</span><span class="sxs-lookup"><span data-stu-id="be43a-113">This command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkSpace, and then passes it to the **Set-AzOperationalInsightsWorkspace** cmdlet by using the pipeline operator to set the SKU to Premium.</span></span>

## <span data-ttu-id="be43a-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="be43a-114">PARAMETERS</span></span>

### <span data-ttu-id="be43a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be43a-115">-DefaultProfile</span></span>
<span data-ttu-id="be43a-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="be43a-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="be43a-117">-Name</span><span class="sxs-lookup"><span data-stu-id="be43a-117">-Name</span></span>
<span data-ttu-id="be43a-118">Especifica o nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="be43a-118">Specifies the workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be43a-119">-PublicNetworkAccessForIngestion</span><span class="sxs-lookup"><span data-stu-id="be43a-119">-PublicNetworkAccessForIngestion</span></span>
<span data-ttu-id="be43a-120">O tipo de acesso à rede para acessar a ingestão de espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="be43a-120">The network access type for accessing workspace ingestion.</span></span> <span data-ttu-id="be43a-121">O valor deve ser 'Habilitado' ou 'Desabilitado'</span><span class="sxs-lookup"><span data-stu-id="be43a-121">Value should be 'Enabled' or 'Disabled'</span></span>

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

### <span data-ttu-id="be43a-122">-PublicNetworkAccessForQuery</span><span class="sxs-lookup"><span data-stu-id="be43a-122">-PublicNetworkAccessForQuery</span></span>
<span data-ttu-id="be43a-123">O tipo de acesso à rede para acessar a consulta de espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="be43a-123">The network access type for accessing workspace query.</span></span> <span data-ttu-id="be43a-124">O valor deve ser 'Habilitado' ou 'Desabilitado'</span><span class="sxs-lookup"><span data-stu-id="be43a-124">Value should be 'Enabled' or 'Disabled'</span></span>

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

### <span data-ttu-id="be43a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be43a-125">-ResourceGroupName</span></span>
<span data-ttu-id="be43a-126">Especifica o nome do grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="be43a-126">Specifies the Azure resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be43a-127">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="be43a-127">-RetentionInDays</span></span>
<span data-ttu-id="be43a-128">A retenção de dados do espaço de trabalho em dias.</span><span class="sxs-lookup"><span data-stu-id="be43a-128">The workspace data retention in days.</span></span> <span data-ttu-id="be43a-129">730 dias é o máximo permitido para todos os outros Skus</span><span class="sxs-lookup"><span data-stu-id="be43a-129">730 days is the maximum allowed for all other Skus</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be43a-130">-Sku</span><span class="sxs-lookup"><span data-stu-id="be43a-130">-Sku</span></span>
<span data-ttu-id="be43a-131">Especifica a camada de serviço do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="be43a-131">Specifies the service tier of the workspace.</span></span>
<span data-ttu-id="be43a-132">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="be43a-132">Valid values are:</span></span> 
- <span data-ttu-id="be43a-133">gratuito</span><span class="sxs-lookup"><span data-stu-id="be43a-133">free</span></span>
- <span data-ttu-id="be43a-134">standard</span><span class="sxs-lookup"><span data-stu-id="be43a-134">standard</span></span>
- <span data-ttu-id="be43a-135">premium</span><span class="sxs-lookup"><span data-stu-id="be43a-135">premium</span></span>
- <span data-ttu-id="be43a-136">pernode</span><span class="sxs-lookup"><span data-stu-id="be43a-136">pernode</span></span>
- <span data-ttu-id="be43a-137">autônomo</span><span class="sxs-lookup"><span data-stu-id="be43a-137">standalone</span></span>
- <span data-ttu-id="be43a-138">pergb2018</span><span class="sxs-lookup"><span data-stu-id="be43a-138">pergb2018</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: free, standard, premium, pernode, standalone, pergb2018

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be43a-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="be43a-139">-Tag</span></span>
<span data-ttu-id="be43a-140">As marcas de recurso do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="be43a-140">The resource tags for the workspace.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be43a-141">-Workspace</span><span class="sxs-lookup"><span data-stu-id="be43a-141">-Workspace</span></span>
<span data-ttu-id="be43a-142">Especifica o espaço de trabalho a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="be43a-142">Specifies the workspace to be updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="be43a-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be43a-143">CommonParameters</span></span>
<span data-ttu-id="be43a-144">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be43a-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be43a-145">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="be43a-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be43a-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="be43a-146">INPUTS</span></span>

### <span data-ttu-id="be43a-147">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="be43a-147">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="be43a-148">System.String</span><span class="sxs-lookup"><span data-stu-id="be43a-148">System.String</span></span>

### <span data-ttu-id="be43a-149">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="be43a-149">System.Collections.Hashtable</span></span>

### <span data-ttu-id="be43a-150">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="be43a-150">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="be43a-151">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="be43a-151">OUTPUTS</span></span>

### <span data-ttu-id="be43a-152">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="be43a-152">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="be43a-153">NOTES</span><span class="sxs-lookup"><span data-stu-id="be43a-153">NOTES</span></span>

## <span data-ttu-id="be43a-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="be43a-154">RELATED LINKS</span></span>

[<span data-ttu-id="be43a-155">Cmdlets do Insights Operacionais do Azure</span><span class="sxs-lookup"><span data-stu-id="be43a-155">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="be43a-156">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="be43a-156">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


