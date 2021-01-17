---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5B5F494-D912-40D0-99E2-A62FAACA3EC9
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscalenotification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleNotification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleNotification.md
ms.openlocfilehash: 010698183dec206002c0966fb8f37d629d24794a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98429476"
---
# <span data-ttu-id="22cf1-101">New-AzAutoscaleNotification</span><span class="sxs-lookup"><span data-stu-id="22cf1-101">New-AzAutoscaleNotification</span></span>

## <span data-ttu-id="22cf1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="22cf1-102">SYNOPSIS</span></span>
<span data-ttu-id="22cf1-103">Cria uma notificação por email de autoescala.</span><span class="sxs-lookup"><span data-stu-id="22cf1-103">Creates an Autoscale email notification.</span></span>

## <span data-ttu-id="22cf1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="22cf1-104">SYNTAX</span></span>

```
New-AzAutoscaleNotification [[-Webhook] <WebhookNotification[]>] [[-CustomEmail] <String[]>]
 [-SendEmailToSubscriptionAdministrator] [-SendEmailToSubscriptionCoAdministrator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="22cf1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="22cf1-105">DESCRIPTION</span></span>
<span data-ttu-id="22cf1-106">O cmdlet **New-AzAutoscaleNotification** cria uma notificação por email para autoescala.</span><span class="sxs-lookup"><span data-stu-id="22cf1-106">The **New-AzAutoscaleNotification** cmdlet creates an email notification for Autoscale.</span></span>

## <span data-ttu-id="22cf1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="22cf1-107">EXAMPLES</span></span>

### <span data-ttu-id="22cf1-108">Exemplo 1: criar uma notificação de email de autoescala</span><span class="sxs-lookup"><span data-stu-id="22cf1-108">Example 1: Create an Autoscale email notification</span></span>
```
PS C:\>New-AzAutoscaleNotification -CustomEmail "pattif@contoso.com, davidchew@contoso.net"
```

<span data-ttu-id="22cf1-109">Esse comando cria uma notificação de email do Autosacale para dois endereços especificados.</span><span class="sxs-lookup"><span data-stu-id="22cf1-109">This command creates an Autosacale email notification for two specified addresses.</span></span>

### <span data-ttu-id="22cf1-110">Exemplo 2: criar uma notificação de email de AutoEscala para o administrador de assinatura</span><span class="sxs-lookup"><span data-stu-id="22cf1-110">Example 2: Create an Autoscale email notification for the subscription administrator</span></span>
```
PS C:\>New-AzAutoscaleNotification -SendEmailToSubscriptionAdministrator
```

<span data-ttu-id="22cf1-111">Esse comando cria uma notificação por email do Autosacale para o administrador da assinatura.</span><span class="sxs-lookup"><span data-stu-id="22cf1-111">This command creates an Autosacale email notification for the subscription administrator.</span></span>

## <span data-ttu-id="22cf1-112">OS</span><span class="sxs-lookup"><span data-stu-id="22cf1-112">PARAMETERS</span></span>

### <span data-ttu-id="22cf1-113">-CustomEmail</span><span class="sxs-lookup"><span data-stu-id="22cf1-113">-CustomEmail</span></span>
<span data-ttu-id="22cf1-114">Especifica uma lista separada por vírgulas de endereços de email.</span><span class="sxs-lookup"><span data-stu-id="22cf1-114">Specifies a comma-separated list of email addresses.</span></span>

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

### <span data-ttu-id="22cf1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22cf1-115">-DefaultProfile</span></span>
<span data-ttu-id="22cf1-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="22cf1-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="22cf1-117">-SendEmailToSubscriptionAdministrator</span><span class="sxs-lookup"><span data-stu-id="22cf1-117">-SendEmailToSubscriptionAdministrator</span></span>
<span data-ttu-id="22cf1-118">Indica que esta operação envia uma notificação por email ao administrador da assinatura.</span><span class="sxs-lookup"><span data-stu-id="22cf1-118">Indicates that this operation sends an email notification to the subscription administrator.</span></span>

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

### <span data-ttu-id="22cf1-119">-SendEmailToSubscriptionCoAdministrator</span><span class="sxs-lookup"><span data-stu-id="22cf1-119">-SendEmailToSubscriptionCoAdministrator</span></span>
<span data-ttu-id="22cf1-120">Indica que esta operação envia uma notificação por email para os coadministradors de assinatura.</span><span class="sxs-lookup"><span data-stu-id="22cf1-120">Indicates that this operation sends an email notification to the subscription co-administrators.</span></span>

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

### <span data-ttu-id="22cf1-121">-Webhook</span><span class="sxs-lookup"><span data-stu-id="22cf1-121">-Webhook</span></span>
<span data-ttu-id="22cf1-122">Especifica uma lista separada por vírgulas de WebHooks autodimensionais.</span><span class="sxs-lookup"><span data-stu-id="22cf1-122">Specifies a comma-separated list of Autoscale webhooks.</span></span>

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

### <span data-ttu-id="22cf1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22cf1-123">CommonParameters</span></span>
<span data-ttu-id="22cf1-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22cf1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22cf1-125">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="22cf1-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22cf1-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="22cf1-126">INPUTS</span></span>

### <span data-ttu-id="22cf1-127">Microsoft. Azure. Management. monitor. Management. Models. WebhookNotification []</span><span class="sxs-lookup"><span data-stu-id="22cf1-127">Microsoft.Azure.Management.Monitor.Management.Models.WebhookNotification[]</span></span>

### <span data-ttu-id="22cf1-128">System. String []</span><span class="sxs-lookup"><span data-stu-id="22cf1-128">System.String[]</span></span>

### <span data-ttu-id="22cf1-129">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="22cf1-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="22cf1-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="22cf1-130">OUTPUTS</span></span>

### <span data-ttu-id="22cf1-131">Microsoft. Azure. Management. monitor. Management. Models. AutoscaleNotification</span><span class="sxs-lookup"><span data-stu-id="22cf1-131">Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification</span></span>

## <span data-ttu-id="22cf1-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="22cf1-132">NOTES</span></span>

## <span data-ttu-id="22cf1-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="22cf1-133">RELATED LINKS</span></span>

[<span data-ttu-id="22cf1-134">New-AzAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="22cf1-134">New-AzAutoscaleWebhook</span></span>](./New-AzAutoscaleWebhook.md)


