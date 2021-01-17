---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2linkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2LinkedService.md
ms.openlocfilehash: ac3a45f9e150d65829a222e75e7072c6a2bdcd1e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98429907"
---
# <span data-ttu-id="87996-101">Get-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="87996-101">Get-AzDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="87996-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="87996-102">SYNOPSIS</span></span>
<span data-ttu-id="87996-103">Obtém informações sobre os serviços vinculados na fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="87996-103">Gets information about linked services in Data Factory.</span></span>

## <span data-ttu-id="87996-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="87996-104">SYNTAX</span></span>

### <span data-ttu-id="87996-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="87996-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2LinkedService [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="87996-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="87996-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2LinkedService [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="87996-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="87996-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2LinkedService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="87996-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="87996-108">DESCRIPTION</span></span>
<span data-ttu-id="87996-109">O cmdlet Get-AzDataFactoryV2LinkedService Obtém informações sobre serviços vinculados no Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="87996-109">The Get-AzDataFactoryV2LinkedService cmdlet gets information about linked services in Azure Data Factory.</span></span>
<span data-ttu-id="87996-110">Se você especificar o nome de um serviço vinculado, esse cmdlet obterá informações sobre esse serviço vinculado.</span><span class="sxs-lookup"><span data-stu-id="87996-110">If you specify the name of a linked service, this cmdlet gets information about that linked service.</span></span>
<span data-ttu-id="87996-111">Se você não especificar um nome, esse cmdlet obterá informações sobre todos os serviços vinculados na fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="87996-111">If you do not specify a name, this cmdlet gets information about all the linked services in the data factory.</span></span>

## <span data-ttu-id="87996-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="87996-112">EXAMPLES</span></span>

### <span data-ttu-id="87996-113">Exemplo 1: obter informações sobre todos os serviços vinculados</span><span class="sxs-lookup"><span data-stu-id="87996-113">Example 1: Get information about all linked services</span></span>
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

<span data-ttu-id="87996-114">Esse comando obtém informações sobre todos os serviços vinculados no data Factory chamado WikiADF e, em seguida, passa os serviços vinculados ao cmdlet Format-List usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="87996-114">This command gets information about all linked services in the data factory named WikiADF, and then passes the linked services to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="87996-115">Esse cmdlet do Windows PowerShell formata os resultados.</span><span class="sxs-lookup"><span data-stu-id="87996-115">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="87996-116">Para obter mais informações, digite Get-Help formato-List.</span><span class="sxs-lookup"><span data-stu-id="87996-116">For more information, type Get-Help Format-List.</span></span>
<span data-ttu-id="87996-117">Você pode usar qualquer uma das seguintes maneiras:</span><span class="sxs-lookup"><span data-stu-id="87996-117">You can use either one of the following ways:</span></span>

### <span data-ttu-id="87996-118">Exemplo 2: obter informações sobre um serviço vinculado específico</span><span class="sxs-lookup"><span data-stu-id="87996-118">Example 2: Get information about a specific linked service</span></span>
```
PS C:\> Get-AzDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceCuratedWikiData"

    LinkedServiceName : LinkedServiceCuratedWikiData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService
```

<span data-ttu-id="87996-119">Esse comando obtém informações sobre o serviço vinculado chamado LinkedServiceCuratedWikiData no data Factory chamado WikiADF.</span><span class="sxs-lookup"><span data-stu-id="87996-119">This command gets information about the linked service named LinkedServiceCuratedWikiData in the data factory named WikiADF.</span></span>

### <span data-ttu-id="87996-120">Exemplo 3: obter informações sobre um serviço específico vinculado especificando o parâmetro datafactory</span><span class="sxs-lookup"><span data-stu-id="87996-120">Example 3: Get information about a specific linked service by specifying the DataFactory parameter</span></span>
```
PS C:\>$DataFactory = Get-AzDataFactoryV2 -ResourceGroupName "ADF" -Name "ContosoFactory"PS C:\> Get-AzDataFactoryV2LinkedService -DataFactory $DataFactory | Format-Table -Property LinkedServiceName, DataFactoryName, ResourceGroupName
```

