---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementIdentityProvider.md
ms.openlocfilehash: e25e3bfad6c40b136c3cbaa65999b8118e0abd11
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432515"
---
# <span data-ttu-id="3e72d-101">Get-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="3e72d-101">Get-AzureRmApiManagementIdentityProvider</span></span>

## <span data-ttu-id="3e72d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3e72d-102">SYNOPSIS</span></span>
<span data-ttu-id="3e72d-103">Obtenha os detalhes de configuração do provedor de identidade.</span><span class="sxs-lookup"><span data-stu-id="3e72d-103">Get the identity provider configuration details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3e72d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3e72d-104">SYNTAX</span></span>

### <span data-ttu-id="3e72d-105">AllIdentityProviders (padrão)</span><span class="sxs-lookup"><span data-stu-id="3e72d-105">AllIdentityProviders (Default)</span></span>
```
Get-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e72d-106">IdentityProviderByType</span><span class="sxs-lookup"><span data-stu-id="3e72d-106">IdentityProviderByType</span></span>
```
Get-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e72d-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3e72d-107">DESCRIPTION</span></span>
<span data-ttu-id="3e72d-108">Obtenha os detalhes de configuração do provedor de identidade.</span><span class="sxs-lookup"><span data-stu-id="3e72d-108">Get the identity provider configuration details.</span></span>

## <span data-ttu-id="3e72d-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3e72d-109">EXAMPLES</span></span>

### <span data-ttu-id="3e72d-110">Exemplo 1: obter todos os provedores de identidade</span><span class="sxs-lookup"><span data-stu-id="3e72d-110">Example 1: Get all Identity Providers</span></span>

```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementIdentityProvider -Context $apimContext
```

<span data-ttu-id="3e72d-111">Obter toda a configuração do provedor de identidade no serviço.</span><span class="sxs-lookup"><span data-stu-id="3e72d-111">Get all the identity provider Configuration on the service.</span></span>

### <span data-ttu-id="3e72d-112">Obter o provedor de identidade do tipo AAD</span><span class="sxs-lookup"><span data-stu-id="3e72d-112">Get the AAD Type Identity Provider</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementIdentityProvider -Context $apimContext -Type Aad
```

<span data-ttu-id="3e72d-113">Obtém a configuração do provedor de identidade do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="3e72d-113">Gets the Identity Provider Configuration of Azure Active Directory.</span></span>

## <span data-ttu-id="3e72d-114">OS</span><span class="sxs-lookup"><span data-stu-id="3e72d-114">PARAMETERS</span></span>

### <span data-ttu-id="3e72d-115">-Contexto</span><span class="sxs-lookup"><span data-stu-id="3e72d-115">-Context</span></span>
<span data-ttu-id="3e72d-116">Instância do PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="3e72d-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="3e72d-117">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="3e72d-117">This parameter is required.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e72d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e72d-118">-DefaultProfile</span></span>
<span data-ttu-id="3e72d-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3e72d-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e72d-120">-Digite</span><span class="sxs-lookup"><span data-stu-id="3e72d-120">-Type</span></span>
<span data-ttu-id="3e72d-121">Identificador de um provedor de identidade.</span><span class="sxs-lookup"><span data-stu-id="3e72d-121">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="3e72d-122">Se especificado, você tentará localizar a configuração do provedor de identidade pelo identificador.</span><span class="sxs-lookup"><span data-stu-id="3e72d-122">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="3e72d-123">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="3e72d-123">This parameter is optional.</span></span>

```yaml
Type: PsApiManagementIdentityProviderType
Parameter Sets: IdentityProviderByType
Aliases: 
Accepted values: Facebook, Google, Microsoft, Twitter, Aad

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e72d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e72d-124">CommonParameters</span></span>
<span data-ttu-id="3e72d-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e72d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e72d-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e72d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e72d-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3e72d-127">INPUTS</span></span>

### <span data-ttu-id="3e72d-128">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="3e72d-128">None</span></span>
<span data-ttu-id="3e72d-129">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="3e72d-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3e72d-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3e72d-130">OUTPUTS</span></span>

### <span data-ttu-id="3e72d-131">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="3e72d-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>
<span data-ttu-id="3e72d-132">Os detalhes do provedor de identidade configurados no serviço de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="3e72d-132">The details of the Identity Provider configured in API Management service.</span></span>

### <span data-ttu-id="3e72d-133">IList<Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementIdentityProvider></span><span class="sxs-lookup"><span data-stu-id="3e72d-133">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider></span></span>
<span data-ttu-id="3e72d-134">A lista de provedores de identidade configurados no serviço de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="3e72d-134">The list of Identity Providers configured in API Management service.</span></span>

## <span data-ttu-id="3e72d-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3e72d-135">NOTES</span></span>

## <span data-ttu-id="3e72d-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3e72d-136">RELATED LINKS</span></span>

