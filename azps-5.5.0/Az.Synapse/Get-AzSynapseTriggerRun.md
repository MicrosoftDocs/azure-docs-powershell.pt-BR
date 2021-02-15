---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsetriggerrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTriggerRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTriggerRun.md
ms.openlocfilehash: 0d6d3bb99062177e1d75c4ab496562782cf142c1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114370"
---
# <span data-ttu-id="bba24-101">Get-AzSynapseTriggerRun</span><span class="sxs-lookup"><span data-stu-id="bba24-101">Get-AzSynapseTriggerRun</span></span>

## <span data-ttu-id="bba24-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bba24-102">SYNOPSIS</span></span>
<span data-ttu-id="bba24-103">Retorna informações sobre o gatilho executado.</span><span class="sxs-lookup"><span data-stu-id="bba24-103">Returns information about trigger runs.</span></span>

## <span data-ttu-id="bba24-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bba24-104">SYNTAX</span></span>

### <span data-ttu-id="bba24-105">GetByName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="bba24-105">GetByName (Default)</span></span>
```
Get-AzSynapseTriggerRun -WorkspaceName <String> -Name <String> -RunStartedAfter <DateTimeOffset>
 -RunStartedBefore <DateTimeOffset> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bba24-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="bba24-106">GetByObject</span></span>
```
Get-AzSynapseTriggerRun -WorkspaceObject <PSSynapseWorkspace> -Name <String> -RunStartedAfter <DateTimeOffset>
 -RunStartedBefore <DateTimeOffset> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bba24-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="bba24-107">DESCRIPTION</span></span>
<span data-ttu-id="bba24-108">O **comando Get-AzSynapseTriframeRun** retorna informações detalhadas sobre o gatilho executado para o gatilho especificado no determinado prazo.</span><span class="sxs-lookup"><span data-stu-id="bba24-108">The **Get-AzSynapseTriggerRun** command returns detailed information about trigger runs for the specified trigger in the given timeframe.</span></span>

## <span data-ttu-id="bba24-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="bba24-109">EXAMPLES</span></span>

### <span data-ttu-id="bba24-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bba24-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseTriggerRun -WorkspaceName ContosoWorkspace -Name ContosoTrigger -RunStartedAfter [DateTimeOffset]"2018-09-01T21:00" -RunStartedBefore [DateTimeOffset]"2019-09-01T21:00"
```

<span data-ttu-id="bba24-111">Este comando mostra informações sobre as executados para ContosoTrigger no espaço de trabalho ContosoWorkspace que começou entre "2018-09-01T21:00" e "2019-09-01T21:00".</span><span class="sxs-lookup"><span data-stu-id="bba24-111">This command shows information about runs for ContosoTrigger in the workspace ContosoWorkspace that started between "2018-09-01T21:00" and "2019-09-01T21:00".</span></span>

### <span data-ttu-id="bba24-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="bba24-112">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseTriggerRun -Name ContosoTrigger -RunStartedAfter [DateTimeOffset]"2018-09-01T21:00" -RunStartedBefore [DateTimeOffset]"2019-09-01T21:00"
```

<span data-ttu-id="bba24-113">Este comando mostra informações sobre as executados para ContosoTri pipeline no espaço de trabalho ContosoWorkspace que começou entre "2018-09-01T21:00" e "2019-09-01T21:00" por meio do pipeline.</span><span class="sxs-lookup"><span data-stu-id="bba24-113">This command shows information about runs for ContosoTrigger in the workspace ContosoWorkspace that started between "2018-09-01T21:00" and "2019-09-01T21:00" through pipeline.</span></span>

## <span data-ttu-id="bba24-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bba24-114">PARAMETERS</span></span>

### <span data-ttu-id="bba24-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bba24-115">-DefaultProfile</span></span>
<span data-ttu-id="bba24-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bba24-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bba24-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="bba24-117">-Name</span></span>
<span data-ttu-id="bba24-118">O nome do gatilho.</span><span class="sxs-lookup"><span data-stu-id="bba24-118">The trigger name.</span></span>

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

### <span data-ttu-id="bba24-119">-ExecutarStartedAfter</span><span class="sxs-lookup"><span data-stu-id="bba24-119">-RunStartedAfter</span></span>
<span data-ttu-id="bba24-120">O horário em que o evento de executar foi atualizado no formato 'ISO 8601'.</span><span class="sxs-lookup"><span data-stu-id="bba24-120">The time at or after which the run event was updated in 'ISO 8601' format.</span></span>

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

### <span data-ttu-id="bba24-121">-ExecutarStartedBefore</span><span class="sxs-lookup"><span data-stu-id="bba24-121">-RunStartedBefore</span></span>
<span data-ttu-id="bba24-122">O horário em que o evento de executar foi atualizado no formato 'ISO 8601'.</span><span class="sxs-lookup"><span data-stu-id="bba24-122">The time at or before which the run event was updated in 'ISO 8601' format.</span></span>

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

### <span data-ttu-id="bba24-123">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="bba24-123">-WorkspaceName</span></span>
<span data-ttu-id="bba24-124">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="bba24-124">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="bba24-125">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="bba24-125">-WorkspaceObject</span></span>
<span data-ttu-id="bba24-126">objeto de entrada de espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="bba24-126">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="bba24-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bba24-127">CommonParameters</span></span>
<span data-ttu-id="bba24-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bba24-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bba24-129">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bba24-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bba24-130">Entradas</span><span class="sxs-lookup"><span data-stu-id="bba24-130">INPUTS</span></span>

### <span data-ttu-id="bba24-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="bba24-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="bba24-132">Saídas</span><span class="sxs-lookup"><span data-stu-id="bba24-132">OUTPUTS</span></span>

### <span data-ttu-id="bba24-133">Microsoft.Azure.Commands.Synapse.Models.PSTri googleRun</span><span class="sxs-lookup"><span data-stu-id="bba24-133">Microsoft.Azure.Commands.Synapse.Models.PSTriggerRun</span></span>

## <span data-ttu-id="bba24-134">Notas</span><span class="sxs-lookup"><span data-stu-id="bba24-134">NOTES</span></span>

## <span data-ttu-id="bba24-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bba24-135">RELATED LINKS</span></span>
