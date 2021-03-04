---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: E94B88AA-B8B0-49F0-AD36-6707E17B40AD
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementProduct.md
ms.openlocfilehash: 12de4862e91555b90a4168ac7ac5908b897d6e49
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890026"
---
# <span data-ttu-id="45664-101">New-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="45664-101">New-AzApiManagementProduct</span></span>

## <span data-ttu-id="45664-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45664-102">SYNOPSIS</span></span>
<span data-ttu-id="45664-103">Cria um produto de Gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="45664-103">Creates an API Management product.</span></span>

## <span data-ttu-id="45664-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="45664-104">SYNTAX</span></span>

```
New-AzApiManagementProduct -Context <PsApiManagementContext> [-ProductId <String>] -Title <String>
 [-Description <String>] [-LegalTerms <String>] [-SubscriptionRequired <Boolean>] [-ApprovalRequired <Boolean>]
 [-SubscriptionsLimit <Int32>] [-State <PsApiManagementProductState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="45664-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="45664-105">DESCRIPTION</span></span>
<span data-ttu-id="45664-106">O cmdlet **New-AzApiManagementProduct** cria um produto de Gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="45664-106">The **New-AzApiManagementProduct** cmdlet creates an API Management product.</span></span>

## <span data-ttu-id="45664-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="45664-107">EXAMPLES</span></span>

### <span data-ttu-id="45664-108">Exemplo 1: Criar um produto que não exige uma assinatura</span><span class="sxs-lookup"><span data-stu-id="45664-108">Example 1: Create a product that does not require a subscription</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementProduct -Context $apimContext -ProductId "0123456789" -Title "Starter" -Description "Starter Product" -LegalTerms "Free for all" -SubscriptionRequired $False -State "Published"
```

<span data-ttu-id="45664-109">Este comando cria um produto de Gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="45664-109">This command creates an API Management product.</span></span>
<span data-ttu-id="45664-110">Nenhuma assinatura é necessária.</span><span class="sxs-lookup"><span data-stu-id="45664-110">No subscription is required.</span></span>

