---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapselinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseLinkedService.md
ms.openlocfilehash: 635c1e064dbc081a5207f5c912c14166b2b01e17
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94113158"
---
# <span data-ttu-id="9ba7c-101">Set-AzSynapseLinkedService</span><span class="sxs-lookup"><span data-stu-id="9ba7c-101">Set-AzSynapseLinkedService</span></span>

## <span data-ttu-id="9ba7c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9ba7c-102">SYNOPSIS</span></span>
<span data-ttu-id="9ba7c-103">Vincula um repositório de dados ou um serviço na nuvem para o espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="9ba7c-103">Links a data store or a cloud service to workspace.</span></span>

## <span data-ttu-id="9ba7c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9ba7c-104">SYNTAX</span></span>

### <span data-ttu-id="9ba7c-105">SetByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="9ba7c-105">SetByName (Default)</span></span>
```
Set-AzSynapseLinkedService -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ba7c-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="9ba7c-106">SetByObject</span></span>
```
Set-AzSynapseLinkedService -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ba7c-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9ba7c-107">DESCRIPTION</span></span>
<span data-ttu-id="9ba7c-108">O cmdlet **set-AzSynapseLinkedService** vincula um repositório de dados ou um serviço na nuvem ao espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="9ba7c-108">The **Set-AzSynapseLinkedService** cmdlet links a data store or a cloud service to workspace.</span></span>

## <span data-ttu-id="9ba7c-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9ba7c-109">EXAMPLES</span></span>

### <span data-ttu-id="9ba7c-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9ba7c-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseLinkedService -WorkspaceName ContosoWorkspace -Name ContosoLinkedService -DefinitionFile "C:\\samples\\LinkedService.json"
```

<span data-ttu-id="9ba7c-111">Esse comando cria um serviço vinculado chamado ContosoLinkedService no espaço de trabalho chamado ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="9ba7c-111">This command creates a linked service named ContosoLinkedService in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="9ba7c-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="9ba7c-112">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Set-AzSynapseLinkedService -Name ContosoLinkedService -DefinitionFile "C:\\samples\\LinkedService.json"
```

<span data-ttu-id="9ba7c-113">Esse comando cria um serviço vinculado chamado ContosoLinkedService no espaço de trabalho chamado ContosoWorkspace pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="9ba7c-113">This command creates a linked service named ContosoLinkedService in the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="9ba7c-114">OS</span><span class="sxs-lookup"><span data-stu-id="9ba7c-114">PARAMETERS</span></span>

### <span data-ttu-id="9ba7c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9ba7c-115">-AsJob</span></span>
<span data-ttu-id="9ba7c-116">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="9ba7c-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9ba7c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ba7c-117">-DefaultProfile</span></span>
<span data-ttu-id="9ba7c-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9ba7c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ba7c-119">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="9ba7c-119">-DefinitionFile</span></span>
<span data-ttu-id="9ba7c-120">O caminho do arquivo JSON.</span><span class="sxs-lookup"><span data-stu-id="9ba7c-120">The JSON file path.</span></span>

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

### <span data-ttu-id="9ba7c-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="9ba7c-121">-Name</span></span>
<span data-ttu-id="9ba7c-122">O nome do serviço vinculado.</span><span class="sxs-lookup"><span data-stu-id="9ba7c-122">The linked service name.</span></span>

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

### <span data-ttu-id="9ba7c-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9ba7c-123">-WorkspaceName</span></span>
<span data-ttu-id="9ba7c-124">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="9ba7c-124">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="9ba7c-125">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="9ba7c-125">-WorkspaceObject</span></span>
<span data-ttu-id="9ba7c-126">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="9ba7c-126">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="9ba7c-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9ba7c-127">-Confirm</span></span>
<span data-ttu-id="9ba7c-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9ba7c-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ba7c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ba7c-129">-WhatIf</span></span>
<span data-ttu-id="9ba7c-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9ba7c-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ba7c-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9ba7c-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ba7c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ba7c-132">CommonParameters</span></span>
<span data-ttu-id="9ba7c-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ba7c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ba7c-134">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9ba7c-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ba7c-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9ba7c-135">INPUTS</span></span>

### <span data-ttu-id="9ba7c-136">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="9ba7c-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="9ba7c-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9ba7c-137">OUTPUTS</span></span>

### <span data-ttu-id="9ba7c-138">Microsoft. Azure. Commands. Synapse. Models. PSLinkedServiceResource</span><span class="sxs-lookup"><span data-stu-id="9ba7c-138">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span></span>

## <span data-ttu-id="9ba7c-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9ba7c-139">NOTES</span></span>

## <span data-ttu-id="9ba7c-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9ba7c-140">RELATED LINKS</span></span>
