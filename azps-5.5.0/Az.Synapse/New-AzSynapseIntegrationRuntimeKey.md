---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapseintegrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseIntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseIntegrationRuntimeKey.md
ms.openlocfilehash: 836dcabaa190b66daf5a4f3f2fdaf300fe47ccdf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116315"
---
# <span data-ttu-id="6ee4d-101">New-AzSynapseIntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="6ee4d-101">New-AzSynapseIntegrationRuntimeKey</span></span>

## <span data-ttu-id="6ee4d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6ee4d-102">SYNOPSIS</span></span>
<span data-ttu-id="6ee4d-103">Regenerar a chave de tempo de execução de integração auto-hospedada.</span><span class="sxs-lookup"><span data-stu-id="6ee4d-103">Regenerate self-hosted integration runtime key.</span></span>

## <span data-ttu-id="6ee4d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6ee4d-104">SYNTAX</span></span>

### <span data-ttu-id="6ee4d-105">NewByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="6ee4d-105">NewByNameParameterSet (Default)</span></span>
```
New-AzSynapseIntegrationRuntimeKey [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 -KeyName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6ee4d-106">NewByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ee4d-106">NewByParentObjectParameterSet</span></span>
```
New-AzSynapseIntegrationRuntimeKey -Name <String> -WorkspaceObject <PSSynapseWorkspace> -KeyName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ee4d-107">NewByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ee4d-107">NewByResourceIdParameterSet</span></span>
```
New-AzSynapseIntegrationRuntimeKey -ResourceId <String> -KeyName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ee4d-108">NewByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ee4d-108">NewByInputObjectParameterSet</span></span>
```
New-AzSynapseIntegrationRuntimeKey -InputObject <PSIntegrationRuntime> -KeyName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ee4d-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="6ee4d-109">DESCRIPTION</span></span>
<span data-ttu-id="6ee4d-110">O cmdlet **New-AzSynapseIntegrationRuntimeKey** regenera a tecla de tempo de execução de integração com o nome da chave especificado pelo parâmetro 'KeyName'.</span><span class="sxs-lookup"><span data-stu-id="6ee4d-110">The cmdlet **New-AzSynapseIntegrationRuntimeKey** regenerates the integration runtime key with the key name specified by 'KeyName' parameter.</span></span> <span data-ttu-id="6ee4d-111">A tecla anterior será inválida.</span><span class="sxs-lookup"><span data-stu-id="6ee4d-111">The previous key will is invalid.</span></span>

## <span data-ttu-id="6ee4d-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6ee4d-112">EXAMPLES</span></span>

### <span data-ttu-id="6ee4d-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6ee4d-113">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseIntegrationRuntimeKey -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' -KeyName authKey2
```

<span data-ttu-id="6ee4d-114">O cmdlet regenera a chave "authKey2" para tempo de execução de integração chamado "test-selfhost-ir".</span><span class="sxs-lookup"><span data-stu-id="6ee4d-114">The cmdlet regenerates key 'authKey2' for integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="6ee4d-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6ee4d-115">PARAMETERS</span></span>

### <span data-ttu-id="6ee4d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ee4d-116">-DefaultProfile</span></span>
<span data-ttu-id="6ee4d-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6ee4d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ee4d-118">-Forçar</span><span class="sxs-lookup"><span data-stu-id="6ee4d-118">-Force</span></span>
<span data-ttu-id="6ee4d-119">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="6ee4d-119">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="6ee4d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6ee4d-120">-InputObject</span></span>
<span data-ttu-id="6ee4d-121">O objeto de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="6ee4d-121">The integration runtime object.</span></span>

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

### <span data-ttu-id="6ee4d-122">-KeyName</span><span class="sxs-lookup"><span data-stu-id="6ee4d-122">-KeyName</span></span>
<span data-ttu-id="6ee4d-123">O nome da chave de autenticação do tempo de execução de integração auto-hospedado.</span><span class="sxs-lookup"><span data-stu-id="6ee4d-123">The authentication key name of the self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="6ee4d-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="6ee4d-124">-Name</span></span>
<span data-ttu-id="6ee4d-125">O nome de tempo de execução da integração.</span><span class="sxs-lookup"><span data-stu-id="6ee4d-125">The integration runtime name.</span></span>

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

### <span data-ttu-id="6ee4d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ee4d-126">-ResourceGroupName</span></span>
<span data-ttu-id="6ee4d-127">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6ee4d-127">Resource group name.</span></span>

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

### <span data-ttu-id="6ee4d-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6ee4d-128">-ResourceId</span></span>
<span data-ttu-id="6ee4d-129">Identificador de recursos do tempo de execução de integração synapse.</span><span class="sxs-lookup"><span data-stu-id="6ee4d-129">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="6ee4d-130">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="6ee4d-130">-WorkspaceName</span></span>
<span data-ttu-id="6ee4d-131">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="6ee4d-131">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="6ee4d-132">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="6ee4d-132">-WorkspaceObject</span></span>
<span data-ttu-id="6ee4d-133">objeto de entrada de espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="6ee4d-133">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="6ee4d-134">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="6ee4d-134">-Confirm</span></span>
<span data-ttu-id="6ee4d-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ee4d-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ee4d-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ee4d-136">-WhatIf</span></span>
<span data-ttu-id="6ee4d-137">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="6ee4d-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ee4d-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6ee4d-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ee4d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ee4d-139">CommonParameters</span></span>
<span data-ttu-id="6ee4d-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ee4d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ee4d-141">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6ee4d-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ee4d-142">Entradas</span><span class="sxs-lookup"><span data-stu-id="6ee4d-142">INPUTS</span></span>

### <span data-ttu-id="6ee4d-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="6ee4d-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="6ee4d-144">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="6ee4d-144">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="6ee4d-145">Saídas</span><span class="sxs-lookup"><span data-stu-id="6ee4d-145">OUTPUTS</span></span>

### <span data-ttu-id="6ee4d-146">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="6ee4d-146">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="6ee4d-147">Notas</span><span class="sxs-lookup"><span data-stu-id="6ee4d-147">NOTES</span></span>

## <span data-ttu-id="6ee4d-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6ee4d-148">RELATED LINKS</span></span>
