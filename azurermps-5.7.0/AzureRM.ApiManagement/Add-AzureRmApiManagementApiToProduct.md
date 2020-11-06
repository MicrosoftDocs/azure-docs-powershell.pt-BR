---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 7C86B385-D784-45FD-9B57-31C895115A2C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/add-azurermapimanagementapitoproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementApiToProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementApiToProduct.md
ms.openlocfilehash: 08d6d8e5ecbcaa8b6810bd173062c5bb244ec5e8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93603066"
---
# <span data-ttu-id="8c724-101">Add-AzureRmApiManagementApiToProduct</span><span class="sxs-lookup"><span data-stu-id="8c724-101">Add-AzureRmApiManagementApiToProduct</span></span>

## <span data-ttu-id="8c724-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8c724-102">SYNOPSIS</span></span>
<span data-ttu-id="8c724-103">Adiciona uma API a um produto.</span><span class="sxs-lookup"><span data-stu-id="8c724-103">Adds an API to a product.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8c724-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8c724-104">SYNTAX</span></span>

```
Add-AzureRmApiManagementApiToProduct -Context <PsApiManagementContext> -ProductId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8c724-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8c724-105">DESCRIPTION</span></span>
<span data-ttu-id="8c724-106">O cmdlet **Add-AzureRmApiManagementApiToProduct** adiciona uma API de gerenciamento de API do Azure a um produto.</span><span class="sxs-lookup"><span data-stu-id="8c724-106">The **Add-AzureRmApiManagementApiToProduct** cmdlet adds an Azure API Management API to a product.</span></span>

## <span data-ttu-id="8c724-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8c724-107">EXAMPLES</span></span>

### <span data-ttu-id="8c724-108">Exemplo 1: adicionar uma API a um produto</span><span class="sxs-lookup"><span data-stu-id="8c724-108">Example 1: Add an API to a product</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzureRmApiManagementApiToProduct -Context $ApiMgmtContext -ProductId "0123456789" -ApiId "0001"
```

<span data-ttu-id="8c724-109">Este comando adiciona a API especificada ao produto especificado.</span><span class="sxs-lookup"><span data-stu-id="8c724-109">This command adds the specified API to the specified product.</span></span>

## <span data-ttu-id="8c724-110">OS</span><span class="sxs-lookup"><span data-stu-id="8c724-110">PARAMETERS</span></span>

### <span data-ttu-id="8c724-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="8c724-111">-ApiId</span></span>
<span data-ttu-id="8c724-112">Especifica a ID de uma API a ser adicionada a um produto.</span><span class="sxs-lookup"><span data-stu-id="8c724-112">Specifies the ID of an API to add to a product.</span></span>

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

### <span data-ttu-id="8c724-113">-Contexto</span><span class="sxs-lookup"><span data-stu-id="8c724-113">-Context</span></span>
<span data-ttu-id="8c724-114">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="8c724-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="8c724-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c724-115">-DefaultProfile</span></span>
<span data-ttu-id="8c724-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8c724-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c724-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8c724-117">-PassThru</span></span>
<span data-ttu-id="8c724-118">PassThru</span><span class="sxs-lookup"><span data-stu-id="8c724-118">passthru</span></span>

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

### <span data-ttu-id="8c724-119">-ProductId</span><span class="sxs-lookup"><span data-stu-id="8c724-119">-ProductId</span></span>
<span data-ttu-id="8c724-120">Especifica a ID do produto ao qual a API será adicionada.</span><span class="sxs-lookup"><span data-stu-id="8c724-120">Specifies the ID of the product to which to add the API.</span></span>

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

### <span data-ttu-id="8c724-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c724-121">CommonParameters</span></span>
<span data-ttu-id="8c724-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c724-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c724-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c724-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c724-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8c724-124">INPUTS</span></span>

### <span data-ttu-id="8c724-125">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="8c724-125">None</span></span>
<span data-ttu-id="8c724-126">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="8c724-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8c724-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8c724-127">OUTPUTS</span></span>

### <span data-ttu-id="8c724-128">Booliana</span><span class="sxs-lookup"><span data-stu-id="8c724-128">Boolean</span></span>

## <span data-ttu-id="8c724-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8c724-129">NOTES</span></span>

## <span data-ttu-id="8c724-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8c724-130">RELATED LINKS</span></span>

[<span data-ttu-id="8c724-131">Remove-AzureRmApiManagementApiFromProduct</span><span class="sxs-lookup"><span data-stu-id="8c724-131">Remove-AzureRmApiManagementApiFromProduct</span></span>](./Remove-AzureRmApiManagementApiFromProduct.md)


