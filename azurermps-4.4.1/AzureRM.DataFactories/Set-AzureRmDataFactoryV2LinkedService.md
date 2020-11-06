---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2LinkedService.md
ms.openlocfilehash: 5e0ee389a5d2d126cfbccc2a91b1644d81a5fedf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610816"
---
# <span data-ttu-id="c76c8-101">Set-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="c76c8-101">Set-AzureRmDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="c76c8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c76c8-102">SYNOPSIS</span></span>
<span data-ttu-id="c76c8-103">Vincula um repositório de dados ou um serviço na nuvem ao data Factory.</span><span class="sxs-lookup"><span data-stu-id="c76c8-103">Links a data store or a cloud service to Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c76c8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c76c8-104">SYNTAX</span></span>

### <span data-ttu-id="c76c8-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="c76c8-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactoryV2LinkedService [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c76c8-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c76c8-106">ByResourceId</span></span>
```
Set-AzureRmDataFactoryV2LinkedService [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c76c8-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c76c8-107">DESCRIPTION</span></span>
<span data-ttu-id="c76c8-108">O cmdlet Set-AzureRmDataFactoryV2LinkedService vincula um repositório de dados ou um serviço na nuvem ao Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="c76c8-108">The Set-AzureRmDataFactoryV2LinkedService cmdlet links a data store or a cloud service to Azure Data Factory.</span></span>
<span data-ttu-id="c76c8-109">Se você especificar um nome para um serviço vinculado que já existe, esse cmdlet solicitará confirmação antes de substituir o serviço vinculado.</span><span class="sxs-lookup"><span data-stu-id="c76c8-109">If you specify a name for a linked service that already exists, this cmdlet prompts you for confirmation before it replaces the linked service.</span></span>
<span data-ttu-id="c76c8-110">Se você especificar o parâmetro Force, o cmdlet substituirá o serviço vinculado existente sem confirmação.</span><span class="sxs-lookup"><span data-stu-id="c76c8-110">If you specify the Force parameter, the cmdlet replaces the existing linked service without confirmation.</span></span>

<span data-ttu-id="c76c8-111">Execute estas operações na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="c76c8-111">Perform these operations in the following order:</span></span>

        -- Create a data factory.
        -- Create linked services.
        -- Create datasets.
        -- Create a pipeline.

## <span data-ttu-id="c76c8-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c76c8-112">EXAMPLES</span></span>

### <span data-ttu-id="c76c8-113">Exemplo 1: criar um serviço vinculado</span><span class="sxs-lookup"><span data-stu-id="c76c8-113">Example 1: Create a linked service</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceCuratedWikiData" -File "C:\\samples\\WikiSample\\LinkedServiceCuratedWikiData.json" | Format-List

    LinkedServiceName : LinkedServiceCuratedWikiData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService
```

<span data-ttu-id="c76c8-114">Esse comando cria um serviço vinculado chamado LinkedServiceCuratedWikiData na fábrica de dados chamado WikiADF.</span><span class="sxs-lookup"><span data-stu-id="c76c8-114">This command creates a linked service named LinkedServiceCuratedWikiData in the data factory named WikiADF.</span></span>
<span data-ttu-id="c76c8-115">Esse serviço vinculado vincula um repositório de blob do Azure especificado no arquivo ao data Factory chamado WikiADF.</span><span class="sxs-lookup"><span data-stu-id="c76c8-115">This linked service links an Azure blob store specified in the file to the data factory named WikiADF.</span></span>
<span data-ttu-id="c76c8-116">O comando passa o resultado para o cmdlet Format-List usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="c76c8-116">The command passes the result to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="c76c8-117">Esse cmdlet do Windows PowerShell formata os resultados.</span><span class="sxs-lookup"><span data-stu-id="c76c8-117">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="c76c8-118">Para obter mais informações, digite Get-Help formato-List.</span><span class="sxs-lookup"><span data-stu-id="c76c8-118">For more information, type Get-Help Format-List.</span></span>

## <span data-ttu-id="c76c8-119">OS</span><span class="sxs-lookup"><span data-stu-id="c76c8-119">PARAMETERS</span></span>

### <span data-ttu-id="c76c8-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c76c8-120">-Confirm</span></span>
<span data-ttu-id="c76c8-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c76c8-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c76c8-122">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="c76c8-122">-DataFactoryName</span></span>
<span data-ttu-id="c76c8-123">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="c76c8-123">Specifies the name of a data factory.</span></span>
<span data-ttu-id="c76c8-124">Esse cmdlet cria um serviço vinculado para a fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="c76c8-124">This cmdlet creates a linked service for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="c76c8-125">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="c76c8-125">-DefinitionFile</span></span>
<span data-ttu-id="c76c8-126">O caminho do arquivo JSON.</span><span class="sxs-lookup"><span data-stu-id="c76c8-126">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c76c8-127">-Force</span><span class="sxs-lookup"><span data-stu-id="c76c8-127">-Force</span></span>
<span data-ttu-id="c76c8-128">Executa o cmdlet sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="c76c8-128">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="c76c8-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="c76c8-129">-Name</span></span>
<span data-ttu-id="c76c8-130">Especifica o nome do serviço vinculado a ser criado.</span><span class="sxs-lookup"><span data-stu-id="c76c8-130">Specifies the name of the linked service to create.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: LinkedServiceName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c76c8-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c76c8-131">-ResourceGroupName</span></span>
<span data-ttu-id="c76c8-132">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="c76c8-132">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="c76c8-133">Esse cmdlet cria um serviço vinculado para o grupo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="c76c8-133">This cmdlet creates a linked service for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="c76c8-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c76c8-134">-ResourceId</span></span>
<span data-ttu-id="c76c8-135">A ID do recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="c76c8-135">The Azure resource ID.</span></span>

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

### <span data-ttu-id="c76c8-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c76c8-136">-WhatIf</span></span>
<span data-ttu-id="c76c8-137">Mostra o que acontece se o cmdlet for executado, mas não executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c76c8-137">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="c76c8-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c76c8-138">-DefaultProfile</span></span>
<span data-ttu-id="c76c8-139">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c76c8-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c76c8-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c76c8-140">CommonParameters</span></span>
<span data-ttu-id="c76c8-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c76c8-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c76c8-142">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c76c8-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c76c8-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c76c8-143">INPUTS</span></span>

### <span data-ttu-id="c76c8-144">System. String</span><span class="sxs-lookup"><span data-stu-id="c76c8-144">System.String</span></span>

## <span data-ttu-id="c76c8-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c76c8-145">OUTPUTS</span></span>

### <span data-ttu-id="c76c8-146">Microsoft. Azure. Commands. DataFactoryV2. Models. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="c76c8-146">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>

## <span data-ttu-id="c76c8-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c76c8-147">NOTES</span></span>
<span data-ttu-id="c76c8-148">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas</span><span class="sxs-lookup"><span data-stu-id="c76c8-148">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="c76c8-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c76c8-149">RELATED LINKS</span></span>

[<span data-ttu-id="c76c8-150">Get-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="c76c8-150">Get-AzureRmDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="c76c8-151">Remove-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="c76c8-151">Remove-AzureRmDataFactoryV2LinkedService</span></span>]()
