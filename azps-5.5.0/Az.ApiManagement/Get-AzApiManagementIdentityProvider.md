---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProvider.md
ms.openlocfilehash: b267fc854127c1cb098481ac483a7572c8b2e12f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118074"
---
# <span data-ttu-id="0142d-101">Get-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="0142d-101">Get-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="0142d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0142d-102">SYNOPSIS</span></span>
<span data-ttu-id="0142d-103">Obter os detalhes de configuração do provedor de identidade.</span><span class="sxs-lookup"><span data-stu-id="0142d-103">Get the identity provider configuration details.</span></span>

## <span data-ttu-id="0142d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0142d-104">SYNTAX</span></span>

### <span data-ttu-id="0142d-105">AllIdentityProviders (Padrão)</span><span class="sxs-lookup"><span data-stu-id="0142d-105">AllIdentityProviders (Default)</span></span>
```
Get-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0142d-106">IdentityProviderByType</span><span class="sxs-lookup"><span data-stu-id="0142d-106">IdentityProviderByType</span></span>
```
Get-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0142d-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="0142d-107">DESCRIPTION</span></span>
<span data-ttu-id="0142d-108">Obter os detalhes de configuração do provedor de identidade.</span><span class="sxs-lookup"><span data-stu-id="0142d-108">Get the identity provider configuration details.</span></span>
<span data-ttu-id="0142d-109">ClientSec ltd não será incluído nos detalhes do resultado.</span><span class="sxs-lookup"><span data-stu-id="0142d-109">ClientSecret will not be included into result details.</span></span> <span data-ttu-id="0142d-110">Para obter o segredo do cliente, use **Get-AzApiManagementIdentityProviderClientSecsec.**</span><span class="sxs-lookup"><span data-stu-id="0142d-110">To get client secret, use **Get-AzApiManagementIdentityProviderClientSecret**.</span></span>

## <span data-ttu-id="0142d-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0142d-111">EXAMPLES</span></span>

### <span data-ttu-id="0142d-112">Exemplo 1: Obter todos os Provedores de Identidade</span><span class="sxs-lookup"><span data-stu-id="0142d-112">Example 1: Get all Identity Providers</span></span>

```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementIdentityProvider -Context $apimContext
```

<span data-ttu-id="0142d-113">Obter todas as configurações do provedor de identidade no serviço.</span><span class="sxs-lookup"><span data-stu-id="0142d-113">Get all the identity provider Configuration on the service.</span></span>

### <span data-ttu-id="0142d-114">Exemplo 2: Obter o Provedor de Identidade de Tipo AAD</span><span class="sxs-lookup"><span data-stu-id="0142d-114">Example 2: Get the AAD Type Identity Provider</span></span>
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

<span data-ttu-id="0142d-115">Obtém a Configuração do Provedor de Identidade do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="0142d-115">Gets the Identity Provider Configuration of Azure Active Directory.</span></span>

### <span data-ttu-id="0142d-116">Exemplo 3: Obter o Provedor de Identidade de Tipo B2C do AAD</span><span class="sxs-lookup"><span data-stu-id="0142d-116">Example 3: Get the AAD B2C Type Identity Provider</span></span>
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

<span data-ttu-id="0142d-117">Obtém a Configuração do Provedor de Identidade do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="0142d-117">Gets the Identity Provider Configuration of Azure Active Directory.</span></span>

## <span data-ttu-id="0142d-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0142d-118">PARAMETERS</span></span>

### <span data-ttu-id="0142d-119">-Contexto</span><span class="sxs-lookup"><span data-stu-id="0142d-119">-Context</span></span>
<span data-ttu-id="0142d-120">Instância de PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="0142d-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="0142d-121">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="0142d-121">This parameter is required.</span></span>

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

### <span data-ttu-id="0142d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0142d-122">-DefaultProfile</span></span>
<span data-ttu-id="0142d-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="0142d-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0142d-124">-Tipo</span><span class="sxs-lookup"><span data-stu-id="0142d-124">-Type</span></span>
<span data-ttu-id="0142d-125">Identificador de um Provedor de Identidade.</span><span class="sxs-lookup"><span data-stu-id="0142d-125">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="0142d-126">Se especificado, você tentará encontrar a configuração do provedor de identidade pelo identificador.</span><span class="sxs-lookup"><span data-stu-id="0142d-126">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="0142d-127">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="0142d-127">This parameter is optional.</span></span>

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

### <span data-ttu-id="0142d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0142d-128">CommonParameters</span></span>
<span data-ttu-id="0142d-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0142d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0142d-130">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0142d-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0142d-131">Entradas</span><span class="sxs-lookup"><span data-stu-id="0142d-131">INPUTS</span></span>

### <span data-ttu-id="0142d-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="0142d-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="0142d-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="0142d-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

## <span data-ttu-id="0142d-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="0142d-134">OUTPUTS</span></span>

### <span data-ttu-id="0142d-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="0142d-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="0142d-136">Notas</span><span class="sxs-lookup"><span data-stu-id="0142d-136">NOTES</span></span>

## <span data-ttu-id="0142d-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0142d-137">RELATED LINKS</span></span>
