---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Trigger.md
ms.openlocfilehash: 989a898605488fc7cfaa828bfd8c5b9b61378a27
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94281045"
---
# <span data-ttu-id="6ad0b-101">Get-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="6ad0b-101">Get-AzDataFactoryV2Trigger</span></span>

## <span data-ttu-id="6ad0b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6ad0b-102">SYNOPSIS</span></span>
<span data-ttu-id="6ad0b-103">Obtém informações sobre gatilhos em uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="6ad0b-103">Gets information about triggers in a data factory.</span></span>

## <span data-ttu-id="6ad0b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6ad0b-104">SYNTAX</span></span>

### <span data-ttu-id="6ad0b-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="6ad0b-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2Trigger [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ad0b-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="6ad0b-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2Trigger [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ad0b-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="6ad0b-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2Trigger [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6ad0b-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6ad0b-108">DESCRIPTION</span></span>
<span data-ttu-id="6ad0b-109">O cmdlet **Get-AzDataFactoryV2Trigger** Obtém informações sobre gatilhos em uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="6ad0b-109">The **Get-AzDataFactoryV2Trigger** cmdlet gets information about triggers in a data factory.</span></span> <span data-ttu-id="6ad0b-110">Se você especificar o nome de um gatilho, o cmdlet obterá informações sobre esse gatilho.</span><span class="sxs-lookup"><span data-stu-id="6ad0b-110">If you specify the name of a trigger, the cmdlet gets information about that trigger.</span></span> <span data-ttu-id="6ad0b-111">Se você não especificar um nome, o cmdlet obterá informações sobre todos os gatilhos na fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="6ad0b-111">If you do not specify a name, the cmdlet gets information about all triggers in the data factory.</span></span>

## <span data-ttu-id="6ad0b-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6ad0b-112">EXAMPLES</span></span>

### <span data-ttu-id="6ad0b-113">Exemplo 1: obter informações sobre um gatilho específico</span><span class="sxs-lookup"><span data-stu-id="6ad0b-113">Example 1: Get information about a specific trigger</span></span>
```
PS C:\> Get-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF"

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

<span data-ttu-id="6ad0b-114">Obtém uma lista de todos os gatilhos que foram criados na fábrica de dados "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="6ad0b-114">Gets a list of all triggers that have been created in the data factory "WikiADF".</span></span>

### <span data-ttu-id="6ad0b-115">Exemplo 2: obter informações sobre todos os gatilhos</span><span class="sxs-lookup"><span data-stu-id="6ad0b-115">Example 2: Get information about all triggers</span></span>
```
Get-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped
```

<span data-ttu-id="6ad0b-116">Obtém um único gatilho chamado "ScheduledTrigger" na fábrica de dados "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="6ad0b-116">Gets a single trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="6ad0b-117">OS</span><span class="sxs-lookup"><span data-stu-id="6ad0b-117">PARAMETERS</span></span>

### <span data-ttu-id="6ad0b-118">-Datafactory</span><span class="sxs-lookup"><span data-stu-id="6ad0b-118">-DataFactory</span></span>
<span data-ttu-id="6ad0b-119">O objeto de fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="6ad0b-119">The data factory object.</span></span>

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

### <span data-ttu-id="6ad0b-120">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="6ad0b-120">-DataFactoryName</span></span>
<span data-ttu-id="6ad0b-121">O nome do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="6ad0b-121">The data factory name.</span></span>

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

### <span data-ttu-id="6ad0b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ad0b-122">-DefaultProfile</span></span>
<span data-ttu-id="6ad0b-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6ad0b-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6ad0b-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="6ad0b-124">-Name</span></span>
<span data-ttu-id="6ad0b-125">O nome do disparador.</span><span class="sxs-lookup"><span data-stu-id="6ad0b-125">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases: TriggerName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ad0b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ad0b-126">-ResourceGroupName</span></span>
<span data-ttu-id="6ad0b-127">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6ad0b-127">The resource group name.</span></span>

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

### <span data-ttu-id="6ad0b-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6ad0b-128">-ResourceId</span></span>
<span data-ttu-id="6ad0b-129">A ID do recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="6ad0b-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="6ad0b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ad0b-130">CommonParameters</span></span>
<span data-ttu-id="6ad0b-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ad0b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ad0b-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ad0b-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ad0b-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6ad0b-133">INPUTS</span></span>

### <span data-ttu-id="6ad0b-134">System. String</span><span class="sxs-lookup"><span data-stu-id="6ad0b-134">System.String</span></span>

### <span data-ttu-id="6ad0b-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="6ad0b-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="6ad0b-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6ad0b-136">OUTPUTS</span></span>

### <span data-ttu-id="6ad0b-137">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="6ad0b-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="6ad0b-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6ad0b-138">NOTES</span></span>

## <span data-ttu-id="6ad0b-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6ad0b-139">RELATED LINKS</span></span>

[<span data-ttu-id="6ad0b-140">Set-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="6ad0b-140">Set-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="6ad0b-141">Start-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="6ad0b-141">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="6ad0b-142">Parar-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="6ad0b-142">Stop-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="6ad0b-143">Remove-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="6ad0b-143">Remove-AzDataFactoryV2Trigger</span></span>]()
