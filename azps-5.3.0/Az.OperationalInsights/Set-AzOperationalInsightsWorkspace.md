---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 54DFBB63-AE8C-4918-870F-19FAD6CC5E4A
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 5abfd1a02687eb2715ad924510176748e04e56cd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427498"
---
# <span data-ttu-id="b11a4-101">Set-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="b11a4-101">Set-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="b11a4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b11a4-102">SYNOPSIS</span></span>
<span data-ttu-id="b11a4-103">Atualiza um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="b11a4-103">Updates a workspace.</span></span>

## <span data-ttu-id="b11a4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b11a4-104">SYNTAX</span></span>

### <span data-ttu-id="b11a4-105">ByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="b11a4-105">ByName (Default)</span></span>
```
Set-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [[-Sku] <String>]
 [[-Tag] <Hashtable>] [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-PublicNetworkAccessForIngestion <String>] [-PublicNetworkAccessForQuery <String>] [<CommonParameters>]
```

### <span data-ttu-id="b11a4-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="b11a4-106">ByObject</span></span>
```
Set-AzOperationalInsightsWorkspace [-Workspace] <PSWorkspace> [[-Sku] <String>] [[-Tag] <Hashtable>]
 [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-PublicNetworkAccessForIngestion <String>] [-PublicNetworkAccessForQuery <String>] [<CommonParameters>]
```

## <span data-ttu-id="b11a4-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b11a4-107">DESCRIPTION</span></span>
<span data-ttu-id="b11a4-108">O cmdlet **set-AzOperationalInsightsWorkspace** altera a configuração de um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="b11a4-108">The **Set-AzOperationalInsightsWorkspace** cmdlet changes the configuration of a workspace.</span></span>

## <span data-ttu-id="b11a4-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b11a4-109">EXAMPLES</span></span>

### <span data-ttu-id="b11a4-110">Exemplo 1: modificar um espaço de trabalho por nome</span><span class="sxs-lookup"><span data-stu-id="b11a4-110">Example 1: Modify a workspace by name</span></span>
```
PS C:\>Set-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku Standard -Tags @{ "Department" = "IT" }
```

