---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5B5F494-D912-40D0-99E2-A62FAACA3EC9
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscalenotification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleNotification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleNotification.md
ms.openlocfilehash: 010698183dec206002c0966fb8f37d629d24794a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114763"
---
# <span data-ttu-id="7a3e5-101">New-AzAutoscaleNotification</span><span class="sxs-lookup"><span data-stu-id="7a3e5-101">New-AzAutoscaleNotification</span></span>

## <span data-ttu-id="7a3e5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7a3e5-102">SYNOPSIS</span></span>
<span data-ttu-id="7a3e5-103">Cria uma notificação de email em escala automática.</span><span class="sxs-lookup"><span data-stu-id="7a3e5-103">Creates an Autoscale email notification.</span></span>

## <span data-ttu-id="7a3e5-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7a3e5-104">SYNTAX</span></span>

```
New-AzAutoscaleNotification [[-Webhook] <WebhookNotification[]>] [[-CustomEmail] <String[]>]
 [-SendEmailToSubscriptionAdministrator] [-SendEmailToSubscriptionCoAdministrator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7a3e5-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="7a3e5-105">DESCRIPTION</span></span>
<span data-ttu-id="7a3e5-106">O **cmdlet New-AzAutoscaleNotification** cria uma notificação por email para Escala Automática.</span><span class="sxs-lookup"><span data-stu-id="7a3e5-106">The **New-AzAutoscaleNotification** cmdlet creates an email notification for Autoscale.</span></span>

## <span data-ttu-id="7a3e5-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7a3e5-107">EXAMPLES</span></span>

### <span data-ttu-id="7a3e5-108">Exemplo 1: Criar uma notificação de email em escala automática</span><span class="sxs-lookup"><span data-stu-id="7a3e5-108">Example 1: Create an Autoscale email notification</span></span>
```
PS C:\>New-AzAutoscaleNotification -CustomEmail "pattif@contoso.com, davidchew@contoso.net"
```

<span data-ttu-id="7a3e5-109">Esse comando cria uma notificação por email de autosacale para dois endereços especificados.</span><span class="sxs-lookup"><span data-stu-id="7a3e5-109">This command creates an Autosacale email notification for two specified addresses.</span></span>

### <span data-ttu-id="7a3e5-110">Exemplo 2: Criar uma notificação de email em escala automática para o administrador da assinatura</span><span class="sxs-lookup"><span data-stu-id="7a3e5-110">Example 2: Create an Autoscale email notification for the subscription administrator</span></span>
```
PS C:\>New-AzAutoscaleNotification -SendEmailToSubscriptionAdministrator
```

<span data-ttu-id="7a3e5-111">Esse comando cria uma notificação por email de autosacale para o administrador da assinatura.</span><span class="sxs-lookup"><span data-stu-id="7a3e5-111">This command creates an Autosacale email notification for the subscription administrator.</span></span>

## <span data-ttu-id="7a3e5-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7a3e5-112">PARAMETERS</span></span>

### <span data-ttu-id="7a3e5-113">-CustomEmail</span><span class="sxs-lookup"><span data-stu-id="7a3e5-113">-CustomEmail</span></span>
<span data-ttu-id="7a3e5-114">Especifica uma lista separada por vírgulas de endereços de email.</span><span class="sxs-lookup"><span data-stu-id="7a3e5-114">Specifies a comma-separated list of email addresses.</span></span>

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

### <span data-ttu-id="7a3e5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a3e5-115">-DefaultProfile</span></span>
<span data-ttu-id="7a3e5-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="7a3e5-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7a3e5-117">-SendEmailToSubscriptionAdministrator</span><span class="sxs-lookup"><span data-stu-id="7a3e5-117">-SendEmailToSubscriptionAdministrator</span></span>
<span data-ttu-id="7a3e5-118">Indica que essa operação envia uma notificação por email ao administrador da assinatura.</span><span class="sxs-lookup"><span data-stu-id="7a3e5-118">Indicates that this operation sends an email notification to the subscription administrator.</span></span>

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

### <span data-ttu-id="7a3e5-119">-SendEmailToSubscriptionCoAdministrator</span><span class="sxs-lookup"><span data-stu-id="7a3e5-119">-SendEmailToSubscriptionCoAdministrator</span></span>
<span data-ttu-id="7a3e5-120">Indica que essa operação envia uma notificação por email para os co-administradores da assinatura.</span><span class="sxs-lookup"><span data-stu-id="7a3e5-120">Indicates that this operation sends an email notification to the subscription co-administrators.</span></span>

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

### <span data-ttu-id="7a3e5-121">-Web browser</span><span class="sxs-lookup"><span data-stu-id="7a3e5-121">-Webhook</span></span>
<span data-ttu-id="7a3e5-122">Especifica uma lista separada por vírgulas de Webscale automaticamente.</span><span class="sxs-lookup"><span data-stu-id="7a3e5-122">Specifies a comma-separated list of Autoscale webhooks.</span></span>

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

### <span data-ttu-id="7a3e5-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a3e5-123">CommonParameters</span></span>
<span data-ttu-id="7a3e5-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a3e5-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a3e5-125">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7a3e5-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a3e5-126">Entradas</span><span class="sxs-lookup"><span data-stu-id="7a3e5-126">INPUTS</span></span>

### <span data-ttu-id="7a3e5-127">Microsoft.Azure.Management.Monitor.Management.Models.WebitorNotification[]</span><span class="sxs-lookup"><span data-stu-id="7a3e5-127">Microsoft.Azure.Management.Monitor.Management.Models.WebhookNotification[]</span></span>

### <span data-ttu-id="7a3e5-128">System.String[]</span><span class="sxs-lookup"><span data-stu-id="7a3e5-128">System.String[]</span></span>

### <span data-ttu-id="7a3e5-129">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7a3e5-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7a3e5-130">Saídas</span><span class="sxs-lookup"><span data-stu-id="7a3e5-130">OUTPUTS</span></span>

### <span data-ttu-id="7a3e5-131">Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification</span><span class="sxs-lookup"><span data-stu-id="7a3e5-131">Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification</span></span>

## <span data-ttu-id="7a3e5-132">Notas</span><span class="sxs-lookup"><span data-stu-id="7a3e5-132">NOTES</span></span>

## <span data-ttu-id="7a3e5-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7a3e5-133">RELATED LINKS</span></span>

[<span data-ttu-id="7a3e5-134">New-AzAutoscaleWebweb</span><span class="sxs-lookup"><span data-stu-id="7a3e5-134">New-AzAutoscaleWebhook</span></span>](./New-AzAutoscaleWebhook.md)


