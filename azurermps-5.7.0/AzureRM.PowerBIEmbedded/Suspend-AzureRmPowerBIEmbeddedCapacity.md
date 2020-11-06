---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/suspend-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Suspend-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Suspend-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: fd50133d4919c52f314ccb7e306a022712e552c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426665"
---
# <span data-ttu-id="56e53-101">Suspend-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="56e53-101">Suspend-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="56e53-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="56e53-102">SYNOPSIS</span></span>
<span data-ttu-id="56e53-103">Suspende uma instância da capacidade inserida do PowerBI.</span><span class="sxs-lookup"><span data-stu-id="56e53-103">Suspends an instance of PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="56e53-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="56e53-104">SYNTAX</span></span>

```
Suspend-AzureRmPowerBIEmbeddedCapacity 
    [-Name] <String> 
    [[-ResourceGroupName] <String>] 
    [-PassThru] 
    [-WhatIf]
    [-Confirm] 
    [<CommonParameters>]
```

## <span data-ttu-id="56e53-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="56e53-105">DESCRIPTION</span></span>
<span data-ttu-id="56e53-106">O cmdlet Suspend-AzureRmPowerBIEmbeddedCapacity suspende uma instância da capacidade inserida do PowerBI</span><span class="sxs-lookup"><span data-stu-id="56e53-106">The Suspend-AzureRmPowerBIEmbeddedCapacity cmdlet suspends an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="56e53-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="56e53-107">EXAMPLES</span></span>

### <span data-ttu-id="56e53-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="56e53-108">Example 1</span></span>
```
PS C:\> Suspend-AzureRmPowerBIEmbeddedCapacity -Name "testcapacity" -ResourceGroupName "testRG" -PassThru
Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/testcapacity
ResourceGroup          : testRG
Name                   : testcapacity
Location               : West Central US
State                  : Paused
Administrator          : {admin@microsoft.com}
Sku                    : A1
Tier                   : PBIE_Azure
Tag                    : {}
```

<span data-ttu-id="56e53-109">Esse comando suspenderá uma capacidade ativa nomeada testcapacity no modo de teste do mymodo de origem</span><span class="sxs-lookup"><span data-stu-id="56e53-109">This command will suspend an active capacity named testcapacity in the resourcegroup testgroup</span></span>

## <span data-ttu-id="56e53-110">OS</span><span class="sxs-lookup"><span data-stu-id="56e53-110">PARAMETERS</span></span>

### <span data-ttu-id="56e53-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="56e53-111">-Name</span></span>
<span data-ttu-id="56e53-112">Nome da capacidade inserida do PowerBI</span><span class="sxs-lookup"><span data-stu-id="56e53-112">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: String
Parameter Sets: ByNameAndResourceGroup
Aliases: 

Required: True
Position: 0
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="56e53-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56e53-113">-ResourceGroupName</span></span>
<span data-ttu-id="56e53-114">Nome do grupo de recursos do Azure ao qual a capacidade pertence</span><span class="sxs-lookup"><span data-stu-id="56e53-114">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: String
Parameter Sets: ByNameAndResourceGroup
Aliases: 

Required: False
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="56e53-115">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="56e53-115">-ResourceId</span></span>
<span data-ttu-id="56e53-116">ID do recurso do Azure</span><span class="sxs-lookup"><span data-stu-id="56e53-116">Azure resource ID</span></span>

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

### <span data-ttu-id="56e53-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="56e53-117">-InputObject</span></span>
<span data-ttu-id="56e53-118">Objeto de entrada para tubulação</span><span class="sxs-lookup"><span data-stu-id="56e53-118">Input object for Piping</span></span>

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

### <span data-ttu-id="56e53-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="56e53-119">-Confirm</span></span>
<span data-ttu-id="56e53-120">Solicita que o usuário confirme se deseja executar a operação</span><span class="sxs-lookup"><span data-stu-id="56e53-120">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="56e53-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56e53-121">-WhatIf</span></span>
<span data-ttu-id="56e53-122">Descreve as ações que a operação atual executará sem realmente executá-las</span><span class="sxs-lookup"><span data-stu-id="56e53-122">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="56e53-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56e53-123">CommonParameters</span></span>
<span data-ttu-id="56e53-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56e53-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56e53-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56e53-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56e53-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="56e53-126">INPUTS</span></span>

### <span data-ttu-id="56e53-127">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="56e53-127">None</span></span>
<span data-ttu-id="56e53-128">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="56e53-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="56e53-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="56e53-129">OUTPUTS</span></span>

### <span data-ttu-id="56e53-130">Microsoft. Azure. Commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="56e53-130">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="56e53-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="56e53-131">NOTES</span></span>

## <span data-ttu-id="56e53-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="56e53-132">RELATED LINKS</span></span>

[<span data-ttu-id="56e53-133">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="56e53-133">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="56e53-134">Currículo-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="56e53-134">Resume-AzureRmPowerBIEmbeddedCapacity</span></span>](./Resume-AzureRmPowerBIEmbeddedCapacity.md)

