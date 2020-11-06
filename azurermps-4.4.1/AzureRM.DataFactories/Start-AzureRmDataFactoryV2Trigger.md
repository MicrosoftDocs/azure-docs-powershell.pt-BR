---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Start-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Start-AzureRmDataFactoryV2Trigger.md
ms.openlocfilehash: d49e04f4a791f6cbf5d609d6553fddcc26dc34e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93603388"
---
# <span data-ttu-id="3e2a5-101">Start-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="3e2a5-101">Start-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="3e2a5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3e2a5-102">SYNOPSIS</span></span>
<span data-ttu-id="3e2a5-103">Inicia um gatilho em uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="3e2a5-103">Starts a trigger in a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3e2a5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3e2a5-104">SYNTAX</span></span>

### <span data-ttu-id="3e2a5-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="3e2a5-105">ByFactoryName (Default)</span></span>
```
Start-AzureRmDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e2a5-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="3e2a5-106">ByInputObject</span></span>
```
Start-AzureRmDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e2a5-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3e2a5-107">ByResourceId</span></span>
```
Start-AzureRmDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e2a5-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3e2a5-108">DESCRIPTION</span></span>
<span data-ttu-id="3e2a5-109">O cmdlet **Start-AzureRmDataFactoryV2Trigger** inicia um gatilho em uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="3e2a5-109">The **Start-AzureRmDataFactoryV2Trigger** cmdlet starts a trigger in a data factory.</span></span> <span data-ttu-id="3e2a5-110">Se o gatilho estiver no estado ' parado ', o cmdlet iniciará o gatilho e eventualmente invocará os pipelines com base em sua definição.</span><span class="sxs-lookup"><span data-stu-id="3e2a5-110">If the trigger is in the 'Stopped' state, the cmdlet starts the trigger and it eventually invokes pipelines based on its definition.</span></span> <span data-ttu-id="3e2a5-111">Se o gatilho já estiver no estado ' iniciado ', esse cmdlet não terá efeito.</span><span class="sxs-lookup"><span data-stu-id="3e2a5-111">If the trigger is already in the 'Started' state, this cmdlet has no effect.</span></span> <span data-ttu-id="3e2a5-112">Se o parâmetro Force for especificado, o cmdlet não avisa antes de iniciar o gatilho.</span><span class="sxs-lookup"><span data-stu-id="3e2a5-112">If the Force parameter is specified, the cmdlet doesn't prompt before starting the trigger.</span></span>

## <span data-ttu-id="3e2a5-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3e2a5-113">EXAMPLES</span></span>

### <span data-ttu-id="3e2a5-114">Exemplo 1: iniciar um gatilho</span><span class="sxs-lookup"><span data-stu-id="3e2a5-114">Example 1: Start a trigger</span></span>
```
Start-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

Confirm
Are you sure you want to start trigger 'ScheduledTrigger' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="3e2a5-115">Inicia um gatilho chamado "ScheduledTrigger" na fábrica de dados "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="3e2a5-115">Starts a trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="3e2a5-116">OS</span><span class="sxs-lookup"><span data-stu-id="3e2a5-116">PARAMETERS</span></span>

### <span data-ttu-id="3e2a5-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3e2a5-117">-Confirm</span></span>
<span data-ttu-id="3e2a5-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e2a5-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e2a5-119">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="3e2a5-119">-DataFactoryName</span></span>
<span data-ttu-id="3e2a5-120">O nome do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="3e2a5-120">The data factory name.</span></span>

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

### <span data-ttu-id="3e2a5-121">-Force</span><span class="sxs-lookup"><span data-stu-id="3e2a5-121">-Force</span></span>
<span data-ttu-id="3e2a5-122">Executa o cmdlet sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="3e2a5-122">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="3e2a5-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="3e2a5-123">-Name</span></span>
<span data-ttu-id="3e2a5-124">O nome do disparador.</span><span class="sxs-lookup"><span data-stu-id="3e2a5-124">The trigger name.</span></span>

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

### <span data-ttu-id="3e2a5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e2a5-125">-ResourceGroupName</span></span>
<span data-ttu-id="3e2a5-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3e2a5-126">The resource group name.</span></span>

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

### <span data-ttu-id="3e2a5-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3e2a5-127">-ResourceId</span></span>
<span data-ttu-id="3e2a5-128">A ID do recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="3e2a5-128">The Azure resource ID.</span></span>

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

### <span data-ttu-id="3e2a5-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3e2a5-129">-InputObject</span></span>
<span data-ttu-id="3e2a5-130">Objeto Trigger para iniciar.</span><span class="sxs-lookup"><span data-stu-id="3e2a5-130">Trigger object to start.</span></span>

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

### <span data-ttu-id="3e2a5-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e2a5-131">-WhatIf</span></span>
<span data-ttu-id="3e2a5-132">Mostra o que acontece se o cmdlet for executado, mas não executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e2a5-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="3e2a5-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e2a5-133">-DefaultProfile</span></span>
<span data-ttu-id="3e2a5-134">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3e2a5-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e2a5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e2a5-135">CommonParameters</span></span>
<span data-ttu-id="3e2a5-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e2a5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e2a5-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e2a5-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e2a5-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3e2a5-138">INPUTS</span></span>

### <span data-ttu-id="3e2a5-139">System. String</span><span class="sxs-lookup"><span data-stu-id="3e2a5-139">System.String</span></span>
<span data-ttu-id="3e2a5-140">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="3e2a5-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="3e2a5-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3e2a5-141">OUTPUTS</span></span>

### <span data-ttu-id="3e2a5-142">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="3e2a5-142">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="3e2a5-143">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="3e2a5-143">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="3e2a5-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3e2a5-144">NOTES</span></span>

## <span data-ttu-id="3e2a5-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3e2a5-145">RELATED LINKS</span></span>

[<span data-ttu-id="3e2a5-146">Get-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="3e2a5-146">Get-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="3e2a5-147">Set-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="3e2a5-147">Set-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="3e2a5-148">Parar-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="3e2a5-148">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="3e2a5-149">Remove-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="3e2a5-149">Remove-AzureRmDataFactoryV2Trigger</span></span>]()
