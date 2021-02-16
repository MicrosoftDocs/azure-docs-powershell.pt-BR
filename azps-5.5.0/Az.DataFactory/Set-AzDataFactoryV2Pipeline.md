---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Pipeline.md
ms.openlocfilehash: 34db93baa063961958bdd4422143fdbe82b5f6a7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117740"
---
# <span data-ttu-id="b0a2f-101">Set-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="b0a2f-101">Set-AzDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="b0a2f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b0a2f-102">SYNOPSIS</span></span>
<span data-ttu-id="b0a2f-103">Cria um pipeline no Data Factory.</span><span class="sxs-lookup"><span data-stu-id="b0a2f-103">Creates a pipeline in Data Factory.</span></span>

## <span data-ttu-id="b0a2f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b0a2f-104">SYNTAX</span></span>

### <span data-ttu-id="b0a2f-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="b0a2f-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2Pipeline [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b0a2f-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b0a2f-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2Pipeline [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0a2f-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="b0a2f-107">DESCRIPTION</span></span>
<span data-ttu-id="b0a2f-108">O Set-AzDataFactoryV2Pipeline cmdlet cria um pipeline no Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="b0a2f-108">The Set-AzDataFactoryV2Pipeline cmdlet creates a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="b0a2f-109">Se você especificar um nome para um pipeline que já existe, o cmdlet solicitará confirmação antes de substituir o pipeline.</span><span class="sxs-lookup"><span data-stu-id="b0a2f-109">If you specify a name for a pipeline that already exists, the cmdlet prompts you for confirmation before it replaces the pipeline.</span></span>
<span data-ttu-id="b0a2f-110">Se você especificar o parâmetro Force, o cmdlet substituirá o pipeline existente sem confirmação.</span><span class="sxs-lookup"><span data-stu-id="b0a2f-110">If you specify the Force parameter, the cmdlet replaces the existing pipeline without confirmation.</span></span>
<span data-ttu-id="b0a2f-111">Execute essas operações na seguinte ordem: - Criar uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="b0a2f-111">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="b0a2f-112">- Criar serviços vinculados.</span><span class="sxs-lookup"><span data-stu-id="b0a2f-112">-- Create linked services.</span></span>
<span data-ttu-id="b0a2f-113">-- Criar conjuntos de dados.</span><span class="sxs-lookup"><span data-stu-id="b0a2f-113">-- Create datasets.</span></span>
<span data-ttu-id="b0a2f-114">- Criar um pipeline.</span><span class="sxs-lookup"><span data-stu-id="b0a2f-114">-- Create a pipeline.</span></span>
<span data-ttu-id="b0a2f-115">Se um pipeline com o mesmo nome já existir na fábrica de dados, esse cmdlet solicitará que você confirme se deve substituir o pipeline existente pelo novo pipeline.</span><span class="sxs-lookup"><span data-stu-id="b0a2f-115">If a pipeline with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing pipeline with the new pipeline.</span></span>
<span data-ttu-id="b0a2f-116">Se você confirmar para substituir o pipeline existente, a definição do pipeline também será substituída.</span><span class="sxs-lookup"><span data-stu-id="b0a2f-116">If you confirm to overwrite the existing pipeline, the pipeline definition is also replaced.</span></span>

## <span data-ttu-id="b0a2f-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b0a2f-117">EXAMPLES</span></span>

### <span data-ttu-id="b0a2f-118">Exemplo 1: Criar um pipeline</span><span class="sxs-lookup"><span data-stu-id="b0a2f-118">Example 1: Create a pipeline</span></span>
```
PS C:\> Set-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" -File "C:\DPWikisample.json"

    PipelineName      : DPWikisample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF11
    Activities        : {MyCopyActivity_0_0, MyCopyActivity_1_0}
    Parameters        : {[OutputBlobName, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}
```

<span data-ttu-id="b0a2f-119">Esse comando cria um pipeline chamado DPWikisample na fábrica de dados chamada ADF.</span><span class="sxs-lookup"><span data-stu-id="b0a2f-119">This command creates a pipeline named DPWikisample in the data factory named ADF.</span></span>
<span data-ttu-id="b0a2f-120">O comando baseia o pipeline em informações no DPWikisample.jsno arquivo.</span><span class="sxs-lookup"><span data-stu-id="b0a2f-120">The command bases the pipeline on information in the DPWikisample.json file.</span></span>
<span data-ttu-id="b0a2f-121">Esse arquivo inclui informações sobre atividades como Copiar Atividade e Atividade HDInsight no pipeline.</span><span class="sxs-lookup"><span data-stu-id="b0a2f-121">This file includes information about activities such as Copy Activity and HDInsight Activity in the pipeline.</span></span>

