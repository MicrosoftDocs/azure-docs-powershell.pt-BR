---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 8CC749F1-B961-4F8F-BAD4-2C0F4385D1C2
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/disable-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Disable-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Disable-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 037a670c0e96d1a9014cd19b32a7d2ba4da282ba
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94125220"
---
# <span data-ttu-id="6b8f7-101">Disable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="6b8f7-101">Disable-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="6b8f7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6b8f7-102">SYNOPSIS</span></span>
<span data-ttu-id="6b8f7-103">Desabilita um ponto de extremidade em um perfil do Gerenciador de tráfego.</span><span class="sxs-lookup"><span data-stu-id="6b8f7-103">Disables an endpoint in a Traffic Manager profile.</span></span>

## <span data-ttu-id="6b8f7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6b8f7-104">SYNTAX</span></span>

### <span data-ttu-id="6b8f7-105">Campos</span><span class="sxs-lookup"><span data-stu-id="6b8f7-105">Fields</span></span>
```
Disable-AzTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String>
 -ResourceGroupName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6b8f7-106">Objeto</span><span class="sxs-lookup"><span data-stu-id="6b8f7-106">Object</span></span>
```
Disable-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b8f7-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6b8f7-107">DESCRIPTION</span></span>
<span data-ttu-id="6b8f7-108">O cmdlet **Disable-AzTrafficManagerEndpoint** desabilita um ponto de extremidade em um perfil do Gerenciador de tráfego do Azure.</span><span class="sxs-lookup"><span data-stu-id="6b8f7-108">The **Disable-AzTrafficManagerEndpoint** cmdlet disables an endpoint in an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="6b8f7-109">Você pode usar o operador pipeline para passar um objeto **TrafficManagerEndpoint** para esse cmdlet, ou pode passar um objeto **TrafficManagerEndpoint** usando o parâmetro *TrafficManagerEndpoint* .</span><span class="sxs-lookup"><span data-stu-id="6b8f7-109">You can use the pipeline operator to pass a **TrafficManagerEndpoint** object to this cmdlet, or you can pass a **TrafficManagerEndpoint** object using the *TrafficManagerEndpoint* parameter.</span></span>

<span data-ttu-id="6b8f7-110">Você também pode especificar o nome e o tipo de ponto de extremidade usando os parâmetros *Name* e *Type* , juntamente com os parâmetros *ProfileName* e *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="6b8f7-110">Alternatively, you can specify the endpoint name and type by using the *Name* and *Type* parameters, together with the *ProfileName* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="6b8f7-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6b8f7-111">EXAMPLES</span></span>

### <span data-ttu-id="6b8f7-112">Exemplo 1: desabilitar um ponto de extremidade por nome</span><span class="sxs-lookup"><span data-stu-id="6b8f7-112">Example 1: Disable an endpoint by name</span></span>
```
PS C:\> Disable-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName ResourceGroup11 -Type ExternalEndpoints
```

<span data-ttu-id="6b8f7-113">Esse comando desabilita o ponto de extremidade externo chamado contoso no perfil chamado ContosoProfile na ResourceGroup11 do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6b8f7-113">This command disables the external endpoint named contoso in the profile named ContosoProfile in resource group ResourceGroup11.</span></span>
<span data-ttu-id="6b8f7-114">O comando solicitará confirmação.</span><span class="sxs-lookup"><span data-stu-id="6b8f7-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="6b8f7-115">Exemplo 2: desabilitar um ponto de extremidade usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="6b8f7-115">Example 2: Disable an endpoint by using the pipeline</span></span>
```
PS C:\>Get-AzTrafficManagerEndpoint -Name "contoso" -Type ExternalEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Disable-AzTrafficManagerEndpoint -Force
```

<span data-ttu-id="6b8f7-116">Esse comando obtém o ponto de extremidade externo chamado contoso do perfil chamado ContosoProfile em ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="6b8f7-116">This command gets the external endpoint named Contoso from the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="6b8f7-117">Em seguida, o comando passa esse ponto de extremidade para o cmdlet **Disable-AzTrafficManagerEndpoint** usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="6b8f7-117">The command then passes that endpoint to the **Disable-AzTrafficManagerEndpoint** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="6b8f7-118">Esse cmdlet desabilita esse ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="6b8f7-118">That cmdlet disables that endpoint.</span></span>
<span data-ttu-id="6b8f7-119">O comando especifica o parâmetro *Force* .</span><span class="sxs-lookup"><span data-stu-id="6b8f7-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="6b8f7-120">Portanto, ele não solicita a confirmação.</span><span class="sxs-lookup"><span data-stu-id="6b8f7-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="6b8f7-121">OS</span><span class="sxs-lookup"><span data-stu-id="6b8f7-121">PARAMETERS</span></span>

