---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM
ms.assetid: 4556C345-55D0-431C-B980-219D5ED14E5F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/get-azurermtrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Get-AzureRmTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Get-AzureRmTrafficManagerEndpoint.md
ms.openlocfilehash: 488643c8f977fb59af0f5b73c9388e65b3425c1d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432369"
---
# <span data-ttu-id="eb8c0-101">Get-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="eb8c0-101">Get-AzureRmTrafficManagerEndpoint</span></span>

## <span data-ttu-id="eb8c0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="eb8c0-102">SYNOPSIS</span></span>
<span data-ttu-id="eb8c0-103">Obtém um ponto de extremidade para um perfil do Gerenciador de tráfego.</span><span class="sxs-lookup"><span data-stu-id="eb8c0-103">Gets an endpoint for a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eb8c0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="eb8c0-104">SYNTAX</span></span>

### <span data-ttu-id="eb8c0-105">Campos</span><span class="sxs-lookup"><span data-stu-id="eb8c0-105">Fields</span></span>
```
Get-AzureRmTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eb8c0-106">Objeto</span><span class="sxs-lookup"><span data-stu-id="eb8c0-106">Object</span></span>
```
Get-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eb8c0-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="eb8c0-107">DESCRIPTION</span></span>
<span data-ttu-id="eb8c0-108">O cmdlet **Get-AzureRmTrafficManagerEndpoint** Obtém um ponto de extremidade para um perfil do Gerenciador de tráfego do Azure.</span><span class="sxs-lookup"><span data-stu-id="eb8c0-108">The **Get-AzureRmTrafficManagerEndpoint** cmdlet gets an endpoint for an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="eb8c0-109">Você pode modificar esse objeto localmente e, em seguida, aplicar as alterações ao perfil usando o cmdlet Set-AzureRmTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="eb8c0-109">You can modify this object locally, and then apply changes to the profile by using the Set-AzureRmTrafficManagerEndpoint cmdlet.</span></span>
<span data-ttu-id="eb8c0-110">Especifique o ponto de extremidade usando os parâmetros *Name* e *Type* .</span><span class="sxs-lookup"><span data-stu-id="eb8c0-110">Specify the endpoint by using the *Name* and *Type* parameters.</span></span>
<span data-ttu-id="eb8c0-111">Você pode especificar o perfil do Gerenciador de tráfego usando o parâmetro *ProfileName* e *ResourceGroupName* ou especificando um objeto **TrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="eb8c0-111">You can specify the Traffic Manager profile either by using the *ProfileName* and *ResourceGroupName* parameter, or by specifying a **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="eb8c0-112">Você também pode passar esse valor usando o pipeline.</span><span class="sxs-lookup"><span data-stu-id="eb8c0-112">Alternatively, you can pass that value by using the pipeline.</span></span>

## <span data-ttu-id="eb8c0-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="eb8c0-113">EXAMPLES</span></span>

### <span data-ttu-id="eb8c0-114">Exemplo 1: obter um ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="eb8c0-114">Example 1: Get an endpoint</span></span>
```
PS C:\>$TrafficManagerEndpoint = Get-AzureRmTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
```

<span data-ttu-id="eb8c0-115">Esse comando obtém o ponto de extremidade do Azure chamado contoso do perfil chamado ContosoProfile no grupo de recursos chamado ResourceGroup11 e, em seguida, armazena esse objeto na variável $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="eb8c0-115">This command gets the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11, and then stores that object in the $TrafficManagerEndpoint variable.</span></span>

## <span data-ttu-id="eb8c0-116">OS</span><span class="sxs-lookup"><span data-stu-id="eb8c0-116">PARAMETERS</span></span>

