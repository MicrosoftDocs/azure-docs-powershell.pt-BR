---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProvider.md
ms.openlocfilehash: fe23034b6fc86c9aa76629f806dcb406608f456c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93595684"
---
# <span data-ttu-id="516c9-101">Get-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="516c9-101">Get-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="516c9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="516c9-102">SYNOPSIS</span></span>
<span data-ttu-id="516c9-103">Obtenha os detalhes de configuração do provedor de identidade.</span><span class="sxs-lookup"><span data-stu-id="516c9-103">Get the identity provider configuration details.</span></span>

## <span data-ttu-id="516c9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="516c9-104">SYNTAX</span></span>

### <span data-ttu-id="516c9-105">AllIdentityProviders (padrão)</span><span class="sxs-lookup"><span data-stu-id="516c9-105">AllIdentityProviders (Default)</span></span>
```
Get-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="516c9-106">IdentityProviderByType</span><span class="sxs-lookup"><span data-stu-id="516c9-106">IdentityProviderByType</span></span>
```
Get-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="516c9-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="516c9-107">DESCRIPTION</span></span>
<span data-ttu-id="516c9-108">Obtenha os detalhes de configuração do provedor de identidade.</span><span class="sxs-lookup"><span data-stu-id="516c9-108">Get the identity provider configuration details.</span></span>

## <span data-ttu-id="516c9-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="516c9-109">EXAMPLES</span></span>

### <span data-ttu-id="516c9-110">Exemplo 1: obter todos os provedores de identidade</span><span class="sxs-lookup"><span data-stu-id="516c9-110">Example 1: Get all Identity Providers</span></span>

```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementIdentityProvider -Context $apimContext
```

<span data-ttu-id="516c9-111">Obter toda a configuração do provedor de identidade no serviço.</span><span class="sxs-lookup"><span data-stu-id="516c9-111">Get all the identity provider Configuration on the service.</span></span>

### <span data-ttu-id="516c9-112">Obter o provedor de identidade do tipo AAD</span><span class="sxs-lookup"><span data-stu-id="516c9-112">Get the AAD Type Identity Provider</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementIdentityProvider -Context $apimContext -Type Aad
```

<span data-ttu-id="516c9-113">Obtém a configuração do provedor de identidade do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="516c9-113">Gets the Identity Provider Configuration of Azure Active Directory.</span></span>

## <span data-ttu-id="516c9-114">OS</span><span class="sxs-lookup"><span data-stu-id="516c9-114">PARAMETERS</span></span>

### <span data-ttu-id="516c9-115">-Contexto</span><span class="sxs-lookup"><span data-stu-id="516c9-115">-Context</span></span>
<span data-ttu-id="516c9-116">Instância do PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="516c9-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="516c9-117">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="516c9-117">This parameter is required.</span></span>

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

### <span data-ttu-id="516c9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="516c9-118">-DefaultProfile</span></span>
<span data-ttu-id="516c9-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="516c9-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="516c9-120">-Digite</span><span class="sxs-lookup"><span data-stu-id="516c9-120">-Type</span></span>
<span data-ttu-id="516c9-121">Identificador de um provedor de identidade.</span><span class="sxs-lookup"><span data-stu-id="516c9-121">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="516c9-122">Se especificado, você tentará localizar a configuração do provedor de identidade pelo identificador.</span><span class="sxs-lookup"><span data-stu-id="516c9-122">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="516c9-123">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="516c9-123">This parameter is optional.</span></span>

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

### <span data-ttu-id="516c9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="516c9-124">CommonParameters</span></span>
<span data-ttu-id="516c9-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="516c9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="516c9-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="516c9-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="516c9-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="516c9-127">INPUTS</span></span>

### <span data-ttu-id="516c9-128">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="516c9-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="516c9-129">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="516c9-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

## <span data-ttu-id="516c9-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="516c9-130">OUTPUTS</span></span>

### <span data-ttu-id="516c9-131">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="516c9-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="516c9-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="516c9-132">NOTES</span></span>

## <span data-ttu-id="516c9-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="516c9-133">RELATED LINKS</span></span>
