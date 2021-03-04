---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTrigger.md
ms.openlocfilehash: 988d2f53ebf0bf69806bf06fedb5e2db31c9d0c2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888019"
---
# <span data-ttu-id="b2db1-101">Get-AzSynapseTrigger</span><span class="sxs-lookup"><span data-stu-id="b2db1-101">Get-AzSynapseTrigger</span></span>

## <span data-ttu-id="b2db1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2db1-102">SYNOPSIS</span></span>
<span data-ttu-id="b2db1-103">Obtém informações sobre gatilhos em um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="b2db1-103">Gets information about triggers in a workspace.</span></span>

## <span data-ttu-id="b2db1-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b2db1-104">SYNTAX</span></span>

### <span data-ttu-id="b2db1-105">GetByName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="b2db1-105">GetByName (Default)</span></span>
```
Get-AzSynapseTrigger -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b2db1-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="b2db1-106">GetByObject</span></span>
```
Get-AzSynapseTrigger -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b2db1-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b2db1-107">DESCRIPTION</span></span>
<span data-ttu-id="b2db1-108">O cmdlet **Get-AzSynapseTrigger** obtém informações sobre gatilhos em um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="b2db1-108">The **Get-AzSynapseTrigger** cmdlet gets information about triggers in a workspace.</span></span> <span data-ttu-id="b2db1-109">Se você especificar o nome de um gatilho, o cmdlet obterá informações sobre esse gatilho.</span><span class="sxs-lookup"><span data-stu-id="b2db1-109">If you specify the name of a trigger, the cmdlet gets information about that trigger.</span></span> <span data-ttu-id="b2db1-110">Se você não especificar um nome, o cmdlet obterá informações sobre todos os gatilhos no espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="b2db1-110">If you do not specify a name, the cmdlet gets information about all triggers in the workspace.</span></span>

## <span data-ttu-id="b2db1-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b2db1-111">EXAMPLES</span></span>

### <span data-ttu-id="b2db1-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b2db1-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="b2db1-113">Obtém uma lista de todos os gatilhos que foram criados no espaço de trabalho ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="b2db1-113">Gets a list of all triggers that have been created in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="b2db1-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="b2db1-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="b2db1-115">Obtém um único gatilho chamado ContosoTrigger no espaço de trabalho ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="b2db1-115">Gets a single trigger called ContosoTrigger in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="b2db1-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="b2db1-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseTrigger -Name ContosoTrigger
```

<span data-ttu-id="b2db1-117">Obtém um único gatilho chamado ContosoTrigger no espaço de trabalho ContosoWorkspace por meio de pipeline.</span><span class="sxs-lookup"><span data-stu-id="b2db1-117">Gets a single trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="b2db1-118">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b2db1-118">PARAMETERS</span></span>

### <span data-ttu-id="b2db1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2db1-119">-DefaultProfile</span></span>
<span data-ttu-id="b2db1-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b2db1-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2db1-121">-Name</span><span class="sxs-lookup"><span data-stu-id="b2db1-121">-Name</span></span>
<span data-ttu-id="b2db1-122">O nome do gatilho.</span><span class="sxs-lookup"><span data-stu-id="b2db1-122">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TriggerName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2db1-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b2db1-123">-WorkspaceName</span></span>
<span data-ttu-id="b2db1-124">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="b2db1-124">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="b2db1-125">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="b2db1-125">-WorkspaceObject</span></span>
<span data-ttu-id="b2db1-126">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="b2db1-126">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="b2db1-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2db1-127">CommonParameters</span></span>
<span data-ttu-id="b2db1-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2db1-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2db1-129">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b2db1-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2db1-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b2db1-130">INPUTS</span></span>

### <span data-ttu-id="b2db1-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="b2db1-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="b2db1-132">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b2db1-132">OUTPUTS</span></span>

### <span data-ttu-id="b2db1-133">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="b2db1-133">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="b2db1-134">NOTES</span><span class="sxs-lookup"><span data-stu-id="b2db1-134">NOTES</span></span>

## <span data-ttu-id="b2db1-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b2db1-135">RELATED LINKS</span></span>
