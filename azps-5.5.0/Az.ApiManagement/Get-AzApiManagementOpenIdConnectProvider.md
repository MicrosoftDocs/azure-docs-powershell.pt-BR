---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 15B6EAE2-56ED-4A01-B8EA-52B9FCDC1F66
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: 6968b4ea1b222d0f046611f10e65f8073a4ba86a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114846"
---
# <span data-ttu-id="57e77-101">Get-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="57e77-101">Get-AzApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="57e77-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="57e77-102">SYNOPSIS</span></span>
<span data-ttu-id="57e77-103">Obtém provedores do OpenID Connect.</span><span class="sxs-lookup"><span data-stu-id="57e77-103">Gets OpenID Connect providers.</span></span>

## <span data-ttu-id="57e77-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="57e77-104">SYNTAX</span></span>

### <span data-ttu-id="57e77-105">GetAllOpenIdConnectProviders (Padrão)</span><span class="sxs-lookup"><span data-stu-id="57e77-105">GetAllOpenIdConnectProviders (Default)</span></span>
```
Get-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="57e77-106">GetByOpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="57e77-106">GetByOpenIdConnectProviderId</span></span>
```
Get-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-OpenIdConnectProviderId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="57e77-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="57e77-107">GetByName</span></span>
```
Get-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="57e77-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="57e77-108">DESCRIPTION</span></span>
<span data-ttu-id="57e77-109">O cmdlet **Get-AzApiManagementOpenIdConnectProvider obtém** provedores do OpenID Connect no Gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="57e77-109">The **Get-AzApiManagementOpenIdConnectProvider** cmdlet gets OpenID Connect providers in Azure API Management.</span></span>
<span data-ttu-id="57e77-110">ClientSec ltd não será incluído nos detalhes do resultado.</span><span class="sxs-lookup"><span data-stu-id="57e77-110">ClientSecret will not be included into result details.</span></span> <span data-ttu-id="57e77-111">Para obter o segredo do cliente, use **Get-AzApiManagementOpenIdConnectProviderClientSecsec.**</span><span class="sxs-lookup"><span data-stu-id="57e77-111">To get client secret, use **Get-AzApiManagementOpenIdConnectProviderClientSecret**.</span></span>

## <span data-ttu-id="57e77-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="57e77-112">EXAMPLES</span></span>

### <span data-ttu-id="57e77-113">Exemplo 1: Obter todos os provedores</span><span class="sxs-lookup"><span data-stu-id="57e77-113">Example 1: Get all providers</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProvider -Context $apimContext
```

<span data-ttu-id="57e77-114">Esse comando obtém todos os provedores do OpenID Connect para o contexto especificado.</span><span class="sxs-lookup"><span data-stu-id="57e77-114">This command gets all OpenID Connect providers for the specified context.</span></span>

### <span data-ttu-id="57e77-115">Exemplo 2: Obter um provedor usando uma ID</span><span class="sxs-lookup"><span data-stu-id="57e77-115">Example 2: Get a provider by using an ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvider01"
```

<span data-ttu-id="57e77-116">Esse comando obtém o provedor que tem a ID OICProvider01.</span><span class="sxs-lookup"><span data-stu-id="57e77-116">This command gets the provider that has the ID OICProvider01.</span></span>

### <span data-ttu-id="57e77-117">Exemplo 3: Obter um provedor usando um nome</span><span class="sxs-lookup"><span data-stu-id="57e77-117">Example 3: Get a provider by using a name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProvider -Context $apimContext -Name "Contoso OpenID Connect Provider"
```

<span data-ttu-id="57e77-118">Esse comando obtém o provedor chamado Provedor de Conexão OpenID da Contoso.</span><span class="sxs-lookup"><span data-stu-id="57e77-118">This command gets the provider named Contoso OpenID Connect Provider.</span></span>

## <span data-ttu-id="57e77-119">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="57e77-119">PARAMETERS</span></span>

### <span data-ttu-id="57e77-120">-Contexto</span><span class="sxs-lookup"><span data-stu-id="57e77-120">-Context</span></span>
<span data-ttu-id="57e77-121">Especifica um **objeto PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="57e77-121">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="57e77-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57e77-122">-DefaultProfile</span></span>
<span data-ttu-id="57e77-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="57e77-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="57e77-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="57e77-124">-Name</span></span>
<span data-ttu-id="57e77-125">Especifica um nome amigável de um provedor.</span><span class="sxs-lookup"><span data-stu-id="57e77-125">Specifies a friendly name of a provider.</span></span>
<span data-ttu-id="57e77-126">Se você especificar um nome, este cmdlet obtém esse provedor.</span><span class="sxs-lookup"><span data-stu-id="57e77-126">If you specify a name, this cmdlet gets that provider.</span></span>

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

### <span data-ttu-id="57e77-127">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="57e77-127">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="57e77-128">Especifica uma ID do provedor que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="57e77-128">Specifies an ID of the provider that this cmdlet removes.</span></span>
<span data-ttu-id="57e77-129">Se você especificar uma ID, esse cmdlet obtém esse provedor.</span><span class="sxs-lookup"><span data-stu-id="57e77-129">If you specify an ID, this cmdlet gets that provider.</span></span>

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

### <span data-ttu-id="57e77-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57e77-130">CommonParameters</span></span>
<span data-ttu-id="57e77-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57e77-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57e77-132">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="57e77-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57e77-133">Entradas</span><span class="sxs-lookup"><span data-stu-id="57e77-133">INPUTS</span></span>

### <span data-ttu-id="57e77-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="57e77-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="57e77-135">System.String</span><span class="sxs-lookup"><span data-stu-id="57e77-135">System.String</span></span>

## <span data-ttu-id="57e77-136">Saídas</span><span class="sxs-lookup"><span data-stu-id="57e77-136">OUTPUTS</span></span>

### <span data-ttu-id="57e77-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="57e77-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="57e77-138">Notas</span><span class="sxs-lookup"><span data-stu-id="57e77-138">NOTES</span></span>

## <span data-ttu-id="57e77-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="57e77-139">RELATED LINKS</span></span>

[<span data-ttu-id="57e77-140">New-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="57e77-140">New-AzApiManagementOpenIdConnectProvider</span></span>](./New-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="57e77-141">Remove-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="57e77-141">Remove-AzApiManagementOpenIdConnectProvider</span></span>](./Remove-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="57e77-142">Set-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="57e77-142">Set-AzApiManagementOpenIdConnectProvider</span></span>](./Set-AzApiManagementOpenIdConnectProvider.md)


