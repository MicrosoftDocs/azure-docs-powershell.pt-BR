---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/invoke-azdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2Pipeline.md
ms.openlocfilehash: e4204068b12a21732cca1802dcc20a770d74d5e0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98429897"
---
# <span data-ttu-id="b62a1-101">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="b62a1-101">Invoke-AzDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="b62a1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b62a1-102">SYNOPSIS</span></span>
  <span data-ttu-id="b62a1-103">Invoca um pipeline para iniciar uma execução para ele.</span><span class="sxs-lookup"><span data-stu-id="b62a1-103">Invokes a pipeline to start a run for it.</span></span>

## <span data-ttu-id="b62a1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b62a1-104">SYNTAX</span></span>

### <span data-ttu-id="b62a1-105">ByFactoryNameByParameterFile (padrão)</span><span class="sxs-lookup"><span data-stu-id="b62a1-105">ByFactoryNameByParameterFile (Default)</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-ParameterFile] <String>] [[-ReferencePipelineRunId] <String>] [-IsRecovery]
 [[-StartActivityName] <String>] [-StartFromFailure] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b62a1-106">ByPipelineObjectByParameterFile</span><span class="sxs-lookup"><span data-stu-id="b62a1-106">ByPipelineObjectByParameterFile</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-ParameterFile] <String>]
 [[-ReferencePipelineRunId] <String>] [-IsRecovery] [[-StartActivityName] <String>] [-StartFromFailure]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b62a1-107">ByPipelineObjectByParameterObject</span><span class="sxs-lookup"><span data-stu-id="b62a1-107">ByPipelineObjectByParameterObject</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-Parameter] <Hashtable>]
 [[-ReferencePipelineRunId] <String>] [-IsRecovery] [[-StartActivityName] <String>] [-StartFromFailure]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b62a1-108">ByFactoryNameByParameterObject</span><span class="sxs-lookup"><span data-stu-id="b62a1-108">ByFactoryNameByParameterObject</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-Parameter] <Hashtable>] [[-ReferencePipelineRunId] <String>] [-IsRecovery]
 [[-StartActivityName] <String>] [-StartFromFailure] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b62a1-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b62a1-109">DESCRIPTION</span></span>
<span data-ttu-id="b62a1-110">O comando **Invoke-AzDataFactoryV2Pipeline** inicia uma execução no pipeline especificado e retorna uma ID para essa execução.</span><span class="sxs-lookup"><span data-stu-id="b62a1-110">The **Invoke-AzDataFactoryV2Pipeline** command starts a run on the specified pipeline and returns a ID for that run.</span></span> <span data-ttu-id="b62a1-111">Esse GUID pode ser passado para **Get-AzDataFactoryV2PipelineRun** ou **Get-AzDataFactoryV2ActivityRun** para obter mais detalhes sobre essa execução.</span><span class="sxs-lookup"><span data-stu-id="b62a1-111">This GUID can be passed to **Get-AzDataFactoryV2PipelineRun** or **Get-AzDataFactoryV2ActivityRun** to obtain further details about this run.</span></span>

## <span data-ttu-id="b62a1-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b62a1-112">EXAMPLES</span></span>

### <span data-ttu-id="b62a1-113">Exemplo 1: invocar um pipeline para iniciar uma execução</span><span class="sxs-lookup"><span data-stu-id="b62a1-113">Example 1: Invoke a pipeline to start a run</span></span>
```powershell
PS C:\> Invoke-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineName "DPWikisample"
867d9d9f-1efc-4fee-974d-d8e6320bfbcb
```

<span data-ttu-id="b62a1-114">Esse comando inicia uma execução para o pipeline "DPWikisample" na fábrica "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="b62a1-114">This command starts a run for "DPWikisample" pipeline in the "WikiADF" factory.</span></span>

### <span data-ttu-id="b62a1-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="b62a1-115">Example 2</span></span>