## <span data-ttu-id="b0a2f-122">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b0a2f-122">PARAMETERS</span></span>

### <span data-ttu-id="b0a2f-123">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="b0a2f-123">-DataFactoryName</span></span>
<span data-ttu-id="b0a2f-124">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="b0a2f-124">Specifies the name of a data factory.</span></span>
<span data-ttu-id="b0a2f-125">Este cmdlet cria um pipeline para a fábrica de dados especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="b0a2f-125">This cmdlet creates a pipeline for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="b0a2f-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0a2f-126">-DefaultProfile</span></span>
<span data-ttu-id="b0a2f-127">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="b0a2f-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b0a2f-128">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="b0a2f-128">-DefinitionFile</span></span>
<span data-ttu-id="b0a2f-129">O caminho do arquivo JSON.</span><span class="sxs-lookup"><span data-stu-id="b0a2f-129">The JSON file path.</span></span>

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

### <span data-ttu-id="b0a2f-130">-Forçar</span><span class="sxs-lookup"><span data-stu-id="b0a2f-130">-Force</span></span>
<span data-ttu-id="b0a2f-131">Indica que esse cmdlet substitui um pipeline existente sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="b0a2f-131">Indicates that this cmdlet replaces an existing pipeline without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="b0a2f-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="b0a2f-132">-Name</span></span>
<span data-ttu-id="b0a2f-133">Especifica o nome do pipeline a ser criado.</span><span class="sxs-lookup"><span data-stu-id="b0a2f-133">Specifies the name of the pipeline to create.</span></span>

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

### <span data-ttu-id="b0a2f-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0a2f-134">-ResourceGroupName</span></span>
<span data-ttu-id="b0a2f-135">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="b0a2f-135">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="b0a2f-136">Este cmdlet cria um pipeline para o grupo especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="b0a2f-136">This cmdlet creates a pipeline for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="b0a2f-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b0a2f-137">-ResourceId</span></span>
<span data-ttu-id="b0a2f-138">A ID de recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="b0a2f-138">The Azure resource ID.</span></span>

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

### <span data-ttu-id="b0a2f-139">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="b0a2f-139">-Confirm</span></span>
<span data-ttu-id="b0a2f-140">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b0a2f-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0a2f-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0a2f-141">-WhatIf</span></span>
<span data-ttu-id="b0a2f-142">Mostra o que acontece se o cmdlet é executado, mas não executa o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b0a2f-142">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="b0a2f-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0a2f-143">CommonParameters</span></span>
<span data-ttu-id="b0a2f-144">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0a2f-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0a2f-145">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0a2f-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0a2f-146">Entradas</span><span class="sxs-lookup"><span data-stu-id="b0a2f-146">INPUTS</span></span>

### <span data-ttu-id="b0a2f-147">System.String</span><span class="sxs-lookup"><span data-stu-id="b0a2f-147">System.String</span></span>

## <span data-ttu-id="b0a2f-148">Saídas</span><span class="sxs-lookup"><span data-stu-id="b0a2f-148">OUTPUTS</span></span>

### <span data-ttu-id="b0a2f-149">Microsoft.Azure.Commands.DataFactoryV2.Models.PSInaline</span><span class="sxs-lookup"><span data-stu-id="b0a2f-149">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="b0a2f-150">Notas</span><span class="sxs-lookup"><span data-stu-id="b0a2f-150">NOTES</span></span>
<span data-ttu-id="b0a2f-151">Palavras-chave: azure, azurerm, arm, resource, management, manager, data,</span><span class="sxs-lookup"><span data-stu-id="b0a2f-151">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="b0a2f-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b0a2f-152">RELATED LINKS</span></span>

[<span data-ttu-id="b0a2f-153">Get-AzDataFactoryV2Dataline</span><span class="sxs-lookup"><span data-stu-id="b0a2f-153">Get-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="b0a2f-154">Remove-AzDataFactoryV2Dataline</span><span class="sxs-lookup"><span data-stu-id="b0a2f-154">Remove-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="b0a2f-155">Invoke-AzDataFactoryV2 Invokeline</span><span class="sxs-lookup"><span data-stu-id="b0a2f-155">Invoke-AzDataFactoryV2Pipeline</span></span>]()
