---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsenotebook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseNotebook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseNotebook.md
ms.openlocfilehash: 22570fa8d236675a8ad2acd712e1ff66c1bc5049
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94117928"
---
# <span data-ttu-id="2c515-101">Remove-AzSynapseNotebook</span><span class="sxs-lookup"><span data-stu-id="2c515-101">Remove-AzSynapseNotebook</span></span>

## <span data-ttu-id="2c515-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2c515-102">SYNOPSIS</span></span>
<span data-ttu-id="2c515-103">Remove um bloco de anotações de um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="2c515-103">Removes a notebook from a workspace.</span></span>

## <span data-ttu-id="2c515-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2c515-104">SYNTAX</span></span>

### <span data-ttu-id="2c515-105">RemoveByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="2c515-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseNotebook -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c515-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="2c515-106">RemoveByObject</span></span>
```
Remove-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c515-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="2c515-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseNotebook -InputObject <PSNotebookResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c515-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2c515-108">DESCRIPTION</span></span>
<span data-ttu-id="2c515-109">O cmdlet **Remove-AzSynapseNotebook** remove um bloco de anotações de um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="2c515-109">The **Remove-AzSynapseNotebook** cmdlet removes a notebook from a workspace.</span></span>

## <span data-ttu-id="2c515-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2c515-110">EXAMPLES</span></span>

### <span data-ttu-id="2c515-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2c515-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook
```

<span data-ttu-id="2c515-112">Remova um bloco de anotações chamado ContosoNotebook da ContosoWorkspace do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="2c515-112">Remove a notebook called ContosoNotebook from the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="2c515-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="2c515-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseNotebook -Name ContosoNotebook
```

<span data-ttu-id="2c515-114">Remova um bloco de anotações chamado ContosoNotebook do espaço de trabalho ContosoWorkspace pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="2c515-114">Remove a notebook called ContosoNotebook from the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="2c515-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="2c515-115">Example 3</span></span>
```powershell
PS C:\> $notebook = Get-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook
PS C:\> $notebook | Remove-AzSynapseNotebook
```

<span data-ttu-id="2c515-116">Remova um bloco de anotações chamado ContosoNotebook do espaço de trabalho ContosoWorkspace pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="2c515-116">Remove a notebook called ContosoNotebook from the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="2c515-117">OS</span><span class="sxs-lookup"><span data-stu-id="2c515-117">PARAMETERS</span></span>

### <span data-ttu-id="2c515-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2c515-118">-AsJob</span></span>
<span data-ttu-id="2c515-119">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="2c515-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2c515-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c515-120">-DefaultProfile</span></span>
<span data-ttu-id="2c515-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2c515-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c515-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2c515-122">-InputObject</span></span>
<span data-ttu-id="2c515-123">O objeto notebook.</span><span class="sxs-lookup"><span data-stu-id="2c515-123">The notebook object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2c515-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="2c515-124">-Name</span></span>
<span data-ttu-id="2c515-125">O nome do bloco de anotações.</span><span class="sxs-lookup"><span data-stu-id="2c515-125">The notebook name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName, RemoveByObject
Aliases: NotebookName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c515-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2c515-126">-PassThru</span></span>
<span data-ttu-id="2c515-127">Esse cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="2c515-127">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="2c515-128">Se essa opção for especificada, retornará true se for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="2c515-128">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="2c515-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="2c515-129">-WorkspaceName</span></span>
<span data-ttu-id="2c515-130">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="2c515-130">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c515-131">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="2c515-131">-WorkspaceObject</span></span>
<span data-ttu-id="2c515-132">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="2c515-132">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RemoveByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2c515-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2c515-133">-Confirm</span></span>
<span data-ttu-id="2c515-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c515-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c515-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c515-135">-WhatIf</span></span>
<span data-ttu-id="2c515-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2c515-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2c515-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2c515-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c515-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c515-138">CommonParameters</span></span>
<span data-ttu-id="2c515-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c515-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c515-140">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2c515-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c515-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2c515-141">INPUTS</span></span>

### <span data-ttu-id="2c515-142">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="2c515-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="2c515-143">Microsoft. Azure. Commands. Synapse. Models. PSNotebookResource</span><span class="sxs-lookup"><span data-stu-id="2c515-143">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span></span>

## <span data-ttu-id="2c515-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2c515-144">OUTPUTS</span></span>

### <span data-ttu-id="2c515-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2c515-145">System.Boolean</span></span>

## <span data-ttu-id="2c515-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2c515-146">NOTES</span></span>

## <span data-ttu-id="2c515-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2c515-147">RELATED LINKS</span></span>
