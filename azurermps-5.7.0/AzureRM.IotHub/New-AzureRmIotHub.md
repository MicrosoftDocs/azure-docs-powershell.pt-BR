---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/new-azurermiothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/New-AzureRmIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/New-AzureRmIotHub.md
ms.openlocfilehash: c24f8f9e95db65b464da6586d9e3499358fc3edd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440458"
---
# <span data-ttu-id="f82d3-101">New-AzureRmIotHub</span><span class="sxs-lookup"><span data-stu-id="f82d3-101">New-AzureRmIotHub</span></span>

## <span data-ttu-id="f82d3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f82d3-102">SYNOPSIS</span></span>
<span data-ttu-id="f82d3-103">Cria um novo IotHub.</span><span class="sxs-lookup"><span data-stu-id="f82d3-103">Creates a new IotHub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f82d3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f82d3-104">SYNTAX</span></span>

```
New-AzureRmIotHub -ResourceGroupName <String> -Name <String> -SkuName <PSIotHubSku> -Units <Int64>
 -Location <String> [-Properties <PSIotHubInputProperties>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f82d3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f82d3-105">DESCRIPTION</span></span>
<span data-ttu-id="f82d3-106">Cria um novo IotHub.</span><span class="sxs-lookup"><span data-stu-id="f82d3-106">Creates a new IotHub.</span></span>
<span data-ttu-id="f82d3-107">Você pode criar o IotHub com as propriedades padrão ou especificar o proerties de entrada.</span><span class="sxs-lookup"><span data-stu-id="f82d3-107">You can create the IotHub with either the default properties or specify the input proerties.</span></span>

## <span data-ttu-id="f82d3-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f82d3-108">EXAMPLES</span></span>

### <span data-ttu-id="f82d3-109">Exemplo 1 criar uma nova IotHub com propriedades padrão</span><span class="sxs-lookup"><span data-stu-id="f82d3-109">Example 1 Create a new IotHub with default properties</span></span>
```
PS C:\> New-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope"
```

<span data-ttu-id="f82d3-110">Cria um novo IotHub chamado "myiothub" do SKU "S1", a capacidade 1 e o local "northeurope".</span><span class="sxs-lookup"><span data-stu-id="f82d3-110">Creates a new IotHub named "myiothub" of the sku "S1", capacity 1 and location "northeurope".</span></span>

### <span data-ttu-id="f82d3-111">Exemplo 2 crie uma nova IotHub com o MaxDeliveryCount da fila CloudtoDevice definida como 20</span><span class="sxs-lookup"><span data-stu-id="f82d3-111">Example 2 Create a new IotHub with the MaxDeliveryCount of the CloudtoDevice Queue set to 20</span></span>
```
PS C:\> New-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope" -Properties $properties
```

<span data-ttu-id="f82d3-112">Cria um novo IotHub chamado "myiothub" do SKU "S1", a capacidade 1 e o local "northeurope" com propriedades de entrada avançadas representadas por $properties.</span><span class="sxs-lookup"><span data-stu-id="f82d3-112">Creates a new IotHub named "myiothub" of the sku "S1", capacity 1 and location "northeurope" with advanced input properties represented by $properties.</span></span>

<span data-ttu-id="f82d3-113">$psCloudToDeviceProperties = New-Object Microsoft. Azure. Commands. Management. IotHub. Models. PSCloudToDeviceProperties-Property @ {MaxDeliveryCount = 20} $properties = New-Object Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHubInputProperties-Property @ {CloudToDevice = $psCloudToDeviceProperties} New-AzureRmIotHub-ResourceGroupName "myresourceus"-Name "myiothub"-SkuName "S1"-unidades 1-local "northeurope</span><span class="sxs-lookup"><span data-stu-id="f82d3-113">$psCloudToDeviceProperties = New-Object Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceProperties -Property @{MaxDeliveryCount=20} $properties = New-Object Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties -Property @{CloudToDevice=$psCloudToDeviceProperties} New-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope" -Properties $properties</span></span>

## <span data-ttu-id="f82d3-114">OS</span><span class="sxs-lookup"><span data-stu-id="f82d3-114">PARAMETERS</span></span>

### <span data-ttu-id="f82d3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f82d3-115">-DefaultProfile</span></span>
<span data-ttu-id="f82d3-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="f82d3-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f82d3-117">-Local</span><span class="sxs-lookup"><span data-stu-id="f82d3-117">-Location</span></span>
<span data-ttu-id="f82d3-118">Local para onde o Hub IoT precisa ser criado.</span><span class="sxs-lookup"><span data-stu-id="f82d3-118">Location where the IoT hub needs to be created.</span></span> 

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f82d3-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="f82d3-119">-Name</span></span>
<span data-ttu-id="f82d3-120">Nome do IotHub</span><span class="sxs-lookup"><span data-stu-id="f82d3-120">Name of the IotHub</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f82d3-121">-Propriedades</span><span class="sxs-lookup"><span data-stu-id="f82d3-121">-Properties</span></span>
<span data-ttu-id="f82d3-122">Propriedades do Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="f82d3-122">Properties of the IoT hub.</span></span> 

```yaml
Type: PSIotHubInputProperties
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f82d3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f82d3-123">-ResourceGroupName</span></span>
<span data-ttu-id="f82d3-124">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="f82d3-124">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f82d3-125">-SkuName</span><span class="sxs-lookup"><span data-stu-id="f82d3-125">-SkuName</span></span>
<span data-ttu-id="f82d3-126">Nome da SKU</span><span class="sxs-lookup"><span data-stu-id="f82d3-126">Name of the sku</span></span>

```yaml
Type: PSIotHubSku
Parameter Sets: (All)
Aliases: 
Accepted values: F1, S1, S2, S3

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f82d3-127">-Unidades</span><span class="sxs-lookup"><span data-stu-id="f82d3-127">-Units</span></span>
<span data-ttu-id="f82d3-128">Número de unidades</span><span class="sxs-lookup"><span data-stu-id="f82d3-128">Number of units</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f82d3-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f82d3-129">-Confirm</span></span>
<span data-ttu-id="f82d3-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f82d3-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f82d3-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f82d3-131">-WhatIf</span></span>
<span data-ttu-id="f82d3-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f82d3-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f82d3-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f82d3-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f82d3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f82d3-134">CommonParameters</span></span>
<span data-ttu-id="f82d3-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f82d3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f82d3-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f82d3-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f82d3-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f82d3-137">INPUTS</span></span>

### <span data-ttu-id="f82d3-138">System. String</span><span class="sxs-lookup"><span data-stu-id="f82d3-138">System.String</span></span>
<span data-ttu-id="f82d3-139">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHubSku System. Int64 Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHubInputProperties</span><span class="sxs-lookup"><span data-stu-id="f82d3-139">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSku System.Int64 Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties</span></span>

## <span data-ttu-id="f82d3-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f82d3-140">OUTPUTS</span></span>

### <span data-ttu-id="f82d3-141">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="f82d3-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="f82d3-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f82d3-142">NOTES</span></span>

## <span data-ttu-id="f82d3-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f82d3-143">RELATED LINKS</span></span>

