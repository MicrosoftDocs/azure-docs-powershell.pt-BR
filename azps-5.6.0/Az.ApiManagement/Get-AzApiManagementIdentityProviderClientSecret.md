---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementidentityproviderclientsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProviderClientSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProviderClientSecret.md
ms.openlocfilehash: 94480eb224d9ef6cb4e4244fc863e79c39a8d23e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891237"
---
# <span data-ttu-id="8d856-101">Get-AzApiManagementIdentityProviderClientSecret</span><span class="sxs-lookup"><span data-stu-id="8d856-101">Get-AzApiManagementIdentityProviderClientSecret</span></span>

## <span data-ttu-id="8d856-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d856-102">SYNOPSIS</span></span>
<span data-ttu-id="8d856-103">Obter o segredo do cliente do provedor de identidade.</span><span class="sxs-lookup"><span data-stu-id="8d856-103">Get the identity provider client secret.</span></span>

## <span data-ttu-id="8d856-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="8d856-104">SYNTAX</span></span>

```
Get-AzApiManagementIdentityProviderClientSecret -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8d856-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="8d856-105">DESCRIPTION</span></span>
<span data-ttu-id="8d856-106">Obter o segredo do cliente do provedor de identidade.</span><span class="sxs-lookup"><span data-stu-id="8d856-106">Get the identity provider client secret.</span></span>

## <span data-ttu-id="8d856-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8d856-107">EXAMPLES</span></span>

### <span data-ttu-id="8d856-108">Exemplo 1: Obter o segredo do cliente do Provedor de Identidade de Tipo AAD</span><span class="sxs-lookup"><span data-stu-id="8d856-108">Example 1: Get the client secret of AAD Type Identity Provider</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Get-AzApiManagementIdentityProviderClientSecret -Context $apimContext -Type Aad
```

<span data-ttu-id="8d856-109">Obtém o segredo do cliente da Configuração do Provedor de Identidade do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="8d856-109">Gets the client secret of the Identity Provider Configuration of Azure Active Directory.</span></span>

## <span data-ttu-id="8d856-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="8d856-110">PARAMETERS</span></span>

### <span data-ttu-id="8d856-111">-Context</span><span class="sxs-lookup"><span data-stu-id="8d856-111">-Context</span></span>
<span data-ttu-id="8d856-112">Instância de PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="8d856-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="8d856-113">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="8d856-113">This parameter is required.</span></span>

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

### <span data-ttu-id="8d856-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d856-114">-DefaultProfile</span></span>
<span data-ttu-id="8d856-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8d856-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d856-116">-Type</span><span class="sxs-lookup"><span data-stu-id="8d856-116">-Type</span></span>
<span data-ttu-id="8d856-117">Identificador de um Provedor de Identidade.</span><span class="sxs-lookup"><span data-stu-id="8d856-117">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="8d856-118">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="8d856-118">This parameter is required.</span></span>

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

### <span data-ttu-id="8d856-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d856-119">CommonParameters</span></span>
<span data-ttu-id="8d856-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d856-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d856-121">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8d856-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d856-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8d856-122">INPUTS</span></span>

### <span data-ttu-id="8d856-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="8d856-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="8d856-124">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="8d856-124">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

## <span data-ttu-id="8d856-125">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="8d856-125">OUTPUTS</span></span>

### <span data-ttu-id="8d856-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientSecret</span><span class="sxs-lookup"><span data-stu-id="8d856-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientSecret</span></span>

## <span data-ttu-id="8d856-127">NOTES</span><span class="sxs-lookup"><span data-stu-id="8d856-127">NOTES</span></span>

## <span data-ttu-id="8d856-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8d856-128">RELATED LINKS</span></span>
