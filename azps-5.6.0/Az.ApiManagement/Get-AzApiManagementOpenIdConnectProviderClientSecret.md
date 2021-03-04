---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementopenidconnectproviderclientsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProviderClientSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProviderClientSecret.md
ms.openlocfilehash: 0c6757b32a81c689b4b9bbc3397fdd52c19ae4bc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901371"
---
# <span data-ttu-id="937d0-101">Get-AzApiManagementOpenIdConnectProviderClientSecret</span><span class="sxs-lookup"><span data-stu-id="937d0-101">Get-AzApiManagementOpenIdConnectProviderClientSecret</span></span>

## <span data-ttu-id="937d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="937d0-102">SYNOPSIS</span></span>
<span data-ttu-id="937d0-103">Obtém o segredo do cliente do provedor do OpenID Connect.</span><span class="sxs-lookup"><span data-stu-id="937d0-103">Gets OpenID Connect provider client secret.</span></span>

## <span data-ttu-id="937d0-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="937d0-104">SYNTAX</span></span>

```
Get-AzApiManagementOpenIdConnectProviderClientSecret -Context <PsApiManagementContext>
 -OpenIdConnectProviderId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="937d0-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="937d0-105">DESCRIPTION</span></span>
<span data-ttu-id="937d0-106">Obtém o segredo do cliente do provedor do OpenID Connect.</span><span class="sxs-lookup"><span data-stu-id="937d0-106">Gets OpenID Connect provider client secret.</span></span>

## <span data-ttu-id="937d0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="937d0-107">EXAMPLES</span></span>

### <span data-ttu-id="937d0-108">Exemplo 1: Obter um segredo do cliente do provedor usando uma ID</span><span class="sxs-lookup"><span data-stu-id="937d0-108">Example 1: Get a provider client secret by using an ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProviderClientSecret -Context $apimContext -OpenIdConnectProviderId "OICProvider01"
```

<span data-ttu-id="937d0-109">Este comando obtém um segredo do cliente do provedor que tem a ID OICProvider01.</span><span class="sxs-lookup"><span data-stu-id="937d0-109">This command gets a client secret of the provider that has the ID OICProvider01.</span></span>

## <span data-ttu-id="937d0-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="937d0-110">PARAMETERS</span></span>

### <span data-ttu-id="937d0-111">-Context</span><span class="sxs-lookup"><span data-stu-id="937d0-111">-Context</span></span>
<span data-ttu-id="937d0-112">Instância de PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="937d0-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="937d0-113">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="937d0-113">This parameter is required.</span></span>

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

### <span data-ttu-id="937d0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="937d0-114">-DefaultProfile</span></span>
<span data-ttu-id="937d0-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="937d0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="937d0-116">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="937d0-116">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="937d0-117">Identificador de um Provedor de Conexão OpenID.</span><span class="sxs-lookup"><span data-stu-id="937d0-117">Identifier of a OpenID Connect Provider.</span></span>
<span data-ttu-id="937d0-118">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="937d0-118">This parameter is required.</span></span>

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

### <span data-ttu-id="937d0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="937d0-119">CommonParameters</span></span>
<span data-ttu-id="937d0-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="937d0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="937d0-121">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="937d0-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="937d0-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="937d0-122">INPUTS</span></span>

### <span data-ttu-id="937d0-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="937d0-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="937d0-124">System.String</span><span class="sxs-lookup"><span data-stu-id="937d0-124">System.String</span></span>

## <span data-ttu-id="937d0-125">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="937d0-125">OUTPUTS</span></span>

### <span data-ttu-id="937d0-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientSecret</span><span class="sxs-lookup"><span data-stu-id="937d0-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientSecret</span></span>

## <span data-ttu-id="937d0-127">NOTES</span><span class="sxs-lookup"><span data-stu-id="937d0-127">NOTES</span></span>

## <span data-ttu-id="937d0-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="937d0-128">RELATED LINKS</span></span>
