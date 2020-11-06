---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 35C6E85B-E5E1-44E8-86E8-F18E197F69DC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightslinktargets
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsLinkTargets.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsLinkTargets.md
ms.openlocfilehash: 64e74b2c9d4aa5f22d48bb6cb80c5a1952424c38
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428851"
---
# <span data-ttu-id="cfbc0-101">Get-AzureRmOperationalInsightsLinkTargets</span><span class="sxs-lookup"><span data-stu-id="cfbc0-101">Get-AzureRmOperationalInsightsLinkTargets</span></span>

## <span data-ttu-id="cfbc0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cfbc0-102">SYNOPSIS</span></span>
<span data-ttu-id="cfbc0-103">Obtém contas que não estão associadas a uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="cfbc0-103">Gets accounts that are not associated with a subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cfbc0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cfbc0-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsLinkTargets [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cfbc0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cfbc0-105">DESCRIPTION</span></span>
<span data-ttu-id="cfbc0-106">O cmdlet **Get-AzureRmOperationalInsightsLinkTargets** lista contas existentes que não estão associadas a uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="cfbc0-106">The **Get-AzureRmOperationalInsightsLinkTargets** cmdlet lists existing accounts that are not associated with an Azure subscription.</span></span>
<span data-ttu-id="cfbc0-107">Para vincular um novo espaço de trabalho a uma conta existente, use uma ID de cliente retornada por essa operação na propriedade ID do cliente de um novo espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="cfbc0-107">To link a new workspace to an existing account, use a customer ID returned by this operation in the customer ID property of a new workspace.</span></span>

## <span data-ttu-id="cfbc0-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cfbc0-108">EXAMPLES</span></span>

### <span data-ttu-id="cfbc0-109">Exemplo 1: obter contas não vinculadas</span><span class="sxs-lookup"><span data-stu-id="cfbc0-109">Example 1: Get unlinked accounts</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsLinkTargets
```

<span data-ttu-id="cfbc0-110">Esse comando obtém contas não vinculadas que pertencem à identificação do chamador.</span><span class="sxs-lookup"><span data-stu-id="cfbc0-110">This command gets unlinked accounts that are owned by the caller's ID.</span></span>

## <span data-ttu-id="cfbc0-111">OS</span><span class="sxs-lookup"><span data-stu-id="cfbc0-111">PARAMETERS</span></span>

### <span data-ttu-id="cfbc0-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfbc0-112">-DefaultProfile</span></span>
<span data-ttu-id="cfbc0-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="cfbc0-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cfbc0-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfbc0-114">CommonParameters</span></span>
<span data-ttu-id="cfbc0-115">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cfbc0-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfbc0-116">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cfbc0-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfbc0-117">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cfbc0-117">INPUTS</span></span>

### <span data-ttu-id="cfbc0-118">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="cfbc0-118">None</span></span>
<span data-ttu-id="cfbc0-119">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="cfbc0-119">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="cfbc0-120">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cfbc0-120">OUTPUTS</span></span>

### <span data-ttu-id="cfbc0-121">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. OperationalInsights. Models. PSAccount]</span><span class="sxs-lookup"><span data-stu-id="cfbc0-121">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.OperationalInsights.Models.PSAccount]</span></span>

## <span data-ttu-id="cfbc0-122">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cfbc0-122">NOTES</span></span>

## <span data-ttu-id="cfbc0-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cfbc0-123">RELATED LINKS</span></span>

[<span data-ttu-id="cfbc0-124">Cmdlets do Azure Operational insights</span><span class="sxs-lookup"><span data-stu-id="cfbc0-124">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


