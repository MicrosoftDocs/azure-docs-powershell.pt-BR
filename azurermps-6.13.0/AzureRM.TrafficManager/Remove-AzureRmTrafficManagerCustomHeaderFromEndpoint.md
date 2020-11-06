---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D342
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/remove-azurermtrafficmanagercustomheaderfromendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint.md
ms.openlocfilehash: 452e252b7bf9368ea89e81f2d37fd5a80ab079b8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427105"
---
# <span data-ttu-id="5fe3c-101">Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint</span><span class="sxs-lookup"><span data-stu-id="5fe3c-101">Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint</span></span>

## <span data-ttu-id="5fe3c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5fe3c-102">SYNOPSIS</span></span>
<span data-ttu-id="5fe3c-103">Remove informações de cabeçalho personalizadas de um objeto de ponto de extremidade do Gerenciador de tráfego local.</span><span class="sxs-lookup"><span data-stu-id="5fe3c-103">Removes custom header information from a local Traffic Manager endpoint object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5fe3c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5fe3c-104">SYNTAX</span></span>

```
Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint -Name <String>
 -TrafficManagerEndpoint <TrafficManagerEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5fe3c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5fe3c-105">DESCRIPTION</span></span>
<span data-ttu-id="5fe3c-106">O cmdlet **Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint** remove informações de cabeçalho personalizadas de um objeto de ponto de extremidade do Azure Traffic Manager local.</span><span class="sxs-lookup"><span data-stu-id="5fe3c-106">The **Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint** cmdlet removes custom header information from a local Azure Traffic Manager endpoint object.</span></span>
<span data-ttu-id="5fe3c-107">Você pode obter um ponto de extremidade usando os cmdlets New-AzureRmTrafficManagerEndpoint ou Get-AzureRmTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="5fe3c-107">You can get an endpoint by using the New-AzureRmTrafficManagerEndpoint or Get-AzureRmTrafficManagerEndpoint cmdlets.</span></span>

<span data-ttu-id="5fe3c-108">Este cmdlet opera no objeto ponto de extremidade local.</span><span class="sxs-lookup"><span data-stu-id="5fe3c-108">This cmdlet operates on the local endpoint object.</span></span>
<span data-ttu-id="5fe3c-109">Confirme as alterações no ponto de extremidade do Gerenciador de tráfego usando o cmdlet Set-AzureRmTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="5fe3c-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="5fe3c-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5fe3c-110">EXAMPLES</span></span>

### <span data-ttu-id="5fe3c-111">Exemplo 1: remover informações de sub-rede personalizadas de um ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="5fe3c-111">Example 1: Remove custom subnet information from an endpoint</span></span>
```
PS C:\> $TrafficManagerEndpoint = Get-AzureRmTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
PS C:\> Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint -Name "host"
PS C:\> Set-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="5fe3c-112">O primeiro comando obtém o ponto de extremidade do Azure chamado contoso do perfil chamado ContosoProfile no grupo de recursos chamado ResourceGroup11 e, em seguida, armazena esse objeto na variável $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="5fe3c-112">The first command gets the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11, and then stores that object in the $TrafficManagerEndpoint variable.</span></span>
<span data-ttu-id="5fe3c-113">O segundo comando remove informações de cabeçalho personalizadas do ponto de extremidade armazenado no $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="5fe3c-113">The second command removes custom header information from the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="5fe3c-114">O comando final atualiza o ponto de extremidade no Gerenciador de tráfego para corresponder ao valor local em $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="5fe3c-114">The final command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="5fe3c-115">OS</span><span class="sxs-lookup"><span data-stu-id="5fe3c-115">PARAMETERS</span></span>

### <span data-ttu-id="5fe3c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fe3c-116">-DefaultProfile</span></span>
<span data-ttu-id="5fe3c-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5fe3c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5fe3c-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="5fe3c-118">-Name</span></span>
<span data-ttu-id="5fe3c-119">Especifica o nome das informações de cabeçalho personalizado a serem removidas.</span><span class="sxs-lookup"><span data-stu-id="5fe3c-119">Specifies the name of the custom header information to be removed.</span></span>

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

### <span data-ttu-id="5fe3c-120">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="5fe3c-120">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="5fe3c-121">Especifica um objeto **TrafficManagerEndpoint** local.</span><span class="sxs-lookup"><span data-stu-id="5fe3c-121">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="5fe3c-122">Esse cmdlet modifica esse objeto local.</span><span class="sxs-lookup"><span data-stu-id="5fe3c-122">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="5fe3c-123">Para obter um objeto **TrafficManagerEndpoint** , use o cmdlet Get-AzureRmTrafficManagerEndpoint ou New-AzureRmTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="5fe3c-123">To obtain a **TrafficManagerEndpoint** object, use the Get-AzureRmTrafficManagerEndpoint or New-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5fe3c-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5fe3c-124">-Confirm</span></span>
<span data-ttu-id="5fe3c-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5fe3c-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fe3c-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5fe3c-126">-WhatIf</span></span>
<span data-ttu-id="5fe3c-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5fe3c-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5fe3c-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5fe3c-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fe3c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fe3c-129">CommonParameters</span></span>
<span data-ttu-id="5fe3c-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5fe3c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fe3c-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5fe3c-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fe3c-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5fe3c-132">INPUTS</span></span>

### <span data-ttu-id="5fe3c-133">Microsoft. Azure. Commands. Network. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="5fe3c-133">Microsoft.Azure.Commands.Network.TrafficManagerEndpoint</span></span>
<span data-ttu-id="5fe3c-134">Este cmdlet aceita um objeto **TrafficManagerEndpoint** para este cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5fe3c-134">This cmdlet accepts a **TrafficManagerEndpoint** object to this cmdlet.</span></span>

## <span data-ttu-id="5fe3c-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5fe3c-135">OUTPUTS</span></span>

### <span data-ttu-id="5fe3c-136">Microsoft. Azure. Commands. Network. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="5fe3c-136">Microsoft.Azure.Commands.Network.TrafficManagerEndpoint</span></span>
<span data-ttu-id="5fe3c-137">Esse cmdlet retorna um objeto TrafficManagerEndpoint modificado.</span><span class="sxs-lookup"><span data-stu-id="5fe3c-137">This cmdlet returns a modified TrafficManagerEndpoint object.</span></span>

## <span data-ttu-id="5fe3c-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5fe3c-138">NOTES</span></span>

## <span data-ttu-id="5fe3c-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5fe3c-139">RELATED LINKS</span></span>

[<span data-ttu-id="5fe3c-140">Add-AzureRmTrafficManagerCustomHeaderToEndpoint</span><span class="sxs-lookup"><span data-stu-id="5fe3c-140">Add-AzureRmTrafficManagerCustomHeaderToEndpoint</span></span>](./Add-AzureRmTrafficManagerCustomHeaderToEndpoint.md)

[<span data-ttu-id="5fe3c-141">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="5fe3c-141">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="5fe3c-142">New-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="5fe3c-142">New-AzureRmTrafficManagerEndpoint</span></span>](./New-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="5fe3c-143">Set-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="5fe3c-143">Set-AzureRmTrafficManagerEndpoint</span></span>](./Set-AzureRmTrafficManagerEndpoint.md)
