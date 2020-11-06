---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 8CC749F1-B961-4F8F-BAD4-2C0F4385D1C2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/disable-azurermtrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Disable-AzureRmTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Disable-AzureRmTrafficManagerEndpoint.md
ms.openlocfilehash: af05a91fe2281d457cff649bf0de6d986f7f413a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429989"
---
# <span data-ttu-id="66240-101">Disable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="66240-101">Disable-AzureRmTrafficManagerEndpoint</span></span>

## <span data-ttu-id="66240-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="66240-102">SYNOPSIS</span></span>
<span data-ttu-id="66240-103">Desabilita um ponto de extremidade em um perfil do Gerenciador de tráfego.</span><span class="sxs-lookup"><span data-stu-id="66240-103">Disables an endpoint in a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66240-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="66240-104">SYNTAX</span></span>

### <span data-ttu-id="66240-105">Campos</span><span class="sxs-lookup"><span data-stu-id="66240-105">Fields</span></span>
```
Disable-AzureRmTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String>
 -ResourceGroupName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="66240-106">Objeto</span><span class="sxs-lookup"><span data-stu-id="66240-106">Object</span></span>
```
Disable-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66240-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="66240-107">DESCRIPTION</span></span>
<span data-ttu-id="66240-108">O cmdlet **Disable-AzureRmTrafficManagerEndpoint** desabilita um ponto de extremidade em um perfil do Gerenciador de tráfego do Azure.</span><span class="sxs-lookup"><span data-stu-id="66240-108">The **Disable-AzureRmTrafficManagerEndpoint** cmdlet disables an endpoint in an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="66240-109">Você pode usar o operador pipeline para passar um objeto **TrafficManagerEndpoint** para esse cmdlet, ou pode passar um objeto **TrafficManagerEndpoint** usando o parâmetro *TrafficManagerEndpoint* .</span><span class="sxs-lookup"><span data-stu-id="66240-109">You can use the pipeline operator to pass a **TrafficManagerEndpoint** object to this cmdlet, or you can pass a **TrafficManagerEndpoint** object using the *TrafficManagerEndpoint* parameter.</span></span>

<span data-ttu-id="66240-110">Você também pode especificar o nome e o tipo de ponto de extremidade usando os parâmetros *Name* e *Type* , juntamente com os parâmetros *ProfileName* e *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="66240-110">Alternatively, you can specify the endpoint name and type by using the *Name* and *Type* parameters, together with the *ProfileName* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="66240-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="66240-111">EXAMPLES</span></span>

### <span data-ttu-id="66240-112">Exemplo 1: desabilitar um ponto de extremidade por nome</span><span class="sxs-lookup"><span data-stu-id="66240-112">Example 1: Disable an endpoint by name</span></span>
```
PS C:\> Disable-AzureRmTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName ResourceGroup11 -Type ExternalEndpoints
```

<span data-ttu-id="66240-113">Esse comando desabilita o ponto de extremidade externo chamado contoso no perfil chamado ContosoProfile na ResouceGroup11 do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="66240-113">This command disables the external endpoint named contoso in the profile named ContosoProfile in resource group ResouceGroup11.</span></span>
<span data-ttu-id="66240-114">O comando solicitará confirmação.</span><span class="sxs-lookup"><span data-stu-id="66240-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="66240-115">Exemplo 2: desabilitar um ponto de extremidade usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="66240-115">Example 2: Disable an endpoint by using the pipeline</span></span>
```
PS C:\>Get-AzureRmTrafficManagerEndpoint -Name "contoso" -Type ExternalEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Disable-AzureRmTrafficManagerEndpoint -Force
```

<span data-ttu-id="66240-116">Esse comando obtém o ponto de extremidade externo chamado contoso do perfil chamado ContosoProfile em ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="66240-116">This command gets the external endpoint named Contoso from the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="66240-117">Em seguida, o comando passa esse ponto de extremidade para o cmdlet **Disable-AzureRmTrafficManagerEndpoint** usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="66240-117">The command then passes that endpoint to the **Disable-AzureRmTrafficManagerEndpoint** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="66240-118">Esse cmdlet desabilita esse ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="66240-118">That cmdlet disables that endpoint.</span></span>
<span data-ttu-id="66240-119">O comando especifica o parâmetro *Force* .</span><span class="sxs-lookup"><span data-stu-id="66240-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="66240-120">Portanto, ele não solicita a confirmação.</span><span class="sxs-lookup"><span data-stu-id="66240-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="66240-121">OS</span><span class="sxs-lookup"><span data-stu-id="66240-121">PARAMETERS</span></span>

