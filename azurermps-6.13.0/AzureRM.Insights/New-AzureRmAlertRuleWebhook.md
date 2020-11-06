---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 0137ECA3-37E1-4064-8A65-A582519E9017
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermalertrulewebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAlertRuleWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAlertRuleWebhook.md
ms.openlocfilehash: 619219a300bb1b7317ea4c8c5fce442d43b74ff1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429529"
---
# <span data-ttu-id="c9d65-101">New-AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="c9d65-101">New-AzureRmAlertRuleWebhook</span></span>

## <span data-ttu-id="c9d65-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c9d65-102">SYNOPSIS</span></span>
<span data-ttu-id="c9d65-103">Cria um webhook de regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="c9d65-103">Creates an alert rule webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c9d65-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c9d65-104">SYNTAX</span></span>

```
New-AzureRmAlertRuleWebhook [-ServiceUri] <String> [[-Property] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c9d65-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c9d65-105">DESCRIPTION</span></span>
<span data-ttu-id="c9d65-106">O cmdlet **New-AzureRmAlertRuleWebhook** cria um webhook de regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="c9d65-106">The **New-AzureRmAlertRuleWebhook** cmdlet creates an alert rule webhook.</span></span>

## <span data-ttu-id="c9d65-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c9d65-107">EXAMPLES</span></span>

### <span data-ttu-id="c9d65-108">Exemplo 1: criar uma regra de alerta webhook</span><span class="sxs-lookup"><span data-stu-id="c9d65-108">Example 1: Create an alert rule webhook</span></span>
```
PS C:\>New-AzureRmAlertRuleWebhook -ServiceUri "http://contoso.com"
```

<span data-ttu-id="c9d65-109">Esse comando cria um webhook de regra de alerta especificando somente o URI do serviço.</span><span class="sxs-lookup"><span data-stu-id="c9d65-109">This command creates an alert rule webhook by specifying only the service URI.</span></span>

### <span data-ttu-id="c9d65-110">Exemplo 2: criar um webhook com uma propriedade</span><span class="sxs-lookup"><span data-stu-id="c9d65-110">Example 2: Create a webhook with one property</span></span>
```
PS C:\>$Actual = New-AzureRmAlertRuleWebhook -ServiceUri "http://contoso.com" -Properties @{prop1 = 'value1'}
```

<span data-ttu-id="c9d65-111">Esse comando cria um webhook de regra de alerta para Contoso.com que tem uma propriedade e, em seguida, armazena-o na variável $Actual.</span><span class="sxs-lookup"><span data-stu-id="c9d65-111">This command creates an alert rule webhook for Contoso.com that has one property, and then stores it in the $Actual variable.</span></span>

## <span data-ttu-id="c9d65-112">OS</span><span class="sxs-lookup"><span data-stu-id="c9d65-112">PARAMETERS</span></span>

### <span data-ttu-id="c9d65-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9d65-113">-DefaultProfile</span></span>
<span data-ttu-id="c9d65-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="c9d65-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c9d65-115">-Propriedade</span><span class="sxs-lookup"><span data-stu-id="c9d65-115">-Property</span></span>
<span data-ttu-id="c9d65-116">Especifica a lista de propriedades no formato @ (Property1 = "valor1",....).</span><span class="sxs-lookup"><span data-stu-id="c9d65-116">Specifies the list of properties in the format @(property1 = 'value1',....).</span></span>

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

### <span data-ttu-id="c9d65-117">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="c9d65-117">-ServiceUri</span></span>
<span data-ttu-id="c9d65-118">Especifica o URI do serviço.</span><span class="sxs-lookup"><span data-stu-id="c9d65-118">Specifies the service URI.</span></span>

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

### <span data-ttu-id="c9d65-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9d65-119">CommonParameters</span></span>
<span data-ttu-id="c9d65-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9d65-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9d65-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9d65-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9d65-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c9d65-122">INPUTS</span></span>

### <span data-ttu-id="c9d65-123">System. String</span><span class="sxs-lookup"><span data-stu-id="c9d65-123">System.String</span></span>

### <span data-ttu-id="c9d65-124">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="c9d65-124">System.Collections.Hashtable</span></span>

## <span data-ttu-id="c9d65-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c9d65-125">OUTPUTS</span></span>

### <span data-ttu-id="c9d65-126">Microsoft. Azure. Management. monitor. Management. Models. RuleWebhookAction</span><span class="sxs-lookup"><span data-stu-id="c9d65-126">Microsoft.Azure.Management.Monitor.Management.Models.RuleWebhookAction</span></span>

## <span data-ttu-id="c9d65-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c9d65-127">NOTES</span></span>

## <span data-ttu-id="c9d65-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c9d65-128">RELATED LINKS</span></span>

[<span data-ttu-id="c9d65-129">Add-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="c9d65-129">Add-AzureRmLogAlertRule</span></span>](./Add-AzureRmLogAlertRule.md)

[<span data-ttu-id="c9d65-130">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="c9d65-130">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="c9d65-131">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="c9d65-131">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="c9d65-132">New-AzureRmAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="c9d65-132">New-AzureRmAlertRuleEmail</span></span>](./New-AzureRmAlertRuleEmail.md)

[<span data-ttu-id="c9d65-133">New-AzureRmAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="c9d65-133">New-AzureRmAutoscaleWebhook</span></span>](./New-AzureRmAutoscaleWebhook.md)


