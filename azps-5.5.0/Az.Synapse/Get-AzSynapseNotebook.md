---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsenotebook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseNotebook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseNotebook.md
ms.openlocfilehash: 28a4742b2e744fb41bca9402a8c48b830554e231
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118554"
---
# <span data-ttu-id="a2190-101">Get-AzSynapseNotebook</span><span class="sxs-lookup"><span data-stu-id="a2190-101">Get-AzSynapseNotebook</span></span>

## <span data-ttu-id="a2190-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a2190-102">SYNOPSIS</span></span>
<span data-ttu-id="a2190-103">Obtém informações sobre blocos de anotações em um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="a2190-103">Gets information about notebooks in a workspace.</span></span>

## <span data-ttu-id="a2190-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a2190-104">SYNTAX</span></span>

### <span data-ttu-id="a2190-105">GetByName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a2190-105">GetByName (Default)</span></span>
```
Get-AzSynapseNotebook -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a2190-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="a2190-106">GetByObject</span></span>
```
Get-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a2190-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="a2190-107">DESCRIPTION</span></span>
<span data-ttu-id="a2190-108">O **cmdlet Get-AzSynapseNotebook** obtém informações sobre blocos de anotações em um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="a2190-108">The **Get-AzSynapseNotebook** cmdlet gets information about notebooks in a workspace.</span></span> <span data-ttu-id="a2190-109">Se você especificar o nome de um bloco de anotações, o cmdlet obterá informações sobre esse bloco de anotações.</span><span class="sxs-lookup"><span data-stu-id="a2190-109">If you specify the name of a notebook, the cmdlet gets information about that notebook.</span></span> <span data-ttu-id="a2190-110">Se você não especificar um nome, o cmdlet obterá informações sobre todos os blocos de anotações no espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="a2190-110">If you do not specify a name, the cmdlet gets information about all notebooks in the workspace.</span></span>

## <span data-ttu-id="a2190-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a2190-111">EXAMPLES</span></span>

### <span data-ttu-id="a2190-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a2190-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseNotebook -WorkspaceName ContosoWorkspace | Format-Table

WorkspaceName    Properties                                         Name
-------------    ----------                                         --
ContosoWorkspace Microsoft.Azure.Commands.Synapse.Models.PSNotebook ContosoNotebook1
ContosoWorkspace Microsoft.Azure.Commands.Synapse.Models.PSNotebook ContosoNotebook2
```

<span data-ttu-id="a2190-113">Obtém uma lista de todos os blocos de anotações no espaço de trabalho ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="a2190-113">Gets a list of all notebooks in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="a2190-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="a2190-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook
```

<span data-ttu-id="a2190-115">Obtém um único bloco de anotações chamado ContosoNotebook no espaço de trabalho ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="a2190-115">Gets a single notebook called ContosoNotebook in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="a2190-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="a2190-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseNotebook -Name ContosoNotebook
```

<span data-ttu-id="a2190-117">Obtém um único bloco de anotações chamado ContosoNotebook no espaço de trabalho ContosoWorkspace por meio de pipeline.</span><span class="sxs-lookup"><span data-stu-id="a2190-117">Gets a single notebook called ContosoNotebook in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="a2190-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a2190-118">PARAMETERS</span></span>

### <span data-ttu-id="a2190-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2190-119">-DefaultProfile</span></span>
<span data-ttu-id="a2190-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a2190-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2190-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="a2190-121">-Name</span></span>
<span data-ttu-id="a2190-122">O nome do bloco de anotações.</span><span class="sxs-lookup"><span data-stu-id="a2190-122">The notebook name.</span></span>

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

### <span data-ttu-id="a2190-123">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="a2190-123">-WorkspaceName</span></span>
<span data-ttu-id="a2190-124">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="a2190-124">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="a2190-125">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="a2190-125">-WorkspaceObject</span></span>
<span data-ttu-id="a2190-126">objeto de entrada de espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="a2190-126">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="a2190-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2190-127">CommonParameters</span></span>
<span data-ttu-id="a2190-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2190-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2190-129">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a2190-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2190-130">Entradas</span><span class="sxs-lookup"><span data-stu-id="a2190-130">INPUTS</span></span>

### <span data-ttu-id="a2190-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="a2190-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="a2190-132">Saídas</span><span class="sxs-lookup"><span data-stu-id="a2190-132">OUTPUTS</span></span>

### <span data-ttu-id="a2190-133">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span><span class="sxs-lookup"><span data-stu-id="a2190-133">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span></span>

## <span data-ttu-id="a2190-134">Notas</span><span class="sxs-lookup"><span data-stu-id="a2190-134">NOTES</span></span>

## <span data-ttu-id="a2190-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a2190-135">RELATED LINKS</span></span>
