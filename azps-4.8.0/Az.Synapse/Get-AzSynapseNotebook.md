---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsenotebook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseNotebook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseNotebook.md
ms.openlocfilehash: 28a4742b2e744fb41bca9402a8c48b830554e231
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93954506"
---
# <span data-ttu-id="0c89e-101">Get-AzSynapseNotebook</span><span class="sxs-lookup"><span data-stu-id="0c89e-101">Get-AzSynapseNotebook</span></span>

## <span data-ttu-id="0c89e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0c89e-102">SYNOPSIS</span></span>
<span data-ttu-id="0c89e-103">Obtém informações sobre blocos de anotações em um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="0c89e-103">Gets information about notebooks in a workspace.</span></span>

## <span data-ttu-id="0c89e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0c89e-104">SYNTAX</span></span>

### <span data-ttu-id="0c89e-105">GetByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="0c89e-105">GetByName (Default)</span></span>
```
Get-AzSynapseNotebook -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0c89e-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="0c89e-106">GetByObject</span></span>
```
Get-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c89e-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0c89e-107">DESCRIPTION</span></span>
<span data-ttu-id="0c89e-108">O cmdlet **Get-AzSynapseNotebook** Obtém informações sobre blocos de anotações em um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="0c89e-108">The **Get-AzSynapseNotebook** cmdlet gets information about notebooks in a workspace.</span></span> <span data-ttu-id="0c89e-109">Se você especificar o nome de um bloco de anotações, o cmdlet obterá informações sobre esse bloco de anotações.</span><span class="sxs-lookup"><span data-stu-id="0c89e-109">If you specify the name of a notebook, the cmdlet gets information about that notebook.</span></span> <span data-ttu-id="0c89e-110">Se você não especificar um nome, o cmdlet obterá informações sobre todos os blocos de anotações no espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="0c89e-110">If you do not specify a name, the cmdlet gets information about all notebooks in the workspace.</span></span>

## <span data-ttu-id="0c89e-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0c89e-111">EXAMPLES</span></span>

### <span data-ttu-id="0c89e-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0c89e-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseNotebook -WorkspaceName ContosoWorkspace | Format-Table

WorkspaceName    Properties                                         Name
-------------    ----------                                         --
ContosoWorkspace Microsoft.Azure.Commands.Synapse.Models.PSNotebook ContosoNotebook1
ContosoWorkspace Microsoft.Azure.Commands.Synapse.Models.PSNotebook ContosoNotebook2
```

<span data-ttu-id="0c89e-113">Obtém uma lista de todos os blocos de anotações no espaço de trabalho ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="0c89e-113">Gets a list of all notebooks in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="0c89e-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="0c89e-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook
```

<span data-ttu-id="0c89e-115">Obtém um único bloco de anotações chamado ContosoNotebook na ContosoWorkspace do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="0c89e-115">Gets a single notebook called ContosoNotebook in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="0c89e-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="0c89e-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseNotebook -Name ContosoNotebook
```

<span data-ttu-id="0c89e-117">Obtém um único bloco de anotações chamado ContosoNotebook no espaço de trabalho ContosoWorkspace pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="0c89e-117">Gets a single notebook called ContosoNotebook in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="0c89e-118">OS</span><span class="sxs-lookup"><span data-stu-id="0c89e-118">PARAMETERS</span></span>

### <span data-ttu-id="0c89e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c89e-119">-DefaultProfile</span></span>
<span data-ttu-id="0c89e-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0c89e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c89e-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="0c89e-121">-Name</span></span>
<span data-ttu-id="0c89e-122">O nome do bloco de anotações.</span><span class="sxs-lookup"><span data-stu-id="0c89e-122">The notebook name.</span></span>

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

### <span data-ttu-id="0c89e-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="0c89e-123">-WorkspaceName</span></span>
<span data-ttu-id="0c89e-124">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="0c89e-124">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="0c89e-125">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="0c89e-125">-WorkspaceObject</span></span>
<span data-ttu-id="0c89e-126">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="0c89e-126">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="0c89e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c89e-127">CommonParameters</span></span>
<span data-ttu-id="0c89e-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c89e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c89e-129">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0c89e-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c89e-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0c89e-130">INPUTS</span></span>

### <span data-ttu-id="0c89e-131">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="0c89e-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="0c89e-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0c89e-132">OUTPUTS</span></span>

### <span data-ttu-id="0c89e-133">Microsoft. Azure. Commands. Synapse. Models. PSNotebookResource</span><span class="sxs-lookup"><span data-stu-id="0c89e-133">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span></span>

## <span data-ttu-id="0c89e-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0c89e-134">NOTES</span></span>

## <span data-ttu-id="0c89e-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0c89e-135">RELATED LINKS</span></span>
