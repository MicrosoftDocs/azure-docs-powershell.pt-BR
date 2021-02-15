---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapseintegrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseIntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseIntegrationRuntime.md
ms.openlocfilehash: 57b6c6619a45e515c7aff2e30edc346ff39af9ac
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118890"
---
# <span data-ttu-id="4716e-101">Remove-AzSynapseIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="4716e-101">Remove-AzSynapseIntegrationRuntime</span></span>

## <span data-ttu-id="4716e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4716e-102">SYNOPSIS</span></span>
<span data-ttu-id="4716e-103">Remove um tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="4716e-103">Removes an integration runtime.</span></span>

## <span data-ttu-id="4716e-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4716e-104">SYNTAX</span></span>

### <span data-ttu-id="4716e-105">RemoveByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="4716e-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseIntegrationRuntime [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4716e-106">RemoveByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4716e-106">RemoveByParentObjectParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntime -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4716e-107">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4716e-107">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntime -ResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4716e-108">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4716e-108">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntime -InputObject <PSIntegrationRuntime> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4716e-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="4716e-109">DESCRIPTION</span></span>
<span data-ttu-id="4716e-110">O **cmdlet Remove-AzSynapseIntegrationRuntime** remove um tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="4716e-110">The **Remove-AzSynapseIntegrationRuntime** cmdlet removes a integration runtime.</span></span>

## <span data-ttu-id="4716e-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4716e-111">EXAMPLES</span></span>

### <span data-ttu-id="4716e-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4716e-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-reserved-ir' -Confirm
```

<span data-ttu-id="4716e-113">Esse comando remove o tempo de execução de integração chamado "test-reserved-ir" do espaço de trabalho chamado ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="4716e-113">This command removes the integration runtime named 'test-reserved-ir' from the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="4716e-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4716e-114">PARAMETERS</span></span>

### <span data-ttu-id="4716e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4716e-115">-DefaultProfile</span></span>
<span data-ttu-id="4716e-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4716e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4716e-117">-Forçar</span><span class="sxs-lookup"><span data-stu-id="4716e-117">-Force</span></span>
<span data-ttu-id="4716e-118">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="4716e-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="4716e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4716e-119">-InputObject</span></span>
<span data-ttu-id="4716e-120">O objeto de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="4716e-120">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4716e-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="4716e-121">-Name</span></span>
<span data-ttu-id="4716e-122">O nome de tempo de execução da integração.</span><span class="sxs-lookup"><span data-stu-id="4716e-122">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet, RemoveByParentObjectParameterSet
Aliases: IntegrationRuntimeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4716e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4716e-123">-ResourceGroupName</span></span>
<span data-ttu-id="4716e-124">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4716e-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4716e-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4716e-125">-ResourceId</span></span>
<span data-ttu-id="4716e-126">Identificador de recursos do tempo de execução de integração synapse.</span><span class="sxs-lookup"><span data-stu-id="4716e-126">Resource identifier of Synapse integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4716e-127">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="4716e-127">-WorkspaceName</span></span>
<span data-ttu-id="4716e-128">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="4716e-128">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4716e-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="4716e-129">-WorkspaceObject</span></span>
<span data-ttu-id="4716e-130">objeto de entrada de espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="4716e-130">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RemoveByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4716e-131">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="4716e-131">-Confirm</span></span>
<span data-ttu-id="4716e-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4716e-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4716e-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4716e-133">-WhatIf</span></span>
<span data-ttu-id="4716e-134">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="4716e-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4716e-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4716e-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4716e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4716e-136">CommonParameters</span></span>
<span data-ttu-id="4716e-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4716e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4716e-138">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4716e-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4716e-139">Entradas</span><span class="sxs-lookup"><span data-stu-id="4716e-139">INPUTS</span></span>

### <span data-ttu-id="4716e-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="4716e-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="4716e-141">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="4716e-141">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="4716e-142">Saídas</span><span class="sxs-lookup"><span data-stu-id="4716e-142">OUTPUTS</span></span>

### <span data-ttu-id="4716e-143">System.Void</span><span class="sxs-lookup"><span data-stu-id="4716e-143">System.Void</span></span>

## <span data-ttu-id="4716e-144">Notas</span><span class="sxs-lookup"><span data-stu-id="4716e-144">NOTES</span></span>

## <span data-ttu-id="4716e-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4716e-145">RELATED LINKS</span></span>
