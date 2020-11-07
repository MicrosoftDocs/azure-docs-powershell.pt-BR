---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 54DFBB63-AE8C-4918-870F-19FAD6CC5E4A
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: e339becd21be14d3587252b88dd8069b266b2408
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93784971"
---
# <span data-ttu-id="62c19-101">Set-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="62c19-101">Set-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="62c19-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="62c19-102">SYNOPSIS</span></span>
<span data-ttu-id="62c19-103">Atualiza um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="62c19-103">Updates a workspace.</span></span>

## <span data-ttu-id="62c19-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="62c19-104">SYNTAX</span></span>

### <span data-ttu-id="62c19-105">ByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="62c19-105">ByName (Default)</span></span>
```
Set-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [[-Sku] <String>]
 [[-Tag] <Hashtable>] [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="62c19-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="62c19-106">ByObject</span></span>
```
Set-AzOperationalInsightsWorkspace [-Workspace] <PSWorkspace> [[-Sku] <String>] [[-Tag] <Hashtable>]
 [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62c19-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="62c19-107">DESCRIPTION</span></span>
<span data-ttu-id="62c19-108">O cmdlet **set-AzOperationalInsightsWorkspace** altera a configuração de um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="62c19-108">The **Set-AzOperationalInsightsWorkspace** cmdlet changes the configuration of a workspace.</span></span>

## <span data-ttu-id="62c19-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="62c19-109">EXAMPLES</span></span>

### <span data-ttu-id="62c19-110">Exemplo 1: modificar um espaço de trabalho por nome</span><span class="sxs-lookup"><span data-stu-id="62c19-110">Example 1: Modify a workspace by name</span></span>
```
PS C:\>Set-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku Standard -Tags @{ "Department" = "IT" }
```

<span data-ttu-id="62c19-111">Esse comando modifica a SKU e as marcas do espaço de trabalho chamado MyWorkspace no grupo de recursos chamado ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="62c19-111">This command modifies the SKU and tags of the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="62c19-112">Exemplo 2: atualizar um espaço de trabalho usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="62c19-112">Example 2: Update a workspace by using the pipeline</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Set-AzOperationalInsightsWorkspace -Sku "Premium"
```

<span data-ttu-id="62c19-113">Esse comando usa o cmdlet Get-AzOperationalInsightsWorkspace para obter o espaço de trabalho chamado MyWorkspace e, em seguida, passa-o para o cmdlet **set-AzOperationalInsightsWorkspace** usando o operador pipeline para definir a SKU como Premium.</span><span class="sxs-lookup"><span data-stu-id="62c19-113">This command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkSpace, and then passes it to the **Set-AzOperationalInsightsWorkspace** cmdlet by using the pipeline operator to set the SKU to Premium.</span></span>

## <span data-ttu-id="62c19-114">OS</span><span class="sxs-lookup"><span data-stu-id="62c19-114">PARAMETERS</span></span>

### <span data-ttu-id="62c19-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62c19-115">-DefaultProfile</span></span>
<span data-ttu-id="62c19-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="62c19-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="62c19-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="62c19-117">-Name</span></span>
<span data-ttu-id="62c19-118">Especifica o nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="62c19-118">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="62c19-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62c19-119">-ResourceGroupName</span></span>
<span data-ttu-id="62c19-120">Especifica o nome do grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="62c19-120">Specifies the Azure resource group name.</span></span>

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

### <span data-ttu-id="62c19-121">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="62c19-121">-RetentionInDays</span></span>
<span data-ttu-id="62c19-122">A retenção de dados do espaço de trabalho em dias.</span><span class="sxs-lookup"><span data-stu-id="62c19-122">The workspace data retention in days.</span></span> <span data-ttu-id="62c19-123">730 dias é o máximo permitido para todas as outras SKUs</span><span class="sxs-lookup"><span data-stu-id="62c19-123">730 days is the maximum allowed for all other Skus</span></span>

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

### <span data-ttu-id="62c19-124">-SKU</span><span class="sxs-lookup"><span data-stu-id="62c19-124">-Sku</span></span>
<span data-ttu-id="62c19-125">Especifica a camada de serviço do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="62c19-125">Specifies the service tier of the workspace.</span></span>
<span data-ttu-id="62c19-126">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="62c19-126">Valid values are:</span></span> 
- <span data-ttu-id="62c19-127">gratuito</span><span class="sxs-lookup"><span data-stu-id="62c19-127">free</span></span>
- <span data-ttu-id="62c19-128">oficial</span><span class="sxs-lookup"><span data-stu-id="62c19-128">standard</span></span>
- <span data-ttu-id="62c19-129">gratifica</span><span class="sxs-lookup"><span data-stu-id="62c19-129">premium</span></span>

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

### <span data-ttu-id="62c19-130">-Marca</span><span class="sxs-lookup"><span data-stu-id="62c19-130">-Tag</span></span>
<span data-ttu-id="62c19-131">As marcas de recurso do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="62c19-131">The resource tags for the workspace.</span></span>

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

### <span data-ttu-id="62c19-132">-Espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="62c19-132">-Workspace</span></span>
<span data-ttu-id="62c19-133">Especifica o espaço de trabalho a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="62c19-133">Specifies the workspace to be updated.</span></span>

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

### <span data-ttu-id="62c19-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62c19-134">CommonParameters</span></span>
<span data-ttu-id="62c19-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62c19-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62c19-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62c19-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62c19-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="62c19-137">INPUTS</span></span>

### <span data-ttu-id="62c19-138">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="62c19-138">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="62c19-139">System. String</span><span class="sxs-lookup"><span data-stu-id="62c19-139">System.String</span></span>

### <span data-ttu-id="62c19-140">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="62c19-140">System.Collections.Hashtable</span></span>

### <span data-ttu-id="62c19-141">System. Nullable ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="62c19-141">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="62c19-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="62c19-142">OUTPUTS</span></span>

### <span data-ttu-id="62c19-143">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="62c19-143">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="62c19-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="62c19-144">NOTES</span></span>

## <span data-ttu-id="62c19-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="62c19-145">RELATED LINKS</span></span>

[<span data-ttu-id="62c19-146">Cmdlets do Azure Operational insights</span><span class="sxs-lookup"><span data-stu-id="62c19-146">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)

[<span data-ttu-id="62c19-147">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="62c19-147">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


