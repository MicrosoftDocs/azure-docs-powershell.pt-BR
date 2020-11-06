---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6F9BAB0B-7DC7-4672-B2B5-8B139D652DDD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerProbeConfig.md
ms.openlocfilehash: 79e9d856825e174bc8667f99e7b25b301230dec3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432606"
---
# <span data-ttu-id="7d4b9-101">Add-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="7d4b9-101">Add-AzureRmLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="7d4b9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7d4b9-102">SYNOPSIS</span></span>
<span data-ttu-id="7d4b9-103">Adiciona uma configuração de teste a um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="7d4b9-103">Adds a probe configuration to a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d4b9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7d4b9-104">SYNTAX</span></span>

```
Add-AzureRmLoadBalancerProbeConfig -Name <String> -LoadBalancer <PSLoadBalancer> [-RequestPath <String>]
 [-Protocol <String>] -Port <Int32> -IntervalInSeconds <Int32> -ProbeCount <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7d4b9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7d4b9-105">DESCRIPTION</span></span>
<span data-ttu-id="7d4b9-106">O cmdlet **Add-AzureRmLoadBalancerProbeConfig** adiciona uma configuração de teste a um balanceador de carga do Azure.</span><span class="sxs-lookup"><span data-stu-id="7d4b9-106">The **Add-AzureRmLoadBalancerProbeConfig** cmdlet adds a probe configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="7d4b9-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7d4b9-107">EXAMPLES</span></span>

### <span data-ttu-id="7d4b9-108">Exemplo 1 adicionar uma configuração de teste a um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="7d4b9-108">Example 1 Add a probe configuration to a load balancer</span></span>
```
PS C:\>Get-AzureRmLoadBalancer -Name "myLb" -ResourceGroupName "myRg" | Add-AzureRmLoadBalancerProbeConfig -Name "probeName" -RequestPath healthcheck2.aspx -Protocol http -Port 81 -IntervalInSeconds 16 -ProbeCount 3 | Set-AzureRmLoadBalancer
```

<span data-ttu-id="7d4b9-109">Esse comando obtém o balanceador de carga chamado myLb, adiciona a configuração de teste especificada a ele e, em seguida, usa o cmdlet **set-AzureRmLoadBalancer** para atualizar o balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="7d4b9-109">This command gets the load balancer named myLb, adds the specified probe configuration to it, and then uses the **Set-AzureRmLoadBalancer** cmdlet to update the load balancer.</span></span>

## <span data-ttu-id="7d4b9-110">OS</span><span class="sxs-lookup"><span data-stu-id="7d4b9-110">PARAMETERS</span></span>

### <span data-ttu-id="7d4b9-111">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="7d4b9-111">-IntervalInSeconds</span></span>
<span data-ttu-id="7d4b9-112">Especifica o intervalo, em segundos, entre testes para cada instância do serviço de balanceamento de carga.</span><span class="sxs-lookup"><span data-stu-id="7d4b9-112">Specifies the interval, in seconds, between probes to each instance of the load-balanced service.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d4b9-113">-Loadbalancer</span><span class="sxs-lookup"><span data-stu-id="7d4b9-113">-LoadBalancer</span></span>
<span data-ttu-id="7d4b9-114">Especifica um objeto **Loadbalancer** .</span><span class="sxs-lookup"><span data-stu-id="7d4b9-114">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="7d4b9-115">Esse cmdlet adiciona uma configuração de teste ao balanceador de carga que o parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="7d4b9-115">This cmdlet adds a probe configuration to the load balancer that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7d4b9-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="7d4b9-116">-Name</span></span>
<span data-ttu-id="7d4b9-117">Especifica o nome da configuração de sonda a ser adicionada.</span><span class="sxs-lookup"><span data-stu-id="7d4b9-117">Specifies the name of the probe configuration to add.</span></span>

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

### <span data-ttu-id="7d4b9-118">-Porta</span><span class="sxs-lookup"><span data-stu-id="7d4b9-118">-Port</span></span>
<span data-ttu-id="7d4b9-119">Especifica a porta na qual os testes devem se conectar a um serviço de balanceamento de carga.</span><span class="sxs-lookup"><span data-stu-id="7d4b9-119">Specifies the port on which probes should connect to a load-balanced service.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d4b9-120">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="7d4b9-120">-ProbeCount</span></span>
<span data-ttu-id="7d4b9-121">Especifica o número de falhas consecutivas por instância para que uma instância seja considerada não íntegra.</span><span class="sxs-lookup"><span data-stu-id="7d4b9-121">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d4b9-122">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="7d4b9-122">-Protocol</span></span>
<span data-ttu-id="7d4b9-123">Especifica o protocolo a ser usado para o teste.</span><span class="sxs-lookup"><span data-stu-id="7d4b9-123">Specifies the protocol to use for the probe.</span></span>
<span data-ttu-id="7d4b9-124">Os valores aceitáveis para esse parâmetro são: TCP ou http.</span><span class="sxs-lookup"><span data-stu-id="7d4b9-124">The acceptable values for this parameter are: Tcp or Http.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Http

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d4b9-125">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="7d4b9-125">-RequestPath</span></span>
<span data-ttu-id="7d4b9-126">Especifica o caminho no serviço de balanceamento de carga a ser sondado para determinar a integridade.</span><span class="sxs-lookup"><span data-stu-id="7d4b9-126">Specifies the path in the load-balanced service to probe to determine health.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d4b9-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d4b9-127">-DefaultProfile</span></span>
<span data-ttu-id="7d4b9-128">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7d4b9-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d4b9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d4b9-129">CommonParameters</span></span>
<span data-ttu-id="7d4b9-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d4b9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d4b9-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d4b9-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d4b9-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7d4b9-132">INPUTS</span></span>

### <span data-ttu-id="7d4b9-133">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7d4b9-133">PSLoadBalancer</span></span>
<span data-ttu-id="7d4b9-134">O parâmetro ' loadbalancer ' aceita o valor do tipo ' PSLoadBalancer ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="7d4b9-134">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="7d4b9-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7d4b9-135">OUTPUTS</span></span>

### <span data-ttu-id="7d4b9-136">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7d4b9-136">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="7d4b9-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7d4b9-137">NOTES</span></span>

## <span data-ttu-id="7d4b9-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7d4b9-138">RELATED LINKS</span></span>

[<span data-ttu-id="7d4b9-139">Get-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="7d4b9-139">Get-AzureRmLoadBalancerProbeConfig</span></span>](./Get-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="7d4b9-140">New-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="7d4b9-140">New-AzureRmLoadBalancerProbeConfig</span></span>](./New-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="7d4b9-141">Remove-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="7d4b9-141">Remove-AzureRmLoadBalancerProbeConfig</span></span>](./Remove-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="7d4b9-142">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7d4b9-142">Set-AzureRmLoadBalancer</span></span>](./Set-AzureRmLoadBalancer.md)

[<span data-ttu-id="7d4b9-143">Set-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="7d4b9-143">Set-AzureRmLoadBalancerProbeConfig</span></span>](./Set-AzureRmLoadBalancerProbeConfig.md)


