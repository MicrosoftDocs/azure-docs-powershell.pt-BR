---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsetriggerrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTriggerRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTriggerRun.md
ms.openlocfilehash: 284974cc2d4cb98519b82c5c5a50e40d323dc354
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888629"
---
# <span data-ttu-id="30e07-101">Get-AzSynapseTriggerRun</span><span class="sxs-lookup"><span data-stu-id="30e07-101">Get-AzSynapseTriggerRun</span></span>

## <span data-ttu-id="30e07-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30e07-102">SYNOPSIS</span></span>
<span data-ttu-id="30e07-103">Retorna informações sobre disparos executados.</span><span class="sxs-lookup"><span data-stu-id="30e07-103">Returns information about trigger runs.</span></span>

## <span data-ttu-id="30e07-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="30e07-104">SYNTAX</span></span>

### <span data-ttu-id="30e07-105">GetByName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="30e07-105">GetByName (Default)</span></span>
```
Get-AzSynapseTriggerRun -WorkspaceName <String> -Name <String> -RunStartedAfter <DateTimeOffset>
 -RunStartedBefore <DateTimeOffset> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="30e07-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="30e07-106">GetByObject</span></span>
```
Get-AzSynapseTriggerRun -WorkspaceObject <PSSynapseWorkspace> -Name <String> -RunStartedAfter <DateTimeOffset>
 -RunStartedBefore <DateTimeOffset> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="30e07-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="30e07-107">DESCRIPTION</span></span>
<span data-ttu-id="30e07-108">O **comando Get-AzSynapseTriggerRun** retorna informações detalhadas sobre as executações de gatilho para o gatilho especificado no período de tempo determinado.</span><span class="sxs-lookup"><span data-stu-id="30e07-108">The **Get-AzSynapseTriggerRun** command returns detailed information about trigger runs for the specified trigger in the given timeframe.</span></span>

## <span data-ttu-id="30e07-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="30e07-109">EXAMPLES</span></span>

### <span data-ttu-id="30e07-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="30e07-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseTriggerRun -WorkspaceName ContosoWorkspace -Name ContosoTrigger -RunStartedAfter [DateTimeOffset]"2018-09-01T21:00" -RunStartedBefore [DateTimeOffset]"2019-09-01T21:00"
```

<span data-ttu-id="30e07-111">Este comando mostra informações sobre as executados para ContosoTrigger no espaço de trabalho ContosoWorkspace iniciado entre "2018-09-01T21:00" e "2019-09-01T21:00".</span><span class="sxs-lookup"><span data-stu-id="30e07-111">This command shows information about runs for ContosoTrigger in the workspace ContosoWorkspace that started between "2018-09-01T21:00" and "2019-09-01T21:00".</span></span>

### <span data-ttu-id="30e07-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="30e07-112">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseTriggerRun -Name ContosoTrigger -RunStartedAfter [DateTimeOffset]"2018-09-01T21:00" -RunStartedBefore [DateTimeOffset]"2019-09-01T21:00"
```

<span data-ttu-id="30e07-113">Este comando mostra informações sobre as executações para ContosoTrigger no espaço de trabalho ContosoWorkspace que começou entre "2018-09-01T21:00" e "2019-09-01T21:00" por meio de pipeline.</span><span class="sxs-lookup"><span data-stu-id="30e07-113">This command shows information about runs for ContosoTrigger in the workspace ContosoWorkspace that started between "2018-09-01T21:00" and "2019-09-01T21:00" through pipeline.</span></span>

## <span data-ttu-id="30e07-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="30e07-114">PARAMETERS</span></span>

### <span data-ttu-id="30e07-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30e07-115">-DefaultProfile</span></span>
<span data-ttu-id="30e07-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="30e07-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30e07-117">-Name</span><span class="sxs-lookup"><span data-stu-id="30e07-117">-Name</span></span>
<span data-ttu-id="30e07-118">O nome do gatilho.</span><span class="sxs-lookup"><span data-stu-id="30e07-118">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TriggerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30e07-119">-RunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="30e07-119">-RunStartedAfter</span></span>
<span data-ttu-id="30e07-120">A hora em que o evento de executar foi atualizado no formato 'ISO 8601'.</span><span class="sxs-lookup"><span data-stu-id="30e07-120">The time at or after which the run event was updated in 'ISO 8601' format.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30e07-121">-RunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="30e07-121">-RunStartedBefore</span></span>
<span data-ttu-id="30e07-122">A hora em que o evento de executar foi atualizado no formato 'ISO 8601'.</span><span class="sxs-lookup"><span data-stu-id="30e07-122">The time at or before which the run event was updated in 'ISO 8601' format.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30e07-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="30e07-123">-WorkspaceName</span></span>
<span data-ttu-id="30e07-124">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="30e07-124">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30e07-125">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="30e07-125">-WorkspaceObject</span></span>
<span data-ttu-id="30e07-126">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="30e07-126">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="30e07-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30e07-127">CommonParameters</span></span>
<span data-ttu-id="30e07-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30e07-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30e07-129">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="30e07-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30e07-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="30e07-130">INPUTS</span></span>

### <span data-ttu-id="30e07-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="30e07-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="30e07-132">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="30e07-132">OUTPUTS</span></span>

### <span data-ttu-id="30e07-133">Microsoft.Azure.Commands.Synapse.Models.PSTriggerRun</span><span class="sxs-lookup"><span data-stu-id="30e07-133">Microsoft.Azure.Commands.Synapse.Models.PSTriggerRun</span></span>

## <span data-ttu-id="30e07-134">NOTES</span><span class="sxs-lookup"><span data-stu-id="30e07-134">NOTES</span></span>

## <span data-ttu-id="30e07-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="30e07-135">RELATED LINKS</span></span>
