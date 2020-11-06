---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 54DFBB63-AE8C-4918-870F-19FAD6CC5E4A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/set-azurermoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsWorkspace.md
ms.openlocfilehash: a4584e4c0fc64920fbffb7e3d685a9be3ac04ad1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429743"
---
# <span data-ttu-id="0d8a9-101">Set-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="0d8a9-101">Set-AzureRmOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="0d8a9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0d8a9-102">SYNOPSIS</span></span>
<span data-ttu-id="0d8a9-103">Atualiza um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="0d8a9-103">Updates a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d8a9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0d8a9-104">SYNTAX</span></span>

### <span data-ttu-id="0d8a9-105">ByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="0d8a9-105">ByName (Default)</span></span>
```
Set-AzureRmOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [[-Sku] <String>]
 [[-Tag] <Hashtable>] [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0d8a9-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="0d8a9-106">ByObject</span></span>
```
Set-AzureRmOperationalInsightsWorkspace [-Workspace] <PSWorkspace> [[-Sku] <String>] [[-Tag] <Hashtable>]
 [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d8a9-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0d8a9-107">DESCRIPTION</span></span>
<span data-ttu-id="0d8a9-108">O cmdlet **set-AzureRmOperationalInsightsWorkspace** altera a configuração de um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="0d8a9-108">The **Set-AzureRmOperationalInsightsWorkspace** cmdlet changes the configuration of a workspace.</span></span>

## <span data-ttu-id="0d8a9-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0d8a9-109">EXAMPLES</span></span>

### <span data-ttu-id="0d8a9-110">Exemplo 1: modificar um espaço de trabalho por nome</span><span class="sxs-lookup"><span data-stu-id="0d8a9-110">Example 1: Modify a workspace by name</span></span>
```
PS C:\>Set-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku Standard -Tags @{ "Department" = "IT" }
```

<span data-ttu-id="0d8a9-111">Esse comando modifica a SKU e as marcas do espaço de trabalho chamado MyWorkspace no grupo de recursos chamado ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="0d8a9-111">This command modifies the SKU and tags of the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="0d8a9-112">Exemplo 2: atualizar um espaço de trabalho usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="0d8a9-112">Example 2: Update a workspace by using the pipeline</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Set-AzureRmOperationalInsightsWorkspace -Sku "Premium"
```

<span data-ttu-id="0d8a9-113">Esse comando usa o cmdlet Get-AzureRmOperationalInsightsWorkspace para obter o espaço de trabalho chamado MyWorkspace e, em seguida, passa-o para o cmdlet **set-AzureRmOperationalInsightsWorkspace** usando o operador pipeline para definir a SKU como Premium.</span><span class="sxs-lookup"><span data-stu-id="0d8a9-113">This command uses the Get-AzureRmOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkSpace, and then passes it to the **Set-AzureRmOperationalInsightsWorkspace** cmdlet by using the pipeline operator to set the SKU to Premium.</span></span>

## <span data-ttu-id="0d8a9-114">OS</span><span class="sxs-lookup"><span data-stu-id="0d8a9-114">PARAMETERS</span></span>

### <span data-ttu-id="0d8a9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d8a9-115">-DefaultProfile</span></span>
<span data-ttu-id="0d8a9-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="0d8a9-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d8a9-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="0d8a9-117">-Name</span></span>
<span data-ttu-id="0d8a9-118">Especifica o nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="0d8a9-118">Specifies the workspace name.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d8a9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d8a9-119">-ResourceGroupName</span></span>
<span data-ttu-id="0d8a9-120">Especifica o nome do grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="0d8a9-120">Specifies the Azure resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d8a9-121">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="0d8a9-121">-RetentionInDays</span></span>
<span data-ttu-id="0d8a9-122">A retenção de dados do espaço de trabalho em dias.</span><span class="sxs-lookup"><span data-stu-id="0d8a9-122">The workspace data retention in days.</span></span> <span data-ttu-id="0d8a9-123">730 dias é o máximo permitido para todas as outras SKUs</span><span class="sxs-lookup"><span data-stu-id="0d8a9-123">730 days is the maximum allowed for all other Skus</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d8a9-124">-SKU</span><span class="sxs-lookup"><span data-stu-id="0d8a9-124">-Sku</span></span>
<span data-ttu-id="0d8a9-125">Especifica a camada de serviço do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="0d8a9-125">Specifies the service tier of the workspace.</span></span>
<span data-ttu-id="0d8a9-126">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="0d8a9-126">Valid values are:</span></span> 

- <span data-ttu-id="0d8a9-127">gratuito</span><span class="sxs-lookup"><span data-stu-id="0d8a9-127">free</span></span>
- <span data-ttu-id="0d8a9-128">oficial</span><span class="sxs-lookup"><span data-stu-id="0d8a9-128">standard</span></span>
- <span data-ttu-id="0d8a9-129">gratifica</span><span class="sxs-lookup"><span data-stu-id="0d8a9-129">premium</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: free, standard, premium, pernode, standalone

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d8a9-130">-Marca</span><span class="sxs-lookup"><span data-stu-id="0d8a9-130">-Tag</span></span>
<span data-ttu-id="0d8a9-131">As marcas de recurso do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="0d8a9-131">The resource tags for the workspace.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d8a9-132">-Espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="0d8a9-132">-Workspace</span></span>
<span data-ttu-id="0d8a9-133">Especifica o espaço de trabalho a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="0d8a9-133">Specifies the workspace to be updated.</span></span>

```yaml
Type: PSWorkspace
Parameter Sets: ByObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0d8a9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d8a9-134">CommonParameters</span></span>
<span data-ttu-id="0d8a9-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d8a9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d8a9-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d8a9-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d8a9-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0d8a9-137">INPUTS</span></span>

### <span data-ttu-id="0d8a9-138">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="0d8a9-138">PSWorkspace</span></span>
<span data-ttu-id="0d8a9-139">O parâmetro ' Workspace ' aceita o valor do tipo ' PSWorkspace ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="0d8a9-139">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="0d8a9-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0d8a9-140">OUTPUTS</span></span>

### <span data-ttu-id="0d8a9-141">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="0d8a9-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="0d8a9-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0d8a9-142">NOTES</span></span>

## <span data-ttu-id="0d8a9-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0d8a9-143">RELATED LINKS</span></span>

[<span data-ttu-id="0d8a9-144">Cmdlets do Azure Operational insights</span><span class="sxs-lookup"><span data-stu-id="0d8a9-144">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="0d8a9-145">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="0d8a9-145">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)

