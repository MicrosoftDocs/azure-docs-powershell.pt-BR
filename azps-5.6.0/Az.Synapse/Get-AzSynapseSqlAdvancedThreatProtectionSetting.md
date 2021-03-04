---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsesqladvancedthreatprotectionsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAdvancedThreatProtectionSetting.md
ms.openlocfilehash: f35e4787779c49b399659f5e01ed8002df2e19ff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901539"
---
# <span data-ttu-id="88b72-101">Get-AzSynapseSqlAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="88b72-101">Get-AzSynapseSqlAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="88b72-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88b72-102">SYNOPSIS</span></span>
<span data-ttu-id="88b72-103">Obtém as configurações avançadas de proteção contra ameaças para um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="88b72-103">Gets the advanced threat protection settings for a workspace.</span></span>

## <span data-ttu-id="88b72-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="88b72-104">SYNTAX</span></span>

### <span data-ttu-id="88b72-105">GetByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="88b72-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlAdvancedThreatProtectionSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="88b72-106">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="88b72-106">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlAdvancedThreatProtectionSetting -InputObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="88b72-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="88b72-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlAdvancedThreatProtectionSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="88b72-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="88b72-108">DESCRIPTION</span></span>
<span data-ttu-id="88b72-109">O cmdlet **Get-AzSynapseSqlAdvancedThreatProtectionSetting** obtém as configurações avançadas de proteção contra ameaças de um Espaço de Trabalho de Análise do Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="88b72-109">The **Get-AzSynapseSqlAdvancedThreatProtectionSetting** cmdlet gets the advanced threat protection settings of an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="88b72-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="88b72-110">EXAMPLES</span></span>

### <span data-ttu-id="88b72-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="88b72-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlAdvancedThreatProtectionSetting -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="88b72-112">Este comando obtém as configurações avançadas de proteção contra ameaças para um espaço de trabalho chamado ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="88b72-112">This command gets the advanced threat protection settings for a workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="88b72-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="88b72-113">PARAMETERS</span></span>

### <span data-ttu-id="88b72-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88b72-114">-DefaultProfile</span></span>
<span data-ttu-id="88b72-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="88b72-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88b72-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="88b72-116">-InputObject</span></span>
<span data-ttu-id="88b72-117">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="88b72-117">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="88b72-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88b72-118">-ResourceGroupName</span></span>
<span data-ttu-id="88b72-119">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="88b72-119">Resource group name.</span></span>

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

### <span data-ttu-id="88b72-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="88b72-120">-ResourceId</span></span>
<span data-ttu-id="88b72-121">Identificador de recursos do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="88b72-121">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="88b72-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="88b72-122">-WorkspaceName</span></span>
<span data-ttu-id="88b72-123">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="88b72-123">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="88b72-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88b72-124">CommonParameters</span></span>
<span data-ttu-id="88b72-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88b72-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88b72-126">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="88b72-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88b72-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="88b72-127">INPUTS</span></span>

### <span data-ttu-id="88b72-128">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="88b72-128">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="88b72-129">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="88b72-129">OUTPUTS</span></span>

### <span data-ttu-id="88b72-130">Microsoft.Azure.Commands.Synapse.Models.PSServerSecurityAlertPolicy</span><span class="sxs-lookup"><span data-stu-id="88b72-130">Microsoft.Azure.Commands.Synapse.Models.PSServerSecurityAlertPolicy</span></span>

## <span data-ttu-id="88b72-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="88b72-131">NOTES</span></span>

## <span data-ttu-id="88b72-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="88b72-132">RELATED LINKS</span></span>
