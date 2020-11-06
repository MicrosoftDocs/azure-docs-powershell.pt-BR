---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 8CC749F1-B961-4F8F-BAD4-2C0F4385D1C2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Disable-AzureRmTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Disable-AzureRmTrafficManagerEndpoint.md
ms.openlocfilehash: 1481b577e248354eb2fdccbb9d6ecd450ab0cf62
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441520"
---
# <span data-ttu-id="c5f30-101">Disable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="c5f30-101">Disable-AzureRmTrafficManagerEndpoint</span></span>

## <span data-ttu-id="c5f30-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c5f30-102">SYNOPSIS</span></span>
<span data-ttu-id="c5f30-103">Desabilita um ponto de extremidade em um perfil do Gerenciador de tráfego.</span><span class="sxs-lookup"><span data-stu-id="c5f30-103">Disables an endpoint in a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c5f30-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c5f30-104">SYNTAX</span></span>

### <span data-ttu-id="c5f30-105">Campos</span><span class="sxs-lookup"><span data-stu-id="c5f30-105">Fields</span></span>
```
Disable-AzureRmTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String>
 -ResourceGroupName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c5f30-106">Objeto</span><span class="sxs-lookup"><span data-stu-id="c5f30-106">Object</span></span>
```
Disable-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5f30-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c5f30-107">DESCRIPTION</span></span>
<span data-ttu-id="c5f30-108">O cmdlet **Disable-AzureRmTrafficManagerEndpoint** desabilita um ponto de extremidade em um perfil do Gerenciador de tráfego do Azure.</span><span class="sxs-lookup"><span data-stu-id="c5f30-108">The **Disable-AzureRmTrafficManagerEndpoint** cmdlet disables an endpoint in an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="c5f30-109">Você pode usar o operador pipeline para passar um objeto **TrafficManagerEndpoint** para esse cmdlet, ou pode passar um objeto **TrafficManagerEndpoint** usando o parâmetro *TrafficManagerEndpoint* .</span><span class="sxs-lookup"><span data-stu-id="c5f30-109">You can use the pipeline operator to pass a **TrafficManagerEndpoint** object to this cmdlet, or you can pass a **TrafficManagerEndpoint** object using the *TrafficManagerEndpoint* parameter.</span></span>

<span data-ttu-id="c5f30-110">Você também pode especificar o nome e o tipo de ponto de extremidade usando os parâmetros *Name* e *Type* , juntamente com os parâmetros *ProfileName* e *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="c5f30-110">Alternatively, you can specify the endpoint name and type by using the *Name* and *Type* parameters, together with the *ProfileName* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="c5f30-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c5f30-111">EXAMPLES</span></span>

### <span data-ttu-id="c5f30-112">Exemplo 1: desabilitar um ponto de extremidade por nome</span><span class="sxs-lookup"><span data-stu-id="c5f30-112">Example 1: Disable an endpoint by name</span></span>
```
PS C:\> Disable-AzureRmTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName ResourceGroup11 -Type ExternalEndpoints
```

<span data-ttu-id="c5f30-113">Esse comando desabilita o ponto de extremidade externo chamado contoso no perfil chamado ContosoProfile na ResouceGroup11 do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c5f30-113">This command disables the external endpoint named contoso in the profile named ContosoProfile in resource group ResouceGroup11.</span></span>
<span data-ttu-id="c5f30-114">O comando solicitará confirmação.</span><span class="sxs-lookup"><span data-stu-id="c5f30-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="c5f30-115">Exemplo 2: desabilitar um ponto de extremidade usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="c5f30-115">Example 2: Disable an endpoint by using the pipeline</span></span>
```
PS C:\>Get-AzureRmTrafficManagerEndpoint -Name "contoso" -Type ExternalEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Disable-AzureRmTrafficManagerEndpoint -Force
```

<span data-ttu-id="c5f30-116">Esse comando obtém o ponto de extremidade externo chamado contoso do perfil chamado ContosoProfile em ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="c5f30-116">This command gets the external endpoint named Contoso from the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="c5f30-117">Em seguida, o comando passa esse ponto de extremidade para o cmdlet **Disable-AzureRmTrafficManagerEndpoint** usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="c5f30-117">The command then passes that endpoint to the **Disable-AzureRmTrafficManagerEndpoint** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="c5f30-118">Esse cmdlet desabilita esse ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="c5f30-118">That cmdlet disables that endpoint.</span></span>
<span data-ttu-id="c5f30-119">O comando especifica o parâmetro *Force* .</span><span class="sxs-lookup"><span data-stu-id="c5f30-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="c5f30-120">Portanto, ele não solicita a confirmação.</span><span class="sxs-lookup"><span data-stu-id="c5f30-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="c5f30-121">OS</span><span class="sxs-lookup"><span data-stu-id="c5f30-121">PARAMETERS</span></span>

