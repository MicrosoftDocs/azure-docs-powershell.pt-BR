---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D342
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagercustomheaderfromendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerCustomHeaderFromEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerCustomHeaderFromEndpoint.md
ms.openlocfilehash: 35ab92add873e603101400f77e813fb115386fd4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116277"
---
# <span data-ttu-id="0123f-101">Remove-AzTrafficManagerCustomHeaderFromEndpoint</span><span class="sxs-lookup"><span data-stu-id="0123f-101">Remove-AzTrafficManagerCustomHeaderFromEndpoint</span></span>

## <span data-ttu-id="0123f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0123f-102">SYNOPSIS</span></span>
<span data-ttu-id="0123f-103">Remove informações personalizadas de um objeto de ponto de extremidade do Gerenciador de Tráfego local.</span><span class="sxs-lookup"><span data-stu-id="0123f-103">Removes custom header information from a local Traffic Manager endpoint object.</span></span>

## <span data-ttu-id="0123f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0123f-104">SYNTAX</span></span>

```
Remove-AzTrafficManagerCustomHeaderFromEndpoint -Name <String> -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0123f-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="0123f-105">DESCRIPTION</span></span>
<span data-ttu-id="0123f-106">O cmdlet **Remove-AzTrafficManagerCusagerCustomHeaderFromEndpoint** remove informações personalizadas do header de um objeto local do Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="0123f-106">The **Remove-AzTrafficManagerCustomHeaderFromEndpoint** cmdlet removes custom header information from a local Azure Traffic Manager endpoint object.</span></span>
<span data-ttu-id="0123f-107">Você pode obter um ponto de extremidade usando os cmdlets New-AzTrafficManagerEndpoint ou Get-AzTrafficManagerEndpoint de extremidade.</span><span class="sxs-lookup"><span data-stu-id="0123f-107">You can get an endpoint by using the New-AzTrafficManagerEndpoint or Get-AzTrafficManagerEndpoint cmdlets.</span></span>

<span data-ttu-id="0123f-108">Este cmdlet opera no objeto de ponto de extremidade local.</span><span class="sxs-lookup"><span data-stu-id="0123f-108">This cmdlet operates on the local endpoint object.</span></span>
<span data-ttu-id="0123f-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzTrafficManagerEndpoint cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0123f-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="0123f-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0123f-110">EXAMPLES</span></span>

### <span data-ttu-id="0123f-111">Exemplo 1: Remover informações personalizadas da sub-rede de um ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="0123f-111">Example 1: Remove custom subnet information from an endpoint</span></span>
```
PS C:\> $TrafficManagerEndpoint = Get-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
PS C:\> Remove-AzTrafficManagerCustomHeaderFromEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint -Name "host"
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="0123f-112">O primeiro comando obtém o ponto de extremidade do Azure chamado contoso do perfil contosoProfile no grupo de recursos chamado ResourceGroup11 e armazena esse objeto na variável $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="0123f-112">The first command gets the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11, and then stores that object in the $TrafficManagerEndpoint variable.</span></span>
<span data-ttu-id="0123f-113">O segundo comando remove informações personalizadas do header do ponto de extremidade armazenados $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="0123f-113">The second command removes custom header information from the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="0123f-114">O comando final atualiza o ponto de extremidade no Gerenciador de Tráfego para corresponder ao valor local no $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="0123f-114">The final command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="0123f-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0123f-115">PARAMETERS</span></span>

### <span data-ttu-id="0123f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0123f-116">-DefaultProfile</span></span>
<span data-ttu-id="0123f-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="0123f-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0123f-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="0123f-118">-Name</span></span>
<span data-ttu-id="0123f-119">Especifica o nome das informações de cabeça personalizadas a serem removidas.</span><span class="sxs-lookup"><span data-stu-id="0123f-119">Specifies the name of the custom header information to be removed.</span></span>

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

### <span data-ttu-id="0123f-120">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="0123f-120">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="0123f-121">Especifica um objeto **Local TrafficManagerEndpoint.**</span><span class="sxs-lookup"><span data-stu-id="0123f-121">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="0123f-122">Este cmdlet modifica este objeto local.</span><span class="sxs-lookup"><span data-stu-id="0123f-122">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="0123f-123">Para obter um **objeto TrafficManagerEndpoint,** use o Get-AzTrafficManagerEndpoint ou New-AzTrafficManagerEndpoint cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0123f-123">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint or New-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="0123f-124">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="0123f-124">-Confirm</span></span>
<span data-ttu-id="0123f-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0123f-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0123f-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0123f-126">-WhatIf</span></span>
<span data-ttu-id="0123f-127">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="0123f-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0123f-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0123f-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0123f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0123f-129">CommonParameters</span></span>
<span data-ttu-id="0123f-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0123f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0123f-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0123f-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0123f-132">Entradas</span><span class="sxs-lookup"><span data-stu-id="0123f-132">INPUTS</span></span>

### <span data-ttu-id="0123f-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="0123f-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="0123f-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="0123f-134">OUTPUTS</span></span>

### <span data-ttu-id="0123f-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="0123f-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="0123f-136">Notas</span><span class="sxs-lookup"><span data-stu-id="0123f-136">NOTES</span></span>

## <span data-ttu-id="0123f-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0123f-137">RELATED LINKS</span></span>

[<span data-ttu-id="0123f-138">Add-AzTrafficManagerCusagerHeaderToEndpoint</span><span class="sxs-lookup"><span data-stu-id="0123f-138">Add-AzTrafficManagerCustomHeaderToEndpoint</span></span>](./Add-AzTrafficManagerCustomHeaderToEndpoint.md)

[<span data-ttu-id="0123f-139">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0123f-139">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="0123f-140">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="0123f-140">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="0123f-141">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="0123f-141">Set-AzTrafficManagerEndpoint</span></span>](./Set-AzTrafficManagerEndpoint.md)
