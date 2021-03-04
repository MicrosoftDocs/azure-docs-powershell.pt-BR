---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/invoke-azdatafactoryv2triggerrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2TriggerRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2TriggerRun.md
ms.openlocfilehash: 91eb23f3af613cf349219f82d133d08dd6e65b5c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888263"
---
# <span data-ttu-id="a4baf-101">Invoke-AzDataFactoryV2TriggerRun</span><span class="sxs-lookup"><span data-stu-id="a4baf-101">Invoke-AzDataFactoryV2TriggerRun</span></span>

## <span data-ttu-id="a4baf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4baf-102">SYNOPSIS</span></span>
 <span data-ttu-id="a4baf-103">Invoca outra instância de uma operação de gatilho.</span><span class="sxs-lookup"><span data-stu-id="a4baf-103">Invokes another instance of a trigger run.</span></span>

## <span data-ttu-id="a4baf-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a4baf-104">SYNTAX</span></span>

### <span data-ttu-id="a4baf-105">ByFactoryNameByParameterFile (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a4baf-105">ByFactoryNameByParameterFile (Default)</span></span>
```
Invoke-AzDataFactoryV2TriggerRun [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a4baf-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a4baf-106">ByInputObject</span></span>
```
Invoke-AzDataFactoryV2TriggerRun [-InputObject] <PSTriggerRun> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4baf-107">ByFactoryName</span><span class="sxs-lookup"><span data-stu-id="a4baf-107">ByFactoryName</span></span>
```
Invoke-AzDataFactoryV2TriggerRun [-TriggerName] <String> [-TriggerRunId] <String> [-PassThru]
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4baf-108">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="a4baf-108">ByFactoryObject</span></span>
```
Invoke-AzDataFactoryV2TriggerRun [-TriggerName] <String> [-TriggerRunId] <String> [-PassThru]
 [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a4baf-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a4baf-109">DESCRIPTION</span></span>
<span data-ttu-id="a4baf-110">O **comando Invoke-AzDataFactoryV2TriggerRun** inicia outra instância de um gatilho executado com uma nova id de executar gatilho.</span><span class="sxs-lookup"><span data-stu-id="a4baf-110">The **Invoke-AzDataFactoryV2TriggerRun** command starts another instance of a trigger run with a new trigger run id.</span></span>

## <span data-ttu-id="a4baf-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a4baf-111">EXAMPLES</span></span>

### <span data-ttu-id="a4baf-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a4baf-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzDataFactoryV2TriggerRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "testTumblingWindowTrigger" -TriggerRunId 08586002468005888497807248799CU16
```
<span data-ttu-id="a4baf-113">Inicia outra instância de um gatilho executado com uma nova id de execução de gatilho, mantendo a mesma windowStartTime e windowEndTime que o gatilho original é executado.</span><span class="sxs-lookup"><span data-stu-id="a4baf-113">Starts another instance of a trigger run with a new trigger run id, keeping the same windowStartTime and windowEndTime as the original trigger run.</span></span>

## <span data-ttu-id="a4baf-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a4baf-114">PARAMETERS</span></span>

### <span data-ttu-id="a4baf-115">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="a4baf-115">-DataFactory</span></span>
<span data-ttu-id="a4baf-116">O objeto de fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="a4baf-116">The data factory object.</span></span>

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

### <span data-ttu-id="a4baf-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="a4baf-117">-DataFactoryName</span></span>
<span data-ttu-id="a4baf-118">O nome da fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="a4baf-118">The data factory name.</span></span>

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

### <span data-ttu-id="a4baf-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4baf-119">-DefaultProfile</span></span>
<span data-ttu-id="a4baf-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a4baf-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4baf-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a4baf-121">-InputObject</span></span>
<span data-ttu-id="a4baf-122">As informações sobre a operação do gatilho.</span><span class="sxs-lookup"><span data-stu-id="a4baf-122">The information about the trigger run.</span></span>

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

### <span data-ttu-id="a4baf-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a4baf-123">-PassThru</span></span>
<span data-ttu-id="a4baf-124">Se especificado, o cmdlet gravará true caso a operação seja bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="a4baf-124">If specified the cmdlet write true in case operation succeeds.</span></span>

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

### <span data-ttu-id="a4baf-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4baf-125">-ResourceGroupName</span></span>
<span data-ttu-id="a4baf-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a4baf-126">The resource group name.</span></span>

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

### <span data-ttu-id="a4baf-127">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="a4baf-127">-TriggerName</span></span>
<span data-ttu-id="a4baf-128">O nome do gatilho.</span><span class="sxs-lookup"><span data-stu-id="a4baf-128">The trigger name.</span></span>

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

### <span data-ttu-id="a4baf-129">-TriggerRunId</span><span class="sxs-lookup"><span data-stu-id="a4baf-129">-TriggerRunId</span></span>
<span data-ttu-id="a4baf-130">A ID de executar do gatilho.</span><span class="sxs-lookup"><span data-stu-id="a4baf-130">The Run ID of the trigger.</span></span>

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

### <span data-ttu-id="a4baf-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a4baf-131">-Confirm</span></span>
<span data-ttu-id="a4baf-132">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4baf-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4baf-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4baf-133">-WhatIf</span></span>
<span data-ttu-id="a4baf-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a4baf-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4baf-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a4baf-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4baf-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4baf-136">CommonParameters</span></span>
<span data-ttu-id="a4baf-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4baf-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4baf-138">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a4baf-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4baf-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a4baf-139">INPUTS</span></span>

### <span data-ttu-id="a4baf-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun</span><span class="sxs-lookup"><span data-stu-id="a4baf-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun</span></span>

### <span data-ttu-id="a4baf-141">System.String</span><span class="sxs-lookup"><span data-stu-id="a4baf-141">System.String</span></span>

### <span data-ttu-id="a4baf-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="a4baf-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="a4baf-143">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a4baf-143">OUTPUTS</span></span>

### <span data-ttu-id="a4baf-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span><span class="sxs-lookup"><span data-stu-id="a4baf-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="a4baf-145">NOTES</span><span class="sxs-lookup"><span data-stu-id="a4baf-145">NOTES</span></span>

## <span data-ttu-id="a4baf-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a4baf-146">RELATED LINKS</span></span>
