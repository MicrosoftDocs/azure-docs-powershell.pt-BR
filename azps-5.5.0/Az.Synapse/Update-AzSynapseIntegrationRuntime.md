---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapseintegrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseIntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseIntegrationRuntime.md
ms.openlocfilehash: 31647da87319ca6be90962f34d128f5e2c922d47
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114355"
---
# <span data-ttu-id="2e1ee-101">Update-AzSynapseIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="2e1ee-101">Update-AzSynapseIntegrationRuntime</span></span>

## <span data-ttu-id="2e1ee-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2e1ee-102">SYNOPSIS</span></span>
<span data-ttu-id="2e1ee-103">Atualiza um tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="2e1ee-103">Updates an integration runtime.</span></span>

## <span data-ttu-id="2e1ee-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2e1ee-104">SYNTAX</span></span>

### <span data-ttu-id="2e1ee-105">UpdateByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="2e1ee-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseIntegrationRuntime [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e1ee-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2e1ee-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntime -IntegrationRuntimeName <String> -WorkspaceObject <PSSynapseWorkspace>
 [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e1ee-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2e1ee-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntime -ResourceId <String> [-AutoUpdate <String>]
 [-AutoUpdateDelayOffset <TimeSpan>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2e1ee-108">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2e1ee-108">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntime -InputObject <PSIntegrationRuntime> [-AutoUpdate <String>]
 [-AutoUpdateDelayOffset <TimeSpan>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2e1ee-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="2e1ee-109">DESCRIPTION</span></span>
<span data-ttu-id="2e1ee-110">O **cmdlet Update-AzSynapseIntegrationRuntime** atualiza as propriedades de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="2e1ee-110">The **Update-AzSynapseIntegrationRuntime** cmdlet updates integration runtime properties.</span></span> <span data-ttu-id="2e1ee-111">Atualmente, o cmdlet só dá suporte à atualização de 'AutoUpdate' e 'AutoUpdateDelayOffset' para tempo de execução de integração auto-hospedado.</span><span class="sxs-lookup"><span data-stu-id="2e1ee-111">Currently the cmdlet only supports updating 'AutoUpdate' and 'AutoUpdateDelayOffset' for self-hosted integration runtime.</span></span>

## <span data-ttu-id="2e1ee-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2e1ee-112">EXAMPLES</span></span>

### <span data-ttu-id="2e1ee-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2e1ee-113">Example 1</span></span>
```powershell
PS C:\> $ts = New-TimeSpan -Hours 3
PS C:\> Update-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' -AutoUpdate Off -AutoUpdateDelayOffset $ts
```

<span data-ttu-id="2e1ee-114">O cmdlet atualiza o tempo de execução de integração hospedado auto-hospedado chamado "test-selfhost-ir".</span><span class="sxs-lookup"><span data-stu-id="2e1ee-114">The cmdlet updates self-hosted integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="2e1ee-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2e1ee-115">PARAMETERS</span></span>

### <span data-ttu-id="2e1ee-116">-AutoUpdate</span><span class="sxs-lookup"><span data-stu-id="2e1ee-116">-AutoUpdate</span></span>
<span data-ttu-id="2e1ee-117">Habilitar ou desabilitar a atualização automática de tempo de execução de integração hospedada.</span><span class="sxs-lookup"><span data-stu-id="2e1ee-117">Enable or disable the self-hosted integration runtime auto-update.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: On, Off

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e1ee-118">-AutoUpdateDelayOffset</span><span class="sxs-lookup"><span data-stu-id="2e1ee-118">-AutoUpdateDelayOffset</span></span>
<span data-ttu-id="2e1ee-119">A hora do dia para a atualização automática de tempo de execução de integração hospedada.</span><span class="sxs-lookup"><span data-stu-id="2e1ee-119">The time of the day for the self-hosted integration runtime auto-update.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e1ee-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e1ee-120">-DefaultProfile</span></span>
<span data-ttu-id="2e1ee-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2e1ee-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e1ee-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2e1ee-122">-InputObject</span></span>
<span data-ttu-id="2e1ee-123">O objeto de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="2e1ee-123">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2e1ee-124">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="2e1ee-124">-IntegrationRuntimeName</span></span>
<span data-ttu-id="2e1ee-125">O nome de tempo de execução da integração.</span><span class="sxs-lookup"><span data-stu-id="2e1ee-125">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e1ee-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e1ee-126">-ResourceGroupName</span></span>
<span data-ttu-id="2e1ee-127">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2e1ee-127">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e1ee-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2e1ee-128">-ResourceId</span></span>
<span data-ttu-id="2e1ee-129">Identificador de recursos do tempo de execução de integração synapse.</span><span class="sxs-lookup"><span data-stu-id="2e1ee-129">Resource identifier of Synapse integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e1ee-130">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="2e1ee-130">-WorkspaceName</span></span>
<span data-ttu-id="2e1ee-131">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="2e1ee-131">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e1ee-132">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="2e1ee-132">-WorkspaceObject</span></span>
<span data-ttu-id="2e1ee-133">objeto de entrada de espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="2e1ee-133">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2e1ee-134">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="2e1ee-134">-Confirm</span></span>
<span data-ttu-id="2e1ee-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e1ee-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e1ee-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e1ee-136">-WhatIf</span></span>
<span data-ttu-id="2e1ee-137">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="2e1ee-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e1ee-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2e1ee-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e1ee-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e1ee-139">CommonParameters</span></span>
<span data-ttu-id="2e1ee-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e1ee-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e1ee-141">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2e1ee-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e1ee-142">Entradas</span><span class="sxs-lookup"><span data-stu-id="2e1ee-142">INPUTS</span></span>

### <span data-ttu-id="2e1ee-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="2e1ee-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="2e1ee-144">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="2e1ee-144">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="2e1ee-145">Saídas</span><span class="sxs-lookup"><span data-stu-id="2e1ee-145">OUTPUTS</span></span>

### <span data-ttu-id="2e1ee-146">Microsoft.Azure.Commands.Synapse.Models.PSHostedIntegrationRuntimeStatus</span><span class="sxs-lookup"><span data-stu-id="2e1ee-146">Microsoft.Azure.Commands.Synapse.Models.PSSelfHostedIntegrationRuntimeStatus</span></span>

## <span data-ttu-id="2e1ee-147">Notas</span><span class="sxs-lookup"><span data-stu-id="2e1ee-147">NOTES</span></span>

## <span data-ttu-id="2e1ee-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2e1ee-148">RELATED LINKS</span></span>
