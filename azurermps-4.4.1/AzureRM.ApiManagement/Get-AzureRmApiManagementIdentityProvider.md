---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementIdentityProvider.md
ms.openlocfilehash: 2b38728f90de4639bf3e125f226ae2b40527ca45
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431256"
---
# <span data-ttu-id="62cad-101">Get-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="62cad-101">Get-AzureRmApiManagementIdentityProvider</span></span>

## <span data-ttu-id="62cad-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="62cad-102">SYNOPSIS</span></span>
<span data-ttu-id="62cad-103">Obtenha os detalhes de configuração do provedor de identidade.</span><span class="sxs-lookup"><span data-stu-id="62cad-103">Get the identity provider configuration details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="62cad-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="62cad-104">SYNTAX</span></span>

### <span data-ttu-id="62cad-105">AllIdentityProviders (padrão)</span><span class="sxs-lookup"><span data-stu-id="62cad-105">AllIdentityProviders (Default)</span></span>
```
Get-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="62cad-106">IdentityProviderByType</span><span class="sxs-lookup"><span data-stu-id="62cad-106">IdentityProviderByType</span></span>
```
Get-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62cad-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="62cad-107">DESCRIPTION</span></span>
<span data-ttu-id="62cad-108">Obtenha os detalhes de configuração do provedor de identidade.</span><span class="sxs-lookup"><span data-stu-id="62cad-108">Get the identity provider configuration details.</span></span>

## <span data-ttu-id="62cad-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="62cad-109">EXAMPLES</span></span>

### <span data-ttu-id="62cad-110">--------------------------Exemplo 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="62cad-110">--------------------------  Example 1  --------------------------</span></span>
<span data-ttu-id="62cad-111">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="62cad-111">@{paragraph=PS C:\\\>}</span></span>







```
Get-AzureRmApiManagementIdentityProvider -Context $context
```

<span data-ttu-id="62cad-112">Obter toda a configuração do provedor de identidade no serviço.</span><span class="sxs-lookup"><span data-stu-id="62cad-112">Get all the identity provider Configuration on the service.</span></span>

### <span data-ttu-id="62cad-113">--------------------------Exemplo 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="62cad-113">--------------------------  Example 2  --------------------------</span></span>
<span data-ttu-id="62cad-114">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="62cad-114">@{paragraph=PS C:\\\>}</span></span>







```
Get-AzureRmApiManagementIdentityProvider -Context $context -Type Aad
```

<span data-ttu-id="62cad-115">Obtém a configuração do provedor de identidade do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="62cad-115">Gets the Identity Provider Configuration of Azure Active Directory.</span></span>

## <span data-ttu-id="62cad-116">OS</span><span class="sxs-lookup"><span data-stu-id="62cad-116">PARAMETERS</span></span>

### <span data-ttu-id="62cad-117">-Contexto</span><span class="sxs-lookup"><span data-stu-id="62cad-117">-Context</span></span>
<span data-ttu-id="62cad-118">Instância do PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="62cad-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="62cad-119">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="62cad-119">This parameter is required.</span></span>

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

### <span data-ttu-id="62cad-120">-Digite</span><span class="sxs-lookup"><span data-stu-id="62cad-120">-Type</span></span>
<span data-ttu-id="62cad-121">Identificador de um provedor de identidade.</span><span class="sxs-lookup"><span data-stu-id="62cad-121">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="62cad-122">Se especificado, você tentará localizar a configuração do provedor de identidade pelo identificador.</span><span class="sxs-lookup"><span data-stu-id="62cad-122">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="62cad-123">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="62cad-123">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType
Parameter Sets: IdentityProviderByType
Aliases: 
Accepted values: Facebook, Google, Microsoft, Twitter, Aad

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62cad-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62cad-124">-DefaultProfile</span></span>
<span data-ttu-id="62cad-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="62cad-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="62cad-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62cad-126">CommonParameters</span></span>
<span data-ttu-id="62cad-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62cad-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62cad-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62cad-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62cad-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="62cad-129">INPUTS</span></span>

## <span data-ttu-id="62cad-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="62cad-130">OUTPUTS</span></span>

### <span data-ttu-id="62cad-131">IList<Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementIdentityProvider></span><span class="sxs-lookup"><span data-stu-id="62cad-131">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider></span></span>

### <span data-ttu-id="62cad-132">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="62cad-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="62cad-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="62cad-133">NOTES</span></span>

## <span data-ttu-id="62cad-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="62cad-134">RELATED LINKS</span></span>

