---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 0F9D72C1-2E42-4A67-9FDE-6344F5DE6C30
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightsintelligencepacks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsIntelligencePacks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsIntelligencePacks.md
ms.openlocfilehash: 0e63b6926f635a4260e6e3c9d658afa410f29966
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428854"
---
# <span data-ttu-id="95b12-101">Get-AzureRmOperationalInsightsIntelligencePacks</span><span class="sxs-lookup"><span data-stu-id="95b12-101">Get-AzureRmOperationalInsightsIntelligencePacks</span></span>

## <span data-ttu-id="95b12-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="95b12-102">SYNOPSIS</span></span>
<span data-ttu-id="95b12-103">Obtém os pacotes de inteligência disponíveis.</span><span class="sxs-lookup"><span data-stu-id="95b12-103">Gets the available Intelligence Packs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="95b12-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="95b12-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsIntelligencePacks [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95b12-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="95b12-105">DESCRIPTION</span></span>
<span data-ttu-id="95b12-106">O cmdlet **Get-AzureRmOperationalInsightsIntelligencePacks** Obtém os pacotes de inteligência disponíveis.</span><span class="sxs-lookup"><span data-stu-id="95b12-106">The **Get-AzureRmOperationalInsightsIntelligencePacks** cmdlet gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="95b12-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="95b12-107">EXAMPLES</span></span>

### <span data-ttu-id="95b12-108">Exemplo 1: obter pacotes de inteligência</span><span class="sxs-lookup"><span data-stu-id="95b12-108">Example 1: Get Intelligence Packs</span></span>
```
PS C:\>Get-AzureOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="95b12-109">Este comando obtém os pacotes de inteligência disponíveis.</span><span class="sxs-lookup"><span data-stu-id="95b12-109">This command gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="95b12-110">OS</span><span class="sxs-lookup"><span data-stu-id="95b12-110">PARAMETERS</span></span>

### <span data-ttu-id="95b12-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95b12-111">-DefaultProfile</span></span>
<span data-ttu-id="95b12-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="95b12-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="95b12-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95b12-113">-ResourceGroupName</span></span>
<span data-ttu-id="95b12-114">Especifica o nome de um grupo de recursos do Azure que contém um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="95b12-114">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="95b12-115">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="95b12-115">-WorkspaceName</span></span>
<span data-ttu-id="95b12-116">Especifica o nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="95b12-116">Specifies the workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95b12-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95b12-117">CommonParameters</span></span>
<span data-ttu-id="95b12-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95b12-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95b12-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95b12-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95b12-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="95b12-120">INPUTS</span></span>

### <span data-ttu-id="95b12-121">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="95b12-121">None</span></span>
<span data-ttu-id="95b12-122">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="95b12-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="95b12-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="95b12-123">OUTPUTS</span></span>

### <span data-ttu-id="95b12-124">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. OperationalInsights. Models. PSIntelligencePack]</span><span class="sxs-lookup"><span data-stu-id="95b12-124">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.OperationalInsights.Models.PSIntelligencePack]</span></span>

## <span data-ttu-id="95b12-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="95b12-125">NOTES</span></span>

## <span data-ttu-id="95b12-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="95b12-126">RELATED LINKS</span></span>

[<span data-ttu-id="95b12-127">Cmdlets do Azure Operational insights</span><span class="sxs-lookup"><span data-stu-id="95b12-127">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


