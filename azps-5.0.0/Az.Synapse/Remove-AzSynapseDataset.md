---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseDataset.md
ms.openlocfilehash: 712aa1012269c6207b078fefa3a04a46bea4c573
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94125231"
---
# <span data-ttu-id="dcb9c-101">Remove-AzSynapseDataset</span><span class="sxs-lookup"><span data-stu-id="dcb9c-101">Remove-AzSynapseDataset</span></span>

## <span data-ttu-id="dcb9c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dcb9c-102">SYNOPSIS</span></span>
<span data-ttu-id="dcb9c-103">Remove um conjunto de um conjunto de espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="dcb9c-103">Removes a dataset from workspace.</span></span>

## <span data-ttu-id="dcb9c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dcb9c-104">SYNTAX</span></span>

### <span data-ttu-id="dcb9c-105">RemoveByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="dcb9c-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseDataset -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dcb9c-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="dcb9c-106">RemoveByObject</span></span>
```
Remove-AzSynapseDataset -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dcb9c-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="dcb9c-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseDataset -InputObject <PSDatasetResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dcb9c-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dcb9c-108">DESCRIPTION</span></span>
<span data-ttu-id="dcb9c-109">O cmdlet **Remove-AzSynapseDataset** remove um DataSet do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="dcb9c-109">The **Remove-AzSynapseDataset** cmdlet removes a dataset from workspace.</span></span>

## <span data-ttu-id="dcb9c-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dcb9c-110">EXAMPLES</span></span>

### <span data-ttu-id="dcb9c-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="dcb9c-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseDataset -WorkspaceName ContosoWorkspace -Name ContosoDataset
```

<span data-ttu-id="dcb9c-112">Esse comando Remove o DataSet chamado ContosoDataset do espaço de trabalho chamado ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="dcb9c-112">This command removes the dataset named ContosoDataset from the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="dcb9c-113">OS</span><span class="sxs-lookup"><span data-stu-id="dcb9c-113">PARAMETERS</span></span>

### <span data-ttu-id="dcb9c-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dcb9c-114">-AsJob</span></span>
<span data-ttu-id="dcb9c-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="dcb9c-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dcb9c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcb9c-116">-DefaultProfile</span></span>
<span data-ttu-id="dcb9c-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dcb9c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dcb9c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dcb9c-118">-InputObject</span></span>
<span data-ttu-id="dcb9c-119">O objeto DataSet.</span><span class="sxs-lookup"><span data-stu-id="dcb9c-119">The dataset object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dcb9c-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="dcb9c-120">-Name</span></span>
<span data-ttu-id="dcb9c-121">O nome do DataSet.</span><span class="sxs-lookup"><span data-stu-id="dcb9c-121">The dataset name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName, RemoveByObject
Aliases: DatasetName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcb9c-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dcb9c-122">-PassThru</span></span>
<span data-ttu-id="dcb9c-123">Esse cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="dcb9c-123">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="dcb9c-124">Se essa opção for especificada, retornará true se for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="dcb9c-124">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="dcb9c-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="dcb9c-125">-WorkspaceName</span></span>
<span data-ttu-id="dcb9c-126">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="dcb9c-126">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="dcb9c-127">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="dcb9c-127">-WorkspaceObject</span></span>
<span data-ttu-id="dcb9c-128">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="dcb9c-128">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="dcb9c-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="dcb9c-129">-Confirm</span></span>
<span data-ttu-id="dcb9c-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dcb9c-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dcb9c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dcb9c-131">-WhatIf</span></span>
<span data-ttu-id="dcb9c-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="dcb9c-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dcb9c-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="dcb9c-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dcb9c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcb9c-134">CommonParameters</span></span>
<span data-ttu-id="dcb9c-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dcb9c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcb9c-136">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dcb9c-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcb9c-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dcb9c-137">INPUTS</span></span>

### <span data-ttu-id="dcb9c-138">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="dcb9c-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="dcb9c-139">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span><span class="sxs-lookup"><span data-stu-id="dcb9c-139">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span></span>

## <span data-ttu-id="dcb9c-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dcb9c-140">OUTPUTS</span></span>

### <span data-ttu-id="dcb9c-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dcb9c-141">System.Boolean</span></span>

## <span data-ttu-id="dcb9c-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dcb9c-142">NOTES</span></span>

## <span data-ttu-id="dcb9c-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dcb9c-143">RELATED LINKS</span></span>
