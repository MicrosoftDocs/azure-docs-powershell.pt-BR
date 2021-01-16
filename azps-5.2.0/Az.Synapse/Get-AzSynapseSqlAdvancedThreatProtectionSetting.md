---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqladvancedthreatprotectionsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 8c17825dca186f4edf856a2de2ef76082253c39e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98262544"
---
# <span data-ttu-id="cc6f2-101">Get-AzSynapseSqlAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="cc6f2-101">Get-AzSynapseSqlAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="cc6f2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cc6f2-102">SYNOPSIS</span></span>
<span data-ttu-id="cc6f2-103">Obtém as configurações avançadas de proteção contra ameaças para um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="cc6f2-103">Gets the advanced threat protection settings for a workspace.</span></span>

## <span data-ttu-id="cc6f2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cc6f2-104">SYNTAX</span></span>

### <span data-ttu-id="cc6f2-105">GetByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="cc6f2-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlAdvancedThreatProtectionSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cc6f2-106">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc6f2-106">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlAdvancedThreatProtectionSetting -InputObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cc6f2-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc6f2-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlAdvancedThreatProtectionSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cc6f2-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cc6f2-108">DESCRIPTION</span></span>
<span data-ttu-id="cc6f2-109">O cmdlet **Get-AzSynapseSqlAdvancedThreatProtectionSetting** Obtém as configurações avançadas de proteção contra ameaças de um espaço de trabalho de análise do Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="cc6f2-109">The **Get-AzSynapseSqlAdvancedThreatProtectionSetting** cmdlet gets the advanced threat protection settings of an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="cc6f2-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cc6f2-110">EXAMPLES</span></span>

### <span data-ttu-id="cc6f2-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="cc6f2-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlAdvancedThreatProtectionSetting -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="cc6f2-112">Este comando obtém as configurações avançadas de proteção contra ameaças para um espaço de trabalho chamado ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="cc6f2-112">This command gets the advanced threat protection settings for a workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="cc6f2-113">OS</span><span class="sxs-lookup"><span data-stu-id="cc6f2-113">PARAMETERS</span></span>

### <span data-ttu-id="cc6f2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc6f2-114">-DefaultProfile</span></span>
<span data-ttu-id="cc6f2-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cc6f2-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc6f2-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cc6f2-116">-InputObject</span></span>
<span data-ttu-id="cc6f2-117">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="cc6f2-117">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="cc6f2-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc6f2-118">-ResourceGroupName</span></span>
<span data-ttu-id="cc6f2-119">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="cc6f2-119">Resource group name.</span></span>

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

### <span data-ttu-id="cc6f2-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cc6f2-120">-ResourceId</span></span>
<span data-ttu-id="cc6f2-121">Identificador de recurso do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="cc6f2-121">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="cc6f2-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="cc6f2-122">-WorkspaceName</span></span>
<span data-ttu-id="cc6f2-123">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="cc6f2-123">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="cc6f2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc6f2-124">CommonParameters</span></span>
<span data-ttu-id="cc6f2-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc6f2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc6f2-126">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cc6f2-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc6f2-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cc6f2-127">INPUTS</span></span>

### <span data-ttu-id="cc6f2-128">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="cc6f2-128">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="cc6f2-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cc6f2-129">OUTPUTS</span></span>

### <span data-ttu-id="cc6f2-130">Microsoft. Azure. Commands. Synapse. Models. PSServerSecurityAlertPolicy</span><span class="sxs-lookup"><span data-stu-id="cc6f2-130">Microsoft.Azure.Commands.Synapse.Models.PSServerSecurityAlertPolicy</span></span>

## <span data-ttu-id="cc6f2-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cc6f2-131">NOTES</span></span>

## <span data-ttu-id="cc6f2-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cc6f2-132">RELATED LINKS</span></span>
