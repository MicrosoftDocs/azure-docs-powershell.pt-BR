---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDataset.md
ms.openlocfilehash: 8919c554fb32a102991b9c40236e897662709ccb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116065"
---
# <span data-ttu-id="d3f61-101">Get-AzSynapseDataset</span><span class="sxs-lookup"><span data-stu-id="d3f61-101">Get-AzSynapseDataset</span></span>

## <span data-ttu-id="d3f61-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d3f61-102">SYNOPSIS</span></span>
<span data-ttu-id="d3f61-103">Obtém informações sobre conjuntos de dados no espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="d3f61-103">Gets information about datasets in workspace.</span></span>

## <span data-ttu-id="d3f61-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d3f61-104">SYNTAX</span></span>

### <span data-ttu-id="d3f61-105">GetByName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d3f61-105">GetByName (Default)</span></span>
```
Get-AzSynapseDataset -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d3f61-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="d3f61-106">GetByObject</span></span>
```
Get-AzSynapseDataset -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3f61-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="d3f61-107">DESCRIPTION</span></span>
<span data-ttu-id="d3f61-108">O cmdlet **Get-AzSynapseDataset** obtém informações sobre conjuntos de dados no espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="d3f61-108">The **Get-AzSynapseDataset** cmdlet gets information about datasets in workspace.</span></span>
<span data-ttu-id="d3f61-109">Se você especificar o nome de um conjuntos de dados, esse cmdlet obterá informações sobre esse conjuntos de dados.</span><span class="sxs-lookup"><span data-stu-id="d3f61-109">If you specify the name of a dataset, this cmdlet gets information about that dataset.</span></span>
<span data-ttu-id="d3f61-110">Se você não especificar um nome, esse cmdlet obterá informações sobre todos os conjuntos de dados no espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="d3f61-110">If you do not specify a name, this cmdlet gets information about all the datasets in the workspace.</span></span>

## <span data-ttu-id="d3f61-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d3f61-111">EXAMPLES</span></span>

### <span data-ttu-id="d3f61-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d3f61-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseDataset -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="d3f61-113">Esse comando obtém informações sobre todos os conjuntos de dados no espaço de trabalho chamado ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="d3f61-113">This command gets information about all datasets in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="d3f61-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="d3f61-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseDataset -WorkspaceName ContosoWorkspace -Name ContosoDataset
```

<span data-ttu-id="d3f61-115">Esse comando obtém informações sobre o conjuntos de dados chamado ContosoDataset no espaço de trabalho chamado ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="d3f61-115">This command gets information about the dataset named ContosoDataset in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="d3f61-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d3f61-116">PARAMETERS</span></span>

### <span data-ttu-id="d3f61-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3f61-117">-DefaultProfile</span></span>
<span data-ttu-id="d3f61-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d3f61-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3f61-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="d3f61-119">-Name</span></span>
<span data-ttu-id="d3f61-120">O nome do conjuntos de dados.</span><span class="sxs-lookup"><span data-stu-id="d3f61-120">The dataset name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DatasetName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3f61-121">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="d3f61-121">-WorkspaceName</span></span>
<span data-ttu-id="d3f61-122">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="d3f61-122">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="d3f61-123">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="d3f61-123">-WorkspaceObject</span></span>
<span data-ttu-id="d3f61-124">objeto de entrada de espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="d3f61-124">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="d3f61-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3f61-125">CommonParameters</span></span>
<span data-ttu-id="d3f61-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3f61-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3f61-127">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d3f61-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3f61-128">Entradas</span><span class="sxs-lookup"><span data-stu-id="d3f61-128">INPUTS</span></span>

### <span data-ttu-id="d3f61-129">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="d3f61-129">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="d3f61-130">Saídas</span><span class="sxs-lookup"><span data-stu-id="d3f61-130">OUTPUTS</span></span>

### <span data-ttu-id="d3f61-131">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span><span class="sxs-lookup"><span data-stu-id="d3f61-131">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span></span>

## <span data-ttu-id="d3f61-132">Notas</span><span class="sxs-lookup"><span data-stu-id="d3f61-132">NOTES</span></span>

## <span data-ttu-id="d3f61-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d3f61-133">RELATED LINKS</span></span>
