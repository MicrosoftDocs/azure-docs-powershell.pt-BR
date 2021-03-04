---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactoryv2linkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2LinkedService.md
ms.openlocfilehash: 0312b3d2a5ffa973c4ef2934ea592844850d8018
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888281"
---
# <span data-ttu-id="b0be8-101">Get-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="b0be8-101">Get-AzDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="b0be8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0be8-102">SYNOPSIS</span></span>
<span data-ttu-id="b0be8-103">Obtém informações sobre serviços vinculados na Fábrica de Dados.</span><span class="sxs-lookup"><span data-stu-id="b0be8-103">Gets information about linked services in Data Factory.</span></span>

## <span data-ttu-id="b0be8-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b0be8-104">SYNTAX</span></span>

### <span data-ttu-id="b0be8-105">ByFactoryName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="b0be8-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2LinkedService [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b0be8-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="b0be8-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2LinkedService [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b0be8-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b0be8-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2LinkedService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b0be8-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b0be8-108">DESCRIPTION</span></span>
<span data-ttu-id="b0be8-109">O Get-AzDataFactoryV2LinkedService cmdlet obtém informações sobre serviços vinculados no Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="b0be8-109">The Get-AzDataFactoryV2LinkedService cmdlet gets information about linked services in Azure Data Factory.</span></span>
<span data-ttu-id="b0be8-110">Se você especificar o nome de um serviço vinculado, esse cmdlet obterá informações sobre esse serviço vinculado.</span><span class="sxs-lookup"><span data-stu-id="b0be8-110">If you specify the name of a linked service, this cmdlet gets information about that linked service.</span></span>
<span data-ttu-id="b0be8-111">Se você não especificar um nome, este cmdlet obterá informações sobre todos os serviços vinculados no fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="b0be8-111">If you do not specify a name, this cmdlet gets information about all the linked services in the data factory.</span></span>

## <span data-ttu-id="b0be8-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b0be8-112">EXAMPLES</span></span>

### <span data-ttu-id="b0be8-113">Exemplo 1: obter informações sobre todos os serviços vinculados</span><span class="sxs-lookup"><span data-stu-id="b0be8-113">Example 1: Get information about all linked services</span></span>
```
PS C:\> Get-AzDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" | Format-List

    LinkedServiceName : LinkedServiceCuratedWikiData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService

    LinkedServiceName : LinkedServiceHDIStorage
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService

    LinkedServiceName : LinkedServiceWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService
```

<span data-ttu-id="b0be8-114">Este comando obtém informações sobre todos os serviços vinculados no fábrica de dados chamado WikiADF e, em seguida, passa os serviços vinculados para o cmdlet Format-List usando o operador de pipeline.</span><span class="sxs-lookup"><span data-stu-id="b0be8-114">This command gets information about all linked services in the data factory named WikiADF, and then passes the linked services to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="b0be8-115">Esse Windows PowerShell cmdlet formata os resultados.</span><span class="sxs-lookup"><span data-stu-id="b0be8-115">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="b0be8-116">Para obter mais informações, digite Get-Help Format-List.</span><span class="sxs-lookup"><span data-stu-id="b0be8-116">For more information, type Get-Help Format-List.</span></span>
<span data-ttu-id="b0be8-117">Você pode usar uma das seguintes maneiras:</span><span class="sxs-lookup"><span data-stu-id="b0be8-117">You can use either one of the following ways:</span></span>

### <span data-ttu-id="b0be8-118">Exemplo 2: obter informações sobre um serviço vinculado específico</span><span class="sxs-lookup"><span data-stu-id="b0be8-118">Example 2: Get information about a specific linked service</span></span>
```
PS C:\> Get-AzDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceCuratedWikiData"

    LinkedServiceName : LinkedServiceCuratedWikiData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService
```

<span data-ttu-id="b0be8-119">Este comando obtém informações sobre o serviço vinculado chamado LinkedServiceCuratedWikiData no fábrica de dados chamado WikiADF.</span><span class="sxs-lookup"><span data-stu-id="b0be8-119">This command gets information about the linked service named LinkedServiceCuratedWikiData in the data factory named WikiADF.</span></span>

### <span data-ttu-id="b0be8-120">Exemplo 3: obter informações sobre um serviço vinculado específico especificando o parâmetro DataFactory</span><span class="sxs-lookup"><span data-stu-id="b0be8-120">Example 3: Get information about a specific linked service by specifying the DataFactory parameter</span></span>
```
PS C:\>$DataFactory = Get-AzDataFactoryV2 -ResourceGroupName "ADF" -Name "ContosoFactory"PS C:\> Get-AzDataFactoryV2LinkedService -DataFactory $DataFactory | Format-Table -Property LinkedServiceName, DataFactoryName, ResourceGroupName
```

