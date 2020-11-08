---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseWorkspace.md
ms.openlocfilehash: dcc73c78334fba9823ddc1d26463422bcc388bf2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94113463"
---
# <span data-ttu-id="636f8-101">Remove-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="636f8-101">Remove-AzSynapseWorkspace</span></span>

## <span data-ttu-id="636f8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="636f8-102">SYNOPSIS</span></span>
<span data-ttu-id="636f8-103">Exclui um espaço de trabalho de análise do Synapse.</span><span class="sxs-lookup"><span data-stu-id="636f8-103">Deletes a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="636f8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="636f8-104">SYNTAX</span></span>

### <span data-ttu-id="636f8-105">DeleteByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="636f8-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseWorkspace [-ResourceGroupName <String>] -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="636f8-106">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="636f8-106">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseWorkspace -InputObject <PSSynapseWorkspace> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="636f8-107">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="636f8-107">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseWorkspace -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="636f8-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="636f8-108">DESCRIPTION</span></span>
<span data-ttu-id="636f8-109">O cmdlet **Remove-AzSynapseWorkspace** exclui permanentemente um espaço de trabalho de análise do Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="636f8-109">The **Remove-AzSynapseWorkspace** cmdlet permanently deletes an Azure Synapse Analytics workspace.</span></span>

## <span data-ttu-id="636f8-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="636f8-110">EXAMPLES</span></span>

### <span data-ttu-id="636f8-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="636f8-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseWorkspace -Name ContosoWorkspace
```

<span data-ttu-id="636f8-112">Esse comando exclui um espaço de trabalho de análise do Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="636f8-112">This command deletes an Azure Synapse Analytics workspace.</span></span>

### <span data-ttu-id="636f8-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="636f8-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseWorkspace
```

<span data-ttu-id="636f8-114">Esse comando exclui um espaço de trabalho de análise do Azure Synapse por meio do pipeline.</span><span class="sxs-lookup"><span data-stu-id="636f8-114">This command deletes an Azure Synapse Analytics workspace through pipeline.</span></span>

### <span data-ttu-id="636f8-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="636f8-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzSynapseWorkspace -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace
```

<span data-ttu-id="636f8-116">Esse comando exclui um espaço de trabalho de análise do Azure Synapse por meio do pipeline com a ID de recurso especificada.</span><span class="sxs-lookup"><span data-stu-id="636f8-116">This command deletes an Azure Synapse Analytics workspace through pipeline with the specified resource ID.</span></span>

## <span data-ttu-id="636f8-117">OS</span><span class="sxs-lookup"><span data-stu-id="636f8-117">PARAMETERS</span></span>

### <span data-ttu-id="636f8-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="636f8-118">-AsJob</span></span>
<span data-ttu-id="636f8-119">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="636f8-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="636f8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="636f8-120">-DefaultProfile</span></span>
<span data-ttu-id="636f8-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="636f8-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="636f8-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="636f8-122">-InputObject</span></span>
<span data-ttu-id="636f8-123">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="636f8-123">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="636f8-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="636f8-124">-Name</span></span>
<span data-ttu-id="636f8-125">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="636f8-125">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="636f8-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="636f8-126">-PassThru</span></span>
<span data-ttu-id="636f8-127">Esse cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="636f8-127">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="636f8-128">Se essa opção for especificada, retornará true se for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="636f8-128">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="636f8-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="636f8-129">-ResourceGroupName</span></span>
<span data-ttu-id="636f8-130">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="636f8-130">Resource group name.</span></span>

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

### <span data-ttu-id="636f8-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="636f8-131">-ResourceId</span></span>
<span data-ttu-id="636f8-132">Identificador de recurso do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="636f8-132">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="636f8-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="636f8-133">-Confirm</span></span>
<span data-ttu-id="636f8-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="636f8-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="636f8-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="636f8-135">-WhatIf</span></span>
<span data-ttu-id="636f8-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="636f8-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="636f8-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="636f8-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="636f8-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="636f8-138">CommonParameters</span></span>
<span data-ttu-id="636f8-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="636f8-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="636f8-140">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="636f8-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="636f8-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="636f8-141">INPUTS</span></span>

### <span data-ttu-id="636f8-142">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="636f8-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="636f8-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="636f8-143">OUTPUTS</span></span>

### <span data-ttu-id="636f8-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="636f8-144">System.Boolean</span></span>

## <span data-ttu-id="636f8-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="636f8-145">NOTES</span></span>

## <span data-ttu-id="636f8-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="636f8-146">RELATED LINKS</span></span>