### <span data-ttu-id="66240-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66240-122">-DefaultProfile</span></span>
<span data-ttu-id="66240-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="66240-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66240-124">-Force</span><span class="sxs-lookup"><span data-stu-id="66240-124">-Force</span></span>
<span data-ttu-id="66240-125">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="66240-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="66240-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="66240-126">-Name</span></span>
<span data-ttu-id="66240-127">Especifica o nome do ponto de extremidade do Gerenciador de tráfego que esse cmdlet desabilita.</span><span class="sxs-lookup"><span data-stu-id="66240-127">Specifies the name of the Traffic Manager endpoint that this cmdlet disables.</span></span>

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

### <span data-ttu-id="66240-128">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="66240-128">-ProfileName</span></span>
<span data-ttu-id="66240-129">Especifica o nome de um perfil do Gerenciador de tráfego no qual esse cmdlet desabilita um ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="66240-129">Specifies the name of a Traffic Manager profile in which this cmdlet disables an endpoint.</span></span>
<span data-ttu-id="66240-130">Para obter um perfil, use o cmdlet Get-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="66240-130">To obtain a profile, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="66240-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66240-131">-ResourceGroupName</span></span>
<span data-ttu-id="66240-132">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="66240-132">Specifies the name of a resource group.</span></span>
<span data-ttu-id="66240-133">Esse cmdlet desabilita um ponto de extremidade do Gerenciador de tráfego no grupo especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="66240-133">This cmdlet disables a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="66240-134">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="66240-134">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="66240-135">Especifica o ponto de extremidade do Gerenciador de tráfego que esse cmdlet desabilita.</span><span class="sxs-lookup"><span data-stu-id="66240-135">Specifies the Traffic Manager endpoint that this cmdlet disables.</span></span>
<span data-ttu-id="66240-136">Para obter um objeto **TrafficManagerEndpoint** , use o cmdlet Get-AzureRmTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="66240-136">To obtain a **TrafficManagerEndpoint** object, use the Get-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="66240-137">-Digite</span><span class="sxs-lookup"><span data-stu-id="66240-137">-Type</span></span>
<span data-ttu-id="66240-138">Especifica o tipo de ponto de extremidade que este cmdlet adiciona ao perfil do Gerenciador de tráfego.</span><span class="sxs-lookup"><span data-stu-id="66240-138">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="66240-139">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="66240-139">Valid values are:</span></span> 

- <span data-ttu-id="66240-140">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="66240-140">AzureEndpoints</span></span>
- <span data-ttu-id="66240-141">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="66240-141">ExternalEndpoints</span></span>
- <span data-ttu-id="66240-142">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="66240-142">NestedEndpoints</span></span>

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

### <span data-ttu-id="66240-143">-Confirme</span><span class="sxs-lookup"><span data-stu-id="66240-143">-Confirm</span></span>
<span data-ttu-id="66240-144">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="66240-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66240-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66240-145">-WhatIf</span></span>
<span data-ttu-id="66240-146">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="66240-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66240-147">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="66240-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66240-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66240-148">CommonParameters</span></span>
<span data-ttu-id="66240-149">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66240-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66240-150">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66240-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66240-151">SENSORES</span><span class="sxs-lookup"><span data-stu-id="66240-151">INPUTS</span></span>

### <span data-ttu-id="66240-152">TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="66240-152">TrafficManagerEndpoint</span></span>
<span data-ttu-id="66240-153">O parâmetro ' TrafficManagerEndpoint ' aceita o valor do tipo ' TrafficManagerEndpoint ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="66240-153">Parameter 'TrafficManagerEndpoint' accepts value of type 'TrafficManagerEndpoint' from the pipeline</span></span>

## <span data-ttu-id="66240-154">EXIBE</span><span class="sxs-lookup"><span data-stu-id="66240-154">OUTPUTS</span></span>

### <span data-ttu-id="66240-155">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="66240-155">System.Boolean</span></span>

## <span data-ttu-id="66240-156">INFORMA</span><span class="sxs-lookup"><span data-stu-id="66240-156">NOTES</span></span>

## <span data-ttu-id="66240-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="66240-157">RELATED LINKS</span></span>

[<span data-ttu-id="66240-158">Enable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="66240-158">Enable-AzureRmTrafficManagerEndpoint</span></span>](./Enable-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="66240-159">Get-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="66240-159">Get-AzureRmTrafficManagerEndpoint</span></span>](./Get-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="66240-160">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="66240-160">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="66240-161">New-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="66240-161">New-AzureRmTrafficManagerEndpoint</span></span>](./New-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="66240-162">New-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="66240-162">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="66240-163">Remove-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="66240-163">Remove-AzureRmTrafficManagerEndpoint</span></span>](./Remove-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="66240-164">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="66240-164">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


