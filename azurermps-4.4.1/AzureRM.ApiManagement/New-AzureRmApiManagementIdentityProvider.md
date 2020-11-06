---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementIdentityProvider.md
ms.openlocfilehash: d6536c63ab3241e999c87dfb025205571c29596c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431223"
---
# <span data-ttu-id="fec90-101">New-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="fec90-101">New-AzureRmApiManagementIdentityProvider</span></span>

## <span data-ttu-id="fec90-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fec90-102">SYNOPSIS</span></span>
<span data-ttu-id="fec90-103">Cria uma nova configuração de provedor de identidade.</span><span class="sxs-lookup"><span data-stu-id="fec90-103">Creates a new Identity Provider configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fec90-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fec90-104">SYNTAX</span></span>

```
New-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> -ClientId <String> -ClientSecret <String>
 [-AllowedTenants <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fec90-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fec90-105">DESCRIPTION</span></span>
<span data-ttu-id="fec90-106">Cria uma nova configuração de provedor de identidade.</span><span class="sxs-lookup"><span data-stu-id="fec90-106">Creates a new Identity Provider configuration.</span></span>

## <span data-ttu-id="fec90-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fec90-107">EXAMPLES</span></span>

### <span data-ttu-id="fec90-108">Exemplo 1: configura o Facebook como um provedor de identidade para logons do portal do desenvolvedor</span><span class="sxs-lookup"><span data-stu-id="fec90-108">Example 1: Configures Facebook as an identity Provider for Developer Portal Logins</span></span>
```
New-AzureRmApiManagementIdentityProvider -Context $apimContext -Type 'Facebook' -ClientId 'sdfsfwerwerw' -ClientSecret 'sdgsdfgfst43tewfewrf'
```

<span data-ttu-id="fec90-109">Esse comando configura a identidade do Facebook como um provedor de identidade aceito no portal do desenvolvedor do serviço ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="fec90-109">This command configures Facebook Identity as a accepted Identity Provider on the Developer Portal of the ApiManagement service.</span></span>
<span data-ttu-id="fec90-110">Isso aceita como entrada de ClientId e ClientSecret do aplicativo Facebook.</span><span class="sxs-lookup"><span data-stu-id="fec90-110">This takes as input the ClientId and ClientSecret of the Facebook app.</span></span>

## <span data-ttu-id="fec90-111">OS</span><span class="sxs-lookup"><span data-stu-id="fec90-111">PARAMETERS</span></span>

### <span data-ttu-id="fec90-112">-AllowedTenants</span><span class="sxs-lookup"><span data-stu-id="fec90-112">-AllowedTenants</span></span>
<span data-ttu-id="fec90-113">Lista de locatários do Azure Active Directory permitidos</span><span class="sxs-lookup"><span data-stu-id="fec90-113">List of allowed Azure Active Directory Tenants</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fec90-114">-ClientId</span><span class="sxs-lookup"><span data-stu-id="fec90-114">-ClientId</span></span>
<span data-ttu-id="fec90-115">ID do cliente do aplicativo no provedor de identidade externa.</span><span class="sxs-lookup"><span data-stu-id="fec90-115">Client Id of the Application in the external Identity Provider.</span></span>
<span data-ttu-id="fec90-116">Ele é uma ID do aplicativo para o logon do Facebook, ID de cliente para o Google login, ID do aplicativo para a Microsoft.</span><span class="sxs-lookup"><span data-stu-id="fec90-116">It is App ID for Facebook login, Client ID for Google login, App ID for Microsoft.</span></span>

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

### <span data-ttu-id="fec90-117">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="fec90-117">-ClientSecret</span></span>
<span data-ttu-id="fec90-118">Segredo do cliente do aplicativo no provedor de identidade externa, usado para autenticar a solicitação de logon.</span><span class="sxs-lookup"><span data-stu-id="fec90-118">Client secret of the Application in external Identity Provider, used to authenticate login request.</span></span>
<span data-ttu-id="fec90-119">Por exemplo, é o segredo do aplicativo para o logon do Facebook, a chave de API do Google login, a chave pública para a Microsoft.</span><span class="sxs-lookup"><span data-stu-id="fec90-119">For example, it is App Secret for Facebook login, API Key for Google login, Public Key for Microsoft.</span></span>

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

### <span data-ttu-id="fec90-120">-Contexto</span><span class="sxs-lookup"><span data-stu-id="fec90-120">-Context</span></span>
<span data-ttu-id="fec90-121">Instância do PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="fec90-121">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="fec90-122">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="fec90-122">This parameter is required.</span></span>

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

### <span data-ttu-id="fec90-123">-Digite</span><span class="sxs-lookup"><span data-stu-id="fec90-123">-Type</span></span>
<span data-ttu-id="fec90-124">Identificador de um provedor de identidade.</span><span class="sxs-lookup"><span data-stu-id="fec90-124">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="fec90-125">Se especificado, você tentará localizar a configuração do provedor de identidade pelo identificador.</span><span class="sxs-lookup"><span data-stu-id="fec90-125">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="fec90-126">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="fec90-126">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType
Parameter Sets: (All)
Aliases: 
Accepted values: Facebook, Google, Microsoft, Twitter, Aad

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fec90-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="fec90-127">-Confirm</span></span>
<span data-ttu-id="fec90-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fec90-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fec90-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fec90-129">-WhatIf</span></span>
<span data-ttu-id="fec90-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fec90-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fec90-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fec90-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fec90-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fec90-132">-DefaultProfile</span></span>
<span data-ttu-id="fec90-133">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fec90-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fec90-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fec90-134">CommonParameters</span></span>
<span data-ttu-id="fec90-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fec90-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fec90-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fec90-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fec90-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fec90-137">INPUTS</span></span>

## <span data-ttu-id="fec90-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fec90-138">OUTPUTS</span></span>

### <span data-ttu-id="fec90-139">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="fec90-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="fec90-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fec90-140">NOTES</span></span>

## <span data-ttu-id="fec90-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fec90-141">RELATED LINKS</span></span>

[<span data-ttu-id="fec90-142">Get-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="fec90-142">Get-AzureRmApiManagementIdentityProvider</span></span>](./Get-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="fec90-143">Remove-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="fec90-143">Remove-AzureRmApiManagementIdentityProvider</span></span>](./Remove-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="fec90-144">Set-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="fec90-144">Set-AzureRmApiManagementIdentityProvider</span></span>](./Set-AzureRmApiManagementIdentityProvider.md)
