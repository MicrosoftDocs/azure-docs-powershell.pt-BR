---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B1000C10-265E-4465-B167-F1251470BE3E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azalertruleemail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleEmail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleEmail.md
ms.openlocfilehash: 592329ff0793fc99f8e5b0e7031a2248342102f9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98259071"
---
# <span data-ttu-id="fd779-101">New-AzAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="fd779-101">New-AzAlertRuleEmail</span></span>

## <span data-ttu-id="fd779-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fd779-102">SYNOPSIS</span></span>
<span data-ttu-id="fd779-103">Cria uma ação de email para uma regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="fd779-103">Creates an email action for an alert rule.</span></span>

## <span data-ttu-id="fd779-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fd779-104">SYNTAX</span></span>

```
New-AzAlertRuleEmail [[-CustomEmail] <String[]>] [-SendToServiceOwner]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fd779-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fd779-105">DESCRIPTION</span></span>
<span data-ttu-id="fd779-106">O cmdlet **New-AzAlertRuleEmail** cria uma ação de email para uma regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="fd779-106">The **New-AzAlertRuleEmail** cmdlet creates an e-mail action for an alert rule.</span></span>

## <span data-ttu-id="fd779-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fd779-107">EXAMPLES</span></span>

### <span data-ttu-id="fd779-108">Exemplo 1: criar uma ação de email de regra de alerta para proprietários de serviço</span><span class="sxs-lookup"><span data-stu-id="fd779-108">Example 1: Create an alert rule email action for service owners</span></span>
```
PS C:\>New-AzAlertRuleEmail -SendToServiceOwners
```

<span data-ttu-id="fd779-109">Esse comando cria uma ação de email de regra de alerta para enviar para seus proprietários de serviço quando uma regra de alerta é acionada.</span><span class="sxs-lookup"><span data-stu-id="fd779-109">This command creates an alert rule email action to send for its service owners when an alert rule is fired.</span></span>

### <span data-ttu-id="fd779-110">Exemplo 2: criar uma regra de alerta ação de email para proprietários que não são de serviço</span><span class="sxs-lookup"><span data-stu-id="fd779-110">Example 2: Create an alert rule email action for non-service owners</span></span>
```
PS C:\>New-AzAlertRuleEmail -CustomEmail pattif@contoso.com,davidchew@contoso.net
```

<span data-ttu-id="fd779-111">Esse comando cria uma ação de email de regra de alerta para os endereços de email especificados, mas não para os proprietários do serviço.</span><span class="sxs-lookup"><span data-stu-id="fd779-111">This command creates an alert rule email action for the specified email addresses, but not for the service owners.</span></span>

### <span data-ttu-id="fd779-112">Exemplo 3: criar uma regra de alerta ação de email para proprietários de serviços e proprietários não pertencentes ao serviço</span><span class="sxs-lookup"><span data-stu-id="fd779-112">Example 3: Create an alert rule email action for service owners and non-service owners</span></span>
```
PS C:\>New-AzAlertRuleEmail -CustomEmail pattif@contoso.net -SendToServiceOwners
```

<span data-ttu-id="fd779-113">Esse comando cria uma ação de email de regra de alerta para o endereço especificado e para seus proprietários de serviço.</span><span class="sxs-lookup"><span data-stu-id="fd779-113">This command creates an alert rule email action for the specified address and for its service owners.</span></span>

## <span data-ttu-id="fd779-114">OS</span><span class="sxs-lookup"><span data-stu-id="fd779-114">PARAMETERS</span></span>

### <span data-ttu-id="fd779-115">-CustomEmail</span><span class="sxs-lookup"><span data-stu-id="fd779-115">-CustomEmail</span></span>
<span data-ttu-id="fd779-116">Especifica uma lista de endereços de email separados por vírgula.</span><span class="sxs-lookup"><span data-stu-id="fd779-116">Specifies a list of comma-separated e-mail addresses.</span></span>

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

### <span data-ttu-id="fd779-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd779-117">-DefaultProfile</span></span>
<span data-ttu-id="fd779-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="fd779-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fd779-119">-SendToServiceOwner</span><span class="sxs-lookup"><span data-stu-id="fd779-119">-SendToServiceOwner</span></span>
<span data-ttu-id="fd779-120">Indica que esta operação envia um email para os proprietários do serviço quando a regra é acionada.</span><span class="sxs-lookup"><span data-stu-id="fd779-120">Indicates that this operation sends an e-mail to the service owners when the rule fires.</span></span>

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

### <span data-ttu-id="fd779-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd779-121">CommonParameters</span></span>
<span data-ttu-id="fd779-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd779-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd779-123">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fd779-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd779-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fd779-124">INPUTS</span></span>

### <span data-ttu-id="fd779-125">System. String []</span><span class="sxs-lookup"><span data-stu-id="fd779-125">System.String[]</span></span>

### <span data-ttu-id="fd779-126">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="fd779-126">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="fd779-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fd779-127">OUTPUTS</span></span>

### <span data-ttu-id="fd779-128">Microsoft. Azure. Management. monitor. Management. Models. RuleEmailAction</span><span class="sxs-lookup"><span data-stu-id="fd779-128">Microsoft.Azure.Management.Monitor.Management.Models.RuleEmailAction</span></span>

## <span data-ttu-id="fd779-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fd779-129">NOTES</span></span>

## <span data-ttu-id="fd779-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fd779-130">RELATED LINKS</span></span>

[<span data-ttu-id="fd779-131">Add-AzLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="fd779-131">Add-AzLogAlertRule</span></span>](./Add-AzLogAlertRule.md)

[<span data-ttu-id="fd779-132">Add-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="fd779-132">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="fd779-133">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="fd779-133">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="fd779-134">New-AzAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="fd779-134">New-AzAlertRuleWebhook</span></span>](./New-AzAlertRuleWebhook.md)