### <span data-ttu-id="eb8c0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb8c0-117">-DefaultProfile</span></span>
<span data-ttu-id="eb8c0-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="eb8c0-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eb8c0-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="eb8c0-119">-Name</span></span>
<span data-ttu-id="eb8c0-120">Especifica o nome do ponto de extremidade do Gerenciador de tráfego que o cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="eb8c0-120">Specifies the name of the Traffic Manager endpoint that this cmdlet gets.</span></span>

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

### <span data-ttu-id="eb8c0-121">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="eb8c0-121">-ProfileName</span></span>
<span data-ttu-id="eb8c0-122">Especifica o nome do ponto de extremidade do Gerenciador de tráfego que o cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="eb8c0-122">Specifies the name of the Traffic Manager endpoint that this cmdlet gets.</span></span>

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

### <span data-ttu-id="eb8c0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb8c0-123">-ResourceGroupName</span></span>
<span data-ttu-id="eb8c0-124">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="eb8c0-124">Specifies the name of a resource group.</span></span>
<span data-ttu-id="eb8c0-125">Esse cmdlet obtém um ponto de extremidade do Gerenciador de tráfego no grupo especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="eb8c0-125">This cmdlet gets a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="eb8c0-126">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="eb8c0-126">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="eb8c0-127">Especifica o ponto de extremidade do Gerenciador de tráfego que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="eb8c0-127">Specifies the Traffic Manager endpoint that this cmdlet gets.</span></span>

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

### <span data-ttu-id="eb8c0-128">-Digite</span><span class="sxs-lookup"><span data-stu-id="eb8c0-128">-Type</span></span>
<span data-ttu-id="eb8c0-129">Especifica o tipo de ponto de extremidade que este cmdlet adiciona ao perfil do Gerenciador de tráfego.</span><span class="sxs-lookup"><span data-stu-id="eb8c0-129">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="eb8c0-130">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="eb8c0-130">Valid values are:</span></span> 

- <span data-ttu-id="eb8c0-131">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="eb8c0-131">AzureEndpoints</span></span>
- <span data-ttu-id="eb8c0-132">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="eb8c0-132">ExternalEndpoints</span></span>
- <span data-ttu-id="eb8c0-133">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="eb8c0-133">NestedEndpoints</span></span>

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

### <span data-ttu-id="eb8c0-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb8c0-134">CommonParameters</span></span>
<span data-ttu-id="eb8c0-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb8c0-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb8c0-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb8c0-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb8c0-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="eb8c0-137">INPUTS</span></span>

### <span data-ttu-id="eb8c0-138">TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="eb8c0-138">TrafficManagerEndpoint</span></span>
<span data-ttu-id="eb8c0-139">O parâmetro ' TrafficManagerEndpoint ' aceita o valor do tipo ' TrafficManagerEndpoint ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="eb8c0-139">Parameter 'TrafficManagerEndpoint' accepts value of type 'TrafficManagerEndpoint' from the pipeline</span></span>

## <span data-ttu-id="eb8c0-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="eb8c0-140">OUTPUTS</span></span>

### <span data-ttu-id="eb8c0-141">Microsoft. Azure. Commands. Trafficmanager. Models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="eb8c0-141">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="eb8c0-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="eb8c0-142">NOTES</span></span>

## <span data-ttu-id="eb8c0-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="eb8c0-143">RELATED LINKS</span></span>

[<span data-ttu-id="eb8c0-144">Disable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="eb8c0-144">Disable-AzureRmTrafficManagerEndpoint</span></span>](./Disable-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="eb8c0-145">Enable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="eb8c0-145">Enable-AzureRmTrafficManagerEndpoint</span></span>](./Enable-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="eb8c0-146">New-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="eb8c0-146">New-AzureRmTrafficManagerEndpoint</span></span>](./New-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="eb8c0-147">Remove-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="eb8c0-147">Remove-AzureRmTrafficManagerEndpoint</span></span>](./Remove-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="eb8c0-148">Set-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="eb8c0-148">Set-AzureRmTrafficManagerEndpoint</span></span>](./Set-AzureRmTrafficManagerEndpoint.md)


