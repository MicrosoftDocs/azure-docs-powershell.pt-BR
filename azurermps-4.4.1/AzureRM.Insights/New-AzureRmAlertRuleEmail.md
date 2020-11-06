---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B1000C10-265E-4465-B167-F1251470BE3E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAlertRuleEmail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAlertRuleEmail.md
ms.openlocfilehash: 85479695efee536aac054751fdd5a48d4b5de5ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432208"
---
# <span data-ttu-id="7abd3-101">New-AzureRmAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="7abd3-101">New-AzureRmAlertRuleEmail</span></span>

## <span data-ttu-id="7abd3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7abd3-102">SYNOPSIS</span></span>
<span data-ttu-id="7abd3-103">Cria uma ação de email para uma regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="7abd3-103">Creates an email action for an alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7abd3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7abd3-104">SYNTAX</span></span>

```
New-AzureRmAlertRuleEmail [[-CustomEmails] <String[]>] [-SendToServiceOwners]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7abd3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7abd3-105">DESCRIPTION</span></span>
<span data-ttu-id="7abd3-106">O cmdlet **New-AzureRmAlertRuleEmail** cria uma ação de email para uma regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="7abd3-106">The **New-AzureRmAlertRuleEmail** cmdlet creates an e-mail action for an alert rule.</span></span>

## <span data-ttu-id="7abd3-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7abd3-107">EXAMPLES</span></span>

### <span data-ttu-id="7abd3-108">Exemplo 1: criar uma ação de email de regra de alerta para proprietários de serviço</span><span class="sxs-lookup"><span data-stu-id="7abd3-108">Example 1: Create an alert rule email action for service owners</span></span>
```
PS C:\>New-AzureRmAlertRuleEmail -SendToServiceOwners
```

<span data-ttu-id="7abd3-109">Esse comando cria uma ação de email de regra de alerta para enviar para seus proprietários de serviço quando uma regra de alerta é acionada.</span><span class="sxs-lookup"><span data-stu-id="7abd3-109">This command creates an alert rule email action to send for its service owners when an alert rule is fired.</span></span>

### <span data-ttu-id="7abd3-110">Exemplo 2: criar uma regra de alerta ação de email para proprietários que não são de serviço</span><span class="sxs-lookup"><span data-stu-id="7abd3-110">Example 2: Create an alert rule email action for non-service owners</span></span>
```
PS C:\>New-AzureRmAlertRuleEmail -CustomEmails "pattif@contoso.com, davidchew@contoso.net"
```

<span data-ttu-id="7abd3-111">Esse comando cria uma ação de email de regra de alerta para os endereços de email especificados, mas não para os proprietários do serviço.</span><span class="sxs-lookup"><span data-stu-id="7abd3-111">This command creates an alert rule email action for the specified email addresses, but not for the service owners.</span></span>

### <span data-ttu-id="7abd3-112">Exemplo 3: criar uma regra de alerta ação de email para proprietários de serviços e proprietários não pertencentes ao serviço</span><span class="sxs-lookup"><span data-stu-id="7abd3-112">Example 3: Create an alert rule email action for service owners and non-service owners</span></span>
```
PS C:\>New-AzureRmAlertRuleEmail -CustomEmails "pattif@contoso.net" -SendToServiceOwners
```

<span data-ttu-id="7abd3-113">Esse comando cria uma ação de email de regra de alerta para o endereço especificado e para seus proprietários de serviço.</span><span class="sxs-lookup"><span data-stu-id="7abd3-113">This command creates an alert rule email action for the specified address and for its service owners.</span></span>

## <span data-ttu-id="7abd3-114">OS</span><span class="sxs-lookup"><span data-stu-id="7abd3-114">PARAMETERS</span></span>

### <span data-ttu-id="7abd3-115">-CustomEmails</span><span class="sxs-lookup"><span data-stu-id="7abd3-115">-CustomEmails</span></span>
<span data-ttu-id="7abd3-116">Especifica uma lista de endereços de email separados por vírgula.</span><span class="sxs-lookup"><span data-stu-id="7abd3-116">Specifies a list of comma-separated e-mail addresses.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7abd3-117">-SendToServiceOwners</span><span class="sxs-lookup"><span data-stu-id="7abd3-117">-SendToServiceOwners</span></span>
<span data-ttu-id="7abd3-118">Indica que esta operação envia um email para os proprietários do serviço quando a regra é acionada.</span><span class="sxs-lookup"><span data-stu-id="7abd3-118">Indicates that this operation sends an e-mail to the service owners when the rule fires.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7abd3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7abd3-119">-DefaultProfile</span></span>
<span data-ttu-id="7abd3-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7abd3-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7abd3-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7abd3-121">CommonParameters</span></span>
<span data-ttu-id="7abd3-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7abd3-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7abd3-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7abd3-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7abd3-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7abd3-124">INPUTS</span></span>

## <span data-ttu-id="7abd3-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7abd3-125">OUTPUTS</span></span>

### <span data-ttu-id="7abd3-126">Microsoft. Azure. Management. monitor. Management. Models. RuleEmailAction</span><span class="sxs-lookup"><span data-stu-id="7abd3-126">Microsoft.Azure.Management.Monitor.Management.Models.RuleEmailAction</span></span>

## <span data-ttu-id="7abd3-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7abd3-127">NOTES</span></span>

## <span data-ttu-id="7abd3-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7abd3-128">RELATED LINKS</span></span>

[<span data-ttu-id="7abd3-129">Add-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="7abd3-129">Add-AzureRmLogAlertRule</span></span>](./Add-AzureRmLogAlertRule.md)

[<span data-ttu-id="7abd3-130">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="7abd3-130">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="7abd3-131">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="7abd3-131">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="7abd3-132">New-AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="7abd3-132">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)


