---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 2457C7F5-7FB9-4712-AD7C-438E88F591A8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementapifromproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApiFromProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApiFromProduct.md
ms.openlocfilehash: 4bed4b5022292639a5bc55e30fdd8de356dc818a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431460"
---
# <span data-ttu-id="1680a-101">Remove-AzureRmApiManagementApiFromProduct</span><span class="sxs-lookup"><span data-stu-id="1680a-101">Remove-AzureRmApiManagementApiFromProduct</span></span>

## <span data-ttu-id="1680a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1680a-102">SYNOPSIS</span></span>
<span data-ttu-id="1680a-103">Remove uma API de um produto.</span><span class="sxs-lookup"><span data-stu-id="1680a-103">Removes an API from a product.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1680a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1680a-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementApiFromProduct -Context <PsApiManagementContext> -ProductId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1680a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1680a-105">DESCRIPTION</span></span>
<span data-ttu-id="1680a-106">O cmdlet **Remove-AzureRmApiManagementApiFromProduct** remove uma API de gerenciamento de API do Azure de um produto.</span><span class="sxs-lookup"><span data-stu-id="1680a-106">The **Remove-AzureRmApiManagementApiFromProduct** cmdlet removes an Azure API Management API from a product.</span></span>

## <span data-ttu-id="1680a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1680a-107">EXAMPLES</span></span>

### <span data-ttu-id="1680a-108">Exemplo 1: remover uma API de um produto</span><span class="sxs-lookup"><span data-stu-id="1680a-108">Example 1: Remove an API from a product</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementApiFromProduct -Context $ApiMgmtContext -ProductId "0123456789" -ApiId "0001" -PassThru
```

<span data-ttu-id="1680a-109">Isso commnd remove a API especificada de um produto.</span><span class="sxs-lookup"><span data-stu-id="1680a-109">This commnd removes the specified API from a product.</span></span>

## <span data-ttu-id="1680a-110">OS</span><span class="sxs-lookup"><span data-stu-id="1680a-110">PARAMETERS</span></span>

### <span data-ttu-id="1680a-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="1680a-111">-ApiId</span></span>
<span data-ttu-id="1680a-112">Especifica a ID da API a ser removida do produto.</span><span class="sxs-lookup"><span data-stu-id="1680a-112">Specifies the ID of the API to remove from the product.</span></span>

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

### <span data-ttu-id="1680a-113">-Contexto</span><span class="sxs-lookup"><span data-stu-id="1680a-113">-Context</span></span>
<span data-ttu-id="1680a-114">Especifica um **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="1680a-114">Specifies a **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="1680a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1680a-115">-DefaultProfile</span></span>
<span data-ttu-id="1680a-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1680a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1680a-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1680a-117">-PassThru</span></span>
<span data-ttu-id="1680a-118">Indica que esse cmdlet retorna um valor de $True se tiver êxito ou $False, caso contrário.</span><span class="sxs-lookup"><span data-stu-id="1680a-118">Indicates that this cmdlet returns a value of $True if it succeeds, or $False, otherwise.</span></span>

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

### <span data-ttu-id="1680a-119">-ProductId</span><span class="sxs-lookup"><span data-stu-id="1680a-119">-ProductId</span></span>
<span data-ttu-id="1680a-120">Especifica a ID do produto do qual a API deve ser removida.</span><span class="sxs-lookup"><span data-stu-id="1680a-120">Specifies the ID of the product from which to remove the API.</span></span>

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

### <span data-ttu-id="1680a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1680a-121">CommonParameters</span></span>
<span data-ttu-id="1680a-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1680a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1680a-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1680a-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1680a-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1680a-124">INPUTS</span></span>

### <span data-ttu-id="1680a-125">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="1680a-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="1680a-126">System. String</span><span class="sxs-lookup"><span data-stu-id="1680a-126">System.String</span></span>

### <span data-ttu-id="1680a-127">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1680a-127">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="1680a-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1680a-128">OUTPUTS</span></span>

### <span data-ttu-id="1680a-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1680a-129">System.Boolean</span></span>

## <span data-ttu-id="1680a-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1680a-130">NOTES</span></span>

## <span data-ttu-id="1680a-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1680a-131">RELATED LINKS</span></span>

[<span data-ttu-id="1680a-132">Add-AzureRmApiManagementApiToProduct</span><span class="sxs-lookup"><span data-stu-id="1680a-132">Add-AzureRmApiManagementApiToProduct</span></span>](./Add-AzureRmApiManagementApiToProduct.md)


