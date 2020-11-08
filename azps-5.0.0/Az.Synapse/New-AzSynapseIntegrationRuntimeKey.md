---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapseintegrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseIntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseIntegrationRuntimeKey.md
ms.openlocfilehash: 836dcabaa190b66daf5a4f3f2fdaf300fe47ccdf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94117934"
---
# <span data-ttu-id="b9c42-101">New-AzSynapseIntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="b9c42-101">New-AzSynapseIntegrationRuntimeKey</span></span>

## <span data-ttu-id="b9c42-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b9c42-102">SYNOPSIS</span></span>
<span data-ttu-id="b9c42-103">Regenerar a chave de tempo de execução de integração de hospedagem automática.</span><span class="sxs-lookup"><span data-stu-id="b9c42-103">Regenerate self-hosted integration runtime key.</span></span>

## <span data-ttu-id="b9c42-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b9c42-104">SYNTAX</span></span>

### <span data-ttu-id="b9c42-105">NewByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="b9c42-105">NewByNameParameterSet (Default)</span></span>
```
New-AzSynapseIntegrationRuntimeKey [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 -KeyName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b9c42-106">NewByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b9c42-106">NewByParentObjectParameterSet</span></span>
```
New-AzSynapseIntegrationRuntimeKey -Name <String> -WorkspaceObject <PSSynapseWorkspace> -KeyName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9c42-107">NewByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b9c42-107">NewByResourceIdParameterSet</span></span>
```
New-AzSynapseIntegrationRuntimeKey -ResourceId <String> -KeyName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9c42-108">NewByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b9c42-108">NewByInputObjectParameterSet</span></span>
```
New-AzSynapseIntegrationRuntimeKey -InputObject <PSIntegrationRuntime> -KeyName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9c42-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b9c42-109">DESCRIPTION</span></span>
<span data-ttu-id="b9c42-110">O cmdlet **New-AzSynapseIntegrationRuntimeKey** regenera a chave de tempo de execução de integração com o nome de chave especificado pelo parâmetro ' KeyName '.</span><span class="sxs-lookup"><span data-stu-id="b9c42-110">The cmdlet **New-AzSynapseIntegrationRuntimeKey** regenerates the integration runtime key with the key name specified by 'KeyName' parameter.</span></span> <span data-ttu-id="b9c42-111">A chave anterior será inválida.</span><span class="sxs-lookup"><span data-stu-id="b9c42-111">The previous key will is invalid.</span></span>

## <span data-ttu-id="b9c42-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b9c42-112">EXAMPLES</span></span>

### <span data-ttu-id="b9c42-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b9c42-113">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseIntegrationRuntimeKey -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' -KeyName authKey2
```

<span data-ttu-id="b9c42-114">O cmdlet regenera a chave "authKey2" para o tempo de execução de integração chamado "Test-selfhost-IV".</span><span class="sxs-lookup"><span data-stu-id="b9c42-114">The cmdlet regenerates key 'authKey2' for integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="b9c42-115">OS</span><span class="sxs-lookup"><span data-stu-id="b9c42-115">PARAMETERS</span></span>

### <span data-ttu-id="b9c42-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9c42-116">-DefaultProfile</span></span>
<span data-ttu-id="b9c42-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b9c42-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9c42-118">-Force</span><span class="sxs-lookup"><span data-stu-id="b9c42-118">-Force</span></span>
<span data-ttu-id="b9c42-119">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="b9c42-119">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="b9c42-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b9c42-120">-InputObject</span></span>
<span data-ttu-id="b9c42-121">O objeto de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="b9c42-121">The integration runtime object.</span></span>

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

### <span data-ttu-id="b9c42-122">-KeyName</span><span class="sxs-lookup"><span data-stu-id="b9c42-122">-KeyName</span></span>
<span data-ttu-id="b9c42-123">O nome da chave de autenticação do tempo de execução de integração de hospedagem interna.</span><span class="sxs-lookup"><span data-stu-id="b9c42-123">The authentication key name of the self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="b9c42-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="b9c42-124">-Name</span></span>
<span data-ttu-id="b9c42-125">O nome do tempo de execução da integração.</span><span class="sxs-lookup"><span data-stu-id="b9c42-125">The integration runtime name.</span></span>

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

### <span data-ttu-id="b9c42-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9c42-126">-ResourceGroupName</span></span>
<span data-ttu-id="b9c42-127">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b9c42-127">Resource group name.</span></span>

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

### <span data-ttu-id="b9c42-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b9c42-128">-ResourceId</span></span>
<span data-ttu-id="b9c42-129">Identificador de recurso do tempo de execução de integração do Synapse.</span><span class="sxs-lookup"><span data-stu-id="b9c42-129">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="b9c42-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b9c42-130">-WorkspaceName</span></span>
<span data-ttu-id="b9c42-131">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="b9c42-131">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="b9c42-132">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="b9c42-132">-WorkspaceObject</span></span>
<span data-ttu-id="b9c42-133">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="b9c42-133">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="b9c42-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b9c42-134">-Confirm</span></span>
<span data-ttu-id="b9c42-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9c42-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9c42-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9c42-136">-WhatIf</span></span>
<span data-ttu-id="b9c42-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b9c42-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9c42-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b9c42-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9c42-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9c42-139">CommonParameters</span></span>
<span data-ttu-id="b9c42-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9c42-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9c42-141">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b9c42-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9c42-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b9c42-142">INPUTS</span></span>

### <span data-ttu-id="b9c42-143">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="b9c42-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="b9c42-144">Microsoft. Azure. Commands. Synapse. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="b9c42-144">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="b9c42-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b9c42-145">OUTPUTS</span></span>

### <span data-ttu-id="b9c42-146">Microsoft. Azure. Commands. Synapse. Models. PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="b9c42-146">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="b9c42-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b9c42-147">NOTES</span></span>

## <span data-ttu-id="b9c42-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b9c42-148">RELATED LINKS</span></span>
