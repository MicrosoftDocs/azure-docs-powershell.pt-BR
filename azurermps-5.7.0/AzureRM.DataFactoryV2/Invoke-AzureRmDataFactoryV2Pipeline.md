---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/invoke-azurermdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Invoke-AzureRmDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Invoke-AzureRmDataFactoryV2Pipeline.md
ms.openlocfilehash: 1503d7307c38c72eece2eb7cb3d6e9f1543be8bf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610405"
---
# <span data-ttu-id="b95be-101">Invoke-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="b95be-101">Invoke-AzureRmDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="b95be-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b95be-102">SYNOPSIS</span></span>
  <span data-ttu-id="b95be-103">Invoca um pipeline para iniciar uma execução para ele.</span><span class="sxs-lookup"><span data-stu-id="b95be-103">Invokes a pipeline to start a run for it.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b95be-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b95be-104">SYNTAX</span></span>

### <span data-ttu-id="b95be-105">ByFactoryNameByParameterFile (padrão)</span><span class="sxs-lookup"><span data-stu-id="b95be-105">ByFactoryNameByParameterFile (Default)</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-ParameterFile] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b95be-106">ByPipelineObjectByParameterFile</span><span class="sxs-lookup"><span data-stu-id="b95be-106">ByPipelineObjectByParameterFile</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-ParameterFile] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b95be-107">ByPipelineObjectByParameterObject</span><span class="sxs-lookup"><span data-stu-id="b95be-107">ByPipelineObjectByParameterObject</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-Parameter] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b95be-108">ByFactoryNameByParameterObject</span><span class="sxs-lookup"><span data-stu-id="b95be-108">ByFactoryNameByParameterObject</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-Parameter] <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b95be-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b95be-109">DESCRIPTION</span></span>
<span data-ttu-id="b95be-110">O comando **Invoke-AzureRmDataFactoryV2Pipeline** inicia uma execução no pipeline especificado e retorna uma ID para essa execução.</span><span class="sxs-lookup"><span data-stu-id="b95be-110">The **Invoke-AzureRmDataFactoryV2Pipeline** command starts a run on the specified pipeline and returns a ID for that run.</span></span> <span data-ttu-id="b95be-111">Esse GUID pode ser passado para **Get-AzureRmDataFactoryV2PipelineRun** ou **Get-AzureRmDataFactoryV2ActivityRun** para obter mais detalhes sobre essa execução.</span><span class="sxs-lookup"><span data-stu-id="b95be-111">This GUID can be passed to **Get-AzureRmDataFactoryV2PipelineRun** or **Get-AzureRmDataFactoryV2ActivityRun** to obtain further details about this run.</span></span>

## <span data-ttu-id="b95be-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b95be-112">EXAMPLES</span></span>

### <span data-ttu-id="b95be-113">Exemplo 1: invocar um pipeline para iniciar uma execução</span><span class="sxs-lookup"><span data-stu-id="b95be-113">Example 1: Invoke a pipeline to start a run</span></span>
```
PS C:\> Invoke-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineName "DPWikisample"
867d9d9f-1efc-4fee-974d-d8e6320bfbcb
```

<span data-ttu-id="b95be-114">Esse comando inicia uma execução para o pipeline "DPWikisample" na fábrica "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="b95be-114">This command starts a run for "DPWikisample" pipeline in the "WikiADF" factory.</span></span>

## <span data-ttu-id="b95be-115">OS</span><span class="sxs-lookup"><span data-stu-id="b95be-115">PARAMETERS</span></span>

### <span data-ttu-id="b95be-116">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="b95be-116">-DataFactoryName</span></span>
<span data-ttu-id="b95be-117">O nome do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="b95be-117">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryNameByParameterFile, ByFactoryNameByParameterObject
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b95be-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b95be-118">-DefaultProfile</span></span>
<span data-ttu-id="b95be-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b95be-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b95be-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b95be-120">-InputObject</span></span>
<span data-ttu-id="b95be-121">O objeto de fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="b95be-121">The data factory object.</span></span>

```yaml
Type: PSPipeline
Parameter Sets: ByPipelineObjectByParameterFile, ByPipelineObjectByParameterObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b95be-122">-Parâmetro</span><span class="sxs-lookup"><span data-stu-id="b95be-122">-Parameter</span></span>
<span data-ttu-id="b95be-123">Parâmetros para a execução de pipeline.</span><span class="sxs-lookup"><span data-stu-id="b95be-123">Parameters for pipeline run.</span></span>

```yaml
Type: Hashtable
Parameter Sets: ByPipelineObjectByParameterObject, ByFactoryNameByParameterObject
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b95be-124">-Parameterfile</span><span class="sxs-lookup"><span data-stu-id="b95be-124">-ParameterFile</span></span>
<span data-ttu-id="b95be-125">O nome do arquivo com parâmetros para execução de pipeline.</span><span class="sxs-lookup"><span data-stu-id="b95be-125">The name of the file with parameters for pipeline run.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryNameByParameterFile, ByPipelineObjectByParameterFile
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b95be-126">-Pipelinename</span><span class="sxs-lookup"><span data-stu-id="b95be-126">-PipelineName</span></span>
<span data-ttu-id="b95be-127">O nome do pipeline.</span><span class="sxs-lookup"><span data-stu-id="b95be-127">The pipeline name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryNameByParameterFile, ByFactoryNameByParameterObject
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b95be-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b95be-128">-ResourceGroupName</span></span>
<span data-ttu-id="b95be-129">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b95be-129">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryNameByParameterFile, ByFactoryNameByParameterObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b95be-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b95be-130">-Confirm</span></span>
<span data-ttu-id="b95be-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b95be-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b95be-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b95be-132">-WhatIf</span></span>
<span data-ttu-id="b95be-133">Mostra o que acontece se o cmdlet for executado, mas não executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b95be-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b95be-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b95be-134">CommonParameters</span></span>
<span data-ttu-id="b95be-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b95be-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b95be-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b95be-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b95be-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b95be-137">INPUTS</span></span>

### <span data-ttu-id="b95be-138">Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="b95be-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>
<span data-ttu-id="b95be-139">System. String System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="b95be-139">System.String System.Collections.Hashtable</span></span>

## <span data-ttu-id="b95be-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b95be-140">OUTPUTS</span></span>

### <span data-ttu-id="b95be-141">Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="b95be-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="b95be-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b95be-142">NOTES</span></span>

## <span data-ttu-id="b95be-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b95be-143">RELATED LINKS</span></span>

[<span data-ttu-id="b95be-144">Get-AzureRmDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="b95be-144">Get-AzureRmDataFactoryV2PipelineRun</span></span>]()

[<span data-ttu-id="b95be-145">Get-AzureRmDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="b95be-145">Get-AzureRmDataFactoryV2ActivityRun</span></span>]()

