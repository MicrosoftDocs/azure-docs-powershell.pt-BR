---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 9830CD16-D797-47EB-BEF5-6CFE3454BCAA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermactiongroupreceiver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmActionGroupReceiver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmActionGroupReceiver.md
ms.openlocfilehash: 1c35572191ccf66bd7fd4e88e0996a8efdd1b82b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430480"
---
# <span data-ttu-id="e333b-101">New-AzureRmActionGroupReceiver</span><span class="sxs-lookup"><span data-stu-id="e333b-101">New-AzureRmActionGroupReceiver</span></span>

## <span data-ttu-id="e333b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e333b-102">SYNOPSIS</span></span>
<span data-ttu-id="e333b-103">Cria um novo receptor de grupo de ação.</span><span class="sxs-lookup"><span data-stu-id="e333b-103">Creates an new action group receiver.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e333b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e333b-104">SYNTAX</span></span>

### <span data-ttu-id="e333b-105">NewEmailReceiver (padrão)</span><span class="sxs-lookup"><span data-stu-id="e333b-105">NewEmailReceiver (Default)</span></span>
```
New-AzureRmActionGroupReceiver -Name <String> [-EmailReceiver] -EmailAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e333b-106">NewSmsReceiver</span><span class="sxs-lookup"><span data-stu-id="e333b-106">NewSmsReceiver</span></span>
```
New-AzureRmActionGroupReceiver -Name <String> [-SmsReceiver] [-CountryCode <String>] -PhoneNumber <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e333b-107">NewWebhookReceiver</span><span class="sxs-lookup"><span data-stu-id="e333b-107">NewWebhookReceiver</span></span>
```
New-AzureRmActionGroupReceiver -Name <String> [-WebhookReceiver] -ServiceUri <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e333b-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e333b-108">DESCRIPTION</span></span>
<span data-ttu-id="e333b-109">O cmdlet **New-AzureRmActionGroupReceiver** cria um novo receptor de grupo de ação na memória.</span><span class="sxs-lookup"><span data-stu-id="e333b-109">The **New-AzureRmActionGroupReceiver** cmdlet creates new action group receiver in memory.</span></span>

## <span data-ttu-id="e333b-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e333b-110">EXAMPLES</span></span>

### <span data-ttu-id="e333b-111">Exemplo 1: criar um novo receptor de email na memória.</span><span class="sxs-lookup"><span data-stu-id="e333b-111">Example 1: Create a new Email receiver in memory.</span></span>
```
PS C:\>$emailReceiver = New-AzureRmActionGroupReceiver -Name 'emailReceiver1' -EmailReceiver -EmailAddress 'user1@example.com'
```

<span data-ttu-id="e333b-112">Esse comando cria um novo receptor de email na memória.</span><span class="sxs-lookup"><span data-stu-id="e333b-112">This command creates a new Email receiver in memory.</span></span>

### <span data-ttu-id="e333b-113">Exemplo 2: criar um novo receptor de SMS na memória.</span><span class="sxs-lookup"><span data-stu-id="e333b-113">Example 2: Create a new SMS receiver in memory.</span></span>
```
PS C:\>$smsReceiver = New-AzureRmActionGroupReceiver -Name 'smsReceiver1' -SmsReceiver -CountryCode '1' -PhoneNumber '5555555555'
```

<span data-ttu-id="e333b-114">Esse comando cria um novo receptor de SMS na memória.</span><span class="sxs-lookup"><span data-stu-id="e333b-114">This command creates a new SMS receiver in memory.</span></span>

### <span data-ttu-id="e333b-115">Exemplo 3: criar um novo receptor de webhook na memória.</span><span class="sxs-lookup"><span data-stu-id="e333b-115">Example 3: Create a new webhook receiver in memory.</span></span>
```
PS C:\>$webhookReceiver = New-AzureRmActionGroupReceiver -Name 'webhookReceiver1' -SMSReceiver -ServiceUri 'http://test.com'
```

<span data-ttu-id="e333b-116">Esse comando cria um novo receptor de webhook na memória.</span><span class="sxs-lookup"><span data-stu-id="e333b-116">This command creates a new webhook receiver in memory.</span></span>

## <span data-ttu-id="e333b-117">OS</span><span class="sxs-lookup"><span data-stu-id="e333b-117">PARAMETERS</span></span>

### <span data-ttu-id="e333b-118">-CountryCode</span><span class="sxs-lookup"><span data-stu-id="e333b-118">-CountryCode</span></span>
<span data-ttu-id="e333b-119">Especifica o código de país para o receptor de SMS.</span><span class="sxs-lookup"><span data-stu-id="e333b-119">Specifies the country code for the SMS receiver.</span></span>

```yaml
Type: String
Parameter Sets: NewSmsReceiver
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e333b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e333b-120">-DefaultProfile</span></span>
<span data-ttu-id="e333b-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="e333b-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e333b-122">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="e333b-122">-EmailAddress</span></span>
<span data-ttu-id="e333b-123">Especifica o endereço do receptor de email.</span><span class="sxs-lookup"><span data-stu-id="e333b-123">Specifies the address for the Email receiver.</span></span>

