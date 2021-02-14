---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsenotebook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseNotebook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseNotebook.md
ms.openlocfilehash: 23bd6186f31199ab9387df5ee78ce3fdbe89032e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115611"
---
# <span data-ttu-id="89da6-101">Remove-AzSynapseNotebook</span><span class="sxs-lookup"><span data-stu-id="89da6-101">Remove-AzSynapseNotebook</span></span>

## <span data-ttu-id="89da6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="89da6-102">SYNOPSIS</span></span>
<span data-ttu-id="89da6-103">Remove um bloco de anotações de um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="89da6-103">Removes a notebook from a workspace.</span></span>

## <span data-ttu-id="89da6-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="89da6-104">SYNTAX</span></span>

### <span data-ttu-id="89da6-105">RemoveByName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="89da6-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseNotebook -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89da6-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="89da6-106">RemoveByObject</span></span>
```
Remove-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89da6-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="89da6-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseNotebook -InputObject <PSNotebookResource> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89da6-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="89da6-108">DESCRIPTION</span></span>
<span data-ttu-id="89da6-109">O **cmdlet Remove-AzSynapseNotebook** remove um bloco de anotações de um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="89da6-109">The **Remove-AzSynapseNotebook** cmdlet removes a notebook from a workspace.</span></span>

## <span data-ttu-id="89da6-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="89da6-110">EXAMPLES</span></span>

### <span data-ttu-id="89da6-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="89da6-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook
```

<span data-ttu-id="89da6-112">Remova um bloco de anotações chamado ContosoNotebook do espaço de trabalho ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="89da6-112">Remove a notebook called ContosoNotebook from the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="89da6-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="89da6-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseNotebook -Name ContosoNotebook
```

<span data-ttu-id="89da6-114">Remova um bloco de anotações chamado ContosoNotebook do espaço de trabalho ContosoWorkspace por meio de pipeline.</span><span class="sxs-lookup"><span data-stu-id="89da6-114">Remove a notebook called ContosoNotebook from the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="89da6-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="89da6-115">Example 3</span></span>
```powershell
PS C:\> $notebook = Get-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook
PS C:\> $notebook | Remove-AzSynapseNotebook
```

<span data-ttu-id="89da6-116">Remova um bloco de anotações chamado ContosoNotebook do espaço de trabalho ContosoWorkspace por meio de pipeline.</span><span class="sxs-lookup"><span data-stu-id="89da6-116">Remove a notebook called ContosoNotebook from the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="89da6-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="89da6-117">PARAMETERS</span></span>

### <span data-ttu-id="89da6-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="89da6-118">-AsJob</span></span>
<span data-ttu-id="89da6-119">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="89da6-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="89da6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89da6-120">-DefaultProfile</span></span>
<span data-ttu-id="89da6-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="89da6-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89da6-122">-Forçar</span><span class="sxs-lookup"><span data-stu-id="89da6-122">-Force</span></span>
<span data-ttu-id="89da6-123">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="89da6-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="89da6-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="89da6-124">-InputObject</span></span>
<span data-ttu-id="89da6-125">O objeto do bloco de anotações.</span><span class="sxs-lookup"><span data-stu-id="89da6-125">The notebook object.</span></span>

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

### <span data-ttu-id="89da6-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="89da6-126">-Name</span></span>
<span data-ttu-id="89da6-127">O nome do bloco de anotações.</span><span class="sxs-lookup"><span data-stu-id="89da6-127">The notebook name.</span></span>

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

### <span data-ttu-id="89da6-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="89da6-128">-PassThru</span></span>
<span data-ttu-id="89da6-129">Este Cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="89da6-129">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="89da6-130">Se essa opção for especificada, ela retornará verdadeira se for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="89da6-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="89da6-131">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="89da6-131">-WorkspaceName</span></span>
<span data-ttu-id="89da6-132">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="89da6-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="89da6-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="89da6-133">-WorkspaceObject</span></span>
<span data-ttu-id="89da6-134">objeto de entrada de espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="89da6-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="89da6-135">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="89da6-135">-Confirm</span></span>
<span data-ttu-id="89da6-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89da6-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89da6-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89da6-137">-WhatIf</span></span>
<span data-ttu-id="89da6-138">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="89da6-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="89da6-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="89da6-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89da6-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89da6-140">CommonParameters</span></span>
<span data-ttu-id="89da6-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89da6-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89da6-142">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="89da6-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89da6-143">Entradas</span><span class="sxs-lookup"><span data-stu-id="89da6-143">INPUTS</span></span>

### <span data-ttu-id="89da6-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="89da6-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="89da6-145">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span><span class="sxs-lookup"><span data-stu-id="89da6-145">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span></span>

## <span data-ttu-id="89da6-146">Saídas</span><span class="sxs-lookup"><span data-stu-id="89da6-146">OUTPUTS</span></span>

### <span data-ttu-id="89da6-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="89da6-147">System.Boolean</span></span>

## <span data-ttu-id="89da6-148">Notas</span><span class="sxs-lookup"><span data-stu-id="89da6-148">NOTES</span></span>

## <span data-ttu-id="89da6-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="89da6-149">RELATED LINKS</span></span>
