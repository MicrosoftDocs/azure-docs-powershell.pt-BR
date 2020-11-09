---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 223FBBA6-4405-4B7A-BA63-5F2434A2A50D
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementProduct.md
ms.openlocfilehash: 9bee67dd299163b8e660b0e17c4e3bc11da5b40e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94282277"
---
# <span data-ttu-id="cc70b-101">Set-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="cc70b-101">Set-AzApiManagementProduct</span></span>

## <span data-ttu-id="cc70b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cc70b-102">SYNOPSIS</span></span>
<span data-ttu-id="cc70b-103">Define os detalhes do produto de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="cc70b-103">Sets the API Management product details.</span></span>

## <span data-ttu-id="cc70b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cc70b-104">SYNTAX</span></span>

```
Set-AzApiManagementProduct -Context <PsApiManagementContext> -ProductId <String> [-Title <String>]
 [-Description <String>] [-LegalTerms <String>] [-SubscriptionRequired <Boolean>] [-ApprovalRequired <Boolean>]
 [-SubscriptionsLimit <Int32>] [-State <PsApiManagementProductState>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc70b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cc70b-105">DESCRIPTION</span></span>
<span data-ttu-id="cc70b-106">O cmdlet **set-AzApiManagementProduct** define os detalhes do produto de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="cc70b-106">The **Set-AzApiManagementProduct** cmdlet sets the API Management product details.</span></span>

## <span data-ttu-id="cc70b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cc70b-107">EXAMPLES</span></span>

### <span data-ttu-id="cc70b-108">Exemplo 1: atualizar os detalhes do produto</span><span class="sxs-lookup"><span data-stu-id="cc70b-108">Example 1: Update the product details</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementProduct -Context $apimContext -ProductId "0123456789" -Title "Starter" -Description "Starter Product" -LegalTerms "Free for all" -SubscriptionRequired $True -State "NotPublished"
```

<span data-ttu-id="cc70b-109">Esse comando atualiza os detalhes do produto de gerenciamento de API, requer uma assinatura e, em seguida, não publica.</span><span class="sxs-lookup"><span data-stu-id="cc70b-109">This command updates the API Management product details, requires a subscription, and then unpublishes.</span></span>

## <span data-ttu-id="cc70b-110">OS</span><span class="sxs-lookup"><span data-stu-id="cc70b-110">PARAMETERS</span></span>

### <span data-ttu-id="cc70b-111">-ApprovalRequired</span><span class="sxs-lookup"><span data-stu-id="cc70b-111">-ApprovalRequired</span></span>
<span data-ttu-id="cc70b-112">Indica se a assinatura do produto requer aprovação.</span><span class="sxs-lookup"><span data-stu-id="cc70b-112">Indicates whether the subscription to the product requires approval.</span></span>
<span data-ttu-id="cc70b-113">O valor padrão é **$false**.</span><span class="sxs-lookup"><span data-stu-id="cc70b-113">The default value is **$False**.</span></span>

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

### <span data-ttu-id="cc70b-114">-Contexto</span><span class="sxs-lookup"><span data-stu-id="cc70b-114">-Context</span></span>
<span data-ttu-id="cc70b-115">Especifica uma instância do objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="cc70b-115">Specifies an instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="cc70b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc70b-116">-DefaultProfile</span></span>
<span data-ttu-id="cc70b-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cc70b-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cc70b-118">-Descrição</span><span class="sxs-lookup"><span data-stu-id="cc70b-118">-Description</span></span>
<span data-ttu-id="cc70b-119">Especifica a descrição do produto.</span><span class="sxs-lookup"><span data-stu-id="cc70b-119">Specifies the product description.</span></span>

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

### <span data-ttu-id="cc70b-120">-LegalTerms</span><span class="sxs-lookup"><span data-stu-id="cc70b-120">-LegalTerms</span></span>
<span data-ttu-id="cc70b-121">Especifica os termos legais de uso do produto.</span><span class="sxs-lookup"><span data-stu-id="cc70b-121">Specifies the legal terms of use of the product.</span></span>

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

### <span data-ttu-id="cc70b-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cc70b-122">-PassThru</span></span>
<span data-ttu-id="cc70b-123">PassThru</span><span class="sxs-lookup"><span data-stu-id="cc70b-123">passthru</span></span>

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

