---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B85BF332-503D-41CB-A3B7-221B85B9BE30
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSubscription.md
ms.openlocfilehash: 00186ae370b7f5ccaac14bbdc85ba6b1f7aaa762
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890884"
---
# <span data-ttu-id="e8f71-101">New-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="e8f71-101">New-AzApiManagementSubscription</span></span>

## <span data-ttu-id="e8f71-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8f71-102">SYNOPSIS</span></span>
<span data-ttu-id="e8f71-103">Cria uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="e8f71-103">Creates a subscription.</span></span>

## <span data-ttu-id="e8f71-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e8f71-104">SYNTAX</span></span>

### <span data-ttu-id="e8f71-105">OldSubscriptionModel (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e8f71-105">OldSubscriptionModel (Default)</span></span>
```
New-AzApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>] -Name <String>
 -UserId <String> -ProductId <String> [-PrimaryKey <String>] [-SecondaryKey <String>] [-AllowTracing]
 [-State <PsApiManagementSubscriptionState>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e8f71-106">NewSubscriptionModel</span><span class="sxs-lookup"><span data-stu-id="e8f71-106">NewSubscriptionModel</span></span>
```
New-AzApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>] -Name <String>
 [-UserId <String>] -Scope <String> [-PrimaryKey <String>] [-SecondaryKey <String>] [-AllowTracing]
 [-State <PsApiManagementSubscriptionState>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8f71-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e8f71-107">DESCRIPTION</span></span>
<span data-ttu-id="e8f71-108">O cmdlet **New-AzApiManagementSubscription** cria uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="e8f71-108">The **New-AzApiManagementSubscription** cmdlet creates a subscription.</span></span>

## <span data-ttu-id="e8f71-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e8f71-109">EXAMPLES</span></span>

### <span data-ttu-id="e8f71-110">Exemplo 1: Inscrever um usuário em um produto</span><span class="sxs-lookup"><span data-stu-id="e8f71-110">Example 1: Subscribe a user to a product</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementSubscription -Context $apimContext -UserId "777" -ProductId "999"
```

<span data-ttu-id="e8f71-111">Este comando inscreve um usuário existente a um produto.</span><span class="sxs-lookup"><span data-stu-id="e8f71-111">This command subscribes an existing user to a product.</span></span>

### <span data-ttu-id="e8f71-112">Exemplo 2: Criar uma assinatura para todo o Escopo da Api</span><span class="sxs-lookup"><span data-stu-id="e8f71-112">Example 2: Create a subscription for all Api Scope</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementSubscription -Context $context -Scope "/apis" -Name "GlobalApiScope"
```

### <span data-ttu-id="e8f71-113">Exemplo 3: Criar uma assinatura para o Escopo do Produto</span><span class="sxs-lookup"><span data-stu-id="e8f71-113">Example 3: Create a subscription for Product Scope</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementSubscription -Context $context -Scope "/products/starter" -Name "UnlimitedProductSub"
```

## <span data-ttu-id="e8f71-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e8f71-114">PARAMETERS</span></span>

### <span data-ttu-id="e8f71-115">-AllowTracing</span><span class="sxs-lookup"><span data-stu-id="e8f71-115">-AllowTracing</span></span>
<span data-ttu-id="e8f71-116">Sinalizador que determina se o Rastreamento pode ser habilitado no Nível de Assinatura.</span><span class="sxs-lookup"><span data-stu-id="e8f71-116">Flag which determines whether Tracing can be enabled at the Subscription Level.</span></span> <span data-ttu-id="e8f71-117">Este é o parâmetro opcional e o padrão é $null.</span><span class="sxs-lookup"><span data-stu-id="e8f71-117">This is optional parameter and default is $null.</span></span>

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

### <span data-ttu-id="e8f71-118">-Context</span><span class="sxs-lookup"><span data-stu-id="e8f71-118">-Context</span></span>
<span data-ttu-id="e8f71-119">Especifica um **objeto PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="e8f71-119">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="e8f71-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8f71-120">-DefaultProfile</span></span>
<span data-ttu-id="e8f71-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="e8f71-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8f71-122">-Name</span><span class="sxs-lookup"><span data-stu-id="e8f71-122">-Name</span></span>
<span data-ttu-id="e8f71-123">Especifica o nome da assinatura.</span><span class="sxs-lookup"><span data-stu-id="e8f71-123">Specifies the subscription name.</span></span>

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

### <span data-ttu-id="e8f71-124">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="e8f71-124">-PrimaryKey</span></span>
<span data-ttu-id="e8f71-125">Especifica a chave primária de assinatura.</span><span class="sxs-lookup"><span data-stu-id="e8f71-125">Specifies the subscription primary key.</span></span>
<span data-ttu-id="e8f71-126">Se esse parâmetro não for especificado, a chave será gerada automaticamente.</span><span class="sxs-lookup"><span data-stu-id="e8f71-126">If this parameter is not specified the key is generated automatically.</span></span>
<span data-ttu-id="e8f71-127">Esse parâmetro deve ter de 1 a 300 caracteres.</span><span class="sxs-lookup"><span data-stu-id="e8f71-127">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="e8f71-128">-ProductId</span><span class="sxs-lookup"><span data-stu-id="e8f71-128">-ProductId</span></span>
<span data-ttu-id="e8f71-129">Especifica a ID do produto ao qual se inscrever.</span><span class="sxs-lookup"><span data-stu-id="e8f71-129">Specifies the ID of the product to which to subscribe.</span></span>

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

### <span data-ttu-id="e8f71-130">-Scope</span><span class="sxs-lookup"><span data-stu-id="e8f71-130">-Scope</span></span>
<span data-ttu-id="e8f71-131">O Escopo da Assinatura, seja Escopo da Api /apis/{apiId} ou Escopo do Produto /products/{productId} ou Escopo da API Global /apis ou escopo global /.</span><span class="sxs-lookup"><span data-stu-id="e8f71-131">The Scope of the Subscription, whether it is Api Scope /apis/{apiId} or Product Scope /products/{productId} or Global API Scope /apis or Global scope /.</span></span> <span data-ttu-id="e8f71-132">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="e8f71-132">This parameter is required.</span></span>

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

### <span data-ttu-id="e8f71-133">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="e8f71-133">-SecondaryKey</span></span>
<span data-ttu-id="e8f71-134">Especifica a chave secundária de assinatura.</span><span class="sxs-lookup"><span data-stu-id="e8f71-134">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="e8f71-135">Esse parâmetro é gerado automaticamente se não for especificado.</span><span class="sxs-lookup"><span data-stu-id="e8f71-135">This parameter is generated automatically if it is not specified.</span></span>
<span data-ttu-id="e8f71-136">Esse parâmetro deve ter de 1 a 300 caracteres.</span><span class="sxs-lookup"><span data-stu-id="e8f71-136">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="e8f71-137">-State</span><span class="sxs-lookup"><span data-stu-id="e8f71-137">-State</span></span>
<span data-ttu-id="e8f71-138">Especifica o estado da assinatura.</span><span class="sxs-lookup"><span data-stu-id="e8f71-138">Specifies the subscription state.</span></span>
<span data-ttu-id="e8f71-139">O valor padrão é $Null.</span><span class="sxs-lookup"><span data-stu-id="e8f71-139">The default value is $Null.</span></span>

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

### <span data-ttu-id="e8f71-140">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e8f71-140">-SubscriptionId</span></span>
<span data-ttu-id="e8f71-141">Especifica a ID da assinatura.</span><span class="sxs-lookup"><span data-stu-id="e8f71-141">Specifies the subscription ID.</span></span>
<span data-ttu-id="e8f71-142">Esse parâmetro é gerado se não for especificado.</span><span class="sxs-lookup"><span data-stu-id="e8f71-142">This parameter is generated if not specified.</span></span>

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

### <span data-ttu-id="e8f71-143">-UserId</span><span class="sxs-lookup"><span data-stu-id="e8f71-143">-UserId</span></span>
<span data-ttu-id="e8f71-144">Especifica a ID do assinante.</span><span class="sxs-lookup"><span data-stu-id="e8f71-144">Specifies the subscriber ID.</span></span>

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

### <span data-ttu-id="e8f71-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8f71-145">CommonParameters</span></span>
<span data-ttu-id="e8f71-146">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8f71-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8f71-147">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e8f71-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8f71-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e8f71-148">INPUTS</span></span>

### <span data-ttu-id="e8f71-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e8f71-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e8f71-150">System.String</span><span class="sxs-lookup"><span data-stu-id="e8f71-150">System.String</span></span>

### <span data-ttu-id="e8f71-151">System.Nullable'1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="e8f71-151">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="e8f71-152">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e8f71-152">OUTPUTS</span></span>

### <span data-ttu-id="e8f71-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="e8f71-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="e8f71-154">NOTES</span><span class="sxs-lookup"><span data-stu-id="e8f71-154">NOTES</span></span>

## <span data-ttu-id="e8f71-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e8f71-155">RELATED LINKS</span></span>

[<span data-ttu-id="e8f71-156">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="e8f71-156">Get-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="e8f71-157">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="e8f71-157">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)

[<span data-ttu-id="e8f71-158">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="e8f71-158">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)


