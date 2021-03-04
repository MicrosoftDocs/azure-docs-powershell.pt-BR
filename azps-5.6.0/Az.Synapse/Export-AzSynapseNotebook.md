---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/export-azsynapsenotebook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Export-AzSynapseNotebook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Export-AzSynapseNotebook.md
ms.openlocfilehash: 110d72f0a73a6a710e014a08c64cadf3b8be7d0e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889119"
---
# <span data-ttu-id="4cf05-101">Export-AzSynapseNotebook</span><span class="sxs-lookup"><span data-stu-id="4cf05-101">Export-AzSynapseNotebook</span></span>

## <span data-ttu-id="4cf05-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4cf05-102">SYNOPSIS</span></span>
<span data-ttu-id="4cf05-103">Exporta notbooks.</span><span class="sxs-lookup"><span data-stu-id="4cf05-103">Exports notbooks.</span></span>

## <span data-ttu-id="4cf05-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="4cf05-104">SYNTAX</span></span>

### <span data-ttu-id="4cf05-105">ExportByName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="4cf05-105">ExportByName (Default)</span></span>
```
Export-AzSynapseNotebook -WorkspaceName <String> [-Name <String>] -OutputFolder <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4cf05-106">ExportByObject</span><span class="sxs-lookup"><span data-stu-id="4cf05-106">ExportByObject</span></span>
```
Export-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> [-Name <String>] -OutputFolder <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4cf05-107">ExportByInputObject</span><span class="sxs-lookup"><span data-stu-id="4cf05-107">ExportByInputObject</span></span>
```
Export-AzSynapseNotebook -InputObject <PSNotebookResource> -OutputFolder <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4cf05-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="4cf05-108">DESCRIPTION</span></span>
<span data-ttu-id="4cf05-109">O cmdlet **Export-AzSynapseNotebook** exporta um bloco de anotações synapse do Azure para um arquivo de bloco de anotações (.ipynb).</span><span class="sxs-lookup"><span data-stu-id="4cf05-109">The **Export-AzSynapseNotebook** cmdlet exports an Azure Synapse notebook to a notebook (.ipynb) file.</span></span> <span data-ttu-id="4cf05-110">O nome do bloco de anotações se torna o nome do arquivo exportado.</span><span class="sxs-lookup"><span data-stu-id="4cf05-110">The name of the notebook becomes the name of the exported file.</span></span> <span data-ttu-id="4cf05-111">Se você especificar o nome de um bloco de anotações, o cmdlet exportará esse bloco de anotações.</span><span class="sxs-lookup"><span data-stu-id="4cf05-111">If you specify the name of a notebook, the cmdlet exports that notebook.</span></span> <span data-ttu-id="4cf05-112">Se você não especificar um nome, o cmdlet exportará todos os blocos de anotações no espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="4cf05-112">If you do not specify a name, the cmdlet export all notebooks in the workspace.</span></span>

## <span data-ttu-id="4cf05-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4cf05-113">EXAMPLES</span></span>

### <span data-ttu-id="4cf05-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4cf05-114">Example 1</span></span>
```powershell
PS C:\> Export-AzSynapseNotebook -WorkspaceName ContosoWorkspace -OutputFolder "C:\Notebook"
```

<span data-ttu-id="4cf05-115">Exporta todos os blocos de anotações no espaço de trabalho ContosoWorkspace para a pasta "C:\Notebook".</span><span class="sxs-lookup"><span data-stu-id="4cf05-115">Exports all notebooks in the workspace ContosoWorkspace to the folder "C:\Notebook".</span></span>

### <span data-ttu-id="4cf05-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="4cf05-116">Example 2</span></span>
```powershell
PS C:\> Export-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook -OutputFolder "C:\Notebook"
```

<span data-ttu-id="4cf05-117">Exporta um único bloco de anotações chamado ContosoNotebook no espaço de trabalho ContosoWorkspace para a pasta "C:\Notebook".</span><span class="sxs-lookup"><span data-stu-id="4cf05-117">Exports a single notebook called ContosoNotebook in the workspace ContosoWorkspace to the folder "C:\Notebook".</span></span>

### <span data-ttu-id="4cf05-118">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="4cf05-118">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Export-AzSynapseNotebook -Name ContosoNotebook -OutputFolder "C:\Notebook"
```

