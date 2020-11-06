---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 15B6EAE2-56ED-4A01-B8EA-52B9FCDC1F66
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: d97090f6374890d9ae7ba24e53d6e1d60430f7b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427043"
---
# <span data-ttu-id="d402b-101">Get-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="d402b-101">Get-AzureRmApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="d402b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d402b-102">SYNOPSIS</span></span>
<span data-ttu-id="d402b-103">Obtém provedores do OpenID Connect.</span><span class="sxs-lookup"><span data-stu-id="d402b-103">Gets OpenID Connect providers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d402b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d402b-104">SYNTAX</span></span>

### <span data-ttu-id="d402b-105">Obter todos os provedores do OpenID Connect (padrão)</span><span class="sxs-lookup"><span data-stu-id="d402b-105">Get all OpenID Connect Providers (Default)</span></span>
```
Get-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d402b-106">Obter ID do provedor do OpenID Connect</span><span class="sxs-lookup"><span data-stu-id="d402b-106">Get by OpenID Connect Provider ID</span></span>
```
Get-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-OpenIdConnectProviderId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d402b-107">Localizar pelo nome amigável do provedor de conexão OpenID</span><span class="sxs-lookup"><span data-stu-id="d402b-107">Find by OpenID Connect Provider friendly Name</span></span>
```
Get-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d402b-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d402b-108">DESCRIPTION</span></span>
<span data-ttu-id="d402b-109">O cmdlet **Get-AzureRmApiManagementOpenIdConnectProvider** Obtém provedores de conexão OpenID no gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="d402b-109">The **Get-AzureRmApiManagementOpenIdConnectProvider** cmdlet gets OpenID Connect providers in Azure API Management.</span></span>

## <span data-ttu-id="d402b-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d402b-110">EXAMPLES</span></span>

### <span data-ttu-id="d402b-111">Exemplo 1: obter todos os provedores</span><span class="sxs-lookup"><span data-stu-id="d402b-111">Example 1: Get all providers</span></span>
```
PS C:\>Get-AzureRmApiManagementOpenIdConnectProvider -Context $ApimContext
```

<span data-ttu-id="d402b-112">Este comando obtém todos os provedores do OpenID Connect para o contexto especificado.</span><span class="sxs-lookup"><span data-stu-id="d402b-112">This command gets all OpenID Connect providers for the specified context.</span></span>

### <span data-ttu-id="d402b-113">Exemplo 2: obter um provedor usando uma ID</span><span class="sxs-lookup"><span data-stu-id="d402b-113">Example 2: Get a provider by using an ID</span></span>
```
PS C:\>Get-AzureRmApiManagementOpenIdConnectProvider -Context $ApimContext -OpenIdConnectProviderId "OICProvicer01"
```

<span data-ttu-id="d402b-114">Esse comando obtém o provedor com a ID OICProvicer01.</span><span class="sxs-lookup"><span data-stu-id="d402b-114">This command gets the provider that has the ID OICProvicer01.</span></span>

### <span data-ttu-id="d402b-115">Exemplo 3: obter um provedor usando um nome</span><span class="sxs-lookup"><span data-stu-id="d402b-115">Example 3: Get a provider by using a name</span></span>
```
PS C:\>Get-AzureRmApiManagementOpenIdConnectProvider -Context $ApimContext -Name "Contoso OpenID Connect Provider"
```

<span data-ttu-id="d402b-116">Esse comando obtém o provedor chamado provedor de conexão de OpenID do contoso.</span><span class="sxs-lookup"><span data-stu-id="d402b-116">This command gets the provider named Contoso OpenID Connect Provider.</span></span>

## <span data-ttu-id="d402b-117">OS</span><span class="sxs-lookup"><span data-stu-id="d402b-117">PARAMETERS</span></span>

### <span data-ttu-id="d402b-118">-Contexto</span><span class="sxs-lookup"><span data-stu-id="d402b-118">-Context</span></span>
<span data-ttu-id="d402b-119">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="d402b-119">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="d402b-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="d402b-120">-Name</span></span>
<span data-ttu-id="d402b-121">Especifica um nome amigável de um provedor.</span><span class="sxs-lookup"><span data-stu-id="d402b-121">Specifies a friendly name of a provider.</span></span>
<span data-ttu-id="d402b-122">Se você especificar um nome, esse cmdlet obterá esse provedor.</span><span class="sxs-lookup"><span data-stu-id="d402b-122">If you specify a name, this cmdlet gets that provider.</span></span>

```yaml
Type: System.String
Parameter Sets: Find by OpenID Connect Provider friendly Name
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d402b-123">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="d402b-123">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="d402b-124">Especifica uma ID do provedor que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="d402b-124">Specifies an ID of the provider that this cmdlet removes.</span></span>
<span data-ttu-id="d402b-125">Se você especificar uma ID, esse cmdlet obterá esse provedor.</span><span class="sxs-lookup"><span data-stu-id="d402b-125">If you specify an ID, this cmdlet gets that provider.</span></span>

```yaml
Type: System.String
Parameter Sets: Get by OpenID Connect Provider ID
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d402b-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d402b-126">-DefaultProfile</span></span>
<span data-ttu-id="d402b-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d402b-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d402b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d402b-128">CommonParameters</span></span>
<span data-ttu-id="d402b-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d402b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d402b-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d402b-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d402b-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d402b-131">INPUTS</span></span>

## <span data-ttu-id="d402b-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d402b-132">OUTPUTS</span></span>

### <span data-ttu-id="d402b-133">IList<Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementOpenIdConnectProvider></span><span class="sxs-lookup"><span data-stu-id="d402b-133">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider></span></span>

## <span data-ttu-id="d402b-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d402b-134">NOTES</span></span>

## <span data-ttu-id="d402b-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d402b-135">RELATED LINKS</span></span>

[<span data-ttu-id="d402b-136">New-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="d402b-136">New-AzureRmApiManagementOpenIdConnectProvider</span></span>](./New-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="d402b-137">Remove-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="d402b-137">Remove-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Remove-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="d402b-138">Set-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="d402b-138">Set-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Set-AzureRmApiManagementOpenIdConnectProvider.md)


