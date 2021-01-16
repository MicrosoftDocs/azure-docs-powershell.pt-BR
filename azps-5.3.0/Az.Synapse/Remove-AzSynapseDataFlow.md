---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsedataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseDataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseDataFlow.md
ms.openlocfilehash: 2d0bec0c86f51771e971ca2c6b5a22c32f8ee687
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98429634"
---
# <span data-ttu-id="92b1c-101">Remove-AzSynapseDataFlow</span><span class="sxs-lookup"><span data-stu-id="92b1c-101">Remove-AzSynapseDataFlow</span></span>

## <span data-ttu-id="92b1c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="92b1c-102">SYNOPSIS</span></span>
<span data-ttu-id="92b1c-103">Remove um fluxo de dados do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="92b1c-103">Removes a data flow from workspace.</span></span>

## <span data-ttu-id="92b1c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="92b1c-104">SYNTAX</span></span>

### <span data-ttu-id="92b1c-105">RemoveByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="92b1c-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseDataFlow -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92b1c-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="92b1c-106">RemoveByObject</span></span>
```
Remove-AzSynapseDataFlow -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92b1c-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="92b1c-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseDataFlow -InputObject <PSDataFlowResource> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92b1c-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="92b1c-108">DESCRIPTION</span></span>
<span data-ttu-id="92b1c-109">O cmdlet **Remove-AzSynapseDataFlow** remove um fluxo de dados do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="92b1c-109">The **Remove-AzSynapseDataFlow** cmdlet removes a data flow from workspace.</span></span>

## <span data-ttu-id="92b1c-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="92b1c-110">EXAMPLES</span></span>

### <span data-ttu-id="92b1c-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="92b1c-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseDataFlow -WorkspaceName ContosoWorkspace -Name ContosoDataFlow
```

<span data-ttu-id="92b1c-112">Esse comando Remove o fluxo de dados denominado ContosoDataFlow do espaço de trabalho chamado ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="92b1c-112">This command removes the data flow named ContosoDataFlow from the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="92b1c-113">OS</span><span class="sxs-lookup"><span data-stu-id="92b1c-113">PARAMETERS</span></span>

### <span data-ttu-id="92b1c-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="92b1c-114">-AsJob</span></span>
<span data-ttu-id="92b1c-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="92b1c-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="92b1c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92b1c-116">-DefaultProfile</span></span>
<span data-ttu-id="92b1c-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="92b1c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92b1c-118">-Force</span><span class="sxs-lookup"><span data-stu-id="92b1c-118">-Force</span></span>
<span data-ttu-id="92b1c-119">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="92b1c-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="92b1c-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="92b1c-120">-InputObject</span></span>
<span data-ttu-id="92b1c-121">O objeto de fluxo de dados.</span><span class="sxs-lookup"><span data-stu-id="92b1c-121">The data flow object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="92b1c-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="92b1c-122">-Name</span></span>
<span data-ttu-id="92b1c-123">O nome do fluxo de dados.</span><span class="sxs-lookup"><span data-stu-id="92b1c-123">The data flow name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName, RemoveByObject
Aliases: DataFlowName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92b1c-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="92b1c-124">-PassThru</span></span>
<span data-ttu-id="92b1c-125">Esse cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="92b1c-125">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="92b1c-126">Se essa opção for especificada, retornará true se for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="92b1c-126">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="92b1c-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="92b1c-127">-WorkspaceName</span></span>
<span data-ttu-id="92b1c-128">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="92b1c-128">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="92b1c-129">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="92b1c-129">-WorkspaceObject</span></span>
<span data-ttu-id="92b1c-130">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="92b1c-130">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="92b1c-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="92b1c-131">-Confirm</span></span>
<span data-ttu-id="92b1c-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92b1c-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92b1c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92b1c-133">-WhatIf</span></span>
<span data-ttu-id="92b1c-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="92b1c-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92b1c-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="92b1c-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92b1c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92b1c-136">CommonParameters</span></span>
<span data-ttu-id="92b1c-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92b1c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92b1c-138">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="92b1c-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92b1c-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="92b1c-139">INPUTS</span></span>

### <span data-ttu-id="92b1c-140">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="92b1c-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="92b1c-141">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span><span class="sxs-lookup"><span data-stu-id="92b1c-141">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span></span>

## <span data-ttu-id="92b1c-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="92b1c-142">OUTPUTS</span></span>

### <span data-ttu-id="92b1c-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="92b1c-143">System.Boolean</span></span>

## <span data-ttu-id="92b1c-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="92b1c-144">NOTES</span></span>

## <span data-ttu-id="92b1c-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="92b1c-145">RELATED LINKS</span></span>
