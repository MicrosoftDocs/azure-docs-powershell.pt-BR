---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/resume-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Resume-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Resume-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: fe660d200c578d15fe8e23e7bfffc9a249651ae2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426672"
---
# <span data-ttu-id="2bac2-101">Resume-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="2bac2-101">Resume-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="2bac2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2bac2-102">SYNOPSIS</span></span>
<span data-ttu-id="2bac2-103">Retoma uma instância da capacidade inserida do PowerBI.</span><span class="sxs-lookup"><span data-stu-id="2bac2-103">Resumes an instance of PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2bac2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2bac2-104">SYNTAX</span></span>

```
Resume-AzureRmPowerBIEmbeddedCapacity 
    [-Name] <String> 
    [[-ResourceGroupName] <String>] 
    [-PassThru] 
    [-WhatIf]
    [-Confirm] 
    [<CommonParameters>]
```

## <span data-ttu-id="2bac2-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2bac2-105">DESCRIPTION</span></span>
<span data-ttu-id="2bac2-106">O cmdlet Resume-AzureRmPowerBIEmbeddedCapacity retoma uma instância da capacidade inserida do PowerBI</span><span class="sxs-lookup"><span data-stu-id="2bac2-106">The Resume-AzureRmPowerBIEmbeddedCapacity cmdlet resumes an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="2bac2-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2bac2-107">EXAMPLES</span></span>

### <span data-ttu-id="2bac2-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2bac2-108">Example 1</span></span>
```
PS C:\> Resume-AzureRmPowerBIEmbeddedCapacity -Name "testcapacity" -ResourceGroupName "testRG" -PassThru
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

<span data-ttu-id="2bac2-109">Esse comando retomará uma capacidade pausada chamada testcapacity no testRG do nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="2bac2-109">This command will resume a paused capacity named testcapacity in the resourcegroup testRG</span></span>

## <span data-ttu-id="2bac2-110">OS</span><span class="sxs-lookup"><span data-stu-id="2bac2-110">PARAMETERS</span></span>

### <span data-ttu-id="2bac2-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="2bac2-111">-Name</span></span>
<span data-ttu-id="2bac2-112">Nome da capacidade inserida do PowerBI</span><span class="sxs-lookup"><span data-stu-id="2bac2-112">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: String
Parameter Sets: ByNameAndResourceGroup
Aliases: 

Required: True
Position: 0
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="2bac2-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2bac2-113">-ResourceGroupName</span></span>
<span data-ttu-id="2bac2-114">Nome do grupo de recursos do Azure ao qual a capacidade pertence</span><span class="sxs-lookup"><span data-stu-id="2bac2-114">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: String
Parameter Sets: ByNameAndResourceGroup
Aliases: 

Required: False
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="2bac2-115">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2bac2-115">-ResourceId</span></span>
<span data-ttu-id="2bac2-116">ID do recurso do Azure</span><span class="sxs-lookup"><span data-stu-id="2bac2-116">Azure resource ID</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2bac2-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2bac2-117">-InputObject</span></span>
<span data-ttu-id="2bac2-118">Objeto de entrada para tubulação</span><span class="sxs-lookup"><span data-stu-id="2bac2-118">Input object for Piping</span></span>

```yaml
Type: PSPowerBIEmbeddedCapacity
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2bac2-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2bac2-119">-Confirm</span></span>
<span data-ttu-id="2bac2-120">Solicita que o usuário confirme se deseja executar a operação</span><span class="sxs-lookup"><span data-stu-id="2bac2-120">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="2bac2-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2bac2-121">-WhatIf</span></span>
<span data-ttu-id="2bac2-122">Descreve as ações que a operação atual executará sem realmente executá-las</span><span class="sxs-lookup"><span data-stu-id="2bac2-122">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="2bac2-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bac2-123">CommonParameters</span></span>
<span data-ttu-id="2bac2-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2bac2-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bac2-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2bac2-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bac2-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2bac2-126">INPUTS</span></span>

### <span data-ttu-id="2bac2-127">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="2bac2-127">None</span></span>
<span data-ttu-id="2bac2-128">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="2bac2-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2bac2-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2bac2-129">OUTPUTS</span></span>

### <span data-ttu-id="2bac2-130">Microsoft. Azure. Commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="2bac2-130">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="2bac2-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2bac2-131">NOTES</span></span>

## <span data-ttu-id="2bac2-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2bac2-132">RELATED LINKS</span></span>

[<span data-ttu-id="2bac2-133">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="2bac2-133">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="2bac2-134">Suspender-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="2bac2-134">Suspend-AzureRmPowerBIEmbeddedCapacity</span></span>](./Suspend-AzureRmPowerBIEmbeddedCapacity.md)
