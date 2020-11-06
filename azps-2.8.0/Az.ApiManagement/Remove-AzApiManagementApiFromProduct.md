---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 2457C7F5-7FB9-4712-AD7C-438E88F591A8
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapifromproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiFromProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiFromProduct.md
ms.openlocfilehash: 497e830ff5ee51a9b18480a4d3f31f7c51949723
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598005"
---
# <span data-ttu-id="fcea8-101">Remove-AzApiManagementApiFromProduct</span><span class="sxs-lookup"><span data-stu-id="fcea8-101">Remove-AzApiManagementApiFromProduct</span></span>

## <span data-ttu-id="fcea8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fcea8-102">SYNOPSIS</span></span>
<span data-ttu-id="fcea8-103">Remove uma API de um produto.</span><span class="sxs-lookup"><span data-stu-id="fcea8-103">Removes an API from a product.</span></span>

## <span data-ttu-id="fcea8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fcea8-104">SYNTAX</span></span>

```
Remove-AzApiManagementApiFromProduct -Context <PsApiManagementContext> -ProductId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fcea8-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fcea8-105">DESCRIPTION</span></span>
<span data-ttu-id="fcea8-106">O cmdlet **Remove-AzApiManagementApiFromProduct** remove uma API de gerenciamento de API do Azure de um produto.</span><span class="sxs-lookup"><span data-stu-id="fcea8-106">The **Remove-AzApiManagementApiFromProduct** cmdlet removes an Azure API Management API from a product.</span></span>

## <span data-ttu-id="fcea8-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fcea8-107">EXAMPLES</span></span>

### <span data-ttu-id="fcea8-108">Exemplo 1: remover uma API de um produto</span><span class="sxs-lookup"><span data-stu-id="fcea8-108">Example 1: Remove an API from a product</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApiFromProduct -Context $ApiMgmtContext -ProductId "0123456789" -ApiId "0001" -PassThru
```

<span data-ttu-id="fcea8-109">Esse comando Remove a API especificada de um produto.</span><span class="sxs-lookup"><span data-stu-id="fcea8-109">This command removes the specified API from a product.</span></span>

## <span data-ttu-id="fcea8-110">OS</span><span class="sxs-lookup"><span data-stu-id="fcea8-110">PARAMETERS</span></span>

### <span data-ttu-id="fcea8-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="fcea8-111">-ApiId</span></span>
<span data-ttu-id="fcea8-112">Especifica a ID da API a ser removida do produto.</span><span class="sxs-lookup"><span data-stu-id="fcea8-112">Specifies the ID of the API to remove from the product.</span></span>

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

### <span data-ttu-id="fcea8-113">-Contexto</span><span class="sxs-lookup"><span data-stu-id="fcea8-113">-Context</span></span>
<span data-ttu-id="fcea8-114">Especifica um **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="fcea8-114">Specifies a **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="fcea8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcea8-115">-DefaultProfile</span></span>
<span data-ttu-id="fcea8-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fcea8-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fcea8-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fcea8-117">-PassThru</span></span>
<span data-ttu-id="fcea8-118">Indica que esse cmdlet retorna um valor de $True se tiver êxito ou $False, caso contrário.</span><span class="sxs-lookup"><span data-stu-id="fcea8-118">Indicates that this cmdlet returns a value of $True if it succeeds, or $False, otherwise.</span></span>

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

### <span data-ttu-id="fcea8-119">-ProductId</span><span class="sxs-lookup"><span data-stu-id="fcea8-119">-ProductId</span></span>
<span data-ttu-id="fcea8-120">Especifica a ID do produto do qual a API deve ser removida.</span><span class="sxs-lookup"><span data-stu-id="fcea8-120">Specifies the ID of the product from which to remove the API.</span></span>

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

### <span data-ttu-id="fcea8-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcea8-121">CommonParameters</span></span>
<span data-ttu-id="fcea8-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fcea8-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcea8-123">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fcea8-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcea8-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fcea8-124">INPUTS</span></span>

### <span data-ttu-id="fcea8-125">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="fcea8-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="fcea8-126">System. String</span><span class="sxs-lookup"><span data-stu-id="fcea8-126">System.String</span></span>

### <span data-ttu-id="fcea8-127">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="fcea8-127">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="fcea8-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fcea8-128">OUTPUTS</span></span>

### <span data-ttu-id="fcea8-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fcea8-129">System.Boolean</span></span>

## <span data-ttu-id="fcea8-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fcea8-130">NOTES</span></span>

## <span data-ttu-id="fcea8-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fcea8-131">RELATED LINKS</span></span>

[<span data-ttu-id="fcea8-132">Add-AzApiManagementApiToProduct</span><span class="sxs-lookup"><span data-stu-id="fcea8-132">Add-AzApiManagementApiToProduct</span></span>](./Add-AzApiManagementApiToProduct.md)


