---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: E94B88AA-B8B0-49F0-AD36-6707E17B40AD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementProduct.md
ms.openlocfilehash: 636a969f6aef013ee947afbb43d398871848818a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432355"
---
# <span data-ttu-id="c56a0-101">New-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="c56a0-101">New-AzureRmApiManagementProduct</span></span>

## <span data-ttu-id="c56a0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c56a0-102">SYNOPSIS</span></span>
<span data-ttu-id="c56a0-103">Cria um produto de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="c56a0-103">Creates an API Management product.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c56a0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c56a0-104">SYNTAX</span></span>

```
New-AzureRmApiManagementProduct -Context <PsApiManagementContext> [-ProductId <String>] -Title <String>
 [-Description <String>] [-LegalTerms <String>] [-SubscriptionRequired <Boolean>] [-ApprovalRequired <Boolean>]
 [-SubscriptionsLimit <Int32>] [-State <PsApiManagementProductState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c56a0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c56a0-105">DESCRIPTION</span></span>
<span data-ttu-id="c56a0-106">O cmdlet **New-AzureRmApiManagementProduct** cria um produto de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="c56a0-106">The **New-AzureRmApiManagementProduct** cmdlet creates an API Management product.</span></span>

## <span data-ttu-id="c56a0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c56a0-107">EXAMPLES</span></span>

### <span data-ttu-id="c56a0-108">Exemplo 1: criar um produto que não exija uma assinatura</span><span class="sxs-lookup"><span data-stu-id="c56a0-108">Example 1: Create a product that does not require a subscription</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementProduct -Context $apimContext -ProductId "0123456789" -Title "Starter" -Description "Starter Product" -LegalTerms "Free for all" -SubscriptionRequired $False -State "Published"
```

<span data-ttu-id="c56a0-109">Esse comando cria um produto de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="c56a0-109">This command creates an API Management product.</span></span>
<span data-ttu-id="c56a0-110">Não é preciso ter uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="c56a0-110">No subscription is required.</span></span>

