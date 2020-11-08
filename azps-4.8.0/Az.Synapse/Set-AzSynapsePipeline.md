---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsepipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapsePipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapsePipeline.md
ms.openlocfilehash: 2bce821f55b5f8ff39f56fa8a6960cb1f99b47d0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94112488"
---
# <span data-ttu-id="4bf79-101">Set-AzSynapsePipeline</span><span class="sxs-lookup"><span data-stu-id="4bf79-101">Set-AzSynapsePipeline</span></span>

## <span data-ttu-id="4bf79-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4bf79-102">SYNOPSIS</span></span>
<span data-ttu-id="4bf79-103">Cria um pipeline no espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="4bf79-103">Creates a pipeline in workspace.</span></span>

## <span data-ttu-id="4bf79-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4bf79-104">SYNTAX</span></span>

### <span data-ttu-id="4bf79-105">SetByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="4bf79-105">SetByName (Default)</span></span>
```
Set-AzSynapsePipeline -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4bf79-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="4bf79-106">SetByObject</span></span>
```
Set-AzSynapsePipeline -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4bf79-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4bf79-107">DESCRIPTION</span></span>
<span data-ttu-id="4bf79-108">O cmdlet **set-AzSynapsePipeline** cria um pipeline no espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="4bf79-108">The **Set-AzSynapsePipeline** cmdlet creates a pipeline in workspace.</span></span>

## <span data-ttu-id="4bf79-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4bf79-109">EXAMPLES</span></span>

### <span data-ttu-id="4bf79-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4bf79-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline -DefinitionFile "C:\pipeline.json"
```

<span data-ttu-id="4bf79-111">Esse comando cria um pipeline chamado ContosoPipeline no espaço de trabalho chamado ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="4bf79-111">This command creates a pipeline named ContosoPipeline in the workspace named ContosoWorkspace.</span></span>
<span data-ttu-id="4bf79-112">O comando baseia o pipeline nas informações do pipeline.jsem arquivo.</span><span class="sxs-lookup"><span data-stu-id="4bf79-112">The command bases the pipeline on information in the pipeline.json file.</span></span>
<span data-ttu-id="4bf79-113">Esse arquivo inclui informações sobre atividades.</span><span class="sxs-lookup"><span data-stu-id="4bf79-113">This file includes information about activities.</span></span>

### <span data-ttu-id="4bf79-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="4bf79-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Set-AzSynapsePipeline -Name ContosoPipeline -DefinitionFile "C:\pipeline.json"
```

<span data-ttu-id="4bf79-115">Esse comando cria um pipeline chamado ContosoPipeline no espaço de trabalho chamado ContosoWorkspace pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="4bf79-115">This command creates a pipeline named ContosoPipeline in the workspace named ContosoWorkspace through pipeline.</span></span>
<span data-ttu-id="4bf79-116">O comando baseia o pipeline nas informações do pipeline.jsem arquivo.</span><span class="sxs-lookup"><span data-stu-id="4bf79-116">The command bases the pipeline on information in the pipeline.json file.</span></span>
<span data-ttu-id="4bf79-117">Esse arquivo inclui informações sobre atividades.</span><span class="sxs-lookup"><span data-stu-id="4bf79-117">This file includes information about activities.</span></span>

## <span data-ttu-id="4bf79-118">OS</span><span class="sxs-lookup"><span data-stu-id="4bf79-118">PARAMETERS</span></span>

### <span data-ttu-id="4bf79-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4bf79-119">-AsJob</span></span>
<span data-ttu-id="4bf79-120">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="4bf79-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4bf79-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bf79-121">-DefaultProfile</span></span>
<span data-ttu-id="4bf79-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4bf79-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4bf79-123">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="4bf79-123">-DefinitionFile</span></span>
<span data-ttu-id="4bf79-124">O caminho do arquivo JSON.</span><span class="sxs-lookup"><span data-stu-id="4bf79-124">The JSON file path.</span></span>

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

### <span data-ttu-id="4bf79-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="4bf79-125">-Name</span></span>
<span data-ttu-id="4bf79-126">O nome do pipeline.</span><span class="sxs-lookup"><span data-stu-id="4bf79-126">The pipeline name.</span></span>

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

### <span data-ttu-id="4bf79-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="4bf79-127">-WorkspaceName</span></span>
<span data-ttu-id="4bf79-128">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="4bf79-128">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="4bf79-129">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="4bf79-129">-WorkspaceObject</span></span>
<span data-ttu-id="4bf79-130">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="4bf79-130">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="4bf79-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4bf79-131">-Confirm</span></span>
<span data-ttu-id="4bf79-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4bf79-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4bf79-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4bf79-133">-WhatIf</span></span>
<span data-ttu-id="4bf79-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4bf79-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4bf79-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4bf79-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4bf79-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bf79-136">CommonParameters</span></span>
<span data-ttu-id="4bf79-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4bf79-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bf79-138">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4bf79-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bf79-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4bf79-139">INPUTS</span></span>

### <span data-ttu-id="4bf79-140">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="4bf79-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="4bf79-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4bf79-141">OUTPUTS</span></span>

### <span data-ttu-id="4bf79-142">Microsoft. Azure. Commands. Synapse. Models. PSPipelineResource</span><span class="sxs-lookup"><span data-stu-id="4bf79-142">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span></span>

## <span data-ttu-id="4bf79-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4bf79-143">NOTES</span></span>

## <span data-ttu-id="4bf79-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4bf79-144">RELATED LINKS</span></span>
