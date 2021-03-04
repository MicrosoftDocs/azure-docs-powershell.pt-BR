---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 30C1AF6C-A8DC-4CA0-9E5F-10641A29D0E8
online version: https://docs.microsoft.com/powershell/module/az.datafactory/new-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryPipeline.md
ms.openlocfilehash: ad731dc612290e572ee74a967788e324f764a930
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887790"
---
# <span data-ttu-id="cdfdd-101">New-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="cdfdd-101">New-AzDataFactoryPipeline</span></span>

## <span data-ttu-id="cdfdd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cdfdd-102">SYNOPSIS</span></span>
<span data-ttu-id="cdfdd-103">Cria um pipeline na Fábrica de Dados.</span><span class="sxs-lookup"><span data-stu-id="cdfdd-103">Creates a pipeline in Data Factory.</span></span>

## <span data-ttu-id="cdfdd-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="cdfdd-104">SYNTAX</span></span>

### <span data-ttu-id="cdfdd-105">ByFactoryName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="cdfdd-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryPipeline [[-Name] <String>] [-DataFactoryName] <String> [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cdfdd-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="cdfdd-106">ByFactoryObject</span></span>
```
New-AzDataFactoryPipeline [[-Name] <String>] [-DataFactory] <PSDataFactory> [-File] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cdfdd-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="cdfdd-107">DESCRIPTION</span></span>
<span data-ttu-id="cdfdd-108">O cmdlet **New-AzDataFactoryPipeline** cria um pipeline no Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="cdfdd-108">The **New-AzDataFactoryPipeline** cmdlet creates a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="cdfdd-109">Se você especificar um nome para um pipeline que já existe, o cmdlet solicitará confirmação antes de substituir o pipeline.</span><span class="sxs-lookup"><span data-stu-id="cdfdd-109">If you specify a name for a pipeline that already exists, the cmdlet prompts you for confirmation before it replaces the pipeline.</span></span>
<span data-ttu-id="cdfdd-110">Se você especificar o *parâmetro Force,* o cmdlet substituirá o pipeline existente sem confirmação.</span><span class="sxs-lookup"><span data-stu-id="cdfdd-110">If you specify the *Force* parameter, the cmdlet replaces the existing pipeline without confirmation.</span></span>
<span data-ttu-id="cdfdd-111">Execute essas operações na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="cdfdd-111">Perform these operations in the following order:</span></span> 
- <span data-ttu-id="cdfdd-112">Criar uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="cdfdd-112">Create a data factory.</span></span> 
- <span data-ttu-id="cdfdd-113">Criar serviços vinculados.</span><span class="sxs-lookup"><span data-stu-id="cdfdd-113">Create linked services.</span></span> 
- <span data-ttu-id="cdfdd-114">Criar conjuntos de dados.</span><span class="sxs-lookup"><span data-stu-id="cdfdd-114">Create datasets.</span></span> 
- <span data-ttu-id="cdfdd-115">Criar um pipeline.</span><span class="sxs-lookup"><span data-stu-id="cdfdd-115">Create a pipeline.</span></span>
<span data-ttu-id="cdfdd-116">Se um pipeline com o mesmo nome já existir no fábrica de dados, este cmdlet solicitará que você confirme se deve substituir o pipeline existente com o novo pipeline.</span><span class="sxs-lookup"><span data-stu-id="cdfdd-116">If a pipeline with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing pipeline with the new pipeline.</span></span>
<span data-ttu-id="cdfdd-117">Se você confirmar para substituir o pipeline existente, a definição de pipeline também será substituída.</span><span class="sxs-lookup"><span data-stu-id="cdfdd-117">If you confirm to overwrite the existing pipeline, the pipeline definition is also replaced.</span></span>

## <span data-ttu-id="cdfdd-118">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cdfdd-118">EXAMPLES</span></span>

### <span data-ttu-id="cdfdd-119">Exemplo 1: Criar um pipeline</span><span class="sxs-lookup"><span data-stu-id="cdfdd-119">Example 1: Create a pipeline</span></span>
```
PS C:\>New-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" -File "C:\DPWikisample.json" 
PipelineName      : DPWikisample
ResourceGroupName : ADF
DataFactoryName   : WikiADF11
Properties        : Microsoft.DataFactories.PipelineProperties
```

<span data-ttu-id="cdfdd-120">Este comando cria um pipeline chamado DPWikisample no fábrica de dados chamado ADF.</span><span class="sxs-lookup"><span data-stu-id="cdfdd-120">This command creates a pipeline named DPWikisample in the data factory named ADF.</span></span>
<span data-ttu-id="cdfdd-121">O comando baseia o pipeline em informações no arquivo DPWikisample.json.</span><span class="sxs-lookup"><span data-stu-id="cdfdd-121">The command bases the pipeline on information in the DPWikisample.json file.</span></span>
<span data-ttu-id="cdfdd-122">Este arquivo inclui informações sobre atividades como Copiar Atividade e Atividade HDInsight no pipeline.</span><span class="sxs-lookup"><span data-stu-id="cdfdd-122">This file includes information about activities such as Copy Activity and HDInsight Activity in the pipeline.</span></span>

## <span data-ttu-id="cdfdd-123">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="cdfdd-123">PARAMETERS</span></span>

### <span data-ttu-id="cdfdd-124">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="cdfdd-124">-DataFactory</span></span>
<span data-ttu-id="cdfdd-125">Especifica um **objeto PSDataFactory.**</span><span class="sxs-lookup"><span data-stu-id="cdfdd-125">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="cdfdd-126">Este cmdlet cria um pipeline para o fábrica de dados especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="cdfdd-126">This cmdlet creates a pipeline for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="cdfdd-127">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="cdfdd-127">-DataFactoryName</span></span>
<span data-ttu-id="cdfdd-128">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="cdfdd-128">Specifies the name of a data factory.</span></span>
<span data-ttu-id="cdfdd-129">Este cmdlet cria um pipeline para o fábrica de dados especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="cdfdd-129">This cmdlet creates a pipeline for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="cdfdd-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdfdd-130">-DefaultProfile</span></span>
<span data-ttu-id="cdfdd-131">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="cdfdd-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cdfdd-132">-File</span><span class="sxs-lookup"><span data-stu-id="cdfdd-132">-File</span></span>
<span data-ttu-id="cdfdd-133">Especifica o caminho completo do arquivo JSON (Notação de Objeto JavaScript) que contém a descrição do pipeline.</span><span class="sxs-lookup"><span data-stu-id="cdfdd-133">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the pipeline.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdfdd-134">-Force</span><span class="sxs-lookup"><span data-stu-id="cdfdd-134">-Force</span></span>
<span data-ttu-id="cdfdd-135">Indica que esse cmdlet substitui um pipeline existente sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="cdfdd-135">Indicates that this cmdlet replaces an existing pipeline without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="cdfdd-136">-Name</span><span class="sxs-lookup"><span data-stu-id="cdfdd-136">-Name</span></span>
<span data-ttu-id="cdfdd-137">Especifica o nome do pipeline a ser criado.</span><span class="sxs-lookup"><span data-stu-id="cdfdd-137">Specifies the name of the pipeline to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdfdd-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cdfdd-138">-ResourceGroupName</span></span>
<span data-ttu-id="cdfdd-139">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="cdfdd-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="cdfdd-140">Este cmdlet cria um pipeline para o grupo especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="cdfdd-140">This cmdlet creates a pipeline for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="cdfdd-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cdfdd-141">-Confirm</span></span>
<span data-ttu-id="cdfdd-142">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cdfdd-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cdfdd-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cdfdd-143">-WhatIf</span></span>
<span data-ttu-id="cdfdd-144">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cdfdd-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cdfdd-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cdfdd-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cdfdd-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdfdd-146">CommonParameters</span></span>
<span data-ttu-id="cdfdd-147">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cdfdd-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdfdd-148">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cdfdd-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdfdd-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cdfdd-149">INPUTS</span></span>

### <span data-ttu-id="cdfdd-150">System.String</span><span class="sxs-lookup"><span data-stu-id="cdfdd-150">System.String</span></span>

### <span data-ttu-id="cdfdd-151">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="cdfdd-151">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="cdfdd-152">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="cdfdd-152">OUTPUTS</span></span>

### <span data-ttu-id="cdfdd-153">Microsoft.Azure.Commands.DataFactories.Models.PSPipeline</span><span class="sxs-lookup"><span data-stu-id="cdfdd-153">Microsoft.Azure.Commands.DataFactories.Models.PSPipeline</span></span>

## <span data-ttu-id="cdfdd-154">NOTES</span><span class="sxs-lookup"><span data-stu-id="cdfdd-154">NOTES</span></span>
* <span data-ttu-id="cdfdd-155">Palavras-chave: azure, azurerm, arm, resource, management, manager, data, factories</span><span class="sxs-lookup"><span data-stu-id="cdfdd-155">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="cdfdd-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cdfdd-156">RELATED LINKS</span></span>

[<span data-ttu-id="cdfdd-157">Get-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="cdfdd-157">Get-AzDataFactoryPipeline</span></span>](./Get-AzDataFactoryPipeline.md)

[<span data-ttu-id="cdfdd-158">Remove-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="cdfdd-158">Remove-AzDataFactoryPipeline</span></span>](./Remove-AzDataFactoryPipeline.md)

[<span data-ttu-id="cdfdd-159">Resume-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="cdfdd-159">Resume-AzDataFactoryPipeline</span></span>](./Resume-AzDataFactoryPipeline.md)

[<span data-ttu-id="cdfdd-160">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="cdfdd-160">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="cdfdd-161">Suspend-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="cdfdd-161">Suspend-AzDataFactoryPipeline</span></span>](./Suspend-AzDataFactoryPipeline.md)


