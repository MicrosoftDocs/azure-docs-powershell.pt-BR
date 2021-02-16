---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/stop-azdatafactoryv2pipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2PipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2PipelineRun.md
ms.openlocfilehash: 400862dbb27eb38d3189c08f741bb595a8e939b2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117736"
---
# <span data-ttu-id="78cd6-101">Stop-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="78cd6-101">Stop-AzDataFactoryV2PipelineRun</span></span>

## <span data-ttu-id="78cd6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="78cd6-102">SYNOPSIS</span></span>
<span data-ttu-id="78cd6-103">Interrompe a adoção de um pipeline em uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="78cd6-103">Stops a pipeline run in a data factory.</span></span>

## <span data-ttu-id="78cd6-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="78cd6-104">SYNTAX</span></span>

### <span data-ttu-id="78cd6-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="78cd6-105">ByFactoryName (Default)</span></span>
```
Stop-AzDataFactoryV2PipelineRun [-PipelineRunId] <String> [-PassThru] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="78cd6-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="78cd6-106">ByInputObject</span></span>
```
Stop-AzDataFactoryV2PipelineRun [-InputObject] <PSPipelineRun> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78cd6-107">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="78cd6-107">ByFactoryObject</span></span>
```
Stop-AzDataFactoryV2PipelineRun [-PipelineRunId] <String> [-PassThru] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78cd6-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="78cd6-108">DESCRIPTION</span></span>
<span data-ttu-id="78cd6-109">O cmdlet **Stop-AzDataFactoryV2 PipelinelineRun** interrompe um pipeline executado em um fábrica de dados especificado com a ID de pipeline de executar.</span><span class="sxs-lookup"><span data-stu-id="78cd6-109">The **Stop-AzDataFactoryV2PipelineRun** cmdlet stops a pipeline run in a data factory specified with the pipeline run ID.</span></span>

## <span data-ttu-id="78cd6-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="78cd6-110">EXAMPLES</span></span>

### <span data-ttu-id="78cd6-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="78cd6-111">Example 1</span></span>
```
PS C:\> Stop-AzDataFactoryV2PipelineRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineRunId b9730a13-aa12-4926-a8b3-8e3a974ab0bd

Confirm
Are you sure you want to stop pipeline run 'b9730a13-aa12-4926-a8b3-8e3a974ab0bd' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y

true
```

<span data-ttu-id="78cd6-112">Este comando interrompe a executar o pipeline com a ID b9730a13-aa12-4926-a8b3-8e3a974ab0bd no WikiADF de fábrica.</span><span class="sxs-lookup"><span data-stu-id="78cd6-112">This command stops the pipeline run with id b9730a13-aa12-4926-a8b3-8e3a974ab0bd in the factory WikiADF.</span></span>

## <span data-ttu-id="78cd6-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="78cd6-113">PARAMETERS</span></span>

### <span data-ttu-id="78cd6-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="78cd6-114">-DataFactory</span></span>
<span data-ttu-id="78cd6-115">O objeto de fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="78cd6-115">The data factory object.</span></span>

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

### <span data-ttu-id="78cd6-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="78cd6-116">-DataFactoryName</span></span>
<span data-ttu-id="78cd6-117">O nome da fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="78cd6-117">The data factory name.</span></span>

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

### <span data-ttu-id="78cd6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78cd6-118">-DefaultProfile</span></span>
<span data-ttu-id="78cd6-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="78cd6-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="78cd6-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="78cd6-120">-InputObject</span></span>
<span data-ttu-id="78cd6-121">A ID de Executar do pipeline.</span><span class="sxs-lookup"><span data-stu-id="78cd6-121">The Run ID of the pipeline.</span></span>

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

### <span data-ttu-id="78cd6-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="78cd6-122">-PassThru</span></span>
<span data-ttu-id="78cd6-123">Se especificado o cmdlet write true caso a operação seja bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="78cd6-123">If specified the cmdlet write true in case operation succeeds.</span></span>

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

### <span data-ttu-id="78cd6-124">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="78cd6-124">-PipelineRunId</span></span>
<span data-ttu-id="78cd6-125">A ID de Executar do pipeline.</span><span class="sxs-lookup"><span data-stu-id="78cd6-125">The Run ID of the pipeline.</span></span>

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

### <span data-ttu-id="78cd6-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78cd6-126">-ResourceGroupName</span></span>
<span data-ttu-id="78cd6-127">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="78cd6-127">The resource group name.</span></span>

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

### <span data-ttu-id="78cd6-128">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="78cd6-128">-Confirm</span></span>
<span data-ttu-id="78cd6-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78cd6-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78cd6-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78cd6-130">-WhatIf</span></span>
<span data-ttu-id="78cd6-131">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="78cd6-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78cd6-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="78cd6-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78cd6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78cd6-133">CommonParameters</span></span>
<span data-ttu-id="78cd6-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78cd6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78cd6-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78cd6-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78cd6-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="78cd6-136">INPUTS</span></span>

### <span data-ttu-id="78cd6-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PS Ltd.</span><span class="sxs-lookup"><span data-stu-id="78cd6-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun</span></span>

### <span data-ttu-id="78cd6-138">System.String</span><span class="sxs-lookup"><span data-stu-id="78cd6-138">System.String</span></span>

### <span data-ttu-id="78cd6-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="78cd6-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="78cd6-140">Saídas</span><span class="sxs-lookup"><span data-stu-id="78cd6-140">OUTPUTS</span></span>

### <span data-ttu-id="78cd6-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="78cd6-141">System.Boolean</span></span>

## <span data-ttu-id="78cd6-142">Notas</span><span class="sxs-lookup"><span data-stu-id="78cd6-142">NOTES</span></span>

## <span data-ttu-id="78cd6-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="78cd6-143">RELATED LINKS</span></span>
