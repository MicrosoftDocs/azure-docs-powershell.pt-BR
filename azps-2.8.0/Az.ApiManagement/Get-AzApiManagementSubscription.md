---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 227EF8A2-E04A-4F6B-B66E-E77F1276A7E4
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSubscription.md
ms.openlocfilehash: 13ca3444a48d79b3708042f6cf8fd0229f80676a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598094"
---
# <span data-ttu-id="decd6-101">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="decd6-101">Get-AzApiManagementSubscription</span></span>

## <span data-ttu-id="decd6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="decd6-102">SYNOPSIS</span></span>
<span data-ttu-id="decd6-103">Obtém assinaturas.</span><span class="sxs-lookup"><span data-stu-id="decd6-103">Gets subscriptions.</span></span>

## <span data-ttu-id="decd6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="decd6-104">SYNTAX</span></span>

### <span data-ttu-id="decd6-105">GetAllSubscriptions (padrão)</span><span class="sxs-lookup"><span data-stu-id="decd6-105">GetAllSubscriptions (Default)</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="decd6-106">GetBySubscriptionId</span><span class="sxs-lookup"><span data-stu-id="decd6-106">GetBySubscriptionId</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="decd6-107">GetByProductIdAndUser</span><span class="sxs-lookup"><span data-stu-id="decd6-107">GetByProductIdAndUser</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> -UserId <String> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="decd6-108">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="decd6-108">GetByUserId</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="decd6-109">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="decd6-109">GetByProductId</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="decd6-110">GetByScope</span><span class="sxs-lookup"><span data-stu-id="decd6-110">GetByScope</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> -Scope <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="decd6-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="decd6-111">DESCRIPTION</span></span>
<span data-ttu-id="decd6-112">O cmdlet **Get-AzApiManagementSubscription** Obtém uma assinatura especificada, ou todas as assinaturas, se nenhuma assinatura for especificada.</span><span class="sxs-lookup"><span data-stu-id="decd6-112">The **Get-AzApiManagementSubscription** cmdlet gets a specified subscription, or all subscriptions, if no subscription is specified.</span></span>

## <span data-ttu-id="decd6-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="decd6-113">EXAMPLES</span></span>

### <span data-ttu-id="decd6-114">Exemplo 1: obter todas as assinaturas</span><span class="sxs-lookup"><span data-stu-id="decd6-114">Example 1: Get all subscriptions</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext
```

<span data-ttu-id="decd6-115">Este comando obtém todas as assinaturas.</span><span class="sxs-lookup"><span data-stu-id="decd6-115">This command gets all subscriptions.</span></span>

### <span data-ttu-id="decd6-116">Exemplo 2: obter uma assinatura com uma ID especificada</span><span class="sxs-lookup"><span data-stu-id="decd6-116">Example 2: Get a subscription with a specified ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789"
```

<span data-ttu-id="decd6-117">Este comando obtém uma assinatura por ID.</span><span class="sxs-lookup"><span data-stu-id="decd6-117">This command gets a subscription by ID.</span></span>

### <span data-ttu-id="decd6-118">Exemplo 3: obter todas as assinaturas de um usuário</span><span class="sxs-lookup"><span data-stu-id="decd6-118">Example 3: Get all subscriptions for a user</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -UserId "777"
```

<span data-ttu-id="decd6-119">Este comando obtém as assinaturas de um usuário.</span><span class="sxs-lookup"><span data-stu-id="decd6-119">This command gets a user's subscriptions.</span></span>

### <span data-ttu-id="decd6-120">Exemplo 4: obter todas as assinaturas de um produto</span><span class="sxs-lookup"><span data-stu-id="decd6-120">Example 4: Get all subscriptions for a product</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -ProductId "999"
```

<span data-ttu-id="decd6-121">Este comando obtém todas as assinaturas do produto.</span><span class="sxs-lookup"><span data-stu-id="decd6-121">This command gets all subscriptions for the product.</span></span>

### <span data-ttu-id="decd6-122">Exemplo 5: obter todas as assinaturas de um escopo</span><span class="sxs-lookup"><span data-stu-id="decd6-122">Example 5: Get all subscriptions for a Scope</span></span>
```
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

<span data-ttu-id="decd6-123">Este comando obtém todas as assinaturas configuradas para o escopo da API global</span><span class="sxs-lookup"><span data-stu-id="decd6-123">This command gets all subscriptions which are configured for global api scope</span></span>

### <span data-ttu-id="decd6-124">Exemplo 5: obter todas as assinaturas para um produto e um escopo de usuário</span><span class="sxs-lookup"><span data-stu-id="decd6-124">Example 5: Get all subscriptions for a product and user scope</span></span>
```
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

