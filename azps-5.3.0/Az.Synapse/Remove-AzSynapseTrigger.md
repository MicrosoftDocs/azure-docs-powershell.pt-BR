---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseTrigger.md
ms.openlocfilehash: 648d215066fb7bd827d43ec9d063a7994ada82f8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98272339"
---
# <span data-ttu-id="79a0e-101">Remove-AzSynapseTrigger</span><span class="sxs-lookup"><span data-stu-id="79a0e-101">Remove-AzSynapseTrigger</span></span>

## <span data-ttu-id="79a0e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="79a0e-102">SYNOPSIS</span></span>
<span data-ttu-id="79a0e-103">Remove um gatilho de um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="79a0e-103">Removes a trigger from a workspace.</span></span>

## <span data-ttu-id="79a0e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="79a0e-104">SYNTAX</span></span>

### <span data-ttu-id="79a0e-105">RemoveByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="79a0e-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseTrigger -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79a0e-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="79a0e-106">RemoveByObject</span></span>
```
Remove-AzSynapseTrigger -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79a0e-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="79a0e-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseTrigger -InputObject <PSTriggerResource> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79a0e-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="79a0e-108">DESCRIPTION</span></span>
<span data-ttu-id="79a0e-109">O cmdlet **Remove-AzSynapseTrigger** remove um gatilho de um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="79a0e-109">The **Remove-AzSynapseTrigger** cmdlet removes a trigger from a workspace.</span></span>

## <span data-ttu-id="79a0e-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="79a0e-110">EXAMPLES</span></span>

### <span data-ttu-id="79a0e-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="79a0e-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="79a0e-112">Remova um gatilho chamado ContosoTrigger da ContosoWorkspace do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="79a0e-112">Remove a trigger called ContosoTrigger from the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="79a0e-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="79a0e-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseTrigger -Name ContosoTrigger
```

<span data-ttu-id="79a0e-114">Remova um gatilho chamado ContosoTrigger do espaço de trabalho ContosoWorkspace pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="79a0e-114">Remove a trigger called ContosoTrigger from the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="79a0e-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="79a0e-115">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Remove-AzSynapseTrigger
```

<span data-ttu-id="79a0e-116">Remova um gatilho chamado ContosoTrigger do espaço de trabalho ContosoWorkspace pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="79a0e-116">Remove a trigger called ContosoTrigger from the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="79a0e-117">OS</span><span class="sxs-lookup"><span data-stu-id="79a0e-117">PARAMETERS</span></span>

### <span data-ttu-id="79a0e-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="79a0e-118">-AsJob</span></span>
<span data-ttu-id="79a0e-119">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="79a0e-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="79a0e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79a0e-120">-DefaultProfile</span></span>
<span data-ttu-id="79a0e-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="79a0e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79a0e-122">-Force</span><span class="sxs-lookup"><span data-stu-id="79a0e-122">-Force</span></span>
<span data-ttu-id="79a0e-123">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="79a0e-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="79a0e-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="79a0e-124">-InputObject</span></span>
<span data-ttu-id="79a0e-125">O objeto Trigger.</span><span class="sxs-lookup"><span data-stu-id="79a0e-125">The trigger object.</span></span>

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

### <span data-ttu-id="79a0e-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="79a0e-126">-Name</span></span>
<span data-ttu-id="79a0e-127">O nome do disparador.</span><span class="sxs-lookup"><span data-stu-id="79a0e-127">The trigger name.</span></span>

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

### <span data-ttu-id="79a0e-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="79a0e-128">-PassThru</span></span>
<span data-ttu-id="79a0e-129">Esse cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="79a0e-129">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="79a0e-130">Se essa opção for especificada, retornará true se for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="79a0e-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="79a0e-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="79a0e-131">-WorkspaceName</span></span>
<span data-ttu-id="79a0e-132">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="79a0e-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="79a0e-133">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="79a0e-133">-WorkspaceObject</span></span>
<span data-ttu-id="79a0e-134">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="79a0e-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="79a0e-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="79a0e-135">-Confirm</span></span>
<span data-ttu-id="79a0e-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79a0e-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79a0e-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79a0e-137">-WhatIf</span></span>
<span data-ttu-id="79a0e-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="79a0e-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="79a0e-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="79a0e-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79a0e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79a0e-140">CommonParameters</span></span>
<span data-ttu-id="79a0e-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79a0e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79a0e-142">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="79a0e-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79a0e-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="79a0e-143">INPUTS</span></span>

### <span data-ttu-id="79a0e-144">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="79a0e-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="79a0e-145">Microsoft. Azure. Commands. Synapse. Models. PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="79a0e-145">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="79a0e-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="79a0e-146">OUTPUTS</span></span>

### <span data-ttu-id="79a0e-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="79a0e-147">System.Boolean</span></span>

## <span data-ttu-id="79a0e-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="79a0e-148">NOTES</span></span>

## <span data-ttu-id="79a0e-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="79a0e-149">RELATED LINKS</span></span>
