---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/new-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHub.md
ms.openlocfilehash: 392f9362df1cafdb6c047020b3381a7b16320607
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111856"
---
# <span data-ttu-id="2b3ab-101">New-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="2b3ab-101">New-AzIotHub</span></span>

## <span data-ttu-id="2b3ab-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2b3ab-102">SYNOPSIS</span></span>
<span data-ttu-id="2b3ab-103">Cria um novo IotHub.</span><span class="sxs-lookup"><span data-stu-id="2b3ab-103">Creates a new IotHub.</span></span>

## <span data-ttu-id="2b3ab-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2b3ab-104">SYNTAX</span></span>

```
New-AzIotHub -ResourceGroupName <String> -Name <String> -SkuName <PSIotHubSku> -Units <Int64>
 -Location <String> [-Properties <PSIotHubInputProperties>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b3ab-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="2b3ab-105">DESCRIPTION</span></span>
<span data-ttu-id="2b3ab-106">Cria um novo IotHub.</span><span class="sxs-lookup"><span data-stu-id="2b3ab-106">Creates a new IotHub.</span></span>
<span data-ttu-id="2b3ab-107">Você pode criar o IotHub com as propriedades padrão ou especificar as propriedades de entrada.</span><span class="sxs-lookup"><span data-stu-id="2b3ab-107">You can create the IotHub with either the default properties or specify the input properties.</span></span>

## <span data-ttu-id="2b3ab-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2b3ab-108">EXAMPLES</span></span>

### <span data-ttu-id="2b3ab-109">Exemplo 1 Criar um novo IotHub com propriedades padrão</span><span class="sxs-lookup"><span data-stu-id="2b3ab-109">Example 1 Create a new IotHub with default properties</span></span>
```
PS C:\> $tags = @{}
PS C:\> $tags.Add('key1','value1')
PS C:\> New-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope" -Tag $tags
```

<span data-ttu-id="2b3ab-110">Cria um novo IotHub chamado "myiothub" da sku "S1", capacidade 1 e local "northeurope" incluído nas Marcas.</span><span class="sxs-lookup"><span data-stu-id="2b3ab-110">Creates a new IotHub named "myiothub" of the sku "S1", capacity 1 and location "northeurope" included with Tags.</span></span>

### <span data-ttu-id="2b3ab-111">Exemplo 2 Criar um novo IotHub com a MaxDeliveryCount da Fila CloudToDevice definida como 20</span><span class="sxs-lookup"><span data-stu-id="2b3ab-111">Example 2 Create a new IotHub with the MaxDeliveryCount of the CloudToDevice Queue set to 20</span></span>
```
PS C:\> New-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope" -Properties $properties
```

<span data-ttu-id="2b3ab-112">Cria um novo IotHub chamado "myiothub" da sku "S1", capacidade 1 e local "northeurope" com propriedades de entrada avançadas representadas por $properties.</span><span class="sxs-lookup"><span data-stu-id="2b3ab-112">Creates a new IotHub named "myiothub" of the sku "S1", capacity 1 and location "northeurope" with advanced input properties represented by $properties.</span></span>
<span data-ttu-id="2b3ab-113">$psCloudToDeviceProperties = New-Object Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceProperties -Property @{MaxDeliveryCount=20} $properties = New-Object Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties -Property @{CloudToDevice=$psCloudToDeviceProperties} New-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope" -Properties $properties</span><span class="sxs-lookup"><span data-stu-id="2b3ab-113">$psCloudToDeviceProperties = New-Object Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceProperties -Property @{MaxDeliveryCount=20} $properties = New-Object Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties -Property @{CloudToDevice=$psCloudToDeviceProperties} New-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope" -Properties $properties</span></span>

## <span data-ttu-id="2b3ab-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2b3ab-114">PARAMETERS</span></span>

### <span data-ttu-id="2b3ab-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b3ab-115">-DefaultProfile</span></span>
<span data-ttu-id="2b3ab-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="2b3ab-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2b3ab-117">-Local</span><span class="sxs-lookup"><span data-stu-id="2b3ab-117">-Location</span></span>
<span data-ttu-id="2b3ab-118">Local onde o hub de IoT precisa ser criado.</span><span class="sxs-lookup"><span data-stu-id="2b3ab-118">Location where the IoT hub needs to be created.</span></span> 

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

### <span data-ttu-id="2b3ab-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="2b3ab-119">-Name</span></span>
<span data-ttu-id="2b3ab-120">Nome do IotHub</span><span class="sxs-lookup"><span data-stu-id="2b3ab-120">Name of the IotHub</span></span>

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

### <span data-ttu-id="2b3ab-121">-Propriedades</span><span class="sxs-lookup"><span data-stu-id="2b3ab-121">-Properties</span></span>
<span data-ttu-id="2b3ab-122">Propriedades do hub de IoT.</span><span class="sxs-lookup"><span data-stu-id="2b3ab-122">Properties of the IoT hub.</span></span> 

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

### <span data-ttu-id="2b3ab-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b3ab-123">-ResourceGroupName</span></span>
<span data-ttu-id="2b3ab-124">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="2b3ab-124">Resource Group Name</span></span>

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

### <span data-ttu-id="2b3ab-125">-SkuName</span><span class="sxs-lookup"><span data-stu-id="2b3ab-125">-SkuName</span></span>
<span data-ttu-id="2b3ab-126">Nome da sKU</span><span class="sxs-lookup"><span data-stu-id="2b3ab-126">Name of the sku</span></span>

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

### <span data-ttu-id="2b3ab-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="2b3ab-127">-Tag</span></span>
<span data-ttu-id="2b3ab-128">Marcas de instância do hub IoT.</span><span class="sxs-lookup"><span data-stu-id="2b3ab-128">IoT hub instance tags.</span></span> <span data-ttu-id="2b3ab-129">Bolsa de propriedades em pares de valor-chave na forma de uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="2b3ab-129">Property bag in key-value pairs in the form of a hash table.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b3ab-130">-Unidades</span><span class="sxs-lookup"><span data-stu-id="2b3ab-130">-Units</span></span>
<span data-ttu-id="2b3ab-131">Número de unidades</span><span class="sxs-lookup"><span data-stu-id="2b3ab-131">Number of units</span></span>

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

### <span data-ttu-id="2b3ab-132">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="2b3ab-132">-Confirm</span></span>
<span data-ttu-id="2b3ab-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b3ab-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b3ab-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b3ab-134">-WhatIf</span></span>
<span data-ttu-id="2b3ab-135">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="2b3ab-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b3ab-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2b3ab-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b3ab-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b3ab-137">CommonParameters</span></span>
<span data-ttu-id="2b3ab-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b3ab-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b3ab-139">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b3ab-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b3ab-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="2b3ab-140">INPUTS</span></span>

### <span data-ttu-id="2b3ab-141">System.String</span><span class="sxs-lookup"><span data-stu-id="2b3ab-141">System.String</span></span>

## <span data-ttu-id="2b3ab-142">Saídas</span><span class="sxs-lookup"><span data-stu-id="2b3ab-142">OUTPUTS</span></span>

### <span data-ttu-id="2b3ab-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="2b3ab-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="2b3ab-144">Notas</span><span class="sxs-lookup"><span data-stu-id="2b3ab-144">NOTES</span></span>

## <span data-ttu-id="2b3ab-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2b3ab-145">RELATED LINKS</span></span>
