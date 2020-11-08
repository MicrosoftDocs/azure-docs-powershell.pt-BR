---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseRoleDefinition.md
ms.openlocfilehash: f2ac7efad3c08a351e515eccbe519306a89f06a9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110726"
---
# <span data-ttu-id="e47bc-101">Get-AzSynapseRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="e47bc-101">Get-AzSynapseRoleDefinition</span></span>

## <span data-ttu-id="e47bc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e47bc-102">SYNOPSIS</span></span>
<span data-ttu-id="e47bc-103">Obtém uma definição de função de análise do Synapse.</span><span class="sxs-lookup"><span data-stu-id="e47bc-103">Gets a Synapse Analytics role definition.</span></span>

## <span data-ttu-id="e47bc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e47bc-104">SYNTAX</span></span>

### <span data-ttu-id="e47bc-105">GetByWorkspaceNameAndIdParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="e47bc-105">GetByWorkspaceNameAndIdParameterSet (Default)</span></span>
```
Get-AzSynapseRoleDefinition -WorkspaceName <String> [-Id <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e47bc-106">GetByWorkspaceNameAndNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e47bc-106">GetByWorkspaceNameAndNameParameterSet</span></span>
```
Get-AzSynapseRoleDefinition -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e47bc-107">GetByWorkspaceObjectAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e47bc-107">GetByWorkspaceObjectAndIdParameterSet</span></span>
```
Get-AzSynapseRoleDefinition -WorkspaceObject <PSSynapseWorkspace> -Id <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e47bc-108">GetByWorkspaceObjectAndNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e47bc-108">GetByWorkspaceObjectAndNameParameterSet</span></span>
```
Get-AzSynapseRoleDefinition -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e47bc-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e47bc-109">DESCRIPTION</span></span>
<span data-ttu-id="e47bc-110">O cmdlet **Get-AzSynapseRoleDefinition** Obtém uma definição de função de análise do Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="e47bc-110">The **Get-AzSynapseRoleDefinition** cmdlet gets an Azure Synapse Analytics Role Definition.</span></span>
<span data-ttu-id="e47bc-111">Se você não especificar um nome de função ou uma ID de função, esse cmdlet obterá todas as definições de função.</span><span class="sxs-lookup"><span data-stu-id="e47bc-111">If you do not specify a role name or a role Id, this cmdlet gets all role definitions.</span></span>

## <span data-ttu-id="e47bc-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e47bc-112">EXAMPLES</span></span>

### <span data-ttu-id="e47bc-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e47bc-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseRoleDefinition -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="e47bc-114">Esse comando obtém todas as definições de função em um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="e47bc-114">This command gets all role definitions under a workspace.</span></span>

### <span data-ttu-id="e47bc-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="e47bc-115">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseRoleDefinition -WorkspaceName ContosoWorkspace -Name ContosoRole
```

<span data-ttu-id="e47bc-116">Esse comando obtém a definição de função em espaço de trabalho ContosoWorkspace com o nome ContosoRole.</span><span class="sxs-lookup"><span data-stu-id="e47bc-116">This command gets the role definition under workspace ContosoWorkspace with name ContosoRole.</span></span>

### <span data-ttu-id="e47bc-117">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="e47bc-117">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseRoleDefinition
```

<span data-ttu-id="e47bc-118">Esse comando obtém todas as definições de função em um espaço de trabalho por pipeline.</span><span class="sxs-lookup"><span data-stu-id="e47bc-118">This command gets all role definitions under a workspace through pipeline.</span></span>

## <span data-ttu-id="e47bc-119">OS</span><span class="sxs-lookup"><span data-stu-id="e47bc-119">PARAMETERS</span></span>

### <span data-ttu-id="e47bc-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e47bc-120">-DefaultProfile</span></span>
<span data-ttu-id="e47bc-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e47bc-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e47bc-122">-ID</span><span class="sxs-lookup"><span data-stu-id="e47bc-122">-Id</span></span>
<span data-ttu-id="e47bc-123">ID da função atribuída à entidade de segurança.</span><span class="sxs-lookup"><span data-stu-id="e47bc-123">Id of the Role that is assigned to the principal.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceObjectAndIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e47bc-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="e47bc-124">-Name</span></span>
<span data-ttu-id="e47bc-125">Nome da função atribuída à entidade de segurança.</span><span class="sxs-lookup"><span data-stu-id="e47bc-125">Name of the Role that is assigned to the principal.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndNameParameterSet, GetByWorkspaceObjectAndNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e47bc-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e47bc-126">-WorkspaceName</span></span>
<span data-ttu-id="e47bc-127">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="e47bc-127">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndIdParameterSet, GetByWorkspaceNameAndNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e47bc-128">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="e47bc-128">-WorkspaceObject</span></span>
<span data-ttu-id="e47bc-129">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="e47bc-129">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByWorkspaceObjectAndIdParameterSet, GetByWorkspaceObjectAndNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e47bc-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e47bc-130">CommonParameters</span></span>
<span data-ttu-id="e47bc-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e47bc-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e47bc-132">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e47bc-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e47bc-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e47bc-133">INPUTS</span></span>

### <span data-ttu-id="e47bc-134">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="e47bc-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="e47bc-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e47bc-135">OUTPUTS</span></span>

### <span data-ttu-id="e47bc-136">Microsoft. Azure. Commands. Synapse. Models. PSSynapseRole</span><span class="sxs-lookup"><span data-stu-id="e47bc-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseRole</span></span>

## <span data-ttu-id="e47bc-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e47bc-137">NOTES</span></span>

## <span data-ttu-id="e47bc-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e47bc-138">RELATED LINKS</span></span>
