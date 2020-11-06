---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B64E9C13-97A6-4E8B-92DB-EFAF8A48C5B8
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementProduct.md
ms.openlocfilehash: 9b2eb9f45f04b858e0773215ee1ed9fd98f20ff5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93595674"
---
# <span data-ttu-id="609b7-101">Get-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="609b7-101">Get-AzApiManagementProduct</span></span>

## <span data-ttu-id="609b7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="609b7-102">SYNOPSIS</span></span>
<span data-ttu-id="609b7-103">Obtém uma lista ou um produto específico.</span><span class="sxs-lookup"><span data-stu-id="609b7-103">Gets a list or a particular product.</span></span>

## <span data-ttu-id="609b7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="609b7-104">SYNTAX</span></span>

### <span data-ttu-id="609b7-105">GetAllProducts (padrão)</span><span class="sxs-lookup"><span data-stu-id="609b7-105">GetAllProducts (Default)</span></span>
```
Get-AzApiManagementProduct -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="609b7-106">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="609b7-106">GetByProductId</span></span>
```
Get-AzApiManagementProduct -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="609b7-107">GetByTitle</span><span class="sxs-lookup"><span data-stu-id="609b7-107">GetByTitle</span></span>
```
Get-AzApiManagementProduct -Context <PsApiManagementContext> [-Title <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="609b7-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="609b7-108">DESCRIPTION</span></span>
<span data-ttu-id="609b7-109">O cmdlet **Get-AzApiManagementProduct** Obtém uma lista ou um produto específico.</span><span class="sxs-lookup"><span data-stu-id="609b7-109">The **Get-AzApiManagementProduct** cmdlet gets a list or a particular product.</span></span>

## <span data-ttu-id="609b7-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="609b7-110">EXAMPLES</span></span>

### <span data-ttu-id="609b7-111">Exemplo 1: obter todos os produtos</span><span class="sxs-lookup"><span data-stu-id="609b7-111">Example 1: Get all products</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementProduct -Context $apimContext
```

<span data-ttu-id="609b7-112">Este comando obtém todos os produtos de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="609b7-112">This command get all API Management products.</span></span>

### <span data-ttu-id="609b7-113">Exemplo 2: obter um produto por ID</span><span class="sxs-lookup"><span data-stu-id="609b7-113">Example 2: Get a product by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementProduct -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="609b7-114">Este comando obtém um produto de gerenciamento de API por ID.</span><span class="sxs-lookup"><span data-stu-id="609b7-114">This command get an API Management product by ID.</span></span>

## <span data-ttu-id="609b7-115">OS</span><span class="sxs-lookup"><span data-stu-id="609b7-115">PARAMETERS</span></span>

### <span data-ttu-id="609b7-116">-Contexto</span><span class="sxs-lookup"><span data-stu-id="609b7-116">-Context</span></span>
<span data-ttu-id="609b7-117">Especifica uma instância de um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="609b7-117">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="609b7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="609b7-118">-DefaultProfile</span></span>
<span data-ttu-id="609b7-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="609b7-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="609b7-120">-ProductId</span><span class="sxs-lookup"><span data-stu-id="609b7-120">-ProductId</span></span>
<span data-ttu-id="609b7-121">Especifica o identificador do produto a ser pesquisado.</span><span class="sxs-lookup"><span data-stu-id="609b7-121">Specifies the identifier of the product to search for.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByProductId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="609b7-122">-Título</span><span class="sxs-lookup"><span data-stu-id="609b7-122">-Title</span></span>
<span data-ttu-id="609b7-123">Especifica o título do produto a ser procurado.</span><span class="sxs-lookup"><span data-stu-id="609b7-123">Specifies the title of the product to look for.</span></span>
<span data-ttu-id="609b7-124">Se especificado, o cmdlet tenta obter o produto por título.</span><span class="sxs-lookup"><span data-stu-id="609b7-124">If specified, the cmdlet attempts to get the product by title.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByTitle
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="609b7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="609b7-125">CommonParameters</span></span>
<span data-ttu-id="609b7-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="609b7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="609b7-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="609b7-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="609b7-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="609b7-128">INPUTS</span></span>

### <span data-ttu-id="609b7-129">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="609b7-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="609b7-130">System. String</span><span class="sxs-lookup"><span data-stu-id="609b7-130">System.String</span></span>

## <span data-ttu-id="609b7-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="609b7-131">OUTPUTS</span></span>

### <span data-ttu-id="609b7-132">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="609b7-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="609b7-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="609b7-133">NOTES</span></span>

## <span data-ttu-id="609b7-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="609b7-134">RELATED LINKS</span></span>

[<span data-ttu-id="609b7-135">New-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="609b7-135">New-AzApiManagementProduct</span></span>](./New-AzApiManagementProduct.md)

[<span data-ttu-id="609b7-136">Remove-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="609b7-136">Remove-AzApiManagementProduct</span></span>](./Remove-AzApiManagementProduct.md)

[<span data-ttu-id="609b7-137">Set-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="609b7-137">Set-AzApiManagementProduct</span></span>](./Set-AzApiManagementProduct.md)


