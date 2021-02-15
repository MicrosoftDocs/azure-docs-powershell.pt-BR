---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 30C1AF6C-A8DC-4CA0-9E5F-10641A29D0E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryPipeline.md
ms.openlocfilehash: e8917b9c68cb0708d34faa0e0dfec8e0e912f54b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118818"
---
# <span data-ttu-id="ba3fb-101">New-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="ba3fb-101">New-AzDataFactoryPipeline</span></span>

## <span data-ttu-id="ba3fb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ba3fb-102">SYNOPSIS</span></span>
<span data-ttu-id="ba3fb-103">Cria um pipeline no Data Factory.</span><span class="sxs-lookup"><span data-stu-id="ba3fb-103">Creates a pipeline in Data Factory.</span></span>

## <span data-ttu-id="ba3fb-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ba3fb-104">SYNTAX</span></span>

### <span data-ttu-id="ba3fb-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="ba3fb-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryPipeline [[-Name] <String>] [-DataFactoryName] <String> [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ba3fb-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="ba3fb-106">ByFactoryObject</span></span>
```
New-AzDataFactoryPipeline [[-Name] <String>] [-DataFactory] <PSDataFactory> [-File] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba3fb-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="ba3fb-107">DESCRIPTION</span></span>
<span data-ttu-id="ba3fb-108">O cmdlet **New-AzDataFactory Pipelineline** cria um pipeline no Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="ba3fb-108">The **New-AzDataFactoryPipeline** cmdlet creates a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="ba3fb-109">Se você especificar um nome para um pipeline que já existe, o cmdlet solicitará confirmação antes de substituir o pipeline.</span><span class="sxs-lookup"><span data-stu-id="ba3fb-109">If you specify a name for a pipeline that already exists, the cmdlet prompts you for confirmation before it replaces the pipeline.</span></span>
<span data-ttu-id="ba3fb-110">Se você especificar o *parâmetro Force,* o cmdlet substituirá o pipeline existente sem confirmação.</span><span class="sxs-lookup"><span data-stu-id="ba3fb-110">If you specify the *Force* parameter, the cmdlet replaces the existing pipeline without confirmation.</span></span>
<span data-ttu-id="ba3fb-111">Execute essas operações na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="ba3fb-111">Perform these operations in the following order:</span></span> 
- <span data-ttu-id="ba3fb-112">Criar uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="ba3fb-112">Create a data factory.</span></span> 
- <span data-ttu-id="ba3fb-113">Criar serviços vinculados.</span><span class="sxs-lookup"><span data-stu-id="ba3fb-113">Create linked services.</span></span> 
- <span data-ttu-id="ba3fb-114">Criar conjuntos de dados.</span><span class="sxs-lookup"><span data-stu-id="ba3fb-114">Create datasets.</span></span> 
- <span data-ttu-id="ba3fb-115">Criar um pipeline.</span><span class="sxs-lookup"><span data-stu-id="ba3fb-115">Create a pipeline.</span></span>
<span data-ttu-id="ba3fb-116">Se um pipeline com o mesmo nome já existir na fábrica de dados, esse cmdlet solicitará que você confirme se deve substituir o pipeline existente pelo novo pipeline.</span><span class="sxs-lookup"><span data-stu-id="ba3fb-116">If a pipeline with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing pipeline with the new pipeline.</span></span>
<span data-ttu-id="ba3fb-117">Se você confirmar para substituir o pipeline existente, a definição do pipeline também será substituída.</span><span class="sxs-lookup"><span data-stu-id="ba3fb-117">If you confirm to overwrite the existing pipeline, the pipeline definition is also replaced.</span></span>

## <span data-ttu-id="ba3fb-118">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ba3fb-118">EXAMPLES</span></span>

### <span data-ttu-id="ba3fb-119">Exemplo 1: Criar um pipeline</span><span class="sxs-lookup"><span data-stu-id="ba3fb-119">Example 1: Create a pipeline</span></span>
```
PS C:\>New-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" -File "C:\DPWikisample.json" 
PipelineName      : DPWikisample
ResourceGroupName : ADF
DataFactoryName   : WikiADF11
Properties        : Microsoft.DataFactories.PipelineProperties
```

<span data-ttu-id="ba3fb-120">Esse comando cria um pipeline chamado DPWikisample na fábrica de dados chamada ADF.</span><span class="sxs-lookup"><span data-stu-id="ba3fb-120">This command creates a pipeline named DPWikisample in the data factory named ADF.</span></span>
<span data-ttu-id="ba3fb-121">O comando baseia o pipeline em informações no DPWikisample.jsno arquivo.</span><span class="sxs-lookup"><span data-stu-id="ba3fb-121">The command bases the pipeline on information in the DPWikisample.json file.</span></span>
<span data-ttu-id="ba3fb-122">Esse arquivo inclui informações sobre atividades como Copiar Atividade e Atividade HDInsight no pipeline.</span><span class="sxs-lookup"><span data-stu-id="ba3fb-122">This file includes information about activities such as Copy Activity and HDInsight Activity in the pipeline.</span></span>

## <span data-ttu-id="ba3fb-123">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ba3fb-123">PARAMETERS</span></span>

### <span data-ttu-id="ba3fb-124">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="ba3fb-124">-DataFactory</span></span>
<span data-ttu-id="ba3fb-125">Especifica um **objeto PSDataFactory.**</span><span class="sxs-lookup"><span data-stu-id="ba3fb-125">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="ba3fb-126">Este cmdlet cria um pipeline para a fábrica de dados especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="ba3fb-126">This cmdlet creates a pipeline for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="ba3fb-127">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="ba3fb-127">-DataFactoryName</span></span>
<span data-ttu-id="ba3fb-128">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="ba3fb-128">Specifies the name of a data factory.</span></span>
<span data-ttu-id="ba3fb-129">Este cmdlet cria um pipeline para a fábrica de dados especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="ba3fb-129">This cmdlet creates a pipeline for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="ba3fb-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba3fb-130">-DefaultProfile</span></span>
<span data-ttu-id="ba3fb-131">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="ba3fb-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ba3fb-132">-Arquivo</span><span class="sxs-lookup"><span data-stu-id="ba3fb-132">-File</span></span>
<span data-ttu-id="ba3fb-133">Especifica o caminho completo do arquivo JSON (Notação de Objeto JavaScript) que contém a descrição do pipeline.</span><span class="sxs-lookup"><span data-stu-id="ba3fb-133">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the pipeline.</span></span>

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

### <span data-ttu-id="ba3fb-134">-Forçar</span><span class="sxs-lookup"><span data-stu-id="ba3fb-134">-Force</span></span>
<span data-ttu-id="ba3fb-135">Indica que esse cmdlet substitui um pipeline existente sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="ba3fb-135">Indicates that this cmdlet replaces an existing pipeline without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="ba3fb-136">-Nome</span><span class="sxs-lookup"><span data-stu-id="ba3fb-136">-Name</span></span>
<span data-ttu-id="ba3fb-137">Especifica o nome do pipeline a ser criado.</span><span class="sxs-lookup"><span data-stu-id="ba3fb-137">Specifies the name of the pipeline to create.</span></span>

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

### <span data-ttu-id="ba3fb-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba3fb-138">-ResourceGroupName</span></span>
<span data-ttu-id="ba3fb-139">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="ba3fb-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="ba3fb-140">Este cmdlet cria um pipeline para o grupo especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="ba3fb-140">This cmdlet creates a pipeline for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="ba3fb-141">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="ba3fb-141">-Confirm</span></span>
<span data-ttu-id="ba3fb-142">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ba3fb-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba3fb-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba3fb-143">-WhatIf</span></span>
<span data-ttu-id="ba3fb-144">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="ba3fb-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba3fb-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ba3fb-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba3fb-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba3fb-146">CommonParameters</span></span>
<span data-ttu-id="ba3fb-147">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba3fb-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba3fb-148">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba3fb-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba3fb-149">Entradas</span><span class="sxs-lookup"><span data-stu-id="ba3fb-149">INPUTS</span></span>

### <span data-ttu-id="ba3fb-150">System.String</span><span class="sxs-lookup"><span data-stu-id="ba3fb-150">System.String</span></span>

### <span data-ttu-id="ba3fb-151">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="ba3fb-151">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="ba3fb-152">Saídas</span><span class="sxs-lookup"><span data-stu-id="ba3fb-152">OUTPUTS</span></span>

### <span data-ttu-id="ba3fb-153">Microsoft.Azure.Commands.DataFactories.Models.PS Eleline</span><span class="sxs-lookup"><span data-stu-id="ba3fb-153">Microsoft.Azure.Commands.DataFactories.Models.PSPipeline</span></span>

## <span data-ttu-id="ba3fb-154">Notas</span><span class="sxs-lookup"><span data-stu-id="ba3fb-154">NOTES</span></span>
* <span data-ttu-id="ba3fb-155">Palavras-chave: azure, azurerm, arm, resource, management, manager, data,</span><span class="sxs-lookup"><span data-stu-id="ba3fb-155">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="ba3fb-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ba3fb-156">RELATED LINKS</span></span>

[<span data-ttu-id="ba3fb-157">Get-AzDataFactoryFactline</span><span class="sxs-lookup"><span data-stu-id="ba3fb-157">Get-AzDataFactoryPipeline</span></span>](./Get-AzDataFactoryPipeline.md)

[<span data-ttu-id="ba3fb-158">Remove-AzDataFactoryDataDataLine</span><span class="sxs-lookup"><span data-stu-id="ba3fb-158">Remove-AzDataFactoryPipeline</span></span>](./Remove-AzDataFactoryPipeline.md)

[<span data-ttu-id="ba3fb-159">Resume-AzDataDataFactoryDataLine</span><span class="sxs-lookup"><span data-stu-id="ba3fb-159">Resume-AzDataFactoryPipeline</span></span>](./Resume-AzDataFactoryPipeline.md)

[<span data-ttu-id="ba3fb-160">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="ba3fb-160">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="ba3fb-161">Suspend-AzDataFactoryFactline</span><span class="sxs-lookup"><span data-stu-id="ba3fb-161">Suspend-AzDataFactoryPipeline</span></span>](./Suspend-AzDataFactoryPipeline.md)


