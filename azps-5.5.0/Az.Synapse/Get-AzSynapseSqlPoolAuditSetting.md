---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlpoolauditsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolAuditSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolAuditSetting.md
ms.openlocfilehash: 592c35a3407bd42846e8c24786716a73d5729c9a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115621"
---
# <span data-ttu-id="e3485-101">Get-AzSynapseSqlPoolAuditSetting</span><span class="sxs-lookup"><span data-stu-id="e3485-101">Get-AzSynapseSqlPoolAuditSetting</span></span>

## <span data-ttu-id="e3485-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e3485-102">SYNOPSIS</span></span>
<span data-ttu-id="e3485-103">Obtém as configurações de auditoria de um pool SQL do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="e3485-103">Gets the auditing settings of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="e3485-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e3485-104">SYNTAX</span></span>

### <span data-ttu-id="e3485-105">GetByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e3485-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolAuditSetting [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e3485-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3485-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolAuditSetting -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e3485-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3485-107">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolAuditSetting -InputObject <PSSynapseSqlPool> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e3485-108">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3485-108">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlPoolAuditSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e3485-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="e3485-109">DESCRIPTION</span></span>
<span data-ttu-id="e3485-110">O cmdlet **Get-AzSynapseSqlPoolAuditSetting** obtém as configurações de auditoria de um pool SQL do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="e3485-110">The **Get-AzSynapseSqlPoolAuditSetting** cmdlet gets the auditing settings of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="e3485-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e3485-111">EXAMPLES</span></span>

### <span data-ttu-id="e3485-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e3485-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="e3485-113">Esse comando obtém as configurações de auditoria de um pool SQL chamado ContosoSqlPool no espaço de trabalho ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="e3485-113">This command gets the auditing settings of a SQL pool called ContosoSqlPool in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="e3485-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="e3485-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Get-AzSynapseSqlPoolAuditSetting
```

<span data-ttu-id="e3485-115">Esse comando obtém as configurações de auditoria de um pool SQL chamado ContosoSqlPool no espaço de trabalho ContosoWorkspace por meio do pipeline.</span><span class="sxs-lookup"><span data-stu-id="e3485-115">This command gets the auditing settings of a SQL pool called ContosoSqlPool in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="e3485-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e3485-116">PARAMETERS</span></span>

### <span data-ttu-id="e3485-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3485-117">-DefaultProfile</span></span>
<span data-ttu-id="e3485-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e3485-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3485-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e3485-119">-InputObject</span></span>
<span data-ttu-id="e3485-120">Objeto de entrada de pool SQL, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="e3485-120">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="e3485-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="e3485-121">-Name</span></span>
<span data-ttu-id="e3485-122">Nome do pool SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="e3485-122">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="e3485-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3485-123">-ResourceGroupName</span></span>
<span data-ttu-id="e3485-124">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e3485-124">Resource group name.</span></span>

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

### <span data-ttu-id="e3485-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e3485-125">-ResourceId</span></span>
<span data-ttu-id="e3485-126">Identificador de recursos do Pool SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="e3485-126">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="e3485-127">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="e3485-127">-WorkspaceName</span></span>
<span data-ttu-id="e3485-128">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="e3485-128">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="e3485-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="e3485-129">-WorkspaceObject</span></span>
<span data-ttu-id="e3485-130">objeto de entrada de espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="e3485-130">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="e3485-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3485-131">CommonParameters</span></span>
<span data-ttu-id="e3485-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3485-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3485-133">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e3485-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3485-134">Entradas</span><span class="sxs-lookup"><span data-stu-id="e3485-134">INPUTS</span></span>

### <span data-ttu-id="e3485-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="e3485-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="e3485-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="e3485-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="e3485-137">Saídas</span><span class="sxs-lookup"><span data-stu-id="e3485-137">OUTPUTS</span></span>

### <span data-ttu-id="e3485-138">Microsoft.Azure.Commands.Synapse.Models.SqlPoolAuditModel</span><span class="sxs-lookup"><span data-stu-id="e3485-138">Microsoft.Azure.Commands.Synapse.Models.SqlPoolAuditModel</span></span>

## <span data-ttu-id="e3485-139">Notas</span><span class="sxs-lookup"><span data-stu-id="e3485-139">NOTES</span></span>

## <span data-ttu-id="e3485-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e3485-140">RELATED LINKS</span></span>
