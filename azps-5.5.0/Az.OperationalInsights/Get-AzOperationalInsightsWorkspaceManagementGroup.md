---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: F29E0B9C-2479-44FB-B196-EAF97B69E6A6
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspacemanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceManagementGroup.md
ms.openlocfilehash: 1579308aed29a4d42cddfeec6f01c71c72c06c6f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118225"
---
# <span data-ttu-id="3af5e-101">Get-AzOperationalInsightsWorkspaceManagementGroup</span><span class="sxs-lookup"><span data-stu-id="3af5e-101">Get-AzOperationalInsightsWorkspaceManagementGroup</span></span>

## <span data-ttu-id="3af5e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3af5e-102">SYNOPSIS</span></span>
<span data-ttu-id="3af5e-103">Obtém detalhes de grupos de gerenciamento conectados a um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="3af5e-103">Gets details of management groups connected to a workspace.</span></span>

## <span data-ttu-id="3af5e-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3af5e-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsWorkspaceManagementGroup [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3af5e-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="3af5e-105">DESCRIPTION</span></span>
<span data-ttu-id="3af5e-106">O cmdlet **Get-AzOperationalInsightsWorkspaceManagementGroup** lista os grupos de gerenciamento que estão conectados a um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="3af5e-106">The **Get-AzOperationalInsightsWorkspaceManagementGroup** cmdlet lists the management groups that are connected to a workspace.</span></span>

## <span data-ttu-id="3af5e-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3af5e-107">EXAMPLES</span></span>

### <span data-ttu-id="3af5e-108">Exemplo 1: Obter grupos de gerenciamento por nome de espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="3af5e-108">Example 1: Get management groups by workspace name</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspaceManagementGroup -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="3af5e-109">Esse comando obtém os grupos de gerenciamento do espaço de trabalho chamado MyWorkspace no grupo de recursos chamado ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="3af5e-109">This command gets the management groups for the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="3af5e-110">Exemplo 2: Obter grupos de gerenciamento usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="3af5e-110">Example 2: Get management groups by using the pipeline</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzOperationalInsightsWorkspaceManagementGroup
```

<span data-ttu-id="3af5e-111">Esse comando usa o cmdlet Get-AzOperationalInsightsWorkspace para obter o espaço de trabalho chamado MyWorkspace e passa o espaço de trabalho para o cmdlet atual, que obtém os grupos de gerenciamento para esse espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="3af5e-111">This command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then passes the workspace to the current cmdlet, which gets the management groups for that workspace.</span></span>

## <span data-ttu-id="3af5e-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3af5e-112">PARAMETERS</span></span>

### <span data-ttu-id="3af5e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3af5e-113">-DefaultProfile</span></span>
<span data-ttu-id="3af5e-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="3af5e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3af5e-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="3af5e-115">-Name</span></span>
<span data-ttu-id="3af5e-116">Especifica o nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="3af5e-116">Specifies the workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3af5e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3af5e-117">-ResourceGroupName</span></span>
<span data-ttu-id="3af5e-118">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="3af5e-118">Specifies the name of an Azure resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3af5e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3af5e-119">CommonParameters</span></span>
<span data-ttu-id="3af5e-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3af5e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3af5e-121">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3af5e-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3af5e-122">Entradas</span><span class="sxs-lookup"><span data-stu-id="3af5e-122">INPUTS</span></span>

### <span data-ttu-id="3af5e-123">System.String</span><span class="sxs-lookup"><span data-stu-id="3af5e-123">System.String</span></span>

## <span data-ttu-id="3af5e-124">Saídas</span><span class="sxs-lookup"><span data-stu-id="3af5e-124">OUTPUTS</span></span>

### <span data-ttu-id="3af5e-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="3af5e-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSManagementGroup</span></span>

## <span data-ttu-id="3af5e-126">Notas</span><span class="sxs-lookup"><span data-stu-id="3af5e-126">NOTES</span></span>

## <span data-ttu-id="3af5e-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3af5e-127">RELATED LINKS</span></span>

[<span data-ttu-id="3af5e-128">Cmdlets de Insights Operacionais do Azure</span><span class="sxs-lookup"><span data-stu-id="3af5e-128">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="3af5e-129">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="3af5e-129">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


