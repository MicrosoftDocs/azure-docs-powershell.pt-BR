---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2049CB74-E3CB-4294-B97C-B41E91209A1E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerProbeConfig.md
ms.openlocfilehash: 0e5216f88cc860244cf11a693a73e30ba6e83390
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432082"
---
# <span data-ttu-id="b0e3f-101">New-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="b0e3f-101">New-AzureRmLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="b0e3f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b0e3f-102">SYNOPSIS</span></span>
<span data-ttu-id="b0e3f-103">Cria uma configuração de sondagem para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="b0e3f-103">Creates a probe configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b0e3f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b0e3f-104">SYNTAX</span></span>

```
New-AzureRmLoadBalancerProbeConfig -Name <String> [-RequestPath <String>] [-Protocol <String>] -Port <Int32>
 -IntervalInSeconds <Int32> -ProbeCount <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b0e3f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b0e3f-105">DESCRIPTION</span></span>
<span data-ttu-id="b0e3f-106">O cmdlet **New-AzureRmLoadBalancerProbeConfig** cria uma configuração de teste para um balanceador de carga do Azure.</span><span class="sxs-lookup"><span data-stu-id="b0e3f-106">The **New-AzureRmLoadBalancerProbeConfig** cmdlet creates a probe configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="b0e3f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b0e3f-107">EXAMPLES</span></span>

### <span data-ttu-id="b0e3f-108">Exemplo 1: criar uma configuração de sondagem</span><span class="sxs-lookup"><span data-stu-id="b0e3f-108">Example 1: Create a probe configuration</span></span>
```
PS C:\>New-AzureRmLoadBalancerProbeConfig -Name "MyProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 15
```

<span data-ttu-id="b0e3f-109">Esse comando cria uma configuração de sondagem chamada myprobe usando o protocolo HTTP.</span><span class="sxs-lookup"><span data-stu-id="b0e3f-109">This command creates a probe configuration named MyProbe using the HTTP protocol.</span></span>
<span data-ttu-id="b0e3f-110">O novo teste será conectado a um serviço de balanceamento de carga na porta 80.</span><span class="sxs-lookup"><span data-stu-id="b0e3f-110">The new probe will connect to a load-balanced service on port 80.</span></span>

## <span data-ttu-id="b0e3f-111">OS</span><span class="sxs-lookup"><span data-stu-id="b0e3f-111">PARAMETERS</span></span>

### <span data-ttu-id="b0e3f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0e3f-112">-DefaultProfile</span></span>
<span data-ttu-id="b0e3f-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b0e3f-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b0e3f-114">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="b0e3f-114">-IntervalInSeconds</span></span>
<span data-ttu-id="b0e3f-115">Especifica o intervalo, em segundos, entre testes para cada instância de um serviço de balanceamento de carga.</span><span class="sxs-lookup"><span data-stu-id="b0e3f-115">Specifies the interval, in seconds, between probes to each instance of a load-balanced service.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0e3f-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="b0e3f-116">-Name</span></span>
<span data-ttu-id="b0e3f-117">Especifica o nome da configuração de sonda a ser criada.</span><span class="sxs-lookup"><span data-stu-id="b0e3f-117">Specifies the name of the probe configuration to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0e3f-118">-Porta</span><span class="sxs-lookup"><span data-stu-id="b0e3f-118">-Port</span></span>
<span data-ttu-id="b0e3f-119">Especifica a porta na qual o novo teste deve se conectar a um serviço de balanceamento de carga.</span><span class="sxs-lookup"><span data-stu-id="b0e3f-119">Specifies the port on which the new probe should connect to a load-balanced service.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0e3f-120">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="b0e3f-120">-ProbeCount</span></span>
<span data-ttu-id="b0e3f-121">Especifica o número de falhas consecutivas por instância para que uma instância seja considerada não íntegra.</span><span class="sxs-lookup"><span data-stu-id="b0e3f-121">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0e3f-122">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="b0e3f-122">-Protocol</span></span>
<span data-ttu-id="b0e3f-123">Especifica o protocolo a ser usado para a configuração de sondagem.</span><span class="sxs-lookup"><span data-stu-id="b0e3f-123">Specifies the protocol to use for the probe configuration.</span></span>
<span data-ttu-id="b0e3f-124">Os valores aceitáveis para esse parâmetro são: TCP ou http.</span><span class="sxs-lookup"><span data-stu-id="b0e3f-124">The acceptable values for this parameter are: Tcp or Http.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Http

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0e3f-125">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="b0e3f-125">-RequestPath</span></span>
<span data-ttu-id="b0e3f-126">Especifica o caminho em um serviço de balanceamento de carga a ser sondado para determinar a integridade.</span><span class="sxs-lookup"><span data-stu-id="b0e3f-126">Specifies the path in a load-balanced service to probe to determine health.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0e3f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0e3f-127">CommonParameters</span></span>
<span data-ttu-id="b0e3f-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0e3f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0e3f-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0e3f-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0e3f-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b0e3f-130">INPUTS</span></span>

### <span data-ttu-id="b0e3f-131">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="b0e3f-131">None</span></span>
<span data-ttu-id="b0e3f-132">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="b0e3f-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b0e3f-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b0e3f-133">OUTPUTS</span></span>

### <span data-ttu-id="b0e3f-134">Microsoft. Azure. Commands. Network. Models. PSProbe</span><span class="sxs-lookup"><span data-stu-id="b0e3f-134">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="b0e3f-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b0e3f-135">NOTES</span></span>

## <span data-ttu-id="b0e3f-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b0e3f-136">RELATED LINKS</span></span>

[<span data-ttu-id="b0e3f-137">Add-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="b0e3f-137">Add-AzureRmLoadBalancerProbeConfig</span></span>](./Add-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="b0e3f-138">Get-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="b0e3f-138">Get-AzureRmLoadBalancerProbeConfig</span></span>](./Get-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="b0e3f-139">Remove-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="b0e3f-139">Remove-AzureRmLoadBalancerProbeConfig</span></span>](./Remove-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="b0e3f-140">Set-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="b0e3f-140">Set-AzureRmLoadBalancerProbeConfig</span></span>](./Set-AzureRmLoadBalancerProbeConfig.md)

