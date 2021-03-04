---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsesqlpoolauditsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolAuditSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolAuditSetting.md
ms.openlocfilehash: dea94d89bfd5384d8ec614259a5bb342cd9d186b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901532"
---
# <span data-ttu-id="dcdb9-101">Get-AzSynapseSqlPoolAuditSetting</span><span class="sxs-lookup"><span data-stu-id="dcdb9-101">Get-AzSynapseSqlPoolAuditSetting</span></span>

## <span data-ttu-id="dcdb9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dcdb9-102">SYNOPSIS</span></span>
<span data-ttu-id="dcdb9-103">Obtém as configurações de auditoria de um pool do Azure Synapse Analytics SQL pool.</span><span class="sxs-lookup"><span data-stu-id="dcdb9-103">Gets the auditing settings of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="dcdb9-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="dcdb9-104">SYNTAX</span></span>

### <span data-ttu-id="dcdb9-105">GetByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="dcdb9-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolAuditSetting [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dcdb9-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dcdb9-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolAuditSetting -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dcdb9-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dcdb9-107">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolAuditSetting -InputObject <PSSynapseSqlPool> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dcdb9-108">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dcdb9-108">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlPoolAuditSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dcdb9-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="dcdb9-109">DESCRIPTION</span></span>
<span data-ttu-id="dcdb9-110">O cmdlet **Get-AzSynapseSqlPoolAuditSetting** obtém as configurações de auditoria de um pool do Azure Synapse Analytics SQL.</span><span class="sxs-lookup"><span data-stu-id="dcdb9-110">The **Get-AzSynapseSqlPoolAuditSetting** cmdlet gets the auditing settings of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="dcdb9-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dcdb9-111">EXAMPLES</span></span>

### <span data-ttu-id="dcdb9-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="dcdb9-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="dcdb9-113">Este comando obtém as configurações de auditoria de um pool SQL chamado ContosoSqlPool no espaço de trabalho ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="dcdb9-113">This command gets the auditing settings of a SQL pool called ContosoSqlPool in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="dcdb9-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="dcdb9-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Get-AzSynapseSqlPoolAuditSetting
```

<span data-ttu-id="dcdb9-115">Este comando obtém as configurações de auditoria de um pool SQL chamado ContosoSqlPool no espaço de trabalho ContosoWorkspace por meio de pipeline.</span><span class="sxs-lookup"><span data-stu-id="dcdb9-115">This command gets the auditing settings of a SQL pool called ContosoSqlPool in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="dcdb9-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="dcdb9-116">PARAMETERS</span></span>

### <span data-ttu-id="dcdb9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcdb9-117">-DefaultProfile</span></span>
<span data-ttu-id="dcdb9-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dcdb9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dcdb9-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dcdb9-119">-InputObject</span></span>
<span data-ttu-id="dcdb9-120">SQL objeto de entrada do pool, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="dcdb9-120">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="dcdb9-121">-Name</span><span class="sxs-lookup"><span data-stu-id="dcdb9-121">-Name</span></span>
<span data-ttu-id="dcdb9-122">Nome do pool SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="dcdb9-122">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="dcdb9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dcdb9-123">-ResourceGroupName</span></span>
<span data-ttu-id="dcdb9-124">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="dcdb9-124">Resource group name.</span></span>

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

### <span data-ttu-id="dcdb9-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dcdb9-125">-ResourceId</span></span>
<span data-ttu-id="dcdb9-126">Identificador de recursos do Pool SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="dcdb9-126">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="dcdb9-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="dcdb9-127">-WorkspaceName</span></span>
<span data-ttu-id="dcdb9-128">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="dcdb9-128">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="dcdb9-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="dcdb9-129">-WorkspaceObject</span></span>
<span data-ttu-id="dcdb9-130">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="dcdb9-130">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="dcdb9-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcdb9-131">CommonParameters</span></span>
<span data-ttu-id="dcdb9-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dcdb9-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcdb9-133">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dcdb9-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcdb9-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dcdb9-134">INPUTS</span></span>

### <span data-ttu-id="dcdb9-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="dcdb9-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="dcdb9-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="dcdb9-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="dcdb9-137">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="dcdb9-137">OUTPUTS</span></span>

### <span data-ttu-id="dcdb9-138">Microsoft.Azure.Commands.Synapse.Models.SqlPoolAuditModel</span><span class="sxs-lookup"><span data-stu-id="dcdb9-138">Microsoft.Azure.Commands.Synapse.Models.SqlPoolAuditModel</span></span>

## <span data-ttu-id="dcdb9-139">NOTES</span><span class="sxs-lookup"><span data-stu-id="dcdb9-139">NOTES</span></span>

## <span data-ttu-id="dcdb9-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dcdb9-140">RELATED LINKS</span></span>
