---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiVersionSet.md
ms.openlocfilehash: e6b9122481e5e506fc02a13a61b7ebeb71372e96
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116656"
---
# <span data-ttu-id="3b105-101">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="3b105-101">Get-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="3b105-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3b105-102">SYNOPSIS</span></span>
<span data-ttu-id="3b105-103">Obter os detalhes dos Conjuntos de Versão da API</span><span class="sxs-lookup"><span data-stu-id="3b105-103">Get the details of the API Version Sets</span></span>

## <span data-ttu-id="3b105-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3b105-104">SYNTAX</span></span>

### <span data-ttu-id="3b105-105">ContextParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="3b105-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementApiVersionSet -Context <PsApiManagementContext> [-ApiVersionSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3b105-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3b105-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementApiVersionSet -Context <PsApiManagementContext> [-ApiVersionSetId <String>]
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3b105-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="3b105-107">DESCRIPTION</span></span>
<span data-ttu-id="3b105-108">O cmdlet **Get-AzApiManagementApiVersionSet** obtém os detalhes dos Conjuntos de Versão da API configurados em um contexto de Gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="3b105-108">The **Get-AzApiManagementApiVersionSet** cmdlet gets the details of the API Version Sets configured in an API Management context.</span></span>

## <span data-ttu-id="3b105-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3b105-109">EXAMPLES</span></span>

### <span data-ttu-id="3b105-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3b105-110">Example 1</span></span>

### <span data-ttu-id="3b105-111">Exemplo 2: Obter todos os conjuntos de versão da API</span><span class="sxs-lookup"><span data-stu-id="3b105-111">Example 2: Get all API Version Sets</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApiVersionSet -Context $ApiMgmtContext

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

<span data-ttu-id="3b105-112">Esse comando obtém todos os conjuntos de versão da API para o contexto especificado.</span><span class="sxs-lookup"><span data-stu-id="3b105-112">This command gets all of the API Version sets for the specified context.</span></span>

### <span data-ttu-id="3b105-113">Exemplo 3: Obter uma versão da API definida por ID</span><span class="sxs-lookup"><span data-stu-id="3b105-113">Example 3: Get a API Version Set by ID</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApiVersionSet -Context $ApiMgmtContext -ApiVersionSetId $ApiVersionSetId

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

<span data-ttu-id="3b105-114">Esse comando obtém o Conjunto de Versões da API com a ID especificada.</span><span class="sxs-lookup"><span data-stu-id="3b105-114">This command gets the API Version Set with the specified ID.</span></span>

## <span data-ttu-id="3b105-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3b105-115">PARAMETERS</span></span>

### <span data-ttu-id="3b105-116">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="3b105-116">-ApiVersionSetId</span></span>
<span data-ttu-id="3b105-117">Identificador de API a ser pesquisado.</span><span class="sxs-lookup"><span data-stu-id="3b105-117">API identifier to look for.</span></span>
<span data-ttu-id="3b105-118">Se especificado, você tentará obter a API pela ID.</span><span class="sxs-lookup"><span data-stu-id="3b105-118">If specified will try to get the API by the Id.</span></span>

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

### <span data-ttu-id="3b105-119">-Contexto</span><span class="sxs-lookup"><span data-stu-id="3b105-119">-Context</span></span>
<span data-ttu-id="3b105-120">Instância de PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="3b105-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="3b105-121">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="3b105-121">This parameter is required.</span></span>

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

### <span data-ttu-id="3b105-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b105-122">-DefaultProfile</span></span>
<span data-ttu-id="3b105-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3b105-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b105-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3b105-124">-ResourceId</span></span>
<span data-ttu-id="3b105-125">Identificador de Recursos Arm do ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="3b105-125">Arm Resource Identifier of the ApiVersionSet.</span></span> <span data-ttu-id="3b105-126">Se especificado, tentará encontrar apiVersionSet pelo identificador.</span><span class="sxs-lookup"><span data-stu-id="3b105-126">If specified will try to find apiVersionSet by the identifier.</span></span> <span data-ttu-id="3b105-127">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="3b105-127">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b105-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b105-128">CommonParameters</span></span>
<span data-ttu-id="3b105-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b105-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b105-130">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3b105-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b105-131">Entradas</span><span class="sxs-lookup"><span data-stu-id="3b105-131">INPUTS</span></span>

### <span data-ttu-id="3b105-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="3b105-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="3b105-133">System.String</span><span class="sxs-lookup"><span data-stu-id="3b105-133">System.String</span></span>

## <span data-ttu-id="3b105-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="3b105-134">OUTPUTS</span></span>

### <span data-ttu-id="3b105-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="3b105-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

## <span data-ttu-id="3b105-136">Notas</span><span class="sxs-lookup"><span data-stu-id="3b105-136">NOTES</span></span>

## <span data-ttu-id="3b105-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3b105-137">RELATED LINKS</span></span>

[<span data-ttu-id="3b105-138">New-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="3b105-138">New-AzApiManagementApiVersionSet</span></span>](./New-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="3b105-139">Remove-AzApiManagementApiSet</span><span class="sxs-lookup"><span data-stu-id="3b105-139">Remove-AzApiManagementApiSet</span></span>](./Remove-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="3b105-140">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="3b105-140">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiVersionSet.md)
