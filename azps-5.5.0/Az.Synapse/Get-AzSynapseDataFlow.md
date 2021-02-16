---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsedataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDataFlow.md
ms.openlocfilehash: 87627738967a5c3174020932e5c9e7b996980ee9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116317"
---
# <span data-ttu-id="8d4ea-101">Get-AzSynapseDataFlow</span><span class="sxs-lookup"><span data-stu-id="8d4ea-101">Get-AzSynapseDataFlow</span></span>

## <span data-ttu-id="8d4ea-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8d4ea-102">SYNOPSIS</span></span>
<span data-ttu-id="8d4ea-103">Obtém informações sobre fluxos de dados no espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="8d4ea-103">Gets information about data flows in workspace.</span></span>

## <span data-ttu-id="8d4ea-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8d4ea-104">SYNTAX</span></span>

### <span data-ttu-id="8d4ea-105">GetByName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="8d4ea-105">GetByName (Default)</span></span>
```
Get-AzSynapseDataFlow -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8d4ea-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="8d4ea-106">GetByObject</span></span>
```
Get-AzSynapseDataFlow -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8d4ea-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="8d4ea-107">DESCRIPTION</span></span>
<span data-ttu-id="8d4ea-108">O **cmdlet Get-AzSynapseDataFlow** obtém informações sobre fluxos de dados no espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="8d4ea-108">The **Get-AzSynapseDataFlow** cmdlet gets information about data flows in workspace.</span></span>
<span data-ttu-id="8d4ea-109">Se você especificar o nome de um fluxo de dados, esse cmdlet obterá informações sobre esse fluxo de dados.</span><span class="sxs-lookup"><span data-stu-id="8d4ea-109">If you specify the name of a data flow, this cmdlet gets information about that data flow.</span></span>
<span data-ttu-id="8d4ea-110">Se você não especificar um nome, esse cmdlet obterá informações sobre todos os fluxos de dados no espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="8d4ea-110">If you do not specify a name, this cmdlet gets information about all the data flows in the workspace.</span></span>

## <span data-ttu-id="8d4ea-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8d4ea-111">EXAMPLES</span></span>

### <span data-ttu-id="8d4ea-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8d4ea-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseDataFlow -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="8d4ea-113">Esse comando obtém informações sobre todos os fluxos de dados no espaço de trabalho chamado ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="8d4ea-113">This command gets information about all data flows in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="8d4ea-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="8d4ea-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseDataFlow -WorkspaceName ContosoWorkspace -Name ContosoDataFlow
```

<span data-ttu-id="8d4ea-115">Esse comando obtém informações sobre o fluxo de dados chamado ContosoDataFlow no espaço de trabalho chamado ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="8d4ea-115">This command gets information about the data flow named ContosoDataFlow in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="8d4ea-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8d4ea-116">PARAMETERS</span></span>

### <span data-ttu-id="8d4ea-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d4ea-117">-DefaultProfile</span></span>
<span data-ttu-id="8d4ea-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8d4ea-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d4ea-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="8d4ea-119">-Name</span></span>
<span data-ttu-id="8d4ea-120">O nome do fluxo de dados.</span><span class="sxs-lookup"><span data-stu-id="8d4ea-120">The data flow name.</span></span>

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

### <span data-ttu-id="8d4ea-121">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="8d4ea-121">-WorkspaceName</span></span>
<span data-ttu-id="8d4ea-122">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="8d4ea-122">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="8d4ea-123">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="8d4ea-123">-WorkspaceObject</span></span>
<span data-ttu-id="8d4ea-124">objeto de entrada de espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="8d4ea-124">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="8d4ea-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d4ea-125">CommonParameters</span></span>
<span data-ttu-id="8d4ea-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d4ea-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d4ea-127">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8d4ea-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d4ea-128">Entradas</span><span class="sxs-lookup"><span data-stu-id="8d4ea-128">INPUTS</span></span>

### <span data-ttu-id="8d4ea-129">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="8d4ea-129">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="8d4ea-130">Saídas</span><span class="sxs-lookup"><span data-stu-id="8d4ea-130">OUTPUTS</span></span>

### <span data-ttu-id="8d4ea-131">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span><span class="sxs-lookup"><span data-stu-id="8d4ea-131">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span></span>

## <span data-ttu-id="8d4ea-132">Notas</span><span class="sxs-lookup"><span data-stu-id="8d4ea-132">NOTES</span></span>

## <span data-ttu-id="8d4ea-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8d4ea-133">RELATED LINKS</span></span>
