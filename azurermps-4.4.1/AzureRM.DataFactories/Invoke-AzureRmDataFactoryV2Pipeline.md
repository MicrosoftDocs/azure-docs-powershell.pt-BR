---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Invoke-AzureRmDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Invoke-AzureRmDataFactoryV2Pipeline.md
ms.openlocfilehash: a7486c3fc50e5c6517022190e05d099329fc6001
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430754"
---
# <span data-ttu-id="e93bb-101">Invoke-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="e93bb-101">Invoke-AzureRmDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="e93bb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e93bb-102">SYNOPSIS</span></span>
  <span data-ttu-id="e93bb-103">Invoca um pipeline para iniciar uma execução para ele.</span><span class="sxs-lookup"><span data-stu-id="e93bb-103">Invokes a pipeline to start a run for it.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e93bb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e93bb-104">SYNTAX</span></span>

### <span data-ttu-id="e93bb-105">ByFactoryNameByParameterFile (padrão)</span><span class="sxs-lookup"><span data-stu-id="e93bb-105">ByFactoryNameByParameterFile (Default)</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-ParameterFile] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e93bb-106">ByPipelineObjectByParameterFile</span><span class="sxs-lookup"><span data-stu-id="e93bb-106">ByPipelineObjectByParameterFile</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-ParameterFile] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e93bb-107">ByPipelineObjectByParameterObject</span><span class="sxs-lookup"><span data-stu-id="e93bb-107">ByPipelineObjectByParameterObject</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-Parameter] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e93bb-108">ByFactoryNameByParameterObject</span><span class="sxs-lookup"><span data-stu-id="e93bb-108">ByFactoryNameByParameterObject</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-Parameter] <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e93bb-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e93bb-109">DESCRIPTION</span></span>
<span data-ttu-id="e93bb-110">O comando **Invoke-AzureRmDataFactoryV2Pipeline** inicia uma execução no pipeline especificado e retorna uma ID para essa execução.</span><span class="sxs-lookup"><span data-stu-id="e93bb-110">The **Invoke-AzureRmDataFactoryV2Pipeline** command starts a run on the specified pipeline and returns a ID for that run.</span></span> <span data-ttu-id="e93bb-111">Esse GUID pode ser passado para **Get-AzureRmDataFactoryV2PipelineRun** ou **Get-AzureRmDataFactoryV2ActivityRun** para obter mais detalhes sobre essa execução.</span><span class="sxs-lookup"><span data-stu-id="e93bb-111">This GUID can be passed to **Get-AzureRmDataFactoryV2PipelineRun** or **Get-AzureRmDataFactoryV2ActivityRun** to obtain further details about this run.</span></span>

## <span data-ttu-id="e93bb-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e93bb-112">EXAMPLES</span></span>

### <span data-ttu-id="e93bb-113">Exemplo 1: invocar um pipeline para iniciar uma execução</span><span class="sxs-lookup"><span data-stu-id="e93bb-113">Example 1: Invoke a pipeline to start a run</span></span>
```
PS C:\> Invoke-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineName "DPWikisample"
867d9d9f-1efc-4fee-974d-d8e6320bfbcb
```

<span data-ttu-id="e93bb-114">Esse comando inicia uma execução para o pipeline "DPWikisample" na fábrica "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="e93bb-114">This command starts a run for "DPWikisample" pipeline in the "WikiADF" factory.</span></span>

## <span data-ttu-id="e93bb-115">OS</span><span class="sxs-lookup"><span data-stu-id="e93bb-115">PARAMETERS</span></span>

### <span data-ttu-id="e93bb-116">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e93bb-116">-Confirm</span></span>
<span data-ttu-id="e93bb-117">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e93bb-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e93bb-118">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="e93bb-118">-DataFactoryName</span></span>
<span data-ttu-id="e93bb-119">O nome do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="e93bb-119">The data factory name.</span></span>

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

### <span data-ttu-id="e93bb-120">-Parameterfile</span><span class="sxs-lookup"><span data-stu-id="e93bb-120">-ParameterFile</span></span>
<span data-ttu-id="e93bb-121">O nome do arquivo com parâmetros para execução de pipeline.</span><span class="sxs-lookup"><span data-stu-id="e93bb-121">The name of the file with parameters for pipeline run.</span></span>

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

### <span data-ttu-id="e93bb-122">-Parâmetro</span><span class="sxs-lookup"><span data-stu-id="e93bb-122">-Parameter</span></span>
<span data-ttu-id="e93bb-123">Parâmetros para a execução de pipeline.</span><span class="sxs-lookup"><span data-stu-id="e93bb-123">Parameters for pipeline run.</span></span>

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

### <span data-ttu-id="e93bb-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e93bb-124">-InputObject</span></span>
<span data-ttu-id="e93bb-125">O objeto de fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="e93bb-125">The data factory object.</span></span>

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

### <span data-ttu-id="e93bb-126">-Pipelinename</span><span class="sxs-lookup"><span data-stu-id="e93bb-126">-PipelineName</span></span>
<span data-ttu-id="e93bb-127">O nome do pipeline.</span><span class="sxs-lookup"><span data-stu-id="e93bb-127">The pipeline name.</span></span>

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

### <span data-ttu-id="e93bb-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e93bb-128">-ResourceGroupName</span></span>
<span data-ttu-id="e93bb-129">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e93bb-129">The resource group name.</span></span>

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

### <span data-ttu-id="e93bb-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e93bb-130">-WhatIf</span></span>
<span data-ttu-id="e93bb-131">Mostra o que acontece se o cmdlet for executado, mas não executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e93bb-131">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="e93bb-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e93bb-132">-DefaultProfile</span></span>
<span data-ttu-id="e93bb-133">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e93bb-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e93bb-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e93bb-134">CommonParameters</span></span>
<span data-ttu-id="e93bb-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e93bb-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e93bb-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e93bb-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e93bb-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e93bb-137">INPUTS</span></span>

### <span data-ttu-id="e93bb-138">Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="e93bb-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>
<span data-ttu-id="e93bb-139">System. String System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e93bb-139">System.String System.Collections.Hashtable</span></span>

## <span data-ttu-id="e93bb-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e93bb-140">OUTPUTS</span></span>

### <span data-ttu-id="e93bb-141">Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="e93bb-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="e93bb-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e93bb-142">NOTES</span></span>

## <span data-ttu-id="e93bb-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e93bb-143">RELATED LINKS</span></span>

[<span data-ttu-id="e93bb-144">Get-AzureRmDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="e93bb-144">Get-AzureRmDataFactoryV2PipelineRun</span></span>]()

[<span data-ttu-id="e93bb-145">Get-AzureRmDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="e93bb-145">Get-AzureRmDataFactoryV2ActivityRun</span></span>]()

