---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/stop-azdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2Trigger.md
ms.openlocfilehash: 80e9ed345b9d1b80dd75be2036826559ac3bbb9a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111001"
---
# <span data-ttu-id="64055-101">Stop-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="64055-101">Stop-AzDataFactoryV2Trigger</span></span>

## <span data-ttu-id="64055-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="64055-102">SYNOPSIS</span></span>
<span data-ttu-id="64055-103">Interrompe um gatilho em uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="64055-103">Stops a trigger in a data factory.</span></span>

## <span data-ttu-id="64055-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="64055-104">SYNTAX</span></span>

### <span data-ttu-id="64055-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="64055-105">ByFactoryName (Default)</span></span>
```
Stop-AzDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64055-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="64055-106">ByInputObject</span></span>
```
Stop-AzDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64055-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="64055-107">ByResourceId</span></span>
```
Stop-AzDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64055-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="64055-108">DESCRIPTION</span></span>
<span data-ttu-id="64055-109">O cmdlet **Stop-AzDataFactoryV2Triory** interrompe um gatilho em uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="64055-109">The **Stop-AzDataFactoryV2Trigger** cmdlet stops a trigger in a data factory.</span></span> <span data-ttu-id="64055-110">Se o gatilho estiver no estado "Iniciado", o cmdlet parará o gatilho e não invocará mais os pipelines.</span><span class="sxs-lookup"><span data-stu-id="64055-110">If the trigger is in the 'Started' state, the cmdlet stops the trigger and no longer invokes pipelines.</span></span> <span data-ttu-id="64055-111">Se o gatilho já estiver no estado "Parado", esse cmdlet não terá efeito.</span><span class="sxs-lookup"><span data-stu-id="64055-111">If the trigger is already in the 'Stopped' state, this cmdlet has no effect.</span></span> <span data-ttu-id="64055-112">Se o parâmetro Forçar for especificado, o cmdlet não solicitará antes de interromper o gatilho.</span><span class="sxs-lookup"><span data-stu-id="64055-112">If the Force parameter is specified, the cmdlet doesn't prompt before stopping the trigger.</span></span>

## <span data-ttu-id="64055-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="64055-113">EXAMPLES</span></span>

### <span data-ttu-id="64055-114">Exemplo 1: Parar um gatilho</span><span class="sxs-lookup"><span data-stu-id="64055-114">Example 1: Stop a trigger</span></span>
```
Stop-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

Confirm
Are you sure you want to stop trigger 'ScheduledTrigger' in data factory 'TestFactory'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="64055-115">Interrompe um gatilho chamado "ScheduledTri wiki" no fábrica de dados "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="64055-115">Stops a trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="64055-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="64055-116">PARAMETERS</span></span>

### <span data-ttu-id="64055-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="64055-117">-DataFactoryName</span></span>
<span data-ttu-id="64055-118">O nome da fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="64055-118">The data factory name.</span></span>

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

### <span data-ttu-id="64055-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64055-119">-DefaultProfile</span></span>
<span data-ttu-id="64055-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="64055-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="64055-121">-Forçar</span><span class="sxs-lookup"><span data-stu-id="64055-121">-Force</span></span>
<span data-ttu-id="64055-122">Executa o cmdlet sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="64055-122">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="64055-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="64055-123">-InputObject</span></span>
<span data-ttu-id="64055-124">Disparar objeto para iniciar.</span><span class="sxs-lookup"><span data-stu-id="64055-124">Trigger object to start.</span></span>

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

### <span data-ttu-id="64055-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="64055-125">-Name</span></span>
<span data-ttu-id="64055-126">O nome do gatilho.</span><span class="sxs-lookup"><span data-stu-id="64055-126">The trigger name.</span></span>

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

### <span data-ttu-id="64055-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64055-127">-ResourceGroupName</span></span>
<span data-ttu-id="64055-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="64055-128">The resource group name.</span></span>

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

### <span data-ttu-id="64055-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="64055-129">-ResourceId</span></span>
<span data-ttu-id="64055-130">A ID de recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="64055-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="64055-131">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="64055-131">-Confirm</span></span>
<span data-ttu-id="64055-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64055-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64055-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64055-133">-WhatIf</span></span>
<span data-ttu-id="64055-134">Mostra o que acontece se o cmdlet é executado, mas não executa o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64055-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="64055-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64055-135">CommonParameters</span></span>
<span data-ttu-id="64055-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64055-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64055-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64055-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64055-138">Entradas</span><span class="sxs-lookup"><span data-stu-id="64055-138">INPUTS</span></span>

### <span data-ttu-id="64055-139">System.String</span><span class="sxs-lookup"><span data-stu-id="64055-139">System.String</span></span>

### <span data-ttu-id="64055-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriory</span><span class="sxs-lookup"><span data-stu-id="64055-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="64055-141">Saídas</span><span class="sxs-lookup"><span data-stu-id="64055-141">OUTPUTS</span></span>

### <span data-ttu-id="64055-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriory</span><span class="sxs-lookup"><span data-stu-id="64055-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="64055-143">Notas</span><span class="sxs-lookup"><span data-stu-id="64055-143">NOTES</span></span>

## <span data-ttu-id="64055-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="64055-144">RELATED LINKS</span></span>

[<span data-ttu-id="64055-145">Get-AzDataFactoryV2Triory</span><span class="sxs-lookup"><span data-stu-id="64055-145">Get-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="64055-146">Set-AzDataFactoryV2Triory</span><span class="sxs-lookup"><span data-stu-id="64055-146">Set-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="64055-147">Start-AzDataFactoryV2Triory</span><span class="sxs-lookup"><span data-stu-id="64055-147">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="64055-148">Remove-AzDataFactoryV2Triory</span><span class="sxs-lookup"><span data-stu-id="64055-148">Remove-AzDataFactoryV2Trigger</span></span>]()
