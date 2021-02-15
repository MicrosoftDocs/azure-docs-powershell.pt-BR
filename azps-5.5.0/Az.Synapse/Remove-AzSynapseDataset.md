---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseDataset.md
ms.openlocfilehash: 68da67d2a29b6f05ed50adc9eb8aef343a7e973b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112400"
---
# <span data-ttu-id="7bbe3-101">Remove-AzSynapseDataset</span><span class="sxs-lookup"><span data-stu-id="7bbe3-101">Remove-AzSynapseDataset</span></span>

## <span data-ttu-id="7bbe3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7bbe3-102">SYNOPSIS</span></span>
<span data-ttu-id="7bbe3-103">Remove um conjuntos de dados do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="7bbe3-103">Removes a dataset from workspace.</span></span>

## <span data-ttu-id="7bbe3-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7bbe3-104">SYNTAX</span></span>

### <span data-ttu-id="7bbe3-105">RemoveByName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="7bbe3-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseDataset -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7bbe3-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="7bbe3-106">RemoveByObject</span></span>
```
Remove-AzSynapseDataset -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7bbe3-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="7bbe3-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseDataset -InputObject <PSDatasetResource> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7bbe3-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="7bbe3-108">DESCRIPTION</span></span>
<span data-ttu-id="7bbe3-109">O **cmdlet Remove-AzSynapseDataset** remove um conjuntos de dados do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="7bbe3-109">The **Remove-AzSynapseDataset** cmdlet removes a dataset from workspace.</span></span>

## <span data-ttu-id="7bbe3-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7bbe3-110">EXAMPLES</span></span>

### <span data-ttu-id="7bbe3-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7bbe3-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseDataset -WorkspaceName ContosoWorkspace -Name ContosoDataset
```

<span data-ttu-id="7bbe3-112">Esse comando remove o conjuntos de dados chamado ContosoDataset do espaço de trabalho chamado ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="7bbe3-112">This command removes the dataset named ContosoDataset from the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="7bbe3-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7bbe3-113">PARAMETERS</span></span>

### <span data-ttu-id="7bbe3-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7bbe3-114">-AsJob</span></span>
<span data-ttu-id="7bbe3-115">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="7bbe3-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7bbe3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bbe3-116">-DefaultProfile</span></span>
<span data-ttu-id="7bbe3-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7bbe3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7bbe3-118">-Forçar</span><span class="sxs-lookup"><span data-stu-id="7bbe3-118">-Force</span></span>
<span data-ttu-id="7bbe3-119">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="7bbe3-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="7bbe3-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7bbe3-120">-InputObject</span></span>
<span data-ttu-id="7bbe3-121">O objeto de conjuntos de dados.</span><span class="sxs-lookup"><span data-stu-id="7bbe3-121">The dataset object.</span></span>

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

### <span data-ttu-id="7bbe3-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="7bbe3-122">-Name</span></span>
<span data-ttu-id="7bbe3-123">O nome do conjuntos de dados.</span><span class="sxs-lookup"><span data-stu-id="7bbe3-123">The dataset name.</span></span>

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

### <span data-ttu-id="7bbe3-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7bbe3-124">-PassThru</span></span>
<span data-ttu-id="7bbe3-125">Este Cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="7bbe3-125">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="7bbe3-126">Se essa opção for especificada, ela retornará verdadeira se for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="7bbe3-126">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="7bbe3-127">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="7bbe3-127">-WorkspaceName</span></span>
<span data-ttu-id="7bbe3-128">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="7bbe3-128">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="7bbe3-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="7bbe3-129">-WorkspaceObject</span></span>
<span data-ttu-id="7bbe3-130">objeto de entrada de espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="7bbe3-130">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="7bbe3-131">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="7bbe3-131">-Confirm</span></span>
<span data-ttu-id="7bbe3-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7bbe3-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7bbe3-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7bbe3-133">-WhatIf</span></span>
<span data-ttu-id="7bbe3-134">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="7bbe3-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7bbe3-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7bbe3-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7bbe3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bbe3-136">CommonParameters</span></span>
<span data-ttu-id="7bbe3-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7bbe3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bbe3-138">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7bbe3-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bbe3-139">Entradas</span><span class="sxs-lookup"><span data-stu-id="7bbe3-139">INPUTS</span></span>

### <span data-ttu-id="7bbe3-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="7bbe3-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="7bbe3-141">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span><span class="sxs-lookup"><span data-stu-id="7bbe3-141">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span></span>

## <span data-ttu-id="7bbe3-142">Saídas</span><span class="sxs-lookup"><span data-stu-id="7bbe3-142">OUTPUTS</span></span>

### <span data-ttu-id="7bbe3-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7bbe3-143">System.Boolean</span></span>

## <span data-ttu-id="7bbe3-144">Notas</span><span class="sxs-lookup"><span data-stu-id="7bbe3-144">NOTES</span></span>

## <span data-ttu-id="7bbe3-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7bbe3-145">RELATED LINKS</span></span>
