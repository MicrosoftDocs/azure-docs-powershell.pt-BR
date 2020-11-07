---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 9830CD16-D797-47EB-BEF5-6CFE3454BCAA
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azactiongroupreceiver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroupReceiver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroupReceiver.md
ms.openlocfilehash: 35f540d26464b7cdc4b08916f1397b71ee7cca18
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93770313"
---
# <span data-ttu-id="95817-101">New-AzActionGroupReceiver</span><span class="sxs-lookup"><span data-stu-id="95817-101">New-AzActionGroupReceiver</span></span>

## <span data-ttu-id="95817-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="95817-102">SYNOPSIS</span></span>
<span data-ttu-id="95817-103">Cria um novo receptor de grupo de ação.</span><span class="sxs-lookup"><span data-stu-id="95817-103">Creates an new action group receiver.</span></span>

## <span data-ttu-id="95817-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="95817-104">SYNTAX</span></span>

### <span data-ttu-id="95817-105">NewEmailReceiver (padrão)</span><span class="sxs-lookup"><span data-stu-id="95817-105">NewEmailReceiver (Default)</span></span>
```
New-AzActionGroupReceiver -Name <String> [-EmailReceiver] -EmailAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95817-106">NewSmsReceiver</span><span class="sxs-lookup"><span data-stu-id="95817-106">NewSmsReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-SmsReceiver] [-CountryCode <String>] -PhoneNumber <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95817-107">NewWebhookReceiver</span><span class="sxs-lookup"><span data-stu-id="95817-107">NewWebhookReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-WebhookReceiver] -ServiceUri <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95817-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="95817-108">DESCRIPTION</span></span>
<span data-ttu-id="95817-109">O cmdlet **New-AzActionGroupReceiver** cria um novo receptor de grupo de ação na memória.</span><span class="sxs-lookup"><span data-stu-id="95817-109">The **New-AzActionGroupReceiver** cmdlet creates new action group receiver in memory.</span></span>

## <span data-ttu-id="95817-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="95817-110">EXAMPLES</span></span>

### <span data-ttu-id="95817-111">Exemplo 1: criar um novo receptor de email na memória.</span><span class="sxs-lookup"><span data-stu-id="95817-111">Example 1: Create a new Email receiver in memory.</span></span>
```
PS C:\>$emailReceiver = New-AzActionGroupReceiver -Name 'emailReceiver1' -EmailReceiver -EmailAddress 'user1@example.com'
```

<span data-ttu-id="95817-112">Esse comando cria um novo receptor de email na memória.</span><span class="sxs-lookup"><span data-stu-id="95817-112">This command creates a new Email receiver in memory.</span></span>

### <span data-ttu-id="95817-113">Exemplo 2: criar um novo receptor de SMS na memória.</span><span class="sxs-lookup"><span data-stu-id="95817-113">Example 2: Create a new SMS receiver in memory.</span></span>
```
PS C:\>$smsReceiver = New-AzActionGroupReceiver -Name 'smsReceiver1' -SmsReceiver -CountryCode '1' -PhoneNumber '5555555555'
```

<span data-ttu-id="95817-114">Esse comando cria um novo receptor de SMS na memória.</span><span class="sxs-lookup"><span data-stu-id="95817-114">This command creates a new SMS receiver in memory.</span></span>

### <span data-ttu-id="95817-115">Exemplo 3: criar um novo receptor de webhook na memória.</span><span class="sxs-lookup"><span data-stu-id="95817-115">Example 3: Create a new webhook receiver in memory.</span></span>
```
PS C:\>$webhookReceiver = New-AzActionGroupReceiver -Name 'webhookReceiver1' -WebhookReceiver -ServiceUri 'http://test.com'
```

<span data-ttu-id="95817-116">Esse comando cria um novo receptor de webhook na memória.</span><span class="sxs-lookup"><span data-stu-id="95817-116">This command creates a new webhook receiver in memory.</span></span>

## <span data-ttu-id="95817-117">OS</span><span class="sxs-lookup"><span data-stu-id="95817-117">PARAMETERS</span></span>

### <span data-ttu-id="95817-118">-CountryCode</span><span class="sxs-lookup"><span data-stu-id="95817-118">-CountryCode</span></span>
<span data-ttu-id="95817-119">Especifica o código de país para o receptor de SMS.</span><span class="sxs-lookup"><span data-stu-id="95817-119">Specifies the country code for the SMS receiver.</span></span>

```yaml
Type: System.String
Parameter Sets: NewSmsReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95817-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95817-120">-DefaultProfile</span></span>
<span data-ttu-id="95817-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="95817-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="95817-122">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="95817-122">-EmailAddress</span></span>
<span data-ttu-id="95817-123">Especifica o endereço do receptor de email.</span><span class="sxs-lookup"><span data-stu-id="95817-123">Specifies the address for the Email receiver.</span></span>

