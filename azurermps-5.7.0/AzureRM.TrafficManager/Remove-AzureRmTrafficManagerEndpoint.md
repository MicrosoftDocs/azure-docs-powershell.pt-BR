---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM
ms.assetid: 2129C457-592B-484C-A148-828BFD5895D4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/remove-azurermtrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerEndpoint.md
ms.openlocfilehash: 3b3eb2fb0539be4750f4cce7dedb7cd2f26931a6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429642"
---
# <span data-ttu-id="e4cc9-101">Remove-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e4cc9-101">Remove-AzureRmTrafficManagerEndpoint</span></span>

## <span data-ttu-id="e4cc9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e4cc9-102">SYNOPSIS</span></span>
<span data-ttu-id="e4cc9-103">Remove um ponto de extremidade do Gerenciador de tráfego.</span><span class="sxs-lookup"><span data-stu-id="e4cc9-103">Removes an endpoint from Traffic Manager.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e4cc9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e4cc9-104">SYNTAX</span></span>

### <span data-ttu-id="e4cc9-105">Campos</span><span class="sxs-lookup"><span data-stu-id="e4cc9-105">Fields</span></span>
```
Remove-AzureRmTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String>
 -ResourceGroupName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e4cc9-106">Objeto</span><span class="sxs-lookup"><span data-stu-id="e4cc9-106">Object</span></span>
```
Remove-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4cc9-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e4cc9-107">DESCRIPTION</span></span>
<span data-ttu-id="e4cc9-108">O cmdlet **Remove-AzureRmTrafficManagerEndpoint** remove um ponto de extremidade do Gerenciador de tráfego do Azure.</span><span class="sxs-lookup"><span data-stu-id="e4cc9-108">The **Remove-AzureRmTrafficManagerEndpoint** cmdlet removes an endpoint from Azure Traffic Manager.</span></span>

<span data-ttu-id="e4cc9-109">Esse cmdlet confirma cada alteração no serviço do Gerenciador de tráfego.</span><span class="sxs-lookup"><span data-stu-id="e4cc9-109">This cmdlet commits each change to the Traffic Manager service.</span></span>
<span data-ttu-id="e4cc9-110">Para remover vários pontos de extremidade de um objeto de perfil do Gerenciador de tráfego local e confirmar as alterações em uma única operação, use o cmdlet Remove-AzureRmTrafficManagerEndpointConfig.</span><span class="sxs-lookup"><span data-stu-id="e4cc9-110">To remove multiple endpoints from a local Traffic Manager profile object and commit changes in a single operation, use the Remove-AzureRmTrafficManagerEndpointConfig cmdlet.</span></span>

<span data-ttu-id="e4cc9-111">Você pode usar o operador pipeline para passar um objeto **TrafficManagerEndpoint** para esse cmdlet ou pode especificar um objeto **TrafficManagerEndpoint** usando o parâmetro *TrafficManagerEndpoint* .</span><span class="sxs-lookup"><span data-stu-id="e4cc9-111">You can use the pipeline operator to pass a **TrafficManagerEndpoint** object to this cmdlet, or you can specify a **TrafficManagerEndpoint** object by using the *TrafficManagerEndpoint* parameter.</span></span>

<span data-ttu-id="e4cc9-112">Você também pode especificar o nome e o tipo de ponto de extremidade usando os parâmetros *Name* e *Type* , juntamente com os parâmetros *ProfileName* e *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="e4cc9-112">Alternatively, you can specify the endpoint name and type by using the *Name* and *Type* parameters, together with the *ProfileName* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="e4cc9-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e4cc9-113">EXAMPLES</span></span>

### <span data-ttu-id="e4cc9-114">Exemplo 1: remover um ponto de extremidade de um perfil</span><span class="sxs-lookup"><span data-stu-id="e4cc9-114">Example 1: Remove an endpoint from a profile</span></span>
```
PS C:\>Remove-AzureRmTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
```

<span data-ttu-id="e4cc9-115">Esse comando Remove o ponto de extremidade do Azure chamado contoso do perfil chamado ContosoProfile no grupo de recursos chamado ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="e4cc9-115">This command removes the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="e4cc9-116">OS</span><span class="sxs-lookup"><span data-stu-id="e4cc9-116">PARAMETERS</span></span>

