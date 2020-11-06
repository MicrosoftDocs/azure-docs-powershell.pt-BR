---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 674A11E4-36B9-4075-9F4E-952BD9FF07A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermautoscalewebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleWebhook.md
ms.openlocfilehash: 607976539e6bf93a0fa947741a4af4d4a7d34b67
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602480"
---
# <span data-ttu-id="eb1eb-101">New-AzureRmAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="eb1eb-101">New-AzureRmAutoscaleWebhook</span></span>

## <span data-ttu-id="eb1eb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="eb1eb-102">SYNOPSIS</span></span>
<span data-ttu-id="eb1eb-103">Cria um webhook de autoescala.</span><span class="sxs-lookup"><span data-stu-id="eb1eb-103">Creates an Autoscale webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eb1eb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="eb1eb-104">SYNTAX</span></span>

```
New-AzureRmAutoscaleWebhook [-ServiceUri] <String> [[-Property] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eb1eb-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="eb1eb-105">DESCRIPTION</span></span>
<span data-ttu-id="eb1eb-106">O cmdlet **New-AzureRmAutoscaleWebhook** cria um webhook de dimensionamento automático.</span><span class="sxs-lookup"><span data-stu-id="eb1eb-106">The **New-AzureRmAutoscaleWebhook** cmdlet creates an Autoscale webhook.</span></span>

## <span data-ttu-id="eb1eb-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="eb1eb-107">EXAMPLES</span></span>

## <span data-ttu-id="eb1eb-108">OS</span><span class="sxs-lookup"><span data-stu-id="eb1eb-108">PARAMETERS</span></span>

### <span data-ttu-id="eb1eb-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb1eb-109">-DefaultProfile</span></span>
<span data-ttu-id="eb1eb-110">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="eb1eb-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eb1eb-111">-Propriedade</span><span class="sxs-lookup"><span data-stu-id="eb1eb-111">-Property</span></span>
<span data-ttu-id="eb1eb-112">Especifica a lista de propriedades no formato @ (Property1 = "valor1",....).</span><span class="sxs-lookup"><span data-stu-id="eb1eb-112">Specifies the list of properties in the format @(property1 = 'value1',....).</span></span>

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

### <span data-ttu-id="eb1eb-113">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="eb1eb-113">-ServiceUri</span></span>
<span data-ttu-id="eb1eb-114">Especifica o URI do serviço.</span><span class="sxs-lookup"><span data-stu-id="eb1eb-114">Specifies the service URI.</span></span>

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

### <span data-ttu-id="eb1eb-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb1eb-115">CommonParameters</span></span>
<span data-ttu-id="eb1eb-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb1eb-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb1eb-117">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb1eb-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb1eb-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="eb1eb-118">INPUTS</span></span>

### <span data-ttu-id="eb1eb-119">System. String</span><span class="sxs-lookup"><span data-stu-id="eb1eb-119">System.String</span></span>

### <span data-ttu-id="eb1eb-120">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="eb1eb-120">System.Collections.Hashtable</span></span>

## <span data-ttu-id="eb1eb-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="eb1eb-121">OUTPUTS</span></span>

### <span data-ttu-id="eb1eb-122">Microsoft. Azure. Management. monitor. Management. Models. WebhookNotification</span><span class="sxs-lookup"><span data-stu-id="eb1eb-122">Microsoft.Azure.Management.Monitor.Management.Models.WebhookNotification</span></span>

## <span data-ttu-id="eb1eb-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="eb1eb-123">NOTES</span></span>

## <span data-ttu-id="eb1eb-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="eb1eb-124">RELATED LINKS</span></span>

[<span data-ttu-id="eb1eb-125">New-AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="eb1eb-125">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)