<span data-ttu-id="b62a1-116">Invoca um pipeline para iniciar uma execução para ele.</span><span class="sxs-lookup"><span data-stu-id="b62a1-116">Invokes a pipeline to start a run for it.</span></span> <span data-ttu-id="b62a1-117">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="b62a1-117">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Invoke-AzDataFactoryV2Pipeline -DataFactoryName 'WikiADF' -Parameter <Hashtable> -PipelineName 'DPWikisample' -ResourceGroupName 'ADF'
```

## <span data-ttu-id="b62a1-118">OS</span><span class="sxs-lookup"><span data-stu-id="b62a1-118">PARAMETERS</span></span>

### <span data-ttu-id="b62a1-119">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="b62a1-119">-DataFactoryName</span></span>
<span data-ttu-id="b62a1-120">O nome do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="b62a1-120">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryNameByParameterFile, ByFactoryNameByParameterObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b62a1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b62a1-121">-DefaultProfile</span></span>
<span data-ttu-id="b62a1-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b62a1-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b62a1-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b62a1-123">-InputObject</span></span>
<span data-ttu-id="b62a1-124">O objeto de fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="b62a1-124">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline
Parameter Sets: ByPipelineObjectByParameterFile, ByPipelineObjectByParameterObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b62a1-125">-Isrecovery</span><span class="sxs-lookup"><span data-stu-id="b62a1-125">-IsRecovery</span></span>
<span data-ttu-id="b62a1-126">Sinalizador do modo de recuperação.</span><span class="sxs-lookup"><span data-stu-id="b62a1-126">Recovery mode flag.</span></span> <span data-ttu-id="b62a1-127">Se o modo de recuperação for definido como verdadeiro, o pipeline Referenciado especificado e a nova execução serão agrupados sob o mesmo GroupId.</span><span class="sxs-lookup"><span data-stu-id="b62a1-127">If recovery mode is set to true, the specified referenced pipeline run and the new run will be grouped under the same groupId.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b62a1-128">-Parâmetro</span><span class="sxs-lookup"><span data-stu-id="b62a1-128">-Parameter</span></span>
<span data-ttu-id="b62a1-129">Parâmetros para a execução de pipeline.</span><span class="sxs-lookup"><span data-stu-id="b62a1-129">Parameters for pipeline run.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByPipelineObjectByParameterObject, ByFactoryNameByParameterObject
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b62a1-130">-Parameterfile</span><span class="sxs-lookup"><span data-stu-id="b62a1-130">-ParameterFile</span></span>
<span data-ttu-id="b62a1-131">O nome do arquivo com parâmetros para execução de pipeline.</span><span class="sxs-lookup"><span data-stu-id="b62a1-131">The name of the file with parameters for pipeline run.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryNameByParameterFile, ByPipelineObjectByParameterFile
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b62a1-132">-Pipelinename</span><span class="sxs-lookup"><span data-stu-id="b62a1-132">-PipelineName</span></span>
<span data-ttu-id="b62a1-133">O nome do pipeline.</span><span class="sxs-lookup"><span data-stu-id="b62a1-133">The pipeline name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryNameByParameterFile, ByFactoryNameByParameterObject
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b62a1-134">-ReferencePipelineRunId</span><span class="sxs-lookup"><span data-stu-id="b62a1-134">-ReferencePipelineRunId</span></span>
<span data-ttu-id="b62a1-135">A ID de execução do pipeline para executar novamente.</span><span class="sxs-lookup"><span data-stu-id="b62a1-135">The pipeline run ID for rerun.</span></span> <span data-ttu-id="b62a1-136">Se a ID de execução for especificada, os parâmetros da execução especificada serão usados para criar uma nova execução.</span><span class="sxs-lookup"><span data-stu-id="b62a1-136">If run ID is specified, the parameters of the specified run will be used to create a new run.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b62a1-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b62a1-137">-ResourceGroupName</span></span>
<span data-ttu-id="b62a1-138">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b62a1-138">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryNameByParameterFile, ByFactoryNameByParameterObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b62a1-139">-StartActivityName</span><span class="sxs-lookup"><span data-stu-id="b62a1-139">-StartActivityName</span></span>
<span data-ttu-id="b62a1-140">No modo de recuperação, o reinício será iniciado a partir dessa atividade.</span><span class="sxs-lookup"><span data-stu-id="b62a1-140">In recovery mode, the rerun will start from this activity.</span></span> <span data-ttu-id="b62a1-141">Se não for especificado, todas as atividades serão executadas.</span><span class="sxs-lookup"><span data-stu-id="b62a1-141">If not specified, all activities will run.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b62a1-142">-StartFromFailure</span><span class="sxs-lookup"><span data-stu-id="b62a1-142">-StartFromFailure</span></span>
<span data-ttu-id="b62a1-143">Comece a executar novamente a partir de um sinalizador de atividades com falha.</span><span class="sxs-lookup"><span data-stu-id="b62a1-143">Start rerun from failed activities flag.</span></span> <span data-ttu-id="b62a1-144">No modo de recuperação, se especificado, o reinício de atividades com falha será iniciado.</span><span class="sxs-lookup"><span data-stu-id="b62a1-144">In recovery mode, if specified, the rerun will start from failed activities.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b62a1-145">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b62a1-145">-Confirm</span></span>
<span data-ttu-id="b62a1-146">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b62a1-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b62a1-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b62a1-147">-WhatIf</span></span>
<span data-ttu-id="b62a1-148">Mostra o que acontece se o cmdlet for executado, mas não executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b62a1-148">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="b62a1-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b62a1-149">CommonParameters</span></span>
<span data-ttu-id="b62a1-150">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b62a1-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b62a1-151">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b62a1-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b62a1-152">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b62a1-152">INPUTS</span></span>

### <span data-ttu-id="b62a1-153">Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="b62a1-153">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

### <span data-ttu-id="b62a1-154">System. String</span><span class="sxs-lookup"><span data-stu-id="b62a1-154">System.String</span></span>

### <span data-ttu-id="b62a1-155">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="b62a1-155">System.Collections.Hashtable</span></span>

## <span data-ttu-id="b62a1-156">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b62a1-156">OUTPUTS</span></span>

### <span data-ttu-id="b62a1-157">Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="b62a1-157">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="b62a1-158">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b62a1-158">NOTES</span></span>

## <span data-ttu-id="b62a1-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b62a1-159">RELATED LINKS</span></span>

[<span data-ttu-id="b62a1-160">Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="b62a1-160">Get-AzDataFactoryV2PipelineRun</span></span>]()

[<span data-ttu-id="b62a1-161">Get-AzDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="b62a1-161">Get-AzDataFactoryV2ActivityRun</span></span>]()

