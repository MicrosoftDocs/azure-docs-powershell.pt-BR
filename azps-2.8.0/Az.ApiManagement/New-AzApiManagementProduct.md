---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: E94B88AA-B8B0-49F0-AD36-6707E17B40AD
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementProduct.md
ms.openlocfilehash: 1b99a5ac02364b54cf4411a0341ceaf749b8fa70
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598033"
---
# <span data-ttu-id="5bb16-101">New-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="5bb16-101">New-AzApiManagementProduct</span></span>

## <span data-ttu-id="5bb16-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5bb16-102">SYNOPSIS</span></span>
<span data-ttu-id="5bb16-103">Cria um produto de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="5bb16-103">Creates an API Management product.</span></span>

## <span data-ttu-id="5bb16-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5bb16-104">SYNTAX</span></span>

```
New-AzApiManagementProduct -Context <PsApiManagementContext> [-ProductId <String>] -Title <String>
 [-Description <String>] [-LegalTerms <String>] [-SubscriptionRequired <Boolean>] [-ApprovalRequired <Boolean>]
 [-SubscriptionsLimit <Int32>] [-State <PsApiManagementProductState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5bb16-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5bb16-105">DESCRIPTION</span></span>
<span data-ttu-id="5bb16-106">O cmdlet **New-AzApiManagementProduct** cria um produto de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="5bb16-106">The **New-AzApiManagementProduct** cmdlet creates an API Management product.</span></span>

## <span data-ttu-id="5bb16-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5bb16-107">EXAMPLES</span></span>

### <span data-ttu-id="5bb16-108">Exemplo 1: criar um produto que não exija uma assinatura</span><span class="sxs-lookup"><span data-stu-id="5bb16-108">Example 1: Create a product that does not require a subscription</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementProduct -Context $apimContext -ProductId "0123456789" -Title "Starter" -Description "Starter Product" -LegalTerms "Free for all" -SubscriptionRequired $False -State "Published"
```

<span data-ttu-id="5bb16-109">Esse comando cria um produto de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="5bb16-109">This command creates an API Management product.</span></span>
<span data-ttu-id="5bb16-110">Não é preciso ter uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="5bb16-110">No subscription is required.</span></span>

