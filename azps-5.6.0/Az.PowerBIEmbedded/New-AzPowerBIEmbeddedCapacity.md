---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/powershell/module/az.powerbiembedded/new-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/New-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/New-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 86531beb13ef70f8c35de7f4921277b0f9fa0bf2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885568"
---
# <span data-ttu-id="b6a5e-101">New-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="b6a5e-101">New-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="b6a5e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6a5e-102">SYNOPSIS</span></span>
<span data-ttu-id="b6a5e-103">Cria uma nova Capacidade Incorporada do PowerBI.</span><span class="sxs-lookup"><span data-stu-id="b6a5e-103">Creates a new PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="b6a5e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b6a5e-104">SYNTAX</span></span>

```
New-AzPowerBIEmbeddedCapacity [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Sku] <String> [-Administrator] <String[]> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6a5e-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b6a5e-105">DESCRIPTION</span></span>
<span data-ttu-id="b6a5e-106">O New-AzPowerBIEmbeddedCapacity cmdlet cria uma nova Capacidade Incorporada do PowerBI</span><span class="sxs-lookup"><span data-stu-id="b6a5e-106">The New-AzPowerBIEmbeddedCapacity cmdlet creates a new PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="b6a5e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b6a5e-107">EXAMPLES</span></span>

### <span data-ttu-id="b6a5e-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b6a5e-108">Example 1</span></span>
```
PS C:\> New-AzPowerBIEmbeddedCapacity -ResourceGroupName "testRG" -Name "testcapacity" -Location "West Central US" -Sku "A1" -Administrator admin@microsoft.com
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

<span data-ttu-id="b6a5e-109">Cria uma capacidade denominada testcapacity na região centro-oeste dos EUA do Azure e no testRG do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b6a5e-109">Creates a capacity named testcapacity in the Azure region West Central US and in resource group testRG.</span></span> <span data-ttu-id="b6a5e-110">O nível sku da capacidade será A1.</span><span class="sxs-lookup"><span data-stu-id="b6a5e-110">The sku level for the capacity will be A1.</span></span>

## <span data-ttu-id="b6a5e-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b6a5e-111">PARAMETERS</span></span>

### <span data-ttu-id="b6a5e-112">-Administrator</span><span class="sxs-lookup"><span data-stu-id="b6a5e-112">-Administrator</span></span>
<span data-ttu-id="b6a5e-113">Nomes separados por vírgulas para definir como administrador na capacidade</span><span class="sxs-lookup"><span data-stu-id="b6a5e-113">A comma separated names to set as administrator on the capacity</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6a5e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6a5e-114">-DefaultProfile</span></span>
<span data-ttu-id="b6a5e-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b6a5e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6a5e-116">-Location</span><span class="sxs-lookup"><span data-stu-id="b6a5e-116">-Location</span></span>
<span data-ttu-id="b6a5e-117">A região do Azure onde a Capacidade Incorporada do PowerBI está hospedada</span><span class="sxs-lookup"><span data-stu-id="b6a5e-117">The Azure region where the PowerBI Embedded Capacity is hosted</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6a5e-118">-Name</span><span class="sxs-lookup"><span data-stu-id="b6a5e-118">-Name</span></span>
<span data-ttu-id="b6a5e-119">Nome da Capacidade Incorporada do PowerBI</span><span class="sxs-lookup"><span data-stu-id="b6a5e-119">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="b6a5e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6a5e-120">-ResourceGroupName</span></span>
<span data-ttu-id="b6a5e-121">Nome do grupo de recursos do Azure ao qual a capacidade pertence</span><span class="sxs-lookup"><span data-stu-id="b6a5e-121">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="b6a5e-122">-Sku</span><span class="sxs-lookup"><span data-stu-id="b6a5e-122">-Sku</span></span>
<span data-ttu-id="b6a5e-123">O nome do Sku para a capacidade.</span><span class="sxs-lookup"><span data-stu-id="b6a5e-123">The name of the Sku for the capacity.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: A1, A2, A3, A4, A5, A6

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6a5e-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="b6a5e-124">-Tag</span></span>
<span data-ttu-id="b6a5e-125">Pares de valores-chave na forma de um conjunto de tabelas de hash como marcas na capacidade.</span><span class="sxs-lookup"><span data-stu-id="b6a5e-125">Key-value pairs in the form of a hash table set as tags on the capacity.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6a5e-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b6a5e-126">-Confirm</span></span>
<span data-ttu-id="b6a5e-127">Solicita que o usuário confirme se deve executar a operação</span><span class="sxs-lookup"><span data-stu-id="b6a5e-127">Prompts user to confirm whether to perform the operation</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6a5e-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6a5e-128">-WhatIf</span></span>
<span data-ttu-id="b6a5e-129">Descreve as ações que a operação atual executará sem realmente performá-las</span><span class="sxs-lookup"><span data-stu-id="b6a5e-129">Describes the actions the current operation will perform without actually performing them</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6a5e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6a5e-130">CommonParameters</span></span>
<span data-ttu-id="b6a5e-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6a5e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6a5e-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6a5e-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6a5e-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b6a5e-133">INPUTS</span></span>

### <span data-ttu-id="b6a5e-134">System.String</span><span class="sxs-lookup"><span data-stu-id="b6a5e-134">System.String</span></span>

### <span data-ttu-id="b6a5e-135">System.String[]</span><span class="sxs-lookup"><span data-stu-id="b6a5e-135">System.String[]</span></span>

### <span data-ttu-id="b6a5e-136">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="b6a5e-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="b6a5e-137">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b6a5e-137">OUTPUTS</span></span>

### <span data-ttu-id="b6a5e-138">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="b6a5e-138">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="b6a5e-139">NOTES</span><span class="sxs-lookup"><span data-stu-id="b6a5e-139">NOTES</span></span>

## <span data-ttu-id="b6a5e-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b6a5e-140">RELATED LINKS</span></span>

[<span data-ttu-id="b6a5e-141">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="b6a5e-141">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="b6a5e-142">Remove-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="b6a5e-142">Remove-AzPowerBIEmbeddedCapacity</span></span>](./Remove-AzPowerBIEmbeddedCapacity.md)
