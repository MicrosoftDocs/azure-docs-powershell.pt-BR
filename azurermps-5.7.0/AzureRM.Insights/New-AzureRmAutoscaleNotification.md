---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5B5F494-D912-40D0-99E2-A62FAACA3EC9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermautoscalenotification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleNotification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleNotification.md
ms.openlocfilehash: ee95455b5081105ec4e28a4811e46ca92bfbc240
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430473"
---
# <span data-ttu-id="fd180-101">New-AzureRmAutoscaleNotification</span><span class="sxs-lookup"><span data-stu-id="fd180-101">New-AzureRmAutoscaleNotification</span></span>

## <span data-ttu-id="fd180-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fd180-102">SYNOPSIS</span></span>
<span data-ttu-id="fd180-103">Cria uma notificação por email de autoescala.</span><span class="sxs-lookup"><span data-stu-id="fd180-103">Creates an Autoscale email notification.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fd180-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fd180-104">SYNTAX</span></span>

```
New-AzureRmAutoscaleNotification [[-Webhook] <WebhookNotification[]>] [[-CustomEmail] <String[]>]
 [-SendEmailToSubscriptionAdministrator] [-SendEmailToSubscriptionCoAdministrator] 
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fd180-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fd180-105">DESCRIPTION</span></span>
<span data-ttu-id="fd180-106">O cmdlet **New-AzureRmAutoscaleNotification** cria uma notificação por email para autoescala.</span><span class="sxs-lookup"><span data-stu-id="fd180-106">The **New-AzureRmAutoscaleNotification** cmdlet creates an email notification for Autoscale.</span></span>

## <span data-ttu-id="fd180-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fd180-107">EXAMPLES</span></span>

### <span data-ttu-id="fd180-108">Exemplo 1: criar uma notificação de email de autoescala</span><span class="sxs-lookup"><span data-stu-id="fd180-108">Example 1: Create an Autoscale email notification</span></span>
```
PS C:\>New-AzureRmAutoscaleNotification -CustomEmails "pattif@contoso.com, davidchew@contoso.net"
```

<span data-ttu-id="fd180-109">Esse comando cria uma notificação de email do Autosacale para dois endereços especificados.</span><span class="sxs-lookup"><span data-stu-id="fd180-109">This command creates an Autosacale email notification for two specified addresses.</span></span>

### <span data-ttu-id="fd180-110">Exemplo 2: criar uma notificação de email de AutoEscala para o administrador de assinatura</span><span class="sxs-lookup"><span data-stu-id="fd180-110">Example 2: Create an Autoscale email notification for the subscription administrator</span></span>
```
PS C:\>New-AzureRmAutoscaleNotification -SendEmailToSubscriptionAdministrator
```

<span data-ttu-id="fd180-111">Esse comando cria uma notificação por email do Autosacale para o administrador da assinatura.</span><span class="sxs-lookup"><span data-stu-id="fd180-111">This command creates an Autosacale email notification for the subscription administrator.</span></span>

## <span data-ttu-id="fd180-112">OS</span><span class="sxs-lookup"><span data-stu-id="fd180-112">PARAMETERS</span></span>

### <span data-ttu-id="fd180-113">-CustomEmail</span><span class="sxs-lookup"><span data-stu-id="fd180-113">-CustomEmail</span></span>
<span data-ttu-id="fd180-114">Especifica uma lista separada por vírgulas de endereços de email.</span><span class="sxs-lookup"><span data-stu-id="fd180-114">Specifies a comma-separated list of email addresses.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: CustomEmails

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd180-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd180-115">-DefaultProfile</span></span>
<span data-ttu-id="fd180-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="fd180-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fd180-117">-SendEmailToSubscriptionAdministrator</span><span class="sxs-lookup"><span data-stu-id="fd180-117">-SendEmailToSubscriptionAdministrator</span></span>
<span data-ttu-id="fd180-118">Indica que esta operação envia uma notificação por email ao administrador da assinatura.</span><span class="sxs-lookup"><span data-stu-id="fd180-118">Indicates that this operation sends an email notification to the subscription administrator.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd180-119">-SendEmailToSubscriptionCoAdministrator</span><span class="sxs-lookup"><span data-stu-id="fd180-119">-SendEmailToSubscriptionCoAdministrator</span></span>
<span data-ttu-id="fd180-120">Indica que esta operação envia uma notificação por email para os coadministradors de assinatura.</span><span class="sxs-lookup"><span data-stu-id="fd180-120">Indicates that this operation sends an email notification to the subscription co-administrators.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: SendEmailToSubscriptionCoAdministrators

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd180-121">-Webhook</span><span class="sxs-lookup"><span data-stu-id="fd180-121">-Webhook</span></span>
<span data-ttu-id="fd180-122">Especifica uma lista separada por vírgulas de WebHooks autodimensionais.</span><span class="sxs-lookup"><span data-stu-id="fd180-122">Specifies a comma-separated list of Autoscale webhooks.</span></span>

```yaml
Type: WebhookNotification[]
Parameter Sets: (All)
Aliases: Webhooks

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd180-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd180-123">CommonParameters</span></span>
<span data-ttu-id="fd180-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd180-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd180-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd180-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd180-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fd180-126">INPUTS</span></span>

### <span data-ttu-id="fd180-127">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="fd180-127">None</span></span>
<span data-ttu-id="fd180-128">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="fd180-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fd180-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fd180-129">OUTPUTS</span></span>

### <span data-ttu-id="fd180-130">Microsoft. Azure. Management. monitor. Management. Models. AutoscaleNotification</span><span class="sxs-lookup"><span data-stu-id="fd180-130">Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification</span></span>

## <span data-ttu-id="fd180-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fd180-131">NOTES</span></span>

## <span data-ttu-id="fd180-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fd180-132">RELATED LINKS</span></span>

[<span data-ttu-id="fd180-133">New-AzureRmAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="fd180-133">New-AzureRmAutoscaleWebhook</span></span>](./New-AzureRmAutoscaleWebhook.md)


