---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryv2triggerrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2TriggerRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2TriggerRun.md
ms.openlocfilehash: caa3cd25db706a3d025ee439aebb6dbb5491f7d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602965"
---
# <span data-ttu-id="d0613-101">Get-AzureRmDataFactoryV2TriggerRun</span><span class="sxs-lookup"><span data-stu-id="d0613-101">Get-AzureRmDataFactoryV2TriggerRun</span></span>

## <span data-ttu-id="d0613-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d0613-102">SYNOPSIS</span></span>
<span data-ttu-id="d0613-103">Retorna informações sobre execuções de gatilho.</span><span class="sxs-lookup"><span data-stu-id="d0613-103">Returns information about trigger runs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d0613-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d0613-104">SYNTAX</span></span>

### <span data-ttu-id="d0613-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="d0613-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2TriggerRun [-Name] <String> [-TriggerRunStartedAfter] <DateTime>
 [-TriggerRunStartedBefore] <DateTime> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d0613-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="d0613-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2TriggerRun [-Name] <String> [-TriggerRunStartedAfter] <DateTime>
 [-TriggerRunStartedBefore] <DateTime> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d0613-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d0613-107">DESCRIPTION</span></span>
<span data-ttu-id="d0613-108">O comando **Get-AzureRmDataFactoryV2TriggerRun** retorna informações detalhadas sobre execuções de gatilho para o gatilho especificado no período de tempo especificado.</span><span class="sxs-lookup"><span data-stu-id="d0613-108">The **Get-AzureRmDataFactoryV2TriggerRun** command returns detailed information about trigger runs for the specified trigger in the given timeframe.</span></span>

## <span data-ttu-id="d0613-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d0613-109">EXAMPLES</span></span>

### <span data-ttu-id="d0613-110">Exemplo 1: obter informações sobre a execução do gatilho</span><span class="sxs-lookup"><span data-stu-id="d0613-110">Example 1: Get information about trigger run</span></span>
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

<span data-ttu-id="d0613-111">Esse comando mostra informações sobre execuções de "WikiTrigger" no "WikiADF" de fábrica que começaram entre "2017-09-01" e "2019-09-30".</span><span class="sxs-lookup"><span data-stu-id="d0613-111">This command shows information about runs for "WikiTrigger" in the factory "WikiADF" that started between "2017-09-01" and "2019-09-30".</span></span>

## <span data-ttu-id="d0613-112">OS</span><span class="sxs-lookup"><span data-stu-id="d0613-112">PARAMETERS</span></span>

### <span data-ttu-id="d0613-113">-Datafactory</span><span class="sxs-lookup"><span data-stu-id="d0613-113">-DataFactory</span></span>
<span data-ttu-id="d0613-114">O objeto de fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="d0613-114">The data factory object.</span></span>

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

### <span data-ttu-id="d0613-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="d0613-115">-DataFactoryName</span></span>
<span data-ttu-id="d0613-116">O nome do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="d0613-116">The data factory name.</span></span>

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

### <span data-ttu-id="d0613-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0613-117">-DefaultProfile</span></span>
<span data-ttu-id="d0613-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d0613-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d0613-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="d0613-119">-Name</span></span>
<span data-ttu-id="d0613-120">O nome do disparador.</span><span class="sxs-lookup"><span data-stu-id="d0613-120">The trigger name.</span></span>

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

### <span data-ttu-id="d0613-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0613-121">-ResourceGroupName</span></span>
<span data-ttu-id="d0613-122">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d0613-122">The resource group name.</span></span>

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

### <span data-ttu-id="d0613-123">-TriggerRunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="d0613-123">-TriggerRunStartedAfter</span></span>
<span data-ttu-id="d0613-124">A hora em ou após a qual o disparador de execução foi iniciado para ser executado no formato ISO8601.</span><span class="sxs-lookup"><span data-stu-id="d0613-124">The time at or after which the trigger run started to execute in ISO8601 format.</span></span>

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

### <span data-ttu-id="d0613-125">-TriggerRunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="d0613-125">-TriggerRunStartedBefore</span></span>
<span data-ttu-id="d0613-126">O horário em ou antes do qual a execução do disparador foi iniciada para ser executada no formato ISO8601.</span><span class="sxs-lookup"><span data-stu-id="d0613-126">The time at or before which the trigger run started to execute in ISO8601 format.</span></span>

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

### <span data-ttu-id="d0613-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0613-127">CommonParameters</span></span>
<span data-ttu-id="d0613-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0613-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0613-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0613-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0613-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d0613-130">INPUTS</span></span>

### <span data-ttu-id="d0613-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="d0613-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="d0613-132">Parâmetros: datafactory (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d0613-132">Parameters: DataFactory (ByValue)</span></span>

### <span data-ttu-id="d0613-133">System. String</span><span class="sxs-lookup"><span data-stu-id="d0613-133">System.String</span></span>

## <span data-ttu-id="d0613-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d0613-134">OUTPUTS</span></span>

### <span data-ttu-id="d0613-135">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTriggerRun</span><span class="sxs-lookup"><span data-stu-id="d0613-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun</span></span>

## <span data-ttu-id="d0613-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d0613-136">NOTES</span></span>

## <span data-ttu-id="d0613-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d0613-137">RELATED LINKS</span></span>

[<span data-ttu-id="d0613-138">Start-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="d0613-138">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="d0613-139">Parar-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="d0613-139">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

