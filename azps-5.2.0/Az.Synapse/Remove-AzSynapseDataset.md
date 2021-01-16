---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseDataset.md
ms.openlocfilehash: 68da67d2a29b6f05ed50adc9eb8aef343a7e973b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98263904"
---
# <span data-ttu-id="fd3f5-101">Remove-AzSynapseDataset</span><span class="sxs-lookup"><span data-stu-id="fd3f5-101">Remove-AzSynapseDataset</span></span>

## <span data-ttu-id="fd3f5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fd3f5-102">SYNOPSIS</span></span>
<span data-ttu-id="fd3f5-103">Remove um conjunto de um conjunto de espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="fd3f5-103">Removes a dataset from workspace.</span></span>

## <span data-ttu-id="fd3f5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fd3f5-104">SYNTAX</span></span>

### <span data-ttu-id="fd3f5-105">RemoveByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="fd3f5-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseDataset -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd3f5-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="fd3f5-106">RemoveByObject</span></span>
```
Remove-AzSynapseDataset -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd3f5-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="fd3f5-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseDataset -InputObject <PSDatasetResource> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd3f5-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fd3f5-108">DESCRIPTION</span></span>
<span data-ttu-id="fd3f5-109">O cmdlet **Remove-AzSynapseDataset** remove um DataSet do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="fd3f5-109">The **Remove-AzSynapseDataset** cmdlet removes a dataset from workspace.</span></span>

## <span data-ttu-id="fd3f5-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fd3f5-110">EXAMPLES</span></span>

### <span data-ttu-id="fd3f5-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fd3f5-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseDataset -WorkspaceName ContosoWorkspace -Name ContosoDataset
```

<span data-ttu-id="fd3f5-112">Esse comando Remove o DataSet chamado ContosoDataset do espaço de trabalho chamado ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="fd3f5-112">This command removes the dataset named ContosoDataset from the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="fd3f5-113">OS</span><span class="sxs-lookup"><span data-stu-id="fd3f5-113">PARAMETERS</span></span>

### <span data-ttu-id="fd3f5-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fd3f5-114">-AsJob</span></span>
<span data-ttu-id="fd3f5-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="fd3f5-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fd3f5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd3f5-116">-DefaultProfile</span></span>
<span data-ttu-id="fd3f5-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fd3f5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd3f5-118">-Force</span><span class="sxs-lookup"><span data-stu-id="fd3f5-118">-Force</span></span>
<span data-ttu-id="fd3f5-119">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="fd3f5-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="fd3f5-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fd3f5-120">-InputObject</span></span>
<span data-ttu-id="fd3f5-121">O objeto DataSet.</span><span class="sxs-lookup"><span data-stu-id="fd3f5-121">The dataset object.</span></span>

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

### <span data-ttu-id="fd3f5-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="fd3f5-122">-Name</span></span>
<span data-ttu-id="fd3f5-123">O nome do DataSet.</span><span class="sxs-lookup"><span data-stu-id="fd3f5-123">The dataset name.</span></span>

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

### <span data-ttu-id="fd3f5-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fd3f5-124">-PassThru</span></span>
<span data-ttu-id="fd3f5-125">Esse cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="fd3f5-125">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="fd3f5-126">Se essa opção for especificada, retornará true se for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="fd3f5-126">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="fd3f5-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="fd3f5-127">-WorkspaceName</span></span>
<span data-ttu-id="fd3f5-128">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="fd3f5-128">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="fd3f5-129">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="fd3f5-129">-WorkspaceObject</span></span>
<span data-ttu-id="fd3f5-130">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="fd3f5-130">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="fd3f5-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="fd3f5-131">-Confirm</span></span>
<span data-ttu-id="fd3f5-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd3f5-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd3f5-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd3f5-133">-WhatIf</span></span>
<span data-ttu-id="fd3f5-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fd3f5-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd3f5-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fd3f5-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd3f5-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd3f5-136">CommonParameters</span></span>
<span data-ttu-id="fd3f5-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd3f5-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd3f5-138">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fd3f5-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd3f5-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fd3f5-139">INPUTS</span></span>

### <span data-ttu-id="fd3f5-140">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="fd3f5-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="fd3f5-141">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span><span class="sxs-lookup"><span data-stu-id="fd3f5-141">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span></span>

## <span data-ttu-id="fd3f5-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fd3f5-142">OUTPUTS</span></span>

### <span data-ttu-id="fd3f5-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fd3f5-143">System.Boolean</span></span>

## <span data-ttu-id="fd3f5-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fd3f5-144">NOTES</span></span>

## <span data-ttu-id="fd3f5-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fd3f5-145">RELATED LINKS</span></span>
