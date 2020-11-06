---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 15B6EAE2-56ED-4A01-B8EA-52B9FCDC1F66
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: 0ffe2dfbd1ccbb05ef1ad828861e1d439373caa9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426519"
---
# <span data-ttu-id="b462e-101">Get-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="b462e-101">Get-AzureRmApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="b462e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b462e-102">SYNOPSIS</span></span>
<span data-ttu-id="b462e-103">Obtém provedores do OpenID Connect.</span><span class="sxs-lookup"><span data-stu-id="b462e-103">Gets OpenID Connect providers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b462e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b462e-104">SYNTAX</span></span>

### <span data-ttu-id="b462e-105">GetAllOpenIdConnectProviders (padrão)</span><span class="sxs-lookup"><span data-stu-id="b462e-105">GetAllOpenIdConnectProviders (Default)</span></span>
```
Get-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b462e-106">GetByOpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="b462e-106">GetByOpenIdConnectProviderId</span></span>
```
Get-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-OpenIdConnectProviderId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b462e-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="b462e-107">GetByName</span></span>
```
Get-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b462e-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b462e-108">DESCRIPTION</span></span>
<span data-ttu-id="b462e-109">O cmdlet **Get-AzureRmApiManagementOpenIdConnectProvider** Obtém provedores de conexão OpenID no gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="b462e-109">The **Get-AzureRmApiManagementOpenIdConnectProvider** cmdlet gets OpenID Connect providers in Azure API Management.</span></span>

## <span data-ttu-id="b462e-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b462e-110">EXAMPLES</span></span>

### <span data-ttu-id="b462e-111">Exemplo 1: obter todos os provedores</span><span class="sxs-lookup"><span data-stu-id="b462e-111">Example 1: Get all providers</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementOpenIdConnectProvider -Context $apimContext
```

<span data-ttu-id="b462e-112">Este comando obtém todos os provedores do OpenID Connect para o contexto especificado.</span><span class="sxs-lookup"><span data-stu-id="b462e-112">This command gets all OpenID Connect providers for the specified context.</span></span>

### <span data-ttu-id="b462e-113">Exemplo 2: obter um provedor usando uma ID</span><span class="sxs-lookup"><span data-stu-id="b462e-113">Example 2: Get a provider by using an ID</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvicer01"
```

<span data-ttu-id="b462e-114">Esse comando obtém o provedor com a ID OICProvicer01.</span><span class="sxs-lookup"><span data-stu-id="b462e-114">This command gets the provider that has the ID OICProvicer01.</span></span>

### <span data-ttu-id="b462e-115">Exemplo 3: obter um provedor usando um nome</span><span class="sxs-lookup"><span data-stu-id="b462e-115">Example 3: Get a provider by using a name</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementOpenIdConnectProvider -Context $apimContext -Name "Contoso OpenID Connect Provider"
```

<span data-ttu-id="b462e-116">Esse comando obtém o provedor chamado provedor de conexão de OpenID do contoso.</span><span class="sxs-lookup"><span data-stu-id="b462e-116">This command gets the provider named Contoso OpenID Connect Provider.</span></span>

## <span data-ttu-id="b462e-117">OS</span><span class="sxs-lookup"><span data-stu-id="b462e-117">PARAMETERS</span></span>

### <span data-ttu-id="b462e-118">-Contexto</span><span class="sxs-lookup"><span data-stu-id="b462e-118">-Context</span></span>
<span data-ttu-id="b462e-119">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="b462e-119">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="b462e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b462e-120">-DefaultProfile</span></span>
<span data-ttu-id="b462e-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b462e-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b462e-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="b462e-122">-Name</span></span>
<span data-ttu-id="b462e-123">Especifica um nome amigável de um provedor.</span><span class="sxs-lookup"><span data-stu-id="b462e-123">Specifies a friendly name of a provider.</span></span>
<span data-ttu-id="b462e-124">Se você especificar um nome, esse cmdlet obterá esse provedor.</span><span class="sxs-lookup"><span data-stu-id="b462e-124">If you specify a name, this cmdlet gets that provider.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b462e-125">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="b462e-125">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="b462e-126">Especifica uma ID do provedor que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="b462e-126">Specifies an ID of the provider that this cmdlet removes.</span></span>
<span data-ttu-id="b462e-127">Se você especificar uma ID, esse cmdlet obterá esse provedor.</span><span class="sxs-lookup"><span data-stu-id="b462e-127">If you specify an ID, this cmdlet gets that provider.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByOpenIdConnectProviderId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b462e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b462e-128">CommonParameters</span></span>
<span data-ttu-id="b462e-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b462e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b462e-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b462e-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b462e-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b462e-131">INPUTS</span></span>

### <span data-ttu-id="b462e-132">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b462e-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b462e-133">System. String</span><span class="sxs-lookup"><span data-stu-id="b462e-133">System.String</span></span>

## <span data-ttu-id="b462e-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b462e-134">OUTPUTS</span></span>

### <span data-ttu-id="b462e-135">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="b462e-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="b462e-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b462e-136">NOTES</span></span>

## <span data-ttu-id="b462e-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b462e-137">RELATED LINKS</span></span>

[<span data-ttu-id="b462e-138">New-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="b462e-138">New-AzureRmApiManagementOpenIdConnectProvider</span></span>](./New-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="b462e-139">Remove-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="b462e-139">Remove-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Remove-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="b462e-140">Set-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="b462e-140">Set-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Set-AzureRmApiManagementOpenIdConnectProvider.md)


