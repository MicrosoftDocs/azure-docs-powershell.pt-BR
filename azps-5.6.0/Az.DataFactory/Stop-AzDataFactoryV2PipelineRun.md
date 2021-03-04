---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/stop-azdatafactoryv2pipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2PipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2PipelineRun.md
ms.openlocfilehash: 096ee403a0ee12c80462a1fb87db4378e3d86f01
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891446"
---
# <span data-ttu-id="3283e-101">Stop-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="3283e-101">Stop-AzDataFactoryV2PipelineRun</span></span>

## <span data-ttu-id="3283e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3283e-102">SYNOPSIS</span></span>
<span data-ttu-id="3283e-103">Interrompe um pipeline executado em um fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="3283e-103">Stops a pipeline run in a data factory.</span></span>

## <span data-ttu-id="3283e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="3283e-104">SYNTAX</span></span>

### <span data-ttu-id="3283e-105">ByFactoryName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="3283e-105">ByFactoryName (Default)</span></span>
```
Stop-AzDataFactoryV2PipelineRun [-PipelineRunId] <String> [-PassThru] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3283e-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="3283e-106">ByInputObject</span></span>
```
Stop-AzDataFactoryV2PipelineRun [-InputObject] <PSPipelineRun> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3283e-107">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="3283e-107">ByFactoryObject</span></span>
```
Stop-AzDataFactoryV2PipelineRun [-PipelineRunId] <String> [-PassThru] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3283e-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="3283e-108">DESCRIPTION</span></span>
<span data-ttu-id="3283e-109">O cmdlet **Stop-AzDataFactoryV2PipelineRun** interrompe um pipeline executado em um fábrica de dados especificado com a ID de executar pipeline.</span><span class="sxs-lookup"><span data-stu-id="3283e-109">The **Stop-AzDataFactoryV2PipelineRun** cmdlet stops a pipeline run in a data factory specified with the pipeline run ID.</span></span>

## <span data-ttu-id="3283e-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3283e-110">EXAMPLES</span></span>

### <span data-ttu-id="3283e-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3283e-111">Example 1</span></span>
```
PS C:\> Stop-AzDataFactoryV2PipelineRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineRunId b9730a13-aa12-4926-a8b3-8e3a974ab0bd

Confirm
Are you sure you want to stop pipeline run 'b9730a13-aa12-4926-a8b3-8e3a974ab0bd' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y

true
```

<span data-ttu-id="3283e-112">Este comando interrompe o pipeline executado com a id b9730a13-aa12-4926-a8b3-8e3a974ab0bd na fábrica WikiADF.</span><span class="sxs-lookup"><span data-stu-id="3283e-112">This command stops the pipeline run with id b9730a13-aa12-4926-a8b3-8e3a974ab0bd in the factory WikiADF.</span></span>

## <span data-ttu-id="3283e-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="3283e-113">PARAMETERS</span></span>

### <span data-ttu-id="3283e-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="3283e-114">-DataFactory</span></span>
<span data-ttu-id="3283e-115">O objeto de fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="3283e-115">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3283e-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="3283e-116">-DataFactoryName</span></span>
<span data-ttu-id="3283e-117">O nome da fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="3283e-117">The data factory name.</span></span>

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

### <span data-ttu-id="3283e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3283e-118">-DefaultProfile</span></span>
<span data-ttu-id="3283e-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="3283e-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3283e-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3283e-120">-InputObject</span></span>
<span data-ttu-id="3283e-121">A ID de executar do pipeline.</span><span class="sxs-lookup"><span data-stu-id="3283e-121">The Run ID of the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3283e-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3283e-122">-PassThru</span></span>
<span data-ttu-id="3283e-123">Se especificado, o cmdlet gravará true caso a operação seja bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="3283e-123">If specified the cmdlet write true in case operation succeeds.</span></span>

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

### <span data-ttu-id="3283e-124">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="3283e-124">-PipelineRunId</span></span>
<span data-ttu-id="3283e-125">A ID de executar do pipeline.</span><span class="sxs-lookup"><span data-stu-id="3283e-125">The Run ID of the pipeline.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3283e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3283e-126">-ResourceGroupName</span></span>
<span data-ttu-id="3283e-127">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3283e-127">The resource group name.</span></span>

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

### <span data-ttu-id="3283e-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3283e-128">-Confirm</span></span>
<span data-ttu-id="3283e-129">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3283e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3283e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3283e-130">-WhatIf</span></span>
<span data-ttu-id="3283e-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3283e-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3283e-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3283e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3283e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3283e-133">CommonParameters</span></span>
<span data-ttu-id="3283e-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3283e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3283e-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3283e-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3283e-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3283e-136">INPUTS</span></span>

### <span data-ttu-id="3283e-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun</span><span class="sxs-lookup"><span data-stu-id="3283e-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun</span></span>

### <span data-ttu-id="3283e-138">System.String</span><span class="sxs-lookup"><span data-stu-id="3283e-138">System.String</span></span>

### <span data-ttu-id="3283e-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="3283e-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="3283e-140">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="3283e-140">OUTPUTS</span></span>

### <span data-ttu-id="3283e-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3283e-141">System.Boolean</span></span>

## <span data-ttu-id="3283e-142">NOTES</span><span class="sxs-lookup"><span data-stu-id="3283e-142">NOTES</span></span>

## <span data-ttu-id="3283e-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3283e-143">RELATED LINKS</span></span>
