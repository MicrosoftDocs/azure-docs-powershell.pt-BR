---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 7B18FA1B-F616-4479-B2F0-620FC0E3E962
online version: https://docs.microsoft.com/powershell/module/az.datafactory/new-azdatafactory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactory.md
ms.openlocfilehash: c13fdf46dff4ba0b62a8009bad7c4790507b2561
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888262"
---
# <span data-ttu-id="b5a60-101">New-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="b5a60-101">New-AzDataFactory</span></span>

## <span data-ttu-id="b5a60-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5a60-102">SYNOPSIS</span></span>
<span data-ttu-id="b5a60-103">Cria uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="b5a60-103">Creates a data factory.</span></span>

## <span data-ttu-id="b5a60-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b5a60-104">SYNTAX</span></span>

```
New-AzDataFactory [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b5a60-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b5a60-105">DESCRIPTION</span></span>
<span data-ttu-id="b5a60-106">O cmdlet **New-AzDataFactory** cria um fábrica de dados com o nome e o local do grupo de recursos especificados.</span><span class="sxs-lookup"><span data-stu-id="b5a60-106">The **New-AzDataFactory** cmdlet creates a data factory with the specified resource group name and location.</span></span>
<span data-ttu-id="b5a60-107">Execute essas operações na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="b5a60-107">Perform these operations in the following order:</span></span> 
- <span data-ttu-id="b5a60-108">Criar uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="b5a60-108">Create a data factory.</span></span> 
- <span data-ttu-id="b5a60-109">Criar serviços vinculados.</span><span class="sxs-lookup"><span data-stu-id="b5a60-109">Create linked services.</span></span> 
- <span data-ttu-id="b5a60-110">Criar conjuntos de dados.</span><span class="sxs-lookup"><span data-stu-id="b5a60-110">Create datasets.</span></span> 
- <span data-ttu-id="b5a60-111">Criar um pipeline.</span><span class="sxs-lookup"><span data-stu-id="b5a60-111">Create a pipeline.</span></span>

## <span data-ttu-id="b5a60-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b5a60-112">EXAMPLES</span></span>

### <span data-ttu-id="b5a60-113">Exemplo 1: Criar um fábrica de dados</span><span class="sxs-lookup"><span data-stu-id="b5a60-113">Example 1: Create a data factory</span></span>
```
PS C:\>New-AzDataFactory -ResourceGroupName "ADF" -Name "WikiADF" -Location "WestUS"
DataFactoryName   : WikiADF
ResourceGroupName : ADF
Location          : WestUS
Tags              : {}
Properties        : Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryConfiguration
```

<span data-ttu-id="b5a60-114">Este comando cria um fábrica de dados chamado WikiADF no grupo de recursos chamado ADF no local do WestUS.</span><span class="sxs-lookup"><span data-stu-id="b5a60-114">This command creates a data factory named WikiADF in the resource group named ADF in the WestUS location.</span></span>

## <span data-ttu-id="b5a60-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b5a60-115">PARAMETERS</span></span>

### <span data-ttu-id="b5a60-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5a60-116">-DefaultProfile</span></span>
<span data-ttu-id="b5a60-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="b5a60-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b5a60-118">-Force</span><span class="sxs-lookup"><span data-stu-id="b5a60-118">-Force</span></span>
<span data-ttu-id="b5a60-119">Indica que esse cmdlet substitui um fábrica de dados existente sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="b5a60-119">Indicates that this cmdlet replaces an existing data factory without prompting you for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5a60-120">-Location</span><span class="sxs-lookup"><span data-stu-id="b5a60-120">-Location</span></span>
<span data-ttu-id="b5a60-121">Especifica o local do fábrica de dados, como WestUS ou EastUS.</span><span class="sxs-lookup"><span data-stu-id="b5a60-121">Specifies the location for the data factory, such as WestUS or EastUS.</span></span>
<span data-ttu-id="b5a60-122">No momento, somente o WestUS é suportado.</span><span class="sxs-lookup"><span data-stu-id="b5a60-122">Only WestUS is currently supported.</span></span>

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

### <span data-ttu-id="b5a60-123">-Name</span><span class="sxs-lookup"><span data-stu-id="b5a60-123">-Name</span></span>
<span data-ttu-id="b5a60-124">Especifica o nome do fábrica de dados a ser criado.</span><span class="sxs-lookup"><span data-stu-id="b5a60-124">Specifies the name of the data factory to create.</span></span>

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

### <span data-ttu-id="b5a60-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5a60-125">-ResourceGroupName</span></span>
<span data-ttu-id="b5a60-126">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="b5a60-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="b5a60-127">Este cmdlet cria um fábrica de dados que pertence ao grupo especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="b5a60-127">This cmdlet creates a data factory that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="b5a60-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="b5a60-128">-Tag</span></span>
<span data-ttu-id="b5a60-129">As marcas do fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="b5a60-129">The tags of the data factory.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5a60-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b5a60-130">-Confirm</span></span>
<span data-ttu-id="b5a60-131">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5a60-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5a60-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5a60-132">-WhatIf</span></span>
<span data-ttu-id="b5a60-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b5a60-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5a60-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b5a60-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5a60-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5a60-135">CommonParameters</span></span>
<span data-ttu-id="b5a60-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5a60-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5a60-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5a60-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5a60-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b5a60-138">INPUTS</span></span>

### <span data-ttu-id="b5a60-139">System.String</span><span class="sxs-lookup"><span data-stu-id="b5a60-139">System.String</span></span>

### <span data-ttu-id="b5a60-140">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="b5a60-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="b5a60-141">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b5a60-141">OUTPUTS</span></span>

### <span data-ttu-id="b5a60-142">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="b5a60-142">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="b5a60-143">NOTES</span><span class="sxs-lookup"><span data-stu-id="b5a60-143">NOTES</span></span>
* <span data-ttu-id="b5a60-144">Palavras-chave: azure, azurerm, arm, resource, management, manager, data, factories</span><span class="sxs-lookup"><span data-stu-id="b5a60-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="b5a60-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b5a60-145">RELATED LINKS</span></span>

[<span data-ttu-id="b5a60-146">Get-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="b5a60-146">Get-AzDataFactory</span></span>](./Get-AzDataFactory.md)

[<span data-ttu-id="b5a60-147">Remove-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="b5a60-147">Remove-AzDataFactory</span></span>](./Remove-AzDataFactory.md)


