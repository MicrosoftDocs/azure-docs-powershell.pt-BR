---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/invoke-azdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2Pipeline.md
ms.openlocfilehash: a8e75d6ef44453891660a7d5d35216dace346cb5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888272"
---
# <span data-ttu-id="4f912-101">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="4f912-101">Invoke-AzDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="4f912-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f912-102">SYNOPSIS</span></span>
  <span data-ttu-id="4f912-103">Invoca um pipeline para iniciar uma executar para ele.</span><span class="sxs-lookup"><span data-stu-id="4f912-103">Invokes a pipeline to start a run for it.</span></span>

## <span data-ttu-id="4f912-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="4f912-104">SYNTAX</span></span>

### <span data-ttu-id="4f912-105">ByFactoryNameByParameterFile (Padrão)</span><span class="sxs-lookup"><span data-stu-id="4f912-105">ByFactoryNameByParameterFile (Default)</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-ParameterFile] <String>] [[-ReferencePipelineRunId] <String>] [-IsRecovery]
 [[-StartActivityName] <String>] [-StartFromFailure] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f912-106">ByPipelineObjectByParameterFile</span><span class="sxs-lookup"><span data-stu-id="4f912-106">ByPipelineObjectByParameterFile</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-ParameterFile] <String>]
 [[-ReferencePipelineRunId] <String>] [-IsRecovery] [[-StartActivityName] <String>] [-StartFromFailure]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f912-107">ByPipelineObjectByParameterObject</span><span class="sxs-lookup"><span data-stu-id="4f912-107">ByPipelineObjectByParameterObject</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-Parameter] <Hashtable>]
 [[-ReferencePipelineRunId] <String>] [-IsRecovery] [[-StartActivityName] <String>] [-StartFromFailure]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f912-108">ByFactoryNameByParameterObject</span><span class="sxs-lookup"><span data-stu-id="4f912-108">ByFactoryNameByParameterObject</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-Parameter] <Hashtable>] [[-ReferencePipelineRunId] <String>] [-IsRecovery]
 [[-StartActivityName] <String>] [-StartFromFailure] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f912-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="4f912-109">DESCRIPTION</span></span>
<span data-ttu-id="4f912-110">O **comando Invoke-AzDataFactoryV2Pipeline** inicia uma executar no pipeline especificado e retorna uma ID para essa executar.</span><span class="sxs-lookup"><span data-stu-id="4f912-110">The **Invoke-AzDataFactoryV2Pipeline** command starts a run on the specified pipeline and returns a ID for that run.</span></span> <span data-ttu-id="4f912-111">Esse GUID pode ser passado **para Get-AzDataFactoryV2PipelineRun** ou **Get-AzDataFactoryV2ActivityRun** para obter mais detalhes sobre essa executar.</span><span class="sxs-lookup"><span data-stu-id="4f912-111">This GUID can be passed to **Get-AzDataFactoryV2PipelineRun** or **Get-AzDataFactoryV2ActivityRun** to obtain further details about this run.</span></span>

## <span data-ttu-id="4f912-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4f912-112">EXAMPLES</span></span>

### <span data-ttu-id="4f912-113">Exemplo 1: invocar um pipeline para iniciar uma executar</span><span class="sxs-lookup"><span data-stu-id="4f912-113">Example 1: Invoke a pipeline to start a run</span></span>
```powershell
PS C:\> Invoke-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineName "DPWikisample"
867d9d9f-1efc-4fee-974d-d8e6320bfbcb
```

<span data-ttu-id="4f912-114">Este comando inicia uma executar o pipeline "DPWikisample" na fábrica "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="4f912-114">This command starts a run for "DPWikisample" pipeline in the "WikiADF" factory.</span></span>

### <span data-ttu-id="4f912-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="4f912-115">Example 2</span></span>

