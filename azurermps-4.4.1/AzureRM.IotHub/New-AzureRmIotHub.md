---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/New-AzureRmIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/New-AzureRmIotHub.md
ms.openlocfilehash: ad491605fcba26f713fcf295c419990e9db6ff2b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610498"
---
# <span data-ttu-id="ac1b9-101">New-AzureRmIotHub</span><span class="sxs-lookup"><span data-stu-id="ac1b9-101">New-AzureRmIotHub</span></span>

## <span data-ttu-id="ac1b9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ac1b9-102">SYNOPSIS</span></span>
<span data-ttu-id="ac1b9-103">Cria um novo IotHub.</span><span class="sxs-lookup"><span data-stu-id="ac1b9-103">Creates a new IotHub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ac1b9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ac1b9-104">SYNTAX</span></span>

```
New-AzureRmIotHub [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <PSIotHubSku> [-Units] <Int64>
 [-Location] <String> [-Properties <PSIotHubInputProperties>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac1b9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ac1b9-105">DESCRIPTION</span></span>
<span data-ttu-id="ac1b9-106">Cria um novo IotHub.</span><span class="sxs-lookup"><span data-stu-id="ac1b9-106">Creates a new IotHub.</span></span>
<span data-ttu-id="ac1b9-107">Você pode criar o IotHub com as propriedades padrão ou especificar o proerties de entrada.</span><span class="sxs-lookup"><span data-stu-id="ac1b9-107">You can create the IotHub with either the default properties or specify the input proerties.</span></span>

## <span data-ttu-id="ac1b9-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ac1b9-108">EXAMPLES</span></span>

### <span data-ttu-id="ac1b9-109">Exemplo 1 criar uma nova IotHub com propriedades padrão</span><span class="sxs-lookup"><span data-stu-id="ac1b9-109">Example 1 Create a new IotHub with default properties</span></span>
```
PS C:\> New-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope"
```

<span data-ttu-id="ac1b9-110">Cria um novo IotHub chamado "myiothub" do SKU "S1", a capacidade 1 e o local "northeurope".</span><span class="sxs-lookup"><span data-stu-id="ac1b9-110">Creates a new IotHub named "myiothub" of the sku "S1", capacity 1 and location "northeurope".</span></span>

### <span data-ttu-id="ac1b9-111">Exemplo 2 crie uma nova IotHub com o MaxDeliveryCount da fila CloudtoDevice definida como 20</span><span class="sxs-lookup"><span data-stu-id="ac1b9-111">Example 2 Create a new IotHub with the MaxDeliveryCount of the CloudtoDevice Queue set to 20</span></span>
```
PS C:\> New-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope" -Properties $properties
```

<span data-ttu-id="ac1b9-112">Cria um novo IotHub chamado "myiothub" do SKU "S1", a capacidade 1 e o local "northeurope" com propriedades de entrada avançadas representadas por $properties.</span><span class="sxs-lookup"><span data-stu-id="ac1b9-112">Creates a new IotHub named "myiothub" of the sku "S1", capacity 1 and location "northeurope" with advanced input properties represented by $properties.</span></span>

<span data-ttu-id="ac1b9-113">$psCloudToDeviceProperties = New-Object Microsoft. Azure. Commands. Management. IotHub. Models. PSCloudToDeviceProperties-Property @ {MaxDeliveryCount = 20} $properties = New-Object Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHubInputProperties-Property @ {CloudToDevice = $psCloudToDeviceProperties} New-AzureRmIotHub-ResourceGroupName "myresourceus"-Name "myiothub"-SkuName "S1"-unidades 1-local "northeurope</span><span class="sxs-lookup"><span data-stu-id="ac1b9-113">$psCloudToDeviceProperties = New-Object Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceProperties -Property @{MaxDeliveryCount=20} $properties = New-Object Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties -Property @{CloudToDevice=$psCloudToDeviceProperties} New-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope" -Properties $properties</span></span>

## <span data-ttu-id="ac1b9-114">OS</span><span class="sxs-lookup"><span data-stu-id="ac1b9-114">PARAMETERS</span></span>

### <span data-ttu-id="ac1b9-115">-Local</span><span class="sxs-lookup"><span data-stu-id="ac1b9-115">-Location</span></span>
<span data-ttu-id="ac1b9-116">Local para onde o Hub IoT precisa ser criado.</span><span class="sxs-lookup"><span data-stu-id="ac1b9-116">Location where the IoT hub needs to be created.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac1b9-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="ac1b9-117">-Name</span></span>
<span data-ttu-id="ac1b9-118">Nome do IotHub</span><span class="sxs-lookup"><span data-stu-id="ac1b9-118">Name of the IotHub</span></span>

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

### <span data-ttu-id="ac1b9-119">-Propriedades</span><span class="sxs-lookup"><span data-stu-id="ac1b9-119">-Properties</span></span>
<span data-ttu-id="ac1b9-120">Propriedades do Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="ac1b9-120">Properties of the IoT hub.</span></span> 

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac1b9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac1b9-121">-ResourceGroupName</span></span>
<span data-ttu-id="ac1b9-122">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="ac1b9-122">Resource Group Name</span></span>

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

### <span data-ttu-id="ac1b9-123">-SkuName</span><span class="sxs-lookup"><span data-stu-id="ac1b9-123">-SkuName</span></span>
<span data-ttu-id="ac1b9-124">Nome da SKU</span><span class="sxs-lookup"><span data-stu-id="ac1b9-124">Name of the sku</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSku
Parameter Sets: (All)
Aliases: 
Accepted values: F1, S1, S2, S3

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac1b9-125">-Unidades</span><span class="sxs-lookup"><span data-stu-id="ac1b9-125">-Units</span></span>
<span data-ttu-id="ac1b9-126">Número de unidades</span><span class="sxs-lookup"><span data-stu-id="ac1b9-126">Number of units</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac1b9-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ac1b9-127">-Confirm</span></span>
<span data-ttu-id="ac1b9-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ac1b9-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac1b9-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac1b9-129">-WhatIf</span></span>
<span data-ttu-id="ac1b9-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ac1b9-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac1b9-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ac1b9-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac1b9-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac1b9-132">-DefaultProfile</span></span>
<span data-ttu-id="ac1b9-133">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ac1b9-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac1b9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac1b9-134">CommonParameters</span></span>
<span data-ttu-id="ac1b9-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac1b9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac1b9-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac1b9-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac1b9-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ac1b9-137">INPUTS</span></span>

### <span data-ttu-id="ac1b9-138">System. String</span><span class="sxs-lookup"><span data-stu-id="ac1b9-138">System.String</span></span>
<span data-ttu-id="ac1b9-139">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHubSku System. Int64 Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHubInputProperties</span><span class="sxs-lookup"><span data-stu-id="ac1b9-139">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSku System.Int64 Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties</span></span>

## <span data-ttu-id="ac1b9-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ac1b9-140">OUTPUTS</span></span>

### <span data-ttu-id="ac1b9-141">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="ac1b9-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="ac1b9-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ac1b9-142">NOTES</span></span>

## <span data-ttu-id="ac1b9-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ac1b9-143">RELATED LINKS</span></span>