<span data-ttu-id="87996-121">O primeiro comando usa o cmdlet Get-AzDataFactoryV2 para obter a fábrica de dados chamada ContosoFactory e, em seguida, armazena-o na variável $DataFactory.</span><span class="sxs-lookup"><span data-stu-id="87996-121">The first command uses the Get-AzDataFactoryV2 cmdlet to get the data factory named ContosoFactory, and then stores it in the $DataFactory variable.</span></span>
<span data-ttu-id="87996-122">O segundo comando obtém informações sobre o serviço vinculado para o realocador de dados armazenado no $DataFactory e, em seguida, passa essas informações para o cmdlet Format-Table usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="87996-122">The second command gets information about the linked service for the data factory stored in $DataFactory, and then passes that information to the Format-Table cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="87996-123">O cmdlet Format-Table formata a saída como um DataSet com as propriedades especificadas como colunas do DataSet.</span><span class="sxs-lookup"><span data-stu-id="87996-123">The Format-Table cmdlet formats the output as a dataset with the specified properties as dataset columns.</span></span>

## <span data-ttu-id="87996-124">OS</span><span class="sxs-lookup"><span data-stu-id="87996-124">PARAMETERS</span></span>

### <span data-ttu-id="87996-125">-Datafactory</span><span class="sxs-lookup"><span data-stu-id="87996-125">-DataFactory</span></span>
<span data-ttu-id="87996-126">Especifica um objeto PSDataFactory.</span><span class="sxs-lookup"><span data-stu-id="87996-126">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="87996-127">Esse cmdlet obtém serviços vinculados que pertencem à fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="87996-127">This cmdlet gets linked services that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="87996-128">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="87996-128">-DataFactoryName</span></span>
<span data-ttu-id="87996-129">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="87996-129">Specifies the name of a data factory.</span></span>
<span data-ttu-id="87996-130">Esse cmdlet obtém serviços vinculados que pertencem à fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="87996-130">This cmdlet gets linked services that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="87996-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87996-131">-DefaultProfile</span></span>
<span data-ttu-id="87996-132">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="87996-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="87996-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="87996-133">-Name</span></span>
<span data-ttu-id="87996-134">Especifica o nome do serviço vinculado sobre o qual obter informações.</span><span class="sxs-lookup"><span data-stu-id="87996-134">Specifies the name of the linked service about which to get information.</span></span>

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

### <span data-ttu-id="87996-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87996-135">-ResourceGroupName</span></span>
<span data-ttu-id="87996-136">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="87996-136">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="87996-137">Esse cmdlet obtém serviços vinculados que pertencem ao grupo especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="87996-137">This cmdlet gets linked services that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="87996-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="87996-138">-ResourceId</span></span>
<span data-ttu-id="87996-139">A ID do recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="87996-139">The Azure resource ID.</span></span>

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

### <span data-ttu-id="87996-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87996-140">CommonParameters</span></span>
<span data-ttu-id="87996-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87996-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87996-142">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87996-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87996-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="87996-143">INPUTS</span></span>

### <span data-ttu-id="87996-144">System. String</span><span class="sxs-lookup"><span data-stu-id="87996-144">System.String</span></span>

### <span data-ttu-id="87996-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="87996-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="87996-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="87996-146">OUTPUTS</span></span>

### <span data-ttu-id="87996-147">Microsoft. Azure. Commands. DataFactoryV2. Models. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="87996-147">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>

## <span data-ttu-id="87996-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="87996-148">NOTES</span></span>
<span data-ttu-id="87996-149">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas</span><span class="sxs-lookup"><span data-stu-id="87996-149">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="87996-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="87996-150">RELATED LINKS</span></span>

[<span data-ttu-id="87996-151">Set-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="87996-151">Set-AzDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="87996-152">Remove-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="87996-152">Remove-AzDataFactoryV2LinkedService</span></span>]()
