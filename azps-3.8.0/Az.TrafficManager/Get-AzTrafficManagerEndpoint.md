---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 4556C345-55D0-431C-B980-219D5ED14E5F
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/get-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Get-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Get-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 3a24063e7b3d74704aa8d409b5bec6d87e35d095
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941639"
---
# <span data-ttu-id="1a8e6-101">Get-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="1a8e6-101">Get-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="1a8e6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1a8e6-102">SYNOPSIS</span></span>
<span data-ttu-id="1a8e6-103">Obtém um ponto de extremidade para um perfil do Gerenciador de tráfego.</span><span class="sxs-lookup"><span data-stu-id="1a8e6-103">Gets an endpoint for a Traffic Manager profile.</span></span>

## <span data-ttu-id="1a8e6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1a8e6-104">SYNTAX</span></span>

### <span data-ttu-id="1a8e6-105">Campos</span><span class="sxs-lookup"><span data-stu-id="1a8e6-105">Fields</span></span>
```
Get-AzTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1a8e6-106">Objeto</span><span class="sxs-lookup"><span data-stu-id="1a8e6-106">Object</span></span>
```
Get-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1a8e6-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1a8e6-107">DESCRIPTION</span></span>
<span data-ttu-id="1a8e6-108">O cmdlet **Get-AzTrafficManagerEndpoint** Obtém um ponto de extremidade para um perfil do Gerenciador de tráfego do Azure.</span><span class="sxs-lookup"><span data-stu-id="1a8e6-108">The **Get-AzTrafficManagerEndpoint** cmdlet gets an endpoint for an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="1a8e6-109">Você pode modificar esse objeto localmente e, em seguida, aplicar as alterações ao perfil usando o cmdlet Set-AzTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="1a8e6-109">You can modify this object locally, and then apply changes to the profile by using the Set-AzTrafficManagerEndpoint cmdlet.</span></span>
<span data-ttu-id="1a8e6-110">Especifique o ponto de extremidade usando os parâmetros *Name* e *Type* .</span><span class="sxs-lookup"><span data-stu-id="1a8e6-110">Specify the endpoint by using the *Name* and *Type* parameters.</span></span>
<span data-ttu-id="1a8e6-111">Você pode especificar o perfil do Gerenciador de tráfego usando o parâmetro *ProfileName* e *ResourceGroupName* ou especificando um objeto **TrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="1a8e6-111">You can specify the Traffic Manager profile either by using the *ProfileName* and *ResourceGroupName* parameter, or by specifying a **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="1a8e6-112">Você também pode passar esse valor usando o pipeline.</span><span class="sxs-lookup"><span data-stu-id="1a8e6-112">Alternatively, you can pass that value by using the pipeline.</span></span>

## <span data-ttu-id="1a8e6-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1a8e6-113">EXAMPLES</span></span>

### <span data-ttu-id="1a8e6-114">Exemplo 1: obter um ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="1a8e6-114">Example 1: Get an endpoint</span></span>
```
PS C:\>$TrafficManagerEndpoint = Get-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
```

<span data-ttu-id="1a8e6-115">Esse comando obtém o ponto de extremidade do Azure chamado contoso do perfil chamado ContosoProfile no grupo de recursos chamado ResourceGroup11 e, em seguida, armazena esse objeto na variável $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="1a8e6-115">This command gets the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11, and then stores that object in the $TrafficManagerEndpoint variable.</span></span>

## <span data-ttu-id="1a8e6-116">OS</span><span class="sxs-lookup"><span data-stu-id="1a8e6-116">PARAMETERS</span></span>

### <span data-ttu-id="1a8e6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a8e6-117">-DefaultProfile</span></span>
<span data-ttu-id="1a8e6-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1a8e6-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1a8e6-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="1a8e6-119">-Name</span></span>
<span data-ttu-id="1a8e6-120">Especifica o nome do ponto de extremidade do Gerenciador de tráfego que o cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="1a8e6-120">Specifies the name of the Traffic Manager endpoint that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a8e6-121">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="1a8e6-121">-ProfileName</span></span>
<span data-ttu-id="1a8e6-122">Especifica o nome do ponto de extremidade do Gerenciador de tráfego que o cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="1a8e6-122">Specifies the name of the Traffic Manager endpoint that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a8e6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a8e6-123">-ResourceGroupName</span></span>
<span data-ttu-id="1a8e6-124">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1a8e6-124">Specifies the name of a resource group.</span></span>
<span data-ttu-id="1a8e6-125">Esse cmdlet obtém um ponto de extremidade do Gerenciador de tráfego no grupo especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="1a8e6-125">This cmdlet gets a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a8e6-126">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="1a8e6-126">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="1a8e6-127">Especifica o ponto de extremidade do Gerenciador de tráfego que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="1a8e6-127">Specifies the Traffic Manager endpoint that this cmdlet gets.</span></span>

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1a8e6-128">-Digite</span><span class="sxs-lookup"><span data-stu-id="1a8e6-128">-Type</span></span>
<span data-ttu-id="1a8e6-129">Especifica o tipo de ponto de extremidade que este cmdlet adiciona ao perfil do Gerenciador de tráfego.</span><span class="sxs-lookup"><span data-stu-id="1a8e6-129">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="1a8e6-130">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="1a8e6-130">Valid values are:</span></span> 

- <span data-ttu-id="1a8e6-131">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="1a8e6-131">AzureEndpoints</span></span>
- <span data-ttu-id="1a8e6-132">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="1a8e6-132">ExternalEndpoints</span></span>
- <span data-ttu-id="1a8e6-133">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="1a8e6-133">NestedEndpoints</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:
Accepted values: AzureEndpoints, ExternalEndpoints, NestedEndpoints

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a8e6-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a8e6-134">CommonParameters</span></span>
<span data-ttu-id="1a8e6-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a8e6-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a8e6-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a8e6-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a8e6-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1a8e6-137">INPUTS</span></span>

### <span data-ttu-id="1a8e6-138">Microsoft. Azure. Commands. Trafficmanager. Models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="1a8e6-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="1a8e6-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1a8e6-139">OUTPUTS</span></span>

### <span data-ttu-id="1a8e6-140">Microsoft. Azure. Commands. Trafficmanager. Models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="1a8e6-140">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="1a8e6-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1a8e6-141">NOTES</span></span>

## <span data-ttu-id="1a8e6-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1a8e6-142">RELATED LINKS</span></span>

[<span data-ttu-id="1a8e6-143">Disable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="1a8e6-143">Disable-AzTrafficManagerEndpoint</span></span>](./Disable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="1a8e6-144">Enable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="1a8e6-144">Enable-AzTrafficManagerEndpoint</span></span>](./Enable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="1a8e6-145">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="1a8e6-145">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="1a8e6-146">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="1a8e6-146">Remove-AzTrafficManagerEndpoint</span></span>](./Remove-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="1a8e6-147">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="1a8e6-147">Set-AzTrafficManagerEndpoint</span></span>](./Set-AzTrafficManagerEndpoint.md)


