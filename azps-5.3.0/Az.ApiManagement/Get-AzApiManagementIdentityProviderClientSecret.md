---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementidentityproviderclientsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProviderClientSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProviderClientSecret.md
ms.openlocfilehash: d75d385bc158e0855601d3432dff79b2e4339f2f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98432724"
---
# <span data-ttu-id="2be2b-101">Get-AzApiManagementIdentityProviderClientSecret</span><span class="sxs-lookup"><span data-stu-id="2be2b-101">Get-AzApiManagementIdentityProviderClientSecret</span></span>

## <span data-ttu-id="2be2b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2be2b-102">SYNOPSIS</span></span>
<span data-ttu-id="2be2b-103">Obtenha o segredo do cliente do provedor de identidade.</span><span class="sxs-lookup"><span data-stu-id="2be2b-103">Get the identity provider client secret.</span></span>

## <span data-ttu-id="2be2b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2be2b-104">SYNTAX</span></span>

```
Get-AzApiManagementIdentityProviderClientSecret -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2be2b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2be2b-105">DESCRIPTION</span></span>
<span data-ttu-id="2be2b-106">Obtenha o segredo do cliente do provedor de identidade.</span><span class="sxs-lookup"><span data-stu-id="2be2b-106">Get the identity provider client secret.</span></span>

## <span data-ttu-id="2be2b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2be2b-107">EXAMPLES</span></span>

### <span data-ttu-id="2be2b-108">Exemplo 1: obter o segredo do cliente do provedor de identidade do tipo AAD</span><span class="sxs-lookup"><span data-stu-id="2be2b-108">Example 1: Get the client secret of AAD Type Identity Provider</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Get-AzApiManagementIdentityProviderClientSecret -Context $apimContext -Type Aad
```

<span data-ttu-id="2be2b-109">Obtém o segredo do cliente da configuração do provedor de identidade do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="2be2b-109">Gets the client secret of the Identity Provider Configuration of Azure Active Directory.</span></span>

## <span data-ttu-id="2be2b-110">OS</span><span class="sxs-lookup"><span data-stu-id="2be2b-110">PARAMETERS</span></span>

### <span data-ttu-id="2be2b-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="2be2b-111">-Context</span></span>
<span data-ttu-id="2be2b-112">Instância do PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="2be2b-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="2be2b-113">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="2be2b-113">This parameter is required.</span></span>

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

### <span data-ttu-id="2be2b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2be2b-114">-DefaultProfile</span></span>
<span data-ttu-id="2be2b-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2be2b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2be2b-116">-Digite</span><span class="sxs-lookup"><span data-stu-id="2be2b-116">-Type</span></span>
<span data-ttu-id="2be2b-117">Identificador de um provedor de identidade.</span><span class="sxs-lookup"><span data-stu-id="2be2b-117">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="2be2b-118">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="2be2b-118">This parameter is required.</span></span>

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

### <span data-ttu-id="2be2b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2be2b-119">CommonParameters</span></span>
<span data-ttu-id="2be2b-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2be2b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2be2b-121">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2be2b-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2be2b-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2be2b-122">INPUTS</span></span>

### <span data-ttu-id="2be2b-123">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="2be2b-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2be2b-124">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="2be2b-124">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

## <span data-ttu-id="2be2b-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2be2b-125">OUTPUTS</span></span>

### <span data-ttu-id="2be2b-126">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementClientSecret</span><span class="sxs-lookup"><span data-stu-id="2be2b-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientSecret</span></span>

## <span data-ttu-id="2be2b-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2be2b-127">NOTES</span></span>

## <span data-ttu-id="2be2b-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2be2b-128">RELATED LINKS</span></span>