<span data-ttu-id="4f912-116">Invoca um pipeline para iniciar uma executar para ele.</span><span class="sxs-lookup"><span data-stu-id="4f912-116">Invokes a pipeline to start a run for it.</span></span> <span data-ttu-id="4f912-117">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="4f912-117">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Invoke-AzDataFactoryV2Pipeline -DataFactoryName 'WikiADF' -Parameter <Hashtable> -PipelineName 'DPWikisample' -ResourceGroupName 'ADF'
```

## <span data-ttu-id="4f912-118">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="4f912-118">PARAMETERS</span></span>

### <span data-ttu-id="4f912-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="4f912-119">-DataFactoryName</span></span>
<span data-ttu-id="4f912-120">O nome da fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="4f912-120">The data factory name.</span></span>

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

### <span data-ttu-id="4f912-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f912-121">-DefaultProfile</span></span>
<span data-ttu-id="4f912-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="4f912-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4f912-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4f912-123">-InputObject</span></span>
<span data-ttu-id="4f912-124">O objeto de fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="4f912-124">The data factory object.</span></span>

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

### <span data-ttu-id="4f912-125">-IsRecovery</span><span class="sxs-lookup"><span data-stu-id="4f912-125">-IsRecovery</span></span>
<span data-ttu-id="4f912-126">Sinalizador do modo de recuperação.</span><span class="sxs-lookup"><span data-stu-id="4f912-126">Recovery mode flag.</span></span> <span data-ttu-id="4f912-127">Se o modo de recuperação for definido como true, o pipeline referenciado especificado será executado e a nova executar será agrupada sob o mesmo groupId.</span><span class="sxs-lookup"><span data-stu-id="4f912-127">If recovery mode is set to true, the specified referenced pipeline run and the new run will be grouped under the same groupId.</span></span>

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

### <span data-ttu-id="4f912-128">-Parameter</span><span class="sxs-lookup"><span data-stu-id="4f912-128">-Parameter</span></span>
<span data-ttu-id="4f912-129">Parâmetros para a operação do pipeline.</span><span class="sxs-lookup"><span data-stu-id="4f912-129">Parameters for pipeline run.</span></span>

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

### <span data-ttu-id="4f912-130">-ParameterFile</span><span class="sxs-lookup"><span data-stu-id="4f912-130">-ParameterFile</span></span>
<span data-ttu-id="4f912-131">O nome do arquivo com parâmetros para a operação de pipeline.</span><span class="sxs-lookup"><span data-stu-id="4f912-131">The name of the file with parameters for pipeline run.</span></span>

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

### <span data-ttu-id="4f912-132">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="4f912-132">-PipelineName</span></span>
<span data-ttu-id="4f912-133">O nome do pipeline.</span><span class="sxs-lookup"><span data-stu-id="4f912-133">The pipeline name.</span></span>

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

### <span data-ttu-id="4f912-134">-ReferencePipelineRunId</span><span class="sxs-lookup"><span data-stu-id="4f912-134">-ReferencePipelineRunId</span></span>
<span data-ttu-id="4f912-135">A ID de executar pipeline para reprise.</span><span class="sxs-lookup"><span data-stu-id="4f912-135">The pipeline run ID for rerun.</span></span> <span data-ttu-id="4f912-136">Se a ID de executar for especificada, os parâmetros da executar especificada serão usados para criar uma nova executar.</span><span class="sxs-lookup"><span data-stu-id="4f912-136">If run ID is specified, the parameters of the specified run will be used to create a new run.</span></span>

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

### <span data-ttu-id="4f912-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f912-137">-ResourceGroupName</span></span>
<span data-ttu-id="4f912-138">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4f912-138">The resource group name.</span></span>

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

### <span data-ttu-id="4f912-139">-StartActivityName</span><span class="sxs-lookup"><span data-stu-id="4f912-139">-StartActivityName</span></span>
<span data-ttu-id="4f912-140">No modo de recuperação, a reprise iniciará a partir dessa atividade.</span><span class="sxs-lookup"><span data-stu-id="4f912-140">In recovery mode, the rerun will start from this activity.</span></span> <span data-ttu-id="4f912-141">Se não for especificado, todas as atividades serão executados.</span><span class="sxs-lookup"><span data-stu-id="4f912-141">If not specified, all activities will run.</span></span>

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

### <span data-ttu-id="4f912-142">-StartFromFailure</span><span class="sxs-lookup"><span data-stu-id="4f912-142">-StartFromFailure</span></span>
<span data-ttu-id="4f912-143">Inicie a reprise do sinalizador de atividades com falha.</span><span class="sxs-lookup"><span data-stu-id="4f912-143">Start rerun from failed activities flag.</span></span> <span data-ttu-id="4f912-144">No modo de recuperação, se especificado, a reprise iniciará de atividades com falha.</span><span class="sxs-lookup"><span data-stu-id="4f912-144">In recovery mode, if specified, the rerun will start from failed activities.</span></span>

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

### <span data-ttu-id="4f912-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4f912-145">-Confirm</span></span>
<span data-ttu-id="4f912-146">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4f912-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f912-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f912-147">-WhatIf</span></span>
<span data-ttu-id="4f912-148">Mostra o que acontece se o cmdlet for executado, mas não executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4f912-148">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="4f912-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f912-149">CommonParameters</span></span>
<span data-ttu-id="4f912-150">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f912-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f912-151">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4f912-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f912-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4f912-152">INPUTS</span></span>

### <span data-ttu-id="4f912-153">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span><span class="sxs-lookup"><span data-stu-id="4f912-153">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

### <span data-ttu-id="4f912-154">System.String</span><span class="sxs-lookup"><span data-stu-id="4f912-154">System.String</span></span>

### <span data-ttu-id="4f912-155">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="4f912-155">System.Collections.Hashtable</span></span>

## <span data-ttu-id="4f912-156">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="4f912-156">OUTPUTS</span></span>

### <span data-ttu-id="4f912-157">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span><span class="sxs-lookup"><span data-stu-id="4f912-157">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="4f912-158">NOTES</span><span class="sxs-lookup"><span data-stu-id="4f912-158">NOTES</span></span>

## <span data-ttu-id="4f912-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4f912-159">RELATED LINKS</span></span>

[<span data-ttu-id="4f912-160">Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="4f912-160">Get-AzDataFactoryV2PipelineRun</span></span>]()

[<span data-ttu-id="4f912-161">Get-AzDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="4f912-161">Get-AzDataFactoryV2ActivityRun</span></span>]()

