---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: D5B18FF4-3294-4561-A4CD-CF0FA5E4A59B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: f008d21e1d1d3f2aba7c87255fa7c95074bca532
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431221"
---
# <span data-ttu-id="4274d-101">New-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="4274d-101">New-AzureRmApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="4274d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4274d-102">SYNOPSIS</span></span>
<span data-ttu-id="4274d-103">Cria um provedor de conexão OpenID.</span><span class="sxs-lookup"><span data-stu-id="4274d-103">Creates an OpenID Connect provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4274d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4274d-104">SYNTAX</span></span>

```
New-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-OpenIdConnectProviderId <String>] -Name <String> -MetadataEndpointUri <String> -ClientId <String>
 [-ClientSecret <String>] [-Description <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4274d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4274d-105">DESCRIPTION</span></span>
<span data-ttu-id="4274d-106">O cmdlet **New-AzureRmApiManagementOpenIdConnectProvider** cria um provedor de conexão OpenID no gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="4274d-106">The **New-AzureRmApiManagementOpenIdConnectProvider** cmdlet creates an OpenID Connect provider in Azure API Management.</span></span>

## <span data-ttu-id="4274d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4274d-107">EXAMPLES</span></span>

### <span data-ttu-id="4274d-108">Exemplo 1: criar um provedor</span><span class="sxs-lookup"><span data-stu-id="4274d-108">Example 1: Create a provider</span></span>
```
PS C:\>New-AzureRmApiManagementOpenIdConnectProvider -Context $ApimContext -OpenIdConnectProviderId "OICProvicer01" -Name "Contoso OpenID Connect Provider" -MetadataEndpointUri "https://openid.provider/configuration" -ClientId "12432143" -Description "OpenID Connect provider description"
```

<span data-ttu-id="4274d-109">Esse comando cria um **provedor** de conexão OpenID chamado de provedor de conexão do contoso OpenID</span><span class="sxs-lookup"><span data-stu-id="4274d-109">This command creates an OpenID Connect **Provider** named Contoso OpenID Connect Provider</span></span>

## <span data-ttu-id="4274d-110">OS</span><span class="sxs-lookup"><span data-stu-id="4274d-110">PARAMETERS</span></span>

### <span data-ttu-id="4274d-111">-ClientId</span><span class="sxs-lookup"><span data-stu-id="4274d-111">-ClientId</span></span>
<span data-ttu-id="4274d-112">Especifica a ID do cliente do console de desenvolvedor.</span><span class="sxs-lookup"><span data-stu-id="4274d-112">Specifies the client ID of the developer console.</span></span>

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

### <span data-ttu-id="4274d-113">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="4274d-113">-ClientSecret</span></span>
<span data-ttu-id="4274d-114">Especifica o segredo do cliente do console de desenvolvedor.</span><span class="sxs-lookup"><span data-stu-id="4274d-114">Specifies the client secret of the developer console.</span></span>

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

### <span data-ttu-id="4274d-115">-Contexto</span><span class="sxs-lookup"><span data-stu-id="4274d-115">-Context</span></span>
<span data-ttu-id="4274d-116">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="4274d-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="4274d-117">-Descrição</span><span class="sxs-lookup"><span data-stu-id="4274d-117">-Description</span></span>
<span data-ttu-id="4274d-118">Especifica uma descrição.</span><span class="sxs-lookup"><span data-stu-id="4274d-118">Specifies a description.</span></span>

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

### <span data-ttu-id="4274d-119">-MetadataEndpointUri</span><span class="sxs-lookup"><span data-stu-id="4274d-119">-MetadataEndpointUri</span></span>
<span data-ttu-id="4274d-120">Especifica um URI de ponto de extremidade de metadados do provedor.</span><span class="sxs-lookup"><span data-stu-id="4274d-120">Specifies a metadata endpoint URI of the provider.</span></span>

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

### <span data-ttu-id="4274d-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="4274d-121">-Name</span></span>
<span data-ttu-id="4274d-122">Especifica um nome amigável para o provedor.</span><span class="sxs-lookup"><span data-stu-id="4274d-122">Specifies a friendly name for the provider.</span></span>

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

### <span data-ttu-id="4274d-123">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="4274d-123">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="4274d-124">Especifica uma ID para o provedor.</span><span class="sxs-lookup"><span data-stu-id="4274d-124">Specifies an ID for the provider.</span></span>
<span data-ttu-id="4274d-125">Se você não especificar uma ID, esse cmdlet gerará uma.</span><span class="sxs-lookup"><span data-stu-id="4274d-125">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="4274d-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4274d-126">-DefaultProfile</span></span>
<span data-ttu-id="4274d-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4274d-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4274d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4274d-128">CommonParameters</span></span>
<span data-ttu-id="4274d-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4274d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4274d-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4274d-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4274d-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4274d-131">INPUTS</span></span>

## <span data-ttu-id="4274d-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4274d-132">OUTPUTS</span></span>

### <span data-ttu-id="4274d-133">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="4274d-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="4274d-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4274d-134">NOTES</span></span>

## <span data-ttu-id="4274d-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4274d-135">RELATED LINKS</span></span>

[<span data-ttu-id="4274d-136">Get-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="4274d-136">Get-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Get-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="4274d-137">Remove-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="4274d-137">Remove-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Remove-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="4274d-138">Set-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="4274d-138">Set-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Set-AzureRmApiManagementOpenIdConnectProvider.md)