```yaml
Type: String
Parameter Sets: NewEmailReceiver
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e333b-124">-EmailReceiver</span><span class="sxs-lookup"><span data-stu-id="e333b-124">-EmailReceiver</span></span>
<span data-ttu-id="e333b-125">Especifica a criação de um receptor de email</span><span class="sxs-lookup"><span data-stu-id="e333b-125">Specifies to create an Email receiver</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: NewEmailReceiver
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e333b-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="e333b-126">-Name</span></span>
<span data-ttu-id="e333b-127">Especifica o nome do destinatário.</span><span class="sxs-lookup"><span data-stu-id="e333b-127">Specifies the name for the receiver.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e333b-128">-Intervalo</span><span class="sxs-lookup"><span data-stu-id="e333b-128">-PhoneNumber</span></span>
<span data-ttu-id="e333b-129">Especifica o número de telefone do receptor de SMS.</span><span class="sxs-lookup"><span data-stu-id="e333b-129">Specifies the phone number for the SMS receiver.</span></span>

```yaml
Type: String
Parameter Sets: NewSmsReceiver
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e333b-130">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="e333b-130">-ServiceUri</span></span>
<span data-ttu-id="e333b-131">Especifica o URI para o receptor de webhook.</span><span class="sxs-lookup"><span data-stu-id="e333b-131">Specifies the URI for the webhook receiver.</span></span>

```yaml
Type: String
Parameter Sets: NewWebhookReceiver
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e333b-132">-SmsReceiver</span><span class="sxs-lookup"><span data-stu-id="e333b-132">-SmsReceiver</span></span>
<span data-ttu-id="e333b-133">Especifica a criação de um receptor de SMS</span><span class="sxs-lookup"><span data-stu-id="e333b-133">Specifies to create a SMS receiver</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: NewSmsReceiver
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e333b-134">-WebhookReceiver</span><span class="sxs-lookup"><span data-stu-id="e333b-134">-WebhookReceiver</span></span>
<span data-ttu-id="e333b-135">Especifica a criação de um receptor de webhook</span><span class="sxs-lookup"><span data-stu-id="e333b-135">Specifies to create a webhook receiver</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: NewWebhookReceiver
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e333b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e333b-136">CommonParameters</span></span>
<span data-ttu-id="e333b-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e333b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e333b-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e333b-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e333b-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e333b-139">INPUTS</span></span>

### <span data-ttu-id="e333b-140">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="e333b-140">None</span></span>
<span data-ttu-id="e333b-141">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="e333b-141">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e333b-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e333b-142">OUTPUTS</span></span>

### <span data-ttu-id="e333b-143">Microsoft. Azure. Commands. insights. OutputClasses. PSActionGroupReceiverBase</span><span class="sxs-lookup"><span data-stu-id="e333b-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase</span></span>

## <span data-ttu-id="e333b-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e333b-144">NOTES</span></span>

## <span data-ttu-id="e333b-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e333b-145">RELATED LINKS</span></span>

<span data-ttu-id="e333b-146">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md) 
 [Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md) 
 [Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md)</span><span class="sxs-lookup"><span data-stu-id="e333b-146">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md)
[Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md)
[Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md)</span></span>