### <span data-ttu-id="6b8f7-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b8f7-122">-DefaultProfile</span></span>
<span data-ttu-id="6b8f7-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6b8f7-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6b8f7-124">-Force</span><span class="sxs-lookup"><span data-stu-id="6b8f7-124">-Force</span></span>
<span data-ttu-id="6b8f7-125">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="6b8f7-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6b8f7-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="6b8f7-126">-Name</span></span>
<span data-ttu-id="6b8f7-127">Especifica o nome do ponto de extremidade do Gerenciador de tráfego que esse cmdlet desabilita.</span><span class="sxs-lookup"><span data-stu-id="6b8f7-127">Specifies the name of the Traffic Manager endpoint that this cmdlet disables.</span></span>

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

### <span data-ttu-id="6b8f7-128">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="6b8f7-128">-ProfileName</span></span>
<span data-ttu-id="6b8f7-129">Especifica o nome de um perfil do Gerenciador de tráfego no qual esse cmdlet desabilita um ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="6b8f7-129">Specifies the name of a Traffic Manager profile in which this cmdlet disables an endpoint.</span></span>
<span data-ttu-id="6b8f7-130">Para obter um perfil, use o cmdlet Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="6b8f7-130">To obtain a profile, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="6b8f7-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b8f7-131">-ResourceGroupName</span></span>
<span data-ttu-id="6b8f7-132">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6b8f7-132">Specifies the name of a resource group.</span></span>
<span data-ttu-id="6b8f7-133">Esse cmdlet desabilita um ponto de extremidade do Gerenciador de tráfego no grupo especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="6b8f7-133">This cmdlet disables a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="6b8f7-134">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="6b8f7-134">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="6b8f7-135">Especifica o ponto de extremidade do Gerenciador de tráfego que esse cmdlet desabilita.</span><span class="sxs-lookup"><span data-stu-id="6b8f7-135">Specifies the Traffic Manager endpoint that this cmdlet disables.</span></span>
<span data-ttu-id="6b8f7-136">Para obter um objeto **TrafficManagerEndpoint** , use o cmdlet Get-AzTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="6b8f7-136">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="6b8f7-137">-Digite</span><span class="sxs-lookup"><span data-stu-id="6b8f7-137">-Type</span></span>
<span data-ttu-id="6b8f7-138">Especifica o tipo de ponto de extremidade que este cmdlet adiciona ao perfil do Gerenciador de tráfego.</span><span class="sxs-lookup"><span data-stu-id="6b8f7-138">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="6b8f7-139">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="6b8f7-139">Valid values are:</span></span> 

- <span data-ttu-id="6b8f7-140">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="6b8f7-140">AzureEndpoints</span></span>
- <span data-ttu-id="6b8f7-141">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="6b8f7-141">ExternalEndpoints</span></span>
- <span data-ttu-id="6b8f7-142">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="6b8f7-142">NestedEndpoints</span></span>

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

### <span data-ttu-id="6b8f7-143">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6b8f7-143">-Confirm</span></span>
<span data-ttu-id="6b8f7-144">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6b8f7-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b8f7-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b8f7-145">-WhatIf</span></span>
<span data-ttu-id="6b8f7-146">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6b8f7-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b8f7-147">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6b8f7-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b8f7-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b8f7-148">CommonParameters</span></span>
<span data-ttu-id="6b8f7-149">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b8f7-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b8f7-150">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b8f7-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b8f7-151">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6b8f7-151">INPUTS</span></span>

### <span data-ttu-id="6b8f7-152">Microsoft. Azure. Commands. Trafficmanager. Models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="6b8f7-152">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="6b8f7-153">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6b8f7-153">OUTPUTS</span></span>

### <span data-ttu-id="6b8f7-154">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6b8f7-154">System.Boolean</span></span>

## <span data-ttu-id="6b8f7-155">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6b8f7-155">NOTES</span></span>

## <span data-ttu-id="6b8f7-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6b8f7-156">RELATED LINKS</span></span>

[<span data-ttu-id="6b8f7-157">Enable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="6b8f7-157">Enable-AzTrafficManagerEndpoint</span></span>](./Enable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="6b8f7-158">Get-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="6b8f7-158">Get-AzTrafficManagerEndpoint</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="6b8f7-159">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="6b8f7-159">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="6b8f7-160">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="6b8f7-160">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="6b8f7-161">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="6b8f7-161">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="6b8f7-162">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="6b8f7-162">Remove-AzTrafficManagerEndpoint</span></span>](./Remove-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="6b8f7-163">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="6b8f7-163">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


