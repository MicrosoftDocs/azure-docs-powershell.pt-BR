---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/export-azsynapsenotebook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Export-AzSynapseNotebook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Export-AzSynapseNotebook.md
ms.openlocfilehash: d61038add8ded9f697bfef551e00aec24c8aaf3e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118900"
---
# <span data-ttu-id="6e2d8-101">Export-AzSynapseNotebook</span><span class="sxs-lookup"><span data-stu-id="6e2d8-101">Export-AzSynapseNotebook</span></span>

## <span data-ttu-id="6e2d8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6e2d8-102">SYNOPSIS</span></span>
<span data-ttu-id="6e2d8-103">Exporta não livros.</span><span class="sxs-lookup"><span data-stu-id="6e2d8-103">Exports notbooks.</span></span>

## <span data-ttu-id="6e2d8-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6e2d8-104">SYNTAX</span></span>

### <span data-ttu-id="6e2d8-105">ExportByName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="6e2d8-105">ExportByName (Default)</span></span>
```
Export-AzSynapseNotebook -WorkspaceName <String> [-Name <String>] -OutputFolder <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6e2d8-106">ExportByObject</span><span class="sxs-lookup"><span data-stu-id="6e2d8-106">ExportByObject</span></span>
```
Export-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> [-Name <String>] -OutputFolder <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6e2d8-107">ExportByInputObject</span><span class="sxs-lookup"><span data-stu-id="6e2d8-107">ExportByInputObject</span></span>
```
Export-AzSynapseNotebook -InputObject <PSNotebookResource> -OutputFolder <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6e2d8-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="6e2d8-108">DESCRIPTION</span></span>
<span data-ttu-id="6e2d8-109">O cmdlet **Export-AzSynapseNotebook** exporta um bloco de anotações Azure Synapse para um arquivo de bloco de anotações (.ipynb).</span><span class="sxs-lookup"><span data-stu-id="6e2d8-109">The **Export-AzSynapseNotebook** cmdlet exports an Azure Synapse notebook to a notebook (.ipynb) file.</span></span> <span data-ttu-id="6e2d8-110">O nome do bloco de anotações torna-se o nome do arquivo exportado.</span><span class="sxs-lookup"><span data-stu-id="6e2d8-110">The name of the notebook becomes the name of the exported file.</span></span> <span data-ttu-id="6e2d8-111">Se você especificar o nome de um bloco de anotações, o cmdlet exportará esse bloco de anotações.</span><span class="sxs-lookup"><span data-stu-id="6e2d8-111">If you specify the name of a notebook, the cmdlet exports that notebook.</span></span> <span data-ttu-id="6e2d8-112">Se você não especificar um nome, o cmdlet exportará todos os blocos de anotações no espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="6e2d8-112">If you do not specify a name, the cmdlet export all notebooks in the workspace.</span></span>

## <span data-ttu-id="6e2d8-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6e2d8-113">EXAMPLES</span></span>

### <span data-ttu-id="6e2d8-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6e2d8-114">Example 1</span></span>
```powershell
PS C:\> Export-AzSynapseNotebook -WorkspaceName ContosoWorkspace -OutputFolder "C:\Notebook"
```

<span data-ttu-id="6e2d8-115">Exporta todos os blocos de anotações no espaço de trabalho ContosoWorkspace para a pasta "C:\Bloco de Anotações".</span><span class="sxs-lookup"><span data-stu-id="6e2d8-115">Exports all notebooks in the workspace ContosoWorkspace to the folder "C:\Notebook".</span></span>

### <span data-ttu-id="6e2d8-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="6e2d8-116">Example 2</span></span>
```powershell
PS C:\> Export-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook -OutputFolder "C:\Notebook"
```

<span data-ttu-id="6e2d8-117">Exporta um único bloco de anotações chamado ContosoNotebook no espaço de trabalho ContosoWorkspace para a pasta "C:\Bloco de Anotações".</span><span class="sxs-lookup"><span data-stu-id="6e2d8-117">Exports a single notebook called ContosoNotebook in the workspace ContosoWorkspace to the folder "C:\Notebook".</span></span>

### <span data-ttu-id="6e2d8-118">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="6e2d8-118">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Export-AzSynapseNotebook -Name ContosoNotebook -OutputFolder "C:\Notebook"
```

