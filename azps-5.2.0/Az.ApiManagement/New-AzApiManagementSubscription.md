---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B85BF332-503D-41CB-A3B7-221B85B9BE30
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSubscription.md
ms.openlocfilehash: ea68d17d482a73a528cfe450a84700e48bfdd9f9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98262746"
---
# <span data-ttu-id="873b8-101">New-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="873b8-101">New-AzApiManagementSubscription</span></span>

## <span data-ttu-id="873b8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="873b8-102">SYNOPSIS</span></span>
<span data-ttu-id="873b8-103">Cria uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="873b8-103">Creates a subscription.</span></span>

## <span data-ttu-id="873b8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="873b8-104">SYNTAX</span></span>

### <span data-ttu-id="873b8-105">OldSubscriptionModel (padrão)</span><span class="sxs-lookup"><span data-stu-id="873b8-105">OldSubscriptionModel (Default)</span></span>
```
New-AzApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>] -Name <String>
 -UserId <String> -ProductId <String> [-PrimaryKey <String>] [-SecondaryKey <String>] [-AllowTracing]
 [-State <PsApiManagementSubscriptionState>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="873b8-106">NewSubscriptionModel</span><span class="sxs-lookup"><span data-stu-id="873b8-106">NewSubscriptionModel</span></span>
```
New-AzApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>] -Name <String>
 [-UserId <String>] -Scope <String> [-PrimaryKey <String>] [-SecondaryKey <String>] [-AllowTracing]
 [-State <PsApiManagementSubscriptionState>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="873b8-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="873b8-107">DESCRIPTION</span></span>
<span data-ttu-id="873b8-108">O cmdlet **New-AzApiManagementSubscription** cria uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="873b8-108">The **New-AzApiManagementSubscription** cmdlet creates a subscription.</span></span>

## <span data-ttu-id="873b8-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="873b8-109">EXAMPLES</span></span>

### <span data-ttu-id="873b8-110">Exemplo 1: assinar um usuário para um produto</span><span class="sxs-lookup"><span data-stu-id="873b8-110">Example 1: Subscribe a user to a product</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementSubscription -Context $apimContext -UserId "777" -ProductId "999"
```

<span data-ttu-id="873b8-111">Esse comando assina um usuário existente para um produto.</span><span class="sxs-lookup"><span data-stu-id="873b8-111">This command subscribes an existing user to a product.</span></span>

### <span data-ttu-id="873b8-112">Exemplo 2: criar uma assinatura para todos os escopos de API</span><span class="sxs-lookup"><span data-stu-id="873b8-112">Example 2: Create a subscription for all Api Scope</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementSubscription -Context $context -Scope "/apis" -Name "GlobalApiScope"
```

### <span data-ttu-id="873b8-113">Exemplo 3: criar uma assinatura para o escopo do produto</span><span class="sxs-lookup"><span data-stu-id="873b8-113">Example 3: Create a subscription for Product Scope</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementSubscription -Context $context -Scope "/products/starter" -Name "UnlimitedProductSub"
```

## <span data-ttu-id="873b8-114">OS</span><span class="sxs-lookup"><span data-stu-id="873b8-114">PARAMETERS</span></span>

### <span data-ttu-id="873b8-115">-AllowTracing</span><span class="sxs-lookup"><span data-stu-id="873b8-115">-AllowTracing</span></span>
<span data-ttu-id="873b8-116">Sinalizador que determina se o rastreamento pode ser habilitado no nível da assinatura.</span><span class="sxs-lookup"><span data-stu-id="873b8-116">Flag which determines whether Tracing can be enabled at the Subscription Level.</span></span> <span data-ttu-id="873b8-117">Esse é um parâmetro opcional e o padrão é $null.</span><span class="sxs-lookup"><span data-stu-id="873b8-117">This is optional parameter and default is $null.</span></span>

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

### <span data-ttu-id="873b8-118">-Contexto</span><span class="sxs-lookup"><span data-stu-id="873b8-118">-Context</span></span>
<span data-ttu-id="873b8-119">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="873b8-119">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="873b8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="873b8-120">-DefaultProfile</span></span>
<span data-ttu-id="873b8-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="873b8-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="873b8-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="873b8-122">-Name</span></span>
<span data-ttu-id="873b8-123">Especifica o nome da assinatura.</span><span class="sxs-lookup"><span data-stu-id="873b8-123">Specifies the subscription name.</span></span>

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

### <span data-ttu-id="873b8-124">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="873b8-124">-PrimaryKey</span></span>
<span data-ttu-id="873b8-125">Especifica a chave primária de assinatura.</span><span class="sxs-lookup"><span data-stu-id="873b8-125">Specifies the subscription primary key.</span></span>
<span data-ttu-id="873b8-126">Se esse parâmetro não for especificado, a chave será gerada automaticamente.</span><span class="sxs-lookup"><span data-stu-id="873b8-126">If this parameter is not specified the key is generated automatically.</span></span>
<span data-ttu-id="873b8-127">Esse parâmetro deve ter de 1 a 300 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="873b8-127">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="873b8-128">-ProductId</span><span class="sxs-lookup"><span data-stu-id="873b8-128">-ProductId</span></span>
<span data-ttu-id="873b8-129">Especifica a ID do produto a ser assinado.</span><span class="sxs-lookup"><span data-stu-id="873b8-129">Specifies the ID of the product to which to subscribe.</span></span>

```yaml
Type: System.String
Parameter Sets: OldSubscriptionModel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="873b8-130">-Escopo</span><span class="sxs-lookup"><span data-stu-id="873b8-130">-Scope</span></span>
<span data-ttu-id="873b8-131">O escopo da assinatura, seja o escopo da API/apis/{apiId} ou o escopo do produto/products/{productId} ou o escopo da API global/APIs ou escopo global/.</span><span class="sxs-lookup"><span data-stu-id="873b8-131">The Scope of the Subscription, whether it is Api Scope /apis/{apiId} or Product Scope /products/{productId} or Global API Scope /apis or Global scope /.</span></span> <span data-ttu-id="873b8-132">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="873b8-132">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: NewSubscriptionModel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="873b8-133">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="873b8-133">-SecondaryKey</span></span>
<span data-ttu-id="873b8-134">Especifica a chave secundária de assinatura.</span><span class="sxs-lookup"><span data-stu-id="873b8-134">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="873b8-135">Esse parâmetro é gerado automaticamente se não for especificado.</span><span class="sxs-lookup"><span data-stu-id="873b8-135">This parameter is generated automatically if it is not specified.</span></span>
<span data-ttu-id="873b8-136">Esse parâmetro deve ter de 1 a 300 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="873b8-136">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="873b8-137">-Estado</span><span class="sxs-lookup"><span data-stu-id="873b8-137">-State</span></span>
<span data-ttu-id="873b8-138">Especifica o estado da assinatura.</span><span class="sxs-lookup"><span data-stu-id="873b8-138">Specifies the subscription state.</span></span>
<span data-ttu-id="873b8-139">O valor padrão é $Null.</span><span class="sxs-lookup"><span data-stu-id="873b8-139">The default value is $Null.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState]
Parameter Sets: (All)
Aliases:
Accepted values: Suspended, Active, Expired, Submitted, Rejected, Cancelled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="873b8-140">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="873b8-140">-SubscriptionId</span></span>
<span data-ttu-id="873b8-141">Especifica a ID da assinatura.</span><span class="sxs-lookup"><span data-stu-id="873b8-141">Specifies the subscription ID.</span></span>
<span data-ttu-id="873b8-142">Esse parâmetro é gerado se não for especificado.</span><span class="sxs-lookup"><span data-stu-id="873b8-142">This parameter is generated if not specified.</span></span>

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

