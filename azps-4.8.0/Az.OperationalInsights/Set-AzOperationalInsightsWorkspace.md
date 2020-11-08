---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 54DFBB63-AE8C-4918-870F-19FAD6CC5E4A
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 5abfd1a02687eb2715ad924510176748e04e56cd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94112942"
---
# <span data-ttu-id="c8365-101">Set-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="c8365-101">Set-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="c8365-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c8365-102">SYNOPSIS</span></span>
<span data-ttu-id="c8365-103">Atualiza um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="c8365-103">Updates a workspace.</span></span>

## <span data-ttu-id="c8365-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c8365-104">SYNTAX</span></span>

### <span data-ttu-id="c8365-105">ByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="c8365-105">ByName (Default)</span></span>
```
Set-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [[-Sku] <String>]
 [[-Tag] <Hashtable>] [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-PublicNetworkAccessForIngestion <String>] [-PublicNetworkAccessForQuery <String>] [<CommonParameters>]
```

### <span data-ttu-id="c8365-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="c8365-106">ByObject</span></span>
```
Set-AzOperationalInsightsWorkspace [-Workspace] <PSWorkspace> [[-Sku] <String>] [[-Tag] <Hashtable>]
 [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-PublicNetworkAccessForIngestion <String>] [-PublicNetworkAccessForQuery <String>] [<CommonParameters>]
```

## <span data-ttu-id="c8365-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c8365-107">DESCRIPTION</span></span>
<span data-ttu-id="c8365-108">O cmdlet **set-AzOperationalInsightsWorkspace** altera a configuração de um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="c8365-108">The **Set-AzOperationalInsightsWorkspace** cmdlet changes the configuration of a workspace.</span></span>

## <span data-ttu-id="c8365-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c8365-109">EXAMPLES</span></span>

### <span data-ttu-id="c8365-110">Exemplo 1: modificar um espaço de trabalho por nome</span><span class="sxs-lookup"><span data-stu-id="c8365-110">Example 1: Modify a workspace by name</span></span>
```
PS C:\>Set-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku Standard -Tags @{ "Department" = "IT" }
```

