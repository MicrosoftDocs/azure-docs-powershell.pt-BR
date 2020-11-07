---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 32263236-C207-4FE0-AB8A-018118FC7729
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/enable-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Enable-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Enable-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 5d7ef8e2fd778b5bcaaea1413bddd85eceb0582c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93955262"
---
# <span data-ttu-id="d7469-101">Enable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="d7469-101">Enable-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="d7469-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d7469-102">SYNOPSIS</span></span>
<span data-ttu-id="d7469-103">Habilita um ponto de extremidade em um perfil do Gerenciador de tráfego.</span><span class="sxs-lookup"><span data-stu-id="d7469-103">Enables an endpoint in a Traffic Manager profile.</span></span>

## <span data-ttu-id="d7469-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d7469-104">SYNTAX</span></span>

### <span data-ttu-id="d7469-105">Campos</span><span class="sxs-lookup"><span data-stu-id="d7469-105">Fields</span></span>
```
Enable-AzTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d7469-106">Objeto</span><span class="sxs-lookup"><span data-stu-id="d7469-106">Object</span></span>
```
Enable-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7469-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d7469-107">DESCRIPTION</span></span>
<span data-ttu-id="d7469-108">O cmdlet **Enable-AzTrafficManagerEndpoint** habilita um ponto de extremidade em um perfil do Gerenciador de tráfego do Azure.</span><span class="sxs-lookup"><span data-stu-id="d7469-108">The **Enable-AzTrafficManagerEndpoint** cmdlet enables an endpoint in an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="d7469-109">Você pode usar o operador pipeline para passar um objeto **TrafficManagerEndpoint** para esse cmdlet ou pode especificar um objeto **TrafficManagerEndpoint** usando o parâmetro *TrafficManagerEndpoint* .</span><span class="sxs-lookup"><span data-stu-id="d7469-109">You can use the pipeline operator to pass a **TrafficManagerEndpoint** object to this cmdlet, or you can specify a **TrafficManagerEndpoint** object by using the *TrafficManagerEndpoint* parameter.</span></span>

<span data-ttu-id="d7469-110">Você também pode especificar o nome e o tipo de ponto de extremidade usando os parâmetros *Name* e *Type* , juntamente com os parâmetros *ProfileName* e *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="d7469-110">Alternatively, you can specify the endpoint name and type by using the *Name* and *Type* parameters, together with the *ProfileName* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="d7469-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d7469-111">EXAMPLES</span></span>

### <span data-ttu-id="d7469-112">Exemplo 1: habilitar um ponto de extremidade de um perfil</span><span class="sxs-lookup"><span data-stu-id="d7469-112">Example 1: Enable an endpoint from a profile</span></span>
```
PS C:\>Enable-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName ResourceGroup11 -Type ExternalEndpoints
```

<span data-ttu-id="d7469-113">Esse comando habilita o ponto de extremidade externo chamado contoso no perfil chamado ContosoProfile na ResourceGroup11 do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d7469-113">This command enables the external endpoint named contoso in the profile named ContosoProfile in resource group ResourceGroup11.</span></span>

### <span data-ttu-id="d7469-114">Exemplo 2: habilitar um ponto de extremidade usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="d7469-114">Example 2: Enable an endpoint by using the pipeline</span></span>
```
PS C:\>Get-AzTrafficManagerEndpoint -Name "contoso" -Type ExternalEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Enable-AzTrafficManagerEndpoint
```

<span data-ttu-id="d7469-115">Esse comando obtém o ponto de extremidade externo chamado contoso do perfil chamado ContosoProfile em ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="d7469-115">This command gets the external endpoint named Contoso from the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="d7469-116">Em seguida, o comando passa esse ponto de extremidade para o cmdlet **Enable-AzTrafficManagerEndpoint** usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="d7469-116">The command then passes that endpoint to the **Enable-AzTrafficManagerEndpoint** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="d7469-117">Esse cmdlet habilita esse ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="d7469-117">That cmdlet enables that endpoint.</span></span>

