---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementgatewayhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGatewayHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGatewayHostnameConfiguration.md
ms.openlocfilehash: ecdae500b0c1d81635e23ca6ca4bc4c803665912
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98263402"
---
# <span data-ttu-id="f9b85-101">Get-AzApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="f9b85-101">Get-AzApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="f9b85-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f9b85-102">SYNOPSIS</span></span>
<span data-ttu-id="f9b85-103">Obtém toda a configuração ou um nome de host especificado para o gateway existente.</span><span class="sxs-lookup"><span data-stu-id="f9b85-103">Gets all or specific hostname configuration for the existing Gateway.</span></span>

## <span data-ttu-id="f9b85-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f9b85-104">SYNTAX</span></span>

### <span data-ttu-id="f9b85-105">GetByGatewayId (padrão)</span><span class="sxs-lookup"><span data-stu-id="f9b85-105">GetByGatewayId (Default)</span></span>
```
Get-AzApiManagementGatewayHostnameConfiguration -Context <PsApiManagementContext> -GatewayId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f9b85-106">GetByGatewayHostnameId</span><span class="sxs-lookup"><span data-stu-id="f9b85-106">GetByGatewayHostnameId</span></span>
```
Get-AzApiManagementGatewayHostnameConfiguration -Context <PsApiManagementContext> -GatewayId <String>
 -GatewayHostnameConfigurationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f9b85-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f9b85-107">DESCRIPTION</span></span>
<span data-ttu-id="f9b85-108">O cmdlet **Get-AzApiManagementGatewayHostnameConfiguration** Obtém toda a configuração do nome do host existente do gateway existente.</span><span class="sxs-lookup"><span data-stu-id="f9b85-108">The **Get-AzApiManagementGatewayHostnameConfiguration** cmdlet gets all or specific hostname configuration for the existing Gateway.</span></span>

## <span data-ttu-id="f9b85-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f9b85-109">EXAMPLES</span></span>

### <span data-ttu-id="f9b85-110">Exemplo 1: obter todas as configurações de nome de host para o gateway</span><span class="sxs-lookup"><span data-stu-id="f9b85-110">Example 1: Get all hostname configurations for the gateway</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGatewayHostnameConfiguration -Context $apimContext  -GatewayId "0123456789"
```

<span data-ttu-id="f9b85-111">Esse comando obtém todas as configurações de nome de host para um gateway "0123456789".</span><span class="sxs-lookup"><span data-stu-id="f9b85-111">This command gets all hostname configurations for a "0123456789" gateway.</span></span>

### <span data-ttu-id="f9b85-112">Exemplo 2: obter uma configuração de nome de host para o gateway</span><span class="sxs-lookup"><span data-stu-id="f9b85-112">Example 2: Get a hostname configuration for the gateway</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGatewayHostnameConfiguration -Context $apimContext -GatewayId "0123456789" -GatewayHostnameConfigurationId "123"
```

<span data-ttu-id="f9b85-113">Esse comando obtém a configuração do nome do host "123" para um gateway "0123456789".</span><span class="sxs-lookup"><span data-stu-id="f9b85-113">This command gets "123" hostname configuration for a "0123456789" gateway.</span></span>

## <span data-ttu-id="f9b85-114">OS</span><span class="sxs-lookup"><span data-stu-id="f9b85-114">PARAMETERS</span></span>

### <span data-ttu-id="f9b85-115">-Contexto</span><span class="sxs-lookup"><span data-stu-id="f9b85-115">-Context</span></span>
<span data-ttu-id="f9b85-116">Instância do PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="f9b85-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="f9b85-117">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="f9b85-117">This parameter is required.</span></span>

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

### <span data-ttu-id="f9b85-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9b85-118">-DefaultProfile</span></span>
<span data-ttu-id="f9b85-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f9b85-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9b85-120">-GatewayHostnameConfigurationId</span><span class="sxs-lookup"><span data-stu-id="f9b85-120">-GatewayHostnameConfigurationId</span></span>
<span data-ttu-id="f9b85-121">Identificador de configuração de nome de host.</span><span class="sxs-lookup"><span data-stu-id="f9b85-121">Hostname Configuration identifier.</span></span>
<span data-ttu-id="f9b85-122">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="f9b85-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="f9b85-123">-Gatewayid</span><span class="sxs-lookup"><span data-stu-id="f9b85-123">-GatewayId</span></span>
<span data-ttu-id="f9b85-124">Identificador do gateway.</span><span class="sxs-lookup"><span data-stu-id="f9b85-124">Gateway identifier.</span></span>
<span data-ttu-id="f9b85-125">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="f9b85-125">This parameter is required.</span></span>

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

### <span data-ttu-id="f9b85-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9b85-126">CommonParameters</span></span>
<span data-ttu-id="f9b85-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9b85-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9b85-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f9b85-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9b85-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f9b85-129">INPUTS</span></span>

### <span data-ttu-id="f9b85-130">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="f9b85-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f9b85-131">System. String</span><span class="sxs-lookup"><span data-stu-id="f9b85-131">System.String</span></span>

## <span data-ttu-id="f9b85-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f9b85-132">OUTPUTS</span></span>

### <span data-ttu-id="f9b85-133">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="f9b85-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="f9b85-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f9b85-134">NOTES</span></span>

## <span data-ttu-id="f9b85-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f9b85-135">RELATED LINKS</span></span>