<span data-ttu-id="c8365-111">Esse comando modifica a SKU e as marcas do espaço de trabalho chamado MyWorkspace no grupo de recursos chamado ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="c8365-111">This command modifies the SKU and tags of the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="c8365-112">Exemplo 2: atualizar um espaço de trabalho usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="c8365-112">Example 2: Update a workspace by using the pipeline</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Set-AzOperationalInsightsWorkspace -Sku "Premium"
```

<span data-ttu-id="c8365-113">Esse comando usa o cmdlet Get-AzOperationalInsightsWorkspace para obter o espaço de trabalho chamado MyWorkspace e, em seguida, passa-o para o cmdlet **set-AzOperationalInsightsWorkspace** usando o operador pipeline para definir a SKU como Premium.</span><span class="sxs-lookup"><span data-stu-id="c8365-113">This command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkSpace, and then passes it to the **Set-AzOperationalInsightsWorkspace** cmdlet by using the pipeline operator to set the SKU to Premium.</span></span>

## <span data-ttu-id="c8365-114">OS</span><span class="sxs-lookup"><span data-stu-id="c8365-114">PARAMETERS</span></span>

### <span data-ttu-id="c8365-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8365-115">-DefaultProfile</span></span>
<span data-ttu-id="c8365-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="c8365-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c8365-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="c8365-117">-Name</span></span>
<span data-ttu-id="c8365-118">Especifica o nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="c8365-118">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="c8365-119">-PublicNetworkAccessForIngestion</span><span class="sxs-lookup"><span data-stu-id="c8365-119">-PublicNetworkAccessForIngestion</span></span>
<span data-ttu-id="c8365-120">O tipo de acesso à rede para acessar a inclusão de espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="c8365-120">The network access type for accessing workspace ingestion.</span></span> <span data-ttu-id="c8365-121">O valor deve ser ' Enabled ' ou ' disabled '</span><span class="sxs-lookup"><span data-stu-id="c8365-121">Value should be 'Enabled' or 'Disabled'</span></span>

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

### <span data-ttu-id="c8365-122">-PublicNetworkAccessForQuery</span><span class="sxs-lookup"><span data-stu-id="c8365-122">-PublicNetworkAccessForQuery</span></span>
<span data-ttu-id="c8365-123">O tipo de acesso à rede para acessar a consulta do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="c8365-123">The network access type for accessing workspace query.</span></span> <span data-ttu-id="c8365-124">O valor deve ser ' Enabled ' ou ' disabled '</span><span class="sxs-lookup"><span data-stu-id="c8365-124">Value should be 'Enabled' or 'Disabled'</span></span>

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

### <span data-ttu-id="c8365-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8365-125">-ResourceGroupName</span></span>
<span data-ttu-id="c8365-126">Especifica o nome do grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="c8365-126">Specifies the Azure resource group name.</span></span>

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

### <span data-ttu-id="c8365-127">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="c8365-127">-RetentionInDays</span></span>
<span data-ttu-id="c8365-128">A retenção de dados do espaço de trabalho em dias.</span><span class="sxs-lookup"><span data-stu-id="c8365-128">The workspace data retention in days.</span></span> <span data-ttu-id="c8365-129">730 dias é o máximo permitido para todas as outras SKUs</span><span class="sxs-lookup"><span data-stu-id="c8365-129">730 days is the maximum allowed for all other Skus</span></span>

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

### <span data-ttu-id="c8365-130">-SKU</span><span class="sxs-lookup"><span data-stu-id="c8365-130">-Sku</span></span>
<span data-ttu-id="c8365-131">Especifica a camada de serviço do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="c8365-131">Specifies the service tier of the workspace.</span></span>
<span data-ttu-id="c8365-132">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="c8365-132">Valid values are:</span></span> 
- <span data-ttu-id="c8365-133">gratuito</span><span class="sxs-lookup"><span data-stu-id="c8365-133">free</span></span>
- <span data-ttu-id="c8365-134">oficial</span><span class="sxs-lookup"><span data-stu-id="c8365-134">standard</span></span>
- <span data-ttu-id="c8365-135">gratifica</span><span class="sxs-lookup"><span data-stu-id="c8365-135">premium</span></span>
- <span data-ttu-id="c8365-136">PerNode</span><span class="sxs-lookup"><span data-stu-id="c8365-136">pernode</span></span>
- <span data-ttu-id="c8365-137">autônoma</span><span class="sxs-lookup"><span data-stu-id="c8365-137">standalone</span></span>
- <span data-ttu-id="c8365-138">pergb2018</span><span class="sxs-lookup"><span data-stu-id="c8365-138">pergb2018</span></span>

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

### <span data-ttu-id="c8365-139">-Marca</span><span class="sxs-lookup"><span data-stu-id="c8365-139">-Tag</span></span>
<span data-ttu-id="c8365-140">As marcas de recurso do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="c8365-140">The resource tags for the workspace.</span></span>

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

### <span data-ttu-id="c8365-141">-Espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="c8365-141">-Workspace</span></span>
<span data-ttu-id="c8365-142">Especifica o espaço de trabalho a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="c8365-142">Specifies the workspace to be updated.</span></span>

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

### <span data-ttu-id="c8365-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8365-143">CommonParameters</span></span>
<span data-ttu-id="c8365-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8365-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8365-145">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c8365-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8365-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c8365-146">INPUTS</span></span>

### <span data-ttu-id="c8365-147">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="c8365-147">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="c8365-148">System. String</span><span class="sxs-lookup"><span data-stu-id="c8365-148">System.String</span></span>

### <span data-ttu-id="c8365-149">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="c8365-149">System.Collections.Hashtable</span></span>

### <span data-ttu-id="c8365-150">System. Nullable ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="c8365-150">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="c8365-151">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c8365-151">OUTPUTS</span></span>

### <span data-ttu-id="c8365-152">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="c8365-152">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="c8365-153">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c8365-153">NOTES</span></span>

## <span data-ttu-id="c8365-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c8365-154">RELATED LINKS</span></span>

[<span data-ttu-id="c8365-155">Cmdlets do Azure Operational insights</span><span class="sxs-lookup"><span data-stu-id="c8365-155">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="c8365-156">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="c8365-156">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