### <span data-ttu-id="45664-111">Exemplo 2: Criar um produto que exija uma assinatura e aprovação</span><span class="sxs-lookup"><span data-stu-id="45664-111">Example 2: Create a product that requires a subscription and approval</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementProduct -Context $apimContext -ProductId "9876543210" -Title "Unlimited" -Description "Subscribers have completely unlimited access to the API. Administrator approval is required." -LegalTerms "Free for all" -ApprovalRequired $True -State "Published" -NotificationPeriod "D10" -SubscriptionPeriod "Y1"
```

<span data-ttu-id="45664-112">Este comando cria um produto.</span><span class="sxs-lookup"><span data-stu-id="45664-112">This command creates a product.</span></span>
<span data-ttu-id="45664-113">Uma assinatura e aprovação são necessárias.</span><span class="sxs-lookup"><span data-stu-id="45664-113">A subscription and approval are required.</span></span>
<span data-ttu-id="45664-114">Este comando define o período de notificação como 10 dias.</span><span class="sxs-lookup"><span data-stu-id="45664-114">This command sets the notification period to 10 days.</span></span>
<span data-ttu-id="45664-115">A duração da assinatura é definida como um ano.</span><span class="sxs-lookup"><span data-stu-id="45664-115">The subscription duration is set to one year.</span></span>

## <span data-ttu-id="45664-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="45664-116">PARAMETERS</span></span>

### <span data-ttu-id="45664-117">-ApprovalRequired</span><span class="sxs-lookup"><span data-stu-id="45664-117">-ApprovalRequired</span></span>
<span data-ttu-id="45664-118">Indica se a assinatura do produto requer aprovação ou não.</span><span class="sxs-lookup"><span data-stu-id="45664-118">Indicates whether the subscription to the product requires approval or not.</span></span>
<span data-ttu-id="45664-119">Por padrão, esse parâmetro é **$False**.</span><span class="sxs-lookup"><span data-stu-id="45664-119">By default, this parameter is **$False**.</span></span>

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

### <span data-ttu-id="45664-120">-Context</span><span class="sxs-lookup"><span data-stu-id="45664-120">-Context</span></span>
<span data-ttu-id="45664-121">Especifica uma instância de um **objeto PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="45664-121">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="45664-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45664-122">-DefaultProfile</span></span>
<span data-ttu-id="45664-123">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="45664-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="45664-124">-Description</span><span class="sxs-lookup"><span data-stu-id="45664-124">-Description</span></span>
<span data-ttu-id="45664-125">Especifica a descrição do produto.</span><span class="sxs-lookup"><span data-stu-id="45664-125">Specifies the product description.</span></span>

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

### <span data-ttu-id="45664-126">-LegalTerms</span><span class="sxs-lookup"><span data-stu-id="45664-126">-LegalTerms</span></span>
<span data-ttu-id="45664-127">Especifica os termos legais de uso do produto.</span><span class="sxs-lookup"><span data-stu-id="45664-127">Specifies the legal terms of use of the product.</span></span>

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

### <span data-ttu-id="45664-128">-ProductId</span><span class="sxs-lookup"><span data-stu-id="45664-128">-ProductId</span></span>
<span data-ttu-id="45664-129">Especifica o identificador do novo produto.</span><span class="sxs-lookup"><span data-stu-id="45664-129">Specifies the identifier of new product.</span></span>
<span data-ttu-id="45664-130">Se você não especificar esse parâmetro, um novo produto será gerado.</span><span class="sxs-lookup"><span data-stu-id="45664-130">If you do not specify this parameter, a new product is generated.</span></span>

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

### <span data-ttu-id="45664-131">-State</span><span class="sxs-lookup"><span data-stu-id="45664-131">-State</span></span>
<span data-ttu-id="45664-132">Especifica o estado do produto.</span><span class="sxs-lookup"><span data-stu-id="45664-132">Specifies the product state.</span></span>
<span data-ttu-id="45664-133">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="45664-133">psdx_paramvalues</span></span>
- <span data-ttu-id="45664-134">NotPublished</span><span class="sxs-lookup"><span data-stu-id="45664-134">NotPublished</span></span>
- <span data-ttu-id="45664-135">Publicado O valor padrão é NotPublished.</span><span class="sxs-lookup"><span data-stu-id="45664-135">Published The default value is NotPublished.</span></span>

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

### <span data-ttu-id="45664-136">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="45664-136">-SubscriptionRequired</span></span>
<span data-ttu-id="45664-137">Indica se o produto requer uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="45664-137">Indicates whether the product requires a subscription.</span></span>
<span data-ttu-id="45664-138">O valor padrão é **$True**.</span><span class="sxs-lookup"><span data-stu-id="45664-138">The default value is **$True**.</span></span>

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

### <span data-ttu-id="45664-139">-SubscriptionsLimit</span><span class="sxs-lookup"><span data-stu-id="45664-139">-SubscriptionsLimit</span></span>
<span data-ttu-id="45664-140">Especifica o número máximo de assinaturas simultâneas.</span><span class="sxs-lookup"><span data-stu-id="45664-140">Specifies the maximum number of simultaneous subscriptions.</span></span>
<span data-ttu-id="45664-141">O valor padrão é None.</span><span class="sxs-lookup"><span data-stu-id="45664-141">The default value is None.</span></span>

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

### <span data-ttu-id="45664-142">-Title</span><span class="sxs-lookup"><span data-stu-id="45664-142">-Title</span></span>
<span data-ttu-id="45664-143">Especifica o título do produto.</span><span class="sxs-lookup"><span data-stu-id="45664-143">Specifies the product title.</span></span>

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

### <span data-ttu-id="45664-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45664-144">CommonParameters</span></span>
<span data-ttu-id="45664-145">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45664-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45664-146">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="45664-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45664-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="45664-147">INPUTS</span></span>

### <span data-ttu-id="45664-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="45664-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="45664-149">System.String</span><span class="sxs-lookup"><span data-stu-id="45664-149">System.String</span></span>

### <span data-ttu-id="45664-150">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="45664-150">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="45664-151">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="45664-151">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="45664-152">System.Nullable'1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProductState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="45664-152">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProductState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="45664-153">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="45664-153">OUTPUTS</span></span>

### <span data-ttu-id="45664-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="45664-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="45664-155">NOTES</span><span class="sxs-lookup"><span data-stu-id="45664-155">NOTES</span></span>

## <span data-ttu-id="45664-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="45664-156">RELATED LINKS</span></span>

[<span data-ttu-id="45664-157">Get-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="45664-157">Get-AzApiManagementProduct</span></span>](./Get-AzApiManagementProduct.md)

[<span data-ttu-id="45664-158">Remove-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="45664-158">Remove-AzApiManagementProduct</span></span>](./Remove-AzApiManagementProduct.md)

[<span data-ttu-id="45664-159">Set-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="45664-159">Set-AzApiManagementProduct</span></span>](./Set-AzApiManagementProduct.md)


