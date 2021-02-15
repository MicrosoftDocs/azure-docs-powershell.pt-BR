---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 8E12A392-A100-4814-9003-B2999150DCE1
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagerendpointconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpointConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpointConfig.md
ms.openlocfilehash: 4795e89013acaadcc08477370441ff5acdded85a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114350"
---
# <span data-ttu-id="3eefe-101">Remove-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="3eefe-101">Remove-AzTrafficManagerEndpointConfig</span></span>

## <span data-ttu-id="3eefe-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3eefe-102">SYNOPSIS</span></span>
<span data-ttu-id="3eefe-103">Remove um ponto de extremidade de um objeto de perfil local do Gerenciador de Tráfego.</span><span class="sxs-lookup"><span data-stu-id="3eefe-103">Removes an endpoint from a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="3eefe-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3eefe-104">SYNTAX</span></span>

```
Remove-AzTrafficManagerEndpointConfig -EndpointName <String> -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3eefe-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="3eefe-105">DESCRIPTION</span></span>
<span data-ttu-id="3eefe-106">O cmdlet **Remove-AzTrafficManagerEndpointConfig** remove um ponto de extremidade de um objeto de perfil local do Gerenciador de Tráfego do Azure.</span><span class="sxs-lookup"><span data-stu-id="3eefe-106">The **Remove-AzTrafficManagerEndpointConfig** cmdlet removes an endpoint from a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="3eefe-107">Você pode obter um perfil usando o cmdlet Get-AzTrafficManagerProfile dados.</span><span class="sxs-lookup"><span data-stu-id="3eefe-107">You can get a profile by using the Get-AzTrafficManagerProfile cmdlet.</span></span>

<span data-ttu-id="3eefe-108">Este cmdlet opera no objeto de perfil local.</span><span class="sxs-lookup"><span data-stu-id="3eefe-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="3eefe-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3eefe-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="3eefe-110">Para remover um ponto de extremidade e comprometer as alterações em uma única operação, use o cmdlet Remove-AzTrafficManagerEndpoint ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="3eefe-110">To remove an endpoint and commit changes in a single operation, use the Remove-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="3eefe-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3eefe-111">EXAMPLES</span></span>

### <span data-ttu-id="3eefe-112">Exemplo 1: Remover um ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="3eefe-112">Example 1: Remove an endpoint</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Remove-AzTrafficManagerEndpointConfig -EndpointName "contoso" -TrafficManagerProfile $TrafficManagerProfile 
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="3eefe-113">O primeiro comando obtém um perfil do Gerenciador de Tráfego do Azure usando o cmdlet **Get-AzTrafficManagerProfile.**</span><span class="sxs-lookup"><span data-stu-id="3eefe-113">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="3eefe-114">O comando armazena o perfil local na variável $TrafficManagerProfile dados.</span><span class="sxs-lookup"><span data-stu-id="3eefe-114">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="3eefe-115">O segundo comando remove um ponto de extremidade do Azure chamado contoso do perfil armazenado $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="3eefe-115">The second command removes an Azure endpoint named contoso from the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="3eefe-116">Esse comando altera apenas o objeto local.</span><span class="sxs-lookup"><span data-stu-id="3eefe-116">This command changes only the local object.</span></span>

<span data-ttu-id="3eefe-117">O comando final atualiza o perfil do Gerenciador de Tráfego chamado ContosoProfile para corresponder ao valor local no $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="3eefe-117">The final command updates the Traffic Manager profile named ContosoProfile to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="3eefe-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3eefe-118">PARAMETERS</span></span>

### <span data-ttu-id="3eefe-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3eefe-119">-DefaultProfile</span></span>
<span data-ttu-id="3eefe-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="3eefe-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3eefe-121">-Nomedo Ponto de Extremidade</span><span class="sxs-lookup"><span data-stu-id="3eefe-121">-EndpointName</span></span>
<span data-ttu-id="3eefe-122">Especifica o nome do ponto de extremidade do Gerenciador de Tráfego que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="3eefe-122">Specifies the name of the Traffic Manager endpoint that this cmdlet removes.</span></span>

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

### <span data-ttu-id="3eefe-123">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3eefe-123">-TrafficManagerProfile</span></span>
<span data-ttu-id="3eefe-124">Especifica um objeto **TrafficManagerProfile** local.</span><span class="sxs-lookup"><span data-stu-id="3eefe-124">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="3eefe-125">Este cmdlet modifica este objeto local.</span><span class="sxs-lookup"><span data-stu-id="3eefe-125">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="3eefe-126">Para obter um **objeto TrafficManagerProfile,** use o cmdlet Get-AzTrafficManagerProfile dados.</span><span class="sxs-lookup"><span data-stu-id="3eefe-126">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="3eefe-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3eefe-127">CommonParameters</span></span>
<span data-ttu-id="3eefe-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3eefe-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3eefe-129">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3eefe-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3eefe-130">Entradas</span><span class="sxs-lookup"><span data-stu-id="3eefe-130">INPUTS</span></span>

### <span data-ttu-id="3eefe-131">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3eefe-131">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="3eefe-132">Saídas</span><span class="sxs-lookup"><span data-stu-id="3eefe-132">OUTPUTS</span></span>

### <span data-ttu-id="3eefe-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3eefe-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="3eefe-134">Notas</span><span class="sxs-lookup"><span data-stu-id="3eefe-134">NOTES</span></span>

## <span data-ttu-id="3eefe-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3eefe-135">RELATED LINKS</span></span>

[<span data-ttu-id="3eefe-136">Add-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="3eefe-136">Add-AzTrafficManagerEndpointConfig</span></span>](./Add-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="3eefe-137">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3eefe-137">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="3eefe-138">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="3eefe-138">Remove-AzTrafficManagerEndpoint</span></span>](./Remove-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="3eefe-139">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3eefe-139">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