<span data-ttu-id="4cf05-119">Exporta um único bloco de anotações chamado ContosoNotebook no espaço de trabalho ContosoWorkspace para a pasta "C:\Notebook" por meio de pipeline.</span><span class="sxs-lookup"><span data-stu-id="4cf05-119">Exports a single notebook called ContosoNotebook in the workspace ContosoWorkspace to the folder "C:\Notebook" through pipeline.</span></span>

### <span data-ttu-id="4cf05-120">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="4cf05-120">Example 4</span></span>
```powershell
PS C:\> $notebook = Get-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook
PS C:\> $notebook | Export-AzSynapseNotebook -OutputFolder "C:\Notebook"
```

<span data-ttu-id="4cf05-121">Exporta um único bloco de anotações chamado ContosoNotebook no espaço de trabalho ContosoWorkspace para a pasta "C:\Notebook" por meio de pipeline.</span><span class="sxs-lookup"><span data-stu-id="4cf05-121">Exports a single notebook called ContosoNotebook in the workspace ContosoWorkspace to the folder "C:\Notebook" through pipeline.</span></span>

## <span data-ttu-id="4cf05-122">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="4cf05-122">PARAMETERS</span></span>

### <span data-ttu-id="4cf05-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4cf05-123">-AsJob</span></span>
<span data-ttu-id="4cf05-124">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="4cf05-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4cf05-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cf05-125">-DefaultProfile</span></span>
<span data-ttu-id="4cf05-126">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4cf05-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4cf05-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4cf05-127">-InputObject</span></span>
<span data-ttu-id="4cf05-128">O objeto notebook.</span><span class="sxs-lookup"><span data-stu-id="4cf05-128">The notebook object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource
Parameter Sets: ExportByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4cf05-129">-Name</span><span class="sxs-lookup"><span data-stu-id="4cf05-129">-Name</span></span>
<span data-ttu-id="4cf05-130">O nome do bloco de anotações.</span><span class="sxs-lookup"><span data-stu-id="4cf05-130">The notebook name.</span></span>

```yaml
Type: System.String
Parameter Sets: ExportByName, ExportByObject
Aliases: NotebookName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cf05-131">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="4cf05-131">-OutputFolder</span></span>
<span data-ttu-id="4cf05-132">A pasta onde o bloco de anotações deve ser colocado.</span><span class="sxs-lookup"><span data-stu-id="4cf05-132">The folder where the notebook should be placed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cf05-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="4cf05-133">-WorkspaceName</span></span>
<span data-ttu-id="4cf05-134">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="4cf05-134">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: ExportByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cf05-135">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="4cf05-135">-WorkspaceObject</span></span>
<span data-ttu-id="4cf05-136">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="4cf05-136">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: ExportByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4cf05-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cf05-137">CommonParameters</span></span>
<span data-ttu-id="4cf05-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4cf05-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cf05-139">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4cf05-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cf05-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4cf05-140">INPUTS</span></span>

### <span data-ttu-id="4cf05-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="4cf05-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="4cf05-142">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span><span class="sxs-lookup"><span data-stu-id="4cf05-142">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span></span>

## <span data-ttu-id="4cf05-143">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="4cf05-143">OUTPUTS</span></span>

### <span data-ttu-id="4cf05-144">System.IO.FileInfo</span><span class="sxs-lookup"><span data-stu-id="4cf05-144">System.IO.FileInfo</span></span>

## <span data-ttu-id="4cf05-145">NOTES</span><span class="sxs-lookup"><span data-stu-id="4cf05-145">NOTES</span></span>

## <span data-ttu-id="4cf05-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4cf05-146">RELATED LINKS</span></span>