<span data-ttu-id="b0be8-121">O primeiro comando usa o cmdlet Get-AzDataFactoryV2 para obter o fábrica de dados chamado ContosoFactory e, em seguida, o armazena na variável $DataFactory.</span><span class="sxs-lookup"><span data-stu-id="b0be8-121">The first command uses the Get-AzDataFactoryV2 cmdlet to get the data factory named ContosoFactory, and then stores it in the $DataFactory variable.</span></span>
<span data-ttu-id="b0be8-122">O segundo comando obtém informações sobre o serviço vinculado para o fábrica de dados armazenado no $DataFactory e, em seguida, passa essas informações para o cmdlet Format-Table usando o operador de pipeline.</span><span class="sxs-lookup"><span data-stu-id="b0be8-122">The second command gets information about the linked service for the data factory stored in $DataFactory, and then passes that information to the Format-Table cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="b0be8-123">O Format-Table cmdlet formata a saída como um conjuntos de dados com as propriedades especificadas como colunas de conjuntos de dados.</span><span class="sxs-lookup"><span data-stu-id="b0be8-123">The Format-Table cmdlet formats the output as a dataset with the specified properties as dataset columns.</span></span>

## <span data-ttu-id="b0be8-124">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b0be8-124">PARAMETERS</span></span>

### <span data-ttu-id="b0be8-125">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="b0be8-125">-DataFactory</span></span>
<span data-ttu-id="b0be8-126">Especifica um objeto PSDataFactory.</span><span class="sxs-lookup"><span data-stu-id="b0be8-126">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="b0be8-127">Este cmdlet obtém serviços vinculados que pertencem ao fábrica de dados especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="b0be8-127">This cmdlet gets linked services that belong to the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b0be8-128">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="b0be8-128">-DataFactoryName</span></span>
<span data-ttu-id="b0be8-129">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="b0be8-129">Specifies the name of a data factory.</span></span>
<span data-ttu-id="b0be8-130">Este cmdlet obtém serviços vinculados que pertencem ao fábrica de dados especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="b0be8-130">This cmdlet gets linked services that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="b0be8-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0be8-131">-DefaultProfile</span></span>
<span data-ttu-id="b0be8-132">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="b0be8-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b0be8-133">-Name</span><span class="sxs-lookup"><span data-stu-id="b0be8-133">-Name</span></span>
<span data-ttu-id="b0be8-134">Especifica o nome do serviço vinculado sobre o qual obter informações.</span><span class="sxs-lookup"><span data-stu-id="b0be8-134">Specifies the name of the linked service about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases: LinkedServiceName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0be8-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0be8-135">-ResourceGroupName</span></span>
<span data-ttu-id="b0be8-136">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="b0be8-136">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="b0be8-137">Este cmdlet obtém serviços vinculados que pertencem ao grupo especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="b0be8-137">This cmdlet gets linked services that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="b0be8-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b0be8-138">-ResourceId</span></span>
<span data-ttu-id="b0be8-139">A ID de recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="b0be8-139">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0be8-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0be8-140">CommonParameters</span></span>
<span data-ttu-id="b0be8-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0be8-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0be8-142">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0be8-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0be8-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b0be8-143">INPUTS</span></span>

### <span data-ttu-id="b0be8-144">System.String</span><span class="sxs-lookup"><span data-stu-id="b0be8-144">System.String</span></span>

### <span data-ttu-id="b0be8-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="b0be8-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="b0be8-146">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b0be8-146">OUTPUTS</span></span>

### <span data-ttu-id="b0be8-147">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="b0be8-147">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>

## <span data-ttu-id="b0be8-148">NOTES</span><span class="sxs-lookup"><span data-stu-id="b0be8-148">NOTES</span></span>
<span data-ttu-id="b0be8-149">Palavras-chave: azure, azurerm, arm, resource, management, manager, data, factories</span><span class="sxs-lookup"><span data-stu-id="b0be8-149">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="b0be8-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b0be8-150">RELATED LINKS</span></span>

[<span data-ttu-id="b0be8-151">Set-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="b0be8-151">Set-AzDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="b0be8-152">Remove-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="b0be8-152">Remove-AzDataFactoryV2LinkedService</span></span>]()
