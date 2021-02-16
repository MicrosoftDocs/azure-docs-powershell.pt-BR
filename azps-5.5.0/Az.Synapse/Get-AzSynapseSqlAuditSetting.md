---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlauditsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAuditSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAuditSetting.md
ms.openlocfilehash: ab1a8f9b91f8a47f5c6b97b537489c65a53e146e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118546"
---
# <span data-ttu-id="a0a6c-101">Get-AzSynapseSqlAuditSetting</span><span class="sxs-lookup"><span data-stu-id="a0a6c-101">Get-AzSynapseSqlAuditSetting</span></span>

## <span data-ttu-id="a0a6c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a0a6c-102">SYNOPSIS</span></span>
<span data-ttu-id="a0a6c-103">Obtém as configurações de auditoria de um Espaço de Trabalho do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="a0a6c-103">Gets the auditing settings of an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="a0a6c-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a0a6c-104">SYNTAX</span></span>

### <span data-ttu-id="a0a6c-105">GetByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a0a6c-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlAuditSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a0a6c-106">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0a6c-106">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlAuditSetting -InputObject <PSSynapseWorkspace> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a0a6c-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0a6c-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlAuditSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a0a6c-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="a0a6c-108">DESCRIPTION</span></span>
<span data-ttu-id="a0a6c-109">O cmdlet **Get-AzSynapseSqlAuditSetting obtém** as configurações de auditoria de um Espaço de Trabalho do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="a0a6c-109">The **Get-AzSynapseSqlAuditSetting** cmdlet gets the auditing settings of an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="a0a6c-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a0a6c-110">EXAMPLES</span></span>

### <span data-ttu-id="a0a6c-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a0a6c-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlAuditSetting -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="a0a6c-112">Obtém as configurações de auditoria de um espaço de trabalho chamado ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="a0a6c-112">Gets the auditing settings of a workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="a0a6c-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="a0a6c-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace | Get-AzSynapseSqlAuditSetting
```

<span data-ttu-id="a0a6c-114">Obtém as configurações de auditoria de um espaço de trabalho chamado ContosoWorkspace por meio de pipeline.</span><span class="sxs-lookup"><span data-stu-id="a0a6c-114">Gets the auditing settings of a workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="a0a6c-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a0a6c-115">PARAMETERS</span></span>

### <span data-ttu-id="a0a6c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0a6c-116">-DefaultProfile</span></span>
<span data-ttu-id="a0a6c-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a0a6c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0a6c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a0a6c-118">-InputObject</span></span>
<span data-ttu-id="a0a6c-119">objeto de entrada de espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="a0a6c-119">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="a0a6c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0a6c-120">-ResourceGroupName</span></span>
<span data-ttu-id="a0a6c-121">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a0a6c-121">Resource group name.</span></span>

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

### <span data-ttu-id="a0a6c-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a0a6c-122">-ResourceId</span></span>
<span data-ttu-id="a0a6c-123">Identificador de recurso do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="a0a6c-123">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="a0a6c-124">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="a0a6c-124">-WorkspaceName</span></span>
<span data-ttu-id="a0a6c-125">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="a0a6c-125">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="a0a6c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0a6c-126">CommonParameters</span></span>
<span data-ttu-id="a0a6c-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0a6c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0a6c-128">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a0a6c-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0a6c-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="a0a6c-129">INPUTS</span></span>

### <span data-ttu-id="a0a6c-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="a0a6c-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="a0a6c-131">Saídas</span><span class="sxs-lookup"><span data-stu-id="a0a6c-131">OUTPUTS</span></span>

### <span data-ttu-id="a0a6c-132">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAuditModel</span><span class="sxs-lookup"><span data-stu-id="a0a6c-132">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAuditModel</span></span>

## <span data-ttu-id="a0a6c-133">Notas</span><span class="sxs-lookup"><span data-stu-id="a0a6c-133">NOTES</span></span>

## <span data-ttu-id="a0a6c-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a0a6c-134">RELATED LINKS</span></span>
