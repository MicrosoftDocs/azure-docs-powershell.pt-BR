---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/remove-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Remove-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Remove-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: bbdfe43b4f6cad72432c85876c71bcd34a9a371c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93603254"
---
# <span data-ttu-id="61e4e-101">Remove-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="61e4e-101">Remove-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="61e4e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="61e4e-102">SYNOPSIS</span></span>
<span data-ttu-id="61e4e-103">Exclui uma instância da capacidade inserida do PowerBI.</span><span class="sxs-lookup"><span data-stu-id="61e4e-103">Deletes an instance of PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="61e4e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="61e4e-104">SYNTAX</span></span>

```
Remove-AzureRmPowerBIEmbeddedCapacity 
    [-Name] <String> 
    [[-ResourceGroupName] <String>] 
    [-PassThru] 
    [-WhatIf]
    [-Confirm] 
    [<CommonParameters>]
```

## <span data-ttu-id="61e4e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="61e4e-105">DESCRIPTION</span></span>
<span data-ttu-id="61e4e-106">O cmdlet Remove-AzureRmPowerBIEmbeddedCapacity exclui uma instância da capacidade inserida do PowerBI</span><span class="sxs-lookup"><span data-stu-id="61e4e-106">The Remove-AzureRmPowerBIEmbeddedCapacity cmdlet deletes an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="61e4e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="61e4e-107">EXAMPLES</span></span>

### <span data-ttu-id="61e4e-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="61e4e-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmPowerBIEmbeddedCapacity -Name "testcapacity" -ResourceGroupName "testRG"
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

<span data-ttu-id="61e4e-109">Esse comando removerá a capacidade denominada testcapacity no testRG de Resource</span><span class="sxs-lookup"><span data-stu-id="61e4e-109">This command will remove the capacity named testcapacity in the resourcegroup testRG</span></span>

## <span data-ttu-id="61e4e-110">OS</span><span class="sxs-lookup"><span data-stu-id="61e4e-110">PARAMETERS</span></span>

### <span data-ttu-id="61e4e-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61e4e-111">-ResourceGroupName</span></span>
<span data-ttu-id="61e4e-112">Nome do grupo de recursos do Azure ao qual a capacidade pertence</span><span class="sxs-lookup"><span data-stu-id="61e4e-112">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: String
Parameter Sets: ByNameAndResourceGroup
Aliases: 

Required: False
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="61e4e-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="61e4e-113">-Name</span></span>
<span data-ttu-id="61e4e-114">Nome da capacidade inserida do PowerBI</span><span class="sxs-lookup"><span data-stu-id="61e4e-114">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: String
Parameter Sets: ByNameAndResourceGroup
Aliases: 

Required: False
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="61e4e-115">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="61e4e-115">-ResourceId</span></span>
<span data-ttu-id="61e4e-116">ID do recurso do Azure</span><span class="sxs-lookup"><span data-stu-id="61e4e-116">Azure resource ID</span></span>

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

### <span data-ttu-id="61e4e-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="61e4e-117">-InputObject</span></span>
<span data-ttu-id="61e4e-118">Objeto de entrada para tubulação</span><span class="sxs-lookup"><span data-stu-id="61e4e-118">Input object for Piping</span></span>

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

### <span data-ttu-id="61e4e-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="61e4e-119">-PassThru</span></span>
<span data-ttu-id="61e4e-120">Retornará os detalhes de capacidade excluídos se a operação for concluída com êxito</span><span class="sxs-lookup"><span data-stu-id="61e4e-120">Will return the deleted capacity details if the operation completes successfully</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61e4e-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="61e4e-121">-Confirm</span></span>
<span data-ttu-id="61e4e-122">Solicita que o usuário confirme se deseja executar a operação</span><span class="sxs-lookup"><span data-stu-id="61e4e-122">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="61e4e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61e4e-123">-WhatIf</span></span>
<span data-ttu-id="61e4e-124">Descreve as ações que a operação atual executará sem realmente executá-las</span><span class="sxs-lookup"><span data-stu-id="61e4e-124">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="61e4e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61e4e-125">CommonParameters</span></span>
<span data-ttu-id="61e4e-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61e4e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61e4e-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61e4e-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61e4e-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="61e4e-128">INPUTS</span></span>

### <span data-ttu-id="61e4e-129">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="61e4e-129">None</span></span>
<span data-ttu-id="61e4e-130">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="61e4e-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="61e4e-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="61e4e-131">OUTPUTS</span></span>

### <span data-ttu-id="61e4e-132">Microsoft. Azure. Commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="61e4e-132">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="61e4e-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="61e4e-133">NOTES</span></span>

## <span data-ttu-id="61e4e-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="61e4e-134">RELATED LINKS</span></span>

[<span data-ttu-id="61e4e-135">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="61e4e-135">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="61e4e-136">New-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="61e4e-136">New-AzureRmPowerBIEmbeddedCapacity</span></span>](./New-AzureRmPowerBIEmbeddedCapacity.md)
