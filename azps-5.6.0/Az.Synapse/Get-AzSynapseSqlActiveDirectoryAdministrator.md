---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsesqlactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlActiveDirectoryAdministrator.md
ms.openlocfilehash: 1f5c9c619c037c243246f9dec26ae2504a162d9b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901541"
---
# <span data-ttu-id="a9faa-101">Get-AzSynapseSqlActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="a9faa-101">Get-AzSynapseSqlActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="a9faa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9faa-102">SYNOPSIS</span></span>
<span data-ttu-id="a9faa-103">Obtém informações sobre um administrador do Azure AD para o Espaço de Trabalho do Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="a9faa-103">Gets information about an Azure AD administrator for Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="a9faa-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a9faa-104">SYNTAX</span></span>

### <span data-ttu-id="a9faa-105">GetByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a9faa-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlActiveDirectoryAdministrator [-ResourceGroupName <String>] -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9faa-106">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9faa-106">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlActiveDirectoryAdministrator -InputObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9faa-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9faa-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlActiveDirectoryAdministrator -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a9faa-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a9faa-108">DESCRIPTION</span></span>
<span data-ttu-id="a9faa-109">O cmdlet **Get-AzSynapseSqlActiveDirectoryAdministrator** obtém informações sobre um administrador do Azure Active Directory (Azure AD) para um Espaço de Trabalho de Análise do Azure Synapse na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="a9faa-109">The **Get-AzSynapseSqlActiveDirectoryAdministrator** cmdlet gets information about an Azure Active Directory (Azure AD) administrator for an Azure Synapse Analytics Workspace in the current subscription.</span></span>

## <span data-ttu-id="a9faa-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a9faa-110">EXAMPLES</span></span>

### <span data-ttu-id="a9faa-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a9faa-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlActiveDirectoryAdministrator -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="a9faa-112">Este comando obtém informações sobre um administrador do Azure AD para um espaço de trabalho chamado ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="a9faa-112">This command gets information about an Azure AD administrator for a workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="a9faa-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a9faa-113">PARAMETERS</span></span>

### <span data-ttu-id="a9faa-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9faa-114">-DefaultProfile</span></span>
<span data-ttu-id="a9faa-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a9faa-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9faa-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a9faa-116">-InputObject</span></span>
<span data-ttu-id="a9faa-117">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="a9faa-117">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a9faa-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9faa-118">-ResourceGroupName</span></span>
<span data-ttu-id="a9faa-119">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a9faa-119">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9faa-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a9faa-120">-ResourceId</span></span>
<span data-ttu-id="a9faa-121">Identificador de recursos do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="a9faa-121">Resource identifier of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9faa-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a9faa-122">-WorkspaceName</span></span>
<span data-ttu-id="a9faa-123">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="a9faa-123">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9faa-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9faa-124">CommonParameters</span></span>
<span data-ttu-id="a9faa-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9faa-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9faa-126">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a9faa-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9faa-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a9faa-127">INPUTS</span></span>

### <span data-ttu-id="a9faa-128">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="a9faa-128">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="a9faa-129">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a9faa-129">OUTPUTS</span></span>

### <span data-ttu-id="a9faa-130">Microsoft.Azure.Commands.Synapse.Models.PSWorkspaceAadAdminInfo</span><span class="sxs-lookup"><span data-stu-id="a9faa-130">Microsoft.Azure.Commands.Synapse.Models.PSWorkspaceAadAdminInfo</span></span>

## <span data-ttu-id="a9faa-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="a9faa-131">NOTES</span></span>

## <span data-ttu-id="a9faa-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a9faa-132">RELATED LINKS</span></span>
