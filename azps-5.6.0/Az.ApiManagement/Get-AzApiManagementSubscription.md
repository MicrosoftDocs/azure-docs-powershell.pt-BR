---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 227EF8A2-E04A-4F6B-B66E-E77F1276A7E4
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSubscription.md
ms.openlocfilehash: 26e555be760a71defc7f21f5ffc84cada7a21d04
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893259"
---
# <span data-ttu-id="4c756-101">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="4c756-101">Get-AzApiManagementSubscription</span></span>

## <span data-ttu-id="4c756-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c756-102">SYNOPSIS</span></span>
<span data-ttu-id="4c756-103">Obtém assinaturas.</span><span class="sxs-lookup"><span data-stu-id="4c756-103">Gets subscriptions.</span></span>

## <span data-ttu-id="4c756-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="4c756-104">SYNTAX</span></span>

### <span data-ttu-id="4c756-105">GetAllSubscriptions (Padrão)</span><span class="sxs-lookup"><span data-stu-id="4c756-105">GetAllSubscriptions (Default)</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4c756-106">GetBySubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4c756-106">GetBySubscriptionId</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4c756-107">GetByProductIdAndUser</span><span class="sxs-lookup"><span data-stu-id="4c756-107">GetByProductIdAndUser</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> -UserId <String> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4c756-108">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="4c756-108">GetByUserId</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4c756-109">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="4c756-109">GetByProductId</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4c756-110">GetByScope</span><span class="sxs-lookup"><span data-stu-id="4c756-110">GetByScope</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> -Scope <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4c756-111">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="4c756-111">DESCRIPTION</span></span>
<span data-ttu-id="4c756-112">O cmdlet **Get-AzApiManagementSubscription** obtém uma assinatura especificada ou todas as assinaturas, se nenhuma assinatura for especificada.</span><span class="sxs-lookup"><span data-stu-id="4c756-112">The **Get-AzApiManagementSubscription** cmdlet gets a specified subscription, or all subscriptions, if no subscription is specified.</span></span>
<span data-ttu-id="4c756-113">As chaves não serão incluídas nos detalhes do resultado.</span><span class="sxs-lookup"><span data-stu-id="4c756-113">Keys will not be included into result details.</span></span> <span data-ttu-id="4c756-114">Para obter chaves, use **Get-AzApiManagementSubscriptionKey**.</span><span class="sxs-lookup"><span data-stu-id="4c756-114">To get keys, use **Get-AzApiManagementSubscriptionKey**.</span></span>

## <span data-ttu-id="4c756-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4c756-115">EXAMPLES</span></span>

### <span data-ttu-id="4c756-116">Exemplo 1: Obter todas as assinaturas</span><span class="sxs-lookup"><span data-stu-id="4c756-116">Example 1: Get all subscriptions</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext
```

<span data-ttu-id="4c756-117">Este comando obtém todas as assinaturas.</span><span class="sxs-lookup"><span data-stu-id="4c756-117">This command gets all subscriptions.</span></span>

### <span data-ttu-id="4c756-118">Exemplo 2: Obter uma assinatura com uma ID especificada</span><span class="sxs-lookup"><span data-stu-id="4c756-118">Example 2: Get a subscription with a specified ID</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789"
```

<span data-ttu-id="4c756-119">Este comando obtém uma assinatura por ID.</span><span class="sxs-lookup"><span data-stu-id="4c756-119">This command gets a subscription by ID.</span></span>

### <span data-ttu-id="4c756-120">Exemplo 3: Obter todas as assinaturas de um usuário</span><span class="sxs-lookup"><span data-stu-id="4c756-120">Example 3: Get all subscriptions for a user</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -UserId "777"
```

<span data-ttu-id="4c756-121">Esse comando obtém assinaturas de um usuário.</span><span class="sxs-lookup"><span data-stu-id="4c756-121">This command gets a user's subscriptions.</span></span>

### <span data-ttu-id="4c756-122">Exemplo 4: Obter todas as assinaturas de um produto</span><span class="sxs-lookup"><span data-stu-id="4c756-122">Example 4: Get all subscriptions for a product</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -ProductId "999"
```

<span data-ttu-id="4c756-123">Este comando obtém todas as assinaturas do produto.</span><span class="sxs-lookup"><span data-stu-id="4c756-123">This command gets all subscriptions for the product.</span></span>

### <span data-ttu-id="4c756-124">Exemplo 5: Obter todas as assinaturas de um Escopo</span><span class="sxs-lookup"><span data-stu-id="4c756-124">Example 5: Get all subscriptions for a Scope</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -Scope "/apis"

