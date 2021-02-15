---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsetriggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseTriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseTriggerSubscription.md
ms.openlocfilehash: ac0606b73145a0d72a5776ede00a24bb802642e7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114362"
---
# <span data-ttu-id="852d1-101">Remove-AzSynapseTriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="852d1-101">Remove-AzSynapseTriggerSubscription</span></span>

## <span data-ttu-id="852d1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="852d1-102">SYNOPSIS</span></span>
<span data-ttu-id="852d1-103">Cancelar a assinatura do gatilho do evento para eventos de serviço externo.</span><span class="sxs-lookup"><span data-stu-id="852d1-103">Unsubscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="852d1-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="852d1-104">SYNTAX</span></span>

### <span data-ttu-id="852d1-105">RemoveByName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="852d1-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseTriggerSubscription -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="852d1-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="852d1-106">RemoveByObject</span></span>
```
Remove-AzSynapseTriggerSubscription -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="852d1-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="852d1-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseTriggerSubscription -InputObject <PSTriggerResource> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="852d1-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="852d1-108">DESCRIPTION</span></span>
<span data-ttu-id="852d1-109">O **cmdlet Remove-AzSynapseTriscriptionSubscription** cancela a assinatura do gatilho do evento para os eventos de serviço externo especificados a partir da definição do gatilho.</span><span class="sxs-lookup"><span data-stu-id="852d1-109">The **Remove-AzSynapseTriggerSubscription** cmdlet unsubscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="852d1-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="852d1-110">EXAMPLES</span></span>

### <span data-ttu-id="852d1-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="852d1-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseTriggerSubscription -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="852d1-112">Esse comando cancelará o gatilho de assinatura chamado ContosoTrifique para os eventos especificados a partir da definição do gatilho.</span><span class="sxs-lookup"><span data-stu-id="852d1-112">This command will unsubscribe trigger called ContosoTrigger to the specified events from the trigger defintion.</span></span>

### <span data-ttu-id="852d1-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="852d1-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseTriggerSubscription -Name ContosoTrigger
```

<span data-ttu-id="852d1-114">Esse comando cancelará o gatilho de assinatura chamado ContosoTri pipeline para os eventos especificados a partir da definição do gatilho através do pipeline.</span><span class="sxs-lookup"><span data-stu-id="852d1-114">This command will unsubscribe trigger called ContosoTrigger to the specified events from the trigger defintion through pipeline.</span></span>

### <span data-ttu-id="852d1-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="852d1-115">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Remove-AzSynapseTriggerSubscription
```

<span data-ttu-id="852d1-116">Esse comando cancelará o gatilho de assinatura chamado ContosoTri pipeline para os eventos especificados a partir da definição do gatilho através do pipeline.</span><span class="sxs-lookup"><span data-stu-id="852d1-116">This command will unsubscribe trigger called ContosoTrigger to the specified events from the trigger defintion through pipeline.</span></span>

## <span data-ttu-id="852d1-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="852d1-117">PARAMETERS</span></span>

### <span data-ttu-id="852d1-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="852d1-118">-AsJob</span></span>
<span data-ttu-id="852d1-119">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="852d1-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="852d1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="852d1-120">-DefaultProfile</span></span>
<span data-ttu-id="852d1-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="852d1-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="852d1-122">-Forçar</span><span class="sxs-lookup"><span data-stu-id="852d1-122">-Force</span></span>
<span data-ttu-id="852d1-123">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="852d1-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="852d1-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="852d1-124">-InputObject</span></span>
<span data-ttu-id="852d1-125">O objeto de gatilho.</span><span class="sxs-lookup"><span data-stu-id="852d1-125">The trigger object.</span></span>

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

### <span data-ttu-id="852d1-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="852d1-126">-Name</span></span>
<span data-ttu-id="852d1-127">O nome do gatilho.</span><span class="sxs-lookup"><span data-stu-id="852d1-127">The trigger name.</span></span>

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

### <span data-ttu-id="852d1-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="852d1-128">-PassThru</span></span>
<span data-ttu-id="852d1-129">Este Cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="852d1-129">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="852d1-130">Se essa opção for especificada, ela retornará verdadeira se for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="852d1-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="852d1-131">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="852d1-131">-WorkspaceName</span></span>
<span data-ttu-id="852d1-132">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="852d1-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="852d1-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="852d1-133">-WorkspaceObject</span></span>
<span data-ttu-id="852d1-134">objeto de entrada de espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="852d1-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="852d1-135">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="852d1-135">-Confirm</span></span>
<span data-ttu-id="852d1-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="852d1-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="852d1-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="852d1-137">-WhatIf</span></span>
<span data-ttu-id="852d1-138">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="852d1-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="852d1-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="852d1-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="852d1-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="852d1-140">CommonParameters</span></span>
<span data-ttu-id="852d1-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="852d1-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="852d1-142">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="852d1-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="852d1-143">Entradas</span><span class="sxs-lookup"><span data-stu-id="852d1-143">INPUTS</span></span>

### <span data-ttu-id="852d1-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="852d1-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="852d1-145">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="852d1-145">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="852d1-146">Saídas</span><span class="sxs-lookup"><span data-stu-id="852d1-146">OUTPUTS</span></span>

### <span data-ttu-id="852d1-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="852d1-147">System.Boolean</span></span>

## <span data-ttu-id="852d1-148">Notas</span><span class="sxs-lookup"><span data-stu-id="852d1-148">NOTES</span></span>

## <span data-ttu-id="852d1-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="852d1-149">RELATED LINKS</span></span>
