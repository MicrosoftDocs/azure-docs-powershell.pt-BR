---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactoryv2triggerrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2TriggerRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2TriggerRun.md
ms.openlocfilehash: ba9ea38f5915f5a89326c806e11a055ec6aeed75
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888276"
---
# <span data-ttu-id="2df18-101">Get-AzDataFactoryV2TriggerRun</span><span class="sxs-lookup"><span data-stu-id="2df18-101">Get-AzDataFactoryV2TriggerRun</span></span>

## <span data-ttu-id="2df18-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2df18-102">SYNOPSIS</span></span>
<span data-ttu-id="2df18-103">Retorna informações sobre disparos executados.</span><span class="sxs-lookup"><span data-stu-id="2df18-103">Returns information about trigger runs.</span></span>

## <span data-ttu-id="2df18-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="2df18-104">SYNTAX</span></span>

### <span data-ttu-id="2df18-105">ByFactoryName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="2df18-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2TriggerRun [-Name] <String> [-TriggerRunStartedAfter] <DateTime>
 [-TriggerRunStartedBefore] <DateTime> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2df18-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="2df18-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2TriggerRun [-Name] <String> [-TriggerRunStartedAfter] <DateTime>
 [-TriggerRunStartedBefore] <DateTime> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2df18-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="2df18-107">DESCRIPTION</span></span>
<span data-ttu-id="2df18-108">O **comando Get-AzDataFactoryV2TriggerRun** retorna informações detalhadas sobre as executações de gatilho para o gatilho especificado no determinado período de tempo.</span><span class="sxs-lookup"><span data-stu-id="2df18-108">The **Get-AzDataFactoryV2TriggerRun** command returns detailed information about trigger runs for the specified trigger in the given timeframe.</span></span>

## <span data-ttu-id="2df18-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2df18-109">EXAMPLES</span></span>

### <span data-ttu-id="2df18-110">Exemplo 1: Obter informações sobre a operação de gatilho</span><span class="sxs-lookup"><span data-stu-id="2df18-110">Example 1: Get information about trigger run</span></span>
```
PS C:\> Get-AzDataFactoryV2TriggerRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "WikiTrigger" -TriggerRunStartedAfter "2017-09-01" -TriggerRunStartedBefore "2019-09-30"

    ResourceGroupName   : ADF
    DataFactoryName     : WikiADF
    TriggerName         : WikiTrigger
    TriggerRunId        : 08586958400454144995526033731
    TriggerType         : ScheduleTrigger
    TriggerRunTimestamp : 9/18/2017 8:34:00 PM
    Status              : Succeeded
```

<span data-ttu-id="2df18-111">Este comando mostra informações sobre as executados para "WikiTrigger" na fábrica "WikiADF" que começou entre "2017-09-01" e "2019-09-30".</span><span class="sxs-lookup"><span data-stu-id="2df18-111">This command shows information about runs for "WikiTrigger" in the factory "WikiADF" that started between "2017-09-01" and "2019-09-30".</span></span>

## <span data-ttu-id="2df18-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="2df18-112">PARAMETERS</span></span>

### <span data-ttu-id="2df18-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="2df18-113">-DataFactory</span></span>
<span data-ttu-id="2df18-114">O objeto de fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="2df18-114">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2df18-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="2df18-115">-DataFactoryName</span></span>
<span data-ttu-id="2df18-116">O nome da fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="2df18-116">The data factory name.</span></span>

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

### <span data-ttu-id="2df18-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2df18-117">-DefaultProfile</span></span>
<span data-ttu-id="2df18-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="2df18-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2df18-119">-Name</span><span class="sxs-lookup"><span data-stu-id="2df18-119">-Name</span></span>
<span data-ttu-id="2df18-120">O nome do gatilho.</span><span class="sxs-lookup"><span data-stu-id="2df18-120">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2df18-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2df18-121">-ResourceGroupName</span></span>
<span data-ttu-id="2df18-122">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2df18-122">The resource group name.</span></span>

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

### <span data-ttu-id="2df18-123">-TriggerRunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="2df18-123">-TriggerRunStartedAfter</span></span>
<span data-ttu-id="2df18-124">A hora em que a execução do gatilho começou a ser executada no formato ISO8601.</span><span class="sxs-lookup"><span data-stu-id="2df18-124">The time at or after which the trigger run started to execute in ISO8601 format.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2df18-125">-TriggerRunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="2df18-125">-TriggerRunStartedBefore</span></span>
<span data-ttu-id="2df18-126">A hora em que a execução do gatilho começou a ser executada no formato ISO8601.</span><span class="sxs-lookup"><span data-stu-id="2df18-126">The time at or before which the trigger run started to execute in ISO8601 format.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2df18-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2df18-127">CommonParameters</span></span>
<span data-ttu-id="2df18-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2df18-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2df18-129">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2df18-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2df18-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2df18-130">INPUTS</span></span>

### <span data-ttu-id="2df18-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="2df18-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="2df18-132">System.String</span><span class="sxs-lookup"><span data-stu-id="2df18-132">System.String</span></span>

## <span data-ttu-id="2df18-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="2df18-133">OUTPUTS</span></span>

### <span data-ttu-id="2df18-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun</span><span class="sxs-lookup"><span data-stu-id="2df18-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun</span></span>

## <span data-ttu-id="2df18-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="2df18-135">NOTES</span></span>

## <span data-ttu-id="2df18-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2df18-136">RELATED LINKS</span></span>

[<span data-ttu-id="2df18-137">Start-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="2df18-137">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="2df18-138">Stop-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="2df18-138">Stop-AzDataFactoryV2Trigger</span></span>]()

