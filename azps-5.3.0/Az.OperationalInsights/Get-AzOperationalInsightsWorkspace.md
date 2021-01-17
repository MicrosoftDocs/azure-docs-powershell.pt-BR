---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: F94415DA-1A4A-4D37-A626-1EDF5D1EFE74
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 1a0d36c2e871bd0495216bce18d84dff60e1044d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98434561"
---
# <span data-ttu-id="06f8c-101">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="06f8c-101">Get-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="06f8c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="06f8c-102">SYNOPSIS</span></span>
<span data-ttu-id="06f8c-103">Obtém informações sobre um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="06f8c-103">Gets information about a workspace.</span></span>

## <span data-ttu-id="06f8c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="06f8c-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsWorkspace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06f8c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="06f8c-105">DESCRIPTION</span></span>
<span data-ttu-id="06f8c-106">O cmdlet **Get-AzOperationalInsightsWorkspace** Obtém informações sobre um espaço de trabalho existente.</span><span class="sxs-lookup"><span data-stu-id="06f8c-106">The **Get-AzOperationalInsightsWorkspace** cmdlet gets information about an existing workspace.</span></span>
<span data-ttu-id="06f8c-107">Se você especificar um nome de espaço de trabalho, este cmdlet obterá informações sobre esse espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="06f8c-107">If you specify a workspace name, this cmdlet gets information about that workspace.</span></span>
<span data-ttu-id="06f8c-108">Se você não especificar um nome, esse cmdlet obterá informações sobre todos os espaços de trabalho em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="06f8c-108">If you do not specify a name, this cmdlet gets information about all workspaces in a resource group.</span></span>
<span data-ttu-id="06f8c-109">Se você não especificar um nome e um grupo de recursos, esse cmdlet obterá informações sobre todos os espaços de trabalho em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="06f8c-109">If you do not specify a name and resource group, this cmdlet gets information about all workspaces in a subscription.</span></span>

## <span data-ttu-id="06f8c-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="06f8c-110">EXAMPLES</span></span>

### <span data-ttu-id="06f8c-111">Exemplo 1: obter um espaço de trabalho por nome</span><span class="sxs-lookup"><span data-stu-id="06f8c-111">Example 1: Get a workspace by name</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -Name "MyWorkspace" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="06f8c-112">Esse comando obtém um espaço de trabalho chamado MyWorkspace no grupo de recursos chamado ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="06f8c-112">This command gets a workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="06f8c-113">OS</span><span class="sxs-lookup"><span data-stu-id="06f8c-113">PARAMETERS</span></span>

### <span data-ttu-id="06f8c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06f8c-114">-DefaultProfile</span></span>
<span data-ttu-id="06f8c-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="06f8c-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="06f8c-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="06f8c-116">-Name</span></span>
<span data-ttu-id="06f8c-117">Especifica o nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="06f8c-117">Specifies the workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06f8c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06f8c-118">-ResourceGroupName</span></span>
<span data-ttu-id="06f8c-119">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="06f8c-119">Specifies the name of an Azure resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06f8c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06f8c-120">CommonParameters</span></span>
<span data-ttu-id="06f8c-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06f8c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06f8c-122">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06f8c-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06f8c-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="06f8c-123">INPUTS</span></span>

### <span data-ttu-id="06f8c-124">System. String</span><span class="sxs-lookup"><span data-stu-id="06f8c-124">System.String</span></span>

## <span data-ttu-id="06f8c-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="06f8c-125">OUTPUTS</span></span>

### <span data-ttu-id="06f8c-126">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="06f8c-126">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="06f8c-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="06f8c-127">NOTES</span></span>

## <span data-ttu-id="06f8c-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="06f8c-128">RELATED LINKS</span></span>

[<span data-ttu-id="06f8c-129">Cmdlets do Azure Operational insights</span><span class="sxs-lookup"><span data-stu-id="06f8c-129">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


