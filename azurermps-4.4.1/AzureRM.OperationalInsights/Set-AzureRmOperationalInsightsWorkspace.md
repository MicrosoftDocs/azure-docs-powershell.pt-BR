---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 54DFBB63-AE8C-4918-870F-19FAD6CC5E4A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsWorkspace.md
ms.openlocfilehash: e24597d25fffdc1b516c5a18cf011f7222d288c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427817"
---
# <span data-ttu-id="e73bf-101">Set-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="e73bf-101">Set-AzureRmOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="e73bf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e73bf-102">SYNOPSIS</span></span>
<span data-ttu-id="e73bf-103">Atualiza um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="e73bf-103">Updates a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e73bf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e73bf-104">SYNTAX</span></span>

### <span data-ttu-id="e73bf-105">ByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="e73bf-105">ByName (Default)</span></span>
```
Set-AzureRmOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [[-Sku] <String>]
 [[-Tags] <Hashtable>] [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e73bf-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="e73bf-106">ByObject</span></span>
```
Set-AzureRmOperationalInsightsWorkspace [-Workspace] <PSWorkspace> [[-Sku] <String>] [[-Tags] <Hashtable>]
 [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e73bf-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e73bf-107">DESCRIPTION</span></span>
<span data-ttu-id="e73bf-108">O cmdlet **set-AzureRmOperationalInsightsWorkspace** altera a configuração de um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="e73bf-108">The **Set-AzureRmOperationalInsightsWorkspace** cmdlet changes the configuration of a workspace.</span></span>

## <span data-ttu-id="e73bf-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e73bf-109">EXAMPLES</span></span>

### <span data-ttu-id="e73bf-110">Exemplo 1: modificar um espaço de trabalho por nome</span><span class="sxs-lookup"><span data-stu-id="e73bf-110">Example 1: Modify a workspace by name</span></span>
```
PS C:\>Set-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku Standard -Tags @{ "Department" = "IT" }
```

<span data-ttu-id="e73bf-111">Esse comando modifica a SKU e as marcas do espaço de trabalho chamado MyWorkspace no grupo de recursos chamado ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="e73bf-111">This command modifies the SKU and tags of the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="e73bf-112">Exemplo 2: atualizar um espaço de trabalho usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="e73bf-112">Example 2: Update a workspace by using the pipeline</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Set-AzureRmOperationalInsightsWorkspace -Sku "Premium"
```

<span data-ttu-id="e73bf-113">Esse comando usa o cmdlet Get-AzureRmOperationalInsightsWorkspace para obter o espaço de trabalho chamado MyWorkspace e, em seguida, passa-o para o cmdlet **set-AzureRmOperationalInsightsWorkspace** usando o operador pipeline para definir a SKU como Premium.</span><span class="sxs-lookup"><span data-stu-id="e73bf-113">This command uses the Get-AzureRmOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkSpace, and then passes it to the **Set-AzureRmOperationalInsightsWorkspace** cmdlet by using the pipeline operator to set the SKU to Premium.</span></span>

## <span data-ttu-id="e73bf-114">OS</span><span class="sxs-lookup"><span data-stu-id="e73bf-114">PARAMETERS</span></span>

### <span data-ttu-id="e73bf-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="e73bf-115">-Name</span></span>
<span data-ttu-id="e73bf-116">Especifica o nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="e73bf-116">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="e73bf-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e73bf-117">-ResourceGroupName</span></span>
<span data-ttu-id="e73bf-118">Especifica o nome do grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="e73bf-118">Specifies the Azure resource group name.</span></span>

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

### <span data-ttu-id="e73bf-119">-SKU</span><span class="sxs-lookup"><span data-stu-id="e73bf-119">-Sku</span></span>
<span data-ttu-id="e73bf-120">Especifica a camada de serviço do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="e73bf-120">Specifies the service tier of the workspace.</span></span>
<span data-ttu-id="e73bf-121">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="e73bf-121">Valid values are:</span></span> 

- <span data-ttu-id="e73bf-122">gratuito</span><span class="sxs-lookup"><span data-stu-id="e73bf-122">free</span></span>
- <span data-ttu-id="e73bf-123">oficial</span><span class="sxs-lookup"><span data-stu-id="e73bf-123">standard</span></span>
- <span data-ttu-id="e73bf-124">gratifica</span><span class="sxs-lookup"><span data-stu-id="e73bf-124">premium</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: free, standard, premium

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e73bf-125">-Marcas</span><span class="sxs-lookup"><span data-stu-id="e73bf-125">-Tags</span></span>
<span data-ttu-id="e73bf-126">Especifica as marcas de recurso do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="e73bf-126">Specifies the resource tags for the workspace.</span></span>

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

### <span data-ttu-id="e73bf-127">-Espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="e73bf-127">-Workspace</span></span>
<span data-ttu-id="e73bf-128">Especifica o espaço de trabalho a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="e73bf-128">Specifies the workspace to be updated.</span></span>

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

### <span data-ttu-id="e73bf-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e73bf-129">-DefaultProfile</span></span>
<span data-ttu-id="e73bf-130">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e73bf-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e73bf-131">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="e73bf-131">-RetentionInDays</span></span>
<span data-ttu-id="e73bf-132">A retenção de dados do espaço de trabalho em dias.</span><span class="sxs-lookup"><span data-stu-id="e73bf-132">The workspace data retention in days.</span></span> <span data-ttu-id="e73bf-133">730 dias é o máximo permitido para todas as outras SKUs.</span><span class="sxs-lookup"><span data-stu-id="e73bf-133">730 days is the maximum allowed for all other Skus.</span></span>

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

### <span data-ttu-id="e73bf-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e73bf-134">CommonParameters</span></span>
<span data-ttu-id="e73bf-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e73bf-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e73bf-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e73bf-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e73bf-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e73bf-137">INPUTS</span></span>

### <span data-ttu-id="e73bf-138">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="e73bf-138">PSWorkspace</span></span>
<span data-ttu-id="e73bf-139">O parâmetro ' Workspace ' aceita o valor do tipo ' PSWorkspace ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="e73bf-139">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="e73bf-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e73bf-140">OUTPUTS</span></span>

### <span data-ttu-id="e73bf-141">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="e73bf-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="e73bf-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e73bf-142">NOTES</span></span>

## <span data-ttu-id="e73bf-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e73bf-143">RELATED LINKS</span></span>

[<span data-ttu-id="e73bf-144">Cmdlets do Azure Operational insights</span><span class="sxs-lookup"><span data-stu-id="e73bf-144">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="e73bf-145">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="e73bf-145">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)


