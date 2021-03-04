---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/start-azdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2Trigger.md
ms.openlocfilehash: d9ce325979a40315341a0e43049bd2c5bb512622
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886997"
---
# <span data-ttu-id="faf02-101">Start-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="faf02-101">Start-AzDataFactoryV2Trigger</span></span>

## <span data-ttu-id="faf02-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="faf02-102">SYNOPSIS</span></span>
<span data-ttu-id="faf02-103">Inicia um gatilho em um fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="faf02-103">Starts a trigger in a data factory.</span></span>

## <span data-ttu-id="faf02-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="faf02-104">SYNTAX</span></span>

### <span data-ttu-id="faf02-105">ByFactoryName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="faf02-105">ByFactoryName (Default)</span></span>
```
Start-AzDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="faf02-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="faf02-106">ByInputObject</span></span>
```
Start-AzDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="faf02-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="faf02-107">ByResourceId</span></span>
```
Start-AzDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="faf02-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="faf02-108">DESCRIPTION</span></span>
<span data-ttu-id="faf02-109">O cmdlet **Start-AzDataFactoryV2Trigger** inicia um gatilho em um fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="faf02-109">The **Start-AzDataFactoryV2Trigger** cmdlet starts a trigger in a data factory.</span></span> <span data-ttu-id="faf02-110">Se o gatilho estiver no estado 'Parado', o cmdlet iniciará o gatilho e, eventualmente, invocará pipelines com base em sua definição.</span><span class="sxs-lookup"><span data-stu-id="faf02-110">If the trigger is in the 'Stopped' state, the cmdlet starts the trigger and it eventually invokes pipelines based on its definition.</span></span> <span data-ttu-id="faf02-111">Se o gatilho já estiver no estado 'Iniciado', esse cmdlet não terá efeito.</span><span class="sxs-lookup"><span data-stu-id="faf02-111">If the trigger is already in the 'Started' state, this cmdlet has no effect.</span></span> <span data-ttu-id="faf02-112">Se o parâmetro Force for especificado, o cmdlet não solicitará antes de iniciar o gatilho.</span><span class="sxs-lookup"><span data-stu-id="faf02-112">If the Force parameter is specified, the cmdlet doesn't prompt before starting the trigger.</span></span>

## <span data-ttu-id="faf02-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="faf02-113">EXAMPLES</span></span>

### <span data-ttu-id="faf02-114">Exemplo 1: Iniciar um gatilho</span><span class="sxs-lookup"><span data-stu-id="faf02-114">Example 1: Start a trigger</span></span>
```
Start-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

Confirm
Are you sure you want to start trigger 'ScheduledTrigger' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="faf02-115">Inicia um gatilho chamado "ScheduledTrigger" no fábrica de dados "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="faf02-115">Starts a trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="faf02-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="faf02-116">PARAMETERS</span></span>

### <span data-ttu-id="faf02-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="faf02-117">-DataFactoryName</span></span>
<span data-ttu-id="faf02-118">O nome da fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="faf02-118">The data factory name.</span></span>

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

### <span data-ttu-id="faf02-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="faf02-119">-DefaultProfile</span></span>
<span data-ttu-id="faf02-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="faf02-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="faf02-121">-Force</span><span class="sxs-lookup"><span data-stu-id="faf02-121">-Force</span></span>
<span data-ttu-id="faf02-122">Executa o cmdlet sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="faf02-122">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="faf02-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="faf02-123">-InputObject</span></span>
<span data-ttu-id="faf02-124">Objeto Trigger para iniciar.</span><span class="sxs-lookup"><span data-stu-id="faf02-124">Trigger object to start.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="faf02-125">-Name</span><span class="sxs-lookup"><span data-stu-id="faf02-125">-Name</span></span>
<span data-ttu-id="faf02-126">O nome do gatilho.</span><span class="sxs-lookup"><span data-stu-id="faf02-126">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="faf02-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="faf02-127">-ResourceGroupName</span></span>
<span data-ttu-id="faf02-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="faf02-128">The resource group name.</span></span>

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

### <span data-ttu-id="faf02-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="faf02-129">-ResourceId</span></span>
<span data-ttu-id="faf02-130">A ID de recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="faf02-130">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="faf02-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="faf02-131">-Confirm</span></span>
<span data-ttu-id="faf02-132">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="faf02-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="faf02-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="faf02-133">-WhatIf</span></span>
<span data-ttu-id="faf02-134">Mostra o que acontece se o cmdlet for executado, mas não executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="faf02-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="faf02-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="faf02-135">CommonParameters</span></span>
<span data-ttu-id="faf02-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="faf02-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="faf02-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="faf02-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="faf02-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="faf02-138">INPUTS</span></span>

### <span data-ttu-id="faf02-139">System.String</span><span class="sxs-lookup"><span data-stu-id="faf02-139">System.String</span></span>

### <span data-ttu-id="faf02-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span><span class="sxs-lookup"><span data-stu-id="faf02-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="faf02-141">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="faf02-141">OUTPUTS</span></span>

### <span data-ttu-id="faf02-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span><span class="sxs-lookup"><span data-stu-id="faf02-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="faf02-143">NOTES</span><span class="sxs-lookup"><span data-stu-id="faf02-143">NOTES</span></span>

## <span data-ttu-id="faf02-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="faf02-144">RELATED LINKS</span></span>

[<span data-ttu-id="faf02-145">Get-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="faf02-145">Get-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="faf02-146">Set-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="faf02-146">Set-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="faf02-147">Stop-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="faf02-147">Stop-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="faf02-148">Remove-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="faf02-148">Remove-AzDataFactoryV2Trigger</span></span>]()
