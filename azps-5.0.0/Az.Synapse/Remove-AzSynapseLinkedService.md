---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapselinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseLinkedService.md
ms.openlocfilehash: ca493914cc91d16566fddcebed5367fa81be1d2d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94117913"
---
# <span data-ttu-id="e0358-101">Remove-AzSynapseLinkedService</span><span class="sxs-lookup"><span data-stu-id="e0358-101">Remove-AzSynapseLinkedService</span></span>

## <span data-ttu-id="e0358-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e0358-102">SYNOPSIS</span></span>
<span data-ttu-id="e0358-103">Remove um serviço vinculado do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="e0358-103">Removes a linked service from workspace.</span></span>

## <span data-ttu-id="e0358-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e0358-104">SYNTAX</span></span>

### <span data-ttu-id="e0358-105">RemoveByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="e0358-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseLinkedService -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0358-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="e0358-106">RemoveByObject</span></span>
```
Remove-AzSynapseLinkedService -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0358-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="e0358-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseLinkedService -InputObject <PSLinkedServiceResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0358-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e0358-108">DESCRIPTION</span></span>
<span data-ttu-id="e0358-109">O cmdlet **Remove-AzSynapseLinkedService** remove um serviço vinculado do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="e0358-109">The **Remove-AzSynapseLinkedService** cmdlet removes a linked service from workspace.</span></span>

## <span data-ttu-id="e0358-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e0358-110">EXAMPLES</span></span>

### <span data-ttu-id="e0358-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e0358-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseLinkedService -WorkspaceName ContosoWorkspace -Name ContosoLinkedService
```

<span data-ttu-id="e0358-112">Esse comando Remove o serviço vinculado denominado ContosoLinkedService do espaço de trabalho chamado ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="e0358-112">This command removes the linked service named ContosoLinkedService from the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="e0358-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="e0358-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseLinkedService -Name ContosoLinkedService
```

<span data-ttu-id="e0358-114">Esse comando Remove o serviço vinculado denominado ContosoLinkedService do espaço de trabalho chamado ContosoWorkspace pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="e0358-114">This command removes the linked service named ContosoLinkedService from the workspace named ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="e0358-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="e0358-115">Example 3</span></span>
```powershell
PS C:\> $linkedService = Get-AzSynapseLinkedService -WorkspaceName ContosoWorkspace -Name ContosoLinkedService
PS C:\> $linkedService | Remove-AzSynapseLinkedService
```

<span data-ttu-id="e0358-116">Esse comando Remove o serviço vinculado denominado ContosoLinkedService do espaço de trabalho chamado ContosoWorkspace pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="e0358-116">This command removes the linked service named ContosoLinkedService from the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="e0358-117">OS</span><span class="sxs-lookup"><span data-stu-id="e0358-117">PARAMETERS</span></span>

### <span data-ttu-id="e0358-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e0358-118">-AsJob</span></span>
<span data-ttu-id="e0358-119">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="e0358-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e0358-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0358-120">-DefaultProfile</span></span>
<span data-ttu-id="e0358-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e0358-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0358-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e0358-122">-InputObject</span></span>
<span data-ttu-id="e0358-123">O objeto de serviço vinculado.</span><span class="sxs-lookup"><span data-stu-id="e0358-123">The linked service object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e0358-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="e0358-124">-Name</span></span>
<span data-ttu-id="e0358-125">O nome do serviço vinculado.</span><span class="sxs-lookup"><span data-stu-id="e0358-125">The linked service name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName, RemoveByObject
Aliases: LinkedServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0358-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e0358-126">-PassThru</span></span>
<span data-ttu-id="e0358-127">Esse cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="e0358-127">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="e0358-128">Se essa opção for especificada, retornará true se for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="e0358-128">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="e0358-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e0358-129">-WorkspaceName</span></span>
<span data-ttu-id="e0358-130">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="e0358-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="e0358-131">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="e0358-131">-WorkspaceObject</span></span>
<span data-ttu-id="e0358-132">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="e0358-132">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="e0358-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e0358-133">-Confirm</span></span>
<span data-ttu-id="e0358-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0358-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0358-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0358-135">-WhatIf</span></span>
<span data-ttu-id="e0358-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e0358-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e0358-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e0358-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0358-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0358-138">CommonParameters</span></span>
<span data-ttu-id="e0358-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0358-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0358-140">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e0358-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0358-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e0358-141">INPUTS</span></span>

### <span data-ttu-id="e0358-142">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="e0358-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="e0358-143">Microsoft. Azure. Commands. Synapse. Models. PSLinkedServiceResource</span><span class="sxs-lookup"><span data-stu-id="e0358-143">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span></span>

## <span data-ttu-id="e0358-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e0358-144">OUTPUTS</span></span>

### <span data-ttu-id="e0358-145">Microsoft. Azure. Commands. Synapse. Models. PSLinkedServiceResource</span><span class="sxs-lookup"><span data-stu-id="e0358-145">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span></span>

## <span data-ttu-id="e0358-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e0358-146">NOTES</span></span>

## <span data-ttu-id="e0358-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e0358-147">RELATED LINKS</span></span>
