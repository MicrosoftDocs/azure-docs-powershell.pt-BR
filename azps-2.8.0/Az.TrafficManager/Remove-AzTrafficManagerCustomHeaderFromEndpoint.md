---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D342
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagercustomheaderfromendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerCustomHeaderFromEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerCustomHeaderFromEndpoint.md
ms.openlocfilehash: f1575de761180c6ce17bcd6af1186d3e5bff60ce
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93774357"
---
# <span data-ttu-id="7a4e6-101">Remove-AzTrafficManagerCustomHeaderFromEndpoint</span><span class="sxs-lookup"><span data-stu-id="7a4e6-101">Remove-AzTrafficManagerCustomHeaderFromEndpoint</span></span>

## <span data-ttu-id="7a4e6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7a4e6-102">SYNOPSIS</span></span>
<span data-ttu-id="7a4e6-103">Remove informações de cabeçalho personalizadas de um objeto de ponto de extremidade do Gerenciador de tráfego local.</span><span class="sxs-lookup"><span data-stu-id="7a4e6-103">Removes custom header information from a local Traffic Manager endpoint object.</span></span>

## <span data-ttu-id="7a4e6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7a4e6-104">SYNTAX</span></span>

```
Remove-AzTrafficManagerCustomHeaderFromEndpoint -Name <String> -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a4e6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7a4e6-105">DESCRIPTION</span></span>
<span data-ttu-id="7a4e6-106">O cmdlet **Remove-AzTrafficManagerCustomHeaderFromEndpoint** remove informações de cabeçalho personalizadas de um objeto de ponto de extremidade do Azure Traffic Manager local.</span><span class="sxs-lookup"><span data-stu-id="7a4e6-106">The **Remove-AzTrafficManagerCustomHeaderFromEndpoint** cmdlet removes custom header information from a local Azure Traffic Manager endpoint object.</span></span>
<span data-ttu-id="7a4e6-107">Você pode obter um ponto de extremidade usando os cmdlets New-AzTrafficManagerEndpoint ou Get-AzTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="7a4e6-107">You can get an endpoint by using the New-AzTrafficManagerEndpoint or Get-AzTrafficManagerEndpoint cmdlets.</span></span>

<span data-ttu-id="7a4e6-108">Este cmdlet opera no objeto ponto de extremidade local.</span><span class="sxs-lookup"><span data-stu-id="7a4e6-108">This cmdlet operates on the local endpoint object.</span></span>
<span data-ttu-id="7a4e6-109">Confirme as alterações no ponto de extremidade do Gerenciador de tráfego usando o cmdlet Set-AzTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="7a4e6-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="7a4e6-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7a4e6-110">EXAMPLES</span></span>

### <span data-ttu-id="7a4e6-111">Exemplo 1: remover informações de sub-rede personalizadas de um ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="7a4e6-111">Example 1: Remove custom subnet information from an endpoint</span></span>
```
PS C:\> $TrafficManagerEndpoint = Get-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
PS C:\> Remove-AzTrafficManagerCustomHeaderFromEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint -Name "host"
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="7a4e6-112">O primeiro comando obtém o ponto de extremidade do Azure chamado contoso do perfil chamado ContosoProfile no grupo de recursos chamado ResourceGroup11 e, em seguida, armazena esse objeto na variável $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="7a4e6-112">The first command gets the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11, and then stores that object in the $TrafficManagerEndpoint variable.</span></span>
<span data-ttu-id="7a4e6-113">O segundo comando remove informações de cabeçalho personalizadas do ponto de extremidade armazenado no $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="7a4e6-113">The second command removes custom header information from the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="7a4e6-114">O comando final atualiza o ponto de extremidade no Gerenciador de tráfego para corresponder ao valor local em $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="7a4e6-114">The final command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="7a4e6-115">OS</span><span class="sxs-lookup"><span data-stu-id="7a4e6-115">PARAMETERS</span></span>

### <span data-ttu-id="7a4e6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a4e6-116">-DefaultProfile</span></span>
<span data-ttu-id="7a4e6-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7a4e6-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7a4e6-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="7a4e6-118">-Name</span></span>
<span data-ttu-id="7a4e6-119">Especifica o nome das informações de cabeçalho personalizado a serem removidas.</span><span class="sxs-lookup"><span data-stu-id="7a4e6-119">Specifies the name of the custom header information to be removed.</span></span>

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

### <span data-ttu-id="7a4e6-120">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="7a4e6-120">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="7a4e6-121">Especifica um objeto **TrafficManagerEndpoint** local.</span><span class="sxs-lookup"><span data-stu-id="7a4e6-121">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="7a4e6-122">Esse cmdlet modifica esse objeto local.</span><span class="sxs-lookup"><span data-stu-id="7a4e6-122">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="7a4e6-123">Para obter um objeto **TrafficManagerEndpoint** , use o cmdlet Get-AzTrafficManagerEndpoint ou New-AzTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="7a4e6-123">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint or New-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="7a4e6-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7a4e6-124">-Confirm</span></span>
<span data-ttu-id="7a4e6-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a4e6-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a4e6-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a4e6-126">-WhatIf</span></span>
<span data-ttu-id="7a4e6-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7a4e6-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7a4e6-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7a4e6-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a4e6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a4e6-129">CommonParameters</span></span>
<span data-ttu-id="7a4e6-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a4e6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a4e6-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a4e6-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a4e6-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7a4e6-132">INPUTS</span></span>

### <span data-ttu-id="7a4e6-133">Microsoft. Azure. Commands. Trafficmanager. Models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="7a4e6-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="7a4e6-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7a4e6-134">OUTPUTS</span></span>

### <span data-ttu-id="7a4e6-135">Microsoft. Azure. Commands. Trafficmanager. Models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="7a4e6-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="7a4e6-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7a4e6-136">NOTES</span></span>

## <span data-ttu-id="7a4e6-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7a4e6-137">RELATED LINKS</span></span>

[<span data-ttu-id="7a4e6-138">Add-AzTrafficManagerCustomHeaderToEndpoint</span><span class="sxs-lookup"><span data-stu-id="7a4e6-138">Add-AzTrafficManagerCustomHeaderToEndpoint</span></span>](./Add-AzTrafficManagerCustomHeaderToEndpoint.md)

[<span data-ttu-id="7a4e6-139">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7a4e6-139">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="7a4e6-140">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="7a4e6-140">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="7a4e6-141">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="7a4e6-141">Set-AzTrafficManagerEndpoint</span></span>](./Set-AzTrafficManagerEndpoint.md)
