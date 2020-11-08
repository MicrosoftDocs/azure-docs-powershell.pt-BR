---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTrigger.md
ms.openlocfilehash: 9e39d6458ca330909e500a45532d0a9d66f404af
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94117917"
---
# <span data-ttu-id="9b8f8-101">Get-AzSynapseTrigger</span><span class="sxs-lookup"><span data-stu-id="9b8f8-101">Get-AzSynapseTrigger</span></span>

## <span data-ttu-id="9b8f8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9b8f8-102">SYNOPSIS</span></span>
<span data-ttu-id="9b8f8-103">Obtém informações sobre gatilhos em um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="9b8f8-103">Gets information about triggers in a workspace.</span></span>

## <span data-ttu-id="9b8f8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9b8f8-104">SYNTAX</span></span>

### <span data-ttu-id="9b8f8-105">GetByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="9b8f8-105">GetByName (Default)</span></span>
```
Get-AzSynapseTrigger -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9b8f8-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="9b8f8-106">GetByObject</span></span>
```
Get-AzSynapseTrigger -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9b8f8-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9b8f8-107">DESCRIPTION</span></span>
<span data-ttu-id="9b8f8-108">O cmdlet **Get-AzSynapseTrigger** Obtém informações sobre gatilhos em um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="9b8f8-108">The **Get-AzSynapseTrigger** cmdlet gets information about triggers in a workspace.</span></span> <span data-ttu-id="9b8f8-109">Se você especificar o nome de um gatilho, o cmdlet obterá informações sobre esse gatilho.</span><span class="sxs-lookup"><span data-stu-id="9b8f8-109">If you specify the name of a trigger, the cmdlet gets information about that trigger.</span></span> <span data-ttu-id="9b8f8-110">Se você não especificar um nome, o cmdlet obterá informações sobre todos os gatilhos do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="9b8f8-110">If you do not specify a name, the cmdlet gets information about all triggers in the workspace.</span></span>

## <span data-ttu-id="9b8f8-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9b8f8-111">EXAMPLES</span></span>

### <span data-ttu-id="9b8f8-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9b8f8-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="9b8f8-113">Obtém uma lista de todos os gatilhos que foram criados na área de trabalho ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="9b8f8-113">Gets a list of all triggers that have been created in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="9b8f8-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="9b8f8-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="9b8f8-115">Obtém um único gatilho chamado ContosoTrigger na ContosoWorkspace do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="9b8f8-115">Gets a single trigger called ContosoTrigger in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="9b8f8-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="9b8f8-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseTrigger -Name ContosoTrigger
```

<span data-ttu-id="9b8f8-117">Obtém um único gatilho chamado ContosoTrigger no espaço de trabalho ContosoWorkspace pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="9b8f8-117">Gets a single trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="9b8f8-118">OS</span><span class="sxs-lookup"><span data-stu-id="9b8f8-118">PARAMETERS</span></span>

### <span data-ttu-id="9b8f8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b8f8-119">-DefaultProfile</span></span>
<span data-ttu-id="9b8f8-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9b8f8-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b8f8-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="9b8f8-121">-Name</span></span>
<span data-ttu-id="9b8f8-122">O nome do disparador.</span><span class="sxs-lookup"><span data-stu-id="9b8f8-122">The trigger name.</span></span>

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

### <span data-ttu-id="9b8f8-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9b8f8-123">-WorkspaceName</span></span>
<span data-ttu-id="9b8f8-124">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="9b8f8-124">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="9b8f8-125">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="9b8f8-125">-WorkspaceObject</span></span>
<span data-ttu-id="9b8f8-126">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="9b8f8-126">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="9b8f8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b8f8-127">CommonParameters</span></span>
<span data-ttu-id="9b8f8-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b8f8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b8f8-129">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9b8f8-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b8f8-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9b8f8-130">INPUTS</span></span>

### <span data-ttu-id="9b8f8-131">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="9b8f8-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="9b8f8-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9b8f8-132">OUTPUTS</span></span>

### <span data-ttu-id="9b8f8-133">Microsoft. Azure. Commands. Synapse. Models. PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="9b8f8-133">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="9b8f8-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9b8f8-134">NOTES</span></span>

## <span data-ttu-id="9b8f8-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9b8f8-135">RELATED LINKS</span></span>
