---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: E94B88AA-B8B0-49F0-AD36-6707E17B40AD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementProduct.md
ms.openlocfilehash: a978fce4d44a061796597f2f3ae08c78c1021bdd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431217"
---
# <span data-ttu-id="58712-101">New-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="58712-101">New-AzureRmApiManagementProduct</span></span>

## <span data-ttu-id="58712-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="58712-102">SYNOPSIS</span></span>
<span data-ttu-id="58712-103">Cria um produto de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="58712-103">Creates an API Management product.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="58712-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="58712-104">SYNTAX</span></span>

```
New-AzureRmApiManagementProduct -Context <PsApiManagementContext> [-ProductId <String>] -Title <String>
 [-Description <String>] [-LegalTerms <String>] [-SubscriptionRequired <Boolean>] [-ApprovalRequired <Boolean>]
 [-SubscriptionsLimit <Int32>] [-State <PsApiManagementProductState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="58712-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="58712-105">DESCRIPTION</span></span>
<span data-ttu-id="58712-106">O cmdlet **New-AzureRmApiManagementProduct** cria um produto de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="58712-106">The **New-AzureRmApiManagementProduct** cmdlet creates an API Management product.</span></span>

## <span data-ttu-id="58712-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="58712-107">EXAMPLES</span></span>

### <span data-ttu-id="58712-108">Exemplo 1: criar um produto que não exija uma assinatura</span><span class="sxs-lookup"><span data-stu-id="58712-108">Example 1: Create a product that does not require a subscription</span></span>
```
PS C:\>New-AzureRmApiManagementProduct -Context $APImContext -ProductId "0123456789" -Title "Starter" -Description "Starter Product" -LegalTerms "Free for all" -SubscriptionRequired $False -State "Published"
```

<span data-ttu-id="58712-109">Esse comando cria um produto de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="58712-109">This command creates an API Management product.</span></span>
<span data-ttu-id="58712-110">Não é preciso ter uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="58712-110">No subscription is required.</span></span>

### <span data-ttu-id="58712-111">Exemplo 2: criar um produto que exija uma assinatura e uma aprovação</span><span class="sxs-lookup"><span data-stu-id="58712-111">Example 2: Create a product that requires a subscription and approval</span></span>
```
PS C:\>New-AzureRmApiManagementProduct -Context $APImContext -ProductId "9876543210" -Title "Unlimited" -Description "Subscribers have completely unlimited access to the API. Administrator approval is required." -LegalTerms "Free for all" -ApprovalRequired $True -State "Published" -NotificationPeriod "D10" -SubscriptionPeriod "Y1"
```

<span data-ttu-id="58712-112">Esse comando cria um produto.</span><span class="sxs-lookup"><span data-stu-id="58712-112">This command creates a product.</span></span>
<span data-ttu-id="58712-113">Uma assinatura e aprovação são necessárias.</span><span class="sxs-lookup"><span data-stu-id="58712-113">A subscription and approval are required.</span></span>
<span data-ttu-id="58712-114">Esse comando define o período de notificação como 10 dias.</span><span class="sxs-lookup"><span data-stu-id="58712-114">This command sets the notification period to 10 days.</span></span>
<span data-ttu-id="58712-115">A duração da assinatura é definida como um ano.</span><span class="sxs-lookup"><span data-stu-id="58712-115">The subscription duration is set to one year.</span></span>

## <span data-ttu-id="58712-116">OS</span><span class="sxs-lookup"><span data-stu-id="58712-116">PARAMETERS</span></span>

### <span data-ttu-id="58712-117">-ApprovalRequired</span><span class="sxs-lookup"><span data-stu-id="58712-117">-ApprovalRequired</span></span>
<span data-ttu-id="58712-118">Indica se a assinatura do produto requer aprovação ou não.</span><span class="sxs-lookup"><span data-stu-id="58712-118">Indicates whether the subscription to the product requires approval or not.</span></span>
<span data-ttu-id="58712-119">Por padrão, esse parâmetro é **$false**.</span><span class="sxs-lookup"><span data-stu-id="58712-119">By default, this parameter is **$False**.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58712-120">-Contexto</span><span class="sxs-lookup"><span data-stu-id="58712-120">-Context</span></span>
<span data-ttu-id="58712-121">Especifica uma instância de um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="58712-121">Specifies an instance of a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58712-122">-Descrição</span><span class="sxs-lookup"><span data-stu-id="58712-122">-Description</span></span>
<span data-ttu-id="58712-123">Especifica a descrição do produto.</span><span class="sxs-lookup"><span data-stu-id="58712-123">Specifies the product description.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58712-124">-LegalTerms</span><span class="sxs-lookup"><span data-stu-id="58712-124">-LegalTerms</span></span>
<span data-ttu-id="58712-125">Especifica os termos legais de uso do produto.</span><span class="sxs-lookup"><span data-stu-id="58712-125">Specifies the legal terms of use of the product.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58712-126">-ProductId</span><span class="sxs-lookup"><span data-stu-id="58712-126">-ProductId</span></span>
<span data-ttu-id="58712-127">Especifica o identificador do novo produto.</span><span class="sxs-lookup"><span data-stu-id="58712-127">Specifies the identifier of new product.</span></span>
<span data-ttu-id="58712-128">Se você não especificar esse parâmetro, um novo produto será gerado.</span><span class="sxs-lookup"><span data-stu-id="58712-128">If you do not specify this parameter, a new product is generated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58712-129">-Estado</span><span class="sxs-lookup"><span data-stu-id="58712-129">-State</span></span>
<span data-ttu-id="58712-130">Especifica o estado do produto.</span><span class="sxs-lookup"><span data-stu-id="58712-130">Specifies the product state.</span></span>
<span data-ttu-id="58712-131">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="58712-131">psdx_paramvalues</span></span>

- <span data-ttu-id="58712-132">Não publicado</span><span class="sxs-lookup"><span data-stu-id="58712-132">NotPublished</span></span>
- <span data-ttu-id="58712-133">Publish</span><span class="sxs-lookup"><span data-stu-id="58712-133">Published</span></span> 

<span data-ttu-id="58712-134">O valor padrão é não publicado.</span><span class="sxs-lookup"><span data-stu-id="58712-134">The default value is NotPublished.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProductState]
Parameter Sets: (All)
Aliases: 
Accepted values: NotPublished, Published

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58712-135">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="58712-135">-SubscriptionRequired</span></span>
<span data-ttu-id="58712-136">Indica se o produto exige uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="58712-136">Indicates whether the product requires a subscription.</span></span>
<span data-ttu-id="58712-137">O valor padrão é **$true**.</span><span class="sxs-lookup"><span data-stu-id="58712-137">The default value is **$True**.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58712-138">-SubscriptionsLimit</span><span class="sxs-lookup"><span data-stu-id="58712-138">-SubscriptionsLimit</span></span>
<span data-ttu-id="58712-139">Especifica o número máximo de assinaturas simultâneas.</span><span class="sxs-lookup"><span data-stu-id="58712-139">Specifies the maximum number of simultaneous subscriptions.</span></span>
<span data-ttu-id="58712-140">O valor padrão é 1.</span><span class="sxs-lookup"><span data-stu-id="58712-140">The default value is 1.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58712-141">-Título</span><span class="sxs-lookup"><span data-stu-id="58712-141">-Title</span></span>
<span data-ttu-id="58712-142">Especifica o título do produto.</span><span class="sxs-lookup"><span data-stu-id="58712-142">Specifies the product title.</span></span>

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

### <span data-ttu-id="58712-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58712-143">-DefaultProfile</span></span>
<span data-ttu-id="58712-144">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="58712-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58712-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58712-145">CommonParameters</span></span>
<span data-ttu-id="58712-146">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58712-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58712-147">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58712-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58712-148">SENSORES</span><span class="sxs-lookup"><span data-stu-id="58712-148">INPUTS</span></span>

## <span data-ttu-id="58712-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="58712-149">OUTPUTS</span></span>

### <span data-ttu-id="58712-150">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="58712-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="58712-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="58712-151">NOTES</span></span>

## <span data-ttu-id="58712-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="58712-152">RELATED LINKS</span></span>

[<span data-ttu-id="58712-153">Get-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="58712-153">Get-AzureRmApiManagementProduct</span></span>](./Get-AzureRmApiManagementProduct.md)

[<span data-ttu-id="58712-154">Remove-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="58712-154">Remove-AzureRmApiManagementProduct</span></span>](./Remove-AzureRmApiManagementProduct.md)

[<span data-ttu-id="58712-155">Set-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="58712-155">Set-AzureRmApiManagementProduct</span></span>](./Set-AzureRmApiManagementProduct.md)


