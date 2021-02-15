---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 8CC749F1-B961-4F8F-BAD4-2C0F4385D1C2
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/disable-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Disable-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Disable-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 037a670c0e96d1a9014cd19b32a7d2ba4da282ba
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116287"
---
# <span data-ttu-id="b53dd-101">Disable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b53dd-101">Disable-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="b53dd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b53dd-102">SYNOPSIS</span></span>
<span data-ttu-id="b53dd-103">Desabilita um ponto de extremidade em um perfil do Gerenciador de Tráfego.</span><span class="sxs-lookup"><span data-stu-id="b53dd-103">Disables an endpoint in a Traffic Manager profile.</span></span>

## <span data-ttu-id="b53dd-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b53dd-104">SYNTAX</span></span>

### <span data-ttu-id="b53dd-105">Campos</span><span class="sxs-lookup"><span data-stu-id="b53dd-105">Fields</span></span>
```
Disable-AzTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String>
 -ResourceGroupName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b53dd-106">Objeto</span><span class="sxs-lookup"><span data-stu-id="b53dd-106">Object</span></span>
```
Disable-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b53dd-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="b53dd-107">DESCRIPTION</span></span>
<span data-ttu-id="b53dd-108">O cmdlet **Disable-AzTrafficManagerEndpoint** desabilita um ponto de extremidade em um perfil do Gerenciador de Tráfego do Azure.</span><span class="sxs-lookup"><span data-stu-id="b53dd-108">The **Disable-AzTrafficManagerEndpoint** cmdlet disables an endpoint in an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="b53dd-109">Você pode usar o operador de pipeline para passar um objeto **TrafficManagerEndpoint** para esse cmdlet ou pode passar um objeto **TrafficManagerEndpoint** usando o parâmetro *TrafficManagerEndpoint.*</span><span class="sxs-lookup"><span data-stu-id="b53dd-109">You can use the pipeline operator to pass a **TrafficManagerEndpoint** object to this cmdlet, or you can pass a **TrafficManagerEndpoint** object using the *TrafficManagerEndpoint* parameter.</span></span>

<span data-ttu-id="b53dd-110">Como alternativa, você pode especificar o nome  e  o tipo do ponto de extremidade usando os parâmetros Nome e Tipo, juntamente com os parâmetros *ProfileName* e *ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="b53dd-110">Alternatively, you can specify the endpoint name and type by using the *Name* and *Type* parameters, together with the *ProfileName* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="b53dd-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b53dd-111">EXAMPLES</span></span>

### <span data-ttu-id="b53dd-112">Exemplo 1: Desabilitar um ponto de extremidade por nome</span><span class="sxs-lookup"><span data-stu-id="b53dd-112">Example 1: Disable an endpoint by name</span></span>
```
PS C:\> Disable-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName ResourceGroup11 -Type ExternalEndpoints
```

<span data-ttu-id="b53dd-113">Esse comando desabilita o ponto de extremidade externo chamado contoso no perfil chamado ContosoProfile no grupo de recursos ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="b53dd-113">This command disables the external endpoint named contoso in the profile named ContosoProfile in resource group ResourceGroup11.</span></span>
<span data-ttu-id="b53dd-114">O comando solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="b53dd-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="b53dd-115">Exemplo 2: Desabilitar um ponto de extremidade usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="b53dd-115">Example 2: Disable an endpoint by using the pipeline</span></span>
```
PS C:\>Get-AzTrafficManagerEndpoint -Name "contoso" -Type ExternalEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Disable-AzTrafficManagerEndpoint -Force
```

<span data-ttu-id="b53dd-116">Esse comando obtém o ponto de extremidade externo chamado Contoso do perfil contosoProfile no ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="b53dd-116">This command gets the external endpoint named Contoso from the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="b53dd-117">Em seguida, o comando passa esse ponto de extremidade para o cmdlet **Disable-AzTrafficManagerEndpoint** usando o operador de pipeline.</span><span class="sxs-lookup"><span data-stu-id="b53dd-117">The command then passes that endpoint to the **Disable-AzTrafficManagerEndpoint** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="b53dd-118">Esse cmdlet desabilita esse ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="b53dd-118">That cmdlet disables that endpoint.</span></span>
<span data-ttu-id="b53dd-119">O comando especifica o parâmetro *Forçar.*</span><span class="sxs-lookup"><span data-stu-id="b53dd-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="b53dd-120">Portanto, ele não solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="b53dd-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="b53dd-121">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b53dd-121">PARAMETERS</span></span>

