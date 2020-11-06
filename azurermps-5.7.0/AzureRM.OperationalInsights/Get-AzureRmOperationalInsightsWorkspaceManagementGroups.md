---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: F29E0B9C-2479-44FB-B196-EAF97B69E6A6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightsworkspacemanagementgroups
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspaceManagementGroups.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspaceManagementGroups.md
ms.openlocfilehash: 808c92e987d30e97ee0ad2ed56b24be9b0f92a1d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602254"
---
# <span data-ttu-id="b4265-101">Get-AzureRmOperationalInsightsWorkspaceManagementGroups</span><span class="sxs-lookup"><span data-stu-id="b4265-101">Get-AzureRmOperationalInsightsWorkspaceManagementGroups</span></span>

## <span data-ttu-id="b4265-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b4265-102">SYNOPSIS</span></span>
<span data-ttu-id="b4265-103">Obtém detalhes dos grupos de gerenciamento conectados a um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="b4265-103">Gets details of management groups connected to a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b4265-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b4265-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsWorkspaceManagementGroups [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4265-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b4265-105">DESCRIPTION</span></span>
<span data-ttu-id="b4265-106">O cmdlet **Get-AzureRmOperationalInsightsWorkspaceManagementGroups** lista os grupos de gerenciamento que estão conectados a um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="b4265-106">The **Get-AzureRmOperationalInsightsWorkspaceManagementGroups** cmdlet lists the management groups that are connected to a workspace.</span></span>

## <span data-ttu-id="b4265-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b4265-107">EXAMPLES</span></span>

### <span data-ttu-id="b4265-108">Exemplo 1: obter grupos de gerenciamento pelo nome do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="b4265-108">Example 1: Get management groups by workspace name</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspaceManagementGroups -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="b4265-109">Esse comando obtém os grupos de gerenciamento do espaço de trabalho chamado MyWorkspace no grupo de recursos chamado ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="b4265-109">This command gets the management groups for the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="b4265-110">Exemplo 2: obter grupos de gerenciamento usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="b4265-110">Example 2: Get management groups by using the pipeline</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzureOperationalInsightsWorkspaceManagementGroups
```

<span data-ttu-id="b4265-111">Esse comando usa o cmdlet Get-AzureRmOperationalInsightsWorkspace para obter o espaço de trabalho chamado MyWorkspace e, em seguida, passa o espaço de trabalho para o cmdlet atual, que obtém os grupos de gerenciamento desse espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="b4265-111">This command uses the Get-AzureRmOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then passes the workspace to the current cmdlet, which gets the management groups for that workspace.</span></span>

## <span data-ttu-id="b4265-112">OS</span><span class="sxs-lookup"><span data-stu-id="b4265-112">PARAMETERS</span></span>

### <span data-ttu-id="b4265-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4265-113">-DefaultProfile</span></span>
<span data-ttu-id="b4265-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="b4265-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4265-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="b4265-115">-Name</span></span>
<span data-ttu-id="b4265-116">Especifica o nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="b4265-116">Specifies the workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4265-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4265-117">-ResourceGroupName</span></span>
<span data-ttu-id="b4265-118">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="b4265-118">Specifies the name of an Azure resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4265-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4265-119">CommonParameters</span></span>
<span data-ttu-id="b4265-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4265-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4265-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4265-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4265-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b4265-122">INPUTS</span></span>

### <span data-ttu-id="b4265-123">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="b4265-123">None</span></span>
<span data-ttu-id="b4265-124">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="b4265-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b4265-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b4265-125">OUTPUTS</span></span>

### <span data-ttu-id="b4265-126">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. OperationalInsights. Models. PSManagementGroup]</span><span class="sxs-lookup"><span data-stu-id="b4265-126">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.OperationalInsights.Models.PSManagementGroup]</span></span>

## <span data-ttu-id="b4265-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b4265-127">NOTES</span></span>

## <span data-ttu-id="b4265-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b4265-128">RELATED LINKS</span></span>

[<span data-ttu-id="b4265-129">Cmdlets do Azure Operational insights</span><span class="sxs-lookup"><span data-stu-id="b4265-129">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="b4265-130">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="b4265-130">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)


