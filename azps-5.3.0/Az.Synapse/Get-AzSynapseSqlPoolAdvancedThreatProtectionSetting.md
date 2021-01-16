---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlpooladvancedthreatprotectionsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 4e3b6b596f276f3d36a315354a93950524722adc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98272416"
---
# <span data-ttu-id="6a8bc-101">Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="6a8bc-101">Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="6a8bc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6a8bc-102">SYNOPSIS</span></span>
<span data-ttu-id="6a8bc-103">Obtém as configurações avançadas de proteção contra ameaças para um pool do SQL.</span><span class="sxs-lookup"><span data-stu-id="6a8bc-103">Gets the advanced threat protection settings for a SQL pool.</span></span>

## <span data-ttu-id="6a8bc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6a8bc-104">SYNTAX</span></span>

### <span data-ttu-id="6a8bc-105">GetByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="6a8bc-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6a8bc-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6a8bc-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6a8bc-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6a8bc-107">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting -InputObject <PSSynapseSqlPool>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6a8bc-108">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6a8bc-108">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6a8bc-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6a8bc-109">DESCRIPTION</span></span>
<span data-ttu-id="6a8bc-110">O cmdlet **Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting** Obtém as configurações avançadas de proteção contra ameaças de um pool SQL do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="6a8bc-110">The **Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting** cmdlet gets the advanced threat protection settings of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="6a8bc-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6a8bc-111">EXAMPLES</span></span>

### <span data-ttu-id="6a8bc-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6a8bc-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="6a8bc-113">Esse comando obtém as configurações avançadas de proteção contra ameaças para um pool SQL chamado ContosoSqlPool no espaço de trabalho chamado ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="6a8bc-113">This command gets the advanced threat protection settings for a SQL pool named ContosoSqlPool under the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="6a8bc-114">OS</span><span class="sxs-lookup"><span data-stu-id="6a8bc-114">PARAMETERS</span></span>

### <span data-ttu-id="6a8bc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a8bc-115">-DefaultProfile</span></span>
<span data-ttu-id="6a8bc-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6a8bc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a8bc-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6a8bc-117">-InputObject</span></span>
<span data-ttu-id="6a8bc-118">Objeto de entrada de pool SQL, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="6a8bc-118">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="6a8bc-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="6a8bc-119">-Name</span></span>
<span data-ttu-id="6a8bc-120">Nome do pool do SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="6a8bc-120">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="6a8bc-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a8bc-121">-ResourceGroupName</span></span>
<span data-ttu-id="6a8bc-122">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6a8bc-122">Resource group name.</span></span>

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

### <span data-ttu-id="6a8bc-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6a8bc-123">-ResourceId</span></span>
<span data-ttu-id="6a8bc-124">Identificador de recurso do pool do SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="6a8bc-124">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="6a8bc-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6a8bc-125">-WorkspaceName</span></span>
<span data-ttu-id="6a8bc-126">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="6a8bc-126">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="6a8bc-127">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="6a8bc-127">-WorkspaceObject</span></span>
<span data-ttu-id="6a8bc-128">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="6a8bc-128">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="6a8bc-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a8bc-129">CommonParameters</span></span>
<span data-ttu-id="6a8bc-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a8bc-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a8bc-131">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6a8bc-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a8bc-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6a8bc-132">INPUTS</span></span>

### <span data-ttu-id="6a8bc-133">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="6a8bc-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="6a8bc-134">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="6a8bc-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="6a8bc-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6a8bc-135">OUTPUTS</span></span>

### <span data-ttu-id="6a8bc-136">Microsoft. Azure. Commands. Synapse. Models. PSSqlPoolSecurityAlertPolicy</span><span class="sxs-lookup"><span data-stu-id="6a8bc-136">Microsoft.Azure.Commands.Synapse.Models.PSSqlPoolSecurityAlertPolicy</span></span>

## <span data-ttu-id="6a8bc-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6a8bc-137">NOTES</span></span>

## <span data-ttu-id="6a8bc-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6a8bc-138">RELATED LINKS</span></span>
