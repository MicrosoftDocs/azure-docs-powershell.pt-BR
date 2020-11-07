---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 8E12A392-A100-4814-9003-B2999150DCE1
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagerendpointconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpointConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpointConfig.md
ms.openlocfilehash: f40587460cf5e4a1d7f06bfb88229f6e4e3f7975
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93774373"
---
# <span data-ttu-id="a9c61-101">Remove-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="a9c61-101">Remove-AzTrafficManagerEndpointConfig</span></span>

## <span data-ttu-id="a9c61-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a9c61-102">SYNOPSIS</span></span>
<span data-ttu-id="a9c61-103">Remove um ponto de extremidade de um objeto de perfil do Gerenciador de tráfego local.</span><span class="sxs-lookup"><span data-stu-id="a9c61-103">Removes an endpoint from a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="a9c61-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a9c61-104">SYNTAX</span></span>

```
Remove-AzTrafficManagerEndpointConfig -EndpointName <String> -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9c61-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a9c61-105">DESCRIPTION</span></span>
<span data-ttu-id="a9c61-106">O cmdlet **Remove-AzTrafficManagerEndpointConfig** remove um ponto de extremidade de um objeto de perfil do Gerenciador de tráfego do Azure local.</span><span class="sxs-lookup"><span data-stu-id="a9c61-106">The **Remove-AzTrafficManagerEndpointConfig** cmdlet removes an endpoint from a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="a9c61-107">Você pode obter um perfil usando o cmdlet Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="a9c61-107">You can get a profile by using the Get-AzTrafficManagerProfile cmdlet.</span></span>

<span data-ttu-id="a9c61-108">Este cmdlet opera no objeto de perfil local.</span><span class="sxs-lookup"><span data-stu-id="a9c61-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="a9c61-109">Confirme as alterações no perfil do Gerenciador de tráfego usando o cmdlet Set-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="a9c61-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="a9c61-110">Para remover um ponto de extremidade e confirmar as alterações em uma única operação, use o cmdlet Remove-AzTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="a9c61-110">To remove an endpoint and commit changes in a single operation, use the Remove-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="a9c61-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a9c61-111">EXAMPLES</span></span>

### <span data-ttu-id="a9c61-112">Exemplo 1: remover um ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="a9c61-112">Example 1: Remove an endpoint</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Remove-AzTrafficManagerEndpointConfig -EndpointName "contoso" -TrafficManagerProfile $TrafficManagerProfile 
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="a9c61-113">O primeiro comando obtém um perfil do Gerenciador de tráfego do Azure usando o cmdlet **Get-AzTrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="a9c61-113">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="a9c61-114">O comando armazena o perfil local na variável $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="a9c61-114">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="a9c61-115">O segundo comando Remove um ponto de extremidade do Azure chamado contoso do perfil armazenado em $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="a9c61-115">The second command removes an Azure endpoint named contoso from the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="a9c61-116">Esse comando altera somente o objeto local.</span><span class="sxs-lookup"><span data-stu-id="a9c61-116">This command changes only the local object.</span></span>

<span data-ttu-id="a9c61-117">O comando final atualiza o perfil do Gerenciador de tráfego chamado ContosoProfile para corresponder ao valor local em $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="a9c61-117">The final command updates the Traffic Manager profile named ContosoProfile to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="a9c61-118">OS</span><span class="sxs-lookup"><span data-stu-id="a9c61-118">PARAMETERS</span></span>

### <span data-ttu-id="a9c61-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9c61-119">-DefaultProfile</span></span>
<span data-ttu-id="a9c61-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a9c61-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a9c61-121">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="a9c61-121">-EndpointName</span></span>
<span data-ttu-id="a9c61-122">Especifica o nome do ponto de extremidade do Gerenciador de tráfego que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="a9c61-122">Specifies the name of the Traffic Manager endpoint that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9c61-123">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a9c61-123">-TrafficManagerProfile</span></span>
<span data-ttu-id="a9c61-124">Especifica um objeto **TrafficManagerProfile** local.</span><span class="sxs-lookup"><span data-stu-id="a9c61-124">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="a9c61-125">Esse cmdlet modifica esse objeto local.</span><span class="sxs-lookup"><span data-stu-id="a9c61-125">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="a9c61-126">Para obter um objeto **TrafficManagerProfile** , use o cmdlet Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="a9c61-126">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a9c61-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9c61-127">CommonParameters</span></span>
<span data-ttu-id="a9c61-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9c61-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9c61-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9c61-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9c61-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a9c61-130">INPUTS</span></span>

### <span data-ttu-id="a9c61-131">Microsoft. Azure. Commands. Trafficmanager. Models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a9c61-131">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="a9c61-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a9c61-132">OUTPUTS</span></span>

### <span data-ttu-id="a9c61-133">Microsoft. Azure. Commands. Trafficmanager. Models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a9c61-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="a9c61-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a9c61-134">NOTES</span></span>

## <span data-ttu-id="a9c61-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a9c61-135">RELATED LINKS</span></span>

[<span data-ttu-id="a9c61-136">Add-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="a9c61-136">Add-AzTrafficManagerEndpointConfig</span></span>](./Add-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="a9c61-137">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a9c61-137">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="a9c61-138">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a9c61-138">Remove-AzTrafficManagerEndpoint</span></span>](./Remove-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="a9c61-139">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a9c61-139">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


