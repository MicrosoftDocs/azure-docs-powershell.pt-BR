---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 2129C457-592B-484C-A148-828BFD5895D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 6f2884a6d4cefaf52b06ec653db85c9e9ae59f54
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98272266"
---
# <span data-ttu-id="6091e-101">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="6091e-101">Remove-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="6091e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6091e-102">SYNOPSIS</span></span>
<span data-ttu-id="6091e-103">Remove um ponto de extremidade do Gerenciador de tráfego.</span><span class="sxs-lookup"><span data-stu-id="6091e-103">Removes an endpoint from Traffic Manager.</span></span>

## <span data-ttu-id="6091e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6091e-104">SYNTAX</span></span>

### <span data-ttu-id="6091e-105">Campos</span><span class="sxs-lookup"><span data-stu-id="6091e-105">Fields</span></span>
```
Remove-AzTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String> -ResourceGroupName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6091e-106">Objeto</span><span class="sxs-lookup"><span data-stu-id="6091e-106">Object</span></span>
```
Remove-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6091e-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6091e-107">DESCRIPTION</span></span>
<span data-ttu-id="6091e-108">O cmdlet **Remove-AzTrafficManagerEndpoint** remove um ponto de extremidade do Gerenciador de tráfego do Azure.</span><span class="sxs-lookup"><span data-stu-id="6091e-108">The **Remove-AzTrafficManagerEndpoint** cmdlet removes an endpoint from Azure Traffic Manager.</span></span>

<span data-ttu-id="6091e-109">Esse cmdlet confirma cada alteração no serviço do Gerenciador de tráfego.</span><span class="sxs-lookup"><span data-stu-id="6091e-109">This cmdlet commits each change to the Traffic Manager service.</span></span>
<span data-ttu-id="6091e-110">Para remover vários pontos de extremidade de um objeto de perfil do Gerenciador de tráfego local e confirmar as alterações em uma única operação, use o cmdlet Remove-AzTrafficManagerEndpointConfig.</span><span class="sxs-lookup"><span data-stu-id="6091e-110">To remove multiple endpoints from a local Traffic Manager profile object and commit changes in a single operation, use the Remove-AzTrafficManagerEndpointConfig cmdlet.</span></span>

<span data-ttu-id="6091e-111">Você pode usar o operador pipeline para passar um objeto **TrafficManagerEndpoint** para esse cmdlet ou pode especificar um objeto **TrafficManagerEndpoint** usando o parâmetro *TrafficManagerEndpoint* .</span><span class="sxs-lookup"><span data-stu-id="6091e-111">You can use the pipeline operator to pass a **TrafficManagerEndpoint** object to this cmdlet, or you can specify a **TrafficManagerEndpoint** object by using the *TrafficManagerEndpoint* parameter.</span></span>

<span data-ttu-id="6091e-112">Você também pode especificar o nome e o tipo de ponto de extremidade usando os parâmetros *Name* e *Type* , juntamente com os parâmetros *ProfileName* e *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="6091e-112">Alternatively, you can specify the endpoint name and type by using the *Name* and *Type* parameters, together with the *ProfileName* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="6091e-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6091e-113">EXAMPLES</span></span>

### <span data-ttu-id="6091e-114">Exemplo 1: remover um ponto de extremidade de um perfil</span><span class="sxs-lookup"><span data-stu-id="6091e-114">Example 1: Remove an endpoint from a profile</span></span>
```
PS C:\>Remove-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
```

<span data-ttu-id="6091e-115">Esse comando Remove o ponto de extremidade do Azure chamado contoso do perfil chamado ContosoProfile no grupo de recursos chamado ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="6091e-115">This command removes the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="6091e-116">OS</span><span class="sxs-lookup"><span data-stu-id="6091e-116">PARAMETERS</span></span>

### <span data-ttu-id="6091e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6091e-117">-DefaultProfile</span></span>
<span data-ttu-id="6091e-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6091e-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6091e-119">-Force</span><span class="sxs-lookup"><span data-stu-id="6091e-119">-Force</span></span>
<span data-ttu-id="6091e-120">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="6091e-120">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6091e-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="6091e-121">-Name</span></span>
<span data-ttu-id="6091e-122">Especifica o nome do ponto de extremidade do Gerenciador de tráfego que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="6091e-122">Specifies the name of the Traffic Manager endpoint that this cmdlet removes.</span></span>

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

### <span data-ttu-id="6091e-123">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="6091e-123">-ProfileName</span></span>
<span data-ttu-id="6091e-124">Especifica o nome de um perfil do Gerenciador de tráfego do qual esse cmdlet Remove um ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="6091e-124">Specifies the name of a Traffic Manager profile from which this cmdlet removes an endpoint.</span></span>
<span data-ttu-id="6091e-125">Para obter um perfil, use o cmdlet Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="6091e-125">To obtain a profile, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="6091e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6091e-126">-ResourceGroupName</span></span>
<span data-ttu-id="6091e-127">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6091e-127">Specifies the name of a resource group.</span></span>
<span data-ttu-id="6091e-128">Esse cmdlet Remove um ponto de extremidade do Gerenciador de tráfego de um perfil do Gerenciador de tráfego no grupo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="6091e-128">This cmdlet removes a Traffic Manager endpoint from a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="6091e-129">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="6091e-129">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="6091e-130">Especifica o ponto de extremidade do Gerenciador de tráfego que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="6091e-130">Specifies the Traffic Manager endpoint that this cmdlet removes.</span></span>
<span data-ttu-id="6091e-131">Para obter um objeto **TrafficManagerEndpoint** , use o cmdlet Get-AzTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="6091e-131">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="6091e-132">-Digite</span><span class="sxs-lookup"><span data-stu-id="6091e-132">-Type</span></span>
<span data-ttu-id="6091e-133">Especifica o tipo de ponto de extremidade que este cmdlet adiciona ao perfil do Gerenciador de tráfego.</span><span class="sxs-lookup"><span data-stu-id="6091e-133">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="6091e-134">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="6091e-134">Valid values are:</span></span> 

- <span data-ttu-id="6091e-135">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="6091e-135">AzureEndpoints</span></span>
- <span data-ttu-id="6091e-136">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="6091e-136">ExternalEndpoints</span></span>
- <span data-ttu-id="6091e-137">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="6091e-137">NestedEndpoints</span></span>

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

### <span data-ttu-id="6091e-138">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6091e-138">-Confirm</span></span>
<span data-ttu-id="6091e-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6091e-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6091e-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6091e-140">-WhatIf</span></span>
<span data-ttu-id="6091e-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6091e-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6091e-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6091e-142">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6091e-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6091e-143">CommonParameters</span></span>
<span data-ttu-id="6091e-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6091e-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6091e-145">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6091e-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6091e-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6091e-146">INPUTS</span></span>

### <span data-ttu-id="6091e-147">Microsoft. Azure. Commands. Trafficmanager. Models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="6091e-147">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="6091e-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6091e-148">OUTPUTS</span></span>

### <span data-ttu-id="6091e-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6091e-149">System.Boolean</span></span>

## <span data-ttu-id="6091e-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6091e-150">NOTES</span></span>

## <span data-ttu-id="6091e-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6091e-151">RELATED LINKS</span></span>

[<span data-ttu-id="6091e-152">Get-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="6091e-152">Get-AzTrafficManagerEndpoint</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="6091e-153">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="6091e-153">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="6091e-154">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="6091e-154">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="6091e-155">Remove-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="6091e-155">Remove-AzTrafficManagerEndpointConfig</span></span>](./Remove-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="6091e-156">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="6091e-156">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


