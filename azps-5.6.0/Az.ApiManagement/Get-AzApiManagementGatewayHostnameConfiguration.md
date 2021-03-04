---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementgatewayhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGatewayHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGatewayHostnameConfiguration.md
ms.openlocfilehash: 27e833c526dea1b8df6451671ae2fd142c00b6e1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889052"
---
# <span data-ttu-id="677a1-101">Get-AzApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="677a1-101">Get-AzApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="677a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="677a1-102">SYNOPSIS</span></span>
<span data-ttu-id="677a1-103">Obtém toda ou configuração de nome de host específico para o Gateway existente.</span><span class="sxs-lookup"><span data-stu-id="677a1-103">Gets all or specific hostname configuration for the existing Gateway.</span></span>

## <span data-ttu-id="677a1-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="677a1-104">SYNTAX</span></span>

### <span data-ttu-id="677a1-105">GetByGatewayId (Padrão)</span><span class="sxs-lookup"><span data-stu-id="677a1-105">GetByGatewayId (Default)</span></span>
```
Get-AzApiManagementGatewayHostnameConfiguration -Context <PsApiManagementContext> -GatewayId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="677a1-106">GetByGatewayHostnameId</span><span class="sxs-lookup"><span data-stu-id="677a1-106">GetByGatewayHostnameId</span></span>
```
Get-AzApiManagementGatewayHostnameConfiguration -Context <PsApiManagementContext> -GatewayId <String>
 -GatewayHostnameConfigurationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="677a1-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="677a1-107">DESCRIPTION</span></span>
<span data-ttu-id="677a1-108">O cmdlet **Get-AzApiManagementGatewayHostnameConfiguration** obtém toda ou configuração de nome de host específico para o Gateway existente.</span><span class="sxs-lookup"><span data-stu-id="677a1-108">The **Get-AzApiManagementGatewayHostnameConfiguration** cmdlet gets all or specific hostname configuration for the existing Gateway.</span></span>

## <span data-ttu-id="677a1-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="677a1-109">EXAMPLES</span></span>

### <span data-ttu-id="677a1-110">Exemplo 1: Obter todas as configurações de nome de host para o gateway</span><span class="sxs-lookup"><span data-stu-id="677a1-110">Example 1: Get all hostname configurations for the gateway</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGatewayHostnameConfiguration -Context $apimContext  -GatewayId "0123456789"
```

<span data-ttu-id="677a1-111">Este comando obtém todas as configurações de nome de host para um gateway "0123456789".</span><span class="sxs-lookup"><span data-stu-id="677a1-111">This command gets all hostname configurations for a "0123456789" gateway.</span></span>

### <span data-ttu-id="677a1-112">Exemplo 2: Obter uma configuração de nome de host para o gateway</span><span class="sxs-lookup"><span data-stu-id="677a1-112">Example 2: Get a hostname configuration for the gateway</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGatewayHostnameConfiguration -Context $apimContext -GatewayId "0123456789" -GatewayHostnameConfigurationId "123"
```

<span data-ttu-id="677a1-113">Este comando obtém a configuração de nome de host "123" para um gateway "0123456789".</span><span class="sxs-lookup"><span data-stu-id="677a1-113">This command gets "123" hostname configuration for a "0123456789" gateway.</span></span>

## <span data-ttu-id="677a1-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="677a1-114">PARAMETERS</span></span>

### <span data-ttu-id="677a1-115">-Context</span><span class="sxs-lookup"><span data-stu-id="677a1-115">-Context</span></span>
<span data-ttu-id="677a1-116">Instância de PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="677a1-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="677a1-117">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="677a1-117">This parameter is required.</span></span>

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

### <span data-ttu-id="677a1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="677a1-118">-DefaultProfile</span></span>
<span data-ttu-id="677a1-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="677a1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="677a1-120">-GatewayHostnameConfigurationId</span><span class="sxs-lookup"><span data-stu-id="677a1-120">-GatewayHostnameConfigurationId</span></span>
<span data-ttu-id="677a1-121">Identificador de configuração do nomedo host.</span><span class="sxs-lookup"><span data-stu-id="677a1-121">Hostname Configuration identifier.</span></span>
<span data-ttu-id="677a1-122">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="677a1-122">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByGatewayHostnameId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="677a1-123">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="677a1-123">-GatewayId</span></span>
<span data-ttu-id="677a1-124">Identificador de gateway.</span><span class="sxs-lookup"><span data-stu-id="677a1-124">Gateway identifier.</span></span>
<span data-ttu-id="677a1-125">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="677a1-125">This parameter is required.</span></span>

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

### <span data-ttu-id="677a1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="677a1-126">CommonParameters</span></span>
<span data-ttu-id="677a1-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="677a1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="677a1-128">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="677a1-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="677a1-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="677a1-129">INPUTS</span></span>

### <span data-ttu-id="677a1-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="677a1-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="677a1-131">System.String</span><span class="sxs-lookup"><span data-stu-id="677a1-131">System.String</span></span>

## <span data-ttu-id="677a1-132">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="677a1-132">OUTPUTS</span></span>

### <span data-ttu-id="677a1-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="677a1-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="677a1-134">NOTES</span><span class="sxs-lookup"><span data-stu-id="677a1-134">NOTES</span></span>

## <span data-ttu-id="677a1-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="677a1-135">RELATED LINKS</span></span>
