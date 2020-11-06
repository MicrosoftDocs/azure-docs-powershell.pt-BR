---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/new-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/New-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/New-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 6badeec8b2425a5ca8e10dc88039a1d28e055cc4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428120"
---
# <span data-ttu-id="a9d17-101">New-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="a9d17-101">New-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="a9d17-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a9d17-102">SYNOPSIS</span></span>
<span data-ttu-id="a9d17-103">Cria uma nova capacidade inserida do PowerBI.</span><span class="sxs-lookup"><span data-stu-id="a9d17-103">Creates a new PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a9d17-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a9d17-104">SYNTAX</span></span>

```
New-AzureRmPowerBIEmbeddedCapacity 
    [-ResourceGroupName] <String> 
    [-Name] <String> 
    [-Location] <String>
    [-Sku] <String> 
    [-Administrator] <String>
    [[-Tag] <Hashtable>] 
    [-WhatIf] 
    [-Confirm] 
    [<CommonParameters>]
```

## <span data-ttu-id="a9d17-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a9d17-105">DESCRIPTION</span></span>
<span data-ttu-id="a9d17-106">O cmdlet New-AzureRmPowerBIEmbeddedCapacity cria uma nova capacidade inserida do PowerBI</span><span class="sxs-lookup"><span data-stu-id="a9d17-106">The New-AzureRmPowerBIEmbeddedCapacity cmdlet creates a new PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="a9d17-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a9d17-107">EXAMPLES</span></span>

### <span data-ttu-id="a9d17-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a9d17-108">Example 1</span></span>
```
PS C:\> New-AzureRmPowerBIEmbeddedCapacity -ResourceGroupName "testRG" -Name "testcapacity" -Location "West Central US" -Sku "A1" -Administrator admin@microsoft.com
Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/testcapacity
ResourceGroup          : testRG
Name                   : testcapacity
Location               : West Central US
State                  : Succeeded
Administrator          : {admin@microsoft.com}
Sku                    : A1
Tier                   : PBIE_Azure
Tag                    : {}
```

<span data-ttu-id="a9d17-109">Cria uma capacidade chamada testcapacity na região do Azure oeste centro dos EUA e na testRG do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a9d17-109">Creates a capacity named testcapacity in the Azure region West Central US and in resource group testRG.</span></span> <span data-ttu-id="a9d17-110">O nível de SKU para a capacidade será a1.</span><span class="sxs-lookup"><span data-stu-id="a9d17-110">The sku level for the capacity will be A1.</span></span>

## <span data-ttu-id="a9d17-111">OS</span><span class="sxs-lookup"><span data-stu-id="a9d17-111">PARAMETERS</span></span>

### <span data-ttu-id="a9d17-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9d17-112">-ResourceGroupName</span></span>
<span data-ttu-id="a9d17-113">Nome do grupo de recursos do Azure ao qual a capacidade pertence</span><span class="sxs-lookup"><span data-stu-id="a9d17-113">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="a9d17-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="a9d17-114">-Name</span></span>
<span data-ttu-id="a9d17-115">Nome da capacidade inserida do PowerBI</span><span class="sxs-lookup"><span data-stu-id="a9d17-115">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="a9d17-116">-Local</span><span class="sxs-lookup"><span data-stu-id="a9d17-116">-Location</span></span>
<span data-ttu-id="a9d17-117">A região do Azure na qual a capacidade incorporada do PowerBI está hospedada</span><span class="sxs-lookup"><span data-stu-id="a9d17-117">The Azure region where the PowerBI Embedded Capacity is hosted</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="a9d17-118">-SKU</span><span class="sxs-lookup"><span data-stu-id="a9d17-118">-Sku</span></span>
<span data-ttu-id="a9d17-119">O nome da SKU para a capacidade.</span><span class="sxs-lookup"><span data-stu-id="a9d17-119">The name of the Sku for the capacity.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: A1, A2, A3, A4, A5, A6

Required: True
Position: 3
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="a9d17-120">-Administrador</span><span class="sxs-lookup"><span data-stu-id="a9d17-120">-Administrator</span></span>
<span data-ttu-id="a9d17-121">Um nome de capacidade separada por vírgulas para definir como administrador na capacidade</span><span class="sxs-lookup"><span data-stu-id="a9d17-121">A comma separated capacity names to set as administrator on the capacity</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="a9d17-122">-Marca</span><span class="sxs-lookup"><span data-stu-id="a9d17-122">-Tag</span></span>
<span data-ttu-id="a9d17-123">Pares de valores chave na forma de uma tabela de hash definidas como marcas na capacidade.</span><span class="sxs-lookup"><span data-stu-id="a9d17-123">Key-value pairs in the form of a hash table set as tags on the capacity.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="a9d17-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a9d17-124">-Confirm</span></span>
<span data-ttu-id="a9d17-125">Solicita que o usuário confirme se deseja executar a operação</span><span class="sxs-lookup"><span data-stu-id="a9d17-125">Prompts user to confirm whether to perform the operation</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9d17-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9d17-126">-WhatIf</span></span>
<span data-ttu-id="a9d17-127">Descreve as ações que a operação atual executará sem realmente executá-las</span><span class="sxs-lookup"><span data-stu-id="a9d17-127">Describes the actions the current operation will perform without actually performing them</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9d17-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9d17-128">CommonParameters</span></span>
<span data-ttu-id="a9d17-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9d17-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9d17-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9d17-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9d17-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a9d17-131">INPUTS</span></span>

### <span data-ttu-id="a9d17-132">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="a9d17-132">None</span></span>
<span data-ttu-id="a9d17-133">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="a9d17-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a9d17-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a9d17-134">OUTPUTS</span></span>

### <span data-ttu-id="a9d17-135">Microsoft. Azure. Commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="a9d17-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="a9d17-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a9d17-136">NOTES</span></span>

## <span data-ttu-id="a9d17-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a9d17-137">RELATED LINKS</span></span>

[<span data-ttu-id="a9d17-138">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="a9d17-138">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="a9d17-139">Remove-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="a9d17-139">Remove-AzureRmPowerBIEmbeddedCapacity</span></span>](./Remove-AzureRmPowerBIEmbeddedCapacity.md)
