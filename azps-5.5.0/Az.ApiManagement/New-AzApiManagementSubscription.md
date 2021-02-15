---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B85BF332-503D-41CB-A3B7-221B85B9BE30
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSubscription.md
ms.openlocfilehash: ea68d17d482a73a528cfe450a84700e48bfdd9f9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118047"
---
# <span data-ttu-id="af9ca-101">New-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="af9ca-101">New-AzApiManagementSubscription</span></span>

## <span data-ttu-id="af9ca-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="af9ca-102">SYNOPSIS</span></span>
<span data-ttu-id="af9ca-103">Cria uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="af9ca-103">Creates a subscription.</span></span>

## <span data-ttu-id="af9ca-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="af9ca-104">SYNTAX</span></span>

### <span data-ttu-id="af9ca-105">OldSubscriptionModel (Padrão)</span><span class="sxs-lookup"><span data-stu-id="af9ca-105">OldSubscriptionModel (Default)</span></span>
```
New-AzApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>] -Name <String>
 -UserId <String> -ProductId <String> [-PrimaryKey <String>] [-SecondaryKey <String>] [-AllowTracing]
 [-State <PsApiManagementSubscriptionState>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af9ca-106">NewSubscriptionModel</span><span class="sxs-lookup"><span data-stu-id="af9ca-106">NewSubscriptionModel</span></span>
```
New-AzApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>] -Name <String>
 [-UserId <String>] -Scope <String> [-PrimaryKey <String>] [-SecondaryKey <String>] [-AllowTracing]
 [-State <PsApiManagementSubscriptionState>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="af9ca-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="af9ca-107">DESCRIPTION</span></span>
<span data-ttu-id="af9ca-108">O **cmdlet New-AzApiManagementSubscription** cria uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="af9ca-108">The **New-AzApiManagementSubscription** cmdlet creates a subscription.</span></span>

## <span data-ttu-id="af9ca-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="af9ca-109">EXAMPLES</span></span>

### <span data-ttu-id="af9ca-110">Exemplo 1: Inscrever um usuário em um produto</span><span class="sxs-lookup"><span data-stu-id="af9ca-110">Example 1: Subscribe a user to a product</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementSubscription -Context $apimContext -UserId "777" -ProductId "999"
```

<span data-ttu-id="af9ca-111">Este comando inscreve um usuário existente a um produto.</span><span class="sxs-lookup"><span data-stu-id="af9ca-111">This command subscribes an existing user to a product.</span></span>

### <span data-ttu-id="af9ca-112">Exemplo 2: Criar uma assinatura para todo o Escopo da Api</span><span class="sxs-lookup"><span data-stu-id="af9ca-112">Example 2: Create a subscription for all Api Scope</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementSubscription -Context $context -Scope "/apis" -Name "GlobalApiScope"
```

### <span data-ttu-id="af9ca-113">Exemplo 3: Criar uma assinatura para o Escopo do Produto</span><span class="sxs-lookup"><span data-stu-id="af9ca-113">Example 3: Create a subscription for Product Scope</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementSubscription -Context $context -Scope "/products/starter" -Name "UnlimitedProductSub"
```

## <span data-ttu-id="af9ca-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="af9ca-114">PARAMETERS</span></span>

### <span data-ttu-id="af9ca-115">-AllowTracing</span><span class="sxs-lookup"><span data-stu-id="af9ca-115">-AllowTracing</span></span>
<span data-ttu-id="af9ca-116">Sinalizador que determina se o Rastreamento pode ser habilitado no Nível de Assinatura.</span><span class="sxs-lookup"><span data-stu-id="af9ca-116">Flag which determines whether Tracing can be enabled at the Subscription Level.</span></span> <span data-ttu-id="af9ca-117">Esse parâmetro é opcional e o padrão é $null.</span><span class="sxs-lookup"><span data-stu-id="af9ca-117">This is optional parameter and default is $null.</span></span>

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

### <span data-ttu-id="af9ca-118">-Contexto</span><span class="sxs-lookup"><span data-stu-id="af9ca-118">-Context</span></span>
<span data-ttu-id="af9ca-119">Especifica um **objeto PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="af9ca-119">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="af9ca-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af9ca-120">-DefaultProfile</span></span>
<span data-ttu-id="af9ca-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="af9ca-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="af9ca-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="af9ca-122">-Name</span></span>
<span data-ttu-id="af9ca-123">Especifica o nome da assinatura.</span><span class="sxs-lookup"><span data-stu-id="af9ca-123">Specifies the subscription name.</span></span>

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

### <span data-ttu-id="af9ca-124">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="af9ca-124">-PrimaryKey</span></span>
<span data-ttu-id="af9ca-125">Especifica a chave primária da assinatura.</span><span class="sxs-lookup"><span data-stu-id="af9ca-125">Specifies the subscription primary key.</span></span>
<span data-ttu-id="af9ca-126">Se esse parâmetro não for especificado, a chave será gerada automaticamente.</span><span class="sxs-lookup"><span data-stu-id="af9ca-126">If this parameter is not specified the key is generated automatically.</span></span>
<span data-ttu-id="af9ca-127">Esse parâmetro deve ter de 1 a 300 caracteres.</span><span class="sxs-lookup"><span data-stu-id="af9ca-127">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="af9ca-128">-ProductId</span><span class="sxs-lookup"><span data-stu-id="af9ca-128">-ProductId</span></span>
<span data-ttu-id="af9ca-129">Especifica a ID do produto ao qual se inscrever.</span><span class="sxs-lookup"><span data-stu-id="af9ca-129">Specifies the ID of the product to which to subscribe.</span></span>

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

### <span data-ttu-id="af9ca-130">-Escopo</span><span class="sxs-lookup"><span data-stu-id="af9ca-130">-Scope</span></span>
<span data-ttu-id="af9ca-131">O Escopo da Assinatura, seja o Escopo da Api /apis/{apiId} ou o Escopo do Produto /products/{productId} ou Escopo da API Global /apis ou escopo global /.</span><span class="sxs-lookup"><span data-stu-id="af9ca-131">The Scope of the Subscription, whether it is Api Scope /apis/{apiId} or Product Scope /products/{productId} or Global API Scope /apis or Global scope /.</span></span> <span data-ttu-id="af9ca-132">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="af9ca-132">This parameter is required.</span></span>

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

### <span data-ttu-id="af9ca-133">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="af9ca-133">-SecondaryKey</span></span>
<span data-ttu-id="af9ca-134">Especifica a chave secundária da assinatura.</span><span class="sxs-lookup"><span data-stu-id="af9ca-134">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="af9ca-135">Esse parâmetro é gerado automaticamente se não for especificado.</span><span class="sxs-lookup"><span data-stu-id="af9ca-135">This parameter is generated automatically if it is not specified.</span></span>
<span data-ttu-id="af9ca-136">Esse parâmetro deve ter de 1 a 300 caracteres.</span><span class="sxs-lookup"><span data-stu-id="af9ca-136">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="af9ca-137">-Estado</span><span class="sxs-lookup"><span data-stu-id="af9ca-137">-State</span></span>
<span data-ttu-id="af9ca-138">Especifica o estado da assinatura.</span><span class="sxs-lookup"><span data-stu-id="af9ca-138">Specifies the subscription state.</span></span>
<span data-ttu-id="af9ca-139">O valor padrão é $Null.</span><span class="sxs-lookup"><span data-stu-id="af9ca-139">The default value is $Null.</span></span>

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

### <span data-ttu-id="af9ca-140">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="af9ca-140">-SubscriptionId</span></span>
<span data-ttu-id="af9ca-141">Especifica a ID da assinatura.</span><span class="sxs-lookup"><span data-stu-id="af9ca-141">Specifies the subscription ID.</span></span>
<span data-ttu-id="af9ca-142">Esse parâmetro é gerado se não especificado.</span><span class="sxs-lookup"><span data-stu-id="af9ca-142">This parameter is generated if not specified.</span></span>

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

### <span data-ttu-id="af9ca-143">-UserId</span><span class="sxs-lookup"><span data-stu-id="af9ca-143">-UserId</span></span>
<span data-ttu-id="af9ca-144">Especifica a ID do assinante.</span><span class="sxs-lookup"><span data-stu-id="af9ca-144">Specifies the subscriber ID.</span></span>

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

### <span data-ttu-id="af9ca-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af9ca-145">CommonParameters</span></span>
<span data-ttu-id="af9ca-146">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af9ca-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af9ca-147">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="af9ca-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af9ca-148">Entradas</span><span class="sxs-lookup"><span data-stu-id="af9ca-148">INPUTS</span></span>

### <span data-ttu-id="af9ca-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="af9ca-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="af9ca-150">System.String</span><span class="sxs-lookup"><span data-stu-id="af9ca-150">System.String</span></span>

### <span data-ttu-id="af9ca-151">System.Nullable'1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0,0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="af9ca-151">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="af9ca-152">Saídas</span><span class="sxs-lookup"><span data-stu-id="af9ca-152">OUTPUTS</span></span>

### <span data-ttu-id="af9ca-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="af9ca-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="af9ca-154">Notas</span><span class="sxs-lookup"><span data-stu-id="af9ca-154">NOTES</span></span>

## <span data-ttu-id="af9ca-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="af9ca-155">RELATED LINKS</span></span>

[<span data-ttu-id="af9ca-156">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="af9ca-156">Get-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="af9ca-157">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="af9ca-157">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)

[<span data-ttu-id="af9ca-158">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="af9ca-158">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)


