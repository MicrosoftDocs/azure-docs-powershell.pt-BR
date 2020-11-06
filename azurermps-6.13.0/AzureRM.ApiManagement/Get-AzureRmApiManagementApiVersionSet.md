---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementApiVersionSet.md
ms.openlocfilehash: 60a811aaa097ccc95f8dd57fa105ba4b1388b060
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431476"
---
# <span data-ttu-id="ccc52-101">Get-AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="ccc52-101">Get-AzureRmApiManagementApiVersionSet</span></span>

## <span data-ttu-id="ccc52-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ccc52-102">SYNOPSIS</span></span>
<span data-ttu-id="ccc52-103">Obter os detalhes dos conjuntos de versões da API</span><span class="sxs-lookup"><span data-stu-id="ccc52-103">Get the details of the API Version Sets</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ccc52-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ccc52-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementApiVersionSet -Context <PsApiManagementContext> [-ApiVersionSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ccc52-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ccc52-105">DESCRIPTION</span></span>
<span data-ttu-id="ccc52-106">O cmdlet **Get-AzureRmApiManagementApiVersionSet** Obtém os detalhes dos conjuntos de versão da API configurados em um contexto de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="ccc52-106">The **Get-AzureRmApiManagementApiVersionSet** cmdlet gets the details of the API Version Sets configured in an API Management context.</span></span>

## <span data-ttu-id="ccc52-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ccc52-107">EXAMPLES</span></span>

### <span data-ttu-id="ccc52-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ccc52-108">Example 1</span></span>

### <span data-ttu-id="ccc52-109">Exemplo 1: obter todos os conjuntos de versões de API</span><span class="sxs-lookup"><span data-stu-id="ccc52-109">Example 1: Get all API Version Sets</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementApiVersionSet -Context $ApiMgmtContext

ApiVersionSetId   : a93316c8-8b88-46cc-8260-380789a5d598
Description       :
VersionQueryName  :
VersionHeaderName :
DisplayName       : Echo API
VersioningScheme  : Segment
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/api-version-sets/a916c8-8b88-46cc-8260-380789a5d598
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso

ApiVersionSetId   : 4cbdfa34-25f3-4a93-a9b6-76b6eade7562
Description       :
VersionQueryName  : api-version
VersionHeaderName :
DisplayName       : getproduct old
VersioningScheme  : Query
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/api-version-sets/4cbdfa34-25f3-4a93-a9b6-76b6eade7562
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso


ApiVersionSetId   : 8c441e0e-a0cd-47d8-8d88-f944a83b41bd
Description       :
VersionQueryName  :
VersionHeaderName : Api-Version
DisplayName       : ordersapi
VersioningScheme  : Header
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/api-version-sets/8c441e0e-a0cd-47d8-8d88-f944a83b41bd
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso
```

<span data-ttu-id="ccc52-110">Esse comando obtém todos os conjuntos de versões de API do contexto especificado.</span><span class="sxs-lookup"><span data-stu-id="ccc52-110">This command gets all of the API Version sets for the specified context.</span></span>

### <span data-ttu-id="ccc52-111">Exemplo 2: obter uma versão de API definida por ID</span><span class="sxs-lookup"><span data-stu-id="ccc52-111">Example 2: Get a API Version Set by ID</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementApiVersionSet -Context $ApiMgmtContext -ApiVersionSetId $ApiVersionSetId

ApiVersionSetId   : 8c441e0e-a0cd-47d8-8d88-f944a83b41bd
Description       :
VersionQueryName  :
VersionHeaderName : Api-Version
DisplayName       : ordersapi
VersioningScheme  : Header
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/api-version-sets/8c441e0e-a0cd-47d8-8d88-f944a83b41bd
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso
```

<span data-ttu-id="ccc52-112">Esse comando obtém a versão da API definida com a ID especificada.</span><span class="sxs-lookup"><span data-stu-id="ccc52-112">This command gets the API Version Set with the specified ID.</span></span>

## <span data-ttu-id="ccc52-113">OS</span><span class="sxs-lookup"><span data-stu-id="ccc52-113">PARAMETERS</span></span>

### <span data-ttu-id="ccc52-114">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="ccc52-114">-ApiVersionSetId</span></span>
<span data-ttu-id="ccc52-115">Identificador de API a ser procurado.</span><span class="sxs-lookup"><span data-stu-id="ccc52-115">API identifier to look for.</span></span>
<span data-ttu-id="ccc52-116">Se especificado, você tentará obter a API pela ID.</span><span class="sxs-lookup"><span data-stu-id="ccc52-116">If specified will try to get the API by the Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ccc52-117">-Contexto</span><span class="sxs-lookup"><span data-stu-id="ccc52-117">-Context</span></span>
<span data-ttu-id="ccc52-118">Instância do PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="ccc52-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="ccc52-119">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="ccc52-119">This parameter is required.</span></span>

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

### <span data-ttu-id="ccc52-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccc52-120">-DefaultProfile</span></span>
<span data-ttu-id="ccc52-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ccc52-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ccc52-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccc52-122">CommonParameters</span></span>
<span data-ttu-id="ccc52-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ccc52-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccc52-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ccc52-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccc52-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ccc52-125">INPUTS</span></span>

### <span data-ttu-id="ccc52-126">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ccc52-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ccc52-127">System. String</span><span class="sxs-lookup"><span data-stu-id="ccc52-127">System.String</span></span>

## <span data-ttu-id="ccc52-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ccc52-128">OUTPUTS</span></span>

### <span data-ttu-id="ccc52-129">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="ccc52-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

## <span data-ttu-id="ccc52-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ccc52-130">NOTES</span></span>

## <span data-ttu-id="ccc52-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ccc52-131">RELATED LINKS</span></span>

[<span data-ttu-id="ccc52-132">New-AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="ccc52-132">New-AzureRmApiManagementApiVersionSet</span></span>](./New-AzureRmApiManagementApiVersionSet.md)

[<span data-ttu-id="ccc52-133">Remove-AzureRmApiManagementApiSet</span><span class="sxs-lookup"><span data-stu-id="ccc52-133">Remove-AzureRmApiManagementApiSet</span></span>](./Remove-AzureRmApiManagementApiVersionSet.md)

[<span data-ttu-id="ccc52-134">Set-AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="ccc52-134">Set-AzureRmApiManagementApiVersionSet</span></span>](./Set-AzureRmApiManagementApiSet.md)
