---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2Pipeline.md
ms.openlocfilehash: 510f0f5b943a1a0abab1bc97ac5e70fa6f450898
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428245"
---
# <span data-ttu-id="557e9-101">Set-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="557e9-101">Set-AzureRmDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="557e9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="557e9-102">SYNOPSIS</span></span>
<span data-ttu-id="557e9-103">Cria um pipeline na fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="557e9-103">Creates a pipeline in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="557e9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="557e9-104">SYNTAX</span></span>

### <span data-ttu-id="557e9-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="557e9-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactoryV2Pipeline [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="557e9-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="557e9-106">ByResourceId</span></span>
```
Set-AzureRmDataFactoryV2Pipeline [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="557e9-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="557e9-107">DESCRIPTION</span></span>
<span data-ttu-id="557e9-108">O cmdlet Set-AzureRmDataFactoryV2Pipeline cria um pipeline no Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="557e9-108">The Set-AzureRmDataFactoryV2Pipeline cmdlet creates a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="557e9-109">Se você especificar um nome para um pipeline já existente, o cmdlet solicitará confirmação antes de substituir o pipeline.</span><span class="sxs-lookup"><span data-stu-id="557e9-109">If you specify a name for a pipeline that already exists, the cmdlet prompts you for confirmation before it replaces the pipeline.</span></span>
<span data-ttu-id="557e9-110">Se você especificar o parâmetro Force, o cmdlet substituirá o pipeline existente sem confirmação.</span><span class="sxs-lookup"><span data-stu-id="557e9-110">If you specify the Force parameter, the cmdlet replaces the existing pipeline without confirmation.</span></span>

<span data-ttu-id="557e9-111">Execute estas operações na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="557e9-111">Perform these operations in the following order:</span></span>

        -- Create a data factory.
        -- Create linked services.
        -- Create datasets.
        -- Create a pipeline.

<span data-ttu-id="557e9-112">Se um pipeline com o mesmo nome já existir na fábrica de dados, esse cmdlet solicitará que você confirme se deseja substituir o pipeline existente pelo novo pipeline.</span><span class="sxs-lookup"><span data-stu-id="557e9-112">If a pipeline with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing pipeline with the new pipeline.</span></span>
<span data-ttu-id="557e9-113">Se você confirmar para substituir o pipeline existente, a definição de pipeline também será substituída.</span><span class="sxs-lookup"><span data-stu-id="557e9-113">If you confirm to overwrite the existing pipeline, the pipeline definition is also replaced.</span></span>

## <span data-ttu-id="557e9-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="557e9-114">EXAMPLES</span></span>

### <span data-ttu-id="557e9-115">Exemplo 1: criar um pipeline</span><span class="sxs-lookup"><span data-stu-id="557e9-115">Example 1: Create a pipeline</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" -File "C:\DPWikisample.json"

    PipelineName      : DPWikisample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF11
    Activities        : {MyCopyActivity_0_0, MyCopyActivity_1_0}
    Parameters        : {[OutputBlobName, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}
```

<span data-ttu-id="557e9-116">Esse comando cria um pipeline chamado DPWikisample na fábrica de dados chamado ADF.</span><span class="sxs-lookup"><span data-stu-id="557e9-116">This command creates a pipeline named DPWikisample in the data factory named ADF.</span></span>
<span data-ttu-id="557e9-117">O comando baseia o pipeline nas informações do DPWikisample.jsem arquivo.</span><span class="sxs-lookup"><span data-stu-id="557e9-117">The command bases the pipeline on information in the DPWikisample.json file.</span></span>
<span data-ttu-id="557e9-118">Esse arquivo inclui informações sobre atividades como atividades de cópia e atividades do HDInsight no pipeline.</span><span class="sxs-lookup"><span data-stu-id="557e9-118">This file includes information about activities such as Copy Activity and HDInsight Activity in the pipeline.</span></span>

## <span data-ttu-id="557e9-119">OS</span><span class="sxs-lookup"><span data-stu-id="557e9-119">PARAMETERS</span></span>

### <span data-ttu-id="557e9-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="557e9-120">-Confirm</span></span>
<span data-ttu-id="557e9-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="557e9-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="557e9-122">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="557e9-122">-DataFactoryName</span></span>
<span data-ttu-id="557e9-123">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="557e9-123">Specifies the name of a data factory.</span></span>
<span data-ttu-id="557e9-124">Esse cmdlet cria um pipeline para a fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="557e9-124">This cmdlet creates a pipeline for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="557e9-125">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="557e9-125">-DefinitionFile</span></span>
<span data-ttu-id="557e9-126">O caminho do arquivo JSON.</span><span class="sxs-lookup"><span data-stu-id="557e9-126">The JSON file path.</span></span>

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

### <span data-ttu-id="557e9-127">-Force</span><span class="sxs-lookup"><span data-stu-id="557e9-127">-Force</span></span>
<span data-ttu-id="557e9-128">Indica que esse cmdlet substitui um pipeline existente sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="557e9-128">Indicates that this cmdlet replaces an existing pipeline without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="557e9-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="557e9-129">-Name</span></span>
<span data-ttu-id="557e9-130">Especifica o nome do pipeline a ser criado.</span><span class="sxs-lookup"><span data-stu-id="557e9-130">Specifies the name of the pipeline to create.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: PipelineName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="557e9-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="557e9-131">-ResourceGroupName</span></span>
<span data-ttu-id="557e9-132">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="557e9-132">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="557e9-133">Esse cmdlet cria um pipeline para o grupo especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="557e9-133">This cmdlet creates a pipeline for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="557e9-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="557e9-134">-ResourceId</span></span>
<span data-ttu-id="557e9-135">A ID do recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="557e9-135">The Azure resource ID.</span></span>

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

### <span data-ttu-id="557e9-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="557e9-136">-WhatIf</span></span>
<span data-ttu-id="557e9-137">Mostra o que acontece se o cmdlet for executado, mas não executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="557e9-137">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="557e9-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="557e9-138">-DefaultProfile</span></span>
<span data-ttu-id="557e9-139">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="557e9-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="557e9-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="557e9-140">CommonParameters</span></span>
<span data-ttu-id="557e9-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="557e9-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="557e9-142">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="557e9-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="557e9-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="557e9-143">INPUTS</span></span>

### <span data-ttu-id="557e9-144">System. String</span><span class="sxs-lookup"><span data-stu-id="557e9-144">System.String</span></span>

## <span data-ttu-id="557e9-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="557e9-145">OUTPUTS</span></span>

### <span data-ttu-id="557e9-146">Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="557e9-146">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="557e9-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="557e9-147">NOTES</span></span>
<span data-ttu-id="557e9-148">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas</span><span class="sxs-lookup"><span data-stu-id="557e9-148">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="557e9-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="557e9-149">RELATED LINKS</span></span>

[<span data-ttu-id="557e9-150">Get-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="557e9-150">Get-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="557e9-151">Remove-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="557e9-151">Remove-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="557e9-152">Invoke-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="557e9-152">Invoke-AzureRmDataFactoryV2Pipeline</span></span>]()
