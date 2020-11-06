---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: F29E0B9C-2479-44FB-B196-EAF97B69E6A6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightsworkspacemanagementgroups
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspaceManagementGroups.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspaceManagementGroups.md
ms.openlocfilehash: 215e3007de3b3760d974512cdffdd669f32447ec
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428045"
---
# <span data-ttu-id="a3ac5-101">Get-AzureRmOperationalInsightsWorkspaceManagementGroups</span><span class="sxs-lookup"><span data-stu-id="a3ac5-101">Get-AzureRmOperationalInsightsWorkspaceManagementGroups</span></span>

## <span data-ttu-id="a3ac5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a3ac5-102">SYNOPSIS</span></span>
<span data-ttu-id="a3ac5-103">Obtém detalhes dos grupos de gerenciamento conectados a um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="a3ac5-103">Gets details of management groups connected to a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a3ac5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a3ac5-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsWorkspaceManagementGroups [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a3ac5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a3ac5-105">DESCRIPTION</span></span>
<span data-ttu-id="a3ac5-106">O cmdlet **Get-AzureRmOperationalInsightsWorkspaceManagementGroups** lista os grupos de gerenciamento que estão conectados a um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="a3ac5-106">The **Get-AzureRmOperationalInsightsWorkspaceManagementGroups** cmdlet lists the management groups that are connected to a workspace.</span></span>

## <span data-ttu-id="a3ac5-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a3ac5-107">EXAMPLES</span></span>

### <span data-ttu-id="a3ac5-108">Exemplo 1: obter grupos de gerenciamento pelo nome do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="a3ac5-108">Example 1: Get management groups by workspace name</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspaceManagementGroups -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="a3ac5-109">Esse comando obtém os grupos de gerenciamento do espaço de trabalho chamado MyWorkspace no grupo de recursos chamado ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="a3ac5-109">This command gets the management groups for the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="a3ac5-110">Exemplo 2: obter grupos de gerenciamento usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="a3ac5-110">Example 2: Get management groups by using the pipeline</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzureOperationalInsightsWorkspaceManagementGroups
```

<span data-ttu-id="a3ac5-111">Esse comando usa o cmdlet Get-AzureRmOperationalInsightsWorkspace para obter o espaço de trabalho chamado MyWorkspace e, em seguida, passa o espaço de trabalho para o cmdlet atual, que obtém os grupos de gerenciamento desse espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="a3ac5-111">This command uses the Get-AzureRmOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then passes the workspace to the current cmdlet, which gets the management groups for that workspace.</span></span>

## <span data-ttu-id="a3ac5-112">OS</span><span class="sxs-lookup"><span data-stu-id="a3ac5-112">PARAMETERS</span></span>

### <span data-ttu-id="a3ac5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3ac5-113">-DefaultProfile</span></span>
<span data-ttu-id="a3ac5-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="a3ac5-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3ac5-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="a3ac5-115">-Name</span></span>
<span data-ttu-id="a3ac5-116">Especifica o nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="a3ac5-116">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="a3ac5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3ac5-117">-ResourceGroupName</span></span>
<span data-ttu-id="a3ac5-118">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="a3ac5-118">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="a3ac5-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3ac5-119">CommonParameters</span></span>
<span data-ttu-id="a3ac5-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3ac5-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3ac5-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3ac5-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3ac5-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a3ac5-122">INPUTS</span></span>

### <span data-ttu-id="a3ac5-123">System. String</span><span class="sxs-lookup"><span data-stu-id="a3ac5-123">System.String</span></span>

## <span data-ttu-id="a3ac5-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a3ac5-124">OUTPUTS</span></span>

### <span data-ttu-id="a3ac5-125">Microsoft. Azure. Commands. OperationalInsights. Models. PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="a3ac5-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSManagementGroup</span></span>

## <span data-ttu-id="a3ac5-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a3ac5-126">NOTES</span></span>

## <span data-ttu-id="a3ac5-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a3ac5-127">RELATED LINKS</span></span>

[<span data-ttu-id="a3ac5-128">Cmdlets do Azure Operational insights</span><span class="sxs-lookup"><span data-stu-id="a3ac5-128">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="a3ac5-129">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="a3ac5-129">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)


