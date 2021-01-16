---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: DFA41A2B-7C8A-42CB-B0B6-5E6FF853EFEE
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactorylinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryLinkedService.md
ms.openlocfilehash: 5f59dfeeb024b4a81554a700bdcebc9d7f39e80a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433927"
---
# <span data-ttu-id="86a33-101">Get-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="86a33-101">Get-AzDataFactoryLinkedService</span></span>

## <span data-ttu-id="86a33-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="86a33-102">SYNOPSIS</span></span>
<span data-ttu-id="86a33-103">Obtém informações sobre serviços vinculados no Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="86a33-103">Gets information about linked services in Azure Data Factory.</span></span>

## <span data-ttu-id="86a33-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="86a33-104">SYNTAX</span></span>

### <span data-ttu-id="86a33-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="86a33-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryLinkedService [-DataFactoryName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="86a33-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="86a33-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryLinkedService [-DataFactory] <PSDataFactory> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="86a33-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="86a33-107">DESCRIPTION</span></span>
<span data-ttu-id="86a33-108">O cmdlet **Get-AzDataFactoryLinkedService** Obtém informações sobre serviços vinculados no Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="86a33-108">The **Get-AzDataFactoryLinkedService** cmdlet gets information about linked services in Azure Data Factory.</span></span>
<span data-ttu-id="86a33-109">Se você especificar o nome de um serviço vinculado, esse cmdlet obterá informações sobre esse serviço vinculado.</span><span class="sxs-lookup"><span data-stu-id="86a33-109">If you specify the name of a linked service, this cmdlet gets information about that linked service.</span></span>
<span data-ttu-id="86a33-110">Se você não especificar um nome, esse cmdlet obterá informações sobre todos os serviços vinculados na fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="86a33-110">If you do not specify a name, this cmdlet gets information about all the linked services in the data factory.</span></span>

## <span data-ttu-id="86a33-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="86a33-111">EXAMPLES</span></span>

### <span data-ttu-id="86a33-112">Exemplo 1: obter informações sobre todos os serviços vinculados</span><span class="sxs-lookup"><span data-stu-id="86a33-112">Example 1: Get information about all linked services</span></span>
```
PS C:\>Get-AzDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" | Format-List
```

<span data-ttu-id="86a33-113">Esse comando obtém informações sobre todos os serviços vinculados no data Factory chamado WikiADF e, em seguida, passa os serviços vinculados ao cmdlet Format-List usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="86a33-113">This command gets information about all linked services in the data factory named WikiADF, and then passes the linked services to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="86a33-114">Esse cmdlet formata os resultados.</span><span class="sxs-lookup"><span data-stu-id="86a33-114">That cmdlet formats the results.</span></span>
<span data-ttu-id="86a33-115">Para obter mais informações, digite `Get-Help Format-List` .</span><span class="sxs-lookup"><span data-stu-id="86a33-115">For more information, type `Get-Help Format-List`.</span></span>

### <span data-ttu-id="86a33-116">Exemplo 2: obter informações sobre um serviço vinculado específico</span><span class="sxs-lookup"><span data-stu-id="86a33-116">Example 2: Get information about a specific linked service</span></span>
```
PS C:\>Get-AzDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "HDILinkedService"
LinkedServiceName   ResourceGroupName     DataFactoryName              Properties
-----------------   -----------------     ---------------              ----------
HDILinkedService    ADF                   WikiADF                      Microsoft.DataFactories.HDInsightBYOCAsset
```

<span data-ttu-id="86a33-117">Esse comando obtém informações sobre o serviço vinculado chamado HDILinkedService no data Factory chamado WikiADF.</span><span class="sxs-lookup"><span data-stu-id="86a33-117">This command gets information about the linked service named HDILinkedService in the data factory named WikiADF.</span></span>

### <span data-ttu-id="86a33-118">Exemplo 3: obter informações sobre um serviço específico vinculado especificando o parâmetro datafactory</span><span class="sxs-lookup"><span data-stu-id="86a33-118">Example 3: Get information about a specific linked service by specifying the DataFactory parameter</span></span>
```
PS C:\>$DataFactory = Get-AzDataFactory -ResourceGroupName "ADF" -Name "ContosoFactory"
PS C:\> Get-AzDataFactoryLinkedService -DataFactory $DataFactory | Format-Table -Property LinkedServiceName, DataFactoryName, ResourceGroupName
```

