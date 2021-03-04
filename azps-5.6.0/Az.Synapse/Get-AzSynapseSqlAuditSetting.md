---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsesqlauditsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAuditSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAuditSetting.md
ms.openlocfilehash: cf32bea3942c89b408592778657e5ecffae2acd8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901538"
---
# <span data-ttu-id="dc150-101">Get-AzSynapseSqlAuditSetting</span><span class="sxs-lookup"><span data-stu-id="dc150-101">Get-AzSynapseSqlAuditSetting</span></span>

## <span data-ttu-id="dc150-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc150-102">SYNOPSIS</span></span>
<span data-ttu-id="dc150-103">Obtém as configurações de auditoria de um Espaço de Trabalho de Análise do Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="dc150-103">Gets the auditing settings of an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="dc150-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="dc150-104">SYNTAX</span></span>

### <span data-ttu-id="dc150-105">GetByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="dc150-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlAuditSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dc150-106">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc150-106">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlAuditSetting -InputObject <PSSynapseWorkspace> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dc150-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc150-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlAuditSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dc150-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="dc150-108">DESCRIPTION</span></span>
<span data-ttu-id="dc150-109">O cmdlet **Get-AzSynapseSqlAuditSetting** obtém as configurações de auditoria de um Espaço de Trabalho de Análise do Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="dc150-109">The **Get-AzSynapseSqlAuditSetting** cmdlet gets the auditing settings of an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="dc150-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dc150-110">EXAMPLES</span></span>

### <span data-ttu-id="dc150-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="dc150-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlAuditSetting -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="dc150-112">Obtém as configurações de auditoria de um espaço de trabalho chamado ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="dc150-112">Gets the auditing settings of a workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="dc150-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="dc150-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace | Get-AzSynapseSqlAuditSetting
```

<span data-ttu-id="dc150-114">Obtém as configurações de auditoria de um espaço de trabalho chamado ContosoWorkspace por pipeline.</span><span class="sxs-lookup"><span data-stu-id="dc150-114">Gets the auditing settings of a workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="dc150-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="dc150-115">PARAMETERS</span></span>

### <span data-ttu-id="dc150-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc150-116">-DefaultProfile</span></span>
<span data-ttu-id="dc150-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dc150-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc150-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dc150-118">-InputObject</span></span>
<span data-ttu-id="dc150-119">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="dc150-119">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="dc150-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc150-120">-ResourceGroupName</span></span>
<span data-ttu-id="dc150-121">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="dc150-121">Resource group name.</span></span>

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

### <span data-ttu-id="dc150-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dc150-122">-ResourceId</span></span>
<span data-ttu-id="dc150-123">Identificador de recursos do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="dc150-123">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="dc150-124">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="dc150-124">-WorkspaceName</span></span>
<span data-ttu-id="dc150-125">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="dc150-125">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="dc150-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc150-126">CommonParameters</span></span>
<span data-ttu-id="dc150-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc150-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc150-128">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dc150-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc150-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dc150-129">INPUTS</span></span>

### <span data-ttu-id="dc150-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="dc150-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="dc150-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="dc150-131">OUTPUTS</span></span>

### <span data-ttu-id="dc150-132">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAuditModel</span><span class="sxs-lookup"><span data-stu-id="dc150-132">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAuditModel</span></span>

## <span data-ttu-id="dc150-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="dc150-133">NOTES</span></span>

## <span data-ttu-id="dc150-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dc150-134">RELATED LINKS</span></span>