<span data-ttu-id="6e2d8-119">Exporta um único bloco de anotações chamado ContosoNotebook no espaço de trabalho ContosoWorkspace para a pasta "C:\Notebook" por meio do pipeline.</span><span class="sxs-lookup"><span data-stu-id="6e2d8-119">Exports a single notebook called ContosoNotebook in the workspace ContosoWorkspace to the folder "C:\Notebook" through pipeline.</span></span>

### <span data-ttu-id="6e2d8-120">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="6e2d8-120">Example 4</span></span>
```powershell
PS C:\> $notebook = Get-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook
PS C:\> $notebook | Export-AzSynapseNotebook -OutputFolder "C:\Notebook"
```

<span data-ttu-id="6e2d8-121">Exporta um único bloco de anotações chamado ContosoNotebook no espaço de trabalho ContosoWorkspace para a pasta "C:\Notebook" por meio do pipeline.</span><span class="sxs-lookup"><span data-stu-id="6e2d8-121">Exports a single notebook called ContosoNotebook in the workspace ContosoWorkspace to the folder "C:\Notebook" through pipeline.</span></span>

## <span data-ttu-id="6e2d8-122">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6e2d8-122">PARAMETERS</span></span>

### <span data-ttu-id="6e2d8-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6e2d8-123">-AsJob</span></span>
<span data-ttu-id="6e2d8-124">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="6e2d8-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6e2d8-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e2d8-125">-DefaultProfile</span></span>
<span data-ttu-id="6e2d8-126">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6e2d8-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e2d8-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6e2d8-127">-InputObject</span></span>
<span data-ttu-id="6e2d8-128">O objeto do bloco de anotações.</span><span class="sxs-lookup"><span data-stu-id="6e2d8-128">The notebook object.</span></span>

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

### <span data-ttu-id="6e2d8-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="6e2d8-129">-Name</span></span>
<span data-ttu-id="6e2d8-130">O nome do bloco de anotações.</span><span class="sxs-lookup"><span data-stu-id="6e2d8-130">The notebook name.</span></span>

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

### <span data-ttu-id="6e2d8-131">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="6e2d8-131">-OutputFolder</span></span>
<span data-ttu-id="6e2d8-132">A pasta onde o bloco de anotações deve ser colocado.</span><span class="sxs-lookup"><span data-stu-id="6e2d8-132">The folder where the notebook should be placed.</span></span>

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

### <span data-ttu-id="6e2d8-133">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="6e2d8-133">-WorkspaceName</span></span>
<span data-ttu-id="6e2d8-134">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="6e2d8-134">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="6e2d8-135">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="6e2d8-135">-WorkspaceObject</span></span>
<span data-ttu-id="6e2d8-136">objeto de entrada de espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="6e2d8-136">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="6e2d8-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e2d8-137">CommonParameters</span></span>
<span data-ttu-id="6e2d8-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e2d8-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e2d8-139">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6e2d8-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e2d8-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="6e2d8-140">INPUTS</span></span>

### <span data-ttu-id="6e2d8-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="6e2d8-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="6e2d8-142">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span><span class="sxs-lookup"><span data-stu-id="6e2d8-142">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span></span>

## <span data-ttu-id="6e2d8-143">Saídas</span><span class="sxs-lookup"><span data-stu-id="6e2d8-143">OUTPUTS</span></span>

### <span data-ttu-id="6e2d8-144">System.IO.FileInfo</span><span class="sxs-lookup"><span data-stu-id="6e2d8-144">System.IO.FileInfo</span></span>

## <span data-ttu-id="6e2d8-145">Notas</span><span class="sxs-lookup"><span data-stu-id="6e2d8-145">NOTES</span></span>

## <span data-ttu-id="6e2d8-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6e2d8-146">RELATED LINKS</span></span>
