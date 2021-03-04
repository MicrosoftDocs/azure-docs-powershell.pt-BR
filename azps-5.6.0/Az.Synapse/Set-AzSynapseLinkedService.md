---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/set-azsynapselinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseLinkedService.md
ms.openlocfilehash: 1e05754245b4179d02c144538473fa586531f95c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892587"
---
# <span data-ttu-id="ec92b-101">Set-AzSynapseLinkedService</span><span class="sxs-lookup"><span data-stu-id="ec92b-101">Set-AzSynapseLinkedService</span></span>

## <span data-ttu-id="ec92b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec92b-102">SYNOPSIS</span></span>
<span data-ttu-id="ec92b-103">Vincula um armazenamento de dados ou um serviço de nuvem ao espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="ec92b-103">Links a data store or a cloud service to workspace.</span></span>

## <span data-ttu-id="ec92b-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ec92b-104">SYNTAX</span></span>

### <span data-ttu-id="ec92b-105">SetByName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ec92b-105">SetByName (Default)</span></span>
```
Set-AzSynapseLinkedService -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec92b-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="ec92b-106">SetByObject</span></span>
```
Set-AzSynapseLinkedService -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec92b-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ec92b-107">DESCRIPTION</span></span>
<span data-ttu-id="ec92b-108">O cmdlet **Set-AzSynapseLinkedService** vincula um armazenamento de dados ou um serviço de nuvem ao espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="ec92b-108">The **Set-AzSynapseLinkedService** cmdlet links a data store or a cloud service to workspace.</span></span>

## <span data-ttu-id="ec92b-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ec92b-109">EXAMPLES</span></span>

### <span data-ttu-id="ec92b-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ec92b-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseLinkedService -WorkspaceName ContosoWorkspace -Name ContosoLinkedService -DefinitionFile "C:\\samples\\LinkedService.json"
```

<span data-ttu-id="ec92b-111">Este comando cria um serviço vinculado chamado ContosoLinkedService no espaço de trabalho chamado ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="ec92b-111">This command creates a linked service named ContosoLinkedService in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="ec92b-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="ec92b-112">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Set-AzSynapseLinkedService -Name ContosoLinkedService -DefinitionFile "C:\\samples\\LinkedService.json"
```

<span data-ttu-id="ec92b-113">Este comando cria um serviço vinculado chamado ContosoLinkedService no espaço de trabalho chamado ContosoWorkspace por pipeline.</span><span class="sxs-lookup"><span data-stu-id="ec92b-113">This command creates a linked service named ContosoLinkedService in the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="ec92b-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ec92b-114">PARAMETERS</span></span>

### <span data-ttu-id="ec92b-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ec92b-115">-AsJob</span></span>
<span data-ttu-id="ec92b-116">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="ec92b-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ec92b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec92b-117">-DefaultProfile</span></span>
<span data-ttu-id="ec92b-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ec92b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec92b-119">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="ec92b-119">-DefinitionFile</span></span>
<span data-ttu-id="ec92b-120">O caminho do arquivo JSON.</span><span class="sxs-lookup"><span data-stu-id="ec92b-120">The JSON file path.</span></span>

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

### <span data-ttu-id="ec92b-121">-Name</span><span class="sxs-lookup"><span data-stu-id="ec92b-121">-Name</span></span>
<span data-ttu-id="ec92b-122">O nome do serviço vinculado.</span><span class="sxs-lookup"><span data-stu-id="ec92b-122">The linked service name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: LinkedServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec92b-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ec92b-123">-WorkspaceName</span></span>
<span data-ttu-id="ec92b-124">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="ec92b-124">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="ec92b-125">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="ec92b-125">-WorkspaceObject</span></span>
<span data-ttu-id="ec92b-126">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="ec92b-126">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="ec92b-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ec92b-127">-Confirm</span></span>
<span data-ttu-id="ec92b-128">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ec92b-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec92b-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec92b-129">-WhatIf</span></span>
<span data-ttu-id="ec92b-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ec92b-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec92b-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ec92b-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec92b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec92b-132">CommonParameters</span></span>
<span data-ttu-id="ec92b-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec92b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec92b-134">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ec92b-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec92b-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ec92b-135">INPUTS</span></span>

### <span data-ttu-id="ec92b-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="ec92b-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="ec92b-137">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ec92b-137">OUTPUTS</span></span>

### <span data-ttu-id="ec92b-138">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span><span class="sxs-lookup"><span data-stu-id="ec92b-138">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span></span>

## <span data-ttu-id="ec92b-139">NOTES</span><span class="sxs-lookup"><span data-stu-id="ec92b-139">NOTES</span></span>

## <span data-ttu-id="ec92b-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ec92b-140">RELATED LINKS</span></span>