<span data-ttu-id="b11a4-111">Esse comando modifica a SKU e as marcas do espaço de trabalho chamado MyWorkspace no grupo de recursos chamado ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="b11a4-111">This command modifies the SKU and tags of the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="b11a4-112">Exemplo 2: atualizar um espaço de trabalho usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="b11a4-112">Example 2: Update a workspace by using the pipeline</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Set-AzOperationalInsightsWorkspace -Sku "Premium"
```

<span data-ttu-id="b11a4-113">Esse comando usa o cmdlet Get-AzOperationalInsightsWorkspace para obter o espaço de trabalho chamado MyWorkspace e, em seguida, passa-o para o cmdlet **set-AzOperationalInsightsWorkspace** usando o operador pipeline para definir a SKU como Premium.</span><span class="sxs-lookup"><span data-stu-id="b11a4-113">This command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkSpace, and then passes it to the **Set-AzOperationalInsightsWorkspace** cmdlet by using the pipeline operator to set the SKU to Premium.</span></span>

## <span data-ttu-id="b11a4-114">OS</span><span class="sxs-lookup"><span data-stu-id="b11a4-114">PARAMETERS</span></span>

### <span data-ttu-id="b11a4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b11a4-115">-DefaultProfile</span></span>
<span data-ttu-id="b11a4-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="b11a4-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b11a4-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="b11a4-117">-Name</span></span>
<span data-ttu-id="b11a4-118">Especifica o nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="b11a4-118">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="b11a4-119">-PublicNetworkAccessForIngestion</span><span class="sxs-lookup"><span data-stu-id="b11a4-119">-PublicNetworkAccessForIngestion</span></span>
<span data-ttu-id="b11a4-120">O tipo de acesso à rede para acessar a inclusão de espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="b11a4-120">The network access type for accessing workspace ingestion.</span></span> <span data-ttu-id="b11a4-121">O valor deve ser ' Enabled ' ou ' disabled '</span><span class="sxs-lookup"><span data-stu-id="b11a4-121">Value should be 'Enabled' or 'Disabled'</span></span>

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

### <span data-ttu-id="b11a4-122">-PublicNetworkAccessForQuery</span><span class="sxs-lookup"><span data-stu-id="b11a4-122">-PublicNetworkAccessForQuery</span></span>
<span data-ttu-id="b11a4-123">O tipo de acesso à rede para acessar a consulta do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="b11a4-123">The network access type for accessing workspace query.</span></span> <span data-ttu-id="b11a4-124">O valor deve ser ' Enabled ' ou ' disabled '</span><span class="sxs-lookup"><span data-stu-id="b11a4-124">Value should be 'Enabled' or 'Disabled'</span></span>

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

### <span data-ttu-id="b11a4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b11a4-125">-ResourceGroupName</span></span>
<span data-ttu-id="b11a4-126">Especifica o nome do grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="b11a4-126">Specifies the Azure resource group name.</span></span>

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

### <span data-ttu-id="b11a4-127">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="b11a4-127">-RetentionInDays</span></span>
<span data-ttu-id="b11a4-128">A retenção de dados do espaço de trabalho em dias.</span><span class="sxs-lookup"><span data-stu-id="b11a4-128">The workspace data retention in days.</span></span> <span data-ttu-id="b11a4-129">730 dias é o máximo permitido para todas as outras SKUs</span><span class="sxs-lookup"><span data-stu-id="b11a4-129">730 days is the maximum allowed for all other Skus</span></span>

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

### <span data-ttu-id="b11a4-130">-SKU</span><span class="sxs-lookup"><span data-stu-id="b11a4-130">-Sku</span></span>
<span data-ttu-id="b11a4-131">Especifica a camada de serviço do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="b11a4-131">Specifies the service tier of the workspace.</span></span>
<span data-ttu-id="b11a4-132">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="b11a4-132">Valid values are:</span></span> 
- <span data-ttu-id="b11a4-133">gratuito</span><span class="sxs-lookup"><span data-stu-id="b11a4-133">free</span></span>
- <span data-ttu-id="b11a4-134">oficial</span><span class="sxs-lookup"><span data-stu-id="b11a4-134">standard</span></span>
- <span data-ttu-id="b11a4-135">gratifica</span><span class="sxs-lookup"><span data-stu-id="b11a4-135">premium</span></span>
- <span data-ttu-id="b11a4-136">PerNode</span><span class="sxs-lookup"><span data-stu-id="b11a4-136">pernode</span></span>
- <span data-ttu-id="b11a4-137">autônoma</span><span class="sxs-lookup"><span data-stu-id="b11a4-137">standalone</span></span>
- <span data-ttu-id="b11a4-138">pergb2018</span><span class="sxs-lookup"><span data-stu-id="b11a4-138">pergb2018</span></span>

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

### <span data-ttu-id="b11a4-139">-Marca</span><span class="sxs-lookup"><span data-stu-id="b11a4-139">-Tag</span></span>
<span data-ttu-id="b11a4-140">As marcas de recurso do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="b11a4-140">The resource tags for the workspace.</span></span>

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

### <span data-ttu-id="b11a4-141">-Espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="b11a4-141">-Workspace</span></span>
<span data-ttu-id="b11a4-142">Especifica o espaço de trabalho a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="b11a4-142">Specifies the workspace to be updated.</span></span>

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

### <span data-ttu-id="b11a4-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b11a4-143">CommonParameters</span></span>
<span data-ttu-id="b11a4-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b11a4-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b11a4-145">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b11a4-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b11a4-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b11a4-146">INPUTS</span></span>

### <span data-ttu-id="b11a4-147">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="b11a4-147">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="b11a4-148">System. String</span><span class="sxs-lookup"><span data-stu-id="b11a4-148">System.String</span></span>

### <span data-ttu-id="b11a4-149">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="b11a4-149">System.Collections.Hashtable</span></span>

### <span data-ttu-id="b11a4-150">System. Nullable ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="b11a4-150">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="b11a4-151">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b11a4-151">OUTPUTS</span></span>

### <span data-ttu-id="b11a4-152">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="b11a4-152">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="b11a4-153">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b11a4-153">NOTES</span></span>

## <span data-ttu-id="b11a4-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b11a4-154">RELATED LINKS</span></span>

[<span data-ttu-id="b11a4-155">Cmdlets do Azure Operational insights</span><span class="sxs-lookup"><span data-stu-id="b11a4-155">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="b11a4-156">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="b11a4-156">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


