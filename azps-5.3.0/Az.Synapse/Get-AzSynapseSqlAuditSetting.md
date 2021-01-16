---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlauditsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAuditSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAuditSetting.md
ms.openlocfilehash: ab1a8f9b91f8a47f5c6b97b537489c65a53e146e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98272420"
---
# <span data-ttu-id="2e056-101">Get-AzSynapseSqlAuditSetting</span><span class="sxs-lookup"><span data-stu-id="2e056-101">Get-AzSynapseSqlAuditSetting</span></span>

## <span data-ttu-id="2e056-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2e056-102">SYNOPSIS</span></span>
<span data-ttu-id="2e056-103">Obtém as configurações de auditoria de um espaço de trabalho de análise do Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="2e056-103">Gets the auditing settings of an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="2e056-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2e056-104">SYNTAX</span></span>

### <span data-ttu-id="2e056-105">GetByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="2e056-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlAuditSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2e056-106">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2e056-106">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlAuditSetting -InputObject <PSSynapseWorkspace> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2e056-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2e056-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlAuditSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2e056-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2e056-108">DESCRIPTION</span></span>
<span data-ttu-id="2e056-109">O cmdlet **Get-AzSynapseSqlAuditSetting** Obtém as configurações de auditoria de um espaço de trabalho de análise do Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="2e056-109">The **Get-AzSynapseSqlAuditSetting** cmdlet gets the auditing settings of an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="2e056-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2e056-110">EXAMPLES</span></span>

### <span data-ttu-id="2e056-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2e056-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlAuditSetting -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="2e056-112">Obtém as configurações de auditoria de um espaço de trabalho chamado ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="2e056-112">Gets the auditing settings of a workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="2e056-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="2e056-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace | Get-AzSynapseSqlAuditSetting
```

<span data-ttu-id="2e056-114">Obtém as configurações de auditoria de um espaço de trabalho chamado ContosoWorkspace pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="2e056-114">Gets the auditing settings of a workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="2e056-115">OS</span><span class="sxs-lookup"><span data-stu-id="2e056-115">PARAMETERS</span></span>

### <span data-ttu-id="2e056-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e056-116">-DefaultProfile</span></span>
<span data-ttu-id="2e056-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2e056-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e056-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2e056-118">-InputObject</span></span>
<span data-ttu-id="2e056-119">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="2e056-119">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="2e056-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e056-120">-ResourceGroupName</span></span>
<span data-ttu-id="2e056-121">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2e056-121">Resource group name.</span></span>

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

### <span data-ttu-id="2e056-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2e056-122">-ResourceId</span></span>
<span data-ttu-id="2e056-123">Identificador de recurso do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="2e056-123">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="2e056-124">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="2e056-124">-WorkspaceName</span></span>
<span data-ttu-id="2e056-125">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="2e056-125">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="2e056-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e056-126">CommonParameters</span></span>
<span data-ttu-id="2e056-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e056-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e056-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2e056-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e056-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2e056-129">INPUTS</span></span>

### <span data-ttu-id="2e056-130">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="2e056-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="2e056-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2e056-131">OUTPUTS</span></span>

### <span data-ttu-id="2e056-132">Microsoft. Azure. Commands. Synapse. Models. WorkspaceAuditModel</span><span class="sxs-lookup"><span data-stu-id="2e056-132">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAuditModel</span></span>

## <span data-ttu-id="2e056-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2e056-133">NOTES</span></span>

## <span data-ttu-id="2e056-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2e056-134">RELATED LINKS</span></span>
