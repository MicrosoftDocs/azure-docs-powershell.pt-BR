---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 9830CD16-D797-47EB-BEF5-6CFE3454BCAA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmActionGroupReceiver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmActionGroupReceiver.md
ms.openlocfilehash: cd08e0106fe78ddae04ac4543210b310fe3aa579
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93603373"
---
# <span data-ttu-id="1f74f-101">New-AzureRmActionGroupReceiver</span><span class="sxs-lookup"><span data-stu-id="1f74f-101">New-AzureRmActionGroupReceiver</span></span>

## <span data-ttu-id="1f74f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1f74f-102">SYNOPSIS</span></span>
<span data-ttu-id="1f74f-103">Cria um novo receptor de grupo de ação.</span><span class="sxs-lookup"><span data-stu-id="1f74f-103">Creates an new action group receiver.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f74f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1f74f-104">SYNTAX</span></span>

### <span data-ttu-id="1f74f-105">NewEmailReceiver (padrão)</span><span class="sxs-lookup"><span data-stu-id="1f74f-105">NewEmailReceiver (Default)</span></span>
```
New-AzureRmActionGroupReceiver -Name <String> [-EmailReceiver] -EmailAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1f74f-106">NewSmsReceiver</span><span class="sxs-lookup"><span data-stu-id="1f74f-106">NewSmsReceiver</span></span>
```
New-AzureRmActionGroupReceiver -Name <String> [-SmsReceiver] [-CountryCode <String>] -PhoneNumber <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1f74f-107">NewWebhookReceiver</span><span class="sxs-lookup"><span data-stu-id="1f74f-107">NewWebhookReceiver</span></span>
```
New-AzureRmActionGroupReceiver -Name <String> [-WebhookReceiver] -ServiceUri <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1f74f-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1f74f-108">DESCRIPTION</span></span>
<span data-ttu-id="1f74f-109">O cmdlet **New-AzureRmActionGroupReceiver** cria um novo receptor de grupo de ação na memória.</span><span class="sxs-lookup"><span data-stu-id="1f74f-109">The **New-AzureRmActionGroupReceiver** cmdlet creates new action group receiver in memory.</span></span>

## <span data-ttu-id="1f74f-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1f74f-110">EXAMPLES</span></span>

### <span data-ttu-id="1f74f-111">Exemplo 1: criar um novo receptor de email na memória.</span><span class="sxs-lookup"><span data-stu-id="1f74f-111">Example 1: Create a new Email receiver in memory.</span></span>
```
PS C:\>$emailReceiver = New-AzureRmActionGroupReceiver -Name 'emailReceiver1' -EmailReceiver -EmailAddress 'user1@example.com'
```

<span data-ttu-id="1f74f-112">Esse comando cria um novo receptor de email na memória.</span><span class="sxs-lookup"><span data-stu-id="1f74f-112">This command creates a new Email receiver in memory.</span></span>

### <span data-ttu-id="1f74f-113">Exemplo 2: criar um novo receptor de SMS na memória.</span><span class="sxs-lookup"><span data-stu-id="1f74f-113">Example 2: Create a new SMS receiver in memory.</span></span>
```
PS C:\>$smsReceiver = New-AzureRmActionGroupReceiver -Name 'smsReceiver1' -SmsReceiver -CountryCode '1' -PhoneNumber '5555555555'
```

<span data-ttu-id="1f74f-114">Esse comando cria um novo receptor de SMS na memória.</span><span class="sxs-lookup"><span data-stu-id="1f74f-114">This command creates a new SMS receiver in memory.</span></span>

### <span data-ttu-id="1f74f-115">Exemplo 3: criar um novo receptor de webhook na memória.</span><span class="sxs-lookup"><span data-stu-id="1f74f-115">Example 3: Create a new webhook receiver in memory.</span></span>
```
PS C:\>$webhookReceiver = New-AzureRmActionGroupReceiver -Name 'webhookReceiver1' -SMSReceiver -ServiceUri 'http://test.com'
```

<span data-ttu-id="1f74f-116">Esse comando cria um novo receptor de webhook na memória.</span><span class="sxs-lookup"><span data-stu-id="1f74f-116">This command creates a new webhook receiver in memory.</span></span>

## <span data-ttu-id="1f74f-117">OS</span><span class="sxs-lookup"><span data-stu-id="1f74f-117">PARAMETERS</span></span>

### <span data-ttu-id="1f74f-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="1f74f-118">-Name</span></span>
<span data-ttu-id="1f74f-119">Especifica o nome do destinatário.</span><span class="sxs-lookup"><span data-stu-id="1f74f-119">Specifies the name for the receiver.</span></span>

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

### <span data-ttu-id="1f74f-120">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="1f74f-120">-EmailAddress</span></span>
<span data-ttu-id="1f74f-121">Especifica o endereço do receptor de email.</span><span class="sxs-lookup"><span data-stu-id="1f74f-121">Specifies the address for the Email receiver.</span></span>

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

### <span data-ttu-id="1f74f-122">-CountryCode</span><span class="sxs-lookup"><span data-stu-id="1f74f-122">-CountryCode</span></span>
<span data-ttu-id="1f74f-123">Especifica o código de país para o receptor de SMS.</span><span class="sxs-lookup"><span data-stu-id="1f74f-123">Specifies the country code for the SMS receiver.</span></span>

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

### <span data-ttu-id="1f74f-124">-Intervalo</span><span class="sxs-lookup"><span data-stu-id="1f74f-124">-PhoneNumber</span></span>
<span data-ttu-id="1f74f-125">Especifica o número de telefone do receptor de SMS.</span><span class="sxs-lookup"><span data-stu-id="1f74f-125">Specifies the phone number for the SMS receiver.</span></span>

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

### <span data-ttu-id="1f74f-126">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="1f74f-126">-ServiceUri</span></span>
<span data-ttu-id="1f74f-127">Especifica o URI para o receptor de webhook.</span><span class="sxs-lookup"><span data-stu-id="1f74f-127">Specifies the URI for the webhook receiver.</span></span>

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

### <span data-ttu-id="1f74f-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f74f-128">-DefaultProfile</span></span>
<span data-ttu-id="1f74f-129">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1f74f-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f74f-130">-EmailReceiver</span><span class="sxs-lookup"><span data-stu-id="1f74f-130">-EmailReceiver</span></span>
<span data-ttu-id="1f74f-131">Especifica a criação de um receptor de email</span><span class="sxs-lookup"><span data-stu-id="1f74f-131">Specifies to create an Email receiver</span></span>

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

### <span data-ttu-id="1f74f-132">-SmsReceiver</span><span class="sxs-lookup"><span data-stu-id="1f74f-132">-SmsReceiver</span></span>
<span data-ttu-id="1f74f-133">Especifica a criação de um receptor de SMS</span><span class="sxs-lookup"><span data-stu-id="1f74f-133">Specifies to create a SMS receiver</span></span>

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

### <span data-ttu-id="1f74f-134">-WebhookReceiver</span><span class="sxs-lookup"><span data-stu-id="1f74f-134">-WebhookReceiver</span></span>
<span data-ttu-id="1f74f-135">Especifica a criação de um receptor de webhook</span><span class="sxs-lookup"><span data-stu-id="1f74f-135">Specifies to create a webhook receiver</span></span>

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

### <span data-ttu-id="1f74f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f74f-136">CommonParameters</span></span>
<span data-ttu-id="1f74f-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f74f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f74f-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f74f-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f74f-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1f74f-139">INPUTS</span></span>

## <span data-ttu-id="1f74f-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1f74f-140">OUTPUTS</span></span>

### <span data-ttu-id="1f74f-141">Microsoft. Azure. Commands. insights. OutputClasses. PSActionGroupReceiverBase</span><span class="sxs-lookup"><span data-stu-id="1f74f-141">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase</span></span>

## <span data-ttu-id="1f74f-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1f74f-142">NOTES</span></span>

## <span data-ttu-id="1f74f-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1f74f-143">RELATED LINKS</span></span>

<span data-ttu-id="1f74f-144">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md) 
 [Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md) 
 [Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md)</span><span class="sxs-lookup"><span data-stu-id="1f74f-144">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md)
[Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md)
[Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md)</span></span>