<span data-ttu-id="decd6-125">Este comando obtém todas as assinaturas configuradas para o escopo da API global</span><span class="sxs-lookup"><span data-stu-id="decd6-125">This command gets all subscriptions which are configured for global api scope</span></span>

## <span data-ttu-id="decd6-126">OS</span><span class="sxs-lookup"><span data-stu-id="decd6-126">PARAMETERS</span></span>

### <span data-ttu-id="decd6-127">-Contexto</span><span class="sxs-lookup"><span data-stu-id="decd6-127">-Context</span></span>
<span data-ttu-id="decd6-128">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="decd6-128">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="decd6-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="decd6-129">-DefaultProfile</span></span>
<span data-ttu-id="decd6-130">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="decd6-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="decd6-131">-ProductId</span><span class="sxs-lookup"><span data-stu-id="decd6-131">-ProductId</span></span>
<span data-ttu-id="decd6-132">Especifica um identificador de produto.</span><span class="sxs-lookup"><span data-stu-id="decd6-132">Specifies a product identifier.</span></span>
<span data-ttu-id="decd6-133">Se especificado, esse cmdlet encontra todas as assinaturas pelo identificador do produto.</span><span class="sxs-lookup"><span data-stu-id="decd6-133">If specified, this cmdlet finds all subscriptions by the product identifier.</span></span>

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

### <span data-ttu-id="decd6-134">-Escopo</span><span class="sxs-lookup"><span data-stu-id="decd6-134">-Scope</span></span>
<span data-ttu-id="decd6-135">Identificador de escopo.</span><span class="sxs-lookup"><span data-stu-id="decd6-135">Scope identifier.</span></span> <span data-ttu-id="decd6-136">O escopo da assinatura, seja o escopo da API/apis/{apiId} ou o escopo do produto/products/{productId} ou o escopo da API global/APIs ou escopo global/.</span><span class="sxs-lookup"><span data-stu-id="decd6-136">The Scope of the Subscription, whether it is Api Scope /apis/{apiId} or Product Scope /products/{productId} or Global API Scope /apis or Global scope /.</span></span>

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

### <span data-ttu-id="decd6-137">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="decd6-137">-SubscriptionId</span></span>
<span data-ttu-id="decd6-138">Especifica um identificador de assinatura.</span><span class="sxs-lookup"><span data-stu-id="decd6-138">Specifies a subscription identifier.</span></span>
<span data-ttu-id="decd6-139">Se especificado, esse cmdlet localiza a assinatura pelo identificador.</span><span class="sxs-lookup"><span data-stu-id="decd6-139">If specified, this cmdlet finds subscription by the identifier.</span></span>

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

### <span data-ttu-id="decd6-140">-UserId</span><span class="sxs-lookup"><span data-stu-id="decd6-140">-UserId</span></span>
<span data-ttu-id="decd6-141">Especifica um identificador de usuário.</span><span class="sxs-lookup"><span data-stu-id="decd6-141">Specifies a user identifier.</span></span>
<span data-ttu-id="decd6-142">Se especificado, esse cmdlet encontra todas as assinaturas pelo identificador de usuário.</span><span class="sxs-lookup"><span data-stu-id="decd6-142">If specified, this cmdlet finds all subscriptions by the user identifier.</span></span>

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

### <span data-ttu-id="decd6-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="decd6-143">CommonParameters</span></span>
<span data-ttu-id="decd6-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="decd6-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="decd6-145">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="decd6-145">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="decd6-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="decd6-146">INPUTS</span></span>

### <span data-ttu-id="decd6-147">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="decd6-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="decd6-148">System. String</span><span class="sxs-lookup"><span data-stu-id="decd6-148">System.String</span></span>

## <span data-ttu-id="decd6-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="decd6-149">OUTPUTS</span></span>

### <span data-ttu-id="decd6-150">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="decd6-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="decd6-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="decd6-151">NOTES</span></span>

## <span data-ttu-id="decd6-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="decd6-152">RELATED LINKS</span></span>

[<span data-ttu-id="decd6-153">New-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="decd6-153">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="decd6-154">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="decd6-154">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)

[<span data-ttu-id="decd6-155">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="decd6-155">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)


