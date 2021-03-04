---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 0F9D72C1-2E42-4A67-9FDE-6344F5DE6C30
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/get-azoperationalinsightsintelligencepack
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsIntelligencePack.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsIntelligencePack.md
ms.openlocfilehash: a56fd0303e6f610468c9f2784396023fd20edef4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887089"
---
# <span data-ttu-id="060c5-101">Get-AzOperationalInsightsIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="060c5-101">Get-AzOperationalInsightsIntelligencePack</span></span>

## <span data-ttu-id="060c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="060c5-102">SYNOPSIS</span></span>
<span data-ttu-id="060c5-103">Obtém os Pacotes de Inteligência disponíveis.</span><span class="sxs-lookup"><span data-stu-id="060c5-103">Gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="060c5-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="060c5-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsIntelligencePack [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="060c5-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="060c5-105">DESCRIPTION</span></span>
<span data-ttu-id="060c5-106">O cmdlet **Get-AzOperationalInsightsIntelligencePack** obtém os Pacotes de Inteligência disponíveis.</span><span class="sxs-lookup"><span data-stu-id="060c5-106">The **Get-AzOperationalInsightsIntelligencePack** cmdlet gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="060c5-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="060c5-107">EXAMPLES</span></span>

### <span data-ttu-id="060c5-108">Exemplo 1: Obter Pacotes de Inteligência</span><span class="sxs-lookup"><span data-stu-id="060c5-108">Example 1: Get Intelligence Packs</span></span>
```
PS C:\>Get-AzOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="060c5-109">Este comando obtém os Pacotes de Inteligência disponíveis.</span><span class="sxs-lookup"><span data-stu-id="060c5-109">This command gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="060c5-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="060c5-110">PARAMETERS</span></span>

### <span data-ttu-id="060c5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="060c5-111">-DefaultProfile</span></span>
<span data-ttu-id="060c5-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="060c5-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="060c5-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="060c5-113">-ResourceGroupName</span></span>
<span data-ttu-id="060c5-114">Especifica o nome de um grupo de recursos do Azure que contém um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="060c5-114">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="060c5-115">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="060c5-115">-WorkspaceName</span></span>
<span data-ttu-id="060c5-116">Especifica o nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="060c5-116">Specifies the workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="060c5-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="060c5-117">CommonParameters</span></span>
<span data-ttu-id="060c5-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="060c5-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="060c5-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="060c5-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="060c5-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="060c5-120">INPUTS</span></span>

### <span data-ttu-id="060c5-121">System.String</span><span class="sxs-lookup"><span data-stu-id="060c5-121">System.String</span></span>

## <span data-ttu-id="060c5-122">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="060c5-122">OUTPUTS</span></span>

### <span data-ttu-id="060c5-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="060c5-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSIntelligencePack</span></span>

## <span data-ttu-id="060c5-124">NOTES</span><span class="sxs-lookup"><span data-stu-id="060c5-124">NOTES</span></span>

## <span data-ttu-id="060c5-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="060c5-125">RELATED LINKS</span></span>

[<span data-ttu-id="060c5-126">Cmdlets do Insights Operacionais do Azure</span><span class="sxs-lookup"><span data-stu-id="060c5-126">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


