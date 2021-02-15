---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseDataset.md
ms.openlocfilehash: d2471320a27b1af96dba6b5e2b552a01ff5b50e3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116300"
---
# <span data-ttu-id="286ac-101">Set-AzSynapseDataset</span><span class="sxs-lookup"><span data-stu-id="286ac-101">Set-AzSynapseDataset</span></span>

## <span data-ttu-id="286ac-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="286ac-102">SYNOPSIS</span></span>
<span data-ttu-id="286ac-103">Cria ou atualiza um conjuntos de dados no espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="286ac-103">Creates or updates a dataset in workspace.</span></span>

## <span data-ttu-id="286ac-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="286ac-104">SYNTAX</span></span>

### <span data-ttu-id="286ac-105">SetByName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="286ac-105">SetByName (Default)</span></span>
```
Set-AzSynapseDataset -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="286ac-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="286ac-106">SetByObject</span></span>
```
Set-AzSynapseDataset -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="286ac-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="286ac-107">DESCRIPTION</span></span>
<span data-ttu-id="286ac-108">O cmdlet **Set-AzSynapseDataset** cria um conjunto de dados ou atualiza um conjunto de dados existente no espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="286ac-108">The **Set-AzSynapseDataset** cmdlet creates a dataset or updates an existing dataset in workspace.</span></span>

## <span data-ttu-id="286ac-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="286ac-109">EXAMPLES</span></span>

### <span data-ttu-id="286ac-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="286ac-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseDataset -WorkspaceName ContosoWorkspace -Name ContosoDataset -DefinitionFile "C:\\samples\\Dataset.json"
```

<span data-ttu-id="286ac-111">Esse comando cria um grupo de dados chamado ContosoDataset no espaço de trabalho chamado ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="286ac-111">This command creates a dataset named ContosoDataset in the workspace named ContosoWorkspace.</span></span>
<span data-ttu-id="286ac-112">O comando baseia o conjuntos de dados em informações no Dataset.jsno arquivo.</span><span class="sxs-lookup"><span data-stu-id="286ac-112">The command bases the dataset on information in the Dataset.json file.</span></span>

## <span data-ttu-id="286ac-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="286ac-113">PARAMETERS</span></span>

### <span data-ttu-id="286ac-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="286ac-114">-AsJob</span></span>
<span data-ttu-id="286ac-115">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="286ac-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="286ac-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="286ac-116">-DefaultProfile</span></span>
<span data-ttu-id="286ac-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="286ac-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="286ac-118">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="286ac-118">-DefinitionFile</span></span>
<span data-ttu-id="286ac-119">O caminho do arquivo JSON.</span><span class="sxs-lookup"><span data-stu-id="286ac-119">The JSON file path.</span></span>

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

### <span data-ttu-id="286ac-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="286ac-120">-Name</span></span>
<span data-ttu-id="286ac-121">O nome do conjuntos de dados.</span><span class="sxs-lookup"><span data-stu-id="286ac-121">The dataset name.</span></span>

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

### <span data-ttu-id="286ac-122">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="286ac-122">-WorkspaceName</span></span>
<span data-ttu-id="286ac-123">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="286ac-123">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="286ac-124">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="286ac-124">-WorkspaceObject</span></span>
<span data-ttu-id="286ac-125">objeto de entrada de espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="286ac-125">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="286ac-126">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="286ac-126">-Confirm</span></span>
<span data-ttu-id="286ac-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="286ac-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="286ac-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="286ac-128">-WhatIf</span></span>
<span data-ttu-id="286ac-129">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="286ac-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="286ac-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="286ac-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="286ac-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="286ac-131">CommonParameters</span></span>
<span data-ttu-id="286ac-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="286ac-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="286ac-133">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="286ac-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="286ac-134">Entradas</span><span class="sxs-lookup"><span data-stu-id="286ac-134">INPUTS</span></span>

### <span data-ttu-id="286ac-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="286ac-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="286ac-136">Saídas</span><span class="sxs-lookup"><span data-stu-id="286ac-136">OUTPUTS</span></span>

### <span data-ttu-id="286ac-137">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span><span class="sxs-lookup"><span data-stu-id="286ac-137">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span></span>

## <span data-ttu-id="286ac-138">Notas</span><span class="sxs-lookup"><span data-stu-id="286ac-138">NOTES</span></span>

## <span data-ttu-id="286ac-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="286ac-139">RELATED LINKS</span></span>