### <span data-ttu-id="873b8-143">-UserId</span><span class="sxs-lookup"><span data-stu-id="873b8-143">-UserId</span></span>
<span data-ttu-id="873b8-144">Especifica a identificação do Assinante.</span><span class="sxs-lookup"><span data-stu-id="873b8-144">Specifies the subscriber ID.</span></span>

```yaml
Type: System.String
Parameter Sets: OldSubscriptionModel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: NewSubscriptionModel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="873b8-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="873b8-145">CommonParameters</span></span>
<span data-ttu-id="873b8-146">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="873b8-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="873b8-147">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="873b8-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="873b8-148">SENSORES</span><span class="sxs-lookup"><span data-stu-id="873b8-148">INPUTS</span></span>

### <span data-ttu-id="873b8-149">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="873b8-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="873b8-150">System. String</span><span class="sxs-lookup"><span data-stu-id="873b8-150">System.String</span></span>

### <span data-ttu-id="873b8-151">System. Nullable ' 1 [[Microsoft. Azure. Commands. ApiManagement. Management. Models. PsApiManagementSubscriptionState, Microsoft. Azure. PowerShell. cmdlets. ApiManagement. immanagement, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="873b8-151">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="873b8-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="873b8-152">OUTPUTS</span></span>

### <span data-ttu-id="873b8-153">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="873b8-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="873b8-154">INFORMA</span><span class="sxs-lookup"><span data-stu-id="873b8-154">NOTES</span></span>

## <span data-ttu-id="873b8-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="873b8-155">RELATED LINKS</span></span>

[<span data-ttu-id="873b8-156">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="873b8-156">Get-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="873b8-157">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="873b8-157">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)

[<span data-ttu-id="873b8-158">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="873b8-158">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)


