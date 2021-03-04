---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/set-azsynapsedataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseDataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseDataFlow.md
ms.openlocfilehash: 4254a301e599dac542a099b9c4f2ebace8929ab4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885508"
---
# <span data-ttu-id="aa32b-101">Set-AzSynapseDataFlow</span><span class="sxs-lookup"><span data-stu-id="aa32b-101">Set-AzSynapseDataFlow</span></span>

## <span data-ttu-id="aa32b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa32b-102">SYNOPSIS</span></span>
<span data-ttu-id="aa32b-103">Cria ou atualiza um fluxo de dados no espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="aa32b-103">Creates or updates a data flow in workspace.</span></span>

## <span data-ttu-id="aa32b-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="aa32b-104">SYNTAX</span></span>

### <span data-ttu-id="aa32b-105">SetByName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="aa32b-105">SetByName (Default)</span></span>
```
Set-AzSynapseDataFlow -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa32b-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="aa32b-106">SetByObject</span></span>
```
Set-AzSynapseDataFlow -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa32b-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="aa32b-107">DESCRIPTION</span></span>
<span data-ttu-id="aa32b-108">O cmdlet **Set-AzSynapseDataFlow** cria um fluxo de dados ou atualiza um fluxo de dados existente no espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="aa32b-108">The **Set-AzSynapseDataFlow** cmdlet creates a data flow or updates an existing data flow in workspace.</span></span>

## <span data-ttu-id="aa32b-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="aa32b-109">EXAMPLES</span></span>

### <span data-ttu-id="aa32b-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="aa32b-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseDataFlow -WorkspaceName ContosoWorkspace -Name ContosoDataFlow -DefinitionFile "C:\\samples\\DataFlow.json"
```

<span data-ttu-id="aa32b-111">Este comando cria um fluxo de dados chamado ContosoDataFlow no espaço de trabalho chamado ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="aa32b-111">This command creates a data flow named ContosoDataFlow in the workspace named ContosoWorkspace.</span></span>
<span data-ttu-id="aa32b-112">O comando baseia o fluxo de dados em informações no arquivo DataFlow.json.</span><span class="sxs-lookup"><span data-stu-id="aa32b-112">The command bases the data flow on information in the DataFlow.json file.</span></span>

## <span data-ttu-id="aa32b-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="aa32b-113">PARAMETERS</span></span>

### <span data-ttu-id="aa32b-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aa32b-114">-AsJob</span></span>
<span data-ttu-id="aa32b-115">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="aa32b-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa32b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa32b-116">-DefaultProfile</span></span>
<span data-ttu-id="aa32b-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="aa32b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa32b-118">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="aa32b-118">-DefinitionFile</span></span>
<span data-ttu-id="aa32b-119">O caminho do arquivo JSON.</span><span class="sxs-lookup"><span data-stu-id="aa32b-119">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa32b-120">-Name</span><span class="sxs-lookup"><span data-stu-id="aa32b-120">-Name</span></span>
<span data-ttu-id="aa32b-121">O nome do fluxo de dados.</span><span class="sxs-lookup"><span data-stu-id="aa32b-121">The data flow name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DataFlowName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa32b-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="aa32b-122">-WorkspaceName</span></span>
<span data-ttu-id="aa32b-123">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="aa32b-123">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa32b-124">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="aa32b-124">-WorkspaceObject</span></span>
<span data-ttu-id="aa32b-125">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="aa32b-125">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aa32b-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aa32b-126">-Confirm</span></span>
<span data-ttu-id="aa32b-127">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa32b-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa32b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa32b-128">-WhatIf</span></span>
<span data-ttu-id="aa32b-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="aa32b-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa32b-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="aa32b-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa32b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa32b-131">CommonParameters</span></span>
<span data-ttu-id="aa32b-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa32b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa32b-133">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aa32b-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa32b-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="aa32b-134">INPUTS</span></span>

### <span data-ttu-id="aa32b-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="aa32b-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="aa32b-136">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="aa32b-136">OUTPUTS</span></span>

### <span data-ttu-id="aa32b-137">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span><span class="sxs-lookup"><span data-stu-id="aa32b-137">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span></span>

## <span data-ttu-id="aa32b-138">NOTES</span><span class="sxs-lookup"><span data-stu-id="aa32b-138">NOTES</span></span>

## <span data-ttu-id="aa32b-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="aa32b-139">RELATED LINKS</span></span>
