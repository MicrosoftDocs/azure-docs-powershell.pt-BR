---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGateway.md
ms.openlocfilehash: 80b059a82264cf7d0adedbfca477616abcaa232d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98432729"
---
# <span data-ttu-id="792d3-101">Get-AzApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="792d3-101">Get-AzApiManagementGateway</span></span>

## <span data-ttu-id="792d3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="792d3-102">SYNOPSIS</span></span>
<span data-ttu-id="792d3-103">Obtém todo ou gateway de gerenciamento de API específico.</span><span class="sxs-lookup"><span data-stu-id="792d3-103">Gets all or specific API management Gateway.</span></span>

## <span data-ttu-id="792d3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="792d3-104">SYNTAX</span></span>

### <span data-ttu-id="792d3-105">GetAllGateways (padrão)</span><span class="sxs-lookup"><span data-stu-id="792d3-105">GetAllGateways (Default)</span></span>
```
Get-AzApiManagementGateway -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="792d3-106">GetByGatewayId</span><span class="sxs-lookup"><span data-stu-id="792d3-106">GetByGatewayId</span></span>
```
Get-AzApiManagementGateway -Context <PsApiManagementContext> -GatewayId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="792d3-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="792d3-107">DESCRIPTION</span></span>
<span data-ttu-id="792d3-108">O cmdlet **Get-AzApiManagementGateway** Obtém todo ou um gateway de gerenciamento de API específico.</span><span class="sxs-lookup"><span data-stu-id="792d3-108">The **Get-AzApiManagementGateway** cmdlet gets all or specific API management Gateway.</span></span>

## <span data-ttu-id="792d3-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="792d3-109">EXAMPLES</span></span>

### <span data-ttu-id="792d3-110">Exemplo 1: obter todos os gateways</span><span class="sxs-lookup"><span data-stu-id="792d3-110">Example 1: Get all gateways</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGateway -Context $apimContext
```

<span data-ttu-id="792d3-111">Esse comando obtém todos os gateways.</span><span class="sxs-lookup"><span data-stu-id="792d3-111">This command gets all gateways.</span></span>

### <span data-ttu-id="792d3-112">Exemplo 2: obter um gateway por ID</span><span class="sxs-lookup"><span data-stu-id="792d3-112">Example 2: Get a gateway by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGateway -Context $apimContext -GatewayId "0123456789"
```

<span data-ttu-id="792d3-113">Esse comando obtém o gateway 0123456789.</span><span class="sxs-lookup"><span data-stu-id="792d3-113">This command gets the gateway 0123456789.</span></span>

## <span data-ttu-id="792d3-114">OS</span><span class="sxs-lookup"><span data-stu-id="792d3-114">PARAMETERS</span></span>

### <span data-ttu-id="792d3-115">-Contexto</span><span class="sxs-lookup"><span data-stu-id="792d3-115">-Context</span></span>
<span data-ttu-id="792d3-116">Instância do PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="792d3-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="792d3-117">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="792d3-117">This parameter is required.</span></span>

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

### <span data-ttu-id="792d3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="792d3-118">-DefaultProfile</span></span>
<span data-ttu-id="792d3-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="792d3-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="792d3-120">-Gatewayid</span><span class="sxs-lookup"><span data-stu-id="792d3-120">-GatewayId</span></span>
<span data-ttu-id="792d3-121">Identificador de um gateway.</span><span class="sxs-lookup"><span data-stu-id="792d3-121">Identifier of a gateway.</span></span>
<span data-ttu-id="792d3-122">Se especificado, tentará localizar o gateway pelo identificador.</span><span class="sxs-lookup"><span data-stu-id="792d3-122">If specified will try to find gateway by the identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByGatewayId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="792d3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="792d3-123">CommonParameters</span></span>
<span data-ttu-id="792d3-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="792d3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="792d3-125">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="792d3-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="792d3-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="792d3-126">INPUTS</span></span>

### <span data-ttu-id="792d3-127">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="792d3-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="792d3-128">System. String</span><span class="sxs-lookup"><span data-stu-id="792d3-128">System.String</span></span>

## <span data-ttu-id="792d3-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="792d3-129">OUTPUTS</span></span>

### <span data-ttu-id="792d3-130">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="792d3-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway</span></span>

## <span data-ttu-id="792d3-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="792d3-131">NOTES</span></span>

## <span data-ttu-id="792d3-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="792d3-132">RELATED LINKS</span></span>
