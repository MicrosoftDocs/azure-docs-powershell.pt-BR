---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/remove-azsynapselinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseLinkedService.md
ms.openlocfilehash: 640992f0070d6cff14852000b07ecd8eddc61c1c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889879"
---
# <span data-ttu-id="3fe1e-101">Remove-AzSynapseLinkedService</span><span class="sxs-lookup"><span data-stu-id="3fe1e-101">Remove-AzSynapseLinkedService</span></span>

## <span data-ttu-id="3fe1e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3fe1e-102">SYNOPSIS</span></span>
<span data-ttu-id="3fe1e-103">Remove um serviço vinculado do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="3fe1e-103">Removes a linked service from workspace.</span></span>

## <span data-ttu-id="3fe1e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="3fe1e-104">SYNTAX</span></span>

### <span data-ttu-id="3fe1e-105">RemoveByName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="3fe1e-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseLinkedService -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3fe1e-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="3fe1e-106">RemoveByObject</span></span>
```
Remove-AzSynapseLinkedService -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3fe1e-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="3fe1e-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseLinkedService -InputObject <PSLinkedServiceResource> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3fe1e-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="3fe1e-108">DESCRIPTION</span></span>
<span data-ttu-id="3fe1e-109">O cmdlet **Remove-AzSynapseLinkedService** remove um serviço vinculado do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="3fe1e-109">The **Remove-AzSynapseLinkedService** cmdlet removes a linked service from workspace.</span></span>

## <span data-ttu-id="3fe1e-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3fe1e-110">EXAMPLES</span></span>

### <span data-ttu-id="3fe1e-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3fe1e-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseLinkedService -WorkspaceName ContosoWorkspace -Name ContosoLinkedService
```

<span data-ttu-id="3fe1e-112">Este comando remove o serviço vinculado chamado ContosoLinkedService do espaço de trabalho chamado ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="3fe1e-112">This command removes the linked service named ContosoLinkedService from the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="3fe1e-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="3fe1e-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseLinkedService -Name ContosoLinkedService
```

<span data-ttu-id="3fe1e-114">Este comando remove o serviço vinculado chamado ContosoLinkedService do espaço de trabalho chamado ContosoWorkspace por pipeline.</span><span class="sxs-lookup"><span data-stu-id="3fe1e-114">This command removes the linked service named ContosoLinkedService from the workspace named ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="3fe1e-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="3fe1e-115">Example 3</span></span>
```powershell
PS C:\> $linkedService = Get-AzSynapseLinkedService -WorkspaceName ContosoWorkspace -Name ContosoLinkedService
PS C:\> $linkedService | Remove-AzSynapseLinkedService
```

<span data-ttu-id="3fe1e-116">Este comando remove o serviço vinculado chamado ContosoLinkedService do espaço de trabalho chamado ContosoWorkspace por pipeline.</span><span class="sxs-lookup"><span data-stu-id="3fe1e-116">This command removes the linked service named ContosoLinkedService from the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="3fe1e-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="3fe1e-117">PARAMETERS</span></span>

### <span data-ttu-id="3fe1e-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3fe1e-118">-AsJob</span></span>
<span data-ttu-id="3fe1e-119">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="3fe1e-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3fe1e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fe1e-120">-DefaultProfile</span></span>
<span data-ttu-id="3fe1e-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3fe1e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3fe1e-122">-Force</span><span class="sxs-lookup"><span data-stu-id="3fe1e-122">-Force</span></span>
<span data-ttu-id="3fe1e-123">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="3fe1e-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="3fe1e-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3fe1e-124">-InputObject</span></span>
<span data-ttu-id="3fe1e-125">O objeto de serviço vinculado.</span><span class="sxs-lookup"><span data-stu-id="3fe1e-125">The linked service object.</span></span>

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

### <span data-ttu-id="3fe1e-126">-Name</span><span class="sxs-lookup"><span data-stu-id="3fe1e-126">-Name</span></span>
<span data-ttu-id="3fe1e-127">O nome do serviço vinculado.</span><span class="sxs-lookup"><span data-stu-id="3fe1e-127">The linked service name.</span></span>

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

### <span data-ttu-id="3fe1e-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3fe1e-128">-PassThru</span></span>
<span data-ttu-id="3fe1e-129">Este Cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="3fe1e-129">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="3fe1e-130">Se essa opção for especificada, ela retornará true se tiver êxito.</span><span class="sxs-lookup"><span data-stu-id="3fe1e-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="3fe1e-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3fe1e-131">-WorkspaceName</span></span>
<span data-ttu-id="3fe1e-132">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="3fe1e-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="3fe1e-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="3fe1e-133">-WorkspaceObject</span></span>
<span data-ttu-id="3fe1e-134">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="3fe1e-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="3fe1e-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3fe1e-135">-Confirm</span></span>
<span data-ttu-id="3fe1e-136">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3fe1e-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3fe1e-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3fe1e-137">-WhatIf</span></span>
<span data-ttu-id="3fe1e-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3fe1e-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3fe1e-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3fe1e-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3fe1e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fe1e-140">CommonParameters</span></span>
<span data-ttu-id="3fe1e-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3fe1e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fe1e-142">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3fe1e-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fe1e-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3fe1e-143">INPUTS</span></span>

### <span data-ttu-id="3fe1e-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="3fe1e-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="3fe1e-145">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span><span class="sxs-lookup"><span data-stu-id="3fe1e-145">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span></span>

## <span data-ttu-id="3fe1e-146">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="3fe1e-146">OUTPUTS</span></span>

### <span data-ttu-id="3fe1e-147">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span><span class="sxs-lookup"><span data-stu-id="3fe1e-147">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span></span>

## <span data-ttu-id="3fe1e-148">NOTES</span><span class="sxs-lookup"><span data-stu-id="3fe1e-148">NOTES</span></span>

## <span data-ttu-id="3fe1e-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3fe1e-149">RELATED LINKS</span></span>
