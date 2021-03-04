---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 223FBBA6-4405-4B7A-BA63-5F2434A2A50D
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/set-azapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementProduct.md
ms.openlocfilehash: e827fcf43c151f0812d96456de430f57686d4562
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886365"
---
# <span data-ttu-id="1cb1f-101">Set-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="1cb1f-101">Set-AzApiManagementProduct</span></span>

## <span data-ttu-id="1cb1f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1cb1f-102">SYNOPSIS</span></span>
<span data-ttu-id="1cb1f-103">Define os detalhes do produto de Gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="1cb1f-103">Sets the API Management product details.</span></span>

## <span data-ttu-id="1cb1f-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="1cb1f-104">SYNTAX</span></span>

```
Set-AzApiManagementProduct -Context <PsApiManagementContext> -ProductId <String> [-Title <String>]
 [-Description <String>] [-LegalTerms <String>] [-SubscriptionRequired <Boolean>] [-ApprovalRequired <Boolean>]
 [-SubscriptionsLimit <Int32>] [-State <PsApiManagementProductState>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1cb1f-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="1cb1f-105">DESCRIPTION</span></span>
<span data-ttu-id="1cb1f-106">O cmdlet **Set-AzApiManagementProduct** define os detalhes do produto de Gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="1cb1f-106">The **Set-AzApiManagementProduct** cmdlet sets the API Management product details.</span></span>

## <span data-ttu-id="1cb1f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1cb1f-107">EXAMPLES</span></span>

### <span data-ttu-id="1cb1f-108">Exemplo 1: atualizar os detalhes do produto</span><span class="sxs-lookup"><span data-stu-id="1cb1f-108">Example 1: Update the product details</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementProduct -Context $apimContext -ProductId "0123456789" -Title "Starter" -Description "Starter Product" -LegalTerms "Free for all" -SubscriptionRequired $True -State "NotPublished"
```

<span data-ttu-id="1cb1f-109">Este comando atualiza os detalhes do produto de Gerenciamento de API, exige uma assinatura e, em seguida, não publica.</span><span class="sxs-lookup"><span data-stu-id="1cb1f-109">This command updates the API Management product details, requires a subscription, and then unpublishes.</span></span>

## <span data-ttu-id="1cb1f-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="1cb1f-110">PARAMETERS</span></span>

### <span data-ttu-id="1cb1f-111">-ApprovalRequired</span><span class="sxs-lookup"><span data-stu-id="1cb1f-111">-ApprovalRequired</span></span>
<span data-ttu-id="1cb1f-112">Indica se a assinatura do produto requer aprovação.</span><span class="sxs-lookup"><span data-stu-id="1cb1f-112">Indicates whether the subscription to the product requires approval.</span></span>
<span data-ttu-id="1cb1f-113">O valor padrão é **$False**.</span><span class="sxs-lookup"><span data-stu-id="1cb1f-113">The default value is **$False**.</span></span>

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

### <span data-ttu-id="1cb1f-114">-Context</span><span class="sxs-lookup"><span data-stu-id="1cb1f-114">-Context</span></span>
<span data-ttu-id="1cb1f-115">Especifica uma instância do **objeto PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="1cb1f-115">Specifies an instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="1cb1f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cb1f-116">-DefaultProfile</span></span>
<span data-ttu-id="1cb1f-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="1cb1f-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1cb1f-118">-Description</span><span class="sxs-lookup"><span data-stu-id="1cb1f-118">-Description</span></span>
<span data-ttu-id="1cb1f-119">Especifica a descrição do produto.</span><span class="sxs-lookup"><span data-stu-id="1cb1f-119">Specifies the product description.</span></span>

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

### <span data-ttu-id="1cb1f-120">-LegalTerms</span><span class="sxs-lookup"><span data-stu-id="1cb1f-120">-LegalTerms</span></span>
<span data-ttu-id="1cb1f-121">Especifica os termos legais de uso do produto.</span><span class="sxs-lookup"><span data-stu-id="1cb1f-121">Specifies the legal terms of use of the product.</span></span>

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

### <span data-ttu-id="1cb1f-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1cb1f-122">-PassThru</span></span>
<span data-ttu-id="1cb1f-123">passthru</span><span class="sxs-lookup"><span data-stu-id="1cb1f-123">passthru</span></span>

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