### <span data-ttu-id="cc70b-124">-ProductId</span><span class="sxs-lookup"><span data-stu-id="cc70b-124">-ProductId</span></span>
<span data-ttu-id="cc70b-125">Especifica o identificador do produto existente.</span><span class="sxs-lookup"><span data-stu-id="cc70b-125">Specifies the identifier of the existing product.</span></span>

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

### <span data-ttu-id="cc70b-126">-Estado</span><span class="sxs-lookup"><span data-stu-id="cc70b-126">-State</span></span>
<span data-ttu-id="cc70b-127">Especifica o estado do produto.</span><span class="sxs-lookup"><span data-stu-id="cc70b-127">Specifies the product state.</span></span>
<span data-ttu-id="cc70b-128">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="cc70b-128">psdx_paramvalues</span></span>
- <span data-ttu-id="cc70b-129">Não publicado</span><span class="sxs-lookup"><span data-stu-id="cc70b-129">NotPublished</span></span>
- <span data-ttu-id="cc70b-130">Publish</span><span class="sxs-lookup"><span data-stu-id="cc70b-130">Published</span></span>

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

### <span data-ttu-id="cc70b-131">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="cc70b-131">-SubscriptionRequired</span></span>
<span data-ttu-id="cc70b-132">Indica se o produto exige uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="cc70b-132">Indicates whether the product requires a subscription.</span></span>
<span data-ttu-id="cc70b-133">O valor padrão para esse parâmetro é **$true**.</span><span class="sxs-lookup"><span data-stu-id="cc70b-133">The default value for this parameter is **$True**.</span></span>

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

### <span data-ttu-id="cc70b-134">-SubscriptionsLimit</span><span class="sxs-lookup"><span data-stu-id="cc70b-134">-SubscriptionsLimit</span></span>
<span data-ttu-id="cc70b-135">Especifica o número máximo de assinaturas simultâneas.</span><span class="sxs-lookup"><span data-stu-id="cc70b-135">Specifies the maximum number of simultaneous subscriptions.</span></span>
<span data-ttu-id="cc70b-136">O valor padrão para esse parâmetro é nenhum.</span><span class="sxs-lookup"><span data-stu-id="cc70b-136">The default value for this parameter is None.</span></span>

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

### <span data-ttu-id="cc70b-137">-Título</span><span class="sxs-lookup"><span data-stu-id="cc70b-137">-Title</span></span>
<span data-ttu-id="cc70b-138">Especifica o título do produto que este cmdlet define.</span><span class="sxs-lookup"><span data-stu-id="cc70b-138">Specifies the product title this cmdlet sets.</span></span>

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

### <span data-ttu-id="cc70b-139">-Confirme</span><span class="sxs-lookup"><span data-stu-id="cc70b-139">-Confirm</span></span>
<span data-ttu-id="cc70b-140">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cc70b-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc70b-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc70b-141">-WhatIf</span></span>
<span data-ttu-id="cc70b-142">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cc70b-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cc70b-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cc70b-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc70b-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc70b-144">CommonParameters</span></span>
<span data-ttu-id="cc70b-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc70b-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc70b-146">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cc70b-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc70b-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cc70b-147">INPUTS</span></span>

### <span data-ttu-id="cc70b-148">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="cc70b-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="cc70b-149">System. String</span><span class="sxs-lookup"><span data-stu-id="cc70b-149">System.String</span></span>

### <span data-ttu-id="cc70b-150">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="cc70b-150">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="cc70b-151">System. Nullable ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="cc70b-151">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="cc70b-152">System. Nullable ' 1 [[Microsoft. Azure. Commands. ApiManagement. Management. Models. PsApiManagementProductState, Microsoft. Azure. PowerShell. cmdlets. ApiManagement. immanagement, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="cc70b-152">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProductState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="cc70b-153">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="cc70b-153">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="cc70b-154">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cc70b-154">OUTPUTS</span></span>

### <span data-ttu-id="cc70b-155">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="cc70b-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="cc70b-156">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cc70b-156">NOTES</span></span>

## <span data-ttu-id="cc70b-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cc70b-157">RELATED LINKS</span></span>

[<span data-ttu-id="cc70b-158">Get-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="cc70b-158">Get-AzApiManagementProduct</span></span>](./Get-AzApiManagementProduct.md)

[<span data-ttu-id="cc70b-159">New-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="cc70b-159">New-AzApiManagementProduct</span></span>](./New-AzApiManagementProduct.md)

[<span data-ttu-id="cc70b-160">Remove-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="cc70b-160">Remove-AzApiManagementProduct</span></span>](./Remove-AzApiManagementProduct.md)


