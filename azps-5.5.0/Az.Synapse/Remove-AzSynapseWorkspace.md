---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseWorkspace.md
ms.openlocfilehash: fbdca80b33dd15e34a958cb63a41377b400d03ce
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118538"
---
# <span data-ttu-id="8e90a-101">Remove-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="8e90a-101">Remove-AzSynapseWorkspace</span></span>

## <span data-ttu-id="8e90a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8e90a-102">SYNOPSIS</span></span>
<span data-ttu-id="8e90a-103">Exclui um espaço de trabalho do Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="8e90a-103">Deletes a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="8e90a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8e90a-104">SYNTAX</span></span>

### <span data-ttu-id="8e90a-105">DeleteByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="8e90a-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseWorkspace [-ResourceGroupName <String>] -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e90a-106">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e90a-106">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseWorkspace -InputObject <PSSynapseWorkspace> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e90a-107">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e90a-107">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseWorkspace -ResourceId <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e90a-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="8e90a-108">DESCRIPTION</span></span>
<span data-ttu-id="8e90a-109">O cmdlet **Remove-AzSynapseWorkspace** exclui permanentemente um espaço de trabalho do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="8e90a-109">The **Remove-AzSynapseWorkspace** cmdlet permanently deletes an Azure Synapse Analytics workspace.</span></span>

## <span data-ttu-id="8e90a-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8e90a-110">EXAMPLES</span></span>

### <span data-ttu-id="8e90a-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8e90a-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseWorkspace -Name ContosoWorkspace
```

<span data-ttu-id="8e90a-112">Esse comando exclui um espaço de trabalho do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="8e90a-112">This command deletes an Azure Synapse Analytics workspace.</span></span>

### <span data-ttu-id="8e90a-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="8e90a-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseWorkspace
```

<span data-ttu-id="8e90a-114">Esse comando exclui um espaço de trabalho do Azure Synapse Analytics por meio de pipeline.</span><span class="sxs-lookup"><span data-stu-id="8e90a-114">This command deletes an Azure Synapse Analytics workspace through pipeline.</span></span>

### <span data-ttu-id="8e90a-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="8e90a-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzSynapseWorkspace -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace
```

<span data-ttu-id="8e90a-116">Esse comando exclui um espaço de trabalho do Azure Synapse Analytics por meio de pipeline com a ID de recurso especificada.</span><span class="sxs-lookup"><span data-stu-id="8e90a-116">This command deletes an Azure Synapse Analytics workspace through pipeline with the specified resource ID.</span></span>

## <span data-ttu-id="8e90a-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8e90a-117">PARAMETERS</span></span>

### <span data-ttu-id="8e90a-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8e90a-118">-AsJob</span></span>
<span data-ttu-id="8e90a-119">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="8e90a-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8e90a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e90a-120">-DefaultProfile</span></span>
<span data-ttu-id="8e90a-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8e90a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e90a-122">-Forçar</span><span class="sxs-lookup"><span data-stu-id="8e90a-122">-Force</span></span>
<span data-ttu-id="8e90a-123">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="8e90a-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="8e90a-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8e90a-124">-InputObject</span></span>
<span data-ttu-id="8e90a-125">objeto de entrada de espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="8e90a-125">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="8e90a-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="8e90a-126">-Name</span></span>
<span data-ttu-id="8e90a-127">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="8e90a-127">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="8e90a-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8e90a-128">-PassThru</span></span>
<span data-ttu-id="8e90a-129">Este Cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="8e90a-129">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="8e90a-130">Se essa opção for especificada, ela retornará verdadeira se for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="8e90a-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="8e90a-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e90a-131">-ResourceGroupName</span></span>
<span data-ttu-id="8e90a-132">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8e90a-132">Resource group name.</span></span>

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

### <span data-ttu-id="8e90a-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8e90a-133">-ResourceId</span></span>
<span data-ttu-id="8e90a-134">Identificador de recurso do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="8e90a-134">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="8e90a-135">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="8e90a-135">-Confirm</span></span>
<span data-ttu-id="8e90a-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e90a-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e90a-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e90a-137">-WhatIf</span></span>
<span data-ttu-id="8e90a-138">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="8e90a-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e90a-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8e90a-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e90a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e90a-140">CommonParameters</span></span>
<span data-ttu-id="8e90a-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e90a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e90a-142">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8e90a-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e90a-143">Entradas</span><span class="sxs-lookup"><span data-stu-id="8e90a-143">INPUTS</span></span>

### <span data-ttu-id="8e90a-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="8e90a-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="8e90a-145">Saídas</span><span class="sxs-lookup"><span data-stu-id="8e90a-145">OUTPUTS</span></span>

### <span data-ttu-id="8e90a-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8e90a-146">System.Boolean</span></span>

## <span data-ttu-id="8e90a-147">Notas</span><span class="sxs-lookup"><span data-stu-id="8e90a-147">NOTES</span></span>

## <span data-ttu-id="8e90a-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8e90a-148">RELATED LINKS</span></span>
