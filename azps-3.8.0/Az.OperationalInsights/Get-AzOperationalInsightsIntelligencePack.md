---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 0F9D72C1-2E42-4A67-9FDE-6344F5DE6C30
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsintelligencepack
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsIntelligencePack.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsIntelligencePack.md
ms.openlocfilehash: b628f0050ab0aa4b16864b510f4426b940226ec5
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93947273"
---
# <span data-ttu-id="4ee54-101">Get-AzOperationalInsightsIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="4ee54-101">Get-AzOperationalInsightsIntelligencePack</span></span>

## <span data-ttu-id="4ee54-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4ee54-102">SYNOPSIS</span></span>
<span data-ttu-id="4ee54-103">Obtém os pacotes de inteligência disponíveis.</span><span class="sxs-lookup"><span data-stu-id="4ee54-103">Gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="4ee54-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4ee54-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsIntelligencePack [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ee54-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4ee54-105">DESCRIPTION</span></span>
<span data-ttu-id="4ee54-106">O cmdlet **Get-AzOperationalInsightsIntelligencePack** Obtém os pacotes de inteligência disponíveis.</span><span class="sxs-lookup"><span data-stu-id="4ee54-106">The **Get-AzOperationalInsightsIntelligencePack** cmdlet gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="4ee54-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4ee54-107">EXAMPLES</span></span>

### <span data-ttu-id="4ee54-108">Exemplo 1: obter pacotes de inteligência</span><span class="sxs-lookup"><span data-stu-id="4ee54-108">Example 1: Get Intelligence Packs</span></span>
```
PS C:\>Get-AzOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="4ee54-109">Este comando obtém os pacotes de inteligência disponíveis.</span><span class="sxs-lookup"><span data-stu-id="4ee54-109">This command gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="4ee54-110">OS</span><span class="sxs-lookup"><span data-stu-id="4ee54-110">PARAMETERS</span></span>

### <span data-ttu-id="4ee54-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ee54-111">-DefaultProfile</span></span>
<span data-ttu-id="4ee54-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="4ee54-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4ee54-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ee54-113">-ResourceGroupName</span></span>
<span data-ttu-id="4ee54-114">Especifica o nome de um grupo de recursos do Azure que contém um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="4ee54-114">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="4ee54-115">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="4ee54-115">-WorkspaceName</span></span>
<span data-ttu-id="4ee54-116">Especifica o nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="4ee54-116">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="4ee54-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ee54-117">CommonParameters</span></span>
<span data-ttu-id="4ee54-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ee54-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ee54-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ee54-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ee54-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4ee54-120">INPUTS</span></span>

### <span data-ttu-id="4ee54-121">System. String</span><span class="sxs-lookup"><span data-stu-id="4ee54-121">System.String</span></span>

## <span data-ttu-id="4ee54-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4ee54-122">OUTPUTS</span></span>

### <span data-ttu-id="4ee54-123">Microsoft. Azure. Commands. OperationalInsights. Models. PSIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="4ee54-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSIntelligencePack</span></span>

## <span data-ttu-id="4ee54-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4ee54-124">NOTES</span></span>

## <span data-ttu-id="4ee54-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4ee54-125">RELATED LINKS</span></span>

[<span data-ttu-id="4ee54-126">Cmdlets do Azure Operational insights</span><span class="sxs-lookup"><span data-stu-id="4ee54-126">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)


