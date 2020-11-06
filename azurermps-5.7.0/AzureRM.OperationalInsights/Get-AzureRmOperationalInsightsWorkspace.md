---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: F94415DA-1A4A-4D37-A626-1EDF5D1EFE74
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspace.md
ms.openlocfilehash: b2bd8855d9c8b125b4bef72f42f0bd4a63071adb
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "93441606"
---
# <span data-ttu-id="f80ea-101">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="f80ea-101">Get-AzureRmOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="f80ea-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f80ea-102">SYNOPSIS</span></span>
<span data-ttu-id="f80ea-103">Obtém informações sobre um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="f80ea-103">Gets information about a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f80ea-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f80ea-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsWorkspace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f80ea-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f80ea-105">DESCRIPTION</span></span>
<span data-ttu-id="f80ea-106">O cmdlet **Get-AzureRmOperationalInsightsWorkspace** Obtém informações sobre um espaço de trabalho existente.</span><span class="sxs-lookup"><span data-stu-id="f80ea-106">The **Get-AzureRmOperationalInsightsWorkspace** cmdlet gets information about an existing workspace.</span></span>
<span data-ttu-id="f80ea-107">Se você especificar um nome de espaço de trabalho, este cmdlet obterá informações sobre esse espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="f80ea-107">If you specify a workspace name, this cmdlet gets information about that workspace.</span></span>
<span data-ttu-id="f80ea-108">Se você não especificar um nome, esse cmdlet obterá informações sobre todos os espaços de trabalho em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f80ea-108">If you do not specify a name, this cmdlet gets information about all workspaces in a resource group.</span></span>
<span data-ttu-id="f80ea-109">Se você não especificar um nome e um grupo de recursos, esse cmdlet obterá informações sobre todos os espaços de trabalho em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="f80ea-109">If you do not specify a name and resource group, this cmdlet gets information about all workspaces in a subscription.</span></span>

## <span data-ttu-id="f80ea-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f80ea-110">EXAMPLES</span></span>

### <span data-ttu-id="f80ea-111">Exemplo 1: obter um espaço de trabalho por nome</span><span class="sxs-lookup"><span data-stu-id="f80ea-111">Example 1: Get a workspace by name</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspace -Name "MyWorkspace" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="f80ea-112">Esse comando obtém um espaço de trabalho chamado MyWorkspace no grupo de recursos chamado ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="f80ea-112">This command gets a workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="f80ea-113">OS</span><span class="sxs-lookup"><span data-stu-id="f80ea-113">PARAMETERS</span></span>

### <span data-ttu-id="f80ea-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f80ea-114">-DefaultProfile</span></span>
<span data-ttu-id="f80ea-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="f80ea-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f80ea-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="f80ea-116">-Name</span></span>
<span data-ttu-id="f80ea-117">Especifica o nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="f80ea-117">Specifies the workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f80ea-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f80ea-118">-ResourceGroupName</span></span>
<span data-ttu-id="f80ea-119">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="f80ea-119">Specifies the name of an Azure resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f80ea-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f80ea-120">CommonParameters</span></span>
<span data-ttu-id="f80ea-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f80ea-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f80ea-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f80ea-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f80ea-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f80ea-123">INPUTS</span></span>

### <span data-ttu-id="f80ea-124">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="f80ea-124">None</span></span>
<span data-ttu-id="f80ea-125">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="f80ea-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f80ea-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f80ea-126">OUTPUTS</span></span>

### <span data-ttu-id="f80ea-127">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace]</span><span class="sxs-lookup"><span data-stu-id="f80ea-127">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace]</span></span>

### <span data-ttu-id="f80ea-128">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="f80ea-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="f80ea-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f80ea-129">NOTES</span></span>

## <span data-ttu-id="f80ea-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f80ea-130">RELATED LINKS</span></span>

[<span data-ttu-id="f80ea-131">Cmdlets do Azure Operational insights</span><span class="sxs-lookup"><span data-stu-id="f80ea-131">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


