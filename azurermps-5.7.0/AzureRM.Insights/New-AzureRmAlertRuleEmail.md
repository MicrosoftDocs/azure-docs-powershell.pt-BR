---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B1000C10-265E-4465-B167-F1251470BE3E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermalertruleemail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAlertRuleEmail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAlertRuleEmail.md
ms.openlocfilehash: b3484b410ef885567010c05660590808f3995308
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430476"
---
# <span data-ttu-id="72a9c-101">New-AzureRmAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="72a9c-101">New-AzureRmAlertRuleEmail</span></span>

## <span data-ttu-id="72a9c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="72a9c-102">SYNOPSIS</span></span>
<span data-ttu-id="72a9c-103">Cria uma ação de email para uma regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="72a9c-103">Creates an email action for an alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72a9c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="72a9c-104">SYNTAX</span></span>

```
New-AzureRmAlertRuleEmail [[-CustomEmail] <String[]>] [-SendToServiceOwner] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="72a9c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="72a9c-105">DESCRIPTION</span></span>
<span data-ttu-id="72a9c-106">O cmdlet **New-AzureRmAlertRuleEmail** cria uma ação de email para uma regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="72a9c-106">The **New-AzureRmAlertRuleEmail** cmdlet creates an e-mail action for an alert rule.</span></span>

## <span data-ttu-id="72a9c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="72a9c-107">EXAMPLES</span></span>

### <span data-ttu-id="72a9c-108">Exemplo 1: criar uma ação de email de regra de alerta para proprietários de serviço</span><span class="sxs-lookup"><span data-stu-id="72a9c-108">Example 1: Create an alert rule email action for service owners</span></span>
```
PS C:\>New-AzureRmAlertRuleEmail -SendToServiceOwners
```

<span data-ttu-id="72a9c-109">Esse comando cria uma ação de email de regra de alerta para enviar para seus proprietários de serviço quando uma regra de alerta é acionada.</span><span class="sxs-lookup"><span data-stu-id="72a9c-109">This command creates an alert rule email action to send for its service owners when an alert rule is fired.</span></span>

### <span data-ttu-id="72a9c-110">Exemplo 2: criar uma regra de alerta ação de email para proprietários que não são de serviço</span><span class="sxs-lookup"><span data-stu-id="72a9c-110">Example 2: Create an alert rule email action for non-service owners</span></span>
```
PS C:\>New-AzureRmAlertRuleEmail -CustomEmails pattif@contoso.com,davidchew@contoso.net
```

<span data-ttu-id="72a9c-111">Esse comando cria uma ação de email de regra de alerta para os endereços de email especificados, mas não para os proprietários do serviço.</span><span class="sxs-lookup"><span data-stu-id="72a9c-111">This command creates an alert rule email action for the specified email addresses, but not for the service owners.</span></span>

### <span data-ttu-id="72a9c-112">Exemplo 3: criar uma regra de alerta ação de email para proprietários de serviços e proprietários não pertencentes ao serviço</span><span class="sxs-lookup"><span data-stu-id="72a9c-112">Example 3: Create an alert rule email action for service owners and non-service owners</span></span>
```
PS C:\>New-AzureRmAlertRuleEmail -CustomEmails pattif@contoso.net -SendToServiceOwners
```

<span data-ttu-id="72a9c-113">Esse comando cria uma ação de email de regra de alerta para o endereço especificado e para seus proprietários de serviço.</span><span class="sxs-lookup"><span data-stu-id="72a9c-113">This command creates an alert rule email action for the specified address and for its service owners.</span></span>

## <span data-ttu-id="72a9c-114">OS</span><span class="sxs-lookup"><span data-stu-id="72a9c-114">PARAMETERS</span></span>

### <span data-ttu-id="72a9c-115">-CustomEmail</span><span class="sxs-lookup"><span data-stu-id="72a9c-115">-CustomEmail</span></span>
<span data-ttu-id="72a9c-116">Especifica uma lista de endereços de email separados por vírgula.</span><span class="sxs-lookup"><span data-stu-id="72a9c-116">Specifies a list of comma-separated e-mail addresses.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: CustomEmails

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72a9c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72a9c-117">-DefaultProfile</span></span>
<span data-ttu-id="72a9c-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="72a9c-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="72a9c-119">-SendToServiceOwner</span><span class="sxs-lookup"><span data-stu-id="72a9c-119">-SendToServiceOwner</span></span>
<span data-ttu-id="72a9c-120">Indica que esta operação envia um email para os proprietários do serviço quando a regra é acionada.</span><span class="sxs-lookup"><span data-stu-id="72a9c-120">Indicates that this operation sends an e-mail to the service owners when the rule fires.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: SendToServiceOwners

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72a9c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72a9c-121">CommonParameters</span></span>
<span data-ttu-id="72a9c-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72a9c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72a9c-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72a9c-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72a9c-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="72a9c-124">INPUTS</span></span>

### <span data-ttu-id="72a9c-125">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="72a9c-125">None</span></span>
<span data-ttu-id="72a9c-126">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="72a9c-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="72a9c-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="72a9c-127">OUTPUTS</span></span>

### <span data-ttu-id="72a9c-128">Microsoft. Azure. Management. monitor. Management. Models. RuleEmailAction</span><span class="sxs-lookup"><span data-stu-id="72a9c-128">Microsoft.Azure.Management.Monitor.Management.Models.RuleEmailAction</span></span>

## <span data-ttu-id="72a9c-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="72a9c-129">NOTES</span></span>

## <span data-ttu-id="72a9c-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="72a9c-130">RELATED LINKS</span></span>

[<span data-ttu-id="72a9c-131">Add-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="72a9c-131">Add-AzureRmLogAlertRule</span></span>](./Add-AzureRmLogAlertRule.md)

[<span data-ttu-id="72a9c-132">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="72a9c-132">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="72a9c-133">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="72a9c-133">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="72a9c-134">New-AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="72a9c-134">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)


