---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 7C86B385-D784-45FD-9B57-31C895115A2C
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/add-azapimanagementapitoproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementApiToProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementApiToProduct.md
ms.openlocfilehash: a6c338b50341f80ba544e2e725e9fdabc3da4b13
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886286"
---
# <span data-ttu-id="8305e-101">Add-AzApiManagementApiToProduct</span><span class="sxs-lookup"><span data-stu-id="8305e-101">Add-AzApiManagementApiToProduct</span></span>

## <span data-ttu-id="8305e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8305e-102">SYNOPSIS</span></span>
<span data-ttu-id="8305e-103">Adiciona uma API a um produto.</span><span class="sxs-lookup"><span data-stu-id="8305e-103">Adds an API to a product.</span></span>

## <span data-ttu-id="8305e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="8305e-104">SYNTAX</span></span>

```
Add-AzApiManagementApiToProduct -Context <PsApiManagementContext> -ProductId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8305e-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="8305e-105">DESCRIPTION</span></span>
<span data-ttu-id="8305e-106">O cmdlet **Add-AzApiManagementApiToProduct** adiciona uma API de Gerenciamento de API do Azure a um produto.</span><span class="sxs-lookup"><span data-stu-id="8305e-106">The **Add-AzApiManagementApiToProduct** cmdlet adds an Azure API Management API to a product.</span></span>

## <span data-ttu-id="8305e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8305e-107">EXAMPLES</span></span>

### <span data-ttu-id="8305e-108">Exemplo 1: Adicionar uma API a um produto</span><span class="sxs-lookup"><span data-stu-id="8305e-108">Example 1: Add an API to a product</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzApiManagementApiToProduct -Context $ApiMgmtContext -ProductId "0123456789" -ApiId "0001"
```

<span data-ttu-id="8305e-109">Este comando adiciona a API especificada ao produto especificado.</span><span class="sxs-lookup"><span data-stu-id="8305e-109">This command adds the specified API to the specified product.</span></span>

## <span data-ttu-id="8305e-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="8305e-110">PARAMETERS</span></span>

### <span data-ttu-id="8305e-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="8305e-111">-ApiId</span></span>
<span data-ttu-id="8305e-112">Especifica a ID de uma API a ser acrescentada a um produto.</span><span class="sxs-lookup"><span data-stu-id="8305e-112">Specifies the ID of an API to add to a product.</span></span>

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

### <span data-ttu-id="8305e-113">-Context</span><span class="sxs-lookup"><span data-stu-id="8305e-113">-Context</span></span>
<span data-ttu-id="8305e-114">Especifica um **objeto PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="8305e-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="8305e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8305e-115">-DefaultProfile</span></span>
<span data-ttu-id="8305e-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="8305e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8305e-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8305e-117">-PassThru</span></span>
<span data-ttu-id="8305e-118">passthru</span><span class="sxs-lookup"><span data-stu-id="8305e-118">passthru</span></span>

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

### <span data-ttu-id="8305e-119">-ProductId</span><span class="sxs-lookup"><span data-stu-id="8305e-119">-ProductId</span></span>
<span data-ttu-id="8305e-120">Especifica a ID do produto ao qual adicionar a API.</span><span class="sxs-lookup"><span data-stu-id="8305e-120">Specifies the ID of the product to which to add the API.</span></span>

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

### <span data-ttu-id="8305e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8305e-121">CommonParameters</span></span>
<span data-ttu-id="8305e-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8305e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8305e-123">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8305e-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8305e-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8305e-124">INPUTS</span></span>

### <span data-ttu-id="8305e-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="8305e-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="8305e-126">System.String</span><span class="sxs-lookup"><span data-stu-id="8305e-126">System.String</span></span>

### <span data-ttu-id="8305e-127">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="8305e-127">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="8305e-128">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="8305e-128">OUTPUTS</span></span>

### <span data-ttu-id="8305e-129">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8305e-129">System.Boolean</span></span>

## <span data-ttu-id="8305e-130">NOTES</span><span class="sxs-lookup"><span data-stu-id="8305e-130">NOTES</span></span>

## <span data-ttu-id="8305e-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8305e-131">RELATED LINKS</span></span>

[<span data-ttu-id="8305e-132">Remove-AzApiManagementApiFromProduct</span><span class="sxs-lookup"><span data-stu-id="8305e-132">Remove-AzApiManagementApiFromProduct</span></span>](./Remove-AzApiManagementApiFromProduct.md)


