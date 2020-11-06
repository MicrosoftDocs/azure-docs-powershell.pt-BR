---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 0F9D72C1-2E42-4A67-9FDE-6344F5DE6C30
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsIntelligencePacks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsIntelligencePacks.md
ms.openlocfilehash: 56bc2dd74f17daa9a56eac8ebd5128e6f074fe13
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429190"
---
# <span data-ttu-id="258c4-101">Get-AzureRmOperationalInsightsIntelligencePacks</span><span class="sxs-lookup"><span data-stu-id="258c4-101">Get-AzureRmOperationalInsightsIntelligencePacks</span></span>

## <span data-ttu-id="258c4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="258c4-102">SYNOPSIS</span></span>
<span data-ttu-id="258c4-103">Obtém os pacotes de inteligência disponíveis.</span><span class="sxs-lookup"><span data-stu-id="258c4-103">Gets the available Intelligence Packs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="258c4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="258c4-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsIntelligencePacks [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="258c4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="258c4-105">DESCRIPTION</span></span>
<span data-ttu-id="258c4-106">O cmdlet **Get-AzureRmOperationalInsightsIntelligencePacks** Obtém os pacotes de inteligência disponíveis.</span><span class="sxs-lookup"><span data-stu-id="258c4-106">The **Get-AzureRmOperationalInsightsIntelligencePacks** cmdlet gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="258c4-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="258c4-107">EXAMPLES</span></span>

### <span data-ttu-id="258c4-108">Exemplo 1: obter pacotes de inteligência</span><span class="sxs-lookup"><span data-stu-id="258c4-108">Example 1: Get Intelligence Packs</span></span>
```
PS C:\>Get-AzureOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="258c4-109">Este comando obtém os pacotes de inteligência disponíveis.</span><span class="sxs-lookup"><span data-stu-id="258c4-109">This command gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="258c4-110">OS</span><span class="sxs-lookup"><span data-stu-id="258c4-110">PARAMETERS</span></span>

### <span data-ttu-id="258c4-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="258c4-111">-ResourceGroupName</span></span>
<span data-ttu-id="258c4-112">Especifica o nome de um grupo de recursos do Azure que contém um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="258c4-112">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="258c4-113">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="258c4-113">-WorkspaceName</span></span>
<span data-ttu-id="258c4-114">Especifica o nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="258c4-114">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="258c4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="258c4-115">-DefaultProfile</span></span>
<span data-ttu-id="258c4-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="258c4-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="258c4-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="258c4-117">CommonParameters</span></span>
<span data-ttu-id="258c4-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="258c4-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="258c4-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="258c4-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="258c4-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="258c4-120">INPUTS</span></span>

## <span data-ttu-id="258c4-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="258c4-121">OUTPUTS</span></span>

### <span data-ttu-id="258c4-122">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. OperationalInsights. Models. PSIntelligencePack]</span><span class="sxs-lookup"><span data-stu-id="258c4-122">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.OperationalInsights.Models.PSIntelligencePack]</span></span>

## <span data-ttu-id="258c4-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="258c4-123">NOTES</span></span>

## <span data-ttu-id="258c4-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="258c4-124">RELATED LINKS</span></span>

[<span data-ttu-id="258c4-125">Cmdlets do Azure Operational insights</span><span class="sxs-lookup"><span data-stu-id="258c4-125">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


