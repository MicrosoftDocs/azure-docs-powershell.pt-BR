---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseRoleDefinition.md
ms.openlocfilehash: f2ac7efad3c08a351e515eccbe519306a89f06a9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118552"
---
# <span data-ttu-id="789df-101">Get-AzSynapseRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="789df-101">Get-AzSynapseRoleDefinition</span></span>

## <span data-ttu-id="789df-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="789df-102">SYNOPSIS</span></span>
<span data-ttu-id="789df-103">Obtém uma definição de função do Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="789df-103">Gets a Synapse Analytics role definition.</span></span>

## <span data-ttu-id="789df-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="789df-104">SYNTAX</span></span>

### <span data-ttu-id="789df-105">GetByWorkspaceNameAndIdParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="789df-105">GetByWorkspaceNameAndIdParameterSet (Default)</span></span>
```
Get-AzSynapseRoleDefinition -WorkspaceName <String> [-Id <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="789df-106">GetByWorkspaceNameAndNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="789df-106">GetByWorkspaceNameAndNameParameterSet</span></span>
```
Get-AzSynapseRoleDefinition -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="789df-107">GetByWorkspaceObjectAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="789df-107">GetByWorkspaceObjectAndIdParameterSet</span></span>
```
Get-AzSynapseRoleDefinition -WorkspaceObject <PSSynapseWorkspace> -Id <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="789df-108">GetByWorkspaceObjectAndNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="789df-108">GetByWorkspaceObjectAndNameParameterSet</span></span>
```
Get-AzSynapseRoleDefinition -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="789df-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="789df-109">DESCRIPTION</span></span>
<span data-ttu-id="789df-110">O cmdlet **Get-AzSynapseRoleDefinition obtém** uma Definição de Função de Análise Synapse do Azure.</span><span class="sxs-lookup"><span data-stu-id="789df-110">The **Get-AzSynapseRoleDefinition** cmdlet gets an Azure Synapse Analytics Role Definition.</span></span>
<span data-ttu-id="789df-111">Se você não especificar um nome de função ou uma ID de função, este cmdlet obtém todas as definições de função.</span><span class="sxs-lookup"><span data-stu-id="789df-111">If you do not specify a role name or a role Id, this cmdlet gets all role definitions.</span></span>

## <span data-ttu-id="789df-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="789df-112">EXAMPLES</span></span>

### <span data-ttu-id="789df-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="789df-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseRoleDefinition -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="789df-114">Esse comando obtém todas as definições de função em um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="789df-114">This command gets all role definitions under a workspace.</span></span>

### <span data-ttu-id="789df-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="789df-115">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseRoleDefinition -WorkspaceName ContosoWorkspace -Name ContosoRole
```

<span data-ttu-id="789df-116">Esse comando obtém a definição de função no espaço de trabalho ContosoWorkspace com o nome ContosoRole.</span><span class="sxs-lookup"><span data-stu-id="789df-116">This command gets the role definition under workspace ContosoWorkspace with name ContosoRole.</span></span>

### <span data-ttu-id="789df-117">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="789df-117">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseRoleDefinition
```

<span data-ttu-id="789df-118">Esse comando obtém todas as definições de função em um espaço de trabalho por meio do pipeline.</span><span class="sxs-lookup"><span data-stu-id="789df-118">This command gets all role definitions under a workspace through pipeline.</span></span>

## <span data-ttu-id="789df-119">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="789df-119">PARAMETERS</span></span>

### <span data-ttu-id="789df-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="789df-120">-DefaultProfile</span></span>
<span data-ttu-id="789df-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="789df-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="789df-122">-ID</span><span class="sxs-lookup"><span data-stu-id="789df-122">-Id</span></span>
<span data-ttu-id="789df-123">ID da Função atribuída ao diretor.</span><span class="sxs-lookup"><span data-stu-id="789df-123">Id of the Role that is assigned to the principal.</span></span>

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

### <span data-ttu-id="789df-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="789df-124">-Name</span></span>
<span data-ttu-id="789df-125">Nome da Função atribuída ao diretor.</span><span class="sxs-lookup"><span data-stu-id="789df-125">Name of the Role that is assigned to the principal.</span></span>

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

### <span data-ttu-id="789df-126">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="789df-126">-WorkspaceName</span></span>
<span data-ttu-id="789df-127">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="789df-127">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="789df-128">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="789df-128">-WorkspaceObject</span></span>
<span data-ttu-id="789df-129">objeto de entrada de espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="789df-129">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="789df-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="789df-130">CommonParameters</span></span>
<span data-ttu-id="789df-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="789df-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="789df-132">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="789df-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="789df-133">Entradas</span><span class="sxs-lookup"><span data-stu-id="789df-133">INPUTS</span></span>

### <span data-ttu-id="789df-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="789df-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="789df-135">Saídas</span><span class="sxs-lookup"><span data-stu-id="789df-135">OUTPUTS</span></span>

### <span data-ttu-id="789df-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseRole</span><span class="sxs-lookup"><span data-stu-id="789df-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseRole</span></span>

## <span data-ttu-id="789df-137">Notas</span><span class="sxs-lookup"><span data-stu-id="789df-137">NOTES</span></span>

## <span data-ttu-id="789df-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="789df-138">RELATED LINKS</span></span>
