---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 15B6EAE2-56ED-4A01-B8EA-52B9FCDC1F66
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: 1a46cccc38e1b562786e9eda88f3336430559fc0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901373"
---
# <span data-ttu-id="877dd-101">Get-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="877dd-101">Get-AzApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="877dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="877dd-102">SYNOPSIS</span></span>
<span data-ttu-id="877dd-103">Obtém provedores do OpenID Connect.</span><span class="sxs-lookup"><span data-stu-id="877dd-103">Gets OpenID Connect providers.</span></span>

## <span data-ttu-id="877dd-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="877dd-104">SYNTAX</span></span>

### <span data-ttu-id="877dd-105">GetAllOpenIdConnectProviders (Padrão)</span><span class="sxs-lookup"><span data-stu-id="877dd-105">GetAllOpenIdConnectProviders (Default)</span></span>
```
Get-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="877dd-106">GetByOpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="877dd-106">GetByOpenIdConnectProviderId</span></span>
```
Get-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-OpenIdConnectProviderId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="877dd-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="877dd-107">GetByName</span></span>
```
Get-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="877dd-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="877dd-108">DESCRIPTION</span></span>
<span data-ttu-id="877dd-109">O cmdlet **Get-AzApiManagementOpenIdConnectProvider** obtém provedores do OpenID Connect no Gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="877dd-109">The **Get-AzApiManagementOpenIdConnectProvider** cmdlet gets OpenID Connect providers in Azure API Management.</span></span>
<span data-ttu-id="877dd-110">ClientSecret não será incluído nos detalhes do resultado.</span><span class="sxs-lookup"><span data-stu-id="877dd-110">ClientSecret will not be included into result details.</span></span> <span data-ttu-id="877dd-111">Para obter o segredo do cliente, use **Get-AzApiManagementOpenIdConnectProviderClientSecret**.</span><span class="sxs-lookup"><span data-stu-id="877dd-111">To get client secret, use **Get-AzApiManagementOpenIdConnectProviderClientSecret**.</span></span>

## <span data-ttu-id="877dd-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="877dd-112">EXAMPLES</span></span>

### <span data-ttu-id="877dd-113">Exemplo 1: Obter todos os provedores</span><span class="sxs-lookup"><span data-stu-id="877dd-113">Example 1: Get all providers</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProvider -Context $apimContext
```

<span data-ttu-id="877dd-114">Esse comando obtém todos os provedores do OpenID Connect para o contexto especificado.</span><span class="sxs-lookup"><span data-stu-id="877dd-114">This command gets all OpenID Connect providers for the specified context.</span></span>

### <span data-ttu-id="877dd-115">Exemplo 2: Obter um provedor usando uma ID</span><span class="sxs-lookup"><span data-stu-id="877dd-115">Example 2: Get a provider by using an ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvider01"
```

<span data-ttu-id="877dd-116">Este comando obtém o provedor que tem a ID OICProvider01.</span><span class="sxs-lookup"><span data-stu-id="877dd-116">This command gets the provider that has the ID OICProvider01.</span></span>

### <span data-ttu-id="877dd-117">Exemplo 3: Obter um provedor usando um nome</span><span class="sxs-lookup"><span data-stu-id="877dd-117">Example 3: Get a provider by using a name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProvider -Context $apimContext -Name "Contoso OpenID Connect Provider"
```

<span data-ttu-id="877dd-118">Este comando obtém o provedor chamado Contoso OpenID Connect Provider.</span><span class="sxs-lookup"><span data-stu-id="877dd-118">This command gets the provider named Contoso OpenID Connect Provider.</span></span>

## <span data-ttu-id="877dd-119">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="877dd-119">PARAMETERS</span></span>

### <span data-ttu-id="877dd-120">-Context</span><span class="sxs-lookup"><span data-stu-id="877dd-120">-Context</span></span>
<span data-ttu-id="877dd-121">Especifica um **objeto PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="877dd-121">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="877dd-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="877dd-122">-DefaultProfile</span></span>
<span data-ttu-id="877dd-123">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="877dd-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="877dd-124">-Name</span><span class="sxs-lookup"><span data-stu-id="877dd-124">-Name</span></span>
<span data-ttu-id="877dd-125">Especifica um nome amigável de um provedor.</span><span class="sxs-lookup"><span data-stu-id="877dd-125">Specifies a friendly name of a provider.</span></span>
<span data-ttu-id="877dd-126">Se você especificar um nome, esse cmdlet obtém esse provedor.</span><span class="sxs-lookup"><span data-stu-id="877dd-126">If you specify a name, this cmdlet gets that provider.</span></span>

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

### <span data-ttu-id="877dd-127">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="877dd-127">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="877dd-128">Especifica uma ID do provedor que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="877dd-128">Specifies an ID of the provider that this cmdlet removes.</span></span>
<span data-ttu-id="877dd-129">Se você especificar uma ID, esse cmdlet obtém esse provedor.</span><span class="sxs-lookup"><span data-stu-id="877dd-129">If you specify an ID, this cmdlet gets that provider.</span></span>

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

### <span data-ttu-id="877dd-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="877dd-130">CommonParameters</span></span>
<span data-ttu-id="877dd-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="877dd-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="877dd-132">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="877dd-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="877dd-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="877dd-133">INPUTS</span></span>

### <span data-ttu-id="877dd-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="877dd-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="877dd-135">System.String</span><span class="sxs-lookup"><span data-stu-id="877dd-135">System.String</span></span>

## <span data-ttu-id="877dd-136">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="877dd-136">OUTPUTS</span></span>

### <span data-ttu-id="877dd-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="877dd-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="877dd-138">NOTES</span><span class="sxs-lookup"><span data-stu-id="877dd-138">NOTES</span></span>

## <span data-ttu-id="877dd-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="877dd-139">RELATED LINKS</span></span>

[<span data-ttu-id="877dd-140">New-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="877dd-140">New-AzApiManagementOpenIdConnectProvider</span></span>](./New-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="877dd-141">Remove-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="877dd-141">Remove-AzApiManagementOpenIdConnectProvider</span></span>](./Remove-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="877dd-142">Set-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="877dd-142">Set-AzApiManagementOpenIdConnectProvider</span></span>](./Set-AzApiManagementOpenIdConnectProvider.md)


