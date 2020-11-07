---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33E
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/add-aztrafficmanagercustomheadertoendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerCustomHeaderToEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerCustomHeaderToEndpoint.md
ms.openlocfilehash: 7e3661a827bb6864fbd43abde43c7ab2bb440ecb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773146"
---
# <span data-ttu-id="8c5c3-101">Add-AzTrafficManagerCustomHeaderToEndpoint</span><span class="sxs-lookup"><span data-stu-id="8c5c3-101">Add-AzTrafficManagerCustomHeaderToEndpoint</span></span>

## <span data-ttu-id="8c5c3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8c5c3-102">SYNOPSIS</span></span>
<span data-ttu-id="8c5c3-103">Adiciona informações de cabeçalho personalizadas a um objeto de ponto de extremidade do Gerenciador de tráfego local.</span><span class="sxs-lookup"><span data-stu-id="8c5c3-103">Adds custom header information to a local Traffic Manager endpoint object.</span></span>

## <span data-ttu-id="8c5c3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8c5c3-104">SYNTAX</span></span>

```
Add-AzTrafficManagerCustomHeaderToEndpoint -Name <String> -Value <String>
 -TrafficManagerEndpoint <TrafficManagerEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c5c3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8c5c3-105">DESCRIPTION</span></span>
<span data-ttu-id="8c5c3-106">O cmdlet **Add-AzTrafficManagerCustomHeaderToEndpoint** adiciona informações de cabeçalho personalizadas a um objeto de ponto de extremidade do Azure Traffic Manager local.</span><span class="sxs-lookup"><span data-stu-id="8c5c3-106">The **Add-AzTrafficManagerCustomHeaderToEndpoint** cmdlet adds custom header information to a local Azure Traffic Manager endpoint object.</span></span>
<span data-ttu-id="8c5c3-107">Você pode obter um ponto de extremidade usando os cmdlets New-AzTrafficManagerEndpoint ou Get-AzTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="8c5c3-107">You can get an endpoint by using the New-AzTrafficManagerEndpoint or Get-AzTrafficManagerEndpoint cmdlets.</span></span>

<span data-ttu-id="8c5c3-108">Este cmdlet opera no objeto ponto de extremidade local.</span><span class="sxs-lookup"><span data-stu-id="8c5c3-108">This cmdlet operates on the local endpoint object.</span></span>
<span data-ttu-id="8c5c3-109">Confirme as alterações no ponto de extremidade do Gerenciador de tráfego usando o cmdlet Set-AzTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="8c5c3-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="8c5c3-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8c5c3-110">EXAMPLES</span></span>

### <span data-ttu-id="8c5c3-111">Exemplo 1: adicionar informações de cabeçalho personalizado a um ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="8c5c3-111">Example 1: Add custom header information to an endpoint</span></span>
```
PS C:\> $TrafficManagerEndpoint = New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
PS C:\> Add-AzTrafficManagerCustomHeaderToEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint -Name "host" -Value "www.contoso.com"
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="8c5c3-112">O primeiro comando cria um ponto de extremidade do Gerenciador de tráfego do Azure usando o cmdlet **New-AzTrafficManagerEndpoint** .</span><span class="sxs-lookup"><span data-stu-id="8c5c3-112">The first command creates an Azure Traffic Manager endpoint by using the **New-AzTrafficManagerEndpoint** cmdlet.</span></span>
<span data-ttu-id="8c5c3-113">O comando armazena o ponto de extremidade local na variável $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="8c5c3-113">The command stores the local endpoint in the $TrafficManagerEndpoint variable.</span></span>
<span data-ttu-id="8c5c3-114">O segundo comando adiciona informações de cabeçalho personalizado ao ponto de extremidade armazenado em $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="8c5c3-114">The second command adds custom header information to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="8c5c3-115">O comando final atualiza o ponto de extremidade no Gerenciador de tráfego para corresponder ao valor local em $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="8c5c3-115">The final command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="8c5c3-116">OS</span><span class="sxs-lookup"><span data-stu-id="8c5c3-116">PARAMETERS</span></span>

### <span data-ttu-id="8c5c3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c5c3-117">-DefaultProfile</span></span>
<span data-ttu-id="8c5c3-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8c5c3-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c5c3-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="8c5c3-119">-Name</span></span>
<span data-ttu-id="8c5c3-120">Especifica o nome das informações de cabeçalho personalizado a serem adicionadas.</span><span class="sxs-lookup"><span data-stu-id="8c5c3-120">Specifies the name of the custom header information to be added.</span></span>

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

### <span data-ttu-id="8c5c3-121">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="8c5c3-121">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="8c5c3-122">Especifica um objeto **TrafficManagerEndpoint** local.</span><span class="sxs-lookup"><span data-stu-id="8c5c3-122">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="8c5c3-123">Esse cmdlet modifica esse objeto local.</span><span class="sxs-lookup"><span data-stu-id="8c5c3-123">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="8c5c3-124">Para obter um objeto **TrafficManagerEndpoint** , use o cmdlet Get-AzTrafficManagerEndpoint ou New-AzTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="8c5c3-124">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint or New-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="8c5c3-125">-Valor</span><span class="sxs-lookup"><span data-stu-id="8c5c3-125">-Value</span></span>
<span data-ttu-id="8c5c3-126">Especifica o valor das informações de cabeçalho personalizado a serem adicionadas.</span><span class="sxs-lookup"><span data-stu-id="8c5c3-126">Specifies the value of the custom header information to be added.</span></span>

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

### <span data-ttu-id="8c5c3-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8c5c3-127">-Confirm</span></span>
<span data-ttu-id="8c5c3-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8c5c3-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c5c3-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c5c3-129">-WhatIf</span></span>
<span data-ttu-id="8c5c3-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8c5c3-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8c5c3-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8c5c3-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c5c3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c5c3-132">CommonParameters</span></span>
<span data-ttu-id="8c5c3-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c5c3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c5c3-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c5c3-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c5c3-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8c5c3-135">INPUTS</span></span>

### <span data-ttu-id="8c5c3-136">Microsoft. Azure. Commands. Trafficmanager. Models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="8c5c3-136">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="8c5c3-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8c5c3-137">OUTPUTS</span></span>

### <span data-ttu-id="8c5c3-138">Microsoft. Azure. Commands. Trafficmanager. Models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="8c5c3-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="8c5c3-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8c5c3-139">NOTES</span></span>

## <span data-ttu-id="8c5c3-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8c5c3-140">RELATED LINKS</span></span>

[<span data-ttu-id="8c5c3-141">Remove-AzTrafficManagerCustomHeaderFromEndpoint</span><span class="sxs-lookup"><span data-stu-id="8c5c3-141">Remove-AzTrafficManagerCustomHeaderFromEndpoint</span></span>](./Remove-AzTrafficManagerCustomHeaderFromEndpoint.md)

[<span data-ttu-id="8c5c3-142">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="8c5c3-142">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="8c5c3-143">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="8c5c3-143">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="8c5c3-144">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="8c5c3-144">Set-AzTrafficManagerEndpoint</span></span>](./Set-AzTrafficManagerEndpoint.md)