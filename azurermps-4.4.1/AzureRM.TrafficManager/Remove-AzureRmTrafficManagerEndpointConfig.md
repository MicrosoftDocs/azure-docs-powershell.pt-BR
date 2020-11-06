---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 8E12A392-A100-4814-9003-B2999150DCE1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerEndpointConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerEndpointConfig.md
ms.openlocfilehash: 4f936569b5a3c7b3ba63a471aedd6828ef6f36d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602050"
---
# <span data-ttu-id="81af2-101">Remove-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="81af2-101">Remove-AzureRmTrafficManagerEndpointConfig</span></span>

## <span data-ttu-id="81af2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="81af2-102">SYNOPSIS</span></span>
<span data-ttu-id="81af2-103">Remove um ponto de extremidade de um objeto de perfil do Gerenciador de tráfego local.</span><span class="sxs-lookup"><span data-stu-id="81af2-103">Removes an endpoint from a local Traffic Manager profile object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="81af2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="81af2-104">SYNTAX</span></span>

```
Remove-AzureRmTrafficManagerEndpointConfig -EndpointName <String>
 -TrafficManagerProfile <TrafficManagerProfile> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="81af2-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="81af2-105">DESCRIPTION</span></span>
<span data-ttu-id="81af2-106">O cmdlet **Remove-AzureRmTrafficManagerEndpointConfig** remove um ponto de extremidade de um objeto de perfil do Gerenciador de tráfego do Azure local.</span><span class="sxs-lookup"><span data-stu-id="81af2-106">The **Remove-AzureRmTrafficManagerEndpointConfig** cmdlet removes an endpoint from a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="81af2-107">Você pode obter um perfil usando o cmdlet Get-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="81af2-107">You can get a profile by using the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

<span data-ttu-id="81af2-108">Este cmdlet opera no objeto de perfil local.</span><span class="sxs-lookup"><span data-stu-id="81af2-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="81af2-109">Confirme as alterações no perfil do Gerenciador de tráfego usando o cmdlet Set-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="81af2-109">Commit your changes to the profile for Traffic Manager by using the Set-AzureRmTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="81af2-110">Para remover um ponto de extremidade e confirmar as alterações em uma única operação, use o cmdlet Remove-AzureRmTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="81af2-110">To remove an endpoint and commit changes in a single operation, use the Remove-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="81af2-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="81af2-111">EXAMPLES</span></span>

### <span data-ttu-id="81af2-112">Exemplo 1: remover um ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="81af2-112">Example 1: Remove an endpoint</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Remove-AzureRmTrafficManagerEndpointConfig -EndpointName "contoso" -Type AzureEndpoints -TrafficManagerProfile $TrafficManagerProfile 
PS C:\> Set-AzureRmTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="81af2-113">O primeiro comando obtém um perfil do Gerenciador de tráfego do Azure usando o cmdlet **Get-AzureRmTrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="81af2-113">The first command gets an Azure Traffic Manager profile by using the **Get-AzureRmTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="81af2-114">O comando armazena o perfil local na variável $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="81af2-114">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="81af2-115">O segundo comando Remove um ponto de extremidade do Azure chamado contoso do perfil armazenado em $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="81af2-115">The second command removes an Azure endpoint named contoso from the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="81af2-116">Esse comando altera somente o objeto local.</span><span class="sxs-lookup"><span data-stu-id="81af2-116">This command changes only the local object.</span></span>

<span data-ttu-id="81af2-117">O comando final atualiza o perfil do Gerenciador de tráfego chamado ContosoProfile para corresponder ao valor local em $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="81af2-117">The final command updates the Traffic Manager profile named ContosoProfile to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="81af2-118">OS</span><span class="sxs-lookup"><span data-stu-id="81af2-118">PARAMETERS</span></span>

### <span data-ttu-id="81af2-119">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="81af2-119">-EndpointName</span></span>
<span data-ttu-id="81af2-120">Especifica o nome do ponto de extremidade do Gerenciador de tráfego que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="81af2-120">Specifies the name of the Traffic Manager endpoint that this cmdlet removes.</span></span>

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

### <span data-ttu-id="81af2-121">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="81af2-121">-TrafficManagerProfile</span></span>
<span data-ttu-id="81af2-122">Especifica um objeto **TrafficManagerProfile** local.</span><span class="sxs-lookup"><span data-stu-id="81af2-122">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="81af2-123">Esse cmdlet modifica esse objeto local.</span><span class="sxs-lookup"><span data-stu-id="81af2-123">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="81af2-124">Para obter um objeto **TrafficManagerProfile** , use o cmdlet Get-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="81af2-124">To obtain a **TrafficManagerProfile** object, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="81af2-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81af2-125">-DefaultProfile</span></span>
<span data-ttu-id="81af2-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="81af2-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81af2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81af2-127">CommonParameters</span></span>
<span data-ttu-id="81af2-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81af2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81af2-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81af2-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81af2-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="81af2-130">INPUTS</span></span>

### <span data-ttu-id="81af2-131">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="81af2-131">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="81af2-132">Este cmdlet aceita um objeto **TrafficManagerProfile** para este cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81af2-132">This cmdlet accepts a **TrafficManagerProfile** object to this cmdlet.</span></span>

## <span data-ttu-id="81af2-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="81af2-133">OUTPUTS</span></span>

### <span data-ttu-id="81af2-134">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="81af2-134">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="81af2-135">Esse cmdlet retorna um objeto TrafficManagerProfile modificado.</span><span class="sxs-lookup"><span data-stu-id="81af2-135">This cmdlet returns a modified TrafficManagerProfile object.</span></span>

## <span data-ttu-id="81af2-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="81af2-136">NOTES</span></span>

## <span data-ttu-id="81af2-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="81af2-137">RELATED LINKS</span></span>

[<span data-ttu-id="81af2-138">Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="81af2-138">Add-AzureRmTrafficManagerEndpointConfig</span></span>](./Add-AzureRmTrafficManagerEndpointConfig.md)

[<span data-ttu-id="81af2-139">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="81af2-139">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="81af2-140">Remove-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="81af2-140">Remove-AzureRmTrafficManagerEndpoint</span></span>](./Remove-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="81af2-141">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="81af2-141">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


