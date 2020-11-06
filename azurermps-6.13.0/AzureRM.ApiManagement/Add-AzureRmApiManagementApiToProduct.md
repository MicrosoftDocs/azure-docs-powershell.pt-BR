---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 7C86B385-D784-45FD-9B57-31C895115A2C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/add-azurermapimanagementapitoproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementApiToProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementApiToProduct.md
ms.openlocfilehash: 16bb651efd13d42b25509834637faea866678459
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609867"
---
# <span data-ttu-id="32db0-101">Add-AzureRmApiManagementApiToProduct</span><span class="sxs-lookup"><span data-stu-id="32db0-101">Add-AzureRmApiManagementApiToProduct</span></span>

## <span data-ttu-id="32db0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="32db0-102">SYNOPSIS</span></span>
<span data-ttu-id="32db0-103">Adiciona uma API a um produto.</span><span class="sxs-lookup"><span data-stu-id="32db0-103">Adds an API to a product.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="32db0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="32db0-104">SYNTAX</span></span>

```
Add-AzureRmApiManagementApiToProduct -Context <PsApiManagementContext> -ProductId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="32db0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="32db0-105">DESCRIPTION</span></span>
<span data-ttu-id="32db0-106">O cmdlet **Add-AzureRmApiManagementApiToProduct** adiciona uma API de gerenciamento de API do Azure a um produto.</span><span class="sxs-lookup"><span data-stu-id="32db0-106">The **Add-AzureRmApiManagementApiToProduct** cmdlet adds an Azure API Management API to a product.</span></span>

## <span data-ttu-id="32db0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="32db0-107">EXAMPLES</span></span>

### <span data-ttu-id="32db0-108">Exemplo 1: adicionar uma API a um produto</span><span class="sxs-lookup"><span data-stu-id="32db0-108">Example 1: Add an API to a product</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzureRmApiManagementApiToProduct -Context $ApiMgmtContext -ProductId "0123456789" -ApiId "0001"
```

<span data-ttu-id="32db0-109">Este comando adiciona a API especificada ao produto especificado.</span><span class="sxs-lookup"><span data-stu-id="32db0-109">This command adds the specified API to the specified product.</span></span>

## <span data-ttu-id="32db0-110">OS</span><span class="sxs-lookup"><span data-stu-id="32db0-110">PARAMETERS</span></span>

### <span data-ttu-id="32db0-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="32db0-111">-ApiId</span></span>
<span data-ttu-id="32db0-112">Especifica a ID de uma API a ser adicionada a um produto.</span><span class="sxs-lookup"><span data-stu-id="32db0-112">Specifies the ID of an API to add to a product.</span></span>

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

### <span data-ttu-id="32db0-113">-Contexto</span><span class="sxs-lookup"><span data-stu-id="32db0-113">-Context</span></span>
<span data-ttu-id="32db0-114">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="32db0-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="32db0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32db0-115">-DefaultProfile</span></span>
<span data-ttu-id="32db0-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="32db0-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="32db0-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="32db0-117">-PassThru</span></span>
<span data-ttu-id="32db0-118">PassThru</span><span class="sxs-lookup"><span data-stu-id="32db0-118">passthru</span></span>

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

### <span data-ttu-id="32db0-119">-ProductId</span><span class="sxs-lookup"><span data-stu-id="32db0-119">-ProductId</span></span>
<span data-ttu-id="32db0-120">Especifica a ID do produto ao qual a API será adicionada.</span><span class="sxs-lookup"><span data-stu-id="32db0-120">Specifies the ID of the product to which to add the API.</span></span>

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

### <span data-ttu-id="32db0-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32db0-121">CommonParameters</span></span>
<span data-ttu-id="32db0-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32db0-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32db0-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32db0-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32db0-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="32db0-124">INPUTS</span></span>

### <span data-ttu-id="32db0-125">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="32db0-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="32db0-126">System. String</span><span class="sxs-lookup"><span data-stu-id="32db0-126">System.String</span></span>

### <span data-ttu-id="32db0-127">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="32db0-127">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="32db0-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="32db0-128">OUTPUTS</span></span>

### <span data-ttu-id="32db0-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="32db0-129">System.Boolean</span></span>

## <span data-ttu-id="32db0-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="32db0-130">NOTES</span></span>

## <span data-ttu-id="32db0-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="32db0-131">RELATED LINKS</span></span>

[<span data-ttu-id="32db0-132">Remove-AzureRmApiManagementApiFromProduct</span><span class="sxs-lookup"><span data-stu-id="32db0-132">Remove-AzureRmApiManagementApiFromProduct</span></span>](./Remove-AzureRmApiManagementApiFromProduct.md)


