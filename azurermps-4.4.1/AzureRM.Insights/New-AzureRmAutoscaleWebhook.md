---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 674A11E4-36B9-4075-9F4E-952BD9FF07A7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleWebhook.md
ms.openlocfilehash: 2fc67e4f50d3c0a045ed6f0e6d82d5bf46d10c25
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432622"
---
# <span data-ttu-id="c197b-101">New-AzureRmAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="c197b-101">New-AzureRmAutoscaleWebhook</span></span>

## <span data-ttu-id="c197b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c197b-102">SYNOPSIS</span></span>
<span data-ttu-id="c197b-103">Cria um webhook de autoescala.</span><span class="sxs-lookup"><span data-stu-id="c197b-103">Creates an Autoscale webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c197b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c197b-104">SYNTAX</span></span>

```
New-AzureRmAutoscaleWebhook [-ServiceUri] <String> [[-Properties] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c197b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c197b-105">DESCRIPTION</span></span>
<span data-ttu-id="c197b-106">O cmdlet **New-AzureRmAutoscaleWebhook** cria um webhook de dimensionamento automático.</span><span class="sxs-lookup"><span data-stu-id="c197b-106">The **New-AzureRmAutoscaleWebhook** cmdlet creates an Autoscale webhook.</span></span>

## <span data-ttu-id="c197b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c197b-107">EXAMPLES</span></span>

## <span data-ttu-id="c197b-108">OS</span><span class="sxs-lookup"><span data-stu-id="c197b-108">PARAMETERS</span></span>

### <span data-ttu-id="c197b-109">-Propriedades</span><span class="sxs-lookup"><span data-stu-id="c197b-109">-Properties</span></span>
<span data-ttu-id="c197b-110">Especifica a lista de propriedades no formato @ (Property1 = "valor1",....).</span><span class="sxs-lookup"><span data-stu-id="c197b-110">Specifies the list of properties in the format @(property1 = 'value1',....).</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c197b-111">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="c197b-111">-ServiceUri</span></span>
<span data-ttu-id="c197b-112">Especifica o URI do serviço.</span><span class="sxs-lookup"><span data-stu-id="c197b-112">Specifies the service URI.</span></span>

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

### <span data-ttu-id="c197b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c197b-113">-DefaultProfile</span></span>
<span data-ttu-id="c197b-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c197b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c197b-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c197b-115">CommonParameters</span></span>
<span data-ttu-id="c197b-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c197b-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c197b-117">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c197b-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c197b-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c197b-118">INPUTS</span></span>

## <span data-ttu-id="c197b-119">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c197b-119">OUTPUTS</span></span>

### <span data-ttu-id="c197b-120">Microsoft. Azure. Management. monitor. Management. Models. WebhookNotification</span><span class="sxs-lookup"><span data-stu-id="c197b-120">Microsoft.Azure.Management.Monitor.Management.Models.WebhookNotification</span></span>

## <span data-ttu-id="c197b-121">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c197b-121">NOTES</span></span>

## <span data-ttu-id="c197b-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c197b-122">RELATED LINKS</span></span>

[<span data-ttu-id="c197b-123">New-AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="c197b-123">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)


