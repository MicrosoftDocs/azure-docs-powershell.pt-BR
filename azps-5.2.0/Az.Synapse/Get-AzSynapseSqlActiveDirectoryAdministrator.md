---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlActiveDirectoryAdministrator.md
ms.openlocfilehash: d3ea1a67d8afa15549c19d6099dc727aab43adc5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98258389"
---
# <span data-ttu-id="01024-101">Get-AzSynapseSqlActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="01024-101">Get-AzSynapseSqlActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="01024-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="01024-102">SYNOPSIS</span></span>
<span data-ttu-id="01024-103">Obtém informações sobre um administrador do Azure AD para Synapse de trabalho de análise.</span><span class="sxs-lookup"><span data-stu-id="01024-103">Gets information about an Azure AD administrator for Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="01024-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="01024-104">SYNTAX</span></span>

### <span data-ttu-id="01024-105">GetByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="01024-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlActiveDirectoryAdministrator [-ResourceGroupName <String>] -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="01024-106">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="01024-106">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlActiveDirectoryAdministrator -InputObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="01024-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="01024-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlActiveDirectoryAdministrator -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="01024-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="01024-108">DESCRIPTION</span></span>
<span data-ttu-id="01024-109">O cmdlet **Get-AzSynapseSqlActiveDirectoryAdministrator** Obtém informações sobre um administrador do Azure Active Directory (Azure AD) para um espaço de trabalho de análise do Azure Synapse na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="01024-109">The **Get-AzSynapseSqlActiveDirectoryAdministrator** cmdlet gets information about an Azure Active Directory (Azure AD) administrator for an Azure Synapse Analytics Workspace in the current subscription.</span></span>

## <span data-ttu-id="01024-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="01024-110">EXAMPLES</span></span>

### <span data-ttu-id="01024-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="01024-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlActiveDirectoryAdministrator -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="01024-112">Esse comando obtém informações sobre um administrador do Azure AD para um espaço de trabalho chamado ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="01024-112">This command gets information about an Azure AD administrator for a workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="01024-113">OS</span><span class="sxs-lookup"><span data-stu-id="01024-113">PARAMETERS</span></span>

### <span data-ttu-id="01024-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01024-114">-DefaultProfile</span></span>
<span data-ttu-id="01024-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="01024-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01024-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="01024-116">-InputObject</span></span>
<span data-ttu-id="01024-117">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="01024-117">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="01024-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01024-118">-ResourceGroupName</span></span>
<span data-ttu-id="01024-119">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="01024-119">Resource group name.</span></span>

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

### <span data-ttu-id="01024-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="01024-120">-ResourceId</span></span>
<span data-ttu-id="01024-121">Identificador de recurso do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="01024-121">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="01024-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="01024-122">-WorkspaceName</span></span>
<span data-ttu-id="01024-123">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="01024-123">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="01024-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01024-124">CommonParameters</span></span>
<span data-ttu-id="01024-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01024-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01024-126">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="01024-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01024-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="01024-127">INPUTS</span></span>

### <span data-ttu-id="01024-128">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="01024-128">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="01024-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="01024-129">OUTPUTS</span></span>

### <span data-ttu-id="01024-130">Microsoft. Azure. Commands. Synapse. Models. PSWorkspaceAadAdminInfo</span><span class="sxs-lookup"><span data-stu-id="01024-130">Microsoft.Azure.Commands.Synapse.Models.PSWorkspaceAadAdminInfo</span></span>

## <span data-ttu-id="01024-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="01024-131">NOTES</span></span>

## <span data-ttu-id="01024-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="01024-132">RELATED LINKS</span></span>
