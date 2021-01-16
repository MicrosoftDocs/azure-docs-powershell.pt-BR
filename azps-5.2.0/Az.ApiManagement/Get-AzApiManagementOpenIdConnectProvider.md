---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 15B6EAE2-56ED-4A01-B8EA-52B9FCDC1F66
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: 6968b4ea1b222d0f046611f10e65f8073a4ba86a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98263457"
---
# <span data-ttu-id="bb031-101">Get-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="bb031-101">Get-AzApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="bb031-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bb031-102">SYNOPSIS</span></span>
<span data-ttu-id="bb031-103">Obtém provedores do OpenID Connect.</span><span class="sxs-lookup"><span data-stu-id="bb031-103">Gets OpenID Connect providers.</span></span>

## <span data-ttu-id="bb031-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bb031-104">SYNTAX</span></span>

### <span data-ttu-id="bb031-105">GetAllOpenIdConnectProviders (padrão)</span><span class="sxs-lookup"><span data-stu-id="bb031-105">GetAllOpenIdConnectProviders (Default)</span></span>
```
Get-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bb031-106">GetByOpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="bb031-106">GetByOpenIdConnectProviderId</span></span>
```
Get-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-OpenIdConnectProviderId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bb031-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="bb031-107">GetByName</span></span>
```
Get-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb031-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bb031-108">DESCRIPTION</span></span>
<span data-ttu-id="bb031-109">O cmdlet **Get-AzApiManagementOpenIdConnectProvider** Obtém provedores de conexão OpenID no gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="bb031-109">The **Get-AzApiManagementOpenIdConnectProvider** cmdlet gets OpenID Connect providers in Azure API Management.</span></span>
<span data-ttu-id="bb031-110">O ClientSecret não será incluído nos detalhes do resultado.</span><span class="sxs-lookup"><span data-stu-id="bb031-110">ClientSecret will not be included into result details.</span></span> <span data-ttu-id="bb031-111">Para obter o segredo do cliente, use **Get-AzApiManagementOpenIdConnectProviderClientSecret**.</span><span class="sxs-lookup"><span data-stu-id="bb031-111">To get client secret, use **Get-AzApiManagementOpenIdConnectProviderClientSecret**.</span></span>

## <span data-ttu-id="bb031-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bb031-112">EXAMPLES</span></span>

### <span data-ttu-id="bb031-113">Exemplo 1: obter todos os provedores</span><span class="sxs-lookup"><span data-stu-id="bb031-113">Example 1: Get all providers</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProvider -Context $apimContext
```

<span data-ttu-id="bb031-114">Este comando obtém todos os provedores do OpenID Connect para o contexto especificado.</span><span class="sxs-lookup"><span data-stu-id="bb031-114">This command gets all OpenID Connect providers for the specified context.</span></span>

### <span data-ttu-id="bb031-115">Exemplo 2: obter um provedor usando uma ID</span><span class="sxs-lookup"><span data-stu-id="bb031-115">Example 2: Get a provider by using an ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvider01"
```

<span data-ttu-id="bb031-116">Esse comando obtém o provedor com a ID OICProvider01.</span><span class="sxs-lookup"><span data-stu-id="bb031-116">This command gets the provider that has the ID OICProvider01.</span></span>

### <span data-ttu-id="bb031-117">Exemplo 3: obter um provedor usando um nome</span><span class="sxs-lookup"><span data-stu-id="bb031-117">Example 3: Get a provider by using a name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProvider -Context $apimContext -Name "Contoso OpenID Connect Provider"
```

<span data-ttu-id="bb031-118">Esse comando obtém o provedor chamado provedor de conexão de OpenID do contoso.</span><span class="sxs-lookup"><span data-stu-id="bb031-118">This command gets the provider named Contoso OpenID Connect Provider.</span></span>

## <span data-ttu-id="bb031-119">OS</span><span class="sxs-lookup"><span data-stu-id="bb031-119">PARAMETERS</span></span>

### <span data-ttu-id="bb031-120">-Contexto</span><span class="sxs-lookup"><span data-stu-id="bb031-120">-Context</span></span>
<span data-ttu-id="bb031-121">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="bb031-121">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="bb031-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb031-122">-DefaultProfile</span></span>
<span data-ttu-id="bb031-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bb031-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bb031-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="bb031-124">-Name</span></span>
<span data-ttu-id="bb031-125">Especifica um nome amigável de um provedor.</span><span class="sxs-lookup"><span data-stu-id="bb031-125">Specifies a friendly name of a provider.</span></span>
<span data-ttu-id="bb031-126">Se você especificar um nome, esse cmdlet obterá esse provedor.</span><span class="sxs-lookup"><span data-stu-id="bb031-126">If you specify a name, this cmdlet gets that provider.</span></span>

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

### <span data-ttu-id="bb031-127">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="bb031-127">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="bb031-128">Especifica uma ID do provedor que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="bb031-128">Specifies an ID of the provider that this cmdlet removes.</span></span>
<span data-ttu-id="bb031-129">Se você especificar uma ID, esse cmdlet obterá esse provedor.</span><span class="sxs-lookup"><span data-stu-id="bb031-129">If you specify an ID, this cmdlet gets that provider.</span></span>

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

### <span data-ttu-id="bb031-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb031-130">CommonParameters</span></span>
<span data-ttu-id="bb031-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb031-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb031-132">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bb031-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb031-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bb031-133">INPUTS</span></span>

### <span data-ttu-id="bb031-134">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="bb031-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="bb031-135">System. String</span><span class="sxs-lookup"><span data-stu-id="bb031-135">System.String</span></span>

## <span data-ttu-id="bb031-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bb031-136">OUTPUTS</span></span>

### <span data-ttu-id="bb031-137">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="bb031-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="bb031-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bb031-138">NOTES</span></span>

## <span data-ttu-id="bb031-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bb031-139">RELATED LINKS</span></span>

[<span data-ttu-id="bb031-140">New-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="bb031-140">New-AzApiManagementOpenIdConnectProvider</span></span>](./New-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="bb031-141">Remove-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="bb031-141">Remove-AzApiManagementOpenIdConnectProvider</span></span>](./Remove-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="bb031-142">Set-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="bb031-142">Set-AzApiManagementOpenIdConnectProvider</span></span>](./Set-AzApiManagementOpenIdConnectProvider.md)


