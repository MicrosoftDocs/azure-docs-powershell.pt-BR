---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsedataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseDataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseDataFlow.md
ms.openlocfilehash: 4147343b01e53050f88429424ca7a9c70aa445c6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94113460"
---
# <span data-ttu-id="9b819-101">Set-AzSynapseDataFlow</span><span class="sxs-lookup"><span data-stu-id="9b819-101">Set-AzSynapseDataFlow</span></span>

## <span data-ttu-id="9b819-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9b819-102">SYNOPSIS</span></span>
<span data-ttu-id="9b819-103">Cria ou atualiza um fluxo de dados no espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="9b819-103">Creates or updates a data flow in workspace.</span></span>

## <span data-ttu-id="9b819-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9b819-104">SYNTAX</span></span>

### <span data-ttu-id="9b819-105">SetByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="9b819-105">SetByName (Default)</span></span>
```
Set-AzSynapseDataFlow -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b819-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="9b819-106">SetByObject</span></span>
```
Set-AzSynapseDataFlow -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b819-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9b819-107">DESCRIPTION</span></span>
<span data-ttu-id="9b819-108">O cmdlet **set-AzSynapseDataFlow** cria um fluxo de dados ou atualiza um fluxo de dados existente no espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="9b819-108">The **Set-AzSynapseDataFlow** cmdlet creates a data flow or updates an existing data flow in workspace.</span></span>

## <span data-ttu-id="9b819-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9b819-109">EXAMPLES</span></span>

### <span data-ttu-id="9b819-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9b819-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseDataFlow -WorkspaceName ContosoWorkspace -Name ContosoDataFlow -DefinitionFile "C:\\samples\\DataFlow.json"
```

<span data-ttu-id="9b819-111">Esse comando cria um fluxo de dados denominado ContosoDataFlow no espaço de trabalho chamado ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="9b819-111">This command creates a data flow named ContosoDataFlow in the workspace named ContosoWorkspace.</span></span>
<span data-ttu-id="9b819-112">O comando baseia o fluxo de dados nas informações na DataFlow.jsem arquivo.</span><span class="sxs-lookup"><span data-stu-id="9b819-112">The command bases the data flow on information in the DataFlow.json file.</span></span>

## <span data-ttu-id="9b819-113">OS</span><span class="sxs-lookup"><span data-stu-id="9b819-113">PARAMETERS</span></span>

### <span data-ttu-id="9b819-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9b819-114">-AsJob</span></span>
<span data-ttu-id="9b819-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="9b819-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9b819-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b819-116">-DefaultProfile</span></span>
<span data-ttu-id="9b819-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9b819-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b819-118">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="9b819-118">-DefinitionFile</span></span>
<span data-ttu-id="9b819-119">O caminho do arquivo JSON.</span><span class="sxs-lookup"><span data-stu-id="9b819-119">The JSON file path.</span></span>

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

### <span data-ttu-id="9b819-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="9b819-120">-Name</span></span>
<span data-ttu-id="9b819-121">O nome do fluxo de dados.</span><span class="sxs-lookup"><span data-stu-id="9b819-121">The data flow name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DataFlowName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b819-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9b819-122">-WorkspaceName</span></span>
<span data-ttu-id="9b819-123">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="9b819-123">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="9b819-124">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="9b819-124">-WorkspaceObject</span></span>
<span data-ttu-id="9b819-125">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="9b819-125">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="9b819-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9b819-126">-Confirm</span></span>
<span data-ttu-id="9b819-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b819-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b819-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b819-128">-WhatIf</span></span>
<span data-ttu-id="9b819-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9b819-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b819-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9b819-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b819-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b819-131">CommonParameters</span></span>
<span data-ttu-id="9b819-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b819-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b819-133">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9b819-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b819-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9b819-134">INPUTS</span></span>

### <span data-ttu-id="9b819-135">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="9b819-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="9b819-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9b819-136">OUTPUTS</span></span>

### <span data-ttu-id="9b819-137">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span><span class="sxs-lookup"><span data-stu-id="9b819-137">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span></span>

## <span data-ttu-id="9b819-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9b819-138">NOTES</span></span>

## <span data-ttu-id="9b819-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9b819-139">RELATED LINKS</span></span>
