---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlpoolauditsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolAuditSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolAuditSetting.md
ms.openlocfilehash: 592c35a3407bd42846e8c24786716a73d5729c9a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98272413"
---
# <span data-ttu-id="46f38-101">Get-AzSynapseSqlPoolAuditSetting</span><span class="sxs-lookup"><span data-stu-id="46f38-101">Get-AzSynapseSqlPoolAuditSetting</span></span>

## <span data-ttu-id="46f38-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="46f38-102">SYNOPSIS</span></span>
<span data-ttu-id="46f38-103">Obtém as configurações de auditoria de um pool SQL do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="46f38-103">Gets the auditing settings of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="46f38-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="46f38-104">SYNTAX</span></span>

### <span data-ttu-id="46f38-105">GetByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="46f38-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolAuditSetting [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="46f38-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="46f38-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolAuditSetting -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="46f38-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="46f38-107">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolAuditSetting -InputObject <PSSynapseSqlPool> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="46f38-108">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="46f38-108">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlPoolAuditSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="46f38-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="46f38-109">DESCRIPTION</span></span>
<span data-ttu-id="46f38-110">O cmdlet **Get-AzSynapseSqlPoolAuditSetting** Obtém as configurações de auditoria de um pool SQL do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="46f38-110">The **Get-AzSynapseSqlPoolAuditSetting** cmdlet gets the auditing settings of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="46f38-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="46f38-111">EXAMPLES</span></span>

### <span data-ttu-id="46f38-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="46f38-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="46f38-113">Esse comando obtém as configurações de auditoria de um pool SQL chamado ContosoSqlPool na ContosoWorkspace do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="46f38-113">This command gets the auditing settings of a SQL pool called ContosoSqlPool in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="46f38-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="46f38-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Get-AzSynapseSqlPoolAuditSetting
```

<span data-ttu-id="46f38-115">Esse comando obtém as configurações de auditoria de um pool SQL chamado ContosoSqlPool no espaço de trabalho ContosoWorkspace pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="46f38-115">This command gets the auditing settings of a SQL pool called ContosoSqlPool in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="46f38-116">OS</span><span class="sxs-lookup"><span data-stu-id="46f38-116">PARAMETERS</span></span>

### <span data-ttu-id="46f38-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46f38-117">-DefaultProfile</span></span>
<span data-ttu-id="46f38-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="46f38-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46f38-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="46f38-119">-InputObject</span></span>
<span data-ttu-id="46f38-120">Objeto de entrada de pool SQL, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="46f38-120">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="46f38-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="46f38-121">-Name</span></span>
<span data-ttu-id="46f38-122">Nome do pool do SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="46f38-122">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="46f38-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46f38-123">-ResourceGroupName</span></span>
<span data-ttu-id="46f38-124">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="46f38-124">Resource group name.</span></span>

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

### <span data-ttu-id="46f38-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="46f38-125">-ResourceId</span></span>
<span data-ttu-id="46f38-126">Identificador de recurso do pool do SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="46f38-126">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="46f38-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="46f38-127">-WorkspaceName</span></span>
<span data-ttu-id="46f38-128">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="46f38-128">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="46f38-129">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="46f38-129">-WorkspaceObject</span></span>
<span data-ttu-id="46f38-130">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="46f38-130">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="46f38-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46f38-131">CommonParameters</span></span>
<span data-ttu-id="46f38-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46f38-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46f38-133">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="46f38-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46f38-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="46f38-134">INPUTS</span></span>

### <span data-ttu-id="46f38-135">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="46f38-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="46f38-136">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="46f38-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="46f38-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="46f38-137">OUTPUTS</span></span>

### <span data-ttu-id="46f38-138">Microsoft. Azure. Commands. Synapse. Models. SqlPoolAuditModel</span><span class="sxs-lookup"><span data-stu-id="46f38-138">Microsoft.Azure.Commands.Synapse.Models.SqlPoolAuditModel</span></span>

## <span data-ttu-id="46f38-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="46f38-139">NOTES</span></span>

## <span data-ttu-id="46f38-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="46f38-140">RELATED LINKS</span></span>
