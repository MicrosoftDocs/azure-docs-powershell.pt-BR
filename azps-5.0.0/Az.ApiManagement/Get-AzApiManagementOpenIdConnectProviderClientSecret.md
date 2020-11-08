---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementopenidconnectproviderclientsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProviderClientSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProviderClientSecret.md
ms.openlocfilehash: dcc66b6d28157ff9d5551e2fdf0cab18f7727828
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94116942"
---
# <span data-ttu-id="6de60-101">Get-AzApiManagementOpenIdConnectProviderClientSecret</span><span class="sxs-lookup"><span data-stu-id="6de60-101">Get-AzApiManagementOpenIdConnectProviderClientSecret</span></span>

## <span data-ttu-id="6de60-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6de60-102">SYNOPSIS</span></span>
<span data-ttu-id="6de60-103">Obtém segredo do cliente do provedor do OpenID Connect.</span><span class="sxs-lookup"><span data-stu-id="6de60-103">Gets OpenID Connect provider client secret.</span></span>

## <span data-ttu-id="6de60-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6de60-104">SYNTAX</span></span>

```
Get-AzApiManagementOpenIdConnectProviderClientSecret -Context <PsApiManagementContext>
 -OpenIdConnectProviderId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6de60-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6de60-105">DESCRIPTION</span></span>
<span data-ttu-id="6de60-106">Obtém segredo do cliente do provedor do OpenID Connect.</span><span class="sxs-lookup"><span data-stu-id="6de60-106">Gets OpenID Connect provider client secret.</span></span>

## <span data-ttu-id="6de60-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6de60-107">EXAMPLES</span></span>

### <span data-ttu-id="6de60-108">Exemplo 1: obter um segredo de cliente de provedor usando uma ID</span><span class="sxs-lookup"><span data-stu-id="6de60-108">Example 1: Get a provider client secret by using an ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProviderClientSecret -Context $apimContext -OpenIdConnectProviderId "OICProvider01"
```

<span data-ttu-id="6de60-109">Esse comando obtém um segredo do cliente do provedor que tem a ID OICProvider01.</span><span class="sxs-lookup"><span data-stu-id="6de60-109">This command gets a client secret of the provider that has the ID OICProvider01.</span></span>

## <span data-ttu-id="6de60-110">OS</span><span class="sxs-lookup"><span data-stu-id="6de60-110">PARAMETERS</span></span>

### <span data-ttu-id="6de60-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="6de60-111">-Context</span></span>
<span data-ttu-id="6de60-112">Instância do PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="6de60-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="6de60-113">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="6de60-113">This parameter is required.</span></span>

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

### <span data-ttu-id="6de60-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6de60-114">-DefaultProfile</span></span>
<span data-ttu-id="6de60-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6de60-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6de60-116">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="6de60-116">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="6de60-117">Identificador de um provedor de conexão OpenID.</span><span class="sxs-lookup"><span data-stu-id="6de60-117">Identifier of a OpenID Connect Provider.</span></span>
<span data-ttu-id="6de60-118">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="6de60-118">This parameter is required.</span></span>

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

### <span data-ttu-id="6de60-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6de60-119">CommonParameters</span></span>
<span data-ttu-id="6de60-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6de60-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6de60-121">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6de60-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6de60-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6de60-122">INPUTS</span></span>

### <span data-ttu-id="6de60-123">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="6de60-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="6de60-124">System. String</span><span class="sxs-lookup"><span data-stu-id="6de60-124">System.String</span></span>

## <span data-ttu-id="6de60-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6de60-125">OUTPUTS</span></span>

### <span data-ttu-id="6de60-126">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementClientSecret</span><span class="sxs-lookup"><span data-stu-id="6de60-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientSecret</span></span>

## <span data-ttu-id="6de60-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6de60-127">NOTES</span></span>

## <span data-ttu-id="6de60-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6de60-128">RELATED LINKS</span></span>
