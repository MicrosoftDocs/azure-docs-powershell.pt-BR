---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsenotebook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseNotebook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseNotebook.md
ms.openlocfilehash: 23bd6186f31199ab9387df5ee78ce3fdbe89032e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98263342"
---
# <span data-ttu-id="bce2b-101">Remove-AzSynapseNotebook</span><span class="sxs-lookup"><span data-stu-id="bce2b-101">Remove-AzSynapseNotebook</span></span>

## <span data-ttu-id="bce2b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bce2b-102">SYNOPSIS</span></span>
<span data-ttu-id="bce2b-103">Remove um bloco de anotações de um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="bce2b-103">Removes a notebook from a workspace.</span></span>

## <span data-ttu-id="bce2b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bce2b-104">SYNTAX</span></span>

### <span data-ttu-id="bce2b-105">RemoveByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="bce2b-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseNotebook -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bce2b-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="bce2b-106">RemoveByObject</span></span>
```
Remove-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bce2b-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="bce2b-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseNotebook -InputObject <PSNotebookResource> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bce2b-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bce2b-108">DESCRIPTION</span></span>
<span data-ttu-id="bce2b-109">O cmdlet **Remove-AzSynapseNotebook** remove um bloco de anotações de um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="bce2b-109">The **Remove-AzSynapseNotebook** cmdlet removes a notebook from a workspace.</span></span>

## <span data-ttu-id="bce2b-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bce2b-110">EXAMPLES</span></span>

### <span data-ttu-id="bce2b-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bce2b-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook
```

<span data-ttu-id="bce2b-112">Remova um bloco de anotações chamado ContosoNotebook da ContosoWorkspace do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="bce2b-112">Remove a notebook called ContosoNotebook from the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="bce2b-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="bce2b-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseNotebook -Name ContosoNotebook
```

<span data-ttu-id="bce2b-114">Remova um bloco de anotações chamado ContosoNotebook do espaço de trabalho ContosoWorkspace pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="bce2b-114">Remove a notebook called ContosoNotebook from the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="bce2b-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="bce2b-115">Example 3</span></span>
```powershell
PS C:\> $notebook = Get-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook
PS C:\> $notebook | Remove-AzSynapseNotebook
```

<span data-ttu-id="bce2b-116">Remova um bloco de anotações chamado ContosoNotebook do espaço de trabalho ContosoWorkspace pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="bce2b-116">Remove a notebook called ContosoNotebook from the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="bce2b-117">OS</span><span class="sxs-lookup"><span data-stu-id="bce2b-117">PARAMETERS</span></span>

### <span data-ttu-id="bce2b-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bce2b-118">-AsJob</span></span>
<span data-ttu-id="bce2b-119">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="bce2b-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bce2b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bce2b-120">-DefaultProfile</span></span>
<span data-ttu-id="bce2b-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bce2b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bce2b-122">-Force</span><span class="sxs-lookup"><span data-stu-id="bce2b-122">-Force</span></span>
<span data-ttu-id="bce2b-123">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="bce2b-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="bce2b-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bce2b-124">-InputObject</span></span>
<span data-ttu-id="bce2b-125">O objeto notebook.</span><span class="sxs-lookup"><span data-stu-id="bce2b-125">The notebook object.</span></span>

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

### <span data-ttu-id="bce2b-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="bce2b-126">-Name</span></span>
<span data-ttu-id="bce2b-127">O nome do bloco de anotações.</span><span class="sxs-lookup"><span data-stu-id="bce2b-127">The notebook name.</span></span>

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

### <span data-ttu-id="bce2b-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bce2b-128">-PassThru</span></span>
<span data-ttu-id="bce2b-129">Esse cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="bce2b-129">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="bce2b-130">Se essa opção for especificada, retornará true se for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="bce2b-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="bce2b-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="bce2b-131">-WorkspaceName</span></span>
<span data-ttu-id="bce2b-132">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="bce2b-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="bce2b-133">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="bce2b-133">-WorkspaceObject</span></span>
<span data-ttu-id="bce2b-134">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="bce2b-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="bce2b-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="bce2b-135">-Confirm</span></span>
<span data-ttu-id="bce2b-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bce2b-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bce2b-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bce2b-137">-WhatIf</span></span>
<span data-ttu-id="bce2b-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bce2b-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bce2b-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bce2b-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bce2b-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bce2b-140">CommonParameters</span></span>
<span data-ttu-id="bce2b-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bce2b-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bce2b-142">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bce2b-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bce2b-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bce2b-143">INPUTS</span></span>

### <span data-ttu-id="bce2b-144">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="bce2b-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="bce2b-145">Microsoft. Azure. Commands. Synapse. Models. PSNotebookResource</span><span class="sxs-lookup"><span data-stu-id="bce2b-145">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span></span>

## <span data-ttu-id="bce2b-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bce2b-146">OUTPUTS</span></span>

### <span data-ttu-id="bce2b-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bce2b-147">System.Boolean</span></span>

## <span data-ttu-id="bce2b-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bce2b-148">NOTES</span></span>

## <span data-ttu-id="bce2b-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bce2b-149">RELATED LINKS</span></span>
