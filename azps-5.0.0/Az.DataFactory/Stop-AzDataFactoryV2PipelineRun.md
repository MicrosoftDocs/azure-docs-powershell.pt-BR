---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/stop-azdatafactoryv2pipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2PipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2PipelineRun.md
ms.openlocfilehash: 400862dbb27eb38d3189c08f741bb595a8e939b2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94280945"
---
# <span data-ttu-id="4381b-101">Stop-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="4381b-101">Stop-AzDataFactoryV2PipelineRun</span></span>

## <span data-ttu-id="4381b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4381b-102">SYNOPSIS</span></span>
<span data-ttu-id="4381b-103">Interrompe uma execução de pipeline em uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="4381b-103">Stops a pipeline run in a data factory.</span></span>

## <span data-ttu-id="4381b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4381b-104">SYNTAX</span></span>

### <span data-ttu-id="4381b-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="4381b-105">ByFactoryName (Default)</span></span>
```
Stop-AzDataFactoryV2PipelineRun [-PipelineRunId] <String> [-PassThru] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4381b-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="4381b-106">ByInputObject</span></span>
```
Stop-AzDataFactoryV2PipelineRun [-InputObject] <PSPipelineRun> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4381b-107">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="4381b-107">ByFactoryObject</span></span>
```
Stop-AzDataFactoryV2PipelineRun [-PipelineRunId] <String> [-PassThru] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4381b-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4381b-108">DESCRIPTION</span></span>
<span data-ttu-id="4381b-109">O cmdlet **Stop-AzDataFactoryV2PipelineRun** interrompe um pipeline executado em um fábrica de dados especificado com a ID de execução de pipeline.</span><span class="sxs-lookup"><span data-stu-id="4381b-109">The **Stop-AzDataFactoryV2PipelineRun** cmdlet stops a pipeline run in a data factory specified with the pipeline run ID.</span></span>

## <span data-ttu-id="4381b-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4381b-110">EXAMPLES</span></span>

### <span data-ttu-id="4381b-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4381b-111">Example 1</span></span>
```
PS C:\> Stop-AzDataFactoryV2PipelineRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineRunId b9730a13-aa12-4926-a8b3-8e3a974ab0bd

Confirm
Are you sure you want to stop pipeline run 'b9730a13-aa12-4926-a8b3-8e3a974ab0bd' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y

true
```

<span data-ttu-id="4381b-112">Esse comando interrompe o pipeline executado com ID b9730a13-AA12-4926-a8b3-8e3a974ab0bd no WikiADF de fábrica.</span><span class="sxs-lookup"><span data-stu-id="4381b-112">This command stops the pipeline run with id b9730a13-aa12-4926-a8b3-8e3a974ab0bd in the factory WikiADF.</span></span>

## <span data-ttu-id="4381b-113">OS</span><span class="sxs-lookup"><span data-stu-id="4381b-113">PARAMETERS</span></span>

### <span data-ttu-id="4381b-114">-Datafactory</span><span class="sxs-lookup"><span data-stu-id="4381b-114">-DataFactory</span></span>
<span data-ttu-id="4381b-115">O objeto de fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="4381b-115">The data factory object.</span></span>

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

### <span data-ttu-id="4381b-116">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="4381b-116">-DataFactoryName</span></span>
<span data-ttu-id="4381b-117">O nome do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="4381b-117">The data factory name.</span></span>

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

### <span data-ttu-id="4381b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4381b-118">-DefaultProfile</span></span>
<span data-ttu-id="4381b-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4381b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4381b-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4381b-120">-InputObject</span></span>
<span data-ttu-id="4381b-121">A ID de execução do pipeline.</span><span class="sxs-lookup"><span data-stu-id="4381b-121">The Run ID of the pipeline.</span></span>

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

### <span data-ttu-id="4381b-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4381b-122">-PassThru</span></span>
<span data-ttu-id="4381b-123">Se especificado, o cmdlet escrever verdadeiro na operação do caso terá êxito.</span><span class="sxs-lookup"><span data-stu-id="4381b-123">If specified the cmdlet write true in case operation succeeds.</span></span>

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

### <span data-ttu-id="4381b-124">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="4381b-124">-PipelineRunId</span></span>
<span data-ttu-id="4381b-125">A ID de execução do pipeline.</span><span class="sxs-lookup"><span data-stu-id="4381b-125">The Run ID of the pipeline.</span></span>

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

### <span data-ttu-id="4381b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4381b-126">-ResourceGroupName</span></span>
<span data-ttu-id="4381b-127">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4381b-127">The resource group name.</span></span>

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

### <span data-ttu-id="4381b-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4381b-128">-Confirm</span></span>
<span data-ttu-id="4381b-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4381b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4381b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4381b-130">-WhatIf</span></span>
<span data-ttu-id="4381b-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4381b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4381b-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4381b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4381b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4381b-133">CommonParameters</span></span>
<span data-ttu-id="4381b-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4381b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4381b-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4381b-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4381b-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4381b-136">INPUTS</span></span>

### <span data-ttu-id="4381b-137">Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipelineRun</span><span class="sxs-lookup"><span data-stu-id="4381b-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun</span></span>

### <span data-ttu-id="4381b-138">System. String</span><span class="sxs-lookup"><span data-stu-id="4381b-138">System.String</span></span>

### <span data-ttu-id="4381b-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="4381b-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="4381b-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4381b-140">OUTPUTS</span></span>

### <span data-ttu-id="4381b-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4381b-141">System.Boolean</span></span>

## <span data-ttu-id="4381b-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4381b-142">NOTES</span></span>

## <span data-ttu-id="4381b-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4381b-143">RELATED LINKS</span></span>
