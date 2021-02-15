---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementgatewayhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGatewayHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGatewayHostnameConfiguration.md
ms.openlocfilehash: ecdae500b0c1d81635e23ca6ca4bc4c803665912
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118079"
---
# <span data-ttu-id="976a5-101">Get-AzApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="976a5-101">Get-AzApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="976a5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="976a5-102">SYNOPSIS</span></span>
<span data-ttu-id="976a5-103">Obtém configuração de nome de host completo ou específico para o Gateway existente.</span><span class="sxs-lookup"><span data-stu-id="976a5-103">Gets all or specific hostname configuration for the existing Gateway.</span></span>

## <span data-ttu-id="976a5-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="976a5-104">SYNTAX</span></span>

### <span data-ttu-id="976a5-105">GetByGatewayId (Padrão)</span><span class="sxs-lookup"><span data-stu-id="976a5-105">GetByGatewayId (Default)</span></span>
```
Get-AzApiManagementGatewayHostnameConfiguration -Context <PsApiManagementContext> -GatewayId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="976a5-106">GetByGatewayHostnameId</span><span class="sxs-lookup"><span data-stu-id="976a5-106">GetByGatewayHostnameId</span></span>
```
Get-AzApiManagementGatewayHostnameConfiguration -Context <PsApiManagementContext> -GatewayId <String>
 -GatewayHostnameConfigurationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="976a5-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="976a5-107">DESCRIPTION</span></span>
<span data-ttu-id="976a5-108">O cmdlet **Get-AzApiManagementGatewayHostnameConfiguration** obtém configurações de nome de host todas ou específicas para o Gateway existente.</span><span class="sxs-lookup"><span data-stu-id="976a5-108">The **Get-AzApiManagementGatewayHostnameConfiguration** cmdlet gets all or specific hostname configuration for the existing Gateway.</span></span>

## <span data-ttu-id="976a5-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="976a5-109">EXAMPLES</span></span>

### <span data-ttu-id="976a5-110">Exemplo 1: Obter todas as configurações de nome de host para o gateway</span><span class="sxs-lookup"><span data-stu-id="976a5-110">Example 1: Get all hostname configurations for the gateway</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGatewayHostnameConfiguration -Context $apimContext  -GatewayId "0123456789"
```

<span data-ttu-id="976a5-111">Esse comando obtém todas as configurações de nome de host para um gateway "0123456789".</span><span class="sxs-lookup"><span data-stu-id="976a5-111">This command gets all hostname configurations for a "0123456789" gateway.</span></span>

### <span data-ttu-id="976a5-112">Exemplo 2: Obter uma configuração de nome de host para o gateway</span><span class="sxs-lookup"><span data-stu-id="976a5-112">Example 2: Get a hostname configuration for the gateway</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGatewayHostnameConfiguration -Context $apimContext -GatewayId "0123456789" -GatewayHostnameConfigurationId "123"
```

<span data-ttu-id="976a5-113">Esse comando obtém a configuração de nome de host "123" para um gateway "0123456789".</span><span class="sxs-lookup"><span data-stu-id="976a5-113">This command gets "123" hostname configuration for a "0123456789" gateway.</span></span>

## <span data-ttu-id="976a5-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="976a5-114">PARAMETERS</span></span>

### <span data-ttu-id="976a5-115">-Contexto</span><span class="sxs-lookup"><span data-stu-id="976a5-115">-Context</span></span>
<span data-ttu-id="976a5-116">Instância de PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="976a5-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="976a5-117">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="976a5-117">This parameter is required.</span></span>

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

### <span data-ttu-id="976a5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="976a5-118">-DefaultProfile</span></span>
<span data-ttu-id="976a5-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="976a5-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="976a5-120">-GatewayHostnameConfigurationId</span><span class="sxs-lookup"><span data-stu-id="976a5-120">-GatewayHostnameConfigurationId</span></span>
<span data-ttu-id="976a5-121">Identificador de configuração do nome do host.</span><span class="sxs-lookup"><span data-stu-id="976a5-121">Hostname Configuration identifier.</span></span>
<span data-ttu-id="976a5-122">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="976a5-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="976a5-123">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="976a5-123">-GatewayId</span></span>
<span data-ttu-id="976a5-124">Identificador de gateway.</span><span class="sxs-lookup"><span data-stu-id="976a5-124">Gateway identifier.</span></span>
<span data-ttu-id="976a5-125">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="976a5-125">This parameter is required.</span></span>

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

### <span data-ttu-id="976a5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="976a5-126">CommonParameters</span></span>
<span data-ttu-id="976a5-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="976a5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="976a5-128">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="976a5-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="976a5-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="976a5-129">INPUTS</span></span>

### <span data-ttu-id="976a5-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="976a5-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="976a5-131">System.String</span><span class="sxs-lookup"><span data-stu-id="976a5-131">System.String</span></span>

## <span data-ttu-id="976a5-132">Saídas</span><span class="sxs-lookup"><span data-stu-id="976a5-132">OUTPUTS</span></span>

### <span data-ttu-id="976a5-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="976a5-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="976a5-134">Notas</span><span class="sxs-lookup"><span data-stu-id="976a5-134">NOTES</span></span>

## <span data-ttu-id="976a5-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="976a5-135">RELATED LINKS</span></span>
