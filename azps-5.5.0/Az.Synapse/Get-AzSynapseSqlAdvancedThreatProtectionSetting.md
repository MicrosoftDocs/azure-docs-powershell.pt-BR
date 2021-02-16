---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqladvancedthreatprotectionsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 8c17825dca186f4edf856a2de2ef76082253c39e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118550"
---
# <span data-ttu-id="fe7a5-101">Get-AzSynapseSqlAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="fe7a5-101">Get-AzSynapseSqlAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="fe7a5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fe7a5-102">SYNOPSIS</span></span>
<span data-ttu-id="fe7a5-103">Obtém as configurações avançadas de proteção contra ameaças para um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="fe7a5-103">Gets the advanced threat protection settings for a workspace.</span></span>

## <span data-ttu-id="fe7a5-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fe7a5-104">SYNTAX</span></span>

### <span data-ttu-id="fe7a5-105">GetByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="fe7a5-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlAdvancedThreatProtectionSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe7a5-106">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe7a5-106">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlAdvancedThreatProtectionSetting -InputObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe7a5-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe7a5-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlAdvancedThreatProtectionSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fe7a5-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="fe7a5-108">DESCRIPTION</span></span>
<span data-ttu-id="fe7a5-109">O cmdlet **Get-AzSynapseSqlAdvancedThreatProtectionSetting** obtém as configurações avançadas de proteção contra ameaças de um Espaço de Trabalho de Análise do Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="fe7a5-109">The **Get-AzSynapseSqlAdvancedThreatProtectionSetting** cmdlet gets the advanced threat protection settings of an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="fe7a5-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="fe7a5-110">EXAMPLES</span></span>

### <span data-ttu-id="fe7a5-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fe7a5-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlAdvancedThreatProtectionSetting -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="fe7a5-112">Esse comando obtém as configurações avançadas de proteção contra ameaças para um espaço de trabalho chamado ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="fe7a5-112">This command gets the advanced threat protection settings for a workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="fe7a5-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fe7a5-113">PARAMETERS</span></span>

### <span data-ttu-id="fe7a5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe7a5-114">-DefaultProfile</span></span>
<span data-ttu-id="fe7a5-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fe7a5-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe7a5-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fe7a5-116">-InputObject</span></span>
<span data-ttu-id="fe7a5-117">objeto de entrada de espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="fe7a5-117">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="fe7a5-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe7a5-118">-ResourceGroupName</span></span>
<span data-ttu-id="fe7a5-119">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="fe7a5-119">Resource group name.</span></span>

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

### <span data-ttu-id="fe7a5-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fe7a5-120">-ResourceId</span></span>
<span data-ttu-id="fe7a5-121">Identificador de recurso do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="fe7a5-121">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="fe7a5-122">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="fe7a5-122">-WorkspaceName</span></span>
<span data-ttu-id="fe7a5-123">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="fe7a5-123">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="fe7a5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe7a5-124">CommonParameters</span></span>
<span data-ttu-id="fe7a5-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe7a5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe7a5-126">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fe7a5-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe7a5-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="fe7a5-127">INPUTS</span></span>

### <span data-ttu-id="fe7a5-128">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="fe7a5-128">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="fe7a5-129">Saídas</span><span class="sxs-lookup"><span data-stu-id="fe7a5-129">OUTPUTS</span></span>

### <span data-ttu-id="fe7a5-130">Microsoft.Azure.Commands.Synapse.Models.PSServerSecurityAlertPolicy</span><span class="sxs-lookup"><span data-stu-id="fe7a5-130">Microsoft.Azure.Commands.Synapse.Models.PSServerSecurityAlertPolicy</span></span>

## <span data-ttu-id="fe7a5-131">Notas</span><span class="sxs-lookup"><span data-stu-id="fe7a5-131">NOTES</span></span>

## <span data-ttu-id="fe7a5-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fe7a5-132">RELATED LINKS</span></span>
