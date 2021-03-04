---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/set-azsynapsedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseDataset.md
ms.openlocfilehash: 1001aa2f282ab59e6ddc9e3e1ecc654950d8e30e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885507"
---
# <span data-ttu-id="f1451-101">Set-AzSynapseDataset</span><span class="sxs-lookup"><span data-stu-id="f1451-101">Set-AzSynapseDataset</span></span>

## <span data-ttu-id="f1451-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1451-102">SYNOPSIS</span></span>
<span data-ttu-id="f1451-103">Cria ou atualiza um conjuntos de dados no espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="f1451-103">Creates or updates a dataset in workspace.</span></span>

## <span data-ttu-id="f1451-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f1451-104">SYNTAX</span></span>

### <span data-ttu-id="f1451-105">SetByName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="f1451-105">SetByName (Default)</span></span>
```
Set-AzSynapseDataset -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1451-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="f1451-106">SetByObject</span></span>
```
Set-AzSynapseDataset -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1451-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f1451-107">DESCRIPTION</span></span>
<span data-ttu-id="f1451-108">O cmdlet **Set-AzSynapseDataset** cria um conjunto de dados ou atualiza um conjunto de dados existente no espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="f1451-108">The **Set-AzSynapseDataset** cmdlet creates a dataset or updates an existing dataset in workspace.</span></span>

## <span data-ttu-id="f1451-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f1451-109">EXAMPLES</span></span>

### <span data-ttu-id="f1451-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f1451-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseDataset -WorkspaceName ContosoWorkspace -Name ContosoDataset -DefinitionFile "C:\\samples\\Dataset.json"
```

<span data-ttu-id="f1451-111">Este comando cria um grupo de dados chamado ContosoDataset no espaço de trabalho chamado ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="f1451-111">This command creates a dataset named ContosoDataset in the workspace named ContosoWorkspace.</span></span>
<span data-ttu-id="f1451-112">O comando baseia o conjuntos de dados em informações no arquivo Dataset.json.</span><span class="sxs-lookup"><span data-stu-id="f1451-112">The command bases the dataset on information in the Dataset.json file.</span></span>

## <span data-ttu-id="f1451-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f1451-113">PARAMETERS</span></span>

### <span data-ttu-id="f1451-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f1451-114">-AsJob</span></span>
<span data-ttu-id="f1451-115">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="f1451-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f1451-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1451-116">-DefaultProfile</span></span>
<span data-ttu-id="f1451-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f1451-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1451-118">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="f1451-118">-DefinitionFile</span></span>
<span data-ttu-id="f1451-119">O caminho do arquivo JSON.</span><span class="sxs-lookup"><span data-stu-id="f1451-119">The JSON file path.</span></span>

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

### <span data-ttu-id="f1451-120">-Name</span><span class="sxs-lookup"><span data-stu-id="f1451-120">-Name</span></span>
<span data-ttu-id="f1451-121">O nome do conjuntos de dados.</span><span class="sxs-lookup"><span data-stu-id="f1451-121">The dataset name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DatasetName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1451-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f1451-122">-WorkspaceName</span></span>
<span data-ttu-id="f1451-123">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="f1451-123">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="f1451-124">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="f1451-124">-WorkspaceObject</span></span>
<span data-ttu-id="f1451-125">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="f1451-125">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="f1451-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f1451-126">-Confirm</span></span>
<span data-ttu-id="f1451-127">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f1451-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1451-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1451-128">-WhatIf</span></span>
<span data-ttu-id="f1451-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f1451-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1451-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f1451-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1451-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1451-131">CommonParameters</span></span>
<span data-ttu-id="f1451-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1451-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1451-133">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f1451-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1451-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f1451-134">INPUTS</span></span>

### <span data-ttu-id="f1451-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="f1451-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="f1451-136">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f1451-136">OUTPUTS</span></span>

### <span data-ttu-id="f1451-137">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span><span class="sxs-lookup"><span data-stu-id="f1451-137">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span></span>

## <span data-ttu-id="f1451-138">NOTES</span><span class="sxs-lookup"><span data-stu-id="f1451-138">NOTES</span></span>

## <span data-ttu-id="f1451-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f1451-139">RELATED LINKS</span></span>
