---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 30C1AF6C-A8DC-4CA0-9E5F-10641A29D0E8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/new-azurermdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryPipeline.md
ms.openlocfilehash: 7ad7eb0f87972c3a64b3fb966259d25d527c20c1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428516"
---
# <span data-ttu-id="2acdd-101">New-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="2acdd-101">New-AzureRmDataFactoryPipeline</span></span>

## <span data-ttu-id="2acdd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2acdd-102">SYNOPSIS</span></span>
<span data-ttu-id="2acdd-103">Cria um pipeline na fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="2acdd-103">Creates a pipeline in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2acdd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2acdd-104">SYNTAX</span></span>

### <span data-ttu-id="2acdd-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="2acdd-105">ByFactoryName (Default)</span></span>
```
New-AzureRmDataFactoryPipeline [[-Name] <String>] [-DataFactoryName] <String> [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2acdd-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="2acdd-106">ByFactoryObject</span></span>
```
New-AzureRmDataFactoryPipeline [[-Name] <String>] [-DataFactory] <PSDataFactory> [-File] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2acdd-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2acdd-107">DESCRIPTION</span></span>
<span data-ttu-id="2acdd-108">O cmdlet **New-AzureRmDataFactoryPipeline** cria um pipeline no Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="2acdd-108">The **New-AzureRmDataFactoryPipeline** cmdlet creates a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="2acdd-109">Se você especificar um nome para um pipeline já existente, o cmdlet solicitará confirmação antes de substituir o pipeline.</span><span class="sxs-lookup"><span data-stu-id="2acdd-109">If you specify a name for a pipeline that already exists, the cmdlet prompts you for confirmation before it replaces the pipeline.</span></span>
<span data-ttu-id="2acdd-110">Se você especificar o parâmetro *Force* , o cmdlet substituirá o pipeline existente sem confirmação.</span><span class="sxs-lookup"><span data-stu-id="2acdd-110">If you specify the *Force* parameter, the cmdlet replaces the existing pipeline without confirmation.</span></span>
<span data-ttu-id="2acdd-111">Execute estas operações na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="2acdd-111">Perform these operations in the following order:</span></span> 
- <span data-ttu-id="2acdd-112">Criar uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="2acdd-112">Create a data factory.</span></span> 
- <span data-ttu-id="2acdd-113">Criar serviços vinculados.</span><span class="sxs-lookup"><span data-stu-id="2acdd-113">Create linked services.</span></span> 
- <span data-ttu-id="2acdd-114">Criar conjuntos de valores de valores.</span><span class="sxs-lookup"><span data-stu-id="2acdd-114">Create datasets.</span></span> 
- <span data-ttu-id="2acdd-115">Crie um pipeline.</span><span class="sxs-lookup"><span data-stu-id="2acdd-115">Create a pipeline.</span></span>
<span data-ttu-id="2acdd-116">Se um pipeline com o mesmo nome já existir na fábrica de dados, esse cmdlet solicitará que você confirme se deseja substituir o pipeline existente pelo novo pipeline.</span><span class="sxs-lookup"><span data-stu-id="2acdd-116">If a pipeline with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing pipeline with the new pipeline.</span></span>
<span data-ttu-id="2acdd-117">Se você confirmar para substituir o pipeline existente, a definição de pipeline também será substituída.</span><span class="sxs-lookup"><span data-stu-id="2acdd-117">If you confirm to overwrite the existing pipeline, the pipeline definition is also replaced.</span></span>

## <span data-ttu-id="2acdd-118">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2acdd-118">EXAMPLES</span></span>

### <span data-ttu-id="2acdd-119">Exemplo 1: criar um pipeline</span><span class="sxs-lookup"><span data-stu-id="2acdd-119">Example 1: Create a pipeline</span></span>
```
PS C:\>New-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" -File "C:\DPWikisample.json" 
PipelineName      : DPWikisample
ResourceGroupName : ADF
DataFactoryName   : WikiADF11
Properties        : Microsoft.DataFactories.PipelineProperties
```

<span data-ttu-id="2acdd-120">Esse comando cria um pipeline chamado DPWikisample na fábrica de dados chamado ADF.</span><span class="sxs-lookup"><span data-stu-id="2acdd-120">This command creates a pipeline named DPWikisample in the data factory named ADF.</span></span>
<span data-ttu-id="2acdd-121">O comando baseia o pipeline nas informações do DPWikisample.jsem arquivo.</span><span class="sxs-lookup"><span data-stu-id="2acdd-121">The command bases the pipeline on information in the DPWikisample.json file.</span></span>
<span data-ttu-id="2acdd-122">Esse arquivo inclui informações sobre atividades como atividades de cópia e atividades do HDInsight no pipeline.</span><span class="sxs-lookup"><span data-stu-id="2acdd-122">This file includes information about activities such as Copy Activity and HDInsight Activity in the pipeline.</span></span>