### <span data-ttu-id="b53dd-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b53dd-122">-DefaultProfile</span></span>
<span data-ttu-id="b53dd-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="b53dd-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b53dd-124">-Forçar</span><span class="sxs-lookup"><span data-stu-id="b53dd-124">-Force</span></span>
<span data-ttu-id="b53dd-125">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="b53dd-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b53dd-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="b53dd-126">-Name</span></span>
<span data-ttu-id="b53dd-127">Especifica o nome do ponto de extremidade do Gerenciador de Tráfego desabilitado por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b53dd-127">Specifies the name of the Traffic Manager endpoint that this cmdlet disables.</span></span>

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

### <span data-ttu-id="b53dd-128">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="b53dd-128">-ProfileName</span></span>
<span data-ttu-id="b53dd-129">Especifica o nome de um perfil do Gerenciador de Tráfego no qual esse cmdlet desabilita um ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="b53dd-129">Specifies the name of a Traffic Manager profile in which this cmdlet disables an endpoint.</span></span>
<span data-ttu-id="b53dd-130">Para obter um perfil, use o Get-AzTrafficManagerProfile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b53dd-130">To obtain a profile, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="b53dd-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b53dd-131">-ResourceGroupName</span></span>
<span data-ttu-id="b53dd-132">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b53dd-132">Specifies the name of a resource group.</span></span>
<span data-ttu-id="b53dd-133">Esse cmdlet desabilita um ponto de extremidade do Gerenciador de Tráfego no grupo especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="b53dd-133">This cmdlet disables a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="b53dd-134">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b53dd-134">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="b53dd-135">Especifica o ponto de extremidade do Gerenciador de Tráfego desabilitado por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b53dd-135">Specifies the Traffic Manager endpoint that this cmdlet disables.</span></span>
<span data-ttu-id="b53dd-136">Para obter um **objeto TrafficManagerEndpoint,** use Get-AzTrafficManagerEndpoint cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b53dd-136">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="b53dd-137">-Tipo</span><span class="sxs-lookup"><span data-stu-id="b53dd-137">-Type</span></span>
<span data-ttu-id="b53dd-138">Especifica o tipo de ponto de extremidade que esse cmdlet adiciona ao perfil do Gerenciador de Tráfego.</span><span class="sxs-lookup"><span data-stu-id="b53dd-138">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="b53dd-139">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="b53dd-139">Valid values are:</span></span> 

- <span data-ttu-id="b53dd-140">Pontos do AzureEnd</span><span class="sxs-lookup"><span data-stu-id="b53dd-140">AzureEndpoints</span></span>
- <span data-ttu-id="b53dd-141">Pontos Externos</span><span class="sxs-lookup"><span data-stu-id="b53dd-141">ExternalEndpoints</span></span>
- <span data-ttu-id="b53dd-142">Pontos aninhados</span><span class="sxs-lookup"><span data-stu-id="b53dd-142">NestedEndpoints</span></span>

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

### <span data-ttu-id="b53dd-143">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="b53dd-143">-Confirm</span></span>
<span data-ttu-id="b53dd-144">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b53dd-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b53dd-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b53dd-145">-WhatIf</span></span>
<span data-ttu-id="b53dd-146">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="b53dd-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b53dd-147">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b53dd-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b53dd-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b53dd-148">CommonParameters</span></span>
<span data-ttu-id="b53dd-149">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b53dd-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b53dd-150">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b53dd-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b53dd-151">Entradas</span><span class="sxs-lookup"><span data-stu-id="b53dd-151">INPUTS</span></span>

### <span data-ttu-id="b53dd-152">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b53dd-152">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="b53dd-153">Saídas</span><span class="sxs-lookup"><span data-stu-id="b53dd-153">OUTPUTS</span></span>

### <span data-ttu-id="b53dd-154">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b53dd-154">System.Boolean</span></span>

## <span data-ttu-id="b53dd-155">Notas</span><span class="sxs-lookup"><span data-stu-id="b53dd-155">NOTES</span></span>

## <span data-ttu-id="b53dd-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b53dd-156">RELATED LINKS</span></span>

[<span data-ttu-id="b53dd-157">Enable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b53dd-157">Enable-AzTrafficManagerEndpoint</span></span>](./Enable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="b53dd-158">Get-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b53dd-158">Get-AzTrafficManagerEndpoint</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="b53dd-159">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b53dd-159">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="b53dd-160">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b53dd-160">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="b53dd-161">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b53dd-161">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="b53dd-162">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b53dd-162">Remove-AzTrafficManagerEndpoint</span></span>](./Remove-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="b53dd-163">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b53dd-163">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


