---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B64E9C13-97A6-4E8B-92DB-EFAF8A48C5B8
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementProduct.md
ms.openlocfilehash: 8e59cbb9885587ee57103b78400ce8ece9aafd46
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113646"
---
# <span data-ttu-id="e6d73-101">Get-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="e6d73-101">Get-AzApiManagementProduct</span></span>

## <span data-ttu-id="e6d73-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e6d73-102">SYNOPSIS</span></span>
<span data-ttu-id="e6d73-103">Obtém uma lista ou um produto específico.</span><span class="sxs-lookup"><span data-stu-id="e6d73-103">Gets a list or a particular product.</span></span>

## <span data-ttu-id="e6d73-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e6d73-104">SYNTAX</span></span>

### <span data-ttu-id="e6d73-105">GetAllProducts (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e6d73-105">GetAllProducts (Default)</span></span>
```
Get-AzApiManagementProduct -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e6d73-106">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="e6d73-106">GetByProductId</span></span>
```
Get-AzApiManagementProduct -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e6d73-107">GetByTitle</span><span class="sxs-lookup"><span data-stu-id="e6d73-107">GetByTitle</span></span>
```
Get-AzApiManagementProduct -Context <PsApiManagementContext> [-Title <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e6d73-108">GetByApiId</span><span class="sxs-lookup"><span data-stu-id="e6d73-108">GetByApiId</span></span>
```
Get-AzApiManagementProduct -Context <PsApiManagementContext> -ApiId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e6d73-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="e6d73-109">DESCRIPTION</span></span>
<span data-ttu-id="e6d73-110">O cmdlet **Get-AzApiManagementProduct** obtém uma lista ou um produto específico.</span><span class="sxs-lookup"><span data-stu-id="e6d73-110">The **Get-AzApiManagementProduct** cmdlet gets a list or a particular product.</span></span>

## <span data-ttu-id="e6d73-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e6d73-111">EXAMPLES</span></span>

### <span data-ttu-id="e6d73-112">Exemplo 1: Obter todos os produtos</span><span class="sxs-lookup"><span data-stu-id="e6d73-112">Example 1: Get all products</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementProduct -Context $apimContext
```

<span data-ttu-id="e6d73-113">Este comando obterá todos os produtos de Gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="e6d73-113">This command get all API Management products.</span></span>

### <span data-ttu-id="e6d73-114">Exemplo 2: Obter um produto por ID</span><span class="sxs-lookup"><span data-stu-id="e6d73-114">Example 2: Get a product by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementProduct -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="e6d73-115">Este comando obterá um produto de Gerenciamento de API por ID.</span><span class="sxs-lookup"><span data-stu-id="e6d73-115">This command get an API Management product by ID.</span></span>

## <span data-ttu-id="e6d73-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e6d73-116">PARAMETERS</span></span>

### <span data-ttu-id="e6d73-117">-ApiId</span><span class="sxs-lookup"><span data-stu-id="e6d73-117">-ApiId</span></span>
<span data-ttu-id="e6d73-118">ApiId da Api para encontrar os produtos correlacionados.</span><span class="sxs-lookup"><span data-stu-id="e6d73-118">ApiId of the Api to find the correlated products.</span></span> <span data-ttu-id="e6d73-119">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="e6d73-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="e6d73-120">-Contexto</span><span class="sxs-lookup"><span data-stu-id="e6d73-120">-Context</span></span>
<span data-ttu-id="e6d73-121">Especifica uma instância de um **objeto PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="e6d73-121">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="e6d73-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6d73-122">-DefaultProfile</span></span>
<span data-ttu-id="e6d73-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="e6d73-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e6d73-124">-ProductId</span><span class="sxs-lookup"><span data-stu-id="e6d73-124">-ProductId</span></span>
<span data-ttu-id="e6d73-125">Especifica o identificador do produto a ser pesquisado.</span><span class="sxs-lookup"><span data-stu-id="e6d73-125">Specifies the identifier of the product to search for.</span></span>

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

### <span data-ttu-id="e6d73-126">-Título</span><span class="sxs-lookup"><span data-stu-id="e6d73-126">-Title</span></span>
<span data-ttu-id="e6d73-127">Especifica o título do produto a ser procurar.</span><span class="sxs-lookup"><span data-stu-id="e6d73-127">Specifies the title of the product to look for.</span></span>
<span data-ttu-id="e6d73-128">Se especificado, o cmdlet tentará obter o produto por título.</span><span class="sxs-lookup"><span data-stu-id="e6d73-128">If specified, the cmdlet attempts to get the product by title.</span></span>

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

### <span data-ttu-id="e6d73-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6d73-129">CommonParameters</span></span>
<span data-ttu-id="e6d73-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6d73-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6d73-131">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e6d73-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6d73-132">Entradas</span><span class="sxs-lookup"><span data-stu-id="e6d73-132">INPUTS</span></span>

### <span data-ttu-id="e6d73-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e6d73-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e6d73-134">System.String</span><span class="sxs-lookup"><span data-stu-id="e6d73-134">System.String</span></span>

## <span data-ttu-id="e6d73-135">Saídas</span><span class="sxs-lookup"><span data-stu-id="e6d73-135">OUTPUTS</span></span>

### <span data-ttu-id="e6d73-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="e6d73-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="e6d73-137">Notas</span><span class="sxs-lookup"><span data-stu-id="e6d73-137">NOTES</span></span>

## <span data-ttu-id="e6d73-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e6d73-138">RELATED LINKS</span></span>

[<span data-ttu-id="e6d73-139">New-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="e6d73-139">New-AzApiManagementProduct</span></span>](./New-AzApiManagementProduct.md)

[<span data-ttu-id="e6d73-140">Remove-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="e6d73-140">Remove-AzApiManagementProduct</span></span>](./Remove-AzApiManagementProduct.md)

[<span data-ttu-id="e6d73-141">Set-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="e6d73-141">Set-AzApiManagementProduct</span></span>](./Set-AzApiManagementProduct.md)


