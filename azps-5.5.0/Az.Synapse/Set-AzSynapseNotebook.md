---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsenotebook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseNotebook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseNotebook.md
ms.openlocfilehash: da4907200bef198afa1d57b51069c6379d28c8f1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113912"
---
# <span data-ttu-id="62480-101">Set-AzSynapseNotebook</span><span class="sxs-lookup"><span data-stu-id="62480-101">Set-AzSynapseNotebook</span></span>

## <span data-ttu-id="62480-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="62480-102">SYNOPSIS</span></span>
<span data-ttu-id="62480-103">Cria ou atualiza um bloco de anotações em um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="62480-103">Creates or updates a notebook in a workspace.</span></span>

## <span data-ttu-id="62480-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="62480-104">SYNTAX</span></span>

### <span data-ttu-id="62480-105">SetByName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="62480-105">SetByName (Default)</span></span>
```
Set-AzSynapseNotebook -WorkspaceName <String> [-Name <String>] -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62480-106">SetByNameAndSparkPool</span><span class="sxs-lookup"><span data-stu-id="62480-106">SetByNameAndSparkPool</span></span>
```
Set-AzSynapseNotebook -WorkspaceName <String> [-Name <String>] -SparkPoolName <String> [-ExecutorSize <String>]
 -ExecutorCount <Int32> -DefinitionFile <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62480-107">SetByObject</span><span class="sxs-lookup"><span data-stu-id="62480-107">SetByObject</span></span>
```
Set-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> [-Name <String>] -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62480-108">SetByObjectAndSparkPool</span><span class="sxs-lookup"><span data-stu-id="62480-108">SetByObjectAndSparkPool</span></span>
```
Set-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> [-Name <String>] -SparkPoolName <String>
 [-ExecutorSize <String>] -ExecutorCount <Int32> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62480-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="62480-109">DESCRIPTION</span></span>
<span data-ttu-id="62480-110">O **cmdlet Set-AzSynapseNotebook** cria ou atualiza um bloco de anotações em um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="62480-110">The **Set-AzSynapseNotebook** cmdlet creates or updates a notebook in a workspace.</span></span>

## <span data-ttu-id="62480-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="62480-111">EXAMPLES</span></span>

### <span data-ttu-id="62480-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="62480-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseNotebook -WorkspaceName ContosoWorkspace -DefinitionFile "C:\\samples\\notebook.ipynb"

    WorkspaceName : ContosoWorkspace
    Properties    : Microsoft.Azure.Commands.Synapse.Models.PSNotebook
    Name          : notebook
```

<span data-ttu-id="62480-113">Esse comando cria ou atualiza um bloco de anotações do bloco de anotações.ipynb no espaço de trabalho chamado ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="62480-113">This command creates or updates a notebook from notebook file notebook.ipynb in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="62480-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="62480-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Set-AzSynapseNotebook -DefinitionFile "C:\\samples\\notebook.ipynb"
```

<span data-ttu-id="62480-115">Esse comando cria ou atualiza um bloco de anotações do bloco de anotações.ipynb no espaço de trabalho chamado ContosoWorkspace por meio de pipeline.</span><span class="sxs-lookup"><span data-stu-id="62480-115">This command creates or updates a notebook from notebook file notebook.ipynb in the workspace named ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="62480-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="62480-116">Example 3</span></span>
```powershell
PS C:\> Set-AzSynapseNotebook -WorkspaceName ContosoWorkspace -DefinitionFile "C:\\samples\\notebook.ipynb" -SparkPoolName ContosoSparkPool -ExecutorCount 2
```

<span data-ttu-id="62480-117">Esse comando cria ou atualiza um bloco de anotações do bloco de anotações.ipynb que é anexado à ContosoSparkPool e usa 2 laptops no espaço de trabalho chamado ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="62480-117">This command creates or updates a notebook from notebook file notebook.ipynb which attaches to ContosoSparkPool and uses 2 executors in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="62480-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="62480-118">PARAMETERS</span></span>

### <span data-ttu-id="62480-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="62480-119">-AsJob</span></span>
<span data-ttu-id="62480-120">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="62480-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="62480-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62480-121">-DefaultProfile</span></span>
<span data-ttu-id="62480-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="62480-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62480-123">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="62480-123">-DefinitionFile</span></span>
<span data-ttu-id="62480-124">O caminho do arquivo JSON.</span><span class="sxs-lookup"><span data-stu-id="62480-124">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62480-125">-IndemenCount</span><span class="sxs-lookup"><span data-stu-id="62480-125">-ExecutorCount</span></span>
<span data-ttu-id="62480-126">Número de casais a serem alocadas no pool de Spark especificado para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="62480-126">Number of executors to be allocated in the specified Spark pool for the job.</span></span>

```yaml
Type: System.Int32
Parameter Sets: SetByNameAndSparkPool, SetByObjectAndSparkPool
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62480-127">-WidgetSize</span><span class="sxs-lookup"><span data-stu-id="62480-127">-ExecutorSize</span></span>
<span data-ttu-id="62480-128">Número de núcleo e memória a serem usados para os que foram alocados no Pool de Spark especificado para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="62480-128">Number of core and memory to be used for executors allocated in the specified Spark pool for the job.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndSparkPool, SetByObjectAndSparkPool
Aliases:
Accepted values: Small, Medium, Large

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62480-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="62480-129">-Name</span></span>
<span data-ttu-id="62480-130">O nome do bloco de anotações.</span><span class="sxs-lookup"><span data-stu-id="62480-130">The notebook name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NotebookName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62480-131">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="62480-131">-SparkPoolName</span></span>
<span data-ttu-id="62480-132">Nome do pool de miniapse.</span><span class="sxs-lookup"><span data-stu-id="62480-132">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndSparkPool, SetByObjectAndSparkPool
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62480-133">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="62480-133">-WorkspaceName</span></span>
<span data-ttu-id="62480-134">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="62480-134">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByNameAndSparkPool
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62480-135">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="62480-135">-WorkspaceObject</span></span>
<span data-ttu-id="62480-136">objeto de entrada de espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="62480-136">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByObject, SetByObjectAndSparkPool
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="62480-137">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="62480-137">-Confirm</span></span>
<span data-ttu-id="62480-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62480-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62480-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62480-139">-WhatIf</span></span>
<span data-ttu-id="62480-140">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="62480-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62480-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="62480-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62480-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62480-142">CommonParameters</span></span>
<span data-ttu-id="62480-143">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62480-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62480-144">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="62480-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62480-145">Entradas</span><span class="sxs-lookup"><span data-stu-id="62480-145">INPUTS</span></span>

### <span data-ttu-id="62480-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="62480-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="62480-147">Saídas</span><span class="sxs-lookup"><span data-stu-id="62480-147">OUTPUTS</span></span>

### <span data-ttu-id="62480-148">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span><span class="sxs-lookup"><span data-stu-id="62480-148">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span></span>

## <span data-ttu-id="62480-149">Notas</span><span class="sxs-lookup"><span data-stu-id="62480-149">NOTES</span></span>

## <span data-ttu-id="62480-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="62480-150">RELATED LINKS</span></span>