## <span data-ttu-id="d7469-118">OS</span><span class="sxs-lookup"><span data-stu-id="d7469-118">PARAMETERS</span></span>

### <span data-ttu-id="d7469-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7469-119">-DefaultProfile</span></span>
<span data-ttu-id="d7469-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d7469-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d7469-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="d7469-121">-Name</span></span>
<span data-ttu-id="d7469-122">Especifica o nome do ponto de extremidade do Gerenciador de tráfego que o cmdlet habilita.</span><span class="sxs-lookup"><span data-stu-id="d7469-122">Specifies the name of the Traffic Manager endpoint that this cmdlet enables.</span></span>

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

### <span data-ttu-id="d7469-123">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="d7469-123">-ProfileName</span></span>
<span data-ttu-id="d7469-124">Especifica o nome de um perfil do Gerenciador de tráfego no qual esse cmdlet habilita um ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="d7469-124">Specifies the name of a Traffic Manager profile in which this cmdlet enables an endpoint.</span></span>
<span data-ttu-id="d7469-125">Para obter um perfil, use o cmdlet Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="d7469-125">To obtain a profile, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="d7469-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7469-126">-ResourceGroupName</span></span>
<span data-ttu-id="d7469-127">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d7469-127">Specifies the name of a resource group.</span></span>
<span data-ttu-id="d7469-128">Esse cmdlet habilita um ponto de extremidade do Gerenciador de tráfego no grupo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="d7469-128">This cmdlet enables a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="d7469-129">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="d7469-129">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="d7469-130">Especifica o ponto de extremidade do Gerenciador de tráfego que este cmdlet habilita.</span><span class="sxs-lookup"><span data-stu-id="d7469-130">Specifies the Traffic Manager endpoint that this cmdlet enables.</span></span>
<span data-ttu-id="d7469-131">Para obter um objeto **TrafficManagerEndpoint** , use o cmdlet Get-AzTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="d7469-131">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="d7469-132">-Digite</span><span class="sxs-lookup"><span data-stu-id="d7469-132">-Type</span></span>
<span data-ttu-id="d7469-133">Especifica o tipo de ponto de extremidade que esse cmdlet desabilita no perfil do Gerenciador de tráfego.</span><span class="sxs-lookup"><span data-stu-id="d7469-133">Specifies the type of endpoint that this cmdlet disables in the Traffic Manager profile.</span></span>
<span data-ttu-id="d7469-134">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="d7469-134">Valid values are:</span></span> 

- <span data-ttu-id="d7469-135">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="d7469-135">AzureEndpoints</span></span>
- <span data-ttu-id="d7469-136">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="d7469-136">ExternalEndpoints</span></span>
- <span data-ttu-id="d7469-137">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="d7469-137">NestedEndpoints</span></span>

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

### <span data-ttu-id="d7469-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7469-138">CommonParameters</span></span>
<span data-ttu-id="d7469-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7469-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7469-140">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7469-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7469-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d7469-141">INPUTS</span></span>

### <span data-ttu-id="d7469-142">Microsoft. Azure. Commands. Trafficmanager. Models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="d7469-142">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="d7469-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d7469-143">OUTPUTS</span></span>

### <span data-ttu-id="d7469-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d7469-144">System.Boolean</span></span>

## <span data-ttu-id="d7469-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d7469-145">NOTES</span></span>

## <span data-ttu-id="d7469-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d7469-146">RELATED LINKS</span></span>

[<span data-ttu-id="d7469-147">Disable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="d7469-147">Disable-AzTrafficManagerEndpoint</span></span>](./Disable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="d7469-148">Get-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="d7469-148">Get-AzTrafficManagerEndpoint</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="d7469-149">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d7469-149">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="d7469-150">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="d7469-150">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="d7469-151">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d7469-151">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="d7469-152">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="d7469-152">Remove-AzTrafficManagerEndpoint</span></span>](./Remove-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="d7469-153">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d7469-153">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


