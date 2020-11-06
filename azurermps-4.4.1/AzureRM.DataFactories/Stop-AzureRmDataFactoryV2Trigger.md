---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Stop-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Stop-AzureRmDataFactoryV2Trigger.md
ms.openlocfilehash: 8e4f547d615a88957ffbf133dd725e2453ef7a11
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93603385"
---
# <span data-ttu-id="95112-101">Stop-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="95112-101">Stop-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="95112-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="95112-102">SYNOPSIS</span></span>
<span data-ttu-id="95112-103">Interrompe um gatilho em uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="95112-103">Stops a trigger in a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="95112-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="95112-104">SYNTAX</span></span>

### <span data-ttu-id="95112-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="95112-105">ByFactoryName (Default)</span></span>
```
Stop-AzureRmDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95112-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="95112-106">ByInputObject</span></span>
```
Stop-AzureRmDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95112-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="95112-107">ByResourceId</span></span>
```
Stop-AzureRmDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95112-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="95112-108">DESCRIPTION</span></span>
<span data-ttu-id="95112-109">O cmdlet **Stop-AzureRmDataFactoryV2Trigger** interrompe um gatilho em uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="95112-109">The **Stop-AzureRmDataFactoryV2Trigger** cmdlet stops a trigger in a data factory.</span></span> <span data-ttu-id="95112-110">Se o gatilho estiver no estado ' iniciado ', o cmdlet para o gatilho e não invoca mais os pipelines.</span><span class="sxs-lookup"><span data-stu-id="95112-110">If the trigger is in the 'Started' state, the cmdlet stops the trigger and no longer invokes pipelines.</span></span> <span data-ttu-id="95112-111">Se o gatilho já estiver no estado ' interrompido ', esse cmdlet não terá efeito.</span><span class="sxs-lookup"><span data-stu-id="95112-111">If the trigger is already in the 'Stopped' state, this cmdlet has no effect.</span></span> <span data-ttu-id="95112-112">Se o parâmetro Force for especificado, o cmdlet não será avisado antes de parar o gatilho.</span><span class="sxs-lookup"><span data-stu-id="95112-112">If the Force parameter is specified, the cmdlet doesn't prompt before stopping the trigger.</span></span>

## <span data-ttu-id="95112-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="95112-113">EXAMPLES</span></span>

### <span data-ttu-id="95112-114">Exemplo 1: parar um gatilho</span><span class="sxs-lookup"><span data-stu-id="95112-114">Example 1: Stop a trigger</span></span>
```
Stop-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

Confirm
Are you sure you want to stop trigger 'ScheduledTrigger' in data factory 'TestFactory'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="95112-115">Interrompe um gatilho chamado "ScheduledTrigger" na fábrica de dados "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="95112-115">Stops a trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="95112-116">OS</span><span class="sxs-lookup"><span data-stu-id="95112-116">PARAMETERS</span></span>

### <span data-ttu-id="95112-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="95112-117">-Confirm</span></span>
<span data-ttu-id="95112-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="95112-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95112-119">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="95112-119">-DataFactoryName</span></span>
<span data-ttu-id="95112-120">O nome do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="95112-120">The data factory name.</span></span>

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

### <span data-ttu-id="95112-121">-Force</span><span class="sxs-lookup"><span data-stu-id="95112-121">-Force</span></span>
<span data-ttu-id="95112-122">Executa o cmdlet sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="95112-122">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="95112-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="95112-123">-Name</span></span>
<span data-ttu-id="95112-124">O nome do disparador.</span><span class="sxs-lookup"><span data-stu-id="95112-124">The trigger name.</span></span>

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

### <span data-ttu-id="95112-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95112-125">-ResourceGroupName</span></span>
<span data-ttu-id="95112-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="95112-126">The resource group name.</span></span>

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

### <span data-ttu-id="95112-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="95112-127">-ResourceId</span></span>
<span data-ttu-id="95112-128">A ID do recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="95112-128">The Azure resource ID.</span></span>

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

### <span data-ttu-id="95112-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="95112-129">-InputObject</span></span>
<span data-ttu-id="95112-130">Objeto Trigger para iniciar.</span><span class="sxs-lookup"><span data-stu-id="95112-130">Trigger object to start.</span></span>

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

### <span data-ttu-id="95112-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95112-131">-WhatIf</span></span>
<span data-ttu-id="95112-132">Mostra o que acontece se o cmdlet for executado, mas não executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="95112-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="95112-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95112-133">-DefaultProfile</span></span>
<span data-ttu-id="95112-134">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="95112-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95112-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95112-135">CommonParameters</span></span>
<span data-ttu-id="95112-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95112-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95112-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95112-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95112-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="95112-138">INPUTS</span></span>

### <span data-ttu-id="95112-139">System. String</span><span class="sxs-lookup"><span data-stu-id="95112-139">System.String</span></span>
<span data-ttu-id="95112-140">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="95112-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="95112-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="95112-141">OUTPUTS</span></span>

### <span data-ttu-id="95112-142">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="95112-142">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="95112-143">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="95112-143">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="95112-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="95112-144">NOTES</span></span>

## <span data-ttu-id="95112-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="95112-145">RELATED LINKS</span></span>

[<span data-ttu-id="95112-146">Get-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="95112-146">Get-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="95112-147">Set-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="95112-147">Set-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="95112-148">Start-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="95112-148">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="95112-149">Remove-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="95112-149">Remove-AzureRmDataFactoryV2Trigger</span></span>]()
