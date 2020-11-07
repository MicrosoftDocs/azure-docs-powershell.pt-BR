---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProvider.md
ms.openlocfilehash: 75525d3c77c3e2113c0e3cff5a7741ab916d7485
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941933"
---
# <span data-ttu-id="f421a-101">Get-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="f421a-101">Get-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="f421a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f421a-102">SYNOPSIS</span></span>
<span data-ttu-id="f421a-103">Obtenha os detalhes de configuração do provedor de identidade.</span><span class="sxs-lookup"><span data-stu-id="f421a-103">Get the identity provider configuration details.</span></span>

## <span data-ttu-id="f421a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f421a-104">SYNTAX</span></span>

### <span data-ttu-id="f421a-105">AllIdentityProviders (padrão)</span><span class="sxs-lookup"><span data-stu-id="f421a-105">AllIdentityProviders (Default)</span></span>
```
Get-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f421a-106">IdentityProviderByType</span><span class="sxs-lookup"><span data-stu-id="f421a-106">IdentityProviderByType</span></span>
```
Get-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f421a-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f421a-107">DESCRIPTION</span></span>
<span data-ttu-id="f421a-108">Obtenha os detalhes de configuração do provedor de identidade.</span><span class="sxs-lookup"><span data-stu-id="f421a-108">Get the identity provider configuration details.</span></span>

## <span data-ttu-id="f421a-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f421a-109">EXAMPLES</span></span>

### <span data-ttu-id="f421a-110">Exemplo 1: obter todos os provedores de identidade</span><span class="sxs-lookup"><span data-stu-id="f421a-110">Example 1: Get all Identity Providers</span></span>

```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementIdentityProvider -Context $apimContext
```

<span data-ttu-id="f421a-111">Obter toda a configuração do provedor de identidade no serviço.</span><span class="sxs-lookup"><span data-stu-id="f421a-111">Get all the identity provider Configuration on the service.</span></span>

### <span data-ttu-id="f421a-112">Exemplo 2: obter o provedor de identidade do tipo AAD</span><span class="sxs-lookup"><span data-stu-id="f421a-112">Example 2: Get the AAD Type Identity Provider</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Get-AzApiManagementIdentityProvider -Context $apimContext -Type Aad


Type                     : Aad
ClientId                 : aaa
ClientSecret             : xxxxx
AllowedTenants           : {contosotest.onmicrosoft.com}
Authority                : login.microsoftonline.com
SignupPolicyName         :
SigninPolicyName         :
ProfileEditingPolicyName :
PasswordResetPolicyName  :
SigninTenant             :
Id                       : /subscriptions/a200340d-6b82-494d-9dbf-687ba6e33f9e/resourceGroups/Api-Default-West-US/providers/Microsoft.ApiManagement/service/contoso/identityProviders/Aad
ResourceGroupName        : Api-Default-West-US
ServiceName              : contoso
```

<span data-ttu-id="f421a-113">Obtém a configuração do provedor de identidade do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f421a-113">Gets the Identity Provider Configuration of Azure Active Directory.</span></span>

### <span data-ttu-id="f421a-114">Exemplo 3: obter o provedor de identidade do tipo de B2C do AAD</span><span class="sxs-lookup"><span data-stu-id="f421a-114">Example 3: Get the AAD B2C Type Identity Provider</span></span>
```powershell
PS C:\>$context = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Get-AzApiManagementIdentityProvider -Context $context -Type AadB2C


Type                     : AadB2C
ClientId                 : f02dafe2-b8b8-48ec-a38e-27e5c16c51e5
ClientSecret             : xxxxxx
AllowedTenants           : {contosoaadb2c.onmicrosoft.com}
Authority                : login.microsoftonline.com
SignupPolicyName         : B2C_1_policy-signup
SigninPolicyName         : B2C_1_policy-signin
ProfileEditingPolicyName :
PasswordResetPolicyName  :
SigninTenant             : contosoaadb2c.onmicrosoft.com
Id                       : /subscriptions/a200340d-6b82-494d-9dbf-687ba6e33f9e/resourceGroups/Api-Default-West-US/providers/Microsoft.ApiManagement/service/contoso/identityProviders/AadB2C
ResourceGroupName        : Api-Default-West-US
ServiceName              : contoso
```

<span data-ttu-id="f421a-115">Obtém a configuração do provedor de identidade do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f421a-115">Gets the Identity Provider Configuration of Azure Active Directory.</span></span>

## <span data-ttu-id="f421a-116">OS</span><span class="sxs-lookup"><span data-stu-id="f421a-116">PARAMETERS</span></span>

### <span data-ttu-id="f421a-117">-Contexto</span><span class="sxs-lookup"><span data-stu-id="f421a-117">-Context</span></span>
<span data-ttu-id="f421a-118">Instância do PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="f421a-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="f421a-119">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="f421a-119">This parameter is required.</span></span>

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

### <span data-ttu-id="f421a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f421a-120">-DefaultProfile</span></span>
<span data-ttu-id="f421a-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f421a-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f421a-122">-Digite</span><span class="sxs-lookup"><span data-stu-id="f421a-122">-Type</span></span>
<span data-ttu-id="f421a-123">Identificador de um provedor de identidade.</span><span class="sxs-lookup"><span data-stu-id="f421a-123">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="f421a-124">Se especificado, você tentará localizar a configuração do provedor de identidade pelo identificador.</span><span class="sxs-lookup"><span data-stu-id="f421a-124">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="f421a-125">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="f421a-125">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType
Parameter Sets: IdentityProviderByType
Aliases:
Accepted values: Facebook, Google, Microsoft, Twitter, Aad, AadB2C

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f421a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f421a-126">CommonParameters</span></span>
<span data-ttu-id="f421a-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f421a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f421a-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f421a-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f421a-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f421a-129">INPUTS</span></span>

### <span data-ttu-id="f421a-130">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="f421a-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f421a-131">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="f421a-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

## <span data-ttu-id="f421a-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f421a-132">OUTPUTS</span></span>

### <span data-ttu-id="f421a-133">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="f421a-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="f421a-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f421a-134">NOTES</span></span>

## <span data-ttu-id="f421a-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f421a-135">RELATED LINKS</span></span>
