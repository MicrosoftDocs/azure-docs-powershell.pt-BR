---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 35C6E85B-E5E1-44E8-86E8-F18E197F69DC
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightslinktarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkTarget.md
ms.openlocfilehash: beb4fad10424a94b2623070508ac827ea7b15306
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93784994"
---
# <span data-ttu-id="dbbf7-101">Get-AzOperationalInsightsLinkTarget</span><span class="sxs-lookup"><span data-stu-id="dbbf7-101">Get-AzOperationalInsightsLinkTarget</span></span>

## <span data-ttu-id="dbbf7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dbbf7-102">SYNOPSIS</span></span>
<span data-ttu-id="dbbf7-103">Obtém contas que não estão associadas a uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="dbbf7-103">Gets accounts that are not associated with a subscription.</span></span>

## <span data-ttu-id="dbbf7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dbbf7-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsLinkTarget [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dbbf7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dbbf7-105">DESCRIPTION</span></span>
<span data-ttu-id="dbbf7-106">O cmdlet **Get-AzOperationalInsightsLinkTarget** lista contas existentes que não estão associadas a uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="dbbf7-106">The **Get-AzOperationalInsightsLinkTarget** cmdlet lists existing accounts that are not associated with an Azure subscription.</span></span>
<span data-ttu-id="dbbf7-107">Para vincular um novo espaço de trabalho a uma conta existente, use uma ID de cliente retornada por essa operação na propriedade ID do cliente de um novo espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="dbbf7-107">To link a new workspace to an existing account, use a customer ID returned by this operation in the customer ID property of a new workspace.</span></span>

## <span data-ttu-id="dbbf7-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dbbf7-108">EXAMPLES</span></span>

### <span data-ttu-id="dbbf7-109">Exemplo 1: obter contas não vinculadas</span><span class="sxs-lookup"><span data-stu-id="dbbf7-109">Example 1: Get unlinked accounts</span></span>
```
PS C:\>Get-AzOperationalInsightsLinkTarget
```

<span data-ttu-id="dbbf7-110">Esse comando obtém contas não vinculadas que pertencem à identificação do chamador.</span><span class="sxs-lookup"><span data-stu-id="dbbf7-110">This command gets unlinked accounts that are owned by the caller's ID.</span></span>

## <span data-ttu-id="dbbf7-111">OS</span><span class="sxs-lookup"><span data-stu-id="dbbf7-111">PARAMETERS</span></span>

### <span data-ttu-id="dbbf7-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbbf7-112">-DefaultProfile</span></span>
<span data-ttu-id="dbbf7-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="dbbf7-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dbbf7-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbbf7-114">CommonParameters</span></span>
<span data-ttu-id="dbbf7-115">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbbf7-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbbf7-116">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dbbf7-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbbf7-117">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dbbf7-117">INPUTS</span></span>

### <span data-ttu-id="dbbf7-118">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="dbbf7-118">None</span></span>

## <span data-ttu-id="dbbf7-119">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dbbf7-119">OUTPUTS</span></span>

### <span data-ttu-id="dbbf7-120">Microsoft. Azure. Commands. OperationalInsights. Models. PSAccount</span><span class="sxs-lookup"><span data-stu-id="dbbf7-120">Microsoft.Azure.Commands.OperationalInsights.Models.PSAccount</span></span>

## <span data-ttu-id="dbbf7-121">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dbbf7-121">NOTES</span></span>

## <span data-ttu-id="dbbf7-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dbbf7-122">RELATED LINKS</span></span>

[<span data-ttu-id="dbbf7-123">Cmdlets do Azure Operational insights</span><span class="sxs-lookup"><span data-stu-id="dbbf7-123">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)


