---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2triggerrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2TriggerRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2TriggerRun.md
ms.openlocfilehash: 5844863cf56008d5d73fae7eef644dfd8e27c239
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93778356"
---
# <span data-ttu-id="4c4b1-101">Get-AzDataFactoryV2TriggerRun</span><span class="sxs-lookup"><span data-stu-id="4c4b1-101">Get-AzDataFactoryV2TriggerRun</span></span>

## <span data-ttu-id="4c4b1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4c4b1-102">SYNOPSIS</span></span>
<span data-ttu-id="4c4b1-103">Retorna informações sobre execuções de gatilho.</span><span class="sxs-lookup"><span data-stu-id="4c4b1-103">Returns information about trigger runs.</span></span>

## <span data-ttu-id="4c4b1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4c4b1-104">SYNTAX</span></span>

### <span data-ttu-id="4c4b1-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="4c4b1-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2TriggerRun [-Name] <String> [-TriggerRunStartedAfter] <DateTime>
 [-TriggerRunStartedBefore] <DateTime> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4c4b1-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="4c4b1-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2TriggerRun [-Name] <String> [-TriggerRunStartedAfter] <DateTime>
 [-TriggerRunStartedBefore] <DateTime> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4c4b1-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4c4b1-107">DESCRIPTION</span></span>
<span data-ttu-id="4c4b1-108">O comando **Get-AzDataFactoryV2TriggerRun** retorna informações detalhadas sobre execuções de gatilho para o gatilho especificado no período de tempo especificado.</span><span class="sxs-lookup"><span data-stu-id="4c4b1-108">The **Get-AzDataFactoryV2TriggerRun** command returns detailed information about trigger runs for the specified trigger in the given timeframe.</span></span>

## <span data-ttu-id="4c4b1-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4c4b1-109">EXAMPLES</span></span>

### <span data-ttu-id="4c4b1-110">Exemplo 1: obter informações sobre a execução do gatilho</span><span class="sxs-lookup"><span data-stu-id="4c4b1-110">Example 1: Get information about trigger run</span></span>
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

<span data-ttu-id="4c4b1-111">Esse comando mostra informações sobre execuções de "WikiTrigger" no "WikiADF" de fábrica que começaram entre "2017-09-01" e "2019-09-30".</span><span class="sxs-lookup"><span data-stu-id="4c4b1-111">This command shows information about runs for "WikiTrigger" in the factory "WikiADF" that started between "2017-09-01" and "2019-09-30".</span></span>

## <span data-ttu-id="4c4b1-112">OS</span><span class="sxs-lookup"><span data-stu-id="4c4b1-112">PARAMETERS</span></span>

### <span data-ttu-id="4c4b1-113">-Datafactory</span><span class="sxs-lookup"><span data-stu-id="4c4b1-113">-DataFactory</span></span>
<span data-ttu-id="4c4b1-114">O objeto de fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="4c4b1-114">The data factory object.</span></span>

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

### <span data-ttu-id="4c4b1-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="4c4b1-115">-DataFactoryName</span></span>
<span data-ttu-id="4c4b1-116">O nome do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="4c4b1-116">The data factory name.</span></span>

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

### <span data-ttu-id="4c4b1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c4b1-117">-DefaultProfile</span></span>
<span data-ttu-id="4c4b1-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4c4b1-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4c4b1-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="4c4b1-119">-Name</span></span>
<span data-ttu-id="4c4b1-120">O nome do disparador.</span><span class="sxs-lookup"><span data-stu-id="4c4b1-120">The trigger name.</span></span>

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

### <span data-ttu-id="4c4b1-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c4b1-121">-ResourceGroupName</span></span>
<span data-ttu-id="4c4b1-122">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4c4b1-122">The resource group name.</span></span>

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

### <span data-ttu-id="4c4b1-123">-TriggerRunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="4c4b1-123">-TriggerRunStartedAfter</span></span>
<span data-ttu-id="4c4b1-124">A hora em ou após a qual o disparador de execução foi iniciado para ser executado no formato ISO8601.</span><span class="sxs-lookup"><span data-stu-id="4c4b1-124">The time at or after which the trigger run started to execute in ISO8601 format.</span></span>

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

### <span data-ttu-id="4c4b1-125">-TriggerRunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="4c4b1-125">-TriggerRunStartedBefore</span></span>
<span data-ttu-id="4c4b1-126">O horário em ou antes do qual a execução do disparador foi iniciada para ser executada no formato ISO8601.</span><span class="sxs-lookup"><span data-stu-id="4c4b1-126">The time at or before which the trigger run started to execute in ISO8601 format.</span></span>

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

### <span data-ttu-id="4c4b1-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c4b1-127">CommonParameters</span></span>
<span data-ttu-id="4c4b1-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c4b1-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c4b1-129">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c4b1-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c4b1-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4c4b1-130">INPUTS</span></span>

### <span data-ttu-id="4c4b1-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="4c4b1-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="4c4b1-132">System. String</span><span class="sxs-lookup"><span data-stu-id="4c4b1-132">System.String</span></span>

## <span data-ttu-id="4c4b1-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4c4b1-133">OUTPUTS</span></span>

### <span data-ttu-id="4c4b1-134">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTriggerRun</span><span class="sxs-lookup"><span data-stu-id="4c4b1-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun</span></span>

## <span data-ttu-id="4c4b1-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4c4b1-135">NOTES</span></span>

## <span data-ttu-id="4c4b1-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4c4b1-136">RELATED LINKS</span></span>

[<span data-ttu-id="4c4b1-137">Start-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="4c4b1-137">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="4c4b1-138">Parar-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="4c4b1-138">Stop-AzDataFactoryV2Trigger</span></span>]()

