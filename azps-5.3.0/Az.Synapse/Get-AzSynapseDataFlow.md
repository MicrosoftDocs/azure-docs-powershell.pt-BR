---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsedataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDataFlow.md
ms.openlocfilehash: 87627738967a5c3174020932e5c9e7b996980ee9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98272449"
---
# <span data-ttu-id="127dc-101">Get-AzSynapseDataFlow</span><span class="sxs-lookup"><span data-stu-id="127dc-101">Get-AzSynapseDataFlow</span></span>

## <span data-ttu-id="127dc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="127dc-102">SYNOPSIS</span></span>
<span data-ttu-id="127dc-103">Obtém informações sobre fluxos de dados no espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="127dc-103">Gets information about data flows in workspace.</span></span>

## <span data-ttu-id="127dc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="127dc-104">SYNTAX</span></span>

### <span data-ttu-id="127dc-105">GetByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="127dc-105">GetByName (Default)</span></span>
```
Get-AzSynapseDataFlow -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="127dc-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="127dc-106">GetByObject</span></span>
```
Get-AzSynapseDataFlow -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="127dc-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="127dc-107">DESCRIPTION</span></span>
<span data-ttu-id="127dc-108">O cmdlet **Get-AzSynapseDataFlow** Obtém informações sobre fluxos de dados no espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="127dc-108">The **Get-AzSynapseDataFlow** cmdlet gets information about data flows in workspace.</span></span>
<span data-ttu-id="127dc-109">Se você especificar o nome de um fluxo de dados, esse cmdlet obterá informações sobre esse fluxo de dados.</span><span class="sxs-lookup"><span data-stu-id="127dc-109">If you specify the name of a data flow, this cmdlet gets information about that data flow.</span></span>
<span data-ttu-id="127dc-110">Se você não especificar um nome, esse cmdlet obterá informações sobre todos os fluxos de dados no espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="127dc-110">If you do not specify a name, this cmdlet gets information about all the data flows in the workspace.</span></span>

## <span data-ttu-id="127dc-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="127dc-111">EXAMPLES</span></span>

### <span data-ttu-id="127dc-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="127dc-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseDataFlow -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="127dc-113">Esse comando obtém informações sobre todos os fluxos de dados no espaço de trabalho chamado ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="127dc-113">This command gets information about all data flows in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="127dc-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="127dc-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseDataFlow -WorkspaceName ContosoWorkspace -Name ContosoDataFlow
```

<span data-ttu-id="127dc-115">Esse comando obtém informações sobre o fluxo de dados chamado ContosoDataFlow no espaço de trabalho chamado ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="127dc-115">This command gets information about the data flow named ContosoDataFlow in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="127dc-116">OS</span><span class="sxs-lookup"><span data-stu-id="127dc-116">PARAMETERS</span></span>

### <span data-ttu-id="127dc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="127dc-117">-DefaultProfile</span></span>
<span data-ttu-id="127dc-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="127dc-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="127dc-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="127dc-119">-Name</span></span>
<span data-ttu-id="127dc-120">O nome do fluxo de dados.</span><span class="sxs-lookup"><span data-stu-id="127dc-120">The data flow name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DataFlowName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="127dc-121">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="127dc-121">-WorkspaceName</span></span>
<span data-ttu-id="127dc-122">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="127dc-122">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="127dc-123">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="127dc-123">-WorkspaceObject</span></span>
<span data-ttu-id="127dc-124">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="127dc-124">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="127dc-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="127dc-125">CommonParameters</span></span>
<span data-ttu-id="127dc-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="127dc-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="127dc-127">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="127dc-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="127dc-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="127dc-128">INPUTS</span></span>

### <span data-ttu-id="127dc-129">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="127dc-129">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="127dc-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="127dc-130">OUTPUTS</span></span>

### <span data-ttu-id="127dc-131">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span><span class="sxs-lookup"><span data-stu-id="127dc-131">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span></span>

## <span data-ttu-id="127dc-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="127dc-132">NOTES</span></span>

## <span data-ttu-id="127dc-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="127dc-133">RELATED LINKS</span></span>
