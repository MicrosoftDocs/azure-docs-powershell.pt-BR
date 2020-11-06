---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Trigger.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 3a10820bb0e4ed8c2a9ddb95bc716753a4a96ca0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441574"
---
# <span data-ttu-id="adf30-101">Remove-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="adf30-101">Remove-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="adf30-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="adf30-102">SYNOPSIS</span></span>
<span data-ttu-id="adf30-103">Remove um gatilho de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="adf30-103">Removes a trigger from a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="adf30-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="adf30-104">SYNTAX</span></span>

### <span data-ttu-id="adf30-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="adf30-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="adf30-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="adf30-106">ByInputObject</span></span>
```
Remove-AzureRmDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="adf30-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="adf30-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="adf30-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="adf30-108">DESCRIPTION</span></span>
<span data-ttu-id="adf30-109">O cmdlet **Remove-AzureRmDataFactoryV2Trigger** remove um gatilho de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="adf30-109">The **Remove-AzureRmDataFactoryV2Trigger** cmdlet removes a trigger from a data factory.</span></span> <span data-ttu-id="adf30-110">Se o parâmetro _Force_ for especificado, o cmdlet não avisa antes de remover o gatilho.</span><span class="sxs-lookup"><span data-stu-id="adf30-110">If the _Force_ parameter is specified, the cmdlet doesn't prompt before removing the trigger.</span></span>

## <span data-ttu-id="adf30-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="adf30-111">EXAMPLES</span></span>

### <span data-ttu-id="adf30-112">Exemplo 1: remover um gatilho</span><span class="sxs-lookup"><span data-stu-id="adf30-112">Example 1: Remove a trigger</span></span>
```
Remove-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "ScheduledTrigger"

Confirm
Are you sure you want to remove trigger 'ScheduledTrigger' in data factory 'TestFactory'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="adf30-113">Remova um gatilho chamado "ScheduledTrigger" da fábrica de dados "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="adf30-113">Remove a trigger called "ScheduledTrigger" from the data factory "WikiADF".</span></span>

## <span data-ttu-id="adf30-114">OS</span><span class="sxs-lookup"><span data-stu-id="adf30-114">PARAMETERS</span></span>

### <span data-ttu-id="adf30-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="adf30-115">-Confirm</span></span>
<span data-ttu-id="adf30-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="adf30-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="adf30-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="adf30-117">-DataFactoryName</span></span>
<span data-ttu-id="adf30-118">O nome do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="adf30-118">The data factory name.</span></span>

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

### <span data-ttu-id="adf30-119">-Force</span><span class="sxs-lookup"><span data-stu-id="adf30-119">-Force</span></span>
<span data-ttu-id="adf30-120">Executa o cmdlet sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="adf30-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="adf30-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="adf30-121">-Name</span></span>
<span data-ttu-id="adf30-122">O nome do disparador.</span><span class="sxs-lookup"><span data-stu-id="adf30-122">The trigger name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adf30-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="adf30-123">-ResourceGroupName</span></span>
<span data-ttu-id="adf30-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="adf30-124">The resource group name.</span></span>

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

### <span data-ttu-id="adf30-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="adf30-125">-ResourceId</span></span>
<span data-ttu-id="adf30-126">A ID do recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="adf30-126">The Azure resource ID.</span></span>

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

### <span data-ttu-id="adf30-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="adf30-127">-InputObject</span></span>
<span data-ttu-id="adf30-128">O objeto Trigger a ser removido.</span><span class="sxs-lookup"><span data-stu-id="adf30-128">The Trigger object to remove.</span></span>

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

### <span data-ttu-id="adf30-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="adf30-129">-WhatIf</span></span>
<span data-ttu-id="adf30-130">Mostra o que acontece se o cmdlet for executado, mas não executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="adf30-130">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="adf30-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="adf30-131">INPUTS</span></span>

### <span data-ttu-id="adf30-132">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="adf30-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>
<span data-ttu-id="adf30-133">System. String</span><span class="sxs-lookup"><span data-stu-id="adf30-133">System.String</span></span>


## <span data-ttu-id="adf30-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="adf30-134">OUTPUTS</span></span>

### <span data-ttu-id="adf30-135">System. Object</span><span class="sxs-lookup"><span data-stu-id="adf30-135">System.Object</span></span>

## <span data-ttu-id="adf30-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="adf30-136">NOTES</span></span>

## <span data-ttu-id="adf30-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="adf30-137">RELATED LINKS</span></span>
[<span data-ttu-id="adf30-138">Get-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="adf30-138">Get-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="adf30-139">Set-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="adf30-139">Set-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="adf30-140">Start-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="adf30-140">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="adf30-141">Parar-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="adf30-141">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

