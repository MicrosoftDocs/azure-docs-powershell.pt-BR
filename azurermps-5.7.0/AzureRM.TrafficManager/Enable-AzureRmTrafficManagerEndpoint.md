---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM
ms.assetid: 32263236-C207-4FE0-AB8A-018118FC7729
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/enable-azurermtrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Enable-AzureRmTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Enable-AzureRmTrafficManagerEndpoint.md
ms.openlocfilehash: 9412a75ff595424637b36fb64db82ba556c9a057
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432372"
---
# <span data-ttu-id="8fdf0-101">Enable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="8fdf0-101">Enable-AzureRmTrafficManagerEndpoint</span></span>

## <span data-ttu-id="8fdf0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8fdf0-102">SYNOPSIS</span></span>
<span data-ttu-id="8fdf0-103">Habilita um ponto de extremidade em um perfil do Gerenciador de tráfego.</span><span class="sxs-lookup"><span data-stu-id="8fdf0-103">Enables an endpoint in a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8fdf0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8fdf0-104">SYNTAX</span></span>

### <span data-ttu-id="8fdf0-105">Campos</span><span class="sxs-lookup"><span data-stu-id="8fdf0-105">Fields</span></span>
```
Enable-AzureRmTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8fdf0-106">Objeto</span><span class="sxs-lookup"><span data-stu-id="8fdf0-106">Object</span></span>
```
Enable-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8fdf0-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8fdf0-107">DESCRIPTION</span></span>
<span data-ttu-id="8fdf0-108">O cmdlet **Enable-AzureRmTrafficManagerEndpoint** habilita um ponto de extremidade em um perfil do Gerenciador de tráfego do Azure.</span><span class="sxs-lookup"><span data-stu-id="8fdf0-108">The **Enable-AzureRmTrafficManagerEndpoint** cmdlet enables an endpoint in an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="8fdf0-109">Você pode usar o operador pipeline para passar um objeto **TrafficManagerEndpoint** para esse cmdlet ou pode especificar um objeto **TrafficManagerEndpoint** usando o parâmetro *TrafficManagerEndpoint* .</span><span class="sxs-lookup"><span data-stu-id="8fdf0-109">You can use the pipeline operator to pass a **TrafficManagerEndpoint** object to this cmdlet, or you can specify a **TrafficManagerEndpoint** object by using the *TrafficManagerEndpoint* parameter.</span></span>

<span data-ttu-id="8fdf0-110">Você também pode especificar o nome e o tipo de ponto de extremidade usando os parâmetros *Name* e *Type* , juntamente com os parâmetros *ProfileName* e *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="8fdf0-110">Alternatively, you can specify the endpoint name and type by using the *Name* and *Type* parameters, together with the *ProfileName* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="8fdf0-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8fdf0-111">EXAMPLES</span></span>

### <span data-ttu-id="8fdf0-112">Exemplo 1: habilitar um ponto de extremidade de um perfil</span><span class="sxs-lookup"><span data-stu-id="8fdf0-112">Example 1: Enable an endpoint from a profile</span></span>
```
PS C:\>Enable-AzureRmTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName ResourceGroup11 -Type ExternalEndpoints
```

<span data-ttu-id="8fdf0-113">Esse comando habilita o ponto de extremidade externo chamado contoso no perfil chamado ContosoProfile na ResouceGroup11 do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8fdf0-113">This command enables the external endpoint named contoso in the profile named ContosoProfile in resource group ResouceGroup11.</span></span>

### <span data-ttu-id="8fdf0-114">Exemplo 2: habilitar um ponto de extremidade usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="8fdf0-114">Example 2: Enable an endpoint by using the pipeline</span></span>
```
PS C:\>Get-AzureRmTrafficManagerEndpoint -Name "contoso" -Type ExternalEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Enable-AzureRmTrafficManagerEndpoint
```

<span data-ttu-id="8fdf0-115">Esse comando obtém o ponto de extremidade externo chamado contoso do perfil chamado ContosoProfile em ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="8fdf0-115">This command gets the external endpoint named Contoso from the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="8fdf0-116">Em seguida, o comando passa esse ponto de extremidade para o cmdlet **Enable-AzureRmTrafficManagerEndpoint** usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="8fdf0-116">The command then passes that endpoint to the **Enable-AzureRmTrafficManagerEndpoint** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="8fdf0-117">Esse cmdlet habilita esse ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="8fdf0-117">That cmdlet enables that endpoint.</span></span>

## <span data-ttu-id="8fdf0-118">OS</span><span class="sxs-lookup"><span data-stu-id="8fdf0-118">PARAMETERS</span></span>

