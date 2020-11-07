---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: D5B18FF4-3294-4561-A4CD-CF0FA5E4A59B
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: 3b4cec203e39401885874db5391f62a9f1663342
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771417"
---
# <span data-ttu-id="66675-101">New-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="66675-101">New-AzApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="66675-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="66675-102">SYNOPSIS</span></span>
<span data-ttu-id="66675-103">Cria um provedor de conexão OpenID.</span><span class="sxs-lookup"><span data-stu-id="66675-103">Creates an OpenID Connect provider.</span></span>

## <span data-ttu-id="66675-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="66675-104">SYNTAX</span></span>

```
New-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-OpenIdConnectProviderId <String>]
 -Name <String> -MetadataEndpointUri <String> -ClientId <String> [-ClientSecret <String>]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66675-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="66675-105">DESCRIPTION</span></span>
<span data-ttu-id="66675-106">O cmdlet **New-AzApiManagementOpenIdConnectProvider** cria um provedor de conexão OpenID no gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="66675-106">The **New-AzApiManagementOpenIdConnectProvider** cmdlet creates an OpenID Connect provider in Azure API Management.</span></span>

## <span data-ttu-id="66675-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="66675-107">EXAMPLES</span></span>

### <span data-ttu-id="66675-108">Exemplo 1: criar um provedor</span><span class="sxs-lookup"><span data-stu-id="66675-108">Example 1: Create a provider</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvicer01" -Name "Contoso OpenID Connect Provider" -MetadataEndpointUri "https://openid.provider/configuration" -ClientId "12432143" -Description "OpenID Connect provider description"
```

<span data-ttu-id="66675-109">Esse comando cria um **provedor** de conexão OpenID chamado de provedor de conexão do contoso OpenID</span><span class="sxs-lookup"><span data-stu-id="66675-109">This command creates an OpenID Connect **Provider** named Contoso OpenID Connect Provider</span></span>

## <span data-ttu-id="66675-110">OS</span><span class="sxs-lookup"><span data-stu-id="66675-110">PARAMETERS</span></span>

### <span data-ttu-id="66675-111">-ClientId</span><span class="sxs-lookup"><span data-stu-id="66675-111">-ClientId</span></span>
<span data-ttu-id="66675-112">Especifica a ID do cliente do console de desenvolvedor.</span><span class="sxs-lookup"><span data-stu-id="66675-112">Specifies the client ID of the developer console.</span></span>

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

### <span data-ttu-id="66675-113">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="66675-113">-ClientSecret</span></span>
<span data-ttu-id="66675-114">Especifica o segredo do cliente do console de desenvolvedor.</span><span class="sxs-lookup"><span data-stu-id="66675-114">Specifies the client secret of the developer console.</span></span>

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

### <span data-ttu-id="66675-115">-Contexto</span><span class="sxs-lookup"><span data-stu-id="66675-115">-Context</span></span>
<span data-ttu-id="66675-116">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="66675-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="66675-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66675-117">-DefaultProfile</span></span>
<span data-ttu-id="66675-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="66675-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66675-119">-Descrição</span><span class="sxs-lookup"><span data-stu-id="66675-119">-Description</span></span>
<span data-ttu-id="66675-120">Especifica uma descrição.</span><span class="sxs-lookup"><span data-stu-id="66675-120">Specifies a description.</span></span>

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

### <span data-ttu-id="66675-121">-MetadataEndpointUri</span><span class="sxs-lookup"><span data-stu-id="66675-121">-MetadataEndpointUri</span></span>
<span data-ttu-id="66675-122">Especifica um URI de ponto de extremidade de metadados do provedor.</span><span class="sxs-lookup"><span data-stu-id="66675-122">Specifies a metadata endpoint URI of the provider.</span></span>

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

### <span data-ttu-id="66675-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="66675-123">-Name</span></span>
<span data-ttu-id="66675-124">Especifica um nome amigável para o provedor.</span><span class="sxs-lookup"><span data-stu-id="66675-124">Specifies a friendly name for the provider.</span></span>

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

### <span data-ttu-id="66675-125">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="66675-125">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="66675-126">Especifica uma ID para o provedor.</span><span class="sxs-lookup"><span data-stu-id="66675-126">Specifies an ID for the provider.</span></span>
<span data-ttu-id="66675-127">Se você não especificar uma ID, esse cmdlet gerará uma.</span><span class="sxs-lookup"><span data-stu-id="66675-127">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="66675-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66675-128">CommonParameters</span></span>
<span data-ttu-id="66675-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66675-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66675-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66675-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66675-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="66675-131">INPUTS</span></span>

### <span data-ttu-id="66675-132">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="66675-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="66675-133">System. String</span><span class="sxs-lookup"><span data-stu-id="66675-133">System.String</span></span>

## <span data-ttu-id="66675-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="66675-134">OUTPUTS</span></span>

### <span data-ttu-id="66675-135">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="66675-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="66675-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="66675-136">NOTES</span></span>

## <span data-ttu-id="66675-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="66675-137">RELATED LINKS</span></span>

[<span data-ttu-id="66675-138">Get-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="66675-138">Get-AzApiManagementOpenIdConnectProvider</span></span>](./Get-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="66675-139">Remove-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="66675-139">Remove-AzApiManagementOpenIdConnectProvider</span></span>](./Remove-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="66675-140">Set-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="66675-140">Set-AzApiManagementOpenIdConnectProvider</span></span>](./Set-AzApiManagementOpenIdConnectProvider.md)


