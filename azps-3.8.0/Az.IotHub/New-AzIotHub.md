---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/new-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHub.md
ms.openlocfilehash: ad9c032a4384a82e03704529796a209e8c88f4c5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943815"
---
# <span data-ttu-id="72d4a-101">New-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="72d4a-101">New-AzIotHub</span></span>

## <span data-ttu-id="72d4a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="72d4a-102">SYNOPSIS</span></span>
<span data-ttu-id="72d4a-103">Cria um novo IotHub.</span><span class="sxs-lookup"><span data-stu-id="72d4a-103">Creates a new IotHub.</span></span>

## <span data-ttu-id="72d4a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="72d4a-104">SYNTAX</span></span>

```
New-AzIotHub -ResourceGroupName <String> -Name <String> -SkuName <PSIotHubSku> -Units <Int64>
 -Location <String> [-Properties <PSIotHubInputProperties>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72d4a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="72d4a-105">DESCRIPTION</span></span>
<span data-ttu-id="72d4a-106">Cria um novo IotHub.</span><span class="sxs-lookup"><span data-stu-id="72d4a-106">Creates a new IotHub.</span></span>
<span data-ttu-id="72d4a-107">Você pode criar o IotHub com as propriedades padrão ou especificar as propriedades de entrada.</span><span class="sxs-lookup"><span data-stu-id="72d4a-107">You can create the IotHub with either the default properties or specify the input properties.</span></span>

## <span data-ttu-id="72d4a-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="72d4a-108">EXAMPLES</span></span>

### <span data-ttu-id="72d4a-109">Exemplo 1 criar uma nova IotHub com propriedades padrão</span><span class="sxs-lookup"><span data-stu-id="72d4a-109">Example 1 Create a new IotHub with default properties</span></span>
```
PS C:\> New-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope"
```

<span data-ttu-id="72d4a-110">Cria um novo IotHub chamado "myiothub" do SKU "S1", a capacidade 1 e o local "northeurope".</span><span class="sxs-lookup"><span data-stu-id="72d4a-110">Creates a new IotHub named "myiothub" of the sku "S1", capacity 1 and location "northeurope".</span></span>

### <span data-ttu-id="72d4a-111">Exemplo 2 crie uma nova IotHub com o MaxDeliveryCount da fila CloudToDevice definida como 20</span><span class="sxs-lookup"><span data-stu-id="72d4a-111">Example 2 Create a new IotHub with the MaxDeliveryCount of the CloudToDevice Queue set to 20</span></span>
```
PS C:\> New-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope" -Properties $properties
```

<span data-ttu-id="72d4a-112">Cria um novo IotHub chamado "myiothub" do SKU "S1", a capacidade 1 e o local "northeurope" com propriedades de entrada avançadas representadas por $properties.</span><span class="sxs-lookup"><span data-stu-id="72d4a-112">Creates a new IotHub named "myiothub" of the sku "S1", capacity 1 and location "northeurope" with advanced input properties represented by $properties.</span></span>
<span data-ttu-id="72d4a-113">$psCloudToDeviceProperties = New-Object Microsoft. Azure. Commands. Management. IotHub. Models. PSCloudToDeviceProperties-Property @ {MaxDeliveryCount = 20} $properties = New-Object Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHubInputProperties-Property @ {CloudToDevice = $psCloudToDeviceProperties} New-AzIotHub-ResourceGroupName "myresourceus"-Name "myiothub"-SkuName "S1"-unidades 1-local "northeurope</span><span class="sxs-lookup"><span data-stu-id="72d4a-113">$psCloudToDeviceProperties = New-Object Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceProperties -Property @{MaxDeliveryCount=20} $properties = New-Object Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties -Property @{CloudToDevice=$psCloudToDeviceProperties} New-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope" -Properties $properties</span></span>

## <span data-ttu-id="72d4a-114">OS</span><span class="sxs-lookup"><span data-stu-id="72d4a-114">PARAMETERS</span></span>

### <span data-ttu-id="72d4a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72d4a-115">-DefaultProfile</span></span>
<span data-ttu-id="72d4a-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="72d4a-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="72d4a-117">-Local</span><span class="sxs-lookup"><span data-stu-id="72d4a-117">-Location</span></span>
<span data-ttu-id="72d4a-118">Local para onde o Hub IoT precisa ser criado.</span><span class="sxs-lookup"><span data-stu-id="72d4a-118">Location where the IoT hub needs to be created.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72d4a-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="72d4a-119">-Name</span></span>
<span data-ttu-id="72d4a-120">Nome do IotHub</span><span class="sxs-lookup"><span data-stu-id="72d4a-120">Name of the IotHub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72d4a-121">-Propriedades</span><span class="sxs-lookup"><span data-stu-id="72d4a-121">-Properties</span></span>
<span data-ttu-id="72d4a-122">Propriedades do Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="72d4a-122">Properties of the IoT hub.</span></span> 

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

### <span data-ttu-id="72d4a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72d4a-123">-ResourceGroupName</span></span>
<span data-ttu-id="72d4a-124">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="72d4a-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72d4a-125">-SkuName</span><span class="sxs-lookup"><span data-stu-id="72d4a-125">-SkuName</span></span>
<span data-ttu-id="72d4a-126">Nome da SKU</span><span class="sxs-lookup"><span data-stu-id="72d4a-126">Name of the sku</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSku
Parameter Sets: (All)
Aliases:
Accepted values: F1, S1, S2, S3, B1, B2, B3

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72d4a-127">-Unidades</span><span class="sxs-lookup"><span data-stu-id="72d4a-127">-Units</span></span>
<span data-ttu-id="72d4a-128">Número de unidades</span><span class="sxs-lookup"><span data-stu-id="72d4a-128">Number of units</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72d4a-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="72d4a-129">-Confirm</span></span>
<span data-ttu-id="72d4a-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72d4a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72d4a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72d4a-131">-WhatIf</span></span>
<span data-ttu-id="72d4a-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="72d4a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72d4a-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="72d4a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72d4a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72d4a-134">CommonParameters</span></span>
<span data-ttu-id="72d4a-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72d4a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72d4a-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72d4a-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72d4a-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="72d4a-137">INPUTS</span></span>

### <span data-ttu-id="72d4a-138">System. String</span><span class="sxs-lookup"><span data-stu-id="72d4a-138">System.String</span></span>

## <span data-ttu-id="72d4a-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="72d4a-139">OUTPUTS</span></span>

### <span data-ttu-id="72d4a-140">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="72d4a-140">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="72d4a-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="72d4a-141">NOTES</span></span>

## <span data-ttu-id="72d4a-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="72d4a-142">RELATED LINKS</span></span>
