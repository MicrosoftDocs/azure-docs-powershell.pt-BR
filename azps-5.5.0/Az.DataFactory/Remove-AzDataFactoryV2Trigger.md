---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Trigger.md
ms.openlocfilehash: d5426decba60df0e18e331c01481ae4f99d5c27c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116425"
---
# <span data-ttu-id="9f12b-101">Remove-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="9f12b-101">Remove-AzDataFactoryV2Trigger</span></span>

## <span data-ttu-id="9f12b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9f12b-102">SYNOPSIS</span></span>
<span data-ttu-id="9f12b-103">Remove um gatilho de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="9f12b-103">Removes a trigger from a data factory.</span></span>

## <span data-ttu-id="9f12b-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9f12b-104">SYNTAX</span></span>

### <span data-ttu-id="9f12b-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="9f12b-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f12b-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="9f12b-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f12b-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="9f12b-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f12b-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="9f12b-108">DESCRIPTION</span></span>
<span data-ttu-id="9f12b-109">O cmdlet **Remove-AzDataFactoryV2Triory** remove um gatilho de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="9f12b-109">The **Remove-AzDataFactoryV2Trigger** cmdlet removes a trigger from a data factory.</span></span> <span data-ttu-id="9f12b-110">Se o _parâmetro Forçar_ for especificado, o cmdlet não solicitará antes de remover o gatilho.</span><span class="sxs-lookup"><span data-stu-id="9f12b-110">If the _Force_ parameter is specified, the cmdlet doesn't prompt before removing the trigger.</span></span>

## <span data-ttu-id="9f12b-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9f12b-111">EXAMPLES</span></span>

### <span data-ttu-id="9f12b-112">Exemplo 1: Remover um gatilho</span><span class="sxs-lookup"><span data-stu-id="9f12b-112">Example 1: Remove a trigger</span></span>
```
Remove-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "ScheduledTrigger"

Confirm
Are you sure you want to remove trigger 'ScheduledTrigger' in data factory 'TestFactory'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="9f12b-113">Remova um gatilho chamado "ScheduledTrigger" do fábrica de dados "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="9f12b-113">Remove a trigger called "ScheduledTrigger" from the data factory "WikiADF".</span></span>

## <span data-ttu-id="9f12b-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9f12b-114">PARAMETERS</span></span>

### <span data-ttu-id="9f12b-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="9f12b-115">-DataFactoryName</span></span>
<span data-ttu-id="9f12b-116">O nome da fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="9f12b-116">The data factory name.</span></span>

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

### <span data-ttu-id="9f12b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f12b-117">-DefaultProfile</span></span>
<span data-ttu-id="9f12b-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="9f12b-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9f12b-119">-Forçar</span><span class="sxs-lookup"><span data-stu-id="9f12b-119">-Force</span></span>
<span data-ttu-id="9f12b-120">Executa o cmdlet sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="9f12b-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="9f12b-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9f12b-121">-InputObject</span></span>
<span data-ttu-id="9f12b-122">O objeto Trigger a ser removido.</span><span class="sxs-lookup"><span data-stu-id="9f12b-122">The Trigger object to remove.</span></span>

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

### <span data-ttu-id="9f12b-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="9f12b-123">-Name</span></span>
<span data-ttu-id="9f12b-124">O nome do gatilho.</span><span class="sxs-lookup"><span data-stu-id="9f12b-124">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f12b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f12b-125">-ResourceGroupName</span></span>
<span data-ttu-id="9f12b-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9f12b-126">The resource group name.</span></span>

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

### <span data-ttu-id="9f12b-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9f12b-127">-ResourceId</span></span>
<span data-ttu-id="9f12b-128">A ID de recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="9f12b-128">The Azure resource ID.</span></span>

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

### <span data-ttu-id="9f12b-129">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="9f12b-129">-Confirm</span></span>
<span data-ttu-id="9f12b-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9f12b-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f12b-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f12b-131">-WhatIf</span></span>
<span data-ttu-id="9f12b-132">Mostra o que acontece se o cmdlet é executado, mas não executa o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9f12b-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="9f12b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f12b-133">CommonParameters</span></span>
<span data-ttu-id="9f12b-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f12b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f12b-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f12b-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f12b-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="9f12b-136">INPUTS</span></span>

### <span data-ttu-id="9f12b-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriory</span><span class="sxs-lookup"><span data-stu-id="9f12b-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

### <span data-ttu-id="9f12b-138">System.String</span><span class="sxs-lookup"><span data-stu-id="9f12b-138">System.String</span></span>

## <span data-ttu-id="9f12b-139">Saídas</span><span class="sxs-lookup"><span data-stu-id="9f12b-139">OUTPUTS</span></span>

### <span data-ttu-id="9f12b-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9f12b-140">System.Boolean</span></span>

## <span data-ttu-id="9f12b-141">Notas</span><span class="sxs-lookup"><span data-stu-id="9f12b-141">NOTES</span></span>

## <span data-ttu-id="9f12b-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9f12b-142">RELATED LINKS</span></span>

[<span data-ttu-id="9f12b-143">Get-AzDataFactoryV2Triory</span><span class="sxs-lookup"><span data-stu-id="9f12b-143">Get-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="9f12b-144">Set-AzDataFactoryV2Triory</span><span class="sxs-lookup"><span data-stu-id="9f12b-144">Set-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="9f12b-145">Start-AzDataFactoryV2Triory</span><span class="sxs-lookup"><span data-stu-id="9f12b-145">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="9f12b-146">Stop-AzDataFactoryV2Triory</span><span class="sxs-lookup"><span data-stu-id="9f12b-146">Stop-AzDataFactoryV2Trigger</span></span>]()

