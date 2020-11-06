---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/start-azdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2Trigger.md
ms.openlocfilehash: 988f63d9f894de95c4206dc05bcda66e68f3c4ea
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93601110"
---
# <span data-ttu-id="23482-101">Start-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="23482-101">Start-AzDataFactoryV2Trigger</span></span>

## <span data-ttu-id="23482-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="23482-102">SYNOPSIS</span></span>
<span data-ttu-id="23482-103">Inicia um gatilho em uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="23482-103">Starts a trigger in a data factory.</span></span>

## <span data-ttu-id="23482-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="23482-104">SYNTAX</span></span>

### <span data-ttu-id="23482-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="23482-105">ByFactoryName (Default)</span></span>
```
Start-AzDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23482-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="23482-106">ByInputObject</span></span>
```
Start-AzDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23482-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="23482-107">ByResourceId</span></span>
```
Start-AzDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23482-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="23482-108">DESCRIPTION</span></span>
<span data-ttu-id="23482-109">O cmdlet **Start-AzDataFactoryV2Trigger** inicia um gatilho em uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="23482-109">The **Start-AzDataFactoryV2Trigger** cmdlet starts a trigger in a data factory.</span></span> <span data-ttu-id="23482-110">Se o gatilho estiver no estado ' parado ', o cmdlet iniciará o gatilho e eventualmente invocará os pipelines com base em sua definição.</span><span class="sxs-lookup"><span data-stu-id="23482-110">If the trigger is in the 'Stopped' state, the cmdlet starts the trigger and it eventually invokes pipelines based on its definition.</span></span> <span data-ttu-id="23482-111">Se o gatilho já estiver no estado ' iniciado ', esse cmdlet não terá efeito.</span><span class="sxs-lookup"><span data-stu-id="23482-111">If the trigger is already in the 'Started' state, this cmdlet has no effect.</span></span> <span data-ttu-id="23482-112">Se o parâmetro Force for especificado, o cmdlet não avisa antes de iniciar o gatilho.</span><span class="sxs-lookup"><span data-stu-id="23482-112">If the Force parameter is specified, the cmdlet doesn't prompt before starting the trigger.</span></span>

## <span data-ttu-id="23482-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="23482-113">EXAMPLES</span></span>

### <span data-ttu-id="23482-114">Exemplo 1: iniciar um gatilho</span><span class="sxs-lookup"><span data-stu-id="23482-114">Example 1: Start a trigger</span></span>
```
Start-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

Confirm
Are you sure you want to start trigger 'ScheduledTrigger' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="23482-115">Inicia um gatilho chamado "ScheduledTrigger" na fábrica de dados "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="23482-115">Starts a trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="23482-116">OS</span><span class="sxs-lookup"><span data-stu-id="23482-116">PARAMETERS</span></span>

### <span data-ttu-id="23482-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="23482-117">-DataFactoryName</span></span>
<span data-ttu-id="23482-118">O nome do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="23482-118">The data factory name.</span></span>

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

### <span data-ttu-id="23482-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23482-119">-DefaultProfile</span></span>
<span data-ttu-id="23482-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="23482-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23482-121">-Force</span><span class="sxs-lookup"><span data-stu-id="23482-121">-Force</span></span>
<span data-ttu-id="23482-122">Executa o cmdlet sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="23482-122">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="23482-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="23482-123">-InputObject</span></span>
<span data-ttu-id="23482-124">Objeto Trigger para iniciar.</span><span class="sxs-lookup"><span data-stu-id="23482-124">Trigger object to start.</span></span>

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

### <span data-ttu-id="23482-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="23482-125">-Name</span></span>
<span data-ttu-id="23482-126">O nome do disparador.</span><span class="sxs-lookup"><span data-stu-id="23482-126">The trigger name.</span></span>

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

### <span data-ttu-id="23482-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23482-127">-ResourceGroupName</span></span>
<span data-ttu-id="23482-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="23482-128">The resource group name.</span></span>

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

### <span data-ttu-id="23482-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="23482-129">-ResourceId</span></span>
<span data-ttu-id="23482-130">A ID do recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="23482-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="23482-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="23482-131">-Confirm</span></span>
<span data-ttu-id="23482-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23482-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23482-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23482-133">-WhatIf</span></span>
<span data-ttu-id="23482-134">Mostra o que acontece se o cmdlet for executado, mas não executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23482-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="23482-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23482-135">CommonParameters</span></span>
<span data-ttu-id="23482-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23482-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23482-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23482-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23482-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="23482-138">INPUTS</span></span>

### <span data-ttu-id="23482-139">System. String</span><span class="sxs-lookup"><span data-stu-id="23482-139">System.String</span></span>

### <span data-ttu-id="23482-140">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="23482-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="23482-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="23482-141">OUTPUTS</span></span>

### <span data-ttu-id="23482-142">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="23482-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="23482-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="23482-143">NOTES</span></span>

## <span data-ttu-id="23482-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="23482-144">RELATED LINKS</span></span>

[<span data-ttu-id="23482-145">Get-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="23482-145">Get-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="23482-146">Set-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="23482-146">Set-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="23482-147">Parar-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="23482-147">Stop-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="23482-148">Remove-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="23482-148">Remove-AzDataFactoryV2Trigger</span></span>]()
