---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5B5F494-D912-40D0-99E2-A62FAACA3EC9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermautoscalenotification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleNotification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleNotification.md
ms.openlocfilehash: e550341d0bd5a5d2f4e26e4ac736fab9831b67c0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429528"
---
# <span data-ttu-id="2a15c-101">New-AzureRmAutoscaleNotification</span><span class="sxs-lookup"><span data-stu-id="2a15c-101">New-AzureRmAutoscaleNotification</span></span>

## <span data-ttu-id="2a15c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2a15c-102">SYNOPSIS</span></span>
<span data-ttu-id="2a15c-103">Cria uma notificação por email de autoescala.</span><span class="sxs-lookup"><span data-stu-id="2a15c-103">Creates an Autoscale email notification.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2a15c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2a15c-104">SYNTAX</span></span>

```
New-AzureRmAutoscaleNotification [[-Webhook] <WebhookNotification[]>] [[-CustomEmail] <String[]>]
 [-SendEmailToSubscriptionAdministrator] [-SendEmailToSubscriptionCoAdministrator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2a15c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2a15c-105">DESCRIPTION</span></span>
<span data-ttu-id="2a15c-106">O cmdlet **New-AzureRmAutoscaleNotification** cria uma notificação por email para autoescala.</span><span class="sxs-lookup"><span data-stu-id="2a15c-106">The **New-AzureRmAutoscaleNotification** cmdlet creates an email notification for Autoscale.</span></span>

## <span data-ttu-id="2a15c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2a15c-107">EXAMPLES</span></span>

### <span data-ttu-id="2a15c-108">Exemplo 1: criar uma notificação de email de autoescala</span><span class="sxs-lookup"><span data-stu-id="2a15c-108">Example 1: Create an Autoscale email notification</span></span>
```
PS C:\>New-AzureRmAutoscaleNotification -CustomEmails "pattif@contoso.com, davidchew@contoso.net"
```

<span data-ttu-id="2a15c-109">Esse comando cria uma notificação de email do Autosacale para dois endereços especificados.</span><span class="sxs-lookup"><span data-stu-id="2a15c-109">This command creates an Autosacale email notification for two specified addresses.</span></span>

### <span data-ttu-id="2a15c-110">Exemplo 2: criar uma notificação de email de AutoEscala para o administrador de assinatura</span><span class="sxs-lookup"><span data-stu-id="2a15c-110">Example 2: Create an Autoscale email notification for the subscription administrator</span></span>
```
PS C:\>New-AzureRmAutoscaleNotification -SendEmailToSubscriptionAdministrator
```

<span data-ttu-id="2a15c-111">Esse comando cria uma notificação por email do Autosacale para o administrador da assinatura.</span><span class="sxs-lookup"><span data-stu-id="2a15c-111">This command creates an Autosacale email notification for the subscription administrator.</span></span>

## <span data-ttu-id="2a15c-112">OS</span><span class="sxs-lookup"><span data-stu-id="2a15c-112">PARAMETERS</span></span>

### <span data-ttu-id="2a15c-113">-CustomEmail</span><span class="sxs-lookup"><span data-stu-id="2a15c-113">-CustomEmail</span></span>
<span data-ttu-id="2a15c-114">Especifica uma lista separada por vírgulas de endereços de email.</span><span class="sxs-lookup"><span data-stu-id="2a15c-114">Specifies a comma-separated list of email addresses.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a15c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a15c-115">-DefaultProfile</span></span>
<span data-ttu-id="2a15c-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="2a15c-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2a15c-117">-SendEmailToSubscriptionAdministrator</span><span class="sxs-lookup"><span data-stu-id="2a15c-117">-SendEmailToSubscriptionAdministrator</span></span>
<span data-ttu-id="2a15c-118">Indica que esta operação envia uma notificação por email ao administrador da assinatura.</span><span class="sxs-lookup"><span data-stu-id="2a15c-118">Indicates that this operation sends an email notification to the subscription administrator.</span></span>

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

### <span data-ttu-id="2a15c-119">-SendEmailToSubscriptionCoAdministrator</span><span class="sxs-lookup"><span data-stu-id="2a15c-119">-SendEmailToSubscriptionCoAdministrator</span></span>
<span data-ttu-id="2a15c-120">Indica que esta operação envia uma notificação por email para os coadministradors de assinatura.</span><span class="sxs-lookup"><span data-stu-id="2a15c-120">Indicates that this operation sends an email notification to the subscription co-administrators.</span></span>

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

### <span data-ttu-id="2a15c-121">-Webhook</span><span class="sxs-lookup"><span data-stu-id="2a15c-121">-Webhook</span></span>
<span data-ttu-id="2a15c-122">Especifica uma lista separada por vírgulas de WebHooks autodimensionais.</span><span class="sxs-lookup"><span data-stu-id="2a15c-122">Specifies a comma-separated list of Autoscale webhooks.</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.WebhookNotification[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a15c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a15c-123">CommonParameters</span></span>
<span data-ttu-id="2a15c-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a15c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a15c-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a15c-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a15c-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2a15c-126">INPUTS</span></span>

### <span data-ttu-id="2a15c-127">Microsoft. Azure. Management. monitor. Management. Models. WebhookNotification []</span><span class="sxs-lookup"><span data-stu-id="2a15c-127">Microsoft.Azure.Management.Monitor.Management.Models.WebhookNotification[]</span></span>

### <span data-ttu-id="2a15c-128">System. String []</span><span class="sxs-lookup"><span data-stu-id="2a15c-128">System.String[]</span></span>

### <span data-ttu-id="2a15c-129">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2a15c-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2a15c-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2a15c-130">OUTPUTS</span></span>

### <span data-ttu-id="2a15c-131">Microsoft. Azure. Management. monitor. Management. Models. AutoscaleNotification</span><span class="sxs-lookup"><span data-stu-id="2a15c-131">Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification</span></span>

## <span data-ttu-id="2a15c-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2a15c-132">NOTES</span></span>

## <span data-ttu-id="2a15c-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2a15c-133">RELATED LINKS</span></span>

[<span data-ttu-id="2a15c-134">New-AzureRmAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="2a15c-134">New-AzureRmAutoscaleWebhook</span></span>](./New-AzureRmAutoscaleWebhook.md)