### <span data-ttu-id="c5f30-122">-Force</span><span class="sxs-lookup"><span data-stu-id="c5f30-122">-Force</span></span>
<span data-ttu-id="c5f30-123">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="c5f30-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c5f30-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="c5f30-124">-Name</span></span>
<span data-ttu-id="c5f30-125">Especifica o nome do ponto de extremidade do Gerenciador de tráfego que esse cmdlet desabilita.</span><span class="sxs-lookup"><span data-stu-id="c5f30-125">Specifies the name of the Traffic Manager endpoint that this cmdlet disables.</span></span>

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

### <span data-ttu-id="c5f30-126">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="c5f30-126">-ProfileName</span></span>
<span data-ttu-id="c5f30-127">Especifica o nome de um perfil do Gerenciador de tráfego no qual esse cmdlet desabilita um ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="c5f30-127">Specifies the name of a Traffic Manager profile in which this cmdlet disables an endpoint.</span></span>
<span data-ttu-id="c5f30-128">Para obter um perfil, use o cmdlet Get-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="c5f30-128">To obtain a profile, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="c5f30-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5f30-129">-ResourceGroupName</span></span>
<span data-ttu-id="c5f30-130">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c5f30-130">Specifies the name of a resource group.</span></span>
<span data-ttu-id="c5f30-131">Esse cmdlet desabilita um ponto de extremidade do Gerenciador de tráfego no grupo especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="c5f30-131">This cmdlet disables a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="c5f30-132">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="c5f30-132">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="c5f30-133">Especifica o ponto de extremidade do Gerenciador de tráfego que esse cmdlet desabilita.</span><span class="sxs-lookup"><span data-stu-id="c5f30-133">Specifies the Traffic Manager endpoint that this cmdlet disables.</span></span>
<span data-ttu-id="c5f30-134">Para obter um objeto **TrafficManagerEndpoint** , use o cmdlet Get-AzureRmTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="c5f30-134">To obtain a **TrafficManagerEndpoint** object, use the Get-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="c5f30-135">-Digite</span><span class="sxs-lookup"><span data-stu-id="c5f30-135">-Type</span></span>
<span data-ttu-id="c5f30-136">Especifica o tipo de ponto de extremidade que este cmdlet adiciona ao perfil do Gerenciador de tráfego.</span><span class="sxs-lookup"><span data-stu-id="c5f30-136">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="c5f30-137">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="c5f30-137">Valid values are:</span></span> 

- <span data-ttu-id="c5f30-138">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="c5f30-138">AzureEndpoints</span></span>
- <span data-ttu-id="c5f30-139">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="c5f30-139">ExternalEndpoints</span></span>
- <span data-ttu-id="c5f30-140">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="c5f30-140">NestedEndpoints</span></span>

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

### <span data-ttu-id="c5f30-141">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c5f30-141">-Confirm</span></span>
<span data-ttu-id="c5f30-142">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c5f30-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5f30-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5f30-143">-WhatIf</span></span>
<span data-ttu-id="c5f30-144">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c5f30-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5f30-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c5f30-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5f30-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5f30-146">-DefaultProfile</span></span>
<span data-ttu-id="c5f30-147">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c5f30-147">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c5f30-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5f30-148">CommonParameters</span></span>
<span data-ttu-id="c5f30-149">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5f30-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5f30-150">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5f30-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5f30-151">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c5f30-151">INPUTS</span></span>

### <span data-ttu-id="c5f30-152">TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="c5f30-152">TrafficManagerEndpoint</span></span>
<span data-ttu-id="c5f30-153">O parâmetro ' TrafficManagerEndpoint ' aceita o valor do tipo ' TrafficManagerEndpoint ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="c5f30-153">Parameter 'TrafficManagerEndpoint' accepts value of type 'TrafficManagerEndpoint' from the pipeline</span></span>

## <span data-ttu-id="c5f30-154">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c5f30-154">OUTPUTS</span></span>

### <span data-ttu-id="c5f30-155">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c5f30-155">System.Boolean</span></span>

## <span data-ttu-id="c5f30-156">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c5f30-156">NOTES</span></span>

## <span data-ttu-id="c5f30-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c5f30-157">RELATED LINKS</span></span>

[<span data-ttu-id="c5f30-158">Enable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="c5f30-158">Enable-AzureRmTrafficManagerEndpoint</span></span>](./Enable-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="c5f30-159">Get-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="c5f30-159">Get-AzureRmTrafficManagerEndpoint</span></span>](./Get-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="c5f30-160">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c5f30-160">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="c5f30-161">New-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="c5f30-161">New-AzureRmTrafficManagerEndpoint</span></span>](./New-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="c5f30-162">New-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c5f30-162">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="c5f30-163">Remove-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="c5f30-163">Remove-AzureRmTrafficManagerEndpoint</span></span>](./Remove-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="c5f30-164">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c5f30-164">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