### <span data-ttu-id="c56a0-111">Exemplo 2: criar um produto que exija uma assinatura e uma aprovação</span><span class="sxs-lookup"><span data-stu-id="c56a0-111">Example 2: Create a product that requires a subscription and approval</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementProduct -Context $apimContext -ProductId "9876543210" -Title "Unlimited" -Description "Subscribers have completely unlimited access to the API. Administrator approval is required." -LegalTerms "Free for all" -ApprovalRequired $True -State "Published" -NotificationPeriod "D10" -SubscriptionPeriod "Y1"
```

<span data-ttu-id="c56a0-112">Esse comando cria um produto.</span><span class="sxs-lookup"><span data-stu-id="c56a0-112">This command creates a product.</span></span>
<span data-ttu-id="c56a0-113">Uma assinatura e aprovação são necessárias.</span><span class="sxs-lookup"><span data-stu-id="c56a0-113">A subscription and approval are required.</span></span>
<span data-ttu-id="c56a0-114">Esse comando define o período de notificação como 10 dias.</span><span class="sxs-lookup"><span data-stu-id="c56a0-114">This command sets the notification period to 10 days.</span></span>
<span data-ttu-id="c56a0-115">A duração da assinatura é definida como um ano.</span><span class="sxs-lookup"><span data-stu-id="c56a0-115">The subscription duration is set to one year.</span></span>

## <span data-ttu-id="c56a0-116">OS</span><span class="sxs-lookup"><span data-stu-id="c56a0-116">PARAMETERS</span></span>

### <span data-ttu-id="c56a0-117">-ApprovalRequired</span><span class="sxs-lookup"><span data-stu-id="c56a0-117">-ApprovalRequired</span></span>
<span data-ttu-id="c56a0-118">Indica se a assinatura do produto requer aprovação ou não.</span><span class="sxs-lookup"><span data-stu-id="c56a0-118">Indicates whether the subscription to the product requires approval or not.</span></span>
<span data-ttu-id="c56a0-119">Por padrão, esse parâmetro é **$false**.</span><span class="sxs-lookup"><span data-stu-id="c56a0-119">By default, this parameter is **$False**.</span></span>

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

### <span data-ttu-id="c56a0-120">-Contexto</span><span class="sxs-lookup"><span data-stu-id="c56a0-120">-Context</span></span>
<span data-ttu-id="c56a0-121">Especifica uma instância de um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="c56a0-121">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="c56a0-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c56a0-122">-DefaultProfile</span></span>
<span data-ttu-id="c56a0-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c56a0-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c56a0-124">-Descrição</span><span class="sxs-lookup"><span data-stu-id="c56a0-124">-Description</span></span>
<span data-ttu-id="c56a0-125">Especifica a descrição do produto.</span><span class="sxs-lookup"><span data-stu-id="c56a0-125">Specifies the product description.</span></span>

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

### <span data-ttu-id="c56a0-126">-LegalTerms</span><span class="sxs-lookup"><span data-stu-id="c56a0-126">-LegalTerms</span></span>
<span data-ttu-id="c56a0-127">Especifica os termos legais de uso do produto.</span><span class="sxs-lookup"><span data-stu-id="c56a0-127">Specifies the legal terms of use of the product.</span></span>

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

### <span data-ttu-id="c56a0-128">-ProductId</span><span class="sxs-lookup"><span data-stu-id="c56a0-128">-ProductId</span></span>
<span data-ttu-id="c56a0-129">Especifica o identificador do novo produto.</span><span class="sxs-lookup"><span data-stu-id="c56a0-129">Specifies the identifier of new product.</span></span>
<span data-ttu-id="c56a0-130">Se você não especificar esse parâmetro, um novo produto será gerado.</span><span class="sxs-lookup"><span data-stu-id="c56a0-130">If you do not specify this parameter, a new product is generated.</span></span>

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

### <span data-ttu-id="c56a0-131">-Estado</span><span class="sxs-lookup"><span data-stu-id="c56a0-131">-State</span></span>
<span data-ttu-id="c56a0-132">Especifica o estado do produto.</span><span class="sxs-lookup"><span data-stu-id="c56a0-132">Specifies the product state.</span></span>
<span data-ttu-id="c56a0-133">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="c56a0-133">psdx_paramvalues</span></span>
- <span data-ttu-id="c56a0-134">Não publicado</span><span class="sxs-lookup"><span data-stu-id="c56a0-134">NotPublished</span></span>
- <span data-ttu-id="c56a0-135">Publicado o valor padrão é não publicado.</span><span class="sxs-lookup"><span data-stu-id="c56a0-135">Published The default value is NotPublished.</span></span>

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

### <span data-ttu-id="c56a0-136">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="c56a0-136">-SubscriptionRequired</span></span>
<span data-ttu-id="c56a0-137">Indica se o produto exige uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="c56a0-137">Indicates whether the product requires a subscription.</span></span>
<span data-ttu-id="c56a0-138">O valor padrão é **$true**.</span><span class="sxs-lookup"><span data-stu-id="c56a0-138">The default value is **$True**.</span></span>

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

### <span data-ttu-id="c56a0-139">-SubscriptionsLimit</span><span class="sxs-lookup"><span data-stu-id="c56a0-139">-SubscriptionsLimit</span></span>
<span data-ttu-id="c56a0-140">Especifica o número máximo de assinaturas simultâneas.</span><span class="sxs-lookup"><span data-stu-id="c56a0-140">Specifies the maximum number of simultaneous subscriptions.</span></span>
<span data-ttu-id="c56a0-141">O valor padrão é 1.</span><span class="sxs-lookup"><span data-stu-id="c56a0-141">The default value is 1.</span></span>

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

### <span data-ttu-id="c56a0-142">-Título</span><span class="sxs-lookup"><span data-stu-id="c56a0-142">-Title</span></span>
<span data-ttu-id="c56a0-143">Especifica o título do produto.</span><span class="sxs-lookup"><span data-stu-id="c56a0-143">Specifies the product title.</span></span>

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

### <span data-ttu-id="c56a0-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c56a0-144">CommonParameters</span></span>
<span data-ttu-id="c56a0-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c56a0-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c56a0-146">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c56a0-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c56a0-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c56a0-147">INPUTS</span></span>

### <span data-ttu-id="c56a0-148">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c56a0-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c56a0-149">System. String</span><span class="sxs-lookup"><span data-stu-id="c56a0-149">System.String</span></span>

### <span data-ttu-id="c56a0-150">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="c56a0-150">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="c56a0-151">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="c56a0-151">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="c56a0-152">System. Nullable ' 1 [[Microsoft. Azure. Commands. ApiManagement. Management. Models. PsApiManagementProductState, Microsoft. Azure. Commands. ApiManagement. onmanagement, Version = 6.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="c56a0-152">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProductState, Microsoft.Azure.Commands.ApiManagement.ServiceManagement, Version=6.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="c56a0-153">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c56a0-153">OUTPUTS</span></span>

### <span data-ttu-id="c56a0-154">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="c56a0-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="c56a0-155">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c56a0-155">NOTES</span></span>

## <span data-ttu-id="c56a0-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c56a0-156">RELATED LINKS</span></span>

[<span data-ttu-id="c56a0-157">Get-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="c56a0-157">Get-AzureRmApiManagementProduct</span></span>](./Get-AzureRmApiManagementProduct.md)

[<span data-ttu-id="c56a0-158">Remove-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="c56a0-158">Remove-AzureRmApiManagementProduct</span></span>](./Remove-AzureRmApiManagementProduct.md)

[<span data-ttu-id="c56a0-159">Set-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="c56a0-159">Set-AzureRmApiManagementProduct</span></span>](./Set-AzureRmApiManagementProduct.md)


