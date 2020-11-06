---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Trigger.md
gitcommit: https://github.com/Azure/azure-powershell/blob/c396953644d237789e0f4e1f726b553913186d34
ms.openlocfilehash: bc60bbb5b48c4022e7db6a95e26a1f43ef891ae2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441125"
---
# <span data-ttu-id="bbd1a-101">Get-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="bbd1a-101">Get-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="bbd1a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bbd1a-102">SYNOPSIS</span></span>
<span data-ttu-id="bbd1a-103">Obtém informações sobre gatilhos em uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="bbd1a-103">Gets information about triggers in a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bbd1a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bbd1a-104">SYNTAX</span></span>

### <span data-ttu-id="bbd1a-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="bbd1a-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2Trigger [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
```

### <span data-ttu-id="bbd1a-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="bbd1a-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2Trigger [[-Name] <String>] [-DataFactory] <PSDataFactory>
```

## <span data-ttu-id="bbd1a-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bbd1a-107">DESCRIPTION</span></span>
<span data-ttu-id="bbd1a-108">O cmdlet **Get-AzureRmDataFactoryV2Trigger** Obtém informações sobre gatilhos em uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="bbd1a-108">The **Get-AzureRmDataFactoryV2Trigger** cmdlet gets information about triggers in a data factory.</span></span> <span data-ttu-id="bbd1a-109">Se você especificar o nome de um gatilho, o cmdlet obterá informações sobre esse gatilho.</span><span class="sxs-lookup"><span data-stu-id="bbd1a-109">If you specify the name of a trigger, the cmdlet gets information about that trigger.</span></span> <span data-ttu-id="bbd1a-110">Se você não especificar um nome, o cmdlet obterá informações sobre todos os gatilhos na fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="bbd1a-110">If you do not specify a name, the cmdlet gets information about all triggers in the data factory.</span></span>


## <span data-ttu-id="bbd1a-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bbd1a-111">EXAMPLES</span></span>

### <span data-ttu-id="bbd1a-112">Exemplo 1: obter informações sobre um gatilho específico</span><span class="sxs-lookup"><span data-stu-id="bbd1a-112">Example 1: Get information about a specific trigger</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped

    TriggerName       : ScheduledTrigger2
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped
```

<span data-ttu-id="bbd1a-113">Obtém uma lista de todos os gatilhos que foram criados na fábrica de dados "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="bbd1a-113">Gets a list of all triggers that have been created in the data factory "WikiADF".</span></span>

### <span data-ttu-id="bbd1a-114">Exemplo 2: obter informações sobre todos os gatilhos</span><span class="sxs-lookup"><span data-stu-id="bbd1a-114">Example 2: Get information about all triggers</span></span>

```
Get-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped
```

<span data-ttu-id="bbd1a-115">Obtém um único gatilho chamado "ScheduledTrigger" na fábrica de dados "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="bbd1a-115">Gets a single trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="bbd1a-116">OS</span><span class="sxs-lookup"><span data-stu-id="bbd1a-116">PARAMETERS</span></span>

### <span data-ttu-id="bbd1a-117">-Datafactory</span><span class="sxs-lookup"><span data-stu-id="bbd1a-117">-DataFactory</span></span>
<span data-ttu-id="bbd1a-118">O objeto de fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="bbd1a-118">The data factory object.</span></span>

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

### <span data-ttu-id="bbd1a-119">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="bbd1a-119">-DataFactoryName</span></span>
<span data-ttu-id="bbd1a-120">O nome do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="bbd1a-120">The data factory name.</span></span>

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

### <span data-ttu-id="bbd1a-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="bbd1a-121">-Name</span></span>
<span data-ttu-id="bbd1a-122">O nome do disparador.</span><span class="sxs-lookup"><span data-stu-id="bbd1a-122">The trigger name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TriggerName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbd1a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bbd1a-123">-ResourceGroupName</span></span>
<span data-ttu-id="bbd1a-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="bbd1a-124">The resource group name.</span></span>

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

## <span data-ttu-id="bbd1a-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bbd1a-125">INPUTS</span></span>

### <span data-ttu-id="bbd1a-126">System. String</span><span class="sxs-lookup"><span data-stu-id="bbd1a-126">System.String</span></span>
<span data-ttu-id="bbd1a-127">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="bbd1a-127">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>


## <span data-ttu-id="bbd1a-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bbd1a-128">OUTPUTS</span></span>

### <span data-ttu-id="bbd1a-129">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="bbd1a-129">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="bbd1a-130">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="bbd1a-130">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>


## <span data-ttu-id="bbd1a-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bbd1a-131">NOTES</span></span>

## <span data-ttu-id="bbd1a-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bbd1a-132">RELATED LINKS</span></span>
[<span data-ttu-id="bbd1a-133">Set-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="bbd1a-133">Set-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="bbd1a-134">Start-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="bbd1a-134">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="bbd1a-135">Parar-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="bbd1a-135">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="bbd1a-136">Remove-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="bbd1a-136">Remove-AzureRmDataFactoryV2Trigger</span></span>]()
