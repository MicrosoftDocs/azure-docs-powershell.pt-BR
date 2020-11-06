---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 15B6EAE2-56ED-4A01-B8EA-52B9FCDC1F66
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: cdc1341296349897b1ccc2e27785c3cd48360ddb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598102"
---
# <span data-ttu-id="eb439-101">Get-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="eb439-101">Get-AzApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="eb439-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="eb439-102">SYNOPSIS</span></span>
<span data-ttu-id="eb439-103">Obtém provedores do OpenID Connect.</span><span class="sxs-lookup"><span data-stu-id="eb439-103">Gets OpenID Connect providers.</span></span>

## <span data-ttu-id="eb439-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="eb439-104">SYNTAX</span></span>

### <span data-ttu-id="eb439-105">GetAllOpenIdConnectProviders (padrão)</span><span class="sxs-lookup"><span data-stu-id="eb439-105">GetAllOpenIdConnectProviders (Default)</span></span>
```
Get-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eb439-106">GetByOpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="eb439-106">GetByOpenIdConnectProviderId</span></span>
```
Get-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-OpenIdConnectProviderId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eb439-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="eb439-107">GetByName</span></span>
```
Get-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eb439-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="eb439-108">DESCRIPTION</span></span>
<span data-ttu-id="eb439-109">O cmdlet **Get-AzApiManagementOpenIdConnectProvider** Obtém provedores de conexão OpenID no gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="eb439-109">The **Get-AzApiManagementOpenIdConnectProvider** cmdlet gets OpenID Connect providers in Azure API Management.</span></span>

## <span data-ttu-id="eb439-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="eb439-110">EXAMPLES</span></span>

### <span data-ttu-id="eb439-111">Exemplo 1: obter todos os provedores</span><span class="sxs-lookup"><span data-stu-id="eb439-111">Example 1: Get all providers</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProvider -Context $apimContext
```

<span data-ttu-id="eb439-112">Este comando obtém todos os provedores do OpenID Connect para o contexto especificado.</span><span class="sxs-lookup"><span data-stu-id="eb439-112">This command gets all OpenID Connect providers for the specified context.</span></span>

### <span data-ttu-id="eb439-113">Exemplo 2: obter um provedor usando uma ID</span><span class="sxs-lookup"><span data-stu-id="eb439-113">Example 2: Get a provider by using an ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvider01"
```

<span data-ttu-id="eb439-114">Esse comando obtém o provedor com a ID OICProvider01.</span><span class="sxs-lookup"><span data-stu-id="eb439-114">This command gets the provider that has the ID OICProvider01.</span></span>

### <span data-ttu-id="eb439-115">Exemplo 3: obter um provedor usando um nome</span><span class="sxs-lookup"><span data-stu-id="eb439-115">Example 3: Get a provider by using a name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProvider -Context $apimContext -Name "Contoso OpenID Connect Provider"
```

<span data-ttu-id="eb439-116">Esse comando obtém o provedor chamado provedor de conexão de OpenID do contoso.</span><span class="sxs-lookup"><span data-stu-id="eb439-116">This command gets the provider named Contoso OpenID Connect Provider.</span></span>

## <span data-ttu-id="eb439-117">OS</span><span class="sxs-lookup"><span data-stu-id="eb439-117">PARAMETERS</span></span>

### <span data-ttu-id="eb439-118">-Contexto</span><span class="sxs-lookup"><span data-stu-id="eb439-118">-Context</span></span>
<span data-ttu-id="eb439-119">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="eb439-119">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="eb439-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb439-120">-DefaultProfile</span></span>
<span data-ttu-id="eb439-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="eb439-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eb439-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="eb439-122">-Name</span></span>
<span data-ttu-id="eb439-123">Especifica um nome amigável de um provedor.</span><span class="sxs-lookup"><span data-stu-id="eb439-123">Specifies a friendly name of a provider.</span></span>
<span data-ttu-id="eb439-124">Se você especificar um nome, esse cmdlet obterá esse provedor.</span><span class="sxs-lookup"><span data-stu-id="eb439-124">If you specify a name, this cmdlet gets that provider.</span></span>

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

### <span data-ttu-id="eb439-125">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="eb439-125">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="eb439-126">Especifica uma ID do provedor que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="eb439-126">Specifies an ID of the provider that this cmdlet removes.</span></span>
<span data-ttu-id="eb439-127">Se você especificar uma ID, esse cmdlet obterá esse provedor.</span><span class="sxs-lookup"><span data-stu-id="eb439-127">If you specify an ID, this cmdlet gets that provider.</span></span>

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

### <span data-ttu-id="eb439-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb439-128">CommonParameters</span></span>
<span data-ttu-id="eb439-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb439-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb439-130">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eb439-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb439-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="eb439-131">INPUTS</span></span>

### <span data-ttu-id="eb439-132">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="eb439-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="eb439-133">System. String</span><span class="sxs-lookup"><span data-stu-id="eb439-133">System.String</span></span>

## <span data-ttu-id="eb439-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="eb439-134">OUTPUTS</span></span>

### <span data-ttu-id="eb439-135">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="eb439-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="eb439-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="eb439-136">NOTES</span></span>

## <span data-ttu-id="eb439-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="eb439-137">RELATED LINKS</span></span>

[<span data-ttu-id="eb439-138">New-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="eb439-138">New-AzApiManagementOpenIdConnectProvider</span></span>](./New-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="eb439-139">Remove-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="eb439-139">Remove-AzApiManagementOpenIdConnectProvider</span></span>](./Remove-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="eb439-140">Set-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="eb439-140">Set-AzApiManagementOpenIdConnectProvider</span></span>](./Set-AzApiManagementOpenIdConnectProvider.md)


