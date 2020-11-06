---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 223FBBA6-4405-4B7A-BA63-5F2434A2A50D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementProduct.md
ms.openlocfilehash: dac6e48faba1590897161ab59fed05f1f0b331df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431208"
---
# <span data-ttu-id="a7399-101">Set-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="a7399-101">Set-AzureRmApiManagementProduct</span></span>

## <span data-ttu-id="a7399-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a7399-102">SYNOPSIS</span></span>
<span data-ttu-id="a7399-103">Define os detalhes do produto de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="a7399-103">Sets the API Management product details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a7399-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a7399-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementProduct -Context <PsApiManagementContext> -ProductId <String> [-Title <String>]
 [-Description <String>] [-LegalTerms <String>] [-SubscriptionRequired <Boolean>] [-ApprovalRequired <Boolean>]
 [-SubscriptionsLimit <Int32>] [-State <PsApiManagementProductState>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a7399-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a7399-105">DESCRIPTION</span></span>
<span data-ttu-id="a7399-106">O cmdlet **set-AzureRmApiManagementProduct** define os detalhes do produto de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="a7399-106">The **Set-AzureRmApiManagementProduct** cmdlet sets the API Management product details.</span></span>

## <span data-ttu-id="a7399-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a7399-107">EXAMPLES</span></span>

### <span data-ttu-id="a7399-108">Exemplo 1: atualizar os detalhes do produto</span><span class="sxs-lookup"><span data-stu-id="a7399-108">Example 1: Update the product details</span></span>
```
PS C:\>Set-AzureRmApiManagementProduct -Context $APImContext -ProductId "0123456789" -Title "Starter" -Description "Starter Product" -LegalTerms "Free for all" -SubscriptionRequired $True -State "NotPublished"
```

<span data-ttu-id="a7399-109">Esse comando atualiza os detalhes do produto de gerenciamento de API, requer uma assinatura e, em seguida, não publica.</span><span class="sxs-lookup"><span data-stu-id="a7399-109">This command updates the API Management product details, requires a subscription, and then unpublishes.</span></span>

## <span data-ttu-id="a7399-110">OS</span><span class="sxs-lookup"><span data-stu-id="a7399-110">PARAMETERS</span></span>

### <span data-ttu-id="a7399-111">-ApprovalRequired</span><span class="sxs-lookup"><span data-stu-id="a7399-111">-ApprovalRequired</span></span>
<span data-ttu-id="a7399-112">Indica se a assinatura do produto requer aprovação.</span><span class="sxs-lookup"><span data-stu-id="a7399-112">Indicates whether the subscription to the product requires approval.</span></span>
<span data-ttu-id="a7399-113">O valor padrão é **$false**.</span><span class="sxs-lookup"><span data-stu-id="a7399-113">The default value is **$False**.</span></span>

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

### <span data-ttu-id="a7399-114">-Contexto</span><span class="sxs-lookup"><span data-stu-id="a7399-114">-Context</span></span>
<span data-ttu-id="a7399-115">Especifica uma instância do objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="a7399-115">Specifies an instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="a7399-116">-Descrição</span><span class="sxs-lookup"><span data-stu-id="a7399-116">-Description</span></span>
<span data-ttu-id="a7399-117">Especifica a descrição do produto.</span><span class="sxs-lookup"><span data-stu-id="a7399-117">Specifies the product description.</span></span>

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

### <span data-ttu-id="a7399-118">-LegalTerms</span><span class="sxs-lookup"><span data-stu-id="a7399-118">-LegalTerms</span></span>
<span data-ttu-id="a7399-119">Especifica os termos legais de uso do produto.</span><span class="sxs-lookup"><span data-stu-id="a7399-119">Specifies the legal terms of use of the product.</span></span>

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

### <span data-ttu-id="a7399-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a7399-120">-PassThru</span></span>
<span data-ttu-id="a7399-121">PassThru</span><span class="sxs-lookup"><span data-stu-id="a7399-121">passthru</span></span>

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

### <span data-ttu-id="a7399-122">-ProductId</span><span class="sxs-lookup"><span data-stu-id="a7399-122">-ProductId</span></span>
<span data-ttu-id="a7399-123">Especifica o identificador do produto existente.</span><span class="sxs-lookup"><span data-stu-id="a7399-123">Specifies the identifier of the existing product.</span></span>

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

### <span data-ttu-id="a7399-124">-Estado</span><span class="sxs-lookup"><span data-stu-id="a7399-124">-State</span></span>
<span data-ttu-id="a7399-125">Especifica o estado do produto.</span><span class="sxs-lookup"><span data-stu-id="a7399-125">Specifies the product state.</span></span>
<span data-ttu-id="a7399-126">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="a7399-126">psdx_paramvalues</span></span>

- <span data-ttu-id="a7399-127">Não publicado</span><span class="sxs-lookup"><span data-stu-id="a7399-127">NotPublished</span></span>
- <span data-ttu-id="a7399-128">Publish</span><span class="sxs-lookup"><span data-stu-id="a7399-128">Published</span></span>

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

### <span data-ttu-id="a7399-129">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="a7399-129">-SubscriptionRequired</span></span>
<span data-ttu-id="a7399-130">Indica se o produto exige uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="a7399-130">Indicates whether the product requires a subscription.</span></span>
<span data-ttu-id="a7399-131">O valor padrão para esse parâmetro é **$true**.</span><span class="sxs-lookup"><span data-stu-id="a7399-131">The default value for this parameter is **$True**.</span></span>

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

### <span data-ttu-id="a7399-132">-SubscriptionsLimit</span><span class="sxs-lookup"><span data-stu-id="a7399-132">-SubscriptionsLimit</span></span>
<span data-ttu-id="a7399-133">Especifica o número máximo de assinaturas simultâneas.</span><span class="sxs-lookup"><span data-stu-id="a7399-133">Specifies the maximum number of simultaneous subscriptions.</span></span>
<span data-ttu-id="a7399-134">O valor padrão para esse parâmetro é 1.</span><span class="sxs-lookup"><span data-stu-id="a7399-134">The default value for this parameter is 1.</span></span>

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

### <span data-ttu-id="a7399-135">-Título</span><span class="sxs-lookup"><span data-stu-id="a7399-135">-Title</span></span>
<span data-ttu-id="a7399-136">Especifica o título do produto que este cmdlet define.</span><span class="sxs-lookup"><span data-stu-id="a7399-136">Specifies the product title this cmdlet sets.</span></span>

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

### <span data-ttu-id="a7399-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7399-137">-DefaultProfile</span></span>
<span data-ttu-id="a7399-138">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a7399-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7399-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7399-139">CommonParameters</span></span>
<span data-ttu-id="a7399-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7399-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7399-141">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7399-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7399-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a7399-142">INPUTS</span></span>

## <span data-ttu-id="a7399-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a7399-143">OUTPUTS</span></span>

### <span data-ttu-id="a7399-144">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="a7399-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="a7399-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a7399-145">NOTES</span></span>

## <span data-ttu-id="a7399-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a7399-146">RELATED LINKS</span></span>

[<span data-ttu-id="a7399-147">Get-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="a7399-147">Get-AzureRmApiManagementProduct</span></span>](./Get-AzureRmApiManagementProduct.md)

[<span data-ttu-id="a7399-148">New-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="a7399-148">New-AzureRmApiManagementProduct</span></span>](./New-AzureRmApiManagementProduct.md)

[<span data-ttu-id="a7399-149">Remove-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="a7399-149">Remove-AzureRmApiManagementProduct</span></span>](./Remove-AzureRmApiManagementProduct.md)


