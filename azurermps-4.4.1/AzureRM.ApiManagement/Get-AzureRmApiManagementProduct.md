---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: B64E9C13-97A6-4E8B-92DB-EFAF8A48C5B8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementProduct.md
ms.openlocfilehash: ab0aeb77bd5f28520e39548f539d07516cd17ac8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431249"
---
# <span data-ttu-id="f1db8-101">Get-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="f1db8-101">Get-AzureRmApiManagementProduct</span></span>

## <span data-ttu-id="f1db8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f1db8-102">SYNOPSIS</span></span>
<span data-ttu-id="f1db8-103">Obtém uma lista ou um produto específico.</span><span class="sxs-lookup"><span data-stu-id="f1db8-103">Gets a list or a particular product.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f1db8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f1db8-104">SYNTAX</span></span>

### <span data-ttu-id="f1db8-105">Obter todos os producst (padrão)</span><span class="sxs-lookup"><span data-stu-id="f1db8-105">Get all producst (Default)</span></span>
```
Get-AzureRmApiManagementProduct -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f1db8-106">Obter por ID</span><span class="sxs-lookup"><span data-stu-id="f1db8-106">Get by Id</span></span>
```
Get-AzureRmApiManagementProduct -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f1db8-107">Obter por título</span><span class="sxs-lookup"><span data-stu-id="f1db8-107">Get by Title</span></span>
```
Get-AzureRmApiManagementProduct -Context <PsApiManagementContext> [-Title <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f1db8-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f1db8-108">DESCRIPTION</span></span>
<span data-ttu-id="f1db8-109">O cmdlet **Get-AzureRmApiManagementProduct** Obtém uma lista ou um produto específico.</span><span class="sxs-lookup"><span data-stu-id="f1db8-109">The **Get-AzureRmApiManagementProduct** cmdlet gets a list or a particular product.</span></span>

## <span data-ttu-id="f1db8-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f1db8-110">EXAMPLES</span></span>

### <span data-ttu-id="f1db8-111">Exemplo 1: obter todos os produtos</span><span class="sxs-lookup"><span data-stu-id="f1db8-111">Example 1: Get all products</span></span>
```
PS C:\>Get-AzureRmApiManagementProduct -Context $APImContext
```

<span data-ttu-id="f1db8-112">Este comando obtém todos os produtos de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="f1db8-112">This command get all API Management products.</span></span>

### <span data-ttu-id="f1db8-113">Exemplo 2: obter um produto por ID</span><span class="sxs-lookup"><span data-stu-id="f1db8-113">Example 2: Get a product by ID</span></span>
```
PS C:\>Get-AzureRmApiManagementProduct -Context $APImContext -ProductId "0123456789"
```

<span data-ttu-id="f1db8-114">Este comando obtém um produto de gerenciamento de API por ID.</span><span class="sxs-lookup"><span data-stu-id="f1db8-114">This command get an API Management product by ID.</span></span>

## <span data-ttu-id="f1db8-115">OS</span><span class="sxs-lookup"><span data-stu-id="f1db8-115">PARAMETERS</span></span>

### <span data-ttu-id="f1db8-116">-Contexto</span><span class="sxs-lookup"><span data-stu-id="f1db8-116">-Context</span></span>
<span data-ttu-id="f1db8-117">Especifica uma instância de um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="f1db8-117">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="f1db8-118">-ProductId</span><span class="sxs-lookup"><span data-stu-id="f1db8-118">-ProductId</span></span>
<span data-ttu-id="f1db8-119">Especifica o identificador do produto a ser pesquisado.</span><span class="sxs-lookup"><span data-stu-id="f1db8-119">Specifies the identifier of the product to search for.</span></span>

```yaml
Type: System.String
Parameter Sets: Get by Id
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1db8-120">-Título</span><span class="sxs-lookup"><span data-stu-id="f1db8-120">-Title</span></span>
<span data-ttu-id="f1db8-121">Especifica o título do produto a ser procurado.</span><span class="sxs-lookup"><span data-stu-id="f1db8-121">Specifies the title of the product to look for.</span></span>
<span data-ttu-id="f1db8-122">Se especificado, o cmdlet tenta obter o produto por título.</span><span class="sxs-lookup"><span data-stu-id="f1db8-122">If specified, the cmdlet attempts to get the product by title.</span></span>

```yaml
Type: System.String
Parameter Sets: Get by Title
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1db8-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1db8-123">-DefaultProfile</span></span>
<span data-ttu-id="f1db8-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f1db8-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1db8-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1db8-125">CommonParameters</span></span>
<span data-ttu-id="f1db8-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1db8-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1db8-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1db8-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1db8-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f1db8-128">INPUTS</span></span>

## <span data-ttu-id="f1db8-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f1db8-129">OUTPUTS</span></span>

### <span data-ttu-id="f1db8-130">IList<Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementProduct></span><span class="sxs-lookup"><span data-stu-id="f1db8-130">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct></span></span>

## <span data-ttu-id="f1db8-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f1db8-131">NOTES</span></span>

## <span data-ttu-id="f1db8-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f1db8-132">RELATED LINKS</span></span>

[<span data-ttu-id="f1db8-133">New-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="f1db8-133">New-AzureRmApiManagementProduct</span></span>](./New-AzureRmApiManagementProduct.md)

[<span data-ttu-id="f1db8-134">Remove-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="f1db8-134">Remove-AzureRmApiManagementProduct</span></span>](./Remove-AzureRmApiManagementProduct.md)

[<span data-ttu-id="f1db8-135">Set-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="f1db8-135">Set-AzureRmApiManagementProduct</span></span>](./Set-AzureRmApiManagementProduct.md)


