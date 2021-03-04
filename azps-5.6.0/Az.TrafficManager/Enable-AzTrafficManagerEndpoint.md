---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 32263236-C207-4FE0-AB8A-018118FC7729
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/enable-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Enable-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Enable-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 5ab6ba03b9803cc8726eff458776f8ee40d48793
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885235"
---
# <span data-ttu-id="5be3e-101">Enable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="5be3e-101">Enable-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="5be3e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5be3e-102">SYNOPSIS</span></span>
<span data-ttu-id="5be3e-103">Habilita um ponto de extremidade em um perfil do Gerenciador de Tráfego.</span><span class="sxs-lookup"><span data-stu-id="5be3e-103">Enables an endpoint in a Traffic Manager profile.</span></span>

## <span data-ttu-id="5be3e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="5be3e-104">SYNTAX</span></span>

### <span data-ttu-id="5be3e-105">Fields</span><span class="sxs-lookup"><span data-stu-id="5be3e-105">Fields</span></span>
```
Enable-AzTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5be3e-106">Objeto</span><span class="sxs-lookup"><span data-stu-id="5be3e-106">Object</span></span>
```
Enable-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5be3e-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="5be3e-107">DESCRIPTION</span></span>
<span data-ttu-id="5be3e-108">O cmdlet **Enable-AzTrafficManagerEndpoint** habilita um ponto de extremidade em um perfil do Gerenciador de Tráfego do Azure.</span><span class="sxs-lookup"><span data-stu-id="5be3e-108">The **Enable-AzTrafficManagerEndpoint** cmdlet enables an endpoint in an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="5be3e-109">Você pode usar o operador de pipeline para passar um objeto **TrafficManagerEndpoint** para esse cmdlet ou pode especificar um **objeto TrafficManagerEndpoint** usando o parâmetro *TrafficManagerEndpoint.*</span><span class="sxs-lookup"><span data-stu-id="5be3e-109">You can use the pipeline operator to pass a **TrafficManagerEndpoint** object to this cmdlet, or you can specify a **TrafficManagerEndpoint** object by using the *TrafficManagerEndpoint* parameter.</span></span>

<span data-ttu-id="5be3e-110">Como alternativa, você pode especificar o nome e o tipo do ponto de extremidade usando os parâmetros *Name* e *Type,* juntamente com os parâmetros *ProfileName* e *ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="5be3e-110">Alternatively, you can specify the endpoint name and type by using the *Name* and *Type* parameters, together with the *ProfileName* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="5be3e-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5be3e-111">EXAMPLES</span></span>

### <span data-ttu-id="5be3e-112">Exemplo 1: Habilitar um ponto de extremidade de um perfil</span><span class="sxs-lookup"><span data-stu-id="5be3e-112">Example 1: Enable an endpoint from a profile</span></span>
```
PS C:\>Enable-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName ResourceGroup11 -Type ExternalEndpoints
```

<span data-ttu-id="5be3e-113">Esse comando habilita o ponto de extremidade externo chamado contoso no perfil chamado ContosoProfile no grupo de recursos ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="5be3e-113">This command enables the external endpoint named contoso in the profile named ContosoProfile in resource group ResourceGroup11.</span></span>

### <span data-ttu-id="5be3e-114">Exemplo 2: Habilitar um ponto de extremidade usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="5be3e-114">Example 2: Enable an endpoint by using the pipeline</span></span>
```
PS C:\>Get-AzTrafficManagerEndpoint -Name "contoso" -Type ExternalEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Enable-AzTrafficManagerEndpoint
```

<span data-ttu-id="5be3e-115">Este comando obtém o ponto de extremidade externo chamado Contoso do perfil chamado ContosoProfile em ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="5be3e-115">This command gets the external endpoint named Contoso from the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="5be3e-116">Em seguida, o comando passa esse ponto de extremidade para o cmdlet **Enable-AzTrafficManagerEndpoint** usando o operador de pipeline.</span><span class="sxs-lookup"><span data-stu-id="5be3e-116">The command then passes that endpoint to the **Enable-AzTrafficManagerEndpoint** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="5be3e-117">Esse cmdlet habilita esse ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="5be3e-117">That cmdlet enables that endpoint.</span></span>

