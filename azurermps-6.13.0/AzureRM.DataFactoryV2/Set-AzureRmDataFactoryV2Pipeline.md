---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/set-azurermdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2Pipeline.md
ms.openlocfilehash: dcdf7cdf9de6de23a3178fe8cbb4ac0f67f43d30
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440801"
---
# <span data-ttu-id="1d749-101">Set-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="1d749-101">Set-AzureRmDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="1d749-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1d749-102">SYNOPSIS</span></span>
<span data-ttu-id="1d749-103">Cria um pipeline na fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="1d749-103">Creates a pipeline in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1d749-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1d749-104">SYNTAX</span></span>

### <span data-ttu-id="1d749-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="1d749-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactoryV2Pipeline [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1d749-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1d749-106">ByResourceId</span></span>
```
Set-AzureRmDataFactoryV2Pipeline [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d749-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1d749-107">DESCRIPTION</span></span>
<span data-ttu-id="1d749-108">O cmdlet Set-AzureRmDataFactoryV2Pipeline cria um pipeline no Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="1d749-108">The Set-AzureRmDataFactoryV2Pipeline cmdlet creates a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="1d749-109">Se você especificar um nome para um pipeline já existente, o cmdlet solicitará confirmação antes de substituir o pipeline.</span><span class="sxs-lookup"><span data-stu-id="1d749-109">If you specify a name for a pipeline that already exists, the cmdlet prompts you for confirmation before it replaces the pipeline.</span></span>
<span data-ttu-id="1d749-110">Se você especificar o parâmetro Force, o cmdlet substituirá o pipeline existente sem confirmação.</span><span class="sxs-lookup"><span data-stu-id="1d749-110">If you specify the Force parameter, the cmdlet replaces the existing pipeline without confirmation.</span></span>
<span data-ttu-id="1d749-111">Execute estas operações na seguinte ordem:--Crie uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="1d749-111">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="1d749-112">--Criar serviços vinculados.</span><span class="sxs-lookup"><span data-stu-id="1d749-112">-- Create linked services.</span></span>
<span data-ttu-id="1d749-113">--Criar conjuntos de valores.</span><span class="sxs-lookup"><span data-stu-id="1d749-113">-- Create datasets.</span></span>
<span data-ttu-id="1d749-114">--Criar um pipeline.</span><span class="sxs-lookup"><span data-stu-id="1d749-114">-- Create a pipeline.</span></span>
<span data-ttu-id="1d749-115">Se um pipeline com o mesmo nome já existir na fábrica de dados, esse cmdlet solicitará que você confirme se deseja substituir o pipeline existente pelo novo pipeline.</span><span class="sxs-lookup"><span data-stu-id="1d749-115">If a pipeline with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing pipeline with the new pipeline.</span></span>
<span data-ttu-id="1d749-116">Se você confirmar para substituir o pipeline existente, a definição de pipeline também será substituída.</span><span class="sxs-lookup"><span data-stu-id="1d749-116">If you confirm to overwrite the existing pipeline, the pipeline definition is also replaced.</span></span>

## <span data-ttu-id="1d749-117">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1d749-117">EXAMPLES</span></span>

### <span data-ttu-id="1d749-118">Exemplo 1: criar um pipeline</span><span class="sxs-lookup"><span data-stu-id="1d749-118">Example 1: Create a pipeline</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" -File "C:\DPWikisample.json"

    PipelineName      : DPWikisample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF11
    Activities        : {MyCopyActivity_0_0, MyCopyActivity_1_0}
    Parameters        : {[OutputBlobName, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}
```

<span data-ttu-id="1d749-119">Esse comando cria um pipeline chamado DPWikisample na fábrica de dados chamado ADF.</span><span class="sxs-lookup"><span data-stu-id="1d749-119">This command creates a pipeline named DPWikisample in the data factory named ADF.</span></span>
<span data-ttu-id="1d749-120">O comando baseia o pipeline nas informações do DPWikisample.jsem arquivo.</span><span class="sxs-lookup"><span data-stu-id="1d749-120">The command bases the pipeline on information in the DPWikisample.json file.</span></span>
<span data-ttu-id="1d749-121">Esse arquivo inclui informações sobre atividades como atividades de cópia e atividades do HDInsight no pipeline.</span><span class="sxs-lookup"><span data-stu-id="1d749-121">This file includes information about activities such as Copy Activity and HDInsight Activity in the pipeline.</span></span>

## <span data-ttu-id="1d749-122">OS</span><span class="sxs-lookup"><span data-stu-id="1d749-122">PARAMETERS</span></span>

### <span data-ttu-id="1d749-123">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="1d749-123">-DataFactoryName</span></span>
<span data-ttu-id="1d749-124">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="1d749-124">Specifies the name of a data factory.</span></span>
<span data-ttu-id="1d749-125">Esse cmdlet cria um pipeline para a fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="1d749-125">This cmdlet creates a pipeline for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="1d749-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d749-126">-DefaultProfile</span></span>
<span data-ttu-id="1d749-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1d749-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d749-128">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="1d749-128">-DefinitionFile</span></span>
<span data-ttu-id="1d749-129">O caminho do arquivo JSON.</span><span class="sxs-lookup"><span data-stu-id="1d749-129">The JSON file path.</span></span>

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

### <span data-ttu-id="1d749-130">-Force</span><span class="sxs-lookup"><span data-stu-id="1d749-130">-Force</span></span>
<span data-ttu-id="1d749-131">Indica que esse cmdlet substitui um pipeline existente sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="1d749-131">Indicates that this cmdlet replaces an existing pipeline without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="1d749-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="1d749-132">-Name</span></span>
<span data-ttu-id="1d749-133">Especifica o nome do pipeline a ser criado.</span><span class="sxs-lookup"><span data-stu-id="1d749-133">Specifies the name of the pipeline to create.</span></span>

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

### <span data-ttu-id="1d749-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d749-134">-ResourceGroupName</span></span>
<span data-ttu-id="1d749-135">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="1d749-135">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="1d749-136">Esse cmdlet cria um pipeline para o grupo especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="1d749-136">This cmdlet creates a pipeline for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="1d749-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1d749-137">-ResourceId</span></span>
<span data-ttu-id="1d749-138">A ID do recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="1d749-138">The Azure resource ID.</span></span>

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

### <span data-ttu-id="1d749-139">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1d749-139">-Confirm</span></span>
<span data-ttu-id="1d749-140">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1d749-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d749-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d749-141">-WhatIf</span></span>
<span data-ttu-id="1d749-142">Mostra o que acontece se o cmdlet for executado, mas não executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1d749-142">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="1d749-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d749-143">CommonParameters</span></span>
<span data-ttu-id="1d749-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d749-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d749-145">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d749-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d749-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1d749-146">INPUTS</span></span>

### <span data-ttu-id="1d749-147">System. String</span><span class="sxs-lookup"><span data-stu-id="1d749-147">System.String</span></span>

## <span data-ttu-id="1d749-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1d749-148">OUTPUTS</span></span>

### <span data-ttu-id="1d749-149">Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="1d749-149">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="1d749-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1d749-150">NOTES</span></span>
<span data-ttu-id="1d749-151">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas</span><span class="sxs-lookup"><span data-stu-id="1d749-151">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="1d749-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1d749-152">RELATED LINKS</span></span>

[<span data-ttu-id="1d749-153">Get-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="1d749-153">Get-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="1d749-154">Remove-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="1d749-154">Remove-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="1d749-155">Invoke-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="1d749-155">Invoke-AzureRmDataFactoryV2Pipeline</span></span>]()