### <span data-ttu-id="5bb16-111">Exemplo 2: criar um produto que exija uma assinatura e uma aprovação</span><span class="sxs-lookup"><span data-stu-id="5bb16-111">Example 2: Create a product that requires a subscription and approval</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementProduct -Context $apimContext -ProductId "9876543210" -Title "Unlimited" -Description "Subscribers have completely unlimited access to the API. Administrator approval is required." -LegalTerms "Free for all" -ApprovalRequired $True -State "Published" -NotificationPeriod "D10" -SubscriptionPeriod "Y1"
```

<span data-ttu-id="5bb16-112">Esse comando cria um produto.</span><span class="sxs-lookup"><span data-stu-id="5bb16-112">This command creates a product.</span></span>
<span data-ttu-id="5bb16-113">Uma assinatura e aprovação são necessárias.</span><span class="sxs-lookup"><span data-stu-id="5bb16-113">A subscription and approval are required.</span></span>
<span data-ttu-id="5bb16-114">Esse comando define o período de notificação como 10 dias.</span><span class="sxs-lookup"><span data-stu-id="5bb16-114">This command sets the notification period to 10 days.</span></span>
<span data-ttu-id="5bb16-115">A duração da assinatura é definida como um ano.</span><span class="sxs-lookup"><span data-stu-id="5bb16-115">The subscription duration is set to one year.</span></span>

## <span data-ttu-id="5bb16-116">OS</span><span class="sxs-lookup"><span data-stu-id="5bb16-116">PARAMETERS</span></span>

### <span data-ttu-id="5bb16-117">-ApprovalRequired</span><span class="sxs-lookup"><span data-stu-id="5bb16-117">-ApprovalRequired</span></span>
<span data-ttu-id="5bb16-118">Indica se a assinatura do produto requer aprovação ou não.</span><span class="sxs-lookup"><span data-stu-id="5bb16-118">Indicates whether the subscription to the product requires approval or not.</span></span>
<span data-ttu-id="5bb16-119">Por padrão, esse parâmetro é **$false**.</span><span class="sxs-lookup"><span data-stu-id="5bb16-119">By default, this parameter is **$False**.</span></span>

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

### <span data-ttu-id="5bb16-120">-Contexto</span><span class="sxs-lookup"><span data-stu-id="5bb16-120">-Context</span></span>
<span data-ttu-id="5bb16-121">Especifica uma instância de um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="5bb16-121">Specifies an instance of a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5bb16-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bb16-122">-DefaultProfile</span></span>
<span data-ttu-id="5bb16-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5bb16-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5bb16-124">-Descrição</span><span class="sxs-lookup"><span data-stu-id="5bb16-124">-Description</span></span>
<span data-ttu-id="5bb16-125">Especifica a descrição do produto.</span><span class="sxs-lookup"><span data-stu-id="5bb16-125">Specifies the product description.</span></span>

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

### <span data-ttu-id="5bb16-126">-LegalTerms</span><span class="sxs-lookup"><span data-stu-id="5bb16-126">-LegalTerms</span></span>
<span data-ttu-id="5bb16-127">Especifica os termos legais de uso do produto.</span><span class="sxs-lookup"><span data-stu-id="5bb16-127">Specifies the legal terms of use of the product.</span></span>

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

### <span data-ttu-id="5bb16-128">-ProductId</span><span class="sxs-lookup"><span data-stu-id="5bb16-128">-ProductId</span></span>
<span data-ttu-id="5bb16-129">Especifica o identificador do novo produto.</span><span class="sxs-lookup"><span data-stu-id="5bb16-129">Specifies the identifier of new product.</span></span>
<span data-ttu-id="5bb16-130">Se você não especificar esse parâmetro, um novo produto será gerado.</span><span class="sxs-lookup"><span data-stu-id="5bb16-130">If you do not specify this parameter, a new product is generated.</span></span>

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

### <span data-ttu-id="5bb16-131">-Estado</span><span class="sxs-lookup"><span data-stu-id="5bb16-131">-State</span></span>
<span data-ttu-id="5bb16-132">Especifica o estado do produto.</span><span class="sxs-lookup"><span data-stu-id="5bb16-132">Specifies the product state.</span></span>
<span data-ttu-id="5bb16-133">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="5bb16-133">psdx_paramvalues</span></span>
- <span data-ttu-id="5bb16-134">Não publicado</span><span class="sxs-lookup"><span data-stu-id="5bb16-134">NotPublished</span></span>
- <span data-ttu-id="5bb16-135">Publicado o valor padrão é não publicado.</span><span class="sxs-lookup"><span data-stu-id="5bb16-135">Published The default value is NotPublished.</span></span>

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

### <span data-ttu-id="5bb16-136">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="5bb16-136">-SubscriptionRequired</span></span>
<span data-ttu-id="5bb16-137">Indica se o produto exige uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="5bb16-137">Indicates whether the product requires a subscription.</span></span>
<span data-ttu-id="5bb16-138">O valor padrão é **$true**.</span><span class="sxs-lookup"><span data-stu-id="5bb16-138">The default value is **$True**.</span></span>

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

### <span data-ttu-id="5bb16-139">-SubscriptionsLimit</span><span class="sxs-lookup"><span data-stu-id="5bb16-139">-SubscriptionsLimit</span></span>
<span data-ttu-id="5bb16-140">Especifica o número máximo de assinaturas simultâneas.</span><span class="sxs-lookup"><span data-stu-id="5bb16-140">Specifies the maximum number of simultaneous subscriptions.</span></span>
<span data-ttu-id="5bb16-141">O valor padrão é 1.</span><span class="sxs-lookup"><span data-stu-id="5bb16-141">The default value is 1.</span></span>

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

### <span data-ttu-id="5bb16-142">-Título</span><span class="sxs-lookup"><span data-stu-id="5bb16-142">-Title</span></span>
<span data-ttu-id="5bb16-143">Especifica o título do produto.</span><span class="sxs-lookup"><span data-stu-id="5bb16-143">Specifies the product title.</span></span>

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

### <span data-ttu-id="5bb16-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bb16-144">CommonParameters</span></span>
<span data-ttu-id="5bb16-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5bb16-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bb16-146">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5bb16-146">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bb16-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5bb16-147">INPUTS</span></span>

### <span data-ttu-id="5bb16-148">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="5bb16-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="5bb16-149">System. String</span><span class="sxs-lookup"><span data-stu-id="5bb16-149">System.String</span></span>

### <span data-ttu-id="5bb16-150">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="5bb16-150">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="5bb16-151">System. Nullable ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="5bb16-151">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="5bb16-152">System. Nullable ' 1 [[Microsoft. Azure. Commands. ApiManagement. Management. Models. PsApiManagementProductState, Microsoft. Azure. PowerShell. cmdlets. ApiManagement. immanagement, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="5bb16-152">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProductState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="5bb16-153">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5bb16-153">OUTPUTS</span></span>

### <span data-ttu-id="5bb16-154">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="5bb16-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="5bb16-155">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5bb16-155">NOTES</span></span>

## <span data-ttu-id="5bb16-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5bb16-156">RELATED LINKS</span></span>

[<span data-ttu-id="5bb16-157">Get-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="5bb16-157">Get-AzApiManagementProduct</span></span>](./Get-AzApiManagementProduct.md)

[<span data-ttu-id="5bb16-158">Remove-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="5bb16-158">Remove-AzApiManagementProduct</span></span>](./Remove-AzApiManagementProduct.md)

[<span data-ttu-id="5bb16-159">Set-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="5bb16-159">Set-AzApiManagementProduct</span></span>](./Set-AzApiManagementProduct.md)


