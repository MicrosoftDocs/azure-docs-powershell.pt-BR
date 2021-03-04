---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B64E9C13-97A6-4E8B-92DB-EFAF8A48C5B8
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementProduct.md
ms.openlocfilehash: 589338afde60e069646cb677205da11e322ba7da
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893260"
---
# <span data-ttu-id="470b0-101">Get-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="470b0-101">Get-AzApiManagementProduct</span></span>

## <span data-ttu-id="470b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="470b0-102">SYNOPSIS</span></span>
<span data-ttu-id="470b0-103">Obtém uma lista ou um produto específico.</span><span class="sxs-lookup"><span data-stu-id="470b0-103">Gets a list or a particular product.</span></span>

## <span data-ttu-id="470b0-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="470b0-104">SYNTAX</span></span>

### <span data-ttu-id="470b0-105">GetAllProducts (Padrão)</span><span class="sxs-lookup"><span data-stu-id="470b0-105">GetAllProducts (Default)</span></span>
```
Get-AzApiManagementProduct -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="470b0-106">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="470b0-106">GetByProductId</span></span>
```
Get-AzApiManagementProduct -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="470b0-107">GetByTitle</span><span class="sxs-lookup"><span data-stu-id="470b0-107">GetByTitle</span></span>
```
Get-AzApiManagementProduct -Context <PsApiManagementContext> [-Title <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="470b0-108">GetByApiId</span><span class="sxs-lookup"><span data-stu-id="470b0-108">GetByApiId</span></span>
```
Get-AzApiManagementProduct -Context <PsApiManagementContext> -ApiId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="470b0-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="470b0-109">DESCRIPTION</span></span>
<span data-ttu-id="470b0-110">O cmdlet **Get-AzApiManagementProduct** obtém uma lista ou um produto específico.</span><span class="sxs-lookup"><span data-stu-id="470b0-110">The **Get-AzApiManagementProduct** cmdlet gets a list or a particular product.</span></span>

## <span data-ttu-id="470b0-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="470b0-111">EXAMPLES</span></span>

### <span data-ttu-id="470b0-112">Exemplo 1: Obter todos os produtos</span><span class="sxs-lookup"><span data-stu-id="470b0-112">Example 1: Get all products</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementProduct -Context $apimContext
```

<span data-ttu-id="470b0-113">Este comando obterá todos os produtos de Gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="470b0-113">This command get all API Management products.</span></span>

### <span data-ttu-id="470b0-114">Exemplo 2: Obter um produto por ID</span><span class="sxs-lookup"><span data-stu-id="470b0-114">Example 2: Get a product by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementProduct -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="470b0-115">Este comando obter um produto de Gerenciamento de API por ID.</span><span class="sxs-lookup"><span data-stu-id="470b0-115">This command get an API Management product by ID.</span></span>

## <span data-ttu-id="470b0-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="470b0-116">PARAMETERS</span></span>

### <span data-ttu-id="470b0-117">-ApiId</span><span class="sxs-lookup"><span data-stu-id="470b0-117">-ApiId</span></span>
<span data-ttu-id="470b0-118">ApiId da Api para encontrar os produtos correlacionados.</span><span class="sxs-lookup"><span data-stu-id="470b0-118">ApiId of the Api to find the correlated products.</span></span> <span data-ttu-id="470b0-119">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="470b0-119">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByApiId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="470b0-120">-Context</span><span class="sxs-lookup"><span data-stu-id="470b0-120">-Context</span></span>
<span data-ttu-id="470b0-121">Especifica uma instância de um **objeto PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="470b0-121">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="470b0-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="470b0-122">-DefaultProfile</span></span>
<span data-ttu-id="470b0-123">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="470b0-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="470b0-124">-ProductId</span><span class="sxs-lookup"><span data-stu-id="470b0-124">-ProductId</span></span>
<span data-ttu-id="470b0-125">Especifica o identificador do produto a ser pesquisado.</span><span class="sxs-lookup"><span data-stu-id="470b0-125">Specifies the identifier of the product to search for.</span></span>

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

### <span data-ttu-id="470b0-126">-Title</span><span class="sxs-lookup"><span data-stu-id="470b0-126">-Title</span></span>
<span data-ttu-id="470b0-127">Especifica o título do produto a ser buscado.</span><span class="sxs-lookup"><span data-stu-id="470b0-127">Specifies the title of the product to look for.</span></span>
<span data-ttu-id="470b0-128">Se especificado, o cmdlet tenta obter o produto por título.</span><span class="sxs-lookup"><span data-stu-id="470b0-128">If specified, the cmdlet attempts to get the product by title.</span></span>

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

### <span data-ttu-id="470b0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="470b0-129">CommonParameters</span></span>
<span data-ttu-id="470b0-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="470b0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="470b0-131">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="470b0-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="470b0-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="470b0-132">INPUTS</span></span>

### <span data-ttu-id="470b0-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="470b0-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="470b0-134">System.String</span><span class="sxs-lookup"><span data-stu-id="470b0-134">System.String</span></span>

## <span data-ttu-id="470b0-135">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="470b0-135">OUTPUTS</span></span>

### <span data-ttu-id="470b0-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="470b0-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="470b0-137">NOTES</span><span class="sxs-lookup"><span data-stu-id="470b0-137">NOTES</span></span>

## <span data-ttu-id="470b0-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="470b0-138">RELATED LINKS</span></span>

[<span data-ttu-id="470b0-139">New-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="470b0-139">New-AzApiManagementProduct</span></span>](./New-AzApiManagementProduct.md)

[<span data-ttu-id="470b0-140">Remove-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="470b0-140">Remove-AzApiManagementProduct</span></span>](./Remove-AzApiManagementProduct.md)

[<span data-ttu-id="470b0-141">Set-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="470b0-141">Set-AzApiManagementProduct</span></span>](./Set-AzApiManagementProduct.md)


