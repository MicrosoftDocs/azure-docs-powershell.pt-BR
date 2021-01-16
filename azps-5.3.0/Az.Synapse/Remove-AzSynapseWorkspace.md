---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseWorkspace.md
ms.openlocfilehash: fbdca80b33dd15e34a958cb63a41377b400d03ce
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98429631"
---
# <span data-ttu-id="801c2-101">Remove-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="801c2-101">Remove-AzSynapseWorkspace</span></span>

## <span data-ttu-id="801c2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="801c2-102">SYNOPSIS</span></span>
<span data-ttu-id="801c2-103">Exclui um espaço de trabalho de análise do Synapse.</span><span class="sxs-lookup"><span data-stu-id="801c2-103">Deletes a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="801c2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="801c2-104">SYNTAX</span></span>

### <span data-ttu-id="801c2-105">DeleteByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="801c2-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseWorkspace [-ResourceGroupName <String>] -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="801c2-106">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="801c2-106">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseWorkspace -InputObject <PSSynapseWorkspace> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="801c2-107">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="801c2-107">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseWorkspace -ResourceId <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="801c2-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="801c2-108">DESCRIPTION</span></span>
<span data-ttu-id="801c2-109">O cmdlet **Remove-AzSynapseWorkspace** exclui permanentemente um espaço de trabalho de análise do Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="801c2-109">The **Remove-AzSynapseWorkspace** cmdlet permanently deletes an Azure Synapse Analytics workspace.</span></span>

## <span data-ttu-id="801c2-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="801c2-110">EXAMPLES</span></span>

### <span data-ttu-id="801c2-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="801c2-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseWorkspace -Name ContosoWorkspace
```

<span data-ttu-id="801c2-112">Esse comando exclui um espaço de trabalho de análise do Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="801c2-112">This command deletes an Azure Synapse Analytics workspace.</span></span>

### <span data-ttu-id="801c2-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="801c2-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseWorkspace
```

<span data-ttu-id="801c2-114">Esse comando exclui um espaço de trabalho de análise do Azure Synapse por meio do pipeline.</span><span class="sxs-lookup"><span data-stu-id="801c2-114">This command deletes an Azure Synapse Analytics workspace through pipeline.</span></span>

### <span data-ttu-id="801c2-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="801c2-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzSynapseWorkspace -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace
```

<span data-ttu-id="801c2-116">Esse comando exclui um espaço de trabalho de análise do Azure Synapse por meio do pipeline com a ID de recurso especificada.</span><span class="sxs-lookup"><span data-stu-id="801c2-116">This command deletes an Azure Synapse Analytics workspace through pipeline with the specified resource ID.</span></span>

## <span data-ttu-id="801c2-117">OS</span><span class="sxs-lookup"><span data-stu-id="801c2-117">PARAMETERS</span></span>

### <span data-ttu-id="801c2-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="801c2-118">-AsJob</span></span>
<span data-ttu-id="801c2-119">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="801c2-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="801c2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="801c2-120">-DefaultProfile</span></span>
<span data-ttu-id="801c2-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="801c2-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="801c2-122">-Force</span><span class="sxs-lookup"><span data-stu-id="801c2-122">-Force</span></span>
<span data-ttu-id="801c2-123">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="801c2-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="801c2-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="801c2-124">-InputObject</span></span>
<span data-ttu-id="801c2-125">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="801c2-125">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="801c2-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="801c2-126">-Name</span></span>
<span data-ttu-id="801c2-127">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="801c2-127">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="801c2-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="801c2-128">-PassThru</span></span>
<span data-ttu-id="801c2-129">Esse cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="801c2-129">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="801c2-130">Se essa opção for especificada, retornará true se for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="801c2-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="801c2-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="801c2-131">-ResourceGroupName</span></span>
<span data-ttu-id="801c2-132">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="801c2-132">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="801c2-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="801c2-133">-ResourceId</span></span>
<span data-ttu-id="801c2-134">Identificador de recurso do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="801c2-134">Resource identifier of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="801c2-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="801c2-135">-Confirm</span></span>
<span data-ttu-id="801c2-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="801c2-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="801c2-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="801c2-137">-WhatIf</span></span>
<span data-ttu-id="801c2-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="801c2-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="801c2-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="801c2-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="801c2-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="801c2-140">CommonParameters</span></span>
<span data-ttu-id="801c2-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="801c2-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="801c2-142">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="801c2-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="801c2-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="801c2-143">INPUTS</span></span>

### <span data-ttu-id="801c2-144">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="801c2-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="801c2-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="801c2-145">OUTPUTS</span></span>

### <span data-ttu-id="801c2-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="801c2-146">System.Boolean</span></span>

## <span data-ttu-id="801c2-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="801c2-147">NOTES</span></span>

## <span data-ttu-id="801c2-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="801c2-148">RELATED LINKS</span></span>
