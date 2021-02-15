---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsepipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapsePipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapsePipeline.md
ms.openlocfilehash: 2bce821f55b5f8ff39f56fa8a6960cb1f99b47d0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113910"
---
# <span data-ttu-id="551d1-101">Set-AzSynapsePipeline</span><span class="sxs-lookup"><span data-stu-id="551d1-101">Set-AzSynapsePipeline</span></span>

## <span data-ttu-id="551d1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="551d1-102">SYNOPSIS</span></span>
<span data-ttu-id="551d1-103">Cria um pipeline no espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="551d1-103">Creates a pipeline in workspace.</span></span>

## <span data-ttu-id="551d1-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="551d1-104">SYNTAX</span></span>

### <span data-ttu-id="551d1-105">SetByName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="551d1-105">SetByName (Default)</span></span>
```
Set-AzSynapsePipeline -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="551d1-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="551d1-106">SetByObject</span></span>
```
Set-AzSynapsePipeline -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="551d1-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="551d1-107">DESCRIPTION</span></span>
<span data-ttu-id="551d1-108">O cmdlet **Set-AzSynapse Pipelineline** cria um pipeline no espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="551d1-108">The **Set-AzSynapsePipeline** cmdlet creates a pipeline in workspace.</span></span>

## <span data-ttu-id="551d1-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="551d1-109">EXAMPLES</span></span>

### <span data-ttu-id="551d1-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="551d1-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline -DefinitionFile "C:\pipeline.json"
```

<span data-ttu-id="551d1-111">Esse comando cria um pipeline chamado ContosoSpaceline no espaço de trabalho chamado ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="551d1-111">This command creates a pipeline named ContosoPipeline in the workspace named ContosoWorkspace.</span></span>
<span data-ttu-id="551d1-112">O comando baseia o pipeline em informações no pipeline.jsno arquivo.</span><span class="sxs-lookup"><span data-stu-id="551d1-112">The command bases the pipeline on information in the pipeline.json file.</span></span>
<span data-ttu-id="551d1-113">Este arquivo inclui informações sobre atividades.</span><span class="sxs-lookup"><span data-stu-id="551d1-113">This file includes information about activities.</span></span>

### <span data-ttu-id="551d1-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="551d1-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Set-AzSynapsePipeline -Name ContosoPipeline -DefinitionFile "C:\pipeline.json"
```

<span data-ttu-id="551d1-115">Esse comando cria um pipeline chamado Contoso Pipeline no espaço de trabalho chamado ContosoWorkspace por meio de pipeline.</span><span class="sxs-lookup"><span data-stu-id="551d1-115">This command creates a pipeline named ContosoPipeline in the workspace named ContosoWorkspace through pipeline.</span></span>
<span data-ttu-id="551d1-116">O comando baseia o pipeline em informações no pipeline.jsno arquivo.</span><span class="sxs-lookup"><span data-stu-id="551d1-116">The command bases the pipeline on information in the pipeline.json file.</span></span>
<span data-ttu-id="551d1-117">Este arquivo inclui informações sobre atividades.</span><span class="sxs-lookup"><span data-stu-id="551d1-117">This file includes information about activities.</span></span>

## <span data-ttu-id="551d1-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="551d1-118">PARAMETERS</span></span>

### <span data-ttu-id="551d1-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="551d1-119">-AsJob</span></span>
<span data-ttu-id="551d1-120">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="551d1-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="551d1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="551d1-121">-DefaultProfile</span></span>
<span data-ttu-id="551d1-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="551d1-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="551d1-123">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="551d1-123">-DefinitionFile</span></span>
<span data-ttu-id="551d1-124">O caminho do arquivo JSON.</span><span class="sxs-lookup"><span data-stu-id="551d1-124">The JSON file path.</span></span>

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

### <span data-ttu-id="551d1-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="551d1-125">-Name</span></span>
<span data-ttu-id="551d1-126">O nome do pipeline.</span><span class="sxs-lookup"><span data-stu-id="551d1-126">The pipeline name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PipelineName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="551d1-127">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="551d1-127">-WorkspaceName</span></span>
<span data-ttu-id="551d1-128">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="551d1-128">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="551d1-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="551d1-129">-WorkspaceObject</span></span>
<span data-ttu-id="551d1-130">objeto de entrada de espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="551d1-130">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="551d1-131">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="551d1-131">-Confirm</span></span>
<span data-ttu-id="551d1-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="551d1-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="551d1-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="551d1-133">-WhatIf</span></span>
<span data-ttu-id="551d1-134">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="551d1-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="551d1-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="551d1-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="551d1-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="551d1-136">CommonParameters</span></span>
<span data-ttu-id="551d1-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="551d1-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="551d1-138">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="551d1-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="551d1-139">Entradas</span><span class="sxs-lookup"><span data-stu-id="551d1-139">INPUTS</span></span>

### <span data-ttu-id="551d1-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="551d1-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="551d1-141">Saídas</span><span class="sxs-lookup"><span data-stu-id="551d1-141">OUTPUTS</span></span>

### <span data-ttu-id="551d1-142">Microsoft.Azure.Commands.Synapse.Models.PS ElelineResource</span><span class="sxs-lookup"><span data-stu-id="551d1-142">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span></span>

## <span data-ttu-id="551d1-143">Notas</span><span class="sxs-lookup"><span data-stu-id="551d1-143">NOTES</span></span>

## <span data-ttu-id="551d1-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="551d1-144">RELATED LINKS</span></span>
