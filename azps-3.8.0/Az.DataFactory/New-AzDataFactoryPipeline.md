---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 30C1AF6C-A8DC-4CA0-9E5F-10641A29D0E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryPipeline.md
ms.openlocfilehash: e8917b9c68cb0708d34faa0e0dfec8e0e912f54b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93778335"
---
# <span data-ttu-id="e6a1f-101">New-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="e6a1f-101">New-AzDataFactoryPipeline</span></span>

## <span data-ttu-id="e6a1f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e6a1f-102">SYNOPSIS</span></span>
<span data-ttu-id="e6a1f-103">Cria um pipeline na fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="e6a1f-103">Creates a pipeline in Data Factory.</span></span>

## <span data-ttu-id="e6a1f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e6a1f-104">SYNTAX</span></span>

### <span data-ttu-id="e6a1f-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="e6a1f-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryPipeline [[-Name] <String>] [-DataFactoryName] <String> [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e6a1f-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="e6a1f-106">ByFactoryObject</span></span>
```
New-AzDataFactoryPipeline [[-Name] <String>] [-DataFactory] <PSDataFactory> [-File] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6a1f-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e6a1f-107">DESCRIPTION</span></span>
<span data-ttu-id="e6a1f-108">O cmdlet **New-AzDataFactoryPipeline** cria um pipeline no Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="e6a1f-108">The **New-AzDataFactoryPipeline** cmdlet creates a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="e6a1f-109">Se você especificar um nome para um pipeline já existente, o cmdlet solicitará confirmação antes de substituir o pipeline.</span><span class="sxs-lookup"><span data-stu-id="e6a1f-109">If you specify a name for a pipeline that already exists, the cmdlet prompts you for confirmation before it replaces the pipeline.</span></span>
<span data-ttu-id="e6a1f-110">Se você especificar o parâmetro *Force* , o cmdlet substituirá o pipeline existente sem confirmação.</span><span class="sxs-lookup"><span data-stu-id="e6a1f-110">If you specify the *Force* parameter, the cmdlet replaces the existing pipeline without confirmation.</span></span>
<span data-ttu-id="e6a1f-111">Execute estas operações na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="e6a1f-111">Perform these operations in the following order:</span></span> 
- <span data-ttu-id="e6a1f-112">Criar uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="e6a1f-112">Create a data factory.</span></span> 
- <span data-ttu-id="e6a1f-113">Criar serviços vinculados.</span><span class="sxs-lookup"><span data-stu-id="e6a1f-113">Create linked services.</span></span> 
- <span data-ttu-id="e6a1f-114">Criar conjuntos de valores de valores.</span><span class="sxs-lookup"><span data-stu-id="e6a1f-114">Create datasets.</span></span> 
- <span data-ttu-id="e6a1f-115">Crie um pipeline.</span><span class="sxs-lookup"><span data-stu-id="e6a1f-115">Create a pipeline.</span></span>
<span data-ttu-id="e6a1f-116">Se um pipeline com o mesmo nome já existir na fábrica de dados, esse cmdlet solicitará que você confirme se deseja substituir o pipeline existente pelo novo pipeline.</span><span class="sxs-lookup"><span data-stu-id="e6a1f-116">If a pipeline with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing pipeline with the new pipeline.</span></span>
<span data-ttu-id="e6a1f-117">Se você confirmar para substituir o pipeline existente, a definição de pipeline também será substituída.</span><span class="sxs-lookup"><span data-stu-id="e6a1f-117">If you confirm to overwrite the existing pipeline, the pipeline definition is also replaced.</span></span>

## <span data-ttu-id="e6a1f-118">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e6a1f-118">EXAMPLES</span></span>

### <span data-ttu-id="e6a1f-119">Exemplo 1: criar um pipeline</span><span class="sxs-lookup"><span data-stu-id="e6a1f-119">Example 1: Create a pipeline</span></span>
```
PS C:\>New-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" -File "C:\DPWikisample.json" 
PipelineName      : DPWikisample
ResourceGroupName : ADF
DataFactoryName   : WikiADF11
Properties        : Microsoft.DataFactories.PipelineProperties
```

<span data-ttu-id="e6a1f-120">Esse comando cria um pipeline chamado DPWikisample na fábrica de dados chamado ADF.</span><span class="sxs-lookup"><span data-stu-id="e6a1f-120">This command creates a pipeline named DPWikisample in the data factory named ADF.</span></span>
<span data-ttu-id="e6a1f-121">O comando baseia o pipeline nas informações do DPWikisample.jsem arquivo.</span><span class="sxs-lookup"><span data-stu-id="e6a1f-121">The command bases the pipeline on information in the DPWikisample.json file.</span></span>
<span data-ttu-id="e6a1f-122">Esse arquivo inclui informações sobre atividades como atividades de cópia e atividades do HDInsight no pipeline.</span><span class="sxs-lookup"><span data-stu-id="e6a1f-122">This file includes information about activities such as Copy Activity and HDInsight Activity in the pipeline.</span></span>

## <span data-ttu-id="e6a1f-123">OS</span><span class="sxs-lookup"><span data-stu-id="e6a1f-123">PARAMETERS</span></span>

### <span data-ttu-id="e6a1f-124">-Datafactory</span><span class="sxs-lookup"><span data-stu-id="e6a1f-124">-DataFactory</span></span>
<span data-ttu-id="e6a1f-125">Especifica um objeto **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="e6a1f-125">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="e6a1f-126">Esse cmdlet cria um pipeline para a fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="e6a1f-126">This cmdlet creates a pipeline for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="e6a1f-127">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="e6a1f-127">-DataFactoryName</span></span>
<span data-ttu-id="e6a1f-128">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="e6a1f-128">Specifies the name of a data factory.</span></span>
<span data-ttu-id="e6a1f-129">Esse cmdlet cria um pipeline para a fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="e6a1f-129">This cmdlet creates a pipeline for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="e6a1f-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6a1f-130">-DefaultProfile</span></span>
<span data-ttu-id="e6a1f-131">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="e6a1f-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e6a1f-132">-Arquivo</span><span class="sxs-lookup"><span data-stu-id="e6a1f-132">-File</span></span>
<span data-ttu-id="e6a1f-133">Especifica o caminho completo do arquivo JSON (JavaScript Object Notation) que contém a descrição do pipeline.</span><span class="sxs-lookup"><span data-stu-id="e6a1f-133">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the pipeline.</span></span>

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

### <span data-ttu-id="e6a1f-134">-Force</span><span class="sxs-lookup"><span data-stu-id="e6a1f-134">-Force</span></span>
<span data-ttu-id="e6a1f-135">Indica que esse cmdlet substitui um pipeline existente sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="e6a1f-135">Indicates that this cmdlet replaces an existing pipeline without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="e6a1f-136">-Nome</span><span class="sxs-lookup"><span data-stu-id="e6a1f-136">-Name</span></span>
<span data-ttu-id="e6a1f-137">Especifica o nome do pipeline a ser criado.</span><span class="sxs-lookup"><span data-stu-id="e6a1f-137">Specifies the name of the pipeline to create.</span></span>

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

### <span data-ttu-id="e6a1f-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6a1f-138">-ResourceGroupName</span></span>
<span data-ttu-id="e6a1f-139">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="e6a1f-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="e6a1f-140">Esse cmdlet cria um pipeline para o grupo especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="e6a1f-140">This cmdlet creates a pipeline for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="e6a1f-141">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e6a1f-141">-Confirm</span></span>
<span data-ttu-id="e6a1f-142">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6a1f-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6a1f-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6a1f-143">-WhatIf</span></span>
<span data-ttu-id="e6a1f-144">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e6a1f-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6a1f-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e6a1f-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6a1f-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6a1f-146">CommonParameters</span></span>
<span data-ttu-id="e6a1f-147">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6a1f-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6a1f-148">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6a1f-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6a1f-149">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e6a1f-149">INPUTS</span></span>

### <span data-ttu-id="e6a1f-150">System. String</span><span class="sxs-lookup"><span data-stu-id="e6a1f-150">System.String</span></span>

### <span data-ttu-id="e6a1f-151">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="e6a1f-151">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="e6a1f-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e6a1f-152">OUTPUTS</span></span>

### <span data-ttu-id="e6a1f-153">Microsoft. Azure. Commands. datafactorings. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="e6a1f-153">Microsoft.Azure.Commands.DataFactories.Models.PSPipeline</span></span>

## <span data-ttu-id="e6a1f-154">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e6a1f-154">NOTES</span></span>
* <span data-ttu-id="e6a1f-155">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas</span><span class="sxs-lookup"><span data-stu-id="e6a1f-155">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="e6a1f-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e6a1f-156">RELATED LINKS</span></span>

[<span data-ttu-id="e6a1f-157">Get-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="e6a1f-157">Get-AzDataFactoryPipeline</span></span>](./Get-AzDataFactoryPipeline.md)

[<span data-ttu-id="e6a1f-158">Remove-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="e6a1f-158">Remove-AzDataFactoryPipeline</span></span>](./Remove-AzDataFactoryPipeline.md)

[<span data-ttu-id="e6a1f-159">Currículo-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="e6a1f-159">Resume-AzDataFactoryPipeline</span></span>](./Resume-AzDataFactoryPipeline.md)

[<span data-ttu-id="e6a1f-160">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="e6a1f-160">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="e6a1f-161">Suspender-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="e6a1f-161">Suspend-AzDataFactoryPipeline</span></span>](./Suspend-AzDataFactoryPipeline.md)


