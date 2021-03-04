---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/stop-azdatafactoryv2triggerrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2TriggerRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2TriggerRun.md
ms.openlocfilehash: 1e3310b99173c0a7fa83dcada286833747457213
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886995"
---
# <span data-ttu-id="2416e-101">Stop-AzDataFactoryV2TriggerRun</span><span class="sxs-lookup"><span data-stu-id="2416e-101">Stop-AzDataFactoryV2TriggerRun</span></span>

## <span data-ttu-id="2416e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2416e-102">SYNOPSIS</span></span>
<span data-ttu-id="2416e-103">Interrompe um gatilho executado em um fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="2416e-103">Stops a trigger run in a data factory.</span></span>

## <span data-ttu-id="2416e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="2416e-104">SYNTAX</span></span>

### <span data-ttu-id="2416e-105">ByFactoryName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="2416e-105">ByFactoryName (Default)</span></span>
```
Stop-AzDataFactoryV2TriggerRun [-TriggerName] <String> [-TriggerRunId] <String> [-PassThru]
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2416e-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="2416e-106">ByInputObject</span></span>
```
Stop-AzDataFactoryV2TriggerRun [-InputObject] <PSTriggerRun> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2416e-107">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="2416e-107">ByFactoryObject</span></span>
```
Stop-AzDataFactoryV2TriggerRun [-TriggerName] <String> [-TriggerRunId] <String> [-PassThru]
 [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2416e-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="2416e-108">DESCRIPTION</span></span>
<span data-ttu-id="2416e-109">O cmdlet **Stop-AzDataFactoryV2TriggerRun** interrompe um gatilho executado em um fábrica de dados especificado com o nome do gatilho e a ID de executar gatilho.</span><span class="sxs-lookup"><span data-stu-id="2416e-109">The **Stop-AzDataFactoryV2TriggerRun** cmdlet stops a trigger run in a data factory specified with the trigger name and trigger run ID.</span></span>
<span data-ttu-id="2416e-110">Atualmente, só há suporte para WindWindowTriggers no estado WaitingOnDependency.</span><span class="sxs-lookup"><span data-stu-id="2416e-110">Currently only supported for TumblingWindowTriggers in WaitingOnDependency State.</span></span>

## <span data-ttu-id="2416e-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2416e-111">EXAMPLES</span></span>

### <span data-ttu-id="2416e-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2416e-112">Example 1</span></span>
```powershell
PS C:\> Stop-AzDataFactoryV2TriggerRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "testTumblingWindowTrigger" -TriggerRunId 08586002468005888497807248799CU16
```

<span data-ttu-id="2416e-113">Este comando interrompe o gatilho executado com a id '08586002468005888497807248799CU16' na fábrica WikiADF.</span><span class="sxs-lookup"><span data-stu-id="2416e-113">This command stops the trigger run with id '08586002468005888497807248799CU16' in the factory WikiADF.</span></span>

## <span data-ttu-id="2416e-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="2416e-114">PARAMETERS</span></span>

### <span data-ttu-id="2416e-115">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="2416e-115">-DataFactory</span></span>
<span data-ttu-id="2416e-116">O objeto de fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="2416e-116">The data factory object.</span></span>

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

### <span data-ttu-id="2416e-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="2416e-117">-DataFactoryName</span></span>
<span data-ttu-id="2416e-118">O nome da fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="2416e-118">The data factory name.</span></span>

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

### <span data-ttu-id="2416e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2416e-119">-DefaultProfile</span></span>
<span data-ttu-id="2416e-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2416e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2416e-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2416e-121">-InputObject</span></span>
<span data-ttu-id="2416e-122">As informações sobre a operação do gatilho.</span><span class="sxs-lookup"><span data-stu-id="2416e-122">The information about the trigger run.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2416e-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2416e-123">-PassThru</span></span>
<span data-ttu-id="2416e-124">Se especificado, o cmdlet gravará true caso a operação seja bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="2416e-124">If specified the cmdlet write true in case operation succeeds.</span></span>

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

### <span data-ttu-id="2416e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2416e-125">-ResourceGroupName</span></span>
<span data-ttu-id="2416e-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2416e-126">The resource group name.</span></span>

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

### <span data-ttu-id="2416e-127">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="2416e-127">-TriggerName</span></span>
<span data-ttu-id="2416e-128">O nome do gatilho.</span><span class="sxs-lookup"><span data-stu-id="2416e-128">The trigger name.</span></span>

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

### <span data-ttu-id="2416e-129">-TriggerRunId</span><span class="sxs-lookup"><span data-stu-id="2416e-129">-TriggerRunId</span></span>
<span data-ttu-id="2416e-130">A ID de executar do gatilho.</span><span class="sxs-lookup"><span data-stu-id="2416e-130">The Run ID of the trigger.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2416e-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2416e-131">-Confirm</span></span>
<span data-ttu-id="2416e-132">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2416e-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2416e-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2416e-133">-WhatIf</span></span>
<span data-ttu-id="2416e-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2416e-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2416e-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2416e-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2416e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2416e-136">CommonParameters</span></span>
<span data-ttu-id="2416e-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2416e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2416e-138">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2416e-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2416e-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2416e-139">INPUTS</span></span>

### <span data-ttu-id="2416e-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun</span><span class="sxs-lookup"><span data-stu-id="2416e-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun</span></span>

### <span data-ttu-id="2416e-141">System.String</span><span class="sxs-lookup"><span data-stu-id="2416e-141">System.String</span></span>

### <span data-ttu-id="2416e-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="2416e-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="2416e-143">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="2416e-143">OUTPUTS</span></span>

### <span data-ttu-id="2416e-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2416e-144">System.Boolean</span></span>

## <span data-ttu-id="2416e-145">NOTES</span><span class="sxs-lookup"><span data-stu-id="2416e-145">NOTES</span></span>

## <span data-ttu-id="2416e-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2416e-146">RELATED LINKS</span></span>
