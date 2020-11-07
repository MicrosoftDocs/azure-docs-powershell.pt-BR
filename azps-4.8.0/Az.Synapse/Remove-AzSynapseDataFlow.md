---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsedataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseDataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseDataFlow.md
ms.openlocfilehash: dcfcd391d1103b0755a3ffae481e4f1bd5fde2c7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93955859"
---
# <span data-ttu-id="bd053-101">Remove-AzSynapseDataFlow</span><span class="sxs-lookup"><span data-stu-id="bd053-101">Remove-AzSynapseDataFlow</span></span>

## <span data-ttu-id="bd053-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bd053-102">SYNOPSIS</span></span>
<span data-ttu-id="bd053-103">Remove um fluxo de dados do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="bd053-103">Removes a data flow from workspace.</span></span>

## <span data-ttu-id="bd053-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bd053-104">SYNTAX</span></span>

### <span data-ttu-id="bd053-105">RemoveByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="bd053-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseDataFlow -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd053-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="bd053-106">RemoveByObject</span></span>
```
Remove-AzSynapseDataFlow -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd053-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="bd053-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseDataFlow -InputObject <PSDataFlowResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd053-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bd053-108">DESCRIPTION</span></span>
<span data-ttu-id="bd053-109">O cmdlet **Remove-AzSynapseDataFlow** remove um fluxo de dados do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="bd053-109">The **Remove-AzSynapseDataFlow** cmdlet removes a data flow from workspace.</span></span>

## <span data-ttu-id="bd053-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bd053-110">EXAMPLES</span></span>

### <span data-ttu-id="bd053-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bd053-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseDataFlow -WorkspaceName ContosoWorkspace -Name ContosoDataFlow
```

<span data-ttu-id="bd053-112">Esse comando Remove o fluxo de dados denominado ContosoDataFlow do espaço de trabalho chamado ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="bd053-112">This command removes the data flow named ContosoDataFlow from the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="bd053-113">OS</span><span class="sxs-lookup"><span data-stu-id="bd053-113">PARAMETERS</span></span>

### <span data-ttu-id="bd053-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bd053-114">-AsJob</span></span>
<span data-ttu-id="bd053-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="bd053-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bd053-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd053-116">-DefaultProfile</span></span>
<span data-ttu-id="bd053-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bd053-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd053-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bd053-118">-InputObject</span></span>
<span data-ttu-id="bd053-119">O objeto de fluxo de dados.</span><span class="sxs-lookup"><span data-stu-id="bd053-119">The data flow object.</span></span>

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

### <span data-ttu-id="bd053-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="bd053-120">-Name</span></span>
<span data-ttu-id="bd053-121">O nome do fluxo de dados.</span><span class="sxs-lookup"><span data-stu-id="bd053-121">The data flow name.</span></span>

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

### <span data-ttu-id="bd053-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bd053-122">-PassThru</span></span>
<span data-ttu-id="bd053-123">Esse cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="bd053-123">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="bd053-124">Se essa opção for especificada, retornará true se for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="bd053-124">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="bd053-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="bd053-125">-WorkspaceName</span></span>
<span data-ttu-id="bd053-126">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="bd053-126">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="bd053-127">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="bd053-127">-WorkspaceObject</span></span>
<span data-ttu-id="bd053-128">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="bd053-128">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="bd053-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="bd053-129">-Confirm</span></span>
<span data-ttu-id="bd053-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd053-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd053-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd053-131">-WhatIf</span></span>
<span data-ttu-id="bd053-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bd053-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd053-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bd053-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd053-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd053-134">CommonParameters</span></span>
<span data-ttu-id="bd053-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd053-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd053-136">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bd053-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd053-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bd053-137">INPUTS</span></span>

### <span data-ttu-id="bd053-138">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="bd053-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="bd053-139">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span><span class="sxs-lookup"><span data-stu-id="bd053-139">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span></span>

## <span data-ttu-id="bd053-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bd053-140">OUTPUTS</span></span>

### <span data-ttu-id="bd053-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bd053-141">System.Boolean</span></span>

## <span data-ttu-id="bd053-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bd053-142">NOTES</span></span>

## <span data-ttu-id="bd053-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bd053-143">RELATED LINKS</span></span>
