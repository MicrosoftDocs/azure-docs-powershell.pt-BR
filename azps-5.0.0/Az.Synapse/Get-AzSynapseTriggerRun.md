---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsetriggerrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTriggerRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTriggerRun.md
ms.openlocfilehash: 0d6d3bb99062177e1d75c4ab496562782cf142c1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94117148"
---
# <span data-ttu-id="ac1e7-101">Get-AzSynapseTriggerRun</span><span class="sxs-lookup"><span data-stu-id="ac1e7-101">Get-AzSynapseTriggerRun</span></span>

## <span data-ttu-id="ac1e7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ac1e7-102">SYNOPSIS</span></span>
<span data-ttu-id="ac1e7-103">Retorna informações sobre execuções de gatilho.</span><span class="sxs-lookup"><span data-stu-id="ac1e7-103">Returns information about trigger runs.</span></span>

## <span data-ttu-id="ac1e7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ac1e7-104">SYNTAX</span></span>

### <span data-ttu-id="ac1e7-105">GetByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="ac1e7-105">GetByName (Default)</span></span>
```
Get-AzSynapseTriggerRun -WorkspaceName <String> -Name <String> -RunStartedAfter <DateTimeOffset>
 -RunStartedBefore <DateTimeOffset> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ac1e7-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="ac1e7-106">GetByObject</span></span>
```
Get-AzSynapseTriggerRun -WorkspaceObject <PSSynapseWorkspace> -Name <String> -RunStartedAfter <DateTimeOffset>
 -RunStartedBefore <DateTimeOffset> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ac1e7-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ac1e7-107">DESCRIPTION</span></span>
<span data-ttu-id="ac1e7-108">O comando **Get-AzSynapseTriggerRun** retorna informações detalhadas sobre execuções de gatilho para o gatilho especificado no período de tempo especificado.</span><span class="sxs-lookup"><span data-stu-id="ac1e7-108">The **Get-AzSynapseTriggerRun** command returns detailed information about trigger runs for the specified trigger in the given timeframe.</span></span>

## <span data-ttu-id="ac1e7-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ac1e7-109">EXAMPLES</span></span>

### <span data-ttu-id="ac1e7-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ac1e7-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseTriggerRun -WorkspaceName ContosoWorkspace -Name ContosoTrigger -RunStartedAfter [DateTimeOffset]"2018-09-01T21:00" -RunStartedBefore [DateTimeOffset]"2019-09-01T21:00"
```

<span data-ttu-id="ac1e7-111">Esse comando mostra informações sobre execuções de ContosoTrigger no espaço de trabalho ContosoWorkspace que começou entre "2018-09-01T21:00" e "2019-09-01T21:00".</span><span class="sxs-lookup"><span data-stu-id="ac1e7-111">This command shows information about runs for ContosoTrigger in the workspace ContosoWorkspace that started between "2018-09-01T21:00" and "2019-09-01T21:00".</span></span>

### <span data-ttu-id="ac1e7-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="ac1e7-112">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseTriggerRun -Name ContosoTrigger -RunStartedAfter [DateTimeOffset]"2018-09-01T21:00" -RunStartedBefore [DateTimeOffset]"2019-09-01T21:00"
```

<span data-ttu-id="ac1e7-113">Esse comando mostra informações sobre execuções de ContosoTrigger no espaço de trabalho ContosoWorkspace que começou entre "2018-09-01T21:00" e "2019-09-01T21:00" por meio do pipeline.</span><span class="sxs-lookup"><span data-stu-id="ac1e7-113">This command shows information about runs for ContosoTrigger in the workspace ContosoWorkspace that started between "2018-09-01T21:00" and "2019-09-01T21:00" through pipeline.</span></span>

## <span data-ttu-id="ac1e7-114">OS</span><span class="sxs-lookup"><span data-stu-id="ac1e7-114">PARAMETERS</span></span>

### <span data-ttu-id="ac1e7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac1e7-115">-DefaultProfile</span></span>
<span data-ttu-id="ac1e7-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ac1e7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac1e7-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="ac1e7-117">-Name</span></span>
<span data-ttu-id="ac1e7-118">O nome do disparador.</span><span class="sxs-lookup"><span data-stu-id="ac1e7-118">The trigger name.</span></span>

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

### <span data-ttu-id="ac1e7-119">-RunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="ac1e7-119">-RunStartedAfter</span></span>
<span data-ttu-id="ac1e7-120">A hora em ou após a qual o evento de execução foi atualizado no formato ' ISO 8601 '.</span><span class="sxs-lookup"><span data-stu-id="ac1e7-120">The time at or after which the run event was updated in 'ISO 8601' format.</span></span>

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

### <span data-ttu-id="ac1e7-121">-RunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="ac1e7-121">-RunStartedBefore</span></span>
<span data-ttu-id="ac1e7-122">A hora em ou antes da qual o evento de execução foi atualizado no formato ' ISO 8601 '.</span><span class="sxs-lookup"><span data-stu-id="ac1e7-122">The time at or before which the run event was updated in 'ISO 8601' format.</span></span>

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

### <span data-ttu-id="ac1e7-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ac1e7-123">-WorkspaceName</span></span>
<span data-ttu-id="ac1e7-124">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="ac1e7-124">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="ac1e7-125">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="ac1e7-125">-WorkspaceObject</span></span>
<span data-ttu-id="ac1e7-126">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="ac1e7-126">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="ac1e7-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac1e7-127">CommonParameters</span></span>
<span data-ttu-id="ac1e7-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac1e7-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac1e7-129">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ac1e7-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac1e7-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ac1e7-130">INPUTS</span></span>

### <span data-ttu-id="ac1e7-131">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="ac1e7-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="ac1e7-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ac1e7-132">OUTPUTS</span></span>

### <span data-ttu-id="ac1e7-133">Microsoft. Azure. Commands. Synapse. Models. PSTriggerRun</span><span class="sxs-lookup"><span data-stu-id="ac1e7-133">Microsoft.Azure.Commands.Synapse.Models.PSTriggerRun</span></span>

## <span data-ttu-id="ac1e7-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ac1e7-134">NOTES</span></span>

## <span data-ttu-id="ac1e7-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ac1e7-135">RELATED LINKS</span></span>
