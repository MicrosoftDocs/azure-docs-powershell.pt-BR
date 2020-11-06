---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Stop-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Stop-AzureRmDataFactoryV2Trigger.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 3054824876ccaff24f319ae14c704cd975e79434
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609716"
---
# <span data-ttu-id="8813c-101">Stop-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="8813c-101">Stop-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="8813c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8813c-102">SYNOPSIS</span></span>

<span data-ttu-id="8813c-103">Interrompe um gatilho em uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="8813c-103">Stops a trigger in a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8813c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8813c-104">SYNTAX</span></span>

### <span data-ttu-id="8813c-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="8813c-105">ByFactoryName (Default)</span></span>
```
Stop-AzureRmDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="8813c-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="8813c-106">ByInputObject</span></span>
```
Stop-AzureRmDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="8813c-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8813c-107">ByResourceId</span></span>
```
Stop-AzureRmDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="8813c-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8813c-108">DESCRIPTION</span></span>

<span data-ttu-id="8813c-109">O cmdlet **Stop-AzureRmDataFactoryV2Trigger** interrompe um gatilho em uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="8813c-109">The **Stop-AzureRmDataFactoryV2Trigger** cmdlet stops a trigger in a data factory.</span></span> <span data-ttu-id="8813c-110">Se o gatilho estiver no estado ' iniciado ', o cmdlet para o gatilho e não invoca mais os pipelines.</span><span class="sxs-lookup"><span data-stu-id="8813c-110">If the trigger is in the 'Started' state, the cmdlet stops the trigger and no longer invokes pipelines.</span></span> <span data-ttu-id="8813c-111">Se o gatilho já estiver no estado ' interrompido ', esse cmdlet não terá efeito.</span><span class="sxs-lookup"><span data-stu-id="8813c-111">If the trigger is already in the 'Stopped' state, this cmdlet has no effect.</span></span> <span data-ttu-id="8813c-112">Se o parâmetro Force for especificado, o cmdlet não será avisado antes de parar o gatilho.</span><span class="sxs-lookup"><span data-stu-id="8813c-112">If the Force parameter is specified, the cmdlet doesn't prompt before stopping the trigger.</span></span>


## <span data-ttu-id="8813c-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8813c-113">EXAMPLES</span></span>

### <span data-ttu-id="8813c-114">Exemplo 1: parar um gatilho</span><span class="sxs-lookup"><span data-stu-id="8813c-114">Example 1: Stop a trigger</span></span>

```
Stop-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

Confirm
Are you sure you want to stop trigger 'ScheduledTrigger' in data factory 'TestFactory'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="8813c-115">Interrompe um gatilho chamado "ScheduledTrigger" na fábrica de dados "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="8813c-115">Stops a trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>


## <span data-ttu-id="8813c-116">OS</span><span class="sxs-lookup"><span data-stu-id="8813c-116">PARAMETERS</span></span>

### <span data-ttu-id="8813c-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8813c-117">-Confirm</span></span>
<span data-ttu-id="8813c-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8813c-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8813c-119">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="8813c-119">-DataFactoryName</span></span>
<span data-ttu-id="8813c-120">O nome do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="8813c-120">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8813c-121">-Force</span><span class="sxs-lookup"><span data-stu-id="8813c-121">-Force</span></span>
<span data-ttu-id="8813c-122">Executa o cmdlet sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="8813c-122">Runs the cmdlet without prompting for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8813c-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="8813c-123">-Name</span></span>
<span data-ttu-id="8813c-124">O nome do disparador.</span><span class="sxs-lookup"><span data-stu-id="8813c-124">The trigger name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8813c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8813c-125">-ResourceGroupName</span></span>
<span data-ttu-id="8813c-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8813c-126">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8813c-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8813c-127">-ResourceId</span></span>
<span data-ttu-id="8813c-128">A ID do recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="8813c-128">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8813c-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8813c-129">-InputObject</span></span>
<span data-ttu-id="8813c-130">Objeto Trigger para iniciar.</span><span class="sxs-lookup"><span data-stu-id="8813c-130">Trigger object to start.</span></span>

```yaml
Type: PSTrigger
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8813c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8813c-131">-WhatIf</span></span>
<span data-ttu-id="8813c-132">Mostra o que acontece se o cmdlet for executado, mas não executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8813c-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="8813c-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8813c-133">INPUTS</span></span>

### <span data-ttu-id="8813c-134">System. String</span><span class="sxs-lookup"><span data-stu-id="8813c-134">System.String</span></span>
<span data-ttu-id="8813c-135">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="8813c-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>


## <span data-ttu-id="8813c-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8813c-136">OUTPUTS</span></span>

### <span data-ttu-id="8813c-137">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="8813c-137">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="8813c-138">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="8813c-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>


## <span data-ttu-id="8813c-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8813c-139">NOTES</span></span>

## <span data-ttu-id="8813c-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8813c-140">RELATED LINKS</span></span>
[<span data-ttu-id="8813c-141">Get-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="8813c-141">Get-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="8813c-142">Set-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="8813c-142">Set-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="8813c-143">Start-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="8813c-143">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="8813c-144">Remove-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="8813c-144">Remove-AzureRmDataFactoryV2Trigger</span></span>]()
