---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: D5B18FF4-3294-4561-A4CD-CF0FA5E4A59B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: 088b88bcaa7f0d493552060c150e9d76a4b16c7f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426846"
---
# <span data-ttu-id="85d24-101">New-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="85d24-101">New-AzureRmApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="85d24-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="85d24-102">SYNOPSIS</span></span>
<span data-ttu-id="85d24-103">Cria um provedor de conexão OpenID.</span><span class="sxs-lookup"><span data-stu-id="85d24-103">Creates an OpenID Connect provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="85d24-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="85d24-104">SYNTAX</span></span>

```
New-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-OpenIdConnectProviderId <String>] -Name <String> -MetadataEndpointUri <String> -ClientId <String>
 [-ClientSecret <String>] [-Description <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="85d24-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="85d24-105">DESCRIPTION</span></span>
<span data-ttu-id="85d24-106">O cmdlet **New-AzureRmApiManagementOpenIdConnectProvider** cria um provedor de conexão OpenID no gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="85d24-106">The **New-AzureRmApiManagementOpenIdConnectProvider** cmdlet creates an OpenID Connect provider in Azure API Management.</span></span>

## <span data-ttu-id="85d24-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="85d24-107">EXAMPLES</span></span>

### <span data-ttu-id="85d24-108">Exemplo 1: criar um provedor</span><span class="sxs-lookup"><span data-stu-id="85d24-108">Example 1: Create a provider</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvicer01" -Name "Contoso OpenID Connect Provider" -MetadataEndpointUri "https://openid.provider/configuration" -ClientId "12432143" -Description "OpenID Connect provider description"
```

<span data-ttu-id="85d24-109">Esse comando cria um **provedor** de conexão OpenID chamado de provedor de conexão do contoso OpenID</span><span class="sxs-lookup"><span data-stu-id="85d24-109">This command creates an OpenID Connect **Provider** named Contoso OpenID Connect Provider</span></span>

## <span data-ttu-id="85d24-110">OS</span><span class="sxs-lookup"><span data-stu-id="85d24-110">PARAMETERS</span></span>

### <span data-ttu-id="85d24-111">-ClientId</span><span class="sxs-lookup"><span data-stu-id="85d24-111">-ClientId</span></span>
<span data-ttu-id="85d24-112">Especifica a ID do cliente do console de desenvolvedor.</span><span class="sxs-lookup"><span data-stu-id="85d24-112">Specifies the client ID of the developer console.</span></span>

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

### <span data-ttu-id="85d24-113">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="85d24-113">-ClientSecret</span></span>
<span data-ttu-id="85d24-114">Especifica o segredo do cliente do console de desenvolvedor.</span><span class="sxs-lookup"><span data-stu-id="85d24-114">Specifies the client secret of the developer console.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85d24-115">-Contexto</span><span class="sxs-lookup"><span data-stu-id="85d24-115">-Context</span></span>
<span data-ttu-id="85d24-116">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="85d24-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="85d24-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85d24-117">-DefaultProfile</span></span>
<span data-ttu-id="85d24-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="85d24-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="85d24-119">-Descrição</span><span class="sxs-lookup"><span data-stu-id="85d24-119">-Description</span></span>
<span data-ttu-id="85d24-120">Especifica uma descrição.</span><span class="sxs-lookup"><span data-stu-id="85d24-120">Specifies a description.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85d24-121">-MetadataEndpointUri</span><span class="sxs-lookup"><span data-stu-id="85d24-121">-MetadataEndpointUri</span></span>
<span data-ttu-id="85d24-122">Especifica um URI de ponto de extremidade de metadados do provedor.</span><span class="sxs-lookup"><span data-stu-id="85d24-122">Specifies a metadata endpoint URI of the provider.</span></span>

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

### <span data-ttu-id="85d24-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="85d24-123">-Name</span></span>
<span data-ttu-id="85d24-124">Especifica um nome amigável para o provedor.</span><span class="sxs-lookup"><span data-stu-id="85d24-124">Specifies a friendly name for the provider.</span></span>

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

### <span data-ttu-id="85d24-125">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="85d24-125">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="85d24-126">Especifica uma ID para o provedor.</span><span class="sxs-lookup"><span data-stu-id="85d24-126">Specifies an ID for the provider.</span></span>
<span data-ttu-id="85d24-127">Se você não especificar uma ID, esse cmdlet gerará uma.</span><span class="sxs-lookup"><span data-stu-id="85d24-127">If you do not specify an ID, this cmdlet generates one.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85d24-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85d24-128">CommonParameters</span></span>
<span data-ttu-id="85d24-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85d24-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85d24-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85d24-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85d24-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="85d24-131">INPUTS</span></span>

### <span data-ttu-id="85d24-132">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="85d24-132">None</span></span>
<span data-ttu-id="85d24-133">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="85d24-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="85d24-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="85d24-134">OUTPUTS</span></span>

### <span data-ttu-id="85d24-135">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="85d24-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="85d24-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="85d24-136">NOTES</span></span>

## <span data-ttu-id="85d24-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="85d24-137">RELATED LINKS</span></span>

[<span data-ttu-id="85d24-138">Get-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="85d24-138">Get-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Get-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="85d24-139">Remove-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="85d24-139">Remove-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Remove-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="85d24-140">Set-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="85d24-140">Set-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Set-AzureRmApiManagementOpenIdConnectProvider.md)