### <span data-ttu-id="8fdf0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fdf0-119">-DefaultProfile</span></span>
<span data-ttu-id="8fdf0-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8fdf0-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8fdf0-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="8fdf0-121">-Name</span></span>
<span data-ttu-id="8fdf0-122">Especifica o nome do ponto de extremidade do Gerenciador de tráfego que o cmdlet habilita.</span><span class="sxs-lookup"><span data-stu-id="8fdf0-122">Specifies the name of the Traffic Manager endpoint that this cmdlet enables.</span></span>

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

### <span data-ttu-id="8fdf0-123">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="8fdf0-123">-ProfileName</span></span>
<span data-ttu-id="8fdf0-124">Especifica o nome de um perfil do Gerenciador de tráfego no qual esse cmdlet habilita um ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="8fdf0-124">Specifies the name of a Traffic Manager profile in which this cmdlet enables an endpoint.</span></span>
<span data-ttu-id="8fdf0-125">Para obter um perfil, use o cmdlet Get-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="8fdf0-125">To obtain a profile, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="8fdf0-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8fdf0-126">-ResourceGroupName</span></span>
<span data-ttu-id="8fdf0-127">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8fdf0-127">Specifies the name of a resource group.</span></span>
<span data-ttu-id="8fdf0-128">Esse cmdlet habilita um ponto de extremidade do Gerenciador de tráfego no grupo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="8fdf0-128">This cmdlet enables a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="8fdf0-129">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="8fdf0-129">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="8fdf0-130">Especifica o ponto de extremidade do Gerenciador de tráfego que este cmdlet habilita.</span><span class="sxs-lookup"><span data-stu-id="8fdf0-130">Specifies the Traffic Manager endpoint that this cmdlet enables.</span></span>
<span data-ttu-id="8fdf0-131">Para obter um objeto **TrafficManagerEndpoint** , use o cmdlet Get-AzureRmTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="8fdf0-131">To obtain a **TrafficManagerEndpoint** object, use the Get-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="8fdf0-132">-Digite</span><span class="sxs-lookup"><span data-stu-id="8fdf0-132">-Type</span></span>
<span data-ttu-id="8fdf0-133">Especifica o tipo de ponto de extremidade que esse cmdlet desabilita no perfil do Gerenciador de tráfego.</span><span class="sxs-lookup"><span data-stu-id="8fdf0-133">Specifies the type of endpoint that this cmdlet disables in the Traffic Manager profile.</span></span>
<span data-ttu-id="8fdf0-134">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="8fdf0-134">Valid values are:</span></span> 

- <span data-ttu-id="8fdf0-135">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="8fdf0-135">AzureEndpoints</span></span>
- <span data-ttu-id="8fdf0-136">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="8fdf0-136">ExternalEndpoints</span></span>
- <span data-ttu-id="8fdf0-137">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="8fdf0-137">NestedEndpoints</span></span>

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

### <span data-ttu-id="8fdf0-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fdf0-138">CommonParameters</span></span>
<span data-ttu-id="8fdf0-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8fdf0-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fdf0-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8fdf0-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fdf0-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8fdf0-141">INPUTS</span></span>

### <span data-ttu-id="8fdf0-142">TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="8fdf0-142">TrafficManagerEndpoint</span></span>
<span data-ttu-id="8fdf0-143">O parâmetro ' TrafficManagerEndpoint ' aceita o valor do tipo ' TrafficManagerEndpoint ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="8fdf0-143">Parameter 'TrafficManagerEndpoint' accepts value of type 'TrafficManagerEndpoint' from the pipeline</span></span>

## <span data-ttu-id="8fdf0-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8fdf0-144">OUTPUTS</span></span>

### <span data-ttu-id="8fdf0-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8fdf0-145">System.Boolean</span></span>

## <span data-ttu-id="8fdf0-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8fdf0-146">NOTES</span></span>

## <span data-ttu-id="8fdf0-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8fdf0-147">RELATED LINKS</span></span>

[<span data-ttu-id="8fdf0-148">Disable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="8fdf0-148">Disable-AzureRmTrafficManagerEndpoint</span></span>](./Disable-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="8fdf0-149">Get-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="8fdf0-149">Get-AzureRmTrafficManagerEndpoint</span></span>](./Get-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="8fdf0-150">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="8fdf0-150">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="8fdf0-151">New-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="8fdf0-151">New-AzureRmTrafficManagerEndpoint</span></span>](./New-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="8fdf0-152">New-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="8fdf0-152">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="8fdf0-153">Remove-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="8fdf0-153">Remove-AzureRmTrafficManagerEndpoint</span></span>](./Remove-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="8fdf0-154">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="8fdf0-154">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)