```yaml
Type: System.String
Parameter Sets: NewEmailReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95817-124">-EmailReceiver</span><span class="sxs-lookup"><span data-stu-id="95817-124">-EmailReceiver</span></span>
<span data-ttu-id="95817-125">Especifica a criação de um receptor de email</span><span class="sxs-lookup"><span data-stu-id="95817-125">Specifies to create an Email receiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewEmailReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95817-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="95817-126">-Name</span></span>
<span data-ttu-id="95817-127">Especifica o nome do destinatário.</span><span class="sxs-lookup"><span data-stu-id="95817-127">Specifies the name for the receiver.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95817-128">-Intervalo</span><span class="sxs-lookup"><span data-stu-id="95817-128">-PhoneNumber</span></span>
<span data-ttu-id="95817-129">Especifica o número de telefone do receptor de SMS.</span><span class="sxs-lookup"><span data-stu-id="95817-129">Specifies the phone number for the SMS receiver.</span></span>

```yaml
Type: System.String
Parameter Sets: NewSmsReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95817-130">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="95817-130">-ServiceUri</span></span>
<span data-ttu-id="95817-131">Especifica o URI para o receptor de webhook.</span><span class="sxs-lookup"><span data-stu-id="95817-131">Specifies the URI for the webhook receiver.</span></span>

```yaml
Type: System.String
Parameter Sets: NewWebhookReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95817-132">-SmsReceiver</span><span class="sxs-lookup"><span data-stu-id="95817-132">-SmsReceiver</span></span>
<span data-ttu-id="95817-133">Especifica a criação de um receptor de SMS</span><span class="sxs-lookup"><span data-stu-id="95817-133">Specifies to create a SMS receiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewSmsReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95817-134">-WebhookReceiver</span><span class="sxs-lookup"><span data-stu-id="95817-134">-WebhookReceiver</span></span>
<span data-ttu-id="95817-135">Especifica a criação de um receptor de webhook</span><span class="sxs-lookup"><span data-stu-id="95817-135">Specifies to create a webhook receiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewWebhookReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95817-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95817-136">CommonParameters</span></span>
<span data-ttu-id="95817-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95817-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95817-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95817-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95817-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="95817-139">INPUTS</span></span>

### <span data-ttu-id="95817-140">System. String</span><span class="sxs-lookup"><span data-stu-id="95817-140">System.String</span></span>

### <span data-ttu-id="95817-141">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="95817-141">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="95817-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="95817-142">OUTPUTS</span></span>

### <span data-ttu-id="95817-143">Microsoft. Azure. Commands. insights. OutputClasses. PSActionGroupReceiverBase</span><span class="sxs-lookup"><span data-stu-id="95817-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase</span></span>

## <span data-ttu-id="95817-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="95817-144">NOTES</span></span>

## <span data-ttu-id="95817-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="95817-145">RELATED LINKS</span></span>

<span data-ttu-id="95817-146">[Set-AzActionGroup](./Set-AzActionGroup.md) 
 [Get-AzActionGroup](./Get-AzActionGroup.md) 
 [Remove-AzActionGroup](./Remove-AzActionGroup.md)</span><span class="sxs-lookup"><span data-stu-id="95817-146">[Set-AzActionGroup](./Set-AzActionGroup.md)
[Get-AzActionGroup](./Get-AzActionGroup.md)
[Remove-AzActionGroup](./Remove-AzActionGroup.md)</span></span>