### <span data-ttu-id="e4cc9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4cc9-117">-DefaultProfile</span></span>
<span data-ttu-id="e4cc9-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e4cc9-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4cc9-119">-Force</span><span class="sxs-lookup"><span data-stu-id="e4cc9-119">-Force</span></span>
<span data-ttu-id="e4cc9-120">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="e4cc9-120">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4cc9-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="e4cc9-121">-Name</span></span>
<span data-ttu-id="e4cc9-122">Especifica o nome do ponto de extremidade do Gerenciador de tráfego que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="e4cc9-122">Specifies the name of the Traffic Manager endpoint that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4cc9-123">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="e4cc9-123">-ProfileName</span></span>
<span data-ttu-id="e4cc9-124">Especifica o nome de um perfil do Gerenciador de tráfego do qual esse cmdlet Remove um ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="e4cc9-124">Specifies the name of a Traffic Manager profile from which this cmdlet removes an endpoint.</span></span>
<span data-ttu-id="e4cc9-125">Para obter um perfil, use o cmdlet Get-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="e4cc9-125">To obtain a profile, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4cc9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4cc9-126">-ResourceGroupName</span></span>
<span data-ttu-id="e4cc9-127">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e4cc9-127">Specifies the name of a resource group.</span></span>
<span data-ttu-id="e4cc9-128">Esse cmdlet Remove um ponto de extremidade do Gerenciador de tráfego de um perfil do Gerenciador de tráfego no grupo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="e4cc9-128">This cmdlet removes a Traffic Manager endpoint from a Traffic Manager profile in the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4cc9-129">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e4cc9-129">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="e4cc9-130">Especifica o ponto de extremidade do Gerenciador de tráfego que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="e4cc9-130">Specifies the Traffic Manager endpoint that this cmdlet removes.</span></span>
<span data-ttu-id="e4cc9-131">Para obter um objeto **TrafficManagerEndpoint** , use o cmdlet Get-AzureRmTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="e4cc9-131">To obtain a **TrafficManagerEndpoint** object, use the Get-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

```yaml
Type: TrafficManagerEndpoint
Parameter Sets: Object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e4cc9-132">-Digite</span><span class="sxs-lookup"><span data-stu-id="e4cc9-132">-Type</span></span>
<span data-ttu-id="e4cc9-133">Especifica o tipo de ponto de extremidade que este cmdlet adiciona ao perfil do Gerenciador de tráfego.</span><span class="sxs-lookup"><span data-stu-id="e4cc9-133">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="e4cc9-134">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="e4cc9-134">Valid values are:</span></span> 

- <span data-ttu-id="e4cc9-135">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="e4cc9-135">AzureEndpoints</span></span>
- <span data-ttu-id="e4cc9-136">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="e4cc9-136">ExternalEndpoints</span></span>
- <span data-ttu-id="e4cc9-137">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="e4cc9-137">NestedEndpoints</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases: 
Accepted values: AzureEndpoints, ExternalEndpoints, NestedEndpoints

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4cc9-138">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e4cc9-138">-Confirm</span></span>
<span data-ttu-id="e4cc9-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4cc9-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4cc9-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4cc9-140">-WhatIf</span></span>
<span data-ttu-id="e4cc9-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e4cc9-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4cc9-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e4cc9-142">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4cc9-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4cc9-143">CommonParameters</span></span>
<span data-ttu-id="e4cc9-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4cc9-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4cc9-145">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4cc9-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4cc9-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e4cc9-146">INPUTS</span></span>

### <span data-ttu-id="e4cc9-147">TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e4cc9-147">TrafficManagerEndpoint</span></span>
<span data-ttu-id="e4cc9-148">O parâmetro ' TrafficManagerEndpoint ' aceita o valor do tipo ' TrafficManagerEndpoint ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="e4cc9-148">Parameter 'TrafficManagerEndpoint' accepts value of type 'TrafficManagerEndpoint' from the pipeline</span></span>

## <span data-ttu-id="e4cc9-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e4cc9-149">OUTPUTS</span></span>

### <span data-ttu-id="e4cc9-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e4cc9-150">System.Boolean</span></span>

## <span data-ttu-id="e4cc9-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e4cc9-151">NOTES</span></span>

## <span data-ttu-id="e4cc9-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e4cc9-152">RELATED LINKS</span></span>

[<span data-ttu-id="e4cc9-153">Get-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e4cc9-153">Get-AzureRmTrafficManagerEndpoint</span></span>](./Get-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="e4cc9-154">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="e4cc9-154">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="e4cc9-155">New-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e4cc9-155">New-AzureRmTrafficManagerEndpoint</span></span>](./New-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="e4cc9-156">Remove-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="e4cc9-156">Remove-AzureRmTrafficManagerEndpointConfig</span></span>](./Remove-AzureRmTrafficManagerEndpointConfig.md)

[<span data-ttu-id="e4cc9-157">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="e4cc9-157">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)