### <span data-ttu-id="1cb1f-124">-ProductId</span><span class="sxs-lookup"><span data-stu-id="1cb1f-124">-ProductId</span></span>
<span data-ttu-id="1cb1f-125">Especifica o identificador do produto existente.</span><span class="sxs-lookup"><span data-stu-id="1cb1f-125">Specifies the identifier of the existing product.</span></span>

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

### <span data-ttu-id="1cb1f-126">-State</span><span class="sxs-lookup"><span data-stu-id="1cb1f-126">-State</span></span>
<span data-ttu-id="1cb1f-127">Especifica o estado do produto.</span><span class="sxs-lookup"><span data-stu-id="1cb1f-127">Specifies the product state.</span></span>
<span data-ttu-id="1cb1f-128">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="1cb1f-128">psdx_paramvalues</span></span>
- <span data-ttu-id="1cb1f-129">NotPublished</span><span class="sxs-lookup"><span data-stu-id="1cb1f-129">NotPublished</span></span>
- <span data-ttu-id="1cb1f-130">Publicado</span><span class="sxs-lookup"><span data-stu-id="1cb1f-130">Published</span></span>

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

### <span data-ttu-id="1cb1f-131">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="1cb1f-131">-SubscriptionRequired</span></span>
<span data-ttu-id="1cb1f-132">Indica se o produto requer uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="1cb1f-132">Indicates whether the product requires a subscription.</span></span>
<span data-ttu-id="1cb1f-133">O valor padrão para esse parâmetro é **$True**.</span><span class="sxs-lookup"><span data-stu-id="1cb1f-133">The default value for this parameter is **$True**.</span></span>

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

### <span data-ttu-id="1cb1f-134">-SubscriptionsLimit</span><span class="sxs-lookup"><span data-stu-id="1cb1f-134">-SubscriptionsLimit</span></span>
<span data-ttu-id="1cb1f-135">Especifica o número máximo de assinaturas simultâneas.</span><span class="sxs-lookup"><span data-stu-id="1cb1f-135">Specifies the maximum number of simultaneous subscriptions.</span></span>
<span data-ttu-id="1cb1f-136">O valor padrão para esse parâmetro é None.</span><span class="sxs-lookup"><span data-stu-id="1cb1f-136">The default value for this parameter is None.</span></span>

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

### <span data-ttu-id="1cb1f-137">-Title</span><span class="sxs-lookup"><span data-stu-id="1cb1f-137">-Title</span></span>
<span data-ttu-id="1cb1f-138">Especifica o título do produto que este cmdlet define.</span><span class="sxs-lookup"><span data-stu-id="1cb1f-138">Specifies the product title this cmdlet sets.</span></span>

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

### <span data-ttu-id="1cb1f-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1cb1f-139">-Confirm</span></span>
<span data-ttu-id="1cb1f-140">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1cb1f-140">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cb1f-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1cb1f-141">-WhatIf</span></span>
<span data-ttu-id="1cb1f-142">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1cb1f-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1cb1f-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1cb1f-143">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cb1f-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cb1f-144">CommonParameters</span></span>
<span data-ttu-id="1cb1f-145">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1cb1f-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cb1f-146">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1cb1f-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cb1f-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1cb1f-147">INPUTS</span></span>

### <span data-ttu-id="1cb1f-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="1cb1f-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="1cb1f-149">System.String</span><span class="sxs-lookup"><span data-stu-id="1cb1f-149">System.String</span></span>

### <span data-ttu-id="1cb1f-150">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="1cb1f-150">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="1cb1f-151">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="1cb1f-151">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="1cb1f-152">System.Nullable'1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProductState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="1cb1f-152">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProductState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="1cb1f-153">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1cb1f-153">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="1cb1f-154">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="1cb1f-154">OUTPUTS</span></span>

### <span data-ttu-id="1cb1f-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="1cb1f-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="1cb1f-156">NOTES</span><span class="sxs-lookup"><span data-stu-id="1cb1f-156">NOTES</span></span>

## <span data-ttu-id="1cb1f-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1cb1f-157">RELATED LINKS</span></span>

[<span data-ttu-id="1cb1f-158">Get-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="1cb1f-158">Get-AzApiManagementProduct</span></span>](./Get-AzApiManagementProduct.md)

[<span data-ttu-id="1cb1f-159">New-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="1cb1f-159">New-AzApiManagementProduct</span></span>](./New-AzApiManagementProduct.md)

[<span data-ttu-id="1cb1f-160">Remove-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="1cb1f-160">Remove-AzApiManagementProduct</span></span>](./Remove-AzApiManagementProduct.md)


