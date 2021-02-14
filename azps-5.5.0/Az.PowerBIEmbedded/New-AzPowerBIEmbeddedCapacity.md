---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/new-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/New-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/New-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 3b0f64101972e7803961a08565af33ee08b34696
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117256"
---
# <span data-ttu-id="72b6e-101">New-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="72b6e-101">New-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="72b6e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="72b6e-102">SYNOPSIS</span></span>
<span data-ttu-id="72b6e-103">Cria uma nova Capacidade Inserida do PowerBI.</span><span class="sxs-lookup"><span data-stu-id="72b6e-103">Creates a new PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="72b6e-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="72b6e-104">SYNTAX</span></span>

```
New-AzPowerBIEmbeddedCapacity [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Sku] <String> [-Administrator] <String[]> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72b6e-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="72b6e-105">DESCRIPTION</span></span>
<span data-ttu-id="72b6e-106">O New-AzPowerBIEmbeddedCapacity cmdlet cria uma nova Capacidade Inserida do PowerBI</span><span class="sxs-lookup"><span data-stu-id="72b6e-106">The New-AzPowerBIEmbeddedCapacity cmdlet creates a new PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="72b6e-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="72b6e-107">EXAMPLES</span></span>

### <span data-ttu-id="72b6e-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="72b6e-108">Example 1</span></span>
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

<span data-ttu-id="72b6e-109">Cria uma capacidade chamada testcapacity na região do Azure oeste dos EUA e no testRG do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="72b6e-109">Creates a capacity named testcapacity in the Azure region West Central US and in resource group testRG.</span></span> <span data-ttu-id="72b6e-110">O nível de sku para a capacidade será A1.</span><span class="sxs-lookup"><span data-stu-id="72b6e-110">The sku level for the capacity will be A1.</span></span>

## <span data-ttu-id="72b6e-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="72b6e-111">PARAMETERS</span></span>

### <span data-ttu-id="72b6e-112">-Administrador</span><span class="sxs-lookup"><span data-stu-id="72b6e-112">-Administrator</span></span>
<span data-ttu-id="72b6e-113">Nomes separados por vírgulas para definir como administrador na capacidade</span><span class="sxs-lookup"><span data-stu-id="72b6e-113">A comma separated names to set as administrator on the capacity</span></span>

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

### <span data-ttu-id="72b6e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72b6e-114">-DefaultProfile</span></span>
<span data-ttu-id="72b6e-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="72b6e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72b6e-116">-Local</span><span class="sxs-lookup"><span data-stu-id="72b6e-116">-Location</span></span>
<span data-ttu-id="72b6e-117">A região do Azure onde a Capacidade Inserida do PowerBI está hospedada</span><span class="sxs-lookup"><span data-stu-id="72b6e-117">The Azure region where the PowerBI Embedded Capacity is hosted</span></span>

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

### <span data-ttu-id="72b6e-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="72b6e-118">-Name</span></span>
<span data-ttu-id="72b6e-119">Nome da Capacidade Inserida do PowerBI</span><span class="sxs-lookup"><span data-stu-id="72b6e-119">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="72b6e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72b6e-120">-ResourceGroupName</span></span>
<span data-ttu-id="72b6e-121">Nome do grupo de recursos do Azure ao qual a capacidade pertence</span><span class="sxs-lookup"><span data-stu-id="72b6e-121">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="72b6e-122">-SKU</span><span class="sxs-lookup"><span data-stu-id="72b6e-122">-Sku</span></span>
<span data-ttu-id="72b6e-123">O nome da SKU para a capacidade.</span><span class="sxs-lookup"><span data-stu-id="72b6e-123">The name of the Sku for the capacity.</span></span>

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

### <span data-ttu-id="72b6e-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="72b6e-124">-Tag</span></span>
<span data-ttu-id="72b6e-125">Pares de valor-chave na forma de uma tabela hash definida como marcas na capacidade.</span><span class="sxs-lookup"><span data-stu-id="72b6e-125">Key-value pairs in the form of a hash table set as tags on the capacity.</span></span>

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

### <span data-ttu-id="72b6e-126">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="72b6e-126">-Confirm</span></span>
<span data-ttu-id="72b6e-127">Solicita que o usuário confirme se a operação será realizada</span><span class="sxs-lookup"><span data-stu-id="72b6e-127">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="72b6e-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72b6e-128">-WhatIf</span></span>
<span data-ttu-id="72b6e-129">Descreve as ações que a operação atual executará sem realmente executa-las</span><span class="sxs-lookup"><span data-stu-id="72b6e-129">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="72b6e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72b6e-130">CommonParameters</span></span>
<span data-ttu-id="72b6e-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72b6e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72b6e-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72b6e-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72b6e-133">Entradas</span><span class="sxs-lookup"><span data-stu-id="72b6e-133">INPUTS</span></span>

### <span data-ttu-id="72b6e-134">System.String</span><span class="sxs-lookup"><span data-stu-id="72b6e-134">System.String</span></span>

### <span data-ttu-id="72b6e-135">System.String[]</span><span class="sxs-lookup"><span data-stu-id="72b6e-135">System.String[]</span></span>

### <span data-ttu-id="72b6e-136">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="72b6e-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="72b6e-137">Saídas</span><span class="sxs-lookup"><span data-stu-id="72b6e-137">OUTPUTS</span></span>

### <span data-ttu-id="72b6e-138">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="72b6e-138">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="72b6e-139">Notas</span><span class="sxs-lookup"><span data-stu-id="72b6e-139">NOTES</span></span>

## <span data-ttu-id="72b6e-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="72b6e-140">RELATED LINKS</span></span>

[<span data-ttu-id="72b6e-141">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="72b6e-141">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="72b6e-142">Remove-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="72b6e-142">Remove-AzPowerBIEmbeddedCapacity</span></span>](./Remove-AzPowerBIEmbeddedCapacity.md)
