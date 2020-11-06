---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: B64E9C13-97A6-4E8B-92DB-EFAF8A48C5B8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementProduct.md
ms.openlocfilehash: a4bbc330b5cd4d7eaeec1d2e68252ceb5dd261f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429926"
---
# <span data-ttu-id="a174c-101">Get-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="a174c-101">Get-AzureRmApiManagementProduct</span></span>

## <span data-ttu-id="a174c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a174c-102">SYNOPSIS</span></span>
<span data-ttu-id="a174c-103">Obtém uma lista ou um produto específico.</span><span class="sxs-lookup"><span data-stu-id="a174c-103">Gets a list or a particular product.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a174c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a174c-104">SYNTAX</span></span>

### <span data-ttu-id="a174c-105">GetAllProducts (padrão)</span><span class="sxs-lookup"><span data-stu-id="a174c-105">GetAllProducts (Default)</span></span>
```
Get-AzureRmApiManagementProduct -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a174c-106">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="a174c-106">GetByProductId</span></span>
```
Get-AzureRmApiManagementProduct -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a174c-107">GetByTitle</span><span class="sxs-lookup"><span data-stu-id="a174c-107">GetByTitle</span></span>
```
Get-AzureRmApiManagementProduct -Context <PsApiManagementContext> [-Title <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a174c-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a174c-108">DESCRIPTION</span></span>
<span data-ttu-id="a174c-109">O cmdlet **Get-AzureRmApiManagementProduct** Obtém uma lista ou um produto específico.</span><span class="sxs-lookup"><span data-stu-id="a174c-109">The **Get-AzureRmApiManagementProduct** cmdlet gets a list or a particular product.</span></span>

## <span data-ttu-id="a174c-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a174c-110">EXAMPLES</span></span>

### <span data-ttu-id="a174c-111">Exemplo 1: obter todos os produtos</span><span class="sxs-lookup"><span data-stu-id="a174c-111">Example 1: Get all products</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementProduct -Context $apimContext
```

<span data-ttu-id="a174c-112">Este comando obtém todos os produtos de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="a174c-112">This command get all API Management products.</span></span>

### <span data-ttu-id="a174c-113">Exemplo 2: obter um produto por ID</span><span class="sxs-lookup"><span data-stu-id="a174c-113">Example 2: Get a product by ID</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementProduct -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="a174c-114">Este comando obtém um produto de gerenciamento de API por ID.</span><span class="sxs-lookup"><span data-stu-id="a174c-114">This command get an API Management product by ID.</span></span>

## <span data-ttu-id="a174c-115">OS</span><span class="sxs-lookup"><span data-stu-id="a174c-115">PARAMETERS</span></span>

### <span data-ttu-id="a174c-116">-Contexto</span><span class="sxs-lookup"><span data-stu-id="a174c-116">-Context</span></span>
<span data-ttu-id="a174c-117">Especifica uma instância de um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="a174c-117">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="a174c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a174c-118">-DefaultProfile</span></span>
<span data-ttu-id="a174c-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a174c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="a174c-120">-ProductId</span><span class="sxs-lookup"><span data-stu-id="a174c-120">-ProductId</span></span>
<span data-ttu-id="a174c-121">Especifica o identificador do produto a ser pesquisado.</span><span class="sxs-lookup"><span data-stu-id="a174c-121">Specifies the identifier of the product to search for.</span></span>

```yaml
Type: String
Parameter Sets: GetByProductId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a174c-122">-Título</span><span class="sxs-lookup"><span data-stu-id="a174c-122">-Title</span></span>
<span data-ttu-id="a174c-123">Especifica o título do produto a ser procurado.</span><span class="sxs-lookup"><span data-stu-id="a174c-123">Specifies the title of the product to look for.</span></span>
<span data-ttu-id="a174c-124">Se especificado, o cmdlet tenta obter o produto por título.</span><span class="sxs-lookup"><span data-stu-id="a174c-124">If specified, the cmdlet attempts to get the product by title.</span></span>

```yaml
Type: String
Parameter Sets: GetByTitle
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a174c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a174c-125">CommonParameters</span></span>
<span data-ttu-id="a174c-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a174c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a174c-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a174c-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a174c-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a174c-128">INPUTS</span></span>

### <span data-ttu-id="a174c-129">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="a174c-129">None</span></span>
<span data-ttu-id="a174c-130">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="a174c-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a174c-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a174c-131">OUTPUTS</span></span>

### <span data-ttu-id="a174c-132">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="a174c-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>
<span data-ttu-id="a174c-133">Os detalhes do produto no serviço de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="a174c-133">The details of the Product in API Management service.</span></span>

### <span data-ttu-id="a174c-134">IList<Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementProduct></span><span class="sxs-lookup"><span data-stu-id="a174c-134">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct></span></span>
<span data-ttu-id="a174c-135">A lista de produtos no serviço de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="a174c-135">The list of Product in API Management service.</span></span>

## <span data-ttu-id="a174c-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a174c-136">NOTES</span></span>

## <span data-ttu-id="a174c-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a174c-137">RELATED LINKS</span></span>

[<span data-ttu-id="a174c-138">New-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="a174c-138">New-AzureRmApiManagementProduct</span></span>](./New-AzureRmApiManagementProduct.md)

[<span data-ttu-id="a174c-139">Remove-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="a174c-139">Remove-AzureRmApiManagementProduct</span></span>](./Remove-AzureRmApiManagementProduct.md)

[<span data-ttu-id="a174c-140">Set-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="a174c-140">Set-AzureRmApiManagementProduct</span></span>](./Set-AzureRmApiManagementProduct.md)


