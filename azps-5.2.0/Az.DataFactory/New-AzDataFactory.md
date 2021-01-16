---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 7B18FA1B-F616-4479-B2F0-620FC0E3E962
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactory.md
ms.openlocfilehash: 450a833656f6508f70ebd97f5387075c1711c5f9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98264463"
---
# <span data-ttu-id="093f3-101">New-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="093f3-101">New-AzDataFactory</span></span>

## <span data-ttu-id="093f3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="093f3-102">SYNOPSIS</span></span>
<span data-ttu-id="093f3-103">Cria uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="093f3-103">Creates a data factory.</span></span>

## <span data-ttu-id="093f3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="093f3-104">SYNTAX</span></span>

```
New-AzDataFactory [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="093f3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="093f3-105">DESCRIPTION</span></span>
<span data-ttu-id="093f3-106">O cmdlet **New-AzDataFactory** cria uma fábrica de dados com o nome e o local do grupo de recursos especificados.</span><span class="sxs-lookup"><span data-stu-id="093f3-106">The **New-AzDataFactory** cmdlet creates a data factory with the specified resource group name and location.</span></span>
<span data-ttu-id="093f3-107">Execute estas operações na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="093f3-107">Perform these operations in the following order:</span></span> 
- <span data-ttu-id="093f3-108">Criar uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="093f3-108">Create a data factory.</span></span> 
- <span data-ttu-id="093f3-109">Criar serviços vinculados.</span><span class="sxs-lookup"><span data-stu-id="093f3-109">Create linked services.</span></span> 
- <span data-ttu-id="093f3-110">Criar conjuntos de valores de valores.</span><span class="sxs-lookup"><span data-stu-id="093f3-110">Create datasets.</span></span> 
- <span data-ttu-id="093f3-111">Crie um pipeline.</span><span class="sxs-lookup"><span data-stu-id="093f3-111">Create a pipeline.</span></span>

## <span data-ttu-id="093f3-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="093f3-112">EXAMPLES</span></span>

### <span data-ttu-id="093f3-113">Exemplo 1: criar uma fábrica de dados</span><span class="sxs-lookup"><span data-stu-id="093f3-113">Example 1: Create a data factory</span></span>
```
PS C:\>New-AzDataFactory -ResourceGroupName "ADF" -Name "WikiADF" -Location "WestUS"
DataFactoryName   : WikiADF
ResourceGroupName : ADF
Location          : WestUS
Tags              : {}
Properties        : Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryConfiguration
```

<span data-ttu-id="093f3-114">Esse comando cria um data Factory chamado WikiADF no grupo de recursos chamado ADF no local da Westus.</span><span class="sxs-lookup"><span data-stu-id="093f3-114">This command creates a data factory named WikiADF in the resource group named ADF in the WestUS location.</span></span>

## <span data-ttu-id="093f3-115">OS</span><span class="sxs-lookup"><span data-stu-id="093f3-115">PARAMETERS</span></span>

### <span data-ttu-id="093f3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="093f3-116">-DefaultProfile</span></span>
<span data-ttu-id="093f3-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="093f3-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="093f3-118">-Force</span><span class="sxs-lookup"><span data-stu-id="093f3-118">-Force</span></span>
<span data-ttu-id="093f3-119">Indica que esse cmdlet substitui uma fábrica de dados existente sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="093f3-119">Indicates that this cmdlet replaces an existing data factory without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="093f3-120">-Local</span><span class="sxs-lookup"><span data-stu-id="093f3-120">-Location</span></span>
<span data-ttu-id="093f3-121">Especifica o local para a fábrica de dados, como Westus ou Eastus.</span><span class="sxs-lookup"><span data-stu-id="093f3-121">Specifies the location for the data factory, such as WestUS or EastUS.</span></span>
<span data-ttu-id="093f3-122">Somente o Oesteus tem suporte no momento.</span><span class="sxs-lookup"><span data-stu-id="093f3-122">Only WestUS is currently supported.</span></span>

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

### <span data-ttu-id="093f3-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="093f3-123">-Name</span></span>
<span data-ttu-id="093f3-124">Especifica o nome do alocador de dados a ser criado.</span><span class="sxs-lookup"><span data-stu-id="093f3-124">Specifies the name of the data factory to create.</span></span>

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

### <span data-ttu-id="093f3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="093f3-125">-ResourceGroupName</span></span>
<span data-ttu-id="093f3-126">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="093f3-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="093f3-127">Esse cmdlet cria uma fábrica de dados que pertence ao grupo especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="093f3-127">This cmdlet creates a data factory that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="093f3-128">-Marca</span><span class="sxs-lookup"><span data-stu-id="093f3-128">-Tag</span></span>
<span data-ttu-id="093f3-129">As marcas do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="093f3-129">The tags of the data factory.</span></span>

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

### <span data-ttu-id="093f3-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="093f3-130">-Confirm</span></span>
<span data-ttu-id="093f3-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="093f3-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="093f3-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="093f3-132">-WhatIf</span></span>
<span data-ttu-id="093f3-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="093f3-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="093f3-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="093f3-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="093f3-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="093f3-135">CommonParameters</span></span>
<span data-ttu-id="093f3-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="093f3-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="093f3-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="093f3-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="093f3-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="093f3-138">INPUTS</span></span>

### <span data-ttu-id="093f3-139">System. String</span><span class="sxs-lookup"><span data-stu-id="093f3-139">System.String</span></span>

### <span data-ttu-id="093f3-140">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="093f3-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="093f3-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="093f3-141">OUTPUTS</span></span>

### <span data-ttu-id="093f3-142">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="093f3-142">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="093f3-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="093f3-143">NOTES</span></span>
* <span data-ttu-id="093f3-144">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas</span><span class="sxs-lookup"><span data-stu-id="093f3-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="093f3-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="093f3-145">RELATED LINKS</span></span>

[<span data-ttu-id="093f3-146">Get-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="093f3-146">Get-AzDataFactory</span></span>](./Get-AzDataFactory.md)

[<span data-ttu-id="093f3-147">Remove-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="093f3-147">Remove-AzDataFactory</span></span>](./Remove-AzDataFactory.md)