## <span data-ttu-id="5be3e-118">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="5be3e-118">PARAMETERS</span></span>

### <span data-ttu-id="5be3e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5be3e-119">-DefaultProfile</span></span>
<span data-ttu-id="5be3e-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="5be3e-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5be3e-121">-Name</span><span class="sxs-lookup"><span data-stu-id="5be3e-121">-Name</span></span>
<span data-ttu-id="5be3e-122">Especifica o nome do ponto de extremidade do Gerenciador de Tráfego que esse cmdlet habilita.</span><span class="sxs-lookup"><span data-stu-id="5be3e-122">Specifies the name of the Traffic Manager endpoint that this cmdlet enables.</span></span>

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

### <span data-ttu-id="5be3e-123">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="5be3e-123">-ProfileName</span></span>
<span data-ttu-id="5be3e-124">Especifica o nome de um perfil do Gerenciador de Tráfego no qual esse cmdlet habilita um ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="5be3e-124">Specifies the name of a Traffic Manager profile in which this cmdlet enables an endpoint.</span></span>
<span data-ttu-id="5be3e-125">Para obter um perfil, use o Get-AzTrafficManagerProfile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5be3e-125">To obtain a profile, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="5be3e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5be3e-126">-ResourceGroupName</span></span>
<span data-ttu-id="5be3e-127">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5be3e-127">Specifies the name of a resource group.</span></span>
<span data-ttu-id="5be3e-128">Este cmdlet habilita um ponto de extremidade do Gerenciador de Tráfego no grupo especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="5be3e-128">This cmdlet enables a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="5be3e-129">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="5be3e-129">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="5be3e-130">Especifica o ponto de extremidade do Gerenciador de Tráfego que esse cmdlet habilita.</span><span class="sxs-lookup"><span data-stu-id="5be3e-130">Specifies the Traffic Manager endpoint that this cmdlet enables.</span></span>
<span data-ttu-id="5be3e-131">Para obter um **objeto TrafficManagerEndpoint,** use Get-AzTrafficManagerEndpoint cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5be3e-131">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="5be3e-132">-Type</span><span class="sxs-lookup"><span data-stu-id="5be3e-132">-Type</span></span>
<span data-ttu-id="5be3e-133">Especifica o tipo de ponto de extremidade que esse cmdlet desabilita no perfil do Gerenciador de Tráfego.</span><span class="sxs-lookup"><span data-stu-id="5be3e-133">Specifies the type of endpoint that this cmdlet disables in the Traffic Manager profile.</span></span>
<span data-ttu-id="5be3e-134">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="5be3e-134">Valid values are:</span></span> 

- <span data-ttu-id="5be3e-135">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="5be3e-135">AzureEndpoints</span></span>
- <span data-ttu-id="5be3e-136">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="5be3e-136">ExternalEndpoints</span></span>
- <span data-ttu-id="5be3e-137">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="5be3e-137">NestedEndpoints</span></span>

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

### <span data-ttu-id="5be3e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5be3e-138">CommonParameters</span></span>
<span data-ttu-id="5be3e-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5be3e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5be3e-140">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5be3e-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5be3e-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5be3e-141">INPUTS</span></span>

### <span data-ttu-id="5be3e-142">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="5be3e-142">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="5be3e-143">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="5be3e-143">OUTPUTS</span></span>

### <span data-ttu-id="5be3e-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5be3e-144">System.Boolean</span></span>

## <span data-ttu-id="5be3e-145">NOTES</span><span class="sxs-lookup"><span data-stu-id="5be3e-145">NOTES</span></span>

## <span data-ttu-id="5be3e-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5be3e-146">RELATED LINKS</span></span>

[<span data-ttu-id="5be3e-147">Disable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="5be3e-147">Disable-AzTrafficManagerEndpoint</span></span>](./Disable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="5be3e-148">Get-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="5be3e-148">Get-AzTrafficManagerEndpoint</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="5be3e-149">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="5be3e-149">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="5be3e-150">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="5be3e-150">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="5be3e-151">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="5be3e-151">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="5be3e-152">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="5be3e-152">Remove-AzTrafficManagerEndpoint</span></span>](./Remove-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="5be3e-153">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="5be3e-153">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


