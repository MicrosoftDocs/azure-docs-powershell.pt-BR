---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/invoke-azdatafactoryv2triggerrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2TriggerRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2TriggerRun.md
ms.openlocfilehash: af0fcf4e96d919c2c52a2ab30e583f288d20fc4e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111980"
---
# <span data-ttu-id="107f1-101">Invoke-AzDataFactoryV2TriggerRun</span><span class="sxs-lookup"><span data-stu-id="107f1-101">Invoke-AzDataFactoryV2TriggerRun</span></span>

## <span data-ttu-id="107f1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="107f1-102">SYNOPSIS</span></span>
 <span data-ttu-id="107f1-103">Invoca outra instância de uma operação de gatilho.</span><span class="sxs-lookup"><span data-stu-id="107f1-103">Invokes another instance of a trigger run.</span></span>

## <span data-ttu-id="107f1-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="107f1-104">SYNTAX</span></span>

### <span data-ttu-id="107f1-105">ByFactoryNameByParameterFile (Padrão)</span><span class="sxs-lookup"><span data-stu-id="107f1-105">ByFactoryNameByParameterFile (Default)</span></span>
```
Invoke-AzDataFactoryV2TriggerRun [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="107f1-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="107f1-106">ByInputObject</span></span>
```
Invoke-AzDataFactoryV2TriggerRun [-InputObject] <PSTriggerRun> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="107f1-107">ByFactoryName</span><span class="sxs-lookup"><span data-stu-id="107f1-107">ByFactoryName</span></span>
```
Invoke-AzDataFactoryV2TriggerRun [-TriggerName] <String> [-TriggerRunId] <String> [-PassThru]
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="107f1-108">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="107f1-108">ByFactoryObject</span></span>
```
Invoke-AzDataFactoryV2TriggerRun [-TriggerName] <String> [-TriggerRunId] <String> [-PassThru]
 [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="107f1-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="107f1-109">DESCRIPTION</span></span>
<span data-ttu-id="107f1-110">O **comando Invoke-AzDataFactoryV2TrivocRun** inicia outra instância de uma executar gatilho com uma nova id de executar gatilho.</span><span class="sxs-lookup"><span data-stu-id="107f1-110">The **Invoke-AzDataFactoryV2TriggerRun** command starts another instance of a trigger run with a new trigger run id.</span></span>

## <span data-ttu-id="107f1-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="107f1-111">EXAMPLES</span></span>

### <span data-ttu-id="107f1-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="107f1-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzDataFactoryV2TriggerRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "testTumblingWindowTrigger" -TriggerRunId 08586002468005888497807248799CU16
```
<span data-ttu-id="107f1-113">Inicia outra instância de uma execução de gatilho com uma nova ID de execução de gatilho, mantendo a mesma janelaStartTime e windowEndTime que o gatilho original é executado.</span><span class="sxs-lookup"><span data-stu-id="107f1-113">Starts another instance of a trigger run with a new trigger run id, keeping the same windowStartTime and windowEndTime as the original trigger run.</span></span>

## <span data-ttu-id="107f1-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="107f1-114">PARAMETERS</span></span>

### <span data-ttu-id="107f1-115">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="107f1-115">-DataFactory</span></span>
<span data-ttu-id="107f1-116">O objeto de fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="107f1-116">The data factory object.</span></span>

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

### <span data-ttu-id="107f1-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="107f1-117">-DataFactoryName</span></span>
<span data-ttu-id="107f1-118">O nome da fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="107f1-118">The data factory name.</span></span>

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

### <span data-ttu-id="107f1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="107f1-119">-DefaultProfile</span></span>
<span data-ttu-id="107f1-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="107f1-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="107f1-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="107f1-121">-InputObject</span></span>
<span data-ttu-id="107f1-122">As informações sobre o gatilho são executados.</span><span class="sxs-lookup"><span data-stu-id="107f1-122">The information about the trigger run.</span></span>

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

### <span data-ttu-id="107f1-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="107f1-123">-PassThru</span></span>
<span data-ttu-id="107f1-124">Se especificado o cmdlet write true caso a operação seja bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="107f1-124">If specified the cmdlet write true in case operation succeeds.</span></span>

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

### <span data-ttu-id="107f1-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="107f1-125">-ResourceGroupName</span></span>
<span data-ttu-id="107f1-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="107f1-126">The resource group name.</span></span>

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

### <span data-ttu-id="107f1-127">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="107f1-127">-TriggerName</span></span>
<span data-ttu-id="107f1-128">O nome do gatilho.</span><span class="sxs-lookup"><span data-stu-id="107f1-128">The trigger name.</span></span>

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

### <span data-ttu-id="107f1-129">-TriggerRunId</span><span class="sxs-lookup"><span data-stu-id="107f1-129">-TriggerRunId</span></span>
<span data-ttu-id="107f1-130">A ID de Executar do gatilho.</span><span class="sxs-lookup"><span data-stu-id="107f1-130">The Run ID of the trigger.</span></span>

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

### <span data-ttu-id="107f1-131">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="107f1-131">-Confirm</span></span>
<span data-ttu-id="107f1-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="107f1-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="107f1-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="107f1-133">-WhatIf</span></span>
<span data-ttu-id="107f1-134">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="107f1-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="107f1-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="107f1-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="107f1-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="107f1-136">CommonParameters</span></span>
<span data-ttu-id="107f1-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="107f1-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="107f1-138">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="107f1-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="107f1-139">Entradas</span><span class="sxs-lookup"><span data-stu-id="107f1-139">INPUTS</span></span>

### <span data-ttu-id="107f1-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrioryRun</span><span class="sxs-lookup"><span data-stu-id="107f1-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun</span></span>

### <span data-ttu-id="107f1-141">System.String</span><span class="sxs-lookup"><span data-stu-id="107f1-141">System.String</span></span>

### <span data-ttu-id="107f1-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="107f1-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="107f1-143">Saídas</span><span class="sxs-lookup"><span data-stu-id="107f1-143">OUTPUTS</span></span>

### <span data-ttu-id="107f1-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PS Bem-feira</span><span class="sxs-lookup"><span data-stu-id="107f1-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="107f1-145">Notas</span><span class="sxs-lookup"><span data-stu-id="107f1-145">NOTES</span></span>

## <span data-ttu-id="107f1-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="107f1-146">RELATED LINKS</span></span>
