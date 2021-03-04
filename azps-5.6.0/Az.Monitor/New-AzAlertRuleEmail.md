---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B1000C10-265E-4465-B167-F1251470BE3E
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azalertruleemail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleEmail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleEmail.md
ms.openlocfilehash: 481105ca99a2bdc797a7a539f54ab69fd9935ebb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888872"
---
# <span data-ttu-id="ae812-101">New-AzAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="ae812-101">New-AzAlertRuleEmail</span></span>

## <span data-ttu-id="ae812-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae812-102">SYNOPSIS</span></span>
<span data-ttu-id="ae812-103">Cria uma ação de email para uma regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="ae812-103">Creates an email action for an alert rule.</span></span>

## <span data-ttu-id="ae812-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ae812-104">SYNTAX</span></span>

```
New-AzAlertRuleEmail [[-CustomEmail] <String[]>] [-SendToServiceOwner]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae812-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ae812-105">DESCRIPTION</span></span>
<span data-ttu-id="ae812-106">O cmdlet **New-AzAlertRuleEmail** cria uma ação de email para uma regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="ae812-106">The **New-AzAlertRuleEmail** cmdlet creates an e-mail action for an alert rule.</span></span>

## <span data-ttu-id="ae812-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ae812-107">EXAMPLES</span></span>

### <span data-ttu-id="ae812-108">Exemplo 1: Criar uma ação de email de regra de alerta para proprietários de serviço</span><span class="sxs-lookup"><span data-stu-id="ae812-108">Example 1: Create an alert rule email action for service owners</span></span>
```
PS C:\>New-AzAlertRuleEmail -SendToServiceOwners
```

<span data-ttu-id="ae812-109">Este comando cria uma ação de email de regra de alerta para enviar para seus proprietários de serviço quando uma regra de alerta é disparada.</span><span class="sxs-lookup"><span data-stu-id="ae812-109">This command creates an alert rule email action to send for its service owners when an alert rule is fired.</span></span>

### <span data-ttu-id="ae812-110">Exemplo 2: Criar uma ação de email de regra de alerta para proprietários que não são do serviço</span><span class="sxs-lookup"><span data-stu-id="ae812-110">Example 2: Create an alert rule email action for non-service owners</span></span>
```
PS C:\>New-AzAlertRuleEmail -CustomEmail pattif@contoso.com,davidchew@contoso.net
```

<span data-ttu-id="ae812-111">Este comando cria uma ação de email de regra de alerta para os endereços de email especificados, mas não para os proprietários do serviço.</span><span class="sxs-lookup"><span data-stu-id="ae812-111">This command creates an alert rule email action for the specified email addresses, but not for the service owners.</span></span>

### <span data-ttu-id="ae812-112">Exemplo 3: Criar uma ação de email de regra de alerta para proprietários de serviços e proprietários que não são do serviço</span><span class="sxs-lookup"><span data-stu-id="ae812-112">Example 3: Create an alert rule email action for service owners and non-service owners</span></span>
```
PS C:\>New-AzAlertRuleEmail -CustomEmail pattif@contoso.net -SendToServiceOwners
```

<span data-ttu-id="ae812-113">Este comando cria uma ação de email de regra de alerta para o endereço especificado e para seus proprietários de serviço.</span><span class="sxs-lookup"><span data-stu-id="ae812-113">This command creates an alert rule email action for the specified address and for its service owners.</span></span>

## <span data-ttu-id="ae812-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ae812-114">PARAMETERS</span></span>

### <span data-ttu-id="ae812-115">-CustomEmail</span><span class="sxs-lookup"><span data-stu-id="ae812-115">-CustomEmail</span></span>
<span data-ttu-id="ae812-116">Especifica uma lista de endereços de email separados por vírgulas.</span><span class="sxs-lookup"><span data-stu-id="ae812-116">Specifies a list of comma-separated e-mail addresses.</span></span>

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

### <span data-ttu-id="ae812-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae812-117">-DefaultProfile</span></span>
<span data-ttu-id="ae812-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="ae812-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ae812-119">-SendToServiceOwner</span><span class="sxs-lookup"><span data-stu-id="ae812-119">-SendToServiceOwner</span></span>
<span data-ttu-id="ae812-120">Indica que essa operação envia um email para os proprietários do serviço quando a regra é a incêndio.</span><span class="sxs-lookup"><span data-stu-id="ae812-120">Indicates that this operation sends an e-mail to the service owners when the rule fires.</span></span>

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

### <span data-ttu-id="ae812-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae812-121">CommonParameters</span></span>
<span data-ttu-id="ae812-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae812-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae812-123">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ae812-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae812-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ae812-124">INPUTS</span></span>

### <span data-ttu-id="ae812-125">System.String[]</span><span class="sxs-lookup"><span data-stu-id="ae812-125">System.String[]</span></span>

### <span data-ttu-id="ae812-126">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ae812-126">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ae812-127">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ae812-127">OUTPUTS</span></span>

### <span data-ttu-id="ae812-128">Microsoft.Azure.Management.Monitor.Management.Models.RuleEmailAction</span><span class="sxs-lookup"><span data-stu-id="ae812-128">Microsoft.Azure.Management.Monitor.Management.Models.RuleEmailAction</span></span>

## <span data-ttu-id="ae812-129">NOTES</span><span class="sxs-lookup"><span data-stu-id="ae812-129">NOTES</span></span>

## <span data-ttu-id="ae812-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ae812-130">RELATED LINKS</span></span>

[<span data-ttu-id="ae812-131">Add-AzLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="ae812-131">Add-AzLogAlertRule</span></span>](./Add-AzLogAlertRule.md)

[<span data-ttu-id="ae812-132">Add-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="ae812-132">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="ae812-133">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="ae812-133">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="ae812-134">New-AzAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="ae812-134">New-AzAlertRuleWebhook</span></span>](./New-AzAlertRuleWebhook.md)


