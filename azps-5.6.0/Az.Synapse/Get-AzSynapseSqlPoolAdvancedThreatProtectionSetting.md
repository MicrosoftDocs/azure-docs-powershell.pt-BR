---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsesqlpooladvancedthreatprotectionsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting.md
ms.openlocfilehash: c706de537f4d95603399540342bd3ad52d2b30fc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901535"
---
# <span data-ttu-id="f3c42-101">Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="f3c42-101">Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="f3c42-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3c42-102">SYNOPSIS</span></span>
<span data-ttu-id="f3c42-103">Obtém as configurações avançadas de proteção contra ameaças para SQL pool.</span><span class="sxs-lookup"><span data-stu-id="f3c42-103">Gets the advanced threat protection settings for a SQL pool.</span></span>

## <span data-ttu-id="f3c42-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f3c42-104">SYNTAX</span></span>

### <span data-ttu-id="f3c42-105">GetByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="f3c42-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3c42-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3c42-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3c42-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3c42-107">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting -InputObject <PSSynapseSqlPool>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3c42-108">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3c42-108">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3c42-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f3c42-109">DESCRIPTION</span></span>
<span data-ttu-id="f3c42-110">O cmdlet **Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting** obtém as configurações avançadas de proteção contra ameaças de um pool do Azure Synapse Analytics SQL.</span><span class="sxs-lookup"><span data-stu-id="f3c42-110">The **Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting** cmdlet gets the advanced threat protection settings of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="f3c42-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f3c42-111">EXAMPLES</span></span>

### <span data-ttu-id="f3c42-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f3c42-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="f3c42-113">Este comando obtém as configurações avançadas de proteção contra ameaças para um pool SQL chamado ContosoSqlPool no espaço de trabalho chamado ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="f3c42-113">This command gets the advanced threat protection settings for a SQL pool named ContosoSqlPool under the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="f3c42-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f3c42-114">PARAMETERS</span></span>

### <span data-ttu-id="f3c42-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3c42-115">-DefaultProfile</span></span>
<span data-ttu-id="f3c42-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f3c42-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3c42-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f3c42-117">-InputObject</span></span>
<span data-ttu-id="f3c42-118">SQL objeto de entrada do pool, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="f3c42-118">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: GetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f3c42-119">-Name</span><span class="sxs-lookup"><span data-stu-id="f3c42-119">-Name</span></span>
<span data-ttu-id="f3c42-120">Nome do pool SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="f3c42-120">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3c42-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3c42-121">-ResourceGroupName</span></span>
<span data-ttu-id="f3c42-122">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f3c42-122">Resource group name.</span></span>

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

### <span data-ttu-id="f3c42-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f3c42-123">-ResourceId</span></span>
<span data-ttu-id="f3c42-124">Identificador de recursos do Pool SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="f3c42-124">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="f3c42-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f3c42-125">-WorkspaceName</span></span>
<span data-ttu-id="f3c42-126">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="f3c42-126">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="f3c42-127">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="f3c42-127">-WorkspaceObject</span></span>
<span data-ttu-id="f3c42-128">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="f3c42-128">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f3c42-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3c42-129">CommonParameters</span></span>
<span data-ttu-id="f3c42-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3c42-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3c42-131">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f3c42-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3c42-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f3c42-132">INPUTS</span></span>

### <span data-ttu-id="f3c42-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="f3c42-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="f3c42-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="f3c42-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="f3c42-135">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f3c42-135">OUTPUTS</span></span>

### <span data-ttu-id="f3c42-136">Microsoft.Azure.Commands.Synapse.Models.PSSqlPoolSecurityAlertPolicy</span><span class="sxs-lookup"><span data-stu-id="f3c42-136">Microsoft.Azure.Commands.Synapse.Models.PSSqlPoolSecurityAlertPolicy</span></span>

## <span data-ttu-id="f3c42-137">NOTES</span><span class="sxs-lookup"><span data-stu-id="f3c42-137">NOTES</span></span>

## <span data-ttu-id="f3c42-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f3c42-138">RELATED LINKS</span></span>
