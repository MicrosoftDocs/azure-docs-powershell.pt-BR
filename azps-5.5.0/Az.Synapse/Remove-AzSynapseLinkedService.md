---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapselinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseLinkedService.md
ms.openlocfilehash: c70cc0f8659a04e8a10a4fbd2b776d22fca6a616
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115614"
---
# <span data-ttu-id="4beb4-101">Remove-AzSynapseLinkedService</span><span class="sxs-lookup"><span data-stu-id="4beb4-101">Remove-AzSynapseLinkedService</span></span>

## <span data-ttu-id="4beb4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4beb4-102">SYNOPSIS</span></span>
<span data-ttu-id="4beb4-103">Remove um serviço vinculado do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="4beb4-103">Removes a linked service from workspace.</span></span>

## <span data-ttu-id="4beb4-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4beb4-104">SYNTAX</span></span>

### <span data-ttu-id="4beb4-105">RemoveByName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="4beb4-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseLinkedService -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4beb4-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="4beb4-106">RemoveByObject</span></span>
```
Remove-AzSynapseLinkedService -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4beb4-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="4beb4-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseLinkedService -InputObject <PSLinkedServiceResource> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4beb4-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="4beb4-108">DESCRIPTION</span></span>
<span data-ttu-id="4beb4-109">O cmdlet **Remove-AzSynapseLinkedService** remove um serviço vinculado do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="4beb4-109">The **Remove-AzSynapseLinkedService** cmdlet removes a linked service from workspace.</span></span>

## <span data-ttu-id="4beb4-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4beb4-110">EXAMPLES</span></span>

### <span data-ttu-id="4beb4-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4beb4-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseLinkedService -WorkspaceName ContosoWorkspace -Name ContosoLinkedService
```

<span data-ttu-id="4beb4-112">Esse comando remove o serviço vinculado chamado ContosoLinkedService do espaço de trabalho chamado ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="4beb4-112">This command removes the linked service named ContosoLinkedService from the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="4beb4-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="4beb4-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseLinkedService -Name ContosoLinkedService
```

<span data-ttu-id="4beb4-114">Esse comando remove o serviço vinculado chamado ContosoLinkedService do espaço de trabalho chamado ContosoWorkspace por meio de pipeline.</span><span class="sxs-lookup"><span data-stu-id="4beb4-114">This command removes the linked service named ContosoLinkedService from the workspace named ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="4beb4-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="4beb4-115">Example 3</span></span>
```powershell
PS C:\> $linkedService = Get-AzSynapseLinkedService -WorkspaceName ContosoWorkspace -Name ContosoLinkedService
PS C:\> $linkedService | Remove-AzSynapseLinkedService
```

<span data-ttu-id="4beb4-116">Esse comando remove o serviço vinculado chamado ContosoLinkedService do espaço de trabalho chamado ContosoWorkspace por meio de pipeline.</span><span class="sxs-lookup"><span data-stu-id="4beb4-116">This command removes the linked service named ContosoLinkedService from the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="4beb4-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4beb4-117">PARAMETERS</span></span>

### <span data-ttu-id="4beb4-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4beb4-118">-AsJob</span></span>
<span data-ttu-id="4beb4-119">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="4beb4-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4beb4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4beb4-120">-DefaultProfile</span></span>
<span data-ttu-id="4beb4-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4beb4-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4beb4-122">-Forçar</span><span class="sxs-lookup"><span data-stu-id="4beb4-122">-Force</span></span>
<span data-ttu-id="4beb4-123">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="4beb4-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="4beb4-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4beb4-124">-InputObject</span></span>
<span data-ttu-id="4beb4-125">O objeto de serviço vinculado.</span><span class="sxs-lookup"><span data-stu-id="4beb4-125">The linked service object.</span></span>

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

### <span data-ttu-id="4beb4-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="4beb4-126">-Name</span></span>
<span data-ttu-id="4beb4-127">O nome do serviço vinculado.</span><span class="sxs-lookup"><span data-stu-id="4beb4-127">The linked service name.</span></span>

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

### <span data-ttu-id="4beb4-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4beb4-128">-PassThru</span></span>
<span data-ttu-id="4beb4-129">Este Cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="4beb4-129">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="4beb4-130">Se essa opção for especificada, ela retornará verdadeira se for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="4beb4-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="4beb4-131">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="4beb4-131">-WorkspaceName</span></span>
<span data-ttu-id="4beb4-132">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="4beb4-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="4beb4-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="4beb4-133">-WorkspaceObject</span></span>
<span data-ttu-id="4beb4-134">objeto de entrada de espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="4beb4-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="4beb4-135">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="4beb4-135">-Confirm</span></span>
<span data-ttu-id="4beb4-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4beb4-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4beb4-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4beb4-137">-WhatIf</span></span>
<span data-ttu-id="4beb4-138">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="4beb4-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4beb4-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4beb4-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4beb4-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4beb4-140">CommonParameters</span></span>
<span data-ttu-id="4beb4-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4beb4-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4beb4-142">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4beb4-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4beb4-143">Entradas</span><span class="sxs-lookup"><span data-stu-id="4beb4-143">INPUTS</span></span>

### <span data-ttu-id="4beb4-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="4beb4-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="4beb4-145">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span><span class="sxs-lookup"><span data-stu-id="4beb4-145">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span></span>

## <span data-ttu-id="4beb4-146">Saídas</span><span class="sxs-lookup"><span data-stu-id="4beb4-146">OUTPUTS</span></span>

### <span data-ttu-id="4beb4-147">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span><span class="sxs-lookup"><span data-stu-id="4beb4-147">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span></span>

## <span data-ttu-id="4beb4-148">Notas</span><span class="sxs-lookup"><span data-stu-id="4beb4-148">NOTES</span></span>

## <span data-ttu-id="4beb4-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4beb4-149">RELATED LINKS</span></span>
