---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2TriggerRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2TriggerRun.md
gitcommit: https://github.com/Azure/azure-powershell/blob/7fe7039e96038b4a91513dfda26026ad8e0a352b
ms.openlocfilehash: d5ea2dee1f6023b9505c38a58d364b7aa92591db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610017"
---
# <span data-ttu-id="57525-101">Get-AzureRmDataFactoryV2TriggerRun</span><span class="sxs-lookup"><span data-stu-id="57525-101">Get-AzureRmDataFactoryV2TriggerRun</span></span>

## <span data-ttu-id="57525-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="57525-102">SYNOPSIS</span></span>
<span data-ttu-id="57525-103">Retorna informações sobre execuções de gatilho.</span><span class="sxs-lookup"><span data-stu-id="57525-103">Returns information about trigger runs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="57525-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="57525-104">SYNTAX</span></span>

### <span data-ttu-id="57525-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="57525-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2TriggerRun [-Name] <String> [-TriggerRunStartedAfter] <DateTime>
 [-TriggerRunStartedBefore] <DateTime> [-ResourceGroupName] <String> [-DataFactoryName] <String>
```

### <span data-ttu-id="57525-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="57525-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2TriggerRun [-Name] <String> [-TriggerRunStartedAfter] <DateTime>
 [-TriggerRunStartedBefore] <DateTime> [-DataFactory] <PSDataFactory>
```

## <span data-ttu-id="57525-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="57525-107">DESCRIPTION</span></span>
<span data-ttu-id="57525-108">O comando **Get-AzureRmDataFactoryV2TriggerRun** retorna informações detalhadas sobre execuções de gatilho para o gatilho especificado no período de tempo especificado.</span><span class="sxs-lookup"><span data-stu-id="57525-108">The **Get-AzureRmDataFactoryV2TriggerRun** command returns detailed information about trigger runs for the specified trigger in the given timeframe.</span></span>

## <span data-ttu-id="57525-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="57525-109">EXAMPLES</span></span>

### <span data-ttu-id="57525-110">Exemplo 1: obter informações sobre a execução do gatilho</span><span class="sxs-lookup"><span data-stu-id="57525-110">Example 1: Get information about trigger run</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2TriggerRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "WikiTrigger" -TriggerRunStartedAfter "2017-09-01" -TriggerRunStartedBefore "2019-09-30"

    ResourceGroupName   : ADF
    DataFactoryName     : WikiADF
    TriggerName         : WikiTrigger
    TriggerRunId        : 08586958400454144995526033731
    TriggerType         : ScheduleTrigger
    TriggerRunTimestamp : 9/18/2017 8:34:00 PM
    Status              : Succeeded

```

<span data-ttu-id="57525-111">Esse comando mostra informações sobre execuções de "WikiTrigger" no "WikiADF" de fábrica que começaram entre "2017-09-01" e "2019-09-30".</span><span class="sxs-lookup"><span data-stu-id="57525-111">This command shows information about runs for "WikiTrigger" in the factory "WikiADF" that started between "2017-09-01" and "2019-09-30".</span></span>

## <span data-ttu-id="57525-112">OS</span><span class="sxs-lookup"><span data-stu-id="57525-112">PARAMETERS</span></span>

### <span data-ttu-id="57525-113">-Datafactory</span><span class="sxs-lookup"><span data-stu-id="57525-113">-DataFactory</span></span>
<span data-ttu-id="57525-114">O objeto de fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="57525-114">The data factory object.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57525-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="57525-115">-DataFactoryName</span></span>
<span data-ttu-id="57525-116">O nome do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="57525-116">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57525-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="57525-117">-Name</span></span>
<span data-ttu-id="57525-118">O nome do disparador.</span><span class="sxs-lookup"><span data-stu-id="57525-118">The trigger name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57525-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57525-119">-ResourceGroupName</span></span>
<span data-ttu-id="57525-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="57525-120">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57525-121">-TriggerRunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="57525-121">-TriggerRunStartedAfter</span></span>
<span data-ttu-id="57525-122">A hora em ou após a qual o disparador de execução foi iniciado para ser executado no formato ISO8601.</span><span class="sxs-lookup"><span data-stu-id="57525-122">The time at or after which the trigger run started to execute in ISO8601 format.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57525-123">-TriggerRunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="57525-123">-TriggerRunStartedBefore</span></span>
<span data-ttu-id="57525-124">O horário em ou antes do qual a execução do disparador foi iniciada para ser executada no formato ISO8601.</span><span class="sxs-lookup"><span data-stu-id="57525-124">The time at or before which the trigger run started to execute in ISO8601 format.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="57525-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="57525-125">INPUTS</span></span>

### <span data-ttu-id="57525-126">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="57525-126">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="57525-127">System. String</span><span class="sxs-lookup"><span data-stu-id="57525-127">System.String</span></span>


## <span data-ttu-id="57525-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="57525-128">OUTPUTS</span></span>

### <span data-ttu-id="57525-129">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. DataFactoryV2. Models. PSTriggerRun, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="57525-129">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="57525-130">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTriggerRun</span><span class="sxs-lookup"><span data-stu-id="57525-130">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun</span></span>


## <span data-ttu-id="57525-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="57525-131">NOTES</span></span>

## <span data-ttu-id="57525-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="57525-132">RELATED LINKS</span></span>
[<span data-ttu-id="57525-133">Start-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="57525-133">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="57525-134">Parar-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="57525-134">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

