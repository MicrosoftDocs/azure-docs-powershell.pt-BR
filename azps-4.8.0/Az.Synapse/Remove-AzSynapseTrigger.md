---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseTrigger.md
ms.openlocfilehash: 0882789e230c012fe9f23dcdbeeb5378e9b91781
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94113465"
---
# <span data-ttu-id="5efb9-101">Remove-AzSynapseTrigger</span><span class="sxs-lookup"><span data-stu-id="5efb9-101">Remove-AzSynapseTrigger</span></span>

## <span data-ttu-id="5efb9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5efb9-102">SYNOPSIS</span></span>
<span data-ttu-id="5efb9-103">Remove um gatilho de um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="5efb9-103">Removes a trigger from a workspace.</span></span>

## <span data-ttu-id="5efb9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5efb9-104">SYNTAX</span></span>

### <span data-ttu-id="5efb9-105">RemoveByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="5efb9-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseTrigger -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5efb9-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="5efb9-106">RemoveByObject</span></span>
```
Remove-AzSynapseTrigger -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5efb9-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="5efb9-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseTrigger -InputObject <PSTriggerResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5efb9-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5efb9-108">DESCRIPTION</span></span>
<span data-ttu-id="5efb9-109">O cmdlet **Remove-AzSynapseTrigger** remove um gatilho de um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="5efb9-109">The **Remove-AzSynapseTrigger** cmdlet removes a trigger from a workspace.</span></span>

## <span data-ttu-id="5efb9-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5efb9-110">EXAMPLES</span></span>

### <span data-ttu-id="5efb9-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5efb9-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="5efb9-112">Remova um gatilho chamado ContosoTrigger da ContosoWorkspace do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="5efb9-112">Remove a trigger called ContosoTrigger from the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="5efb9-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="5efb9-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseTrigger -Name ContosoTrigger
```

<span data-ttu-id="5efb9-114">Remova um gatilho chamado ContosoTrigger do espaço de trabalho ContosoWorkspace pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="5efb9-114">Remove a trigger called ContosoTrigger from the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="5efb9-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="5efb9-115">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Remove-AzSynapseTrigger
```

<span data-ttu-id="5efb9-116">Remova um gatilho chamado ContosoTrigger do espaço de trabalho ContosoWorkspace pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="5efb9-116">Remove a trigger called ContosoTrigger from the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="5efb9-117">OS</span><span class="sxs-lookup"><span data-stu-id="5efb9-117">PARAMETERS</span></span>

### <span data-ttu-id="5efb9-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5efb9-118">-AsJob</span></span>
<span data-ttu-id="5efb9-119">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="5efb9-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5efb9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5efb9-120">-DefaultProfile</span></span>
<span data-ttu-id="5efb9-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5efb9-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5efb9-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5efb9-122">-InputObject</span></span>
<span data-ttu-id="5efb9-123">O objeto Trigger.</span><span class="sxs-lookup"><span data-stu-id="5efb9-123">The trigger object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5efb9-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="5efb9-124">-Name</span></span>
<span data-ttu-id="5efb9-125">O nome do disparador.</span><span class="sxs-lookup"><span data-stu-id="5efb9-125">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName, RemoveByObject
Aliases: TriggerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5efb9-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5efb9-126">-PassThru</span></span>
<span data-ttu-id="5efb9-127">Esse cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="5efb9-127">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="5efb9-128">Se essa opção for especificada, retornará true se for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="5efb9-128">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="5efb9-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="5efb9-129">-WorkspaceName</span></span>
<span data-ttu-id="5efb9-130">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="5efb9-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="5efb9-131">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="5efb9-131">-WorkspaceObject</span></span>
<span data-ttu-id="5efb9-132">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="5efb9-132">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="5efb9-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5efb9-133">-Confirm</span></span>
<span data-ttu-id="5efb9-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5efb9-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5efb9-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5efb9-135">-WhatIf</span></span>
<span data-ttu-id="5efb9-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5efb9-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5efb9-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5efb9-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5efb9-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5efb9-138">CommonParameters</span></span>
<span data-ttu-id="5efb9-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5efb9-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5efb9-140">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5efb9-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5efb9-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5efb9-141">INPUTS</span></span>

### <span data-ttu-id="5efb9-142">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="5efb9-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="5efb9-143">Microsoft. Azure. Commands. Synapse. Models. PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="5efb9-143">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="5efb9-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5efb9-144">OUTPUTS</span></span>

### <span data-ttu-id="5efb9-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5efb9-145">System.Boolean</span></span>

## <span data-ttu-id="5efb9-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5efb9-146">NOTES</span></span>

## <span data-ttu-id="5efb9-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5efb9-147">RELATED LINKS</span></span>
