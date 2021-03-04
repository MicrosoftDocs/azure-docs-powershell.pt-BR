---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/new-azsynapseintegrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseIntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseIntegrationRuntimeKey.md
ms.openlocfilehash: 143238bfcc8dffc209150a675af0a982d20663bb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888396"
---
# <span data-ttu-id="dadd7-101">New-AzSynapseIntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="dadd7-101">New-AzSynapseIntegrationRuntimeKey</span></span>

## <span data-ttu-id="dadd7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dadd7-102">SYNOPSIS</span></span>
<span data-ttu-id="dadd7-103">Regenerar a chave de tempo de execução de integração auto-hospedada.</span><span class="sxs-lookup"><span data-stu-id="dadd7-103">Regenerate self-hosted integration runtime key.</span></span>

## <span data-ttu-id="dadd7-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="dadd7-104">SYNTAX</span></span>

### <span data-ttu-id="dadd7-105">NewByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="dadd7-105">NewByNameParameterSet (Default)</span></span>
```
New-AzSynapseIntegrationRuntimeKey [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 -KeyName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dadd7-106">NewByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dadd7-106">NewByParentObjectParameterSet</span></span>
```
New-AzSynapseIntegrationRuntimeKey -Name <String> -WorkspaceObject <PSSynapseWorkspace> -KeyName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dadd7-107">NewByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dadd7-107">NewByResourceIdParameterSet</span></span>
```
New-AzSynapseIntegrationRuntimeKey -ResourceId <String> -KeyName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dadd7-108">NewByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dadd7-108">NewByInputObjectParameterSet</span></span>
```
New-AzSynapseIntegrationRuntimeKey -InputObject <PSIntegrationRuntime> -KeyName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dadd7-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="dadd7-109">DESCRIPTION</span></span>
<span data-ttu-id="dadd7-110">O cmdlet **New-AzSynapseIntegrationRuntimeKey** regenera a chave de tempo de execução de integração com o nome da chave especificado pelo parâmetro 'KeyName'.</span><span class="sxs-lookup"><span data-stu-id="dadd7-110">The cmdlet **New-AzSynapseIntegrationRuntimeKey** regenerates the integration runtime key with the key name specified by 'KeyName' parameter.</span></span> <span data-ttu-id="dadd7-111">A chave anterior será inválida.</span><span class="sxs-lookup"><span data-stu-id="dadd7-111">The previous key will is invalid.</span></span>

## <span data-ttu-id="dadd7-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dadd7-112">EXAMPLES</span></span>

### <span data-ttu-id="dadd7-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="dadd7-113">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseIntegrationRuntimeKey -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' -KeyName authKey2
```

<span data-ttu-id="dadd7-114">O cmdlet regenera a chave 'authKey2' para o tempo de execução de integração chamado 'test-selfhost-ir'.</span><span class="sxs-lookup"><span data-stu-id="dadd7-114">The cmdlet regenerates key 'authKey2' for integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="dadd7-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="dadd7-115">PARAMETERS</span></span>

### <span data-ttu-id="dadd7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dadd7-116">-DefaultProfile</span></span>
<span data-ttu-id="dadd7-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dadd7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dadd7-118">-Force</span><span class="sxs-lookup"><span data-stu-id="dadd7-118">-Force</span></span>
<span data-ttu-id="dadd7-119">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="dadd7-119">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="dadd7-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dadd7-120">-InputObject</span></span>
<span data-ttu-id="dadd7-121">O objeto de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="dadd7-121">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: NewByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dadd7-122">-KeyName</span><span class="sxs-lookup"><span data-stu-id="dadd7-122">-KeyName</span></span>
<span data-ttu-id="dadd7-123">O nome da chave de autenticação do tempo de execução de integração auto-hospedado.</span><span class="sxs-lookup"><span data-stu-id="dadd7-123">The authentication key name of the self-hosted integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AuthKey1, AuthKey2

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dadd7-124">-Name</span><span class="sxs-lookup"><span data-stu-id="dadd7-124">-Name</span></span>
<span data-ttu-id="dadd7-125">O nome do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="dadd7-125">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByNameParameterSet, NewByParentObjectParameterSet
Aliases: IntegrationRuntimeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dadd7-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dadd7-126">-ResourceGroupName</span></span>
<span data-ttu-id="dadd7-127">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="dadd7-127">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dadd7-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dadd7-128">-ResourceId</span></span>
<span data-ttu-id="dadd7-129">Identificador de recursos do tempo de execução de integração synapse.</span><span class="sxs-lookup"><span data-stu-id="dadd7-129">Resource identifier of Synapse integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dadd7-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="dadd7-130">-WorkspaceName</span></span>
<span data-ttu-id="dadd7-131">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="dadd7-131">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dadd7-132">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="dadd7-132">-WorkspaceObject</span></span>
<span data-ttu-id="dadd7-133">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="dadd7-133">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: NewByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dadd7-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dadd7-134">-Confirm</span></span>
<span data-ttu-id="dadd7-135">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dadd7-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dadd7-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dadd7-136">-WhatIf</span></span>
<span data-ttu-id="dadd7-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="dadd7-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dadd7-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="dadd7-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dadd7-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dadd7-139">CommonParameters</span></span>
<span data-ttu-id="dadd7-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dadd7-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dadd7-141">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dadd7-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dadd7-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dadd7-142">INPUTS</span></span>

### <span data-ttu-id="dadd7-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="dadd7-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="dadd7-144">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="dadd7-144">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="dadd7-145">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="dadd7-145">OUTPUTS</span></span>

### <span data-ttu-id="dadd7-146">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="dadd7-146">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="dadd7-147">NOTES</span><span class="sxs-lookup"><span data-stu-id="dadd7-147">NOTES</span></span>

## <span data-ttu-id="dadd7-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dadd7-148">RELATED LINKS</span></span>
