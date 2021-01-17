---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/stop-azdatafactoryv2triggerrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2TriggerRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2TriggerRun.md
ms.openlocfilehash: e2800614e414a041073ae5396fb4b0e1e5833b59
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98429853"
---
# <span data-ttu-id="f2f0a-101">Stop-AzDataFactoryV2TriggerRun</span><span class="sxs-lookup"><span data-stu-id="f2f0a-101">Stop-AzDataFactoryV2TriggerRun</span></span>

## <span data-ttu-id="f2f0a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f2f0a-102">SYNOPSIS</span></span>
<span data-ttu-id="f2f0a-103">Interrompe um gatilho executado em uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="f2f0a-103">Stops a trigger run in a data factory.</span></span>

## <span data-ttu-id="f2f0a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f2f0a-104">SYNTAX</span></span>

### <span data-ttu-id="f2f0a-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="f2f0a-105">ByFactoryName (Default)</span></span>
```
Stop-AzDataFactoryV2TriggerRun [-TriggerName] <String> [-TriggerRunId] <String> [-PassThru]
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2f0a-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="f2f0a-106">ByInputObject</span></span>
```
Stop-AzDataFactoryV2TriggerRun [-InputObject] <PSTriggerRun> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2f0a-107">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="f2f0a-107">ByFactoryObject</span></span>
```
Stop-AzDataFactoryV2TriggerRun [-TriggerName] <String> [-TriggerRunId] <String> [-PassThru]
 [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f2f0a-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f2f0a-108">DESCRIPTION</span></span>
<span data-ttu-id="f2f0a-109">O cmdlet **Stop-AzDataFactoryV2TriggerRun** interrompe um gatilho executado em um fábrica de dados especificado com o nome do gatilho e a ID de execução do gatilho.</span><span class="sxs-lookup"><span data-stu-id="f2f0a-109">The **Stop-AzDataFactoryV2TriggerRun** cmdlet stops a trigger run in a data factory specified with the trigger name and trigger run ID.</span></span>
<span data-ttu-id="f2f0a-110">Atualmente só tem suporte para TumblingWindowTriggers no estado WaitingOnDependency.</span><span class="sxs-lookup"><span data-stu-id="f2f0a-110">Currently only supported for TumblingWindowTriggers in WaitingOnDependency State.</span></span>

## <span data-ttu-id="f2f0a-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f2f0a-111">EXAMPLES</span></span>

### <span data-ttu-id="f2f0a-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f2f0a-112">Example 1</span></span>
```powershell
PS C:\> Stop-AzDataFactoryV2TriggerRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "testTumblingWindowTrigger" -TriggerRunId 08586002468005888497807248799CU16
```

<span data-ttu-id="f2f0a-113">Esse comando interrompe o disparo executado com a ID ' 08586002468005888497807248799CU16 ' no WikiADF de fábrica.</span><span class="sxs-lookup"><span data-stu-id="f2f0a-113">This command stops the trigger run with id '08586002468005888497807248799CU16' in the factory WikiADF.</span></span>

## <span data-ttu-id="f2f0a-114">OS</span><span class="sxs-lookup"><span data-stu-id="f2f0a-114">PARAMETERS</span></span>

### <span data-ttu-id="f2f0a-115">-Datafactory</span><span class="sxs-lookup"><span data-stu-id="f2f0a-115">-DataFactory</span></span>
<span data-ttu-id="f2f0a-116">O objeto de fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="f2f0a-116">The data factory object.</span></span>

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

### <span data-ttu-id="f2f0a-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="f2f0a-117">-DataFactoryName</span></span>
<span data-ttu-id="f2f0a-118">O nome do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="f2f0a-118">The data factory name.</span></span>

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

### <span data-ttu-id="f2f0a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2f0a-119">-DefaultProfile</span></span>
<span data-ttu-id="f2f0a-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f2f0a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2f0a-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f2f0a-121">-InputObject</span></span>
<span data-ttu-id="f2f0a-122">As informações sobre o gatilho são executadas.</span><span class="sxs-lookup"><span data-stu-id="f2f0a-122">The information about the trigger run.</span></span>

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

### <span data-ttu-id="f2f0a-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f2f0a-123">-PassThru</span></span>
<span data-ttu-id="f2f0a-124">Se especificado, o cmdlet escrever verdadeiro na operação do caso terá êxito.</span><span class="sxs-lookup"><span data-stu-id="f2f0a-124">If specified the cmdlet write true in case operation succeeds.</span></span>

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

### <span data-ttu-id="f2f0a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2f0a-125">-ResourceGroupName</span></span>
<span data-ttu-id="f2f0a-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f2f0a-126">The resource group name.</span></span>

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

### <span data-ttu-id="f2f0a-127">-Triggername</span><span class="sxs-lookup"><span data-stu-id="f2f0a-127">-TriggerName</span></span>
<span data-ttu-id="f2f0a-128">O nome do disparador.</span><span class="sxs-lookup"><span data-stu-id="f2f0a-128">The trigger name.</span></span>

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

### <span data-ttu-id="f2f0a-129">-TriggerRunId</span><span class="sxs-lookup"><span data-stu-id="f2f0a-129">-TriggerRunId</span></span>
<span data-ttu-id="f2f0a-130">A ID de execução do gatilho.</span><span class="sxs-lookup"><span data-stu-id="f2f0a-130">The Run ID of the trigger.</span></span>

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

### <span data-ttu-id="f2f0a-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f2f0a-131">-Confirm</span></span>
<span data-ttu-id="f2f0a-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2f0a-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2f0a-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2f0a-133">-WhatIf</span></span>
<span data-ttu-id="f2f0a-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f2f0a-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2f0a-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f2f0a-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2f0a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2f0a-136">CommonParameters</span></span>
<span data-ttu-id="f2f0a-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2f0a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2f0a-138">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f2f0a-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2f0a-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f2f0a-139">INPUTS</span></span>

### <span data-ttu-id="f2f0a-140">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTriggerRun</span><span class="sxs-lookup"><span data-stu-id="f2f0a-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun</span></span>

### <span data-ttu-id="f2f0a-141">System. String</span><span class="sxs-lookup"><span data-stu-id="f2f0a-141">System.String</span></span>

### <span data-ttu-id="f2f0a-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="f2f0a-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="f2f0a-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f2f0a-143">OUTPUTS</span></span>

### <span data-ttu-id="f2f0a-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f2f0a-144">System.Boolean</span></span>

## <span data-ttu-id="f2f0a-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f2f0a-145">NOTES</span></span>

## <span data-ttu-id="f2f0a-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f2f0a-146">RELATED LINKS</span></span>
