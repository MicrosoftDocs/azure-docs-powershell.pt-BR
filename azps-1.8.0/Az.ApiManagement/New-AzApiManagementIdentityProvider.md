---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementIdentityProvider.md
ms.openlocfilehash: c0730053dce60dbf556ef00f522aa463ffb26601
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93601671"
---
# <span data-ttu-id="995f7-101">New-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="995f7-101">New-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="995f7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="995f7-102">SYNOPSIS</span></span>
<span data-ttu-id="995f7-103">Cria uma nova configuração de provedor de identidade.</span><span class="sxs-lookup"><span data-stu-id="995f7-103">Creates a new Identity Provider configuration.</span></span>

## <span data-ttu-id="995f7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="995f7-104">SYNTAX</span></span>

```
New-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> -ClientId <String> -ClientSecret <String>
 [-AllowedTenants <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="995f7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="995f7-105">DESCRIPTION</span></span>
<span data-ttu-id="995f7-106">Cria uma nova configuração de provedor de identidade.</span><span class="sxs-lookup"><span data-stu-id="995f7-106">Creates a new Identity Provider configuration.</span></span>

## <span data-ttu-id="995f7-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="995f7-107">EXAMPLES</span></span>

### <span data-ttu-id="995f7-108">Exemplo 1: configura o Facebook como um provedor de identidade para logons do portal do desenvolvedor</span><span class="sxs-lookup"><span data-stu-id="995f7-108">Example 1: Configures Facebook as an identity Provider for Developer Portal Logins</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementIdentityProvider -Context $apimContext -Type 'Facebook' -ClientId 'sdfsfwerwerw' -ClientSecret 'sdgsdfgfst43tewfewrf'
```

<span data-ttu-id="995f7-109">Esse comando configura a identidade do Facebook como um provedor de identidade aceito no portal do desenvolvedor do serviço ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="995f7-109">This command configures Facebook Identity as a accepted Identity Provider on the Developer Portal of the ApiManagement service.</span></span>
<span data-ttu-id="995f7-110">Isso aceita como entrada de ClientId e ClientSecret do aplicativo Facebook.</span><span class="sxs-lookup"><span data-stu-id="995f7-110">This takes as input the ClientId and ClientSecret of the Facebook app.</span></span>

## <span data-ttu-id="995f7-111">OS</span><span class="sxs-lookup"><span data-stu-id="995f7-111">PARAMETERS</span></span>

### <span data-ttu-id="995f7-112">-AllowedTenants</span><span class="sxs-lookup"><span data-stu-id="995f7-112">-AllowedTenants</span></span>
<span data-ttu-id="995f7-113">Lista de locatários do Azure Active Directory permitidos</span><span class="sxs-lookup"><span data-stu-id="995f7-113">List of allowed Azure Active Directory Tenants</span></span>

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

### <span data-ttu-id="995f7-114">-ClientId</span><span class="sxs-lookup"><span data-stu-id="995f7-114">-ClientId</span></span>
<span data-ttu-id="995f7-115">ID do cliente do aplicativo no provedor de identidade externa.</span><span class="sxs-lookup"><span data-stu-id="995f7-115">Client Id of the Application in the external Identity Provider.</span></span>
<span data-ttu-id="995f7-116">Ele é uma ID do aplicativo para o logon do Facebook, ID de cliente para o Google login, ID do aplicativo para a Microsoft.</span><span class="sxs-lookup"><span data-stu-id="995f7-116">It is App ID for Facebook login, Client ID for Google login, App ID for Microsoft.</span></span>

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

### <span data-ttu-id="995f7-117">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="995f7-117">-ClientSecret</span></span>
<span data-ttu-id="995f7-118">Segredo do cliente do aplicativo no provedor de identidade externa, usado para autenticar a solicitação de logon.</span><span class="sxs-lookup"><span data-stu-id="995f7-118">Client secret of the Application in external Identity Provider, used to authenticate login request.</span></span>
<span data-ttu-id="995f7-119">Por exemplo, é o segredo do aplicativo para o logon do Facebook, a chave de API do Google login, a chave pública para a Microsoft.</span><span class="sxs-lookup"><span data-stu-id="995f7-119">For example, it is App Secret for Facebook login, API Key for Google login, Public Key for Microsoft.</span></span>

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

### <span data-ttu-id="995f7-120">-Contexto</span><span class="sxs-lookup"><span data-stu-id="995f7-120">-Context</span></span>
<span data-ttu-id="995f7-121">Instância do PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="995f7-121">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="995f7-122">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="995f7-122">This parameter is required.</span></span>

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

### <span data-ttu-id="995f7-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="995f7-123">-DefaultProfile</span></span>
<span data-ttu-id="995f7-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="995f7-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="995f7-125">-Digite</span><span class="sxs-lookup"><span data-stu-id="995f7-125">-Type</span></span>
<span data-ttu-id="995f7-126">Identificador de um provedor de identidade.</span><span class="sxs-lookup"><span data-stu-id="995f7-126">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="995f7-127">Se especificado, você tentará localizar a configuração do provedor de identidade pelo identificador.</span><span class="sxs-lookup"><span data-stu-id="995f7-127">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="995f7-128">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="995f7-128">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType
Parameter Sets: (All)
Aliases:
Accepted values: Facebook, Google, Microsoft, Twitter, Aad, AadB2C

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="995f7-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="995f7-129">-Confirm</span></span>
<span data-ttu-id="995f7-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="995f7-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="995f7-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="995f7-131">-WhatIf</span></span>
<span data-ttu-id="995f7-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="995f7-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="995f7-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="995f7-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="995f7-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="995f7-134">CommonParameters</span></span>
<span data-ttu-id="995f7-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="995f7-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="995f7-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="995f7-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="995f7-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="995f7-137">INPUTS</span></span>

### <span data-ttu-id="995f7-138">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="995f7-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="995f7-139">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="995f7-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

### <span data-ttu-id="995f7-140">System. String</span><span class="sxs-lookup"><span data-stu-id="995f7-140">System.String</span></span>

### <span data-ttu-id="995f7-141">System. String []</span><span class="sxs-lookup"><span data-stu-id="995f7-141">System.String[]</span></span>

## <span data-ttu-id="995f7-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="995f7-142">OUTPUTS</span></span>

### <span data-ttu-id="995f7-143">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="995f7-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="995f7-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="995f7-144">NOTES</span></span>

## <span data-ttu-id="995f7-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="995f7-145">RELATED LINKS</span></span>

[<span data-ttu-id="995f7-146">Get-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="995f7-146">Get-AzApiManagementIdentityProvider</span></span>](./Get-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="995f7-147">Remove-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="995f7-147">Remove-AzApiManagementIdentityProvider</span></span>](./Remove-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="995f7-148">Set-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="995f7-148">Set-AzApiManagementIdentityProvider</span></span>](./Set-AzApiManagementIdentityProvider.md)