SubscriptionId    : allApScope
UserId            :
OwnerId           :
ProductId         :
Scope             : /subscriptions/subid/resourceGroups/Api-Default-East-US/providers/Microsoft.ApiManagement/service/contoso/apis
Name              : All Api Scope
State             : Active
CreatedDate       : 6/18/2019 5:53:49 PM
StartDate         :
ExpirationDate    :
EndDate           :
NotificationDate  :
PrimaryKey        : 5e48532634114fe999a6979ce0d63a64
SecondaryKey      : 0a8efaf85a664aa0a412241015c7c8f6
StateComment      :
AllowTracing      : False
Id                : /subscriptions/subid/resourceGroups/Api-Default-East-US/providers/Microsoft.ApiManagement/service/contoso/subscriptions/allApScope
ResourceGroupName : Api-Default-East-US
ServiceName       : contoso
```

<span data-ttu-id="4c756-125">Este comando obtém todas as assinaturas configuradas para escopo de api global</span><span class="sxs-lookup"><span data-stu-id="4c756-125">This command gets all subscriptions which are configured for global api scope</span></span>

### <span data-ttu-id="4c756-126">Exemplo 6: Obter todas as assinaturas de um produto e escopo de usuário</span><span class="sxs-lookup"><span data-stu-id="4c756-126">Example 6: Get all subscriptions for a product and user scope</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -ProductId 59b872f28a82740f547e6270 -UserId 1

SubscriptionId    : 59b872f38a82741750c8da56
UserId            : 1
OwnerId           : /subscriptions/subid/resourceGroups/Api-Default-East-US/providers/Microsoft.ApiManagement/service/contoso/users/1
ProductId         : 59b872f28a82740f547e6270
Scope             : /subscriptions/subid/resourceGroups/Api-Default-East-US/providers/Microsoft.ApiManagement/service/contoso/products/59b872f28a82740f547e6270
Name              :
State             : Active
CreatedDate       : 9/12/2017 11:51:15 PM
StartDate         : 9/12/2017 12:00:00 AM
ExpirationDate    :
EndDate           :
NotificationDate  :
PrimaryKey        : 7e64ef904b194706835febf87f729bb0
SecondaryKey      : 0354fccef73e43feb82e5c5da17674d5
StateComment      :
AllowTracing      : True
Id                : /subscriptions/subid/resourceGroups/Api-Default-East-US/providers/Microsoft.ApiManagement/service/contoso/subscriptions/59b872f38a82741750c8da56
ResourceGroupName : Api-Default-East-US
ServiceName       : contoso
```

<span data-ttu-id="4c756-127">Este comando obtém todas as assinaturas configuradas para escopo de api global</span><span class="sxs-lookup"><span data-stu-id="4c756-127">This command gets all subscriptions which are configured for global api scope</span></span>

## <span data-ttu-id="4c756-128">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="4c756-128">PARAMETERS</span></span>

### <span data-ttu-id="4c756-129">-Context</span><span class="sxs-lookup"><span data-stu-id="4c756-129">-Context</span></span>
<span data-ttu-id="4c756-130">Especifica um **objeto PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="4c756-130">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="4c756-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c756-131">-DefaultProfile</span></span>
<span data-ttu-id="4c756-132">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="4c756-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4c756-133">-ProductId</span><span class="sxs-lookup"><span data-stu-id="4c756-133">-ProductId</span></span>
<span data-ttu-id="4c756-134">Especifica um identificador de produto.</span><span class="sxs-lookup"><span data-stu-id="4c756-134">Specifies a product identifier.</span></span>
<span data-ttu-id="4c756-135">Se especificado, este cmdlet localiza todas as assinaturas pelo identificador do produto.</span><span class="sxs-lookup"><span data-stu-id="4c756-135">If specified, this cmdlet finds all subscriptions by the product identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByProductIdAndUser
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByProductId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c756-136">-Scope</span><span class="sxs-lookup"><span data-stu-id="4c756-136">-Scope</span></span>
<span data-ttu-id="4c756-137">Identificador de escopo.</span><span class="sxs-lookup"><span data-stu-id="4c756-137">Scope identifier.</span></span> <span data-ttu-id="4c756-138">O Escopo da Assinatura, seja Escopo da Api /apis/{apiId} ou Escopo do Produto /products/{productId} ou Escopo da API Global /apis ou escopo global /.</span><span class="sxs-lookup"><span data-stu-id="4c756-138">The Scope of the Subscription, whether it is Api Scope /apis/{apiId} or Product Scope /products/{productId} or Global API Scope /apis or Global scope /.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c756-139">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4c756-139">-SubscriptionId</span></span>
<span data-ttu-id="4c756-140">Especifica um identificador de assinatura.</span><span class="sxs-lookup"><span data-stu-id="4c756-140">Specifies a subscription identifier.</span></span>
<span data-ttu-id="4c756-141">Se especificado, este cmdlet localiza a assinatura pelo identificador.</span><span class="sxs-lookup"><span data-stu-id="4c756-141">If specified, this cmdlet finds subscription by the identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetBySubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c756-142">-UserId</span><span class="sxs-lookup"><span data-stu-id="4c756-142">-UserId</span></span>
<span data-ttu-id="4c756-143">Especifica um identificador de usuário.</span><span class="sxs-lookup"><span data-stu-id="4c756-143">Specifies a user identifier.</span></span>
<span data-ttu-id="4c756-144">Se especificado, esse cmdlet localiza todas as assinaturas pelo identificador do usuário.</span><span class="sxs-lookup"><span data-stu-id="4c756-144">If specified, this cmdlet finds all subscriptions by the user identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByProductIdAndUser
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByUserId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c756-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c756-145">CommonParameters</span></span>
<span data-ttu-id="4c756-146">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c756-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c756-147">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4c756-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c756-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4c756-148">INPUTS</span></span>

### <span data-ttu-id="4c756-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="4c756-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="4c756-150">System.String</span><span class="sxs-lookup"><span data-stu-id="4c756-150">System.String</span></span>

## <span data-ttu-id="4c756-151">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="4c756-151">OUTPUTS</span></span>

### <span data-ttu-id="4c756-152">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="4c756-152">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="4c756-153">NOTES</span><span class="sxs-lookup"><span data-stu-id="4c756-153">NOTES</span></span>

## <span data-ttu-id="4c756-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4c756-154">RELATED LINKS</span></span>

[<span data-ttu-id="4c756-155">New-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="4c756-155">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="4c756-156">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="4c756-156">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)

[<span data-ttu-id="4c756-157">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="4c756-157">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)