<span data-ttu-id="86a33-119">O primeiro comando usa o cmdlet Get-AzDataFactory para obter a fábrica de dados chamada ContosoFactory e, em seguida, armazena-o na variável $DataFactory.</span><span class="sxs-lookup"><span data-stu-id="86a33-119">The first command uses the Get-AzDataFactory cmdlet to get the data factory named ContosoFactory, and then stores it in the $DataFactory variable.</span></span>
<span data-ttu-id="86a33-120">O segundo comando obtém informações sobre o serviço vinculado para o realocador de dados armazenado no $DataFactory e, em seguida, passa essas informações para o cmdlet Format-Table usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="86a33-120">The second command gets information about the linked service for the data factory stored in $DataFactory, and then passes that information to the Format-Table cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="86a33-121">**Format-Table** formata a saída como um DataSet com as propriedades especificadas como colunas do DataSet.</span><span class="sxs-lookup"><span data-stu-id="86a33-121">**Format-Table** formats the output as a dataset with the specified properties as dataset columns.</span></span>

## <span data-ttu-id="86a33-122">OS</span><span class="sxs-lookup"><span data-stu-id="86a33-122">PARAMETERS</span></span>

### <span data-ttu-id="86a33-123">-Datafactory</span><span class="sxs-lookup"><span data-stu-id="86a33-123">-DataFactory</span></span>
<span data-ttu-id="86a33-124">Especifica um objeto **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="86a33-124">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="86a33-125">Esse cmdlet obtém serviços vinculados que pertencem à fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="86a33-125">This cmdlet gets linked services that belong to the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86a33-126">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="86a33-126">-DataFactoryName</span></span>
<span data-ttu-id="86a33-127">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="86a33-127">Specifies the name of a data factory.</span></span>
<span data-ttu-id="86a33-128">Esse cmdlet obtém serviços vinculados que pertencem à fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="86a33-128">This cmdlet gets linked services that belong to the data factory that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86a33-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86a33-129">-DefaultProfile</span></span>
<span data-ttu-id="86a33-130">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="86a33-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="86a33-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="86a33-131">-Name</span></span>
<span data-ttu-id="86a33-132">Especifica o nome do serviço vinculado sobre o qual obter informações.</span><span class="sxs-lookup"><span data-stu-id="86a33-132">Specifies the name of the linked service about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86a33-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86a33-133">-ResourceGroupName</span></span>
<span data-ttu-id="86a33-134">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="86a33-134">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="86a33-135">Esse cmdlet obtém serviços vinculados que pertencem ao grupo especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="86a33-135">This cmdlet gets linked services that belong to the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86a33-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86a33-136">CommonParameters</span></span>
<span data-ttu-id="86a33-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86a33-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86a33-138">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86a33-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86a33-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="86a33-139">INPUTS</span></span>

### <span data-ttu-id="86a33-140">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="86a33-140">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="86a33-141">System. String</span><span class="sxs-lookup"><span data-stu-id="86a33-141">System.String</span></span>

## <span data-ttu-id="86a33-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="86a33-142">OUTPUTS</span></span>

### <span data-ttu-id="86a33-143">Microsoft. Azure. Commands. datafactorings. Models. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="86a33-143">Microsoft.Azure.Commands.DataFactories.Models.PSLinkedService</span></span>

## <span data-ttu-id="86a33-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="86a33-144">NOTES</span></span>
* <span data-ttu-id="86a33-145">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas</span><span class="sxs-lookup"><span data-stu-id="86a33-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="86a33-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="86a33-146">RELATED LINKS</span></span>

[<span data-ttu-id="86a33-147">New-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="86a33-147">New-AzDataFactoryLinkedService</span></span>](./New-AzDataFactoryLinkedService.md)

[<span data-ttu-id="86a33-148">Remove-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="86a33-148">Remove-AzDataFactoryLinkedService</span></span>](./Remove-AzDataFactoryLinkedService.md)


