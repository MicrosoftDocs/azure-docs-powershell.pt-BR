---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2triggerrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2TriggerRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2TriggerRun.md
ms.openlocfilehash: 5844863cf56008d5d73fae7eef644dfd8e27c239
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116427"
---
# <span data-ttu-id="536e6-101">Get-AzDataFactoryV2TriggerRun</span><span class="sxs-lookup"><span data-stu-id="536e6-101">Get-AzDataFactoryV2TriggerRun</span></span>

## <span data-ttu-id="536e6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="536e6-102">SYNOPSIS</span></span>
<span data-ttu-id="536e6-103">Retorna informações sobre o gatilho executado.</span><span class="sxs-lookup"><span data-stu-id="536e6-103">Returns information about trigger runs.</span></span>

## <span data-ttu-id="536e6-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="536e6-104">SYNTAX</span></span>

### <span data-ttu-id="536e6-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="536e6-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2TriggerRun [-Name] <String> [-TriggerRunStartedAfter] <DateTime>
 [-TriggerRunStartedBefore] <DateTime> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="536e6-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="536e6-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2TriggerRun [-Name] <String> [-TriggerRunStartedAfter] <DateTime>
 [-TriggerRunStartedBefore] <DateTime> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="536e6-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="536e6-107">DESCRIPTION</span></span>
<span data-ttu-id="536e6-108">O **comando Get-AzDataFactoryV2TriframeRun** retorna informações detalhadas sobre o gatilho executado para o gatilho especificado no determinado prazo.</span><span class="sxs-lookup"><span data-stu-id="536e6-108">The **Get-AzDataFactoryV2TriggerRun** command returns detailed information about trigger runs for the specified trigger in the given timeframe.</span></span>

## <span data-ttu-id="536e6-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="536e6-109">EXAMPLES</span></span>

### <span data-ttu-id="536e6-110">Exemplo 1: Obter informações sobre a acionamento</span><span class="sxs-lookup"><span data-stu-id="536e6-110">Example 1: Get information about trigger run</span></span>
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

<span data-ttu-id="536e6-111">Este comando mostra informações sobre as executados para "WikiTri wikiTri wiki" na fábrica "WikiADF" que começou entre "2017-09-01" e "2019-09-30".</span><span class="sxs-lookup"><span data-stu-id="536e6-111">This command shows information about runs for "WikiTrigger" in the factory "WikiADF" that started between "2017-09-01" and "2019-09-30".</span></span>

## <span data-ttu-id="536e6-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="536e6-112">PARAMETERS</span></span>

### <span data-ttu-id="536e6-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="536e6-113">-DataFactory</span></span>
<span data-ttu-id="536e6-114">O objeto de fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="536e6-114">The data factory object.</span></span>

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

### <span data-ttu-id="536e6-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="536e6-115">-DataFactoryName</span></span>
<span data-ttu-id="536e6-116">O nome da fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="536e6-116">The data factory name.</span></span>

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

### <span data-ttu-id="536e6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="536e6-117">-DefaultProfile</span></span>
<span data-ttu-id="536e6-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="536e6-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="536e6-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="536e6-119">-Name</span></span>
<span data-ttu-id="536e6-120">O nome do gatilho.</span><span class="sxs-lookup"><span data-stu-id="536e6-120">The trigger name.</span></span>

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

### <span data-ttu-id="536e6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="536e6-121">-ResourceGroupName</span></span>
<span data-ttu-id="536e6-122">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="536e6-122">The resource group name.</span></span>

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

### <span data-ttu-id="536e6-123">-TriggerRunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="536e6-123">-TriggerRunStartedAfter</span></span>
<span data-ttu-id="536e6-124">O momento em que a execução do gatilho começou a ser executada no formato ISO8601.</span><span class="sxs-lookup"><span data-stu-id="536e6-124">The time at or after which the trigger run started to execute in ISO8601 format.</span></span>

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

### <span data-ttu-id="536e6-125">-TriggerRunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="536e6-125">-TriggerRunStartedBefore</span></span>
<span data-ttu-id="536e6-126">O momento em que a execução do gatilho começou a ser executada no formato ISO8601.</span><span class="sxs-lookup"><span data-stu-id="536e6-126">The time at or before which the trigger run started to execute in ISO8601 format.</span></span>

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

### <span data-ttu-id="536e6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="536e6-127">CommonParameters</span></span>
<span data-ttu-id="536e6-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="536e6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="536e6-129">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="536e6-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="536e6-130">Entradas</span><span class="sxs-lookup"><span data-stu-id="536e6-130">INPUTS</span></span>

### <span data-ttu-id="536e6-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="536e6-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="536e6-132">System.String</span><span class="sxs-lookup"><span data-stu-id="536e6-132">System.String</span></span>

## <span data-ttu-id="536e6-133">Saídas</span><span class="sxs-lookup"><span data-stu-id="536e6-133">OUTPUTS</span></span>

### <span data-ttu-id="536e6-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrioryRun</span><span class="sxs-lookup"><span data-stu-id="536e6-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun</span></span>

## <span data-ttu-id="536e6-135">Notas</span><span class="sxs-lookup"><span data-stu-id="536e6-135">NOTES</span></span>

## <span data-ttu-id="536e6-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="536e6-136">RELATED LINKS</span></span>

[<span data-ttu-id="536e6-137">Start-AzDataFactoryV2Triory</span><span class="sxs-lookup"><span data-stu-id="536e6-137">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="536e6-138">Stop-AzDataFactoryV2Triory</span><span class="sxs-lookup"><span data-stu-id="536e6-138">Stop-AzDataFactoryV2Trigger</span></span>]()

