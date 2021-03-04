---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5B5F494-D912-40D0-99E2-A62FAACA3EC9
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azautoscalenotification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleNotification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleNotification.md
ms.openlocfilehash: c537908d2249ca5ec8a33adffa4e655b0a9ec6e6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889219"
---
# <span data-ttu-id="edaee-101">New-AzAutoscaleNotification</span><span class="sxs-lookup"><span data-stu-id="edaee-101">New-AzAutoscaleNotification</span></span>

## <span data-ttu-id="edaee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="edaee-102">SYNOPSIS</span></span>
<span data-ttu-id="edaee-103">Cria uma notificação de email de escala automática.</span><span class="sxs-lookup"><span data-stu-id="edaee-103">Creates an Autoscale email notification.</span></span>

## <span data-ttu-id="edaee-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="edaee-104">SYNTAX</span></span>

```
New-AzAutoscaleNotification [[-Webhook] <WebhookNotification[]>] [[-CustomEmail] <String[]>]
 [-SendEmailToSubscriptionAdministrator] [-SendEmailToSubscriptionCoAdministrator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="edaee-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="edaee-105">DESCRIPTION</span></span>
<span data-ttu-id="edaee-106">O cmdlet **New-AzAutoscaleNotification** cria uma notificação de email para Escala Automática.</span><span class="sxs-lookup"><span data-stu-id="edaee-106">The **New-AzAutoscaleNotification** cmdlet creates an email notification for Autoscale.</span></span>

## <span data-ttu-id="edaee-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="edaee-107">EXAMPLES</span></span>

### <span data-ttu-id="edaee-108">Exemplo 1: Criar uma notificação de email de escala automática</span><span class="sxs-lookup"><span data-stu-id="edaee-108">Example 1: Create an Autoscale email notification</span></span>
```
PS C:\>New-AzAutoscaleNotification -CustomEmail "pattif@contoso.com, davidchew@contoso.net"
```

<span data-ttu-id="edaee-109">Este comando cria uma notificação de email Autosacale para dois endereços especificados.</span><span class="sxs-lookup"><span data-stu-id="edaee-109">This command creates an Autosacale email notification for two specified addresses.</span></span>

### <span data-ttu-id="edaee-110">Exemplo 2: Criar uma notificação de email de escala automática para o administrador de assinatura</span><span class="sxs-lookup"><span data-stu-id="edaee-110">Example 2: Create an Autoscale email notification for the subscription administrator</span></span>
```
PS C:\>New-AzAutoscaleNotification -SendEmailToSubscriptionAdministrator
```

<span data-ttu-id="edaee-111">Este comando cria uma notificação de email Autosacale para o administrador de assinatura.</span><span class="sxs-lookup"><span data-stu-id="edaee-111">This command creates an Autosacale email notification for the subscription administrator.</span></span>

## <span data-ttu-id="edaee-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="edaee-112">PARAMETERS</span></span>

### <span data-ttu-id="edaee-113">-CustomEmail</span><span class="sxs-lookup"><span data-stu-id="edaee-113">-CustomEmail</span></span>
<span data-ttu-id="edaee-114">Especifica uma lista separada por vírgulas de endereços de email.</span><span class="sxs-lookup"><span data-stu-id="edaee-114">Specifies a comma-separated list of email addresses.</span></span>

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

### <span data-ttu-id="edaee-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edaee-115">-DefaultProfile</span></span>
<span data-ttu-id="edaee-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="edaee-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="edaee-117">-SendEmailToSubscriptionAdministrator</span><span class="sxs-lookup"><span data-stu-id="edaee-117">-SendEmailToSubscriptionAdministrator</span></span>
<span data-ttu-id="edaee-118">Indica que essa operação envia uma notificação de email para o administrador da assinatura.</span><span class="sxs-lookup"><span data-stu-id="edaee-118">Indicates that this operation sends an email notification to the subscription administrator.</span></span>

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

### <span data-ttu-id="edaee-119">-SendEmailToSubscriptionCoAdministrator</span><span class="sxs-lookup"><span data-stu-id="edaee-119">-SendEmailToSubscriptionCoAdministrator</span></span>
<span data-ttu-id="edaee-120">Indica que essa operação envia uma notificação de email para os co-administradores de assinatura.</span><span class="sxs-lookup"><span data-stu-id="edaee-120">Indicates that this operation sends an email notification to the subscription co-administrators.</span></span>

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

### <span data-ttu-id="edaee-121">-Webhook</span><span class="sxs-lookup"><span data-stu-id="edaee-121">-Webhook</span></span>
<span data-ttu-id="edaee-122">Especifica uma lista separada por vírgulas de webhooks de escala automática.</span><span class="sxs-lookup"><span data-stu-id="edaee-122">Specifies a comma-separated list of Autoscale webhooks.</span></span>

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

### <span data-ttu-id="edaee-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edaee-123">CommonParameters</span></span>
<span data-ttu-id="edaee-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="edaee-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edaee-125">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="edaee-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edaee-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="edaee-126">INPUTS</span></span>

### <span data-ttu-id="edaee-127">Microsoft.Azure.Management.Monitor.Management.Models.WebhookNotification[]</span><span class="sxs-lookup"><span data-stu-id="edaee-127">Microsoft.Azure.Management.Monitor.Management.Models.WebhookNotification[]</span></span>

### <span data-ttu-id="edaee-128">System.String[]</span><span class="sxs-lookup"><span data-stu-id="edaee-128">System.String[]</span></span>

### <span data-ttu-id="edaee-129">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="edaee-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="edaee-130">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="edaee-130">OUTPUTS</span></span>

### <span data-ttu-id="edaee-131">Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification</span><span class="sxs-lookup"><span data-stu-id="edaee-131">Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification</span></span>

## <span data-ttu-id="edaee-132">NOTES</span><span class="sxs-lookup"><span data-stu-id="edaee-132">NOTES</span></span>

## <span data-ttu-id="edaee-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="edaee-133">RELATED LINKS</span></span>

[<span data-ttu-id="edaee-134">New-AzAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="edaee-134">New-AzAutoscaleWebhook</span></span>](./New-AzAutoscaleWebhook.md)


