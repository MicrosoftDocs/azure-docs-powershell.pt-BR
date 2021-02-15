---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementidentityproviderclientsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProviderClientSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProviderClientSecret.md
ms.openlocfilehash: d75d385bc158e0855601d3432dff79b2e4339f2f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118071"
---
# <span data-ttu-id="42b4e-101">Get-AzApiManagementIdentityProviderClientSecret</span><span class="sxs-lookup"><span data-stu-id="42b4e-101">Get-AzApiManagementIdentityProviderClientSecret</span></span>

## <span data-ttu-id="42b4e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="42b4e-102">SYNOPSIS</span></span>
<span data-ttu-id="42b4e-103">Obter o segredo do cliente do provedor de identidade.</span><span class="sxs-lookup"><span data-stu-id="42b4e-103">Get the identity provider client secret.</span></span>

## <span data-ttu-id="42b4e-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="42b4e-104">SYNTAX</span></span>

```
Get-AzApiManagementIdentityProviderClientSecret -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="42b4e-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="42b4e-105">DESCRIPTION</span></span>
<span data-ttu-id="42b4e-106">Obter o segredo do cliente do provedor de identidade.</span><span class="sxs-lookup"><span data-stu-id="42b4e-106">Get the identity provider client secret.</span></span>

## <span data-ttu-id="42b4e-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="42b4e-107">EXAMPLES</span></span>

### <span data-ttu-id="42b4e-108">Exemplo 1: Obter o segredo do cliente do Provedor de Identidade de Tipo AAD</span><span class="sxs-lookup"><span data-stu-id="42b4e-108">Example 1: Get the client secret of AAD Type Identity Provider</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Get-AzApiManagementIdentityProviderClientSecret -Context $apimContext -Type Aad
```

<span data-ttu-id="42b4e-109">Obtém o segredo do cliente da Configuração do Provedor de Identidade do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="42b4e-109">Gets the client secret of the Identity Provider Configuration of Azure Active Directory.</span></span>

## <span data-ttu-id="42b4e-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="42b4e-110">PARAMETERS</span></span>

### <span data-ttu-id="42b4e-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="42b4e-111">-Context</span></span>
<span data-ttu-id="42b4e-112">Instância de PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="42b4e-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="42b4e-113">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="42b4e-113">This parameter is required.</span></span>

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

### <span data-ttu-id="42b4e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42b4e-114">-DefaultProfile</span></span>
<span data-ttu-id="42b4e-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="42b4e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42b4e-116">-Tipo</span><span class="sxs-lookup"><span data-stu-id="42b4e-116">-Type</span></span>
<span data-ttu-id="42b4e-117">Identificador de um Provedor de Identidade.</span><span class="sxs-lookup"><span data-stu-id="42b4e-117">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="42b4e-118">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="42b4e-118">This parameter is required.</span></span>

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

### <span data-ttu-id="42b4e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42b4e-119">CommonParameters</span></span>
<span data-ttu-id="42b4e-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42b4e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42b4e-121">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="42b4e-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42b4e-122">Entradas</span><span class="sxs-lookup"><span data-stu-id="42b4e-122">INPUTS</span></span>

### <span data-ttu-id="42b4e-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="42b4e-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="42b4e-124">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="42b4e-124">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

## <span data-ttu-id="42b4e-125">Saídas</span><span class="sxs-lookup"><span data-stu-id="42b4e-125">OUTPUTS</span></span>

### <span data-ttu-id="42b4e-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientSec limited</span><span class="sxs-lookup"><span data-stu-id="42b4e-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientSecret</span></span>

## <span data-ttu-id="42b4e-127">Notas</span><span class="sxs-lookup"><span data-stu-id="42b4e-127">NOTES</span></span>

## <span data-ttu-id="42b4e-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="42b4e-128">RELATED LINKS</span></span>
