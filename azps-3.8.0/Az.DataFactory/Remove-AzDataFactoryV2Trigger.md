---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Trigger.md
ms.openlocfilehash: d5426decba60df0e18e331c01481ae4f99d5c27c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93778304"
---
# <span data-ttu-id="24684-101">Remove-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="24684-101">Remove-AzDataFactoryV2Trigger</span></span>

## <span data-ttu-id="24684-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="24684-102">SYNOPSIS</span></span>
<span data-ttu-id="24684-103">Remove um gatilho de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="24684-103">Removes a trigger from a data factory.</span></span>

## <span data-ttu-id="24684-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="24684-104">SYNTAX</span></span>

### <span data-ttu-id="24684-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="24684-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24684-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="24684-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24684-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="24684-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24684-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="24684-108">DESCRIPTION</span></span>
<span data-ttu-id="24684-109">O cmdlet **Remove-AzDataFactoryV2Trigger** remove um gatilho de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="24684-109">The **Remove-AzDataFactoryV2Trigger** cmdlet removes a trigger from a data factory.</span></span> <span data-ttu-id="24684-110">Se o parâmetro _Force_ for especificado, o cmdlet não avisa antes de remover o gatilho.</span><span class="sxs-lookup"><span data-stu-id="24684-110">If the _Force_ parameter is specified, the cmdlet doesn't prompt before removing the trigger.</span></span>

## <span data-ttu-id="24684-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="24684-111">EXAMPLES</span></span>

### <span data-ttu-id="24684-112">Exemplo 1: remover um gatilho</span><span class="sxs-lookup"><span data-stu-id="24684-112">Example 1: Remove a trigger</span></span>
```
Remove-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "ScheduledTrigger"

Confirm
Are you sure you want to remove trigger 'ScheduledTrigger' in data factory 'TestFactory'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="24684-113">Remova um gatilho chamado "ScheduledTrigger" da fábrica de dados "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="24684-113">Remove a trigger called "ScheduledTrigger" from the data factory "WikiADF".</span></span>

## <span data-ttu-id="24684-114">OS</span><span class="sxs-lookup"><span data-stu-id="24684-114">PARAMETERS</span></span>

### <span data-ttu-id="24684-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="24684-115">-DataFactoryName</span></span>
<span data-ttu-id="24684-116">O nome do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="24684-116">The data factory name.</span></span>

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

### <span data-ttu-id="24684-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24684-117">-DefaultProfile</span></span>
<span data-ttu-id="24684-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="24684-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24684-119">-Force</span><span class="sxs-lookup"><span data-stu-id="24684-119">-Force</span></span>
<span data-ttu-id="24684-120">Executa o cmdlet sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="24684-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="24684-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="24684-121">-InputObject</span></span>
<span data-ttu-id="24684-122">O objeto Trigger a ser removido.</span><span class="sxs-lookup"><span data-stu-id="24684-122">The Trigger object to remove.</span></span>

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

### <span data-ttu-id="24684-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="24684-123">-Name</span></span>
<span data-ttu-id="24684-124">O nome do disparador.</span><span class="sxs-lookup"><span data-stu-id="24684-124">The trigger name.</span></span>

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

### <span data-ttu-id="24684-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24684-125">-ResourceGroupName</span></span>
<span data-ttu-id="24684-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="24684-126">The resource group name.</span></span>

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

### <span data-ttu-id="24684-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="24684-127">-ResourceId</span></span>
<span data-ttu-id="24684-128">A ID do recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="24684-128">The Azure resource ID.</span></span>

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

### <span data-ttu-id="24684-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="24684-129">-Confirm</span></span>
<span data-ttu-id="24684-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24684-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24684-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24684-131">-WhatIf</span></span>
<span data-ttu-id="24684-132">Mostra o que acontece se o cmdlet for executado, mas não executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24684-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="24684-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24684-133">CommonParameters</span></span>
<span data-ttu-id="24684-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24684-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24684-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24684-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24684-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="24684-136">INPUTS</span></span>

### <span data-ttu-id="24684-137">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="24684-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

### <span data-ttu-id="24684-138">System. String</span><span class="sxs-lookup"><span data-stu-id="24684-138">System.String</span></span>

## <span data-ttu-id="24684-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="24684-139">OUTPUTS</span></span>

### <span data-ttu-id="24684-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="24684-140">System.Boolean</span></span>

## <span data-ttu-id="24684-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="24684-141">NOTES</span></span>

## <span data-ttu-id="24684-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="24684-142">RELATED LINKS</span></span>

[<span data-ttu-id="24684-143">Get-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="24684-143">Get-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="24684-144">Set-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="24684-144">Set-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="24684-145">Start-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="24684-145">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="24684-146">Parar-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="24684-146">Stop-AzDataFactoryV2Trigger</span></span>]()