## <span data-ttu-id="2acdd-123">OS</span><span class="sxs-lookup"><span data-stu-id="2acdd-123">PARAMETERS</span></span>

### <span data-ttu-id="2acdd-124">-Datafactory</span><span class="sxs-lookup"><span data-stu-id="2acdd-124">-DataFactory</span></span>
<span data-ttu-id="2acdd-125">Especifica um objeto **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="2acdd-125">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="2acdd-126">Esse cmdlet cria um pipeline para a fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="2acdd-126">This cmdlet creates a pipeline for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="2acdd-127">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="2acdd-127">-DataFactoryName</span></span>
<span data-ttu-id="2acdd-128">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="2acdd-128">Specifies the name of a data factory.</span></span>
<span data-ttu-id="2acdd-129">Esse cmdlet cria um pipeline para a fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="2acdd-129">This cmdlet creates a pipeline for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="2acdd-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2acdd-130">-DefaultProfile</span></span>
<span data-ttu-id="2acdd-131">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="2acdd-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2acdd-132">-Arquivo</span><span class="sxs-lookup"><span data-stu-id="2acdd-132">-File</span></span>
<span data-ttu-id="2acdd-133">Especifica o caminho completo do arquivo JSON (JavaScript Object Notation) que contém a descrição do pipeline.</span><span class="sxs-lookup"><span data-stu-id="2acdd-133">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the pipeline.</span></span>

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

### <span data-ttu-id="2acdd-134">-Force</span><span class="sxs-lookup"><span data-stu-id="2acdd-134">-Force</span></span>
<span data-ttu-id="2acdd-135">Indica que esse cmdlet substitui um pipeline existente sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="2acdd-135">Indicates that this cmdlet replaces an existing pipeline without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="2acdd-136">-Nome</span><span class="sxs-lookup"><span data-stu-id="2acdd-136">-Name</span></span>
<span data-ttu-id="2acdd-137">Especifica o nome do pipeline a ser criado.</span><span class="sxs-lookup"><span data-stu-id="2acdd-137">Specifies the name of the pipeline to create.</span></span>

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

### <span data-ttu-id="2acdd-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2acdd-138">-ResourceGroupName</span></span>
<span data-ttu-id="2acdd-139">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="2acdd-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="2acdd-140">Esse cmdlet cria um pipeline para o grupo especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="2acdd-140">This cmdlet creates a pipeline for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="2acdd-141">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2acdd-141">-Confirm</span></span>
<span data-ttu-id="2acdd-142">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2acdd-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2acdd-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2acdd-143">-WhatIf</span></span>
<span data-ttu-id="2acdd-144">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2acdd-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2acdd-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2acdd-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2acdd-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2acdd-146">CommonParameters</span></span>
<span data-ttu-id="2acdd-147">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2acdd-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2acdd-148">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2acdd-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2acdd-149">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2acdd-149">INPUTS</span></span>

### <span data-ttu-id="2acdd-150">System. String</span><span class="sxs-lookup"><span data-stu-id="2acdd-150">System.String</span></span>

### <span data-ttu-id="2acdd-151">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="2acdd-151">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="2acdd-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2acdd-152">OUTPUTS</span></span>

### <span data-ttu-id="2acdd-153">Microsoft. Azure. Commands. datafactorings. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="2acdd-153">Microsoft.Azure.Commands.DataFactories.Models.PSPipeline</span></span>

## <span data-ttu-id="2acdd-154">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2acdd-154">NOTES</span></span>
* <span data-ttu-id="2acdd-155">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas</span><span class="sxs-lookup"><span data-stu-id="2acdd-155">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="2acdd-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2acdd-156">RELATED LINKS</span></span>

[<span data-ttu-id="2acdd-157">Get-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="2acdd-157">Get-AzureRmDataFactoryPipeline</span></span>](./Get-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="2acdd-158">Remove-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="2acdd-158">Remove-AzureRmDataFactoryPipeline</span></span>](./Remove-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="2acdd-159">Currículo-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="2acdd-159">Resume-AzureRmDataFactoryPipeline</span></span>](./Resume-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="2acdd-160">Set-AzureRmDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="2acdd-160">Set-AzureRmDataFactoryPipelineActivePeriod</span></span>](./Set-AzureRmDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="2acdd-161">Suspender-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="2acdd-161">Suspend-AzureRmDataFactoryPipeline</span></span>](./Suspend-AzureRmDataFactoryPipeline.md)


