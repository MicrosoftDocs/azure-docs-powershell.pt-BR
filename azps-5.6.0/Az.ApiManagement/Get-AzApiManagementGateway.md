---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGateway.md
ms.openlocfilehash: 980adceb2e5a76532c9b3175c015d5f4e3a6b2e1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891525"
---
# <span data-ttu-id="146dd-101">Get-AzApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="146dd-101">Get-AzApiManagementGateway</span></span>

## <span data-ttu-id="146dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="146dd-102">SYNOPSIS</span></span>
<span data-ttu-id="146dd-103">Obtém gateway de gerenciamento de API todo ou específico.</span><span class="sxs-lookup"><span data-stu-id="146dd-103">Gets all or specific API management Gateway.</span></span>

## <span data-ttu-id="146dd-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="146dd-104">SYNTAX</span></span>

### <span data-ttu-id="146dd-105">GetAllGateways (Padrão)</span><span class="sxs-lookup"><span data-stu-id="146dd-105">GetAllGateways (Default)</span></span>
```
Get-AzApiManagementGateway -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="146dd-106">GetByGatewayId</span><span class="sxs-lookup"><span data-stu-id="146dd-106">GetByGatewayId</span></span>
```
Get-AzApiManagementGateway -Context <PsApiManagementContext> -GatewayId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="146dd-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="146dd-107">DESCRIPTION</span></span>
<span data-ttu-id="146dd-108">O cmdlet **Get-AzApiManagementGateway** obtém o Gateway de gerenciamento de API ou todo ou específico.</span><span class="sxs-lookup"><span data-stu-id="146dd-108">The **Get-AzApiManagementGateway** cmdlet gets all or specific API management Gateway.</span></span>

## <span data-ttu-id="146dd-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="146dd-109">EXAMPLES</span></span>

### <span data-ttu-id="146dd-110">Exemplo 1: Obter todos os gateways</span><span class="sxs-lookup"><span data-stu-id="146dd-110">Example 1: Get all gateways</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGateway -Context $apimContext
```

<span data-ttu-id="146dd-111">Este comando obtém todos os gateways.</span><span class="sxs-lookup"><span data-stu-id="146dd-111">This command gets all gateways.</span></span>

### <span data-ttu-id="146dd-112">Exemplo 2: Obter um gateway por ID</span><span class="sxs-lookup"><span data-stu-id="146dd-112">Example 2: Get a gateway by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGateway -Context $apimContext -GatewayId "0123456789"
```

<span data-ttu-id="146dd-113">Este comando obtém o gateway 0123456789.</span><span class="sxs-lookup"><span data-stu-id="146dd-113">This command gets the gateway 0123456789.</span></span>

## <span data-ttu-id="146dd-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="146dd-114">PARAMETERS</span></span>

### <span data-ttu-id="146dd-115">-Context</span><span class="sxs-lookup"><span data-stu-id="146dd-115">-Context</span></span>
<span data-ttu-id="146dd-116">Instância de PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="146dd-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="146dd-117">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="146dd-117">This parameter is required.</span></span>

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

### <span data-ttu-id="146dd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="146dd-118">-DefaultProfile</span></span>
<span data-ttu-id="146dd-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="146dd-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="146dd-120">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="146dd-120">-GatewayId</span></span>
<span data-ttu-id="146dd-121">Identificador de um gateway.</span><span class="sxs-lookup"><span data-stu-id="146dd-121">Identifier of a gateway.</span></span>
<span data-ttu-id="146dd-122">Se especificado, tentará encontrar gateway pelo identificador.</span><span class="sxs-lookup"><span data-stu-id="146dd-122">If specified will try to find gateway by the identifier.</span></span>

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

### <span data-ttu-id="146dd-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="146dd-123">CommonParameters</span></span>
<span data-ttu-id="146dd-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="146dd-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="146dd-125">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="146dd-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="146dd-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="146dd-126">INPUTS</span></span>

### <span data-ttu-id="146dd-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="146dd-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="146dd-128">System.String</span><span class="sxs-lookup"><span data-stu-id="146dd-128">System.String</span></span>

## <span data-ttu-id="146dd-129">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="146dd-129">OUTPUTS</span></span>

### <span data-ttu-id="146dd-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="146dd-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway</span></span>

## <span data-ttu-id="146dd-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="146dd-131">NOTES</span></span>

## <span data-ttu-id="146dd-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="146dd-132">RELATED LINKS</span></span>
