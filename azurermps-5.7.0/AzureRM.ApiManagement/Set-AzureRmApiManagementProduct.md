---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 223FBBA6-4405-4B7A-BA63-5F2434A2A50D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementProduct.md
ms.openlocfilehash: b050b55c978313cf038e8a27d5be0f7ad722905b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610675"
---
# <span data-ttu-id="c6a7b-101">Set-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="c6a7b-101">Set-AzureRmApiManagementProduct</span></span>

## <span data-ttu-id="c6a7b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c6a7b-102">SYNOPSIS</span></span>
<span data-ttu-id="c6a7b-103">Define os detalhes do produto de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="c6a7b-103">Sets the API Management product details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c6a7b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c6a7b-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementProduct -Context <PsApiManagementContext> -ProductId <String> [-Title <String>]
 [-Description <String>] [-LegalTerms <String>] [-SubscriptionRequired <Boolean>] [-ApprovalRequired <Boolean>]
 [-SubscriptionsLimit <Int32>] [-State <PsApiManagementProductState>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c6a7b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c6a7b-105">DESCRIPTION</span></span>
<span data-ttu-id="c6a7b-106">O cmdlet **set-AzureRmApiManagementProduct** define os detalhes do produto de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="c6a7b-106">The **Set-AzureRmApiManagementProduct** cmdlet sets the API Management product details.</span></span>

## <span data-ttu-id="c6a7b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c6a7b-107">EXAMPLES</span></span>

### <span data-ttu-id="c6a7b-108">Exemplo 1: atualizar os detalhes do produto</span><span class="sxs-lookup"><span data-stu-id="c6a7b-108">Example 1: Update the product details</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementProduct -Context $apimContext -ProductId "0123456789" -Title "Starter" -Description "Starter Product" -LegalTerms "Free for all" -SubscriptionRequired $True -State "NotPublished"
```

<span data-ttu-id="c6a7b-109">Esse comando atualiza os detalhes do produto de gerenciamento de API, requer uma assinatura e, em seguida, não publica.</span><span class="sxs-lookup"><span data-stu-id="c6a7b-109">This command updates the API Management product details, requires a subscription, and then unpublishes.</span></span>

## <span data-ttu-id="c6a7b-110">OS</span><span class="sxs-lookup"><span data-stu-id="c6a7b-110">PARAMETERS</span></span>

### <span data-ttu-id="c6a7b-111">-ApprovalRequired</span><span class="sxs-lookup"><span data-stu-id="c6a7b-111">-ApprovalRequired</span></span>
<span data-ttu-id="c6a7b-112">Indica se a assinatura do produto requer aprovação.</span><span class="sxs-lookup"><span data-stu-id="c6a7b-112">Indicates whether the subscription to the product requires approval.</span></span>
<span data-ttu-id="c6a7b-113">O valor padrão é **$false**.</span><span class="sxs-lookup"><span data-stu-id="c6a7b-113">The default value is **$False**.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6a7b-114">-Contexto</span><span class="sxs-lookup"><span data-stu-id="c6a7b-114">-Context</span></span>
<span data-ttu-id="c6a7b-115">Especifica uma instância do objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="c6a7b-115">Specifies an instance of the **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6a7b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6a7b-116">-DefaultProfile</span></span>
<span data-ttu-id="c6a7b-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c6a7b-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6a7b-118">-Descrição</span><span class="sxs-lookup"><span data-stu-id="c6a7b-118">-Description</span></span>
<span data-ttu-id="c6a7b-119">Especifica a descrição do produto.</span><span class="sxs-lookup"><span data-stu-id="c6a7b-119">Specifies the product description.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6a7b-120">-LegalTerms</span><span class="sxs-lookup"><span data-stu-id="c6a7b-120">-LegalTerms</span></span>
<span data-ttu-id="c6a7b-121">Especifica os termos legais de uso do produto.</span><span class="sxs-lookup"><span data-stu-id="c6a7b-121">Specifies the legal terms of use of the product.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6a7b-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c6a7b-122">-PassThru</span></span>
<span data-ttu-id="c6a7b-123">PassThru</span><span class="sxs-lookup"><span data-stu-id="c6a7b-123">passthru</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6a7b-124">-ProductId</span><span class="sxs-lookup"><span data-stu-id="c6a7b-124">-ProductId</span></span>
<span data-ttu-id="c6a7b-125">Especifica o identificador do produto existente.</span><span class="sxs-lookup"><span data-stu-id="c6a7b-125">Specifies the identifier of the existing product.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6a7b-126">-Estado</span><span class="sxs-lookup"><span data-stu-id="c6a7b-126">-State</span></span>
<span data-ttu-id="c6a7b-127">Especifica o estado do produto.</span><span class="sxs-lookup"><span data-stu-id="c6a7b-127">Specifies the product state.</span></span>
<span data-ttu-id="c6a7b-128">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="c6a7b-128">psdx_paramvalues</span></span>

- <span data-ttu-id="c6a7b-129">Não publicado</span><span class="sxs-lookup"><span data-stu-id="c6a7b-129">NotPublished</span></span>
- <span data-ttu-id="c6a7b-130">Publish</span><span class="sxs-lookup"><span data-stu-id="c6a7b-130">Published</span></span>

```yaml
Type: PsApiManagementProductState
Parameter Sets: (All)
Aliases: 
Accepted values: NotPublished, Published

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6a7b-131">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="c6a7b-131">-SubscriptionRequired</span></span>
<span data-ttu-id="c6a7b-132">Indica se o produto exige uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="c6a7b-132">Indicates whether the product requires a subscription.</span></span>
<span data-ttu-id="c6a7b-133">O valor padrão para esse parâmetro é **$true**.</span><span class="sxs-lookup"><span data-stu-id="c6a7b-133">The default value for this parameter is **$True**.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6a7b-134">-SubscriptionsLimit</span><span class="sxs-lookup"><span data-stu-id="c6a7b-134">-SubscriptionsLimit</span></span>
<span data-ttu-id="c6a7b-135">Especifica o número máximo de assinaturas simultâneas.</span><span class="sxs-lookup"><span data-stu-id="c6a7b-135">Specifies the maximum number of simultaneous subscriptions.</span></span>
<span data-ttu-id="c6a7b-136">O valor padrão para esse parâmetro é 1.</span><span class="sxs-lookup"><span data-stu-id="c6a7b-136">The default value for this parameter is 1.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6a7b-137">-Título</span><span class="sxs-lookup"><span data-stu-id="c6a7b-137">-Title</span></span>
<span data-ttu-id="c6a7b-138">Especifica o título do produto que este cmdlet define.</span><span class="sxs-lookup"><span data-stu-id="c6a7b-138">Specifies the product title this cmdlet sets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6a7b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6a7b-139">CommonParameters</span></span>
<span data-ttu-id="c6a7b-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6a7b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6a7b-141">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6a7b-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6a7b-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c6a7b-142">INPUTS</span></span>

### <span data-ttu-id="c6a7b-143">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="c6a7b-143">None</span></span>
<span data-ttu-id="c6a7b-144">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="c6a7b-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c6a7b-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c6a7b-145">OUTPUTS</span></span>

### <span data-ttu-id="c6a7b-146">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="c6a7b-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="c6a7b-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c6a7b-147">NOTES</span></span>

## <span data-ttu-id="c6a7b-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c6a7b-148">RELATED LINKS</span></span>

[<span data-ttu-id="c6a7b-149">Get-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="c6a7b-149">Get-AzureRmApiManagementProduct</span></span>](./Get-AzureRmApiManagementProduct.md)

[<span data-ttu-id="c6a7b-150">New-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="c6a7b-150">New-AzureRmApiManagementProduct</span></span>](./New-AzureRmApiManagementProduct.md)

[<span data-ttu-id="c6a7b-151">Remove-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="c6a7b-151">Remove-AzureRmApiManagementProduct</span></span>](./Remove-AzureRmApiManagementProduct.md)


