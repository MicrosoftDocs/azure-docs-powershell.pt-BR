---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapseintegrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseIntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseIntegrationRuntime.md
ms.openlocfilehash: 57b6c6619a45e515c7aff2e30edc346ff39af9ac
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260640"
---
# <span data-ttu-id="4a9a9-101">Remove-AzSynapseIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="4a9a9-101">Remove-AzSynapseIntegrationRuntime</span></span>

## <span data-ttu-id="4a9a9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4a9a9-102">SYNOPSIS</span></span>
<span data-ttu-id="4a9a9-103">Remove um tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="4a9a9-103">Removes an integration runtime.</span></span>

## <span data-ttu-id="4a9a9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4a9a9-104">SYNTAX</span></span>

### <span data-ttu-id="4a9a9-105">RemoveByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="4a9a9-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseIntegrationRuntime [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a9a9-106">RemoveByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4a9a9-106">RemoveByParentObjectParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntime -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a9a9-107">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4a9a9-107">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntime -ResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a9a9-108">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4a9a9-108">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntime -InputObject <PSIntegrationRuntime> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a9a9-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4a9a9-109">DESCRIPTION</span></span>
<span data-ttu-id="4a9a9-110">O cmdlet **Remove-AzSynapseIntegrationRuntime** remove um tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="4a9a9-110">The **Remove-AzSynapseIntegrationRuntime** cmdlet removes a integration runtime.</span></span>

## <span data-ttu-id="4a9a9-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4a9a9-111">EXAMPLES</span></span>

### <span data-ttu-id="4a9a9-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4a9a9-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-reserved-ir' -Confirm
```

<span data-ttu-id="4a9a9-113">Esse comando Remove o tempo de execução de integração chamado "Test-reservado-IV" do espaço de trabalho chamado ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="4a9a9-113">This command removes the integration runtime named 'test-reserved-ir' from the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="4a9a9-114">OS</span><span class="sxs-lookup"><span data-stu-id="4a9a9-114">PARAMETERS</span></span>

### <span data-ttu-id="4a9a9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a9a9-115">-DefaultProfile</span></span>
<span data-ttu-id="4a9a9-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4a9a9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a9a9-117">-Force</span><span class="sxs-lookup"><span data-stu-id="4a9a9-117">-Force</span></span>
<span data-ttu-id="4a9a9-118">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="4a9a9-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="4a9a9-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4a9a9-119">-InputObject</span></span>
<span data-ttu-id="4a9a9-120">O objeto de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="4a9a9-120">The integration runtime object.</span></span>

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

### <span data-ttu-id="4a9a9-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="4a9a9-121">-Name</span></span>
<span data-ttu-id="4a9a9-122">O nome do tempo de execução da integração.</span><span class="sxs-lookup"><span data-stu-id="4a9a9-122">The integration runtime name.</span></span>

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

### <span data-ttu-id="4a9a9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a9a9-123">-ResourceGroupName</span></span>
<span data-ttu-id="4a9a9-124">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4a9a9-124">Resource group name.</span></span>

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

### <span data-ttu-id="4a9a9-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4a9a9-125">-ResourceId</span></span>
<span data-ttu-id="4a9a9-126">Identificador de recurso do tempo de execução de integração do Synapse.</span><span class="sxs-lookup"><span data-stu-id="4a9a9-126">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="4a9a9-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="4a9a9-127">-WorkspaceName</span></span>
<span data-ttu-id="4a9a9-128">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="4a9a9-128">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="4a9a9-129">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="4a9a9-129">-WorkspaceObject</span></span>
<span data-ttu-id="4a9a9-130">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="4a9a9-130">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="4a9a9-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4a9a9-131">-Confirm</span></span>
<span data-ttu-id="4a9a9-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4a9a9-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a9a9-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a9a9-133">-WhatIf</span></span>
<span data-ttu-id="4a9a9-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4a9a9-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a9a9-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4a9a9-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a9a9-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a9a9-136">CommonParameters</span></span>
<span data-ttu-id="4a9a9-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a9a9-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a9a9-138">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4a9a9-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a9a9-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4a9a9-139">INPUTS</span></span>

### <span data-ttu-id="4a9a9-140">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="4a9a9-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="4a9a9-141">Microsoft. Azure. Commands. Synapse. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="4a9a9-141">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="4a9a9-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4a9a9-142">OUTPUTS</span></span>

### <span data-ttu-id="4a9a9-143">System. void</span><span class="sxs-lookup"><span data-stu-id="4a9a9-143">System.Void</span></span>

## <span data-ttu-id="4a9a9-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4a9a9-144">NOTES</span></span>

## <span data-ttu-id="4a9a9-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4a9a9-145">RELATED LINKS</span></span>
