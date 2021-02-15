---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/stop-azdatafactoryv2triggerrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2TriggerRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2TriggerRun.md
ms.openlocfilehash: e2800614e414a041073ae5396fb4b0e1e5833b59
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115421"
---
# <span data-ttu-id="3e8bf-101">Stop-AzDataFactoryV2TriggerRun</span><span class="sxs-lookup"><span data-stu-id="3e8bf-101">Stop-AzDataFactoryV2TriggerRun</span></span>

## <span data-ttu-id="3e8bf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3e8bf-102">SYNOPSIS</span></span>
<span data-ttu-id="3e8bf-103">Interrompe a operação de um gatilho em uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="3e8bf-103">Stops a trigger run in a data factory.</span></span>

## <span data-ttu-id="3e8bf-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3e8bf-104">SYNTAX</span></span>

### <span data-ttu-id="3e8bf-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="3e8bf-105">ByFactoryName (Default)</span></span>
```
Stop-AzDataFactoryV2TriggerRun [-TriggerName] <String> [-TriggerRunId] <String> [-PassThru]
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e8bf-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="3e8bf-106">ByInputObject</span></span>
```
Stop-AzDataFactoryV2TriggerRun [-InputObject] <PSTriggerRun> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e8bf-107">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="3e8bf-107">ByFactoryObject</span></span>
```
Stop-AzDataFactoryV2TriggerRun [-TriggerName] <String> [-TriggerRunId] <String> [-PassThru]
 [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3e8bf-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="3e8bf-108">DESCRIPTION</span></span>
<span data-ttu-id="3e8bf-109">O cmdlet **Stop-AzDataFactoryV2TrioryRun** interrompe uma operação de gatilho em um fábrica de dados especificado com o nome do gatilho e a ID de executar gatilho.</span><span class="sxs-lookup"><span data-stu-id="3e8bf-109">The **Stop-AzDataFactoryV2TriggerRun** cmdlet stops a trigger run in a data factory specified with the trigger name and trigger run ID.</span></span>
<span data-ttu-id="3e8bf-110">Atualmente, só há suporte para WindWindowTriwinds no estado WaitingOnDependency.</span><span class="sxs-lookup"><span data-stu-id="3e8bf-110">Currently only supported for TumblingWindowTriggers in WaitingOnDependency State.</span></span>

## <span data-ttu-id="3e8bf-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3e8bf-111">EXAMPLES</span></span>

### <span data-ttu-id="3e8bf-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3e8bf-112">Example 1</span></span>
```powershell
PS C:\> Stop-AzDataFactoryV2TriggerRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "testTumblingWindowTrigger" -TriggerRunId 08586002468005888497807248799CU16
```

<span data-ttu-id="3e8bf-113">Esse comando interrompe a executar o gatilho com a id '08586002468005888497807248799CU16' no WikiADF de fábrica.</span><span class="sxs-lookup"><span data-stu-id="3e8bf-113">This command stops the trigger run with id '08586002468005888497807248799CU16' in the factory WikiADF.</span></span>

## <span data-ttu-id="3e8bf-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3e8bf-114">PARAMETERS</span></span>

### <span data-ttu-id="3e8bf-115">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="3e8bf-115">-DataFactory</span></span>
<span data-ttu-id="3e8bf-116">O objeto de fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="3e8bf-116">The data factory object.</span></span>

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

### <span data-ttu-id="3e8bf-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="3e8bf-117">-DataFactoryName</span></span>
<span data-ttu-id="3e8bf-118">O nome da fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="3e8bf-118">The data factory name.</span></span>

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

### <span data-ttu-id="3e8bf-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e8bf-119">-DefaultProfile</span></span>
<span data-ttu-id="3e8bf-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3e8bf-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e8bf-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3e8bf-121">-InputObject</span></span>
<span data-ttu-id="3e8bf-122">As informações sobre o gatilho são executados.</span><span class="sxs-lookup"><span data-stu-id="3e8bf-122">The information about the trigger run.</span></span>

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

### <span data-ttu-id="3e8bf-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3e8bf-123">-PassThru</span></span>
<span data-ttu-id="3e8bf-124">Se especificado o cmdlet write true caso a operação seja bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="3e8bf-124">If specified the cmdlet write true in case operation succeeds.</span></span>

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

### <span data-ttu-id="3e8bf-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e8bf-125">-ResourceGroupName</span></span>
<span data-ttu-id="3e8bf-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3e8bf-126">The resource group name.</span></span>

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

### <span data-ttu-id="3e8bf-127">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="3e8bf-127">-TriggerName</span></span>
<span data-ttu-id="3e8bf-128">O nome do gatilho.</span><span class="sxs-lookup"><span data-stu-id="3e8bf-128">The trigger name.</span></span>

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

### <span data-ttu-id="3e8bf-129">-TriggerRunId</span><span class="sxs-lookup"><span data-stu-id="3e8bf-129">-TriggerRunId</span></span>
<span data-ttu-id="3e8bf-130">A ID de Executar do gatilho.</span><span class="sxs-lookup"><span data-stu-id="3e8bf-130">The Run ID of the trigger.</span></span>

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

### <span data-ttu-id="3e8bf-131">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="3e8bf-131">-Confirm</span></span>
<span data-ttu-id="3e8bf-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e8bf-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e8bf-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e8bf-133">-WhatIf</span></span>
<span data-ttu-id="3e8bf-134">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="3e8bf-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e8bf-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3e8bf-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e8bf-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e8bf-136">CommonParameters</span></span>
<span data-ttu-id="3e8bf-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e8bf-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e8bf-138">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3e8bf-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e8bf-139">Entradas</span><span class="sxs-lookup"><span data-stu-id="3e8bf-139">INPUTS</span></span>

### <span data-ttu-id="3e8bf-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrioryRun</span><span class="sxs-lookup"><span data-stu-id="3e8bf-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun</span></span>

### <span data-ttu-id="3e8bf-141">System.String</span><span class="sxs-lookup"><span data-stu-id="3e8bf-141">System.String</span></span>

### <span data-ttu-id="3e8bf-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="3e8bf-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="3e8bf-143">Saídas</span><span class="sxs-lookup"><span data-stu-id="3e8bf-143">OUTPUTS</span></span>

### <span data-ttu-id="3e8bf-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3e8bf-144">System.Boolean</span></span>

## <span data-ttu-id="3e8bf-145">Notas</span><span class="sxs-lookup"><span data-stu-id="3e8bf-145">NOTES</span></span>

## <span data-ttu-id="3e8bf-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3e8bf-146">RELATED LINKS</span></span>
