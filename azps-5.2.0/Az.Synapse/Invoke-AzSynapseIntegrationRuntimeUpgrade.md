---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/invoke-azsynapseintegrationruntimeupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapseIntegrationRuntimeUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapseIntegrationRuntimeUpgrade.md
ms.openlocfilehash: 59630bd0ffcf5bebfc68f647cff444466727a990
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98262526"
---
# <span data-ttu-id="96f72-101">Invoke-AzSynapseIntegrationRuntimeUpgrade</span><span class="sxs-lookup"><span data-stu-id="96f72-101">Invoke-AzSynapseIntegrationRuntimeUpgrade</span></span>

## <span data-ttu-id="96f72-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="96f72-102">SYNOPSIS</span></span>
<span data-ttu-id="96f72-103">Atualiza o tempo de execução de integração de hospedagem automática.</span><span class="sxs-lookup"><span data-stu-id="96f72-103">Upgrades self-hosted integration runtime.</span></span>

## <span data-ttu-id="96f72-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="96f72-104">SYNTAX</span></span>

### <span data-ttu-id="96f72-105">InvokeByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="96f72-105">InvokeByNameParameterSet (Default)</span></span>
```
Invoke-AzSynapseIntegrationRuntimeUpgrade [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96f72-106">InvokeByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="96f72-106">InvokeByParentObjectParameterSet</span></span>
```
Invoke-AzSynapseIntegrationRuntimeUpgrade -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96f72-107">InvokeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="96f72-107">InvokeByResourceIdParameterSet</span></span>
```
Invoke-AzSynapseIntegrationRuntimeUpgrade -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96f72-108">InvokeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="96f72-108">InvokeByInputObjectParameterSet</span></span>
```
Invoke-AzSynapseIntegrationRuntimeUpgrade -InputObject <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96f72-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="96f72-109">DESCRIPTION</span></span>
<span data-ttu-id="96f72-110">O cmdlet **Invoke-AzSynapseIntegrationRuntimeUpgrade** atualiza o tempo de execução de integração de hospedagem interna se a nova versão estiver disponível.</span><span class="sxs-lookup"><span data-stu-id="96f72-110">The **Invoke-AzSynapseIntegrationRuntimeUpgrade** cmdlet upgrades self-hosted integration runtime if the new version is available.</span></span>

## <span data-ttu-id="96f72-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="96f72-111">EXAMPLES</span></span>

### <span data-ttu-id="96f72-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="96f72-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSynapseIntegrationRuntimeUpgrade -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir'
```

<span data-ttu-id="96f72-113">O cmdlet atualiza o tempo de execução de integração de hospedagem interna chamado ' test-selfhost-IV ' na ContosoWorkspace do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="96f72-113">The cmdlet upgrades self-hosted integration runtime named 'test-selfhost-ir' in workspace ContosoWorkspace.</span></span>

## <span data-ttu-id="96f72-114">OS</span><span class="sxs-lookup"><span data-stu-id="96f72-114">PARAMETERS</span></span>

### <span data-ttu-id="96f72-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96f72-115">-DefaultProfile</span></span>
<span data-ttu-id="96f72-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="96f72-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96f72-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="96f72-117">-InputObject</span></span>
<span data-ttu-id="96f72-118">O objeto de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="96f72-118">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: InvokeByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="96f72-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="96f72-119">-Name</span></span>
<span data-ttu-id="96f72-120">O nome do tempo de execução da integração.</span><span class="sxs-lookup"><span data-stu-id="96f72-120">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet, InvokeByParentObjectParameterSet
Aliases: IntegrationRuntimeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96f72-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96f72-121">-ResourceGroupName</span></span>
<span data-ttu-id="96f72-122">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="96f72-122">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96f72-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="96f72-123">-ResourceId</span></span>
<span data-ttu-id="96f72-124">Identificador de recurso do tempo de execução de integração do Synapse.</span><span class="sxs-lookup"><span data-stu-id="96f72-124">Resource identifier of Synapse integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96f72-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="96f72-125">-WorkspaceName</span></span>
<span data-ttu-id="96f72-126">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="96f72-126">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96f72-127">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="96f72-127">-WorkspaceObject</span></span>
<span data-ttu-id="96f72-128">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="96f72-128">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: InvokeByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="96f72-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="96f72-129">-Confirm</span></span>
<span data-ttu-id="96f72-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="96f72-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96f72-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96f72-131">-WhatIf</span></span>
<span data-ttu-id="96f72-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="96f72-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96f72-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="96f72-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96f72-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96f72-134">CommonParameters</span></span>
<span data-ttu-id="96f72-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96f72-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96f72-136">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="96f72-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96f72-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="96f72-137">INPUTS</span></span>

### <span data-ttu-id="96f72-138">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="96f72-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="96f72-139">Microsoft. Azure. Commands. Synapse. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="96f72-139">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="96f72-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="96f72-140">OUTPUTS</span></span>

### <span data-ttu-id="96f72-141">System. void</span><span class="sxs-lookup"><span data-stu-id="96f72-141">System.Void</span></span>

## <span data-ttu-id="96f72-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="96f72-142">NOTES</span></span>

## <span data-ttu-id="96f72-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="96f72-143">RELATED LINKS</span></span>
