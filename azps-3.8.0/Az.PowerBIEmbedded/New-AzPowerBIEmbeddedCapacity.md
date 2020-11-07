---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/new-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/New-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/New-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 3b0f64101972e7803961a08565af33ee08b34696
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93940626"
---
# <span data-ttu-id="7d61d-101">New-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="7d61d-101">New-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="7d61d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7d61d-102">SYNOPSIS</span></span>
<span data-ttu-id="7d61d-103">Cria uma nova capacidade inserida do PowerBI.</span><span class="sxs-lookup"><span data-stu-id="7d61d-103">Creates a new PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="7d61d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7d61d-104">SYNTAX</span></span>

```
New-AzPowerBIEmbeddedCapacity [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Sku] <String> [-Administrator] <String[]> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d61d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7d61d-105">DESCRIPTION</span></span>
<span data-ttu-id="7d61d-106">O cmdlet New-AzPowerBIEmbeddedCapacity cria uma nova capacidade inserida do PowerBI</span><span class="sxs-lookup"><span data-stu-id="7d61d-106">The New-AzPowerBIEmbeddedCapacity cmdlet creates a new PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="7d61d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7d61d-107">EXAMPLES</span></span>

### <span data-ttu-id="7d61d-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7d61d-108">Example 1</span></span>
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

<span data-ttu-id="7d61d-109">Cria uma capacidade chamada testcapacity na região do Azure oeste centro dos EUA e na testRG do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7d61d-109">Creates a capacity named testcapacity in the Azure region West Central US and in resource group testRG.</span></span> <span data-ttu-id="7d61d-110">O nível de SKU para a capacidade será a1.</span><span class="sxs-lookup"><span data-stu-id="7d61d-110">The sku level for the capacity will be A1.</span></span>

## <span data-ttu-id="7d61d-111">OS</span><span class="sxs-lookup"><span data-stu-id="7d61d-111">PARAMETERS</span></span>

### <span data-ttu-id="7d61d-112">-Administrador</span><span class="sxs-lookup"><span data-stu-id="7d61d-112">-Administrator</span></span>
<span data-ttu-id="7d61d-113">Um nome separado por vírgulas para definir como administrador na capacidade</span><span class="sxs-lookup"><span data-stu-id="7d61d-113">A comma separated names to set as administrator on the capacity</span></span>

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

### <span data-ttu-id="7d61d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d61d-114">-DefaultProfile</span></span>
<span data-ttu-id="7d61d-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7d61d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d61d-116">-Local</span><span class="sxs-lookup"><span data-stu-id="7d61d-116">-Location</span></span>
<span data-ttu-id="7d61d-117">A região do Azure na qual a capacidade incorporada do PowerBI está hospedada</span><span class="sxs-lookup"><span data-stu-id="7d61d-117">The Azure region where the PowerBI Embedded Capacity is hosted</span></span>

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

### <span data-ttu-id="7d61d-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="7d61d-118">-Name</span></span>
<span data-ttu-id="7d61d-119">Nome da capacidade inserida do PowerBI</span><span class="sxs-lookup"><span data-stu-id="7d61d-119">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="7d61d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d61d-120">-ResourceGroupName</span></span>
<span data-ttu-id="7d61d-121">Nome do grupo de recursos do Azure ao qual a capacidade pertence</span><span class="sxs-lookup"><span data-stu-id="7d61d-121">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="7d61d-122">-SKU</span><span class="sxs-lookup"><span data-stu-id="7d61d-122">-Sku</span></span>
<span data-ttu-id="7d61d-123">O nome da SKU para a capacidade.</span><span class="sxs-lookup"><span data-stu-id="7d61d-123">The name of the Sku for the capacity.</span></span>

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

### <span data-ttu-id="7d61d-124">-Marca</span><span class="sxs-lookup"><span data-stu-id="7d61d-124">-Tag</span></span>
<span data-ttu-id="7d61d-125">Pares de valores chave na forma de uma tabela de hash definidas como marcas na capacidade.</span><span class="sxs-lookup"><span data-stu-id="7d61d-125">Key-value pairs in the form of a hash table set as tags on the capacity.</span></span>

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

### <span data-ttu-id="7d61d-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7d61d-126">-Confirm</span></span>
<span data-ttu-id="7d61d-127">Solicita que o usuário confirme se deseja executar a operação</span><span class="sxs-lookup"><span data-stu-id="7d61d-127">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="7d61d-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d61d-128">-WhatIf</span></span>
<span data-ttu-id="7d61d-129">Descreve as ações que a operação atual executará sem realmente executá-las</span><span class="sxs-lookup"><span data-stu-id="7d61d-129">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="7d61d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d61d-130">CommonParameters</span></span>
<span data-ttu-id="7d61d-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d61d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d61d-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d61d-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d61d-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7d61d-133">INPUTS</span></span>

### <span data-ttu-id="7d61d-134">System. String</span><span class="sxs-lookup"><span data-stu-id="7d61d-134">System.String</span></span>

### <span data-ttu-id="7d61d-135">System. String []</span><span class="sxs-lookup"><span data-stu-id="7d61d-135">System.String[]</span></span>

### <span data-ttu-id="7d61d-136">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="7d61d-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="7d61d-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7d61d-137">OUTPUTS</span></span>

### <span data-ttu-id="7d61d-138">Microsoft. Azure. Commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="7d61d-138">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="7d61d-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7d61d-139">NOTES</span></span>

## <span data-ttu-id="7d61d-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7d61d-140">RELATED LINKS</span></span>

[<span data-ttu-id="7d61d-141">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="7d61d-141">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="7d61d-142">Remove-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="7d61d-142">Remove-AzPowerBIEmbeddedCapacity</span></span>](./Remove-AzPowerBIEmbeddedCapacity.md)
