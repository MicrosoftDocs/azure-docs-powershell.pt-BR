---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/stop-azdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2Trigger.md
ms.openlocfilehash: 80e9ed345b9d1b80dd75be2036826559ac3bbb9a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94280944"
---
# <span data-ttu-id="8665d-101">Stop-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="8665d-101">Stop-AzDataFactoryV2Trigger</span></span>

## <span data-ttu-id="8665d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8665d-102">SYNOPSIS</span></span>
<span data-ttu-id="8665d-103">Interrompe um gatilho em uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="8665d-103">Stops a trigger in a data factory.</span></span>

## <span data-ttu-id="8665d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8665d-104">SYNTAX</span></span>

### <span data-ttu-id="8665d-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="8665d-105">ByFactoryName (Default)</span></span>
```
Stop-AzDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8665d-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="8665d-106">ByInputObject</span></span>
```
Stop-AzDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8665d-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8665d-107">ByResourceId</span></span>
```
Stop-AzDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8665d-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8665d-108">DESCRIPTION</span></span>
<span data-ttu-id="8665d-109">O cmdlet **Stop-AzDataFactoryV2Trigger** interrompe um gatilho em uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="8665d-109">The **Stop-AzDataFactoryV2Trigger** cmdlet stops a trigger in a data factory.</span></span> <span data-ttu-id="8665d-110">Se o gatilho estiver no estado ' iniciado ', o cmdlet para o gatilho e não invoca mais os pipelines.</span><span class="sxs-lookup"><span data-stu-id="8665d-110">If the trigger is in the 'Started' state, the cmdlet stops the trigger and no longer invokes pipelines.</span></span> <span data-ttu-id="8665d-111">Se o gatilho já estiver no estado ' interrompido ', esse cmdlet não terá efeito.</span><span class="sxs-lookup"><span data-stu-id="8665d-111">If the trigger is already in the 'Stopped' state, this cmdlet has no effect.</span></span> <span data-ttu-id="8665d-112">Se o parâmetro Force for especificado, o cmdlet não será avisado antes de parar o gatilho.</span><span class="sxs-lookup"><span data-stu-id="8665d-112">If the Force parameter is specified, the cmdlet doesn't prompt before stopping the trigger.</span></span>

## <span data-ttu-id="8665d-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8665d-113">EXAMPLES</span></span>

### <span data-ttu-id="8665d-114">Exemplo 1: parar um gatilho</span><span class="sxs-lookup"><span data-stu-id="8665d-114">Example 1: Stop a trigger</span></span>
```
Stop-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

Confirm
Are you sure you want to stop trigger 'ScheduledTrigger' in data factory 'TestFactory'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="8665d-115">Interrompe um gatilho chamado "ScheduledTrigger" na fábrica de dados "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="8665d-115">Stops a trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="8665d-116">OS</span><span class="sxs-lookup"><span data-stu-id="8665d-116">PARAMETERS</span></span>

### <span data-ttu-id="8665d-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="8665d-117">-DataFactoryName</span></span>
<span data-ttu-id="8665d-118">O nome do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="8665d-118">The data factory name.</span></span>

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

### <span data-ttu-id="8665d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8665d-119">-DefaultProfile</span></span>
<span data-ttu-id="8665d-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8665d-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8665d-121">-Force</span><span class="sxs-lookup"><span data-stu-id="8665d-121">-Force</span></span>
<span data-ttu-id="8665d-122">Executa o cmdlet sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="8665d-122">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="8665d-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8665d-123">-InputObject</span></span>
<span data-ttu-id="8665d-124">Objeto Trigger para iniciar.</span><span class="sxs-lookup"><span data-stu-id="8665d-124">Trigger object to start.</span></span>

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

### <span data-ttu-id="8665d-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="8665d-125">-Name</span></span>
<span data-ttu-id="8665d-126">O nome do disparador.</span><span class="sxs-lookup"><span data-stu-id="8665d-126">The trigger name.</span></span>

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

### <span data-ttu-id="8665d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8665d-127">-ResourceGroupName</span></span>
<span data-ttu-id="8665d-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8665d-128">The resource group name.</span></span>

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

### <span data-ttu-id="8665d-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8665d-129">-ResourceId</span></span>
<span data-ttu-id="8665d-130">A ID do recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="8665d-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="8665d-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8665d-131">-Confirm</span></span>
<span data-ttu-id="8665d-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8665d-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8665d-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8665d-133">-WhatIf</span></span>
<span data-ttu-id="8665d-134">Mostra o que acontece se o cmdlet for executado, mas não executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8665d-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="8665d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8665d-135">CommonParameters</span></span>
<span data-ttu-id="8665d-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8665d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8665d-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8665d-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8665d-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8665d-138">INPUTS</span></span>

### <span data-ttu-id="8665d-139">System. String</span><span class="sxs-lookup"><span data-stu-id="8665d-139">System.String</span></span>

### <span data-ttu-id="8665d-140">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="8665d-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="8665d-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8665d-141">OUTPUTS</span></span>

### <span data-ttu-id="8665d-142">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="8665d-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="8665d-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8665d-143">NOTES</span></span>

## <span data-ttu-id="8665d-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8665d-144">RELATED LINKS</span></span>

[<span data-ttu-id="8665d-145">Get-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="8665d-145">Get-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="8665d-146">Set-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="8665d-146">Set-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="8665d-147">Start-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="8665d-147">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="8665d-148">Remove-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="8665d-148">Remove-AzDataFactoryV2Trigger</span></span>]()
