---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Trigger.md
ms.openlocfilehash: aba1086db4fb1b106fb20579fde8fffc4db5591d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430333"
---
# <span data-ttu-id="243c8-101">Remove-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="243c8-101">Remove-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="243c8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="243c8-102">SYNOPSIS</span></span>
<span data-ttu-id="243c8-103">Remove um gatilho de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="243c8-103">Removes a trigger from a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="243c8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="243c8-104">SYNTAX</span></span>

### <span data-ttu-id="243c8-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="243c8-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="243c8-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="243c8-106">ByInputObject</span></span>
```
Remove-AzureRmDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="243c8-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="243c8-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="243c8-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="243c8-108">DESCRIPTION</span></span>
<span data-ttu-id="243c8-109">O cmdlet **Remove-AzureRmDataFactoryV2Trigger** remove um gatilho de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="243c8-109">The **Remove-AzureRmDataFactoryV2Trigger** cmdlet removes a trigger from a data factory.</span></span> <span data-ttu-id="243c8-110">Se o parâmetro _Force_ for especificado, o cmdlet não avisa antes de remover o gatilho.</span><span class="sxs-lookup"><span data-stu-id="243c8-110">If the _Force_ parameter is specified, the cmdlet doesn't prompt before removing the trigger.</span></span>

## <span data-ttu-id="243c8-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="243c8-111">EXAMPLES</span></span>

### <span data-ttu-id="243c8-112">Exemplo 1: remover um gatilho</span><span class="sxs-lookup"><span data-stu-id="243c8-112">Example 1: Remove a trigger</span></span>
```
Remove-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "ScheduledTrigger"

Confirm
Are you sure you want to remove trigger 'ScheduledTrigger' in data factory 'TestFactory'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="243c8-113">Remova um gatilho chamado "ScheduledTrigger" da fábrica de dados "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="243c8-113">Remove a trigger called "ScheduledTrigger" from the data factory "WikiADF".</span></span>

## <span data-ttu-id="243c8-114">OS</span><span class="sxs-lookup"><span data-stu-id="243c8-114">PARAMETERS</span></span>

### <span data-ttu-id="243c8-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="243c8-115">-DataFactoryName</span></span>
<span data-ttu-id="243c8-116">O nome do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="243c8-116">The data factory name.</span></span>

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

### <span data-ttu-id="243c8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="243c8-117">-DefaultProfile</span></span>
<span data-ttu-id="243c8-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="243c8-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="243c8-119">-Force</span><span class="sxs-lookup"><span data-stu-id="243c8-119">-Force</span></span>
<span data-ttu-id="243c8-120">Executa o cmdlet sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="243c8-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="243c8-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="243c8-121">-InputObject</span></span>
<span data-ttu-id="243c8-122">O objeto Trigger a ser removido.</span><span class="sxs-lookup"><span data-stu-id="243c8-122">The Trigger object to remove.</span></span>

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

### <span data-ttu-id="243c8-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="243c8-123">-Name</span></span>
<span data-ttu-id="243c8-124">O nome do disparador.</span><span class="sxs-lookup"><span data-stu-id="243c8-124">The trigger name.</span></span>

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

### <span data-ttu-id="243c8-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="243c8-125">-ResourceGroupName</span></span>
<span data-ttu-id="243c8-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="243c8-126">The resource group name.</span></span>

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

### <span data-ttu-id="243c8-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="243c8-127">-ResourceId</span></span>
<span data-ttu-id="243c8-128">A ID do recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="243c8-128">The Azure resource ID.</span></span>

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

### <span data-ttu-id="243c8-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="243c8-129">-Confirm</span></span>
<span data-ttu-id="243c8-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="243c8-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="243c8-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="243c8-131">-WhatIf</span></span>
<span data-ttu-id="243c8-132">Mostra o que acontece se o cmdlet for executado, mas não executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="243c8-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="243c8-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="243c8-133">CommonParameters</span></span>
<span data-ttu-id="243c8-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="243c8-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="243c8-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="243c8-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="243c8-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="243c8-136">INPUTS</span></span>

### <span data-ttu-id="243c8-137">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="243c8-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>
<span data-ttu-id="243c8-138">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="243c8-138">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="243c8-139">System. String</span><span class="sxs-lookup"><span data-stu-id="243c8-139">System.String</span></span>

## <span data-ttu-id="243c8-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="243c8-140">OUTPUTS</span></span>

### <span data-ttu-id="243c8-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="243c8-141">System.Boolean</span></span>

## <span data-ttu-id="243c8-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="243c8-142">NOTES</span></span>

## <span data-ttu-id="243c8-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="243c8-143">RELATED LINKS</span></span>

[<span data-ttu-id="243c8-144">Get-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="243c8-144">Get-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="243c8-145">Set-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="243c8-145">Set-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="243c8-146">Start-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="243c8-146">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="243c8-147">Parar-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="243c8-147">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

