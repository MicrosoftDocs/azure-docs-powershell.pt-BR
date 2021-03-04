---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/set-azdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Pipeline.md
ms.openlocfilehash: b059e48eda6367459bd90bd7ccdf93ea14387ae7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887001"
---
# <span data-ttu-id="63099-101">Set-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="63099-101">Set-AzDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="63099-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63099-102">SYNOPSIS</span></span>
<span data-ttu-id="63099-103">Cria um pipeline na Fábrica de Dados.</span><span class="sxs-lookup"><span data-stu-id="63099-103">Creates a pipeline in Data Factory.</span></span>

## <span data-ttu-id="63099-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="63099-104">SYNTAX</span></span>

### <span data-ttu-id="63099-105">ByFactoryName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="63099-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2Pipeline [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="63099-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="63099-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2Pipeline [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63099-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="63099-107">DESCRIPTION</span></span>
<span data-ttu-id="63099-108">O Set-AzDataFactoryV2Pipeline cmdlet cria um pipeline no Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="63099-108">The Set-AzDataFactoryV2Pipeline cmdlet creates a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="63099-109">Se você especificar um nome para um pipeline que já existe, o cmdlet solicitará confirmação antes de substituir o pipeline.</span><span class="sxs-lookup"><span data-stu-id="63099-109">If you specify a name for a pipeline that already exists, the cmdlet prompts you for confirmation before it replaces the pipeline.</span></span>
<span data-ttu-id="63099-110">Se você especificar o parâmetro Force, o cmdlet substituirá o pipeline existente sem confirmação.</span><span class="sxs-lookup"><span data-stu-id="63099-110">If you specify the Force parameter, the cmdlet replaces the existing pipeline without confirmation.</span></span>
<span data-ttu-id="63099-111">Execute essas operações na seguinte ordem: -- Criar um fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="63099-111">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="63099-112">-- Crie serviços vinculados.</span><span class="sxs-lookup"><span data-stu-id="63099-112">-- Create linked services.</span></span>
<span data-ttu-id="63099-113">-- Criar conjuntos de dados.</span><span class="sxs-lookup"><span data-stu-id="63099-113">-- Create datasets.</span></span>
<span data-ttu-id="63099-114">-- Crie um pipeline.</span><span class="sxs-lookup"><span data-stu-id="63099-114">-- Create a pipeline.</span></span>
<span data-ttu-id="63099-115">Se um pipeline com o mesmo nome já existir no fábrica de dados, este cmdlet solicitará que você confirme se deve substituir o pipeline existente com o novo pipeline.</span><span class="sxs-lookup"><span data-stu-id="63099-115">If a pipeline with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing pipeline with the new pipeline.</span></span>
<span data-ttu-id="63099-116">Se você confirmar para substituir o pipeline existente, a definição de pipeline também será substituída.</span><span class="sxs-lookup"><span data-stu-id="63099-116">If you confirm to overwrite the existing pipeline, the pipeline definition is also replaced.</span></span>

## <span data-ttu-id="63099-117">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="63099-117">EXAMPLES</span></span>

### <span data-ttu-id="63099-118">Exemplo 1: Criar um pipeline</span><span class="sxs-lookup"><span data-stu-id="63099-118">Example 1: Create a pipeline</span></span>
```
PS C:\> Set-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" -File "C:\DPWikisample.json"

    PipelineName      : DPWikisample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF11
    Activities        : {MyCopyActivity_0_0, MyCopyActivity_1_0}
    Parameters        : {[OutputBlobName, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}
```

<span data-ttu-id="63099-119">Este comando cria um pipeline chamado DPWikisample no fábrica de dados chamado ADF.</span><span class="sxs-lookup"><span data-stu-id="63099-119">This command creates a pipeline named DPWikisample in the data factory named ADF.</span></span>
<span data-ttu-id="63099-120">O comando baseia o pipeline em informações no arquivo DPWikisample.json.</span><span class="sxs-lookup"><span data-stu-id="63099-120">The command bases the pipeline on information in the DPWikisample.json file.</span></span>
<span data-ttu-id="63099-121">Este arquivo inclui informações sobre atividades como Copiar Atividade e Atividade HDInsight no pipeline.</span><span class="sxs-lookup"><span data-stu-id="63099-121">This file includes information about activities such as Copy Activity and HDInsight Activity in the pipeline.</span></span>

## <span data-ttu-id="63099-122">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="63099-122">PARAMETERS</span></span>

### <span data-ttu-id="63099-123">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="63099-123">-DataFactoryName</span></span>
<span data-ttu-id="63099-124">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="63099-124">Specifies the name of a data factory.</span></span>
<span data-ttu-id="63099-125">Este cmdlet cria um pipeline para o fábrica de dados especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="63099-125">This cmdlet creates a pipeline for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="63099-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63099-126">-DefaultProfile</span></span>
<span data-ttu-id="63099-127">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="63099-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="63099-128">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="63099-128">-DefinitionFile</span></span>
<span data-ttu-id="63099-129">O caminho do arquivo JSON.</span><span class="sxs-lookup"><span data-stu-id="63099-129">The JSON file path.</span></span>

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

### <span data-ttu-id="63099-130">-Force</span><span class="sxs-lookup"><span data-stu-id="63099-130">-Force</span></span>
<span data-ttu-id="63099-131">Indica que esse cmdlet substitui um pipeline existente sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="63099-131">Indicates that this cmdlet replaces an existing pipeline without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="63099-132">-Name</span><span class="sxs-lookup"><span data-stu-id="63099-132">-Name</span></span>
<span data-ttu-id="63099-133">Especifica o nome do pipeline a ser criado.</span><span class="sxs-lookup"><span data-stu-id="63099-133">Specifies the name of the pipeline to create.</span></span>

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

### <span data-ttu-id="63099-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63099-134">-ResourceGroupName</span></span>
<span data-ttu-id="63099-135">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="63099-135">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="63099-136">Este cmdlet cria um pipeline para o grupo especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="63099-136">This cmdlet creates a pipeline for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="63099-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="63099-137">-ResourceId</span></span>
<span data-ttu-id="63099-138">A ID de recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="63099-138">The Azure resource ID.</span></span>

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

### <span data-ttu-id="63099-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="63099-139">-Confirm</span></span>
<span data-ttu-id="63099-140">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63099-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63099-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63099-141">-WhatIf</span></span>
<span data-ttu-id="63099-142">Mostra o que acontece se o cmdlet for executado, mas não executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63099-142">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="63099-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63099-143">CommonParameters</span></span>
<span data-ttu-id="63099-144">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63099-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63099-145">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63099-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63099-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="63099-146">INPUTS</span></span>

### <span data-ttu-id="63099-147">System.String</span><span class="sxs-lookup"><span data-stu-id="63099-147">System.String</span></span>

## <span data-ttu-id="63099-148">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="63099-148">OUTPUTS</span></span>

### <span data-ttu-id="63099-149">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span><span class="sxs-lookup"><span data-stu-id="63099-149">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="63099-150">NOTES</span><span class="sxs-lookup"><span data-stu-id="63099-150">NOTES</span></span>
<span data-ttu-id="63099-151">Palavras-chave: azure, azurerm, arm, resource, management, manager, data, factories</span><span class="sxs-lookup"><span data-stu-id="63099-151">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="63099-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="63099-152">RELATED LINKS</span></span>

[<span data-ttu-id="63099-153">Get-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="63099-153">Get-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="63099-154">Remove-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="63099-154">Remove-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="63099-155">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="63099-155">Invoke-AzDataFactoryV2Pipeline</span></span>]()
