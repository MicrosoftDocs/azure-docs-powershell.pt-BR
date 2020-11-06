---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: DE31891A-0EF7-44D7-B955-A3279D27CC21
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/new-azurermtrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/New-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/New-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: bc59e5b317588317ae9dc428db76c924847895da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610038"
---
# <span data-ttu-id="11c83-101">New-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="11c83-101">New-AzureRmTrafficManagerProfile</span></span>

## <span data-ttu-id="11c83-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="11c83-102">SYNOPSIS</span></span>
<span data-ttu-id="11c83-103">Cria um perfil do Gerenciador de tráfego.</span><span class="sxs-lookup"><span data-stu-id="11c83-103">Creates a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="11c83-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="11c83-104">SYNTAX</span></span>

```
New-AzureRmTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-ProfileStatus <String>]
 -RelativeDnsName <String> -Ttl <UInt32> -TrafficRoutingMethod <String> -MonitorProtocol <String>
 -MonitorPort <UInt32> [-MonitorPath <String>] [-MonitorIntervalInSeconds <Int32>]
 [-MonitorTimeoutInSeconds <Int32>] [-MonitorToleratedNumberOfFailures <Int32>] [-MaxReturn <Int64>]
 [-Tag <Hashtable>]
 [-CustomHeader <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]>]
 [-ExpectedStatusCodeRange <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerExpectedStatusCodeRange]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11c83-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="11c83-105">DESCRIPTION</span></span>
<span data-ttu-id="11c83-106">O cmdlet **New-AzureRmTrafficManagerProfile** cria um perfil do Gerenciador de tráfego do Azure.</span><span class="sxs-lookup"><span data-stu-id="11c83-106">The **New-AzureRmTrafficManagerProfile** cmdlet creates an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="11c83-107">Especifique o parâmetro *Name* e as configurações necessárias.</span><span class="sxs-lookup"><span data-stu-id="11c83-107">Specify the *Name* parameter and required settings.</span></span>
<span data-ttu-id="11c83-108">Esse cmdlet retorna um objeto local que representa o novo perfil.</span><span class="sxs-lookup"><span data-stu-id="11c83-108">This cmdlet returns a local object that represents the new profile.</span></span>

<span data-ttu-id="11c83-109">Esse cmdlet não configura pontos de extremidade do Gerenciador de tráfego.</span><span class="sxs-lookup"><span data-stu-id="11c83-109">This cmdlet does not configure Traffic Manager endpoints.</span></span>
<span data-ttu-id="11c83-110">Você pode atualizar o objeto de perfil local usando o cmdlet Add-AzureRmTrafficManagerEndpointConfig.</span><span class="sxs-lookup"><span data-stu-id="11c83-110">You can update the local profile object by using the Add-AzureRmTrafficManagerEndpointConfig cmdlet.</span></span>
<span data-ttu-id="11c83-111">Em seguida, carregue alterações no Gerenciador de tráfego usando o cmdlet Set-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="11c83-111">Then upload changes to Traffic Manager by using the Set-AzureRmTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="11c83-112">Você também pode adicionar pontos de extremidade usando o cmdlet New-AzureRmTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="11c83-112">Alternatively, you can add endpoints by using the New-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="11c83-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="11c83-113">EXAMPLES</span></span>

### <span data-ttu-id="11c83-114">Exemplo 1: criar um perfil</span><span class="sxs-lookup"><span data-stu-id="11c83-114">Example 1: Create a profile</span></span>
```
PS C:\>New-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" -ProfileStatus Enabled -TrafficRoutingMethod Performance -RelativeDnsName "contosoapp" -TTL 30 -MonitorProtocol HTTP -MonitorPort 80 -MonitorPath "/default.aspx"
```

<span data-ttu-id="11c83-115">Esse comando cria um perfil do Gerenciador de tráfego do Azure chamado ContosoProfile na ResourceGroup11 do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="11c83-115">This command creates an Azure Traffic Manager profile named ContosoProfile in resource group ResourceGroup11.</span></span>
<span data-ttu-id="11c83-116">O FQDN do DNS é contosoapp.trafficmanager.net.</span><span class="sxs-lookup"><span data-stu-id="11c83-116">The DNS FQDN is contosoapp.trafficmanager.net.</span></span>

## <span data-ttu-id="11c83-117">OS</span><span class="sxs-lookup"><span data-stu-id="11c83-117">PARAMETERS</span></span>

### <span data-ttu-id="11c83-118">-CustomHeader</span><span class="sxs-lookup"><span data-stu-id="11c83-118">-CustomHeader</span></span>
<span data-ttu-id="11c83-119">Lista de pares de nome e valor do cabeçalho personalizado para solicitações de sondagem.</span><span class="sxs-lookup"><span data-stu-id="11c83-119">List of custom header name and value pairs for probe requests.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11c83-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11c83-120">-DefaultProfile</span></span>
<span data-ttu-id="11c83-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="11c83-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="11c83-122">-ExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="11c83-122">-ExpectedStatusCodeRange</span></span>
<span data-ttu-id="11c83-123">Lista de intervalos de código de status HTTP esperados para solicitações de sondagem.</span><span class="sxs-lookup"><span data-stu-id="11c83-123">List of expected HTTP status code ranges for probe requests.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerExpectedStatusCodeRange]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11c83-124">-MaxReturn</span><span class="sxs-lookup"><span data-stu-id="11c83-124">-MaxReturn</span></span>
<span data-ttu-id="11c83-125">O número máximo de respostas retornadas para perfis com um método de roteamento de vários valores.</span><span class="sxs-lookup"><span data-stu-id="11c83-125">The maximum number of answers returned for profiles with a MultiValue routing method.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11c83-126">-MonitorIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="11c83-126">-MonitorIntervalInSeconds</span></span>
<span data-ttu-id="11c83-127">O intervalo (em segundos) em que o Gerenciador de tráfego verificará a integridade de cada ponto de extremidade neste perfil.</span><span class="sxs-lookup"><span data-stu-id="11c83-127">The interval (in seconds) at which Traffic Manager will check the health of each endpoint in this profile.</span></span> <span data-ttu-id="11c83-128">O padrão é 30.</span><span class="sxs-lookup"><span data-stu-id="11c83-128">The default is 30.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: IntervalInSecondsForMonitor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11c83-129">-MonitorPath</span><span class="sxs-lookup"><span data-stu-id="11c83-129">-MonitorPath</span></span>
<span data-ttu-id="11c83-130">Especifica o caminho que é usado para monitorar a integridade do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="11c83-130">Specifies the path that is used to monitor endpoint health.</span></span>
<span data-ttu-id="11c83-131">Especifique um valor relativo ao nome de domínio do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="11c83-131">Specify a value relative to the endpoint domain name.</span></span>
<span data-ttu-id="11c83-132">Esse valor deve começar com uma barra (/).</span><span class="sxs-lookup"><span data-stu-id="11c83-132">This value must begin with a slash (/).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PathForMonitor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11c83-133">-MonitorPort</span><span class="sxs-lookup"><span data-stu-id="11c83-133">-MonitorPort</span></span>
<span data-ttu-id="11c83-134">Especifica a porta TCP que é usada para monitorar a integridade do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="11c83-134">Specifies the TCP port that is used to monitor endpoint health.</span></span>
<span data-ttu-id="11c83-135">Os valores válidos são inteiros de 1 a 65535.</span><span class="sxs-lookup"><span data-stu-id="11c83-135">Valid values are integers from 1 through 65535.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases: PortForMonitor

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11c83-136">-MonitorProtocol</span><span class="sxs-lookup"><span data-stu-id="11c83-136">-MonitorProtocol</span></span>
<span data-ttu-id="11c83-137">Especifica o protocolo a ser usado para monitorar a integridade do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="11c83-137">Specifies the protocol to use to monitor endpoint health.</span></span>
<span data-ttu-id="11c83-138">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="11c83-138">Valid values are:</span></span>

- <span data-ttu-id="11c83-139">HTTP</span><span class="sxs-lookup"><span data-stu-id="11c83-139">HTTP</span></span>
- <span data-ttu-id="11c83-140">HTTPS</span><span class="sxs-lookup"><span data-stu-id="11c83-140">HTTPS</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ProtocolForMonitor
Accepted values: HTTP, HTTPS, TCP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11c83-141">-MonitorTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="11c83-141">-MonitorTimeoutInSeconds</span></span>
<span data-ttu-id="11c83-142">O tempo (em segundos) que o Gerenciador de tráfego permite que pontos de extremidade neste perfil respondam à verificação de integridade.</span><span class="sxs-lookup"><span data-stu-id="11c83-142">The time (in seconds) that Traffic Manager allows endpoints in this profile to respond to the health check.</span></span> <span data-ttu-id="11c83-143">O padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="11c83-143">The default is 10.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: TimeoutInSecondsForMonitor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11c83-144">-MonitorToleratedNumberOfFailures</span><span class="sxs-lookup"><span data-stu-id="11c83-144">-MonitorToleratedNumberOfFailures</span></span>
<span data-ttu-id="11c83-145">O número de verificações de integridade com falha consecutivas que o Gerenciador de tráfego tolera antes de declarar um ponto de extremidade neste perfil danificado após a próxima verificação de integridade de falha consecutiva.</span><span class="sxs-lookup"><span data-stu-id="11c83-145">The number of consecutive failed health checks that Traffic Manager tolerates before declaring an endpoint in this profile Degraded after the next consecutive failed health check.</span></span> <span data-ttu-id="11c83-146">O padrão é 3.</span><span class="sxs-lookup"><span data-stu-id="11c83-146">The default is 3.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ToleratedNumberOfFailuresForMonitor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11c83-147">-Nome</span><span class="sxs-lookup"><span data-stu-id="11c83-147">-Name</span></span>
<span data-ttu-id="11c83-148">Especifica um nome para o perfil do Gerenciador de tráfego que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="11c83-148">Specifies a name for the Traffic Manager profile that this cmdlet creates.</span></span>

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

### <span data-ttu-id="11c83-149">-ProfileStatus</span><span class="sxs-lookup"><span data-stu-id="11c83-149">-ProfileStatus</span></span>
<span data-ttu-id="11c83-150">Especifica o status do perfil.</span><span class="sxs-lookup"><span data-stu-id="11c83-150">Specifies the status of the profile.</span></span>
<span data-ttu-id="11c83-151">Os valores válidos são: Enabled e Disabled.</span><span class="sxs-lookup"><span data-stu-id="11c83-151">Valid values are: Enabled and Disabled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11c83-152">-RelativeDnsName</span><span class="sxs-lookup"><span data-stu-id="11c83-152">-RelativeDnsName</span></span>
<span data-ttu-id="11c83-153">Especifica o nome DNS relativo que esse perfil do Gerenciador de tráfego fornece.</span><span class="sxs-lookup"><span data-stu-id="11c83-153">Specifies the relative DNS name that this Traffic Manager profile provides.</span></span>
<span data-ttu-id="11c83-154">O Gerenciador de tráfego combina esse valor e o nome de domínio DNS que o Gerenciador de tráfego do Azure usa para formar o nome de domínio totalmente qualificado (FQDN) do perfil.</span><span class="sxs-lookup"><span data-stu-id="11c83-154">Traffic Manager combines this value and the DNS domain name that Azure Traffic Manager uses to form the fully qualified domain name (FQDN) of the profile.</span></span>

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

### <span data-ttu-id="11c83-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11c83-155">-ResourceGroupName</span></span>
<span data-ttu-id="11c83-156">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="11c83-156">Specifies the name of a resource group.</span></span>
<span data-ttu-id="11c83-157">Esse cmdlet cria um perfil do Gerenciador de tráfego no grupo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="11c83-157">This cmdlet creates a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="11c83-158">-Marca</span><span class="sxs-lookup"><span data-stu-id="11c83-158">-Tag</span></span>
<span data-ttu-id="11c83-159">Pares de valores chave na forma de uma tabela de hash definidas como marcas no servidor.</span><span class="sxs-lookup"><span data-stu-id="11c83-159">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="11c83-160">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="11c83-160">For example:</span></span>

<span data-ttu-id="11c83-161">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="11c83-161">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11c83-162">-TrafficRoutingMethod</span><span class="sxs-lookup"><span data-stu-id="11c83-162">-TrafficRoutingMethod</span></span>
<span data-ttu-id="11c83-163">Especifica o método de roteamento de tráfego.</span><span class="sxs-lookup"><span data-stu-id="11c83-163">Specifies the traffic routing method.</span></span>
<span data-ttu-id="11c83-164">Esse método determina qual Gerenciador de tráfego de ponto de extremidade retorna em resposta a consultas DNS de entrada.</span><span class="sxs-lookup"><span data-stu-id="11c83-164">This method determines which endpoint Traffic Manager returns in response to incoming DNS queries.</span></span>
<span data-ttu-id="11c83-165">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="11c83-165">Valid values are:</span></span>

- <span data-ttu-id="11c83-166">Execução</span><span class="sxs-lookup"><span data-stu-id="11c83-166">Performance</span></span>
- <span data-ttu-id="11c83-167">Ponderada</span><span class="sxs-lookup"><span data-stu-id="11c83-167">Weighted</span></span>
- <span data-ttu-id="11c83-168">Prioritário</span><span class="sxs-lookup"><span data-stu-id="11c83-168">Priority</span></span>
- <span data-ttu-id="11c83-169">Região</span><span class="sxs-lookup"><span data-stu-id="11c83-169">Geographic</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Performance, Weighted, Priority, Geographic

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11c83-170">-TTL</span><span class="sxs-lookup"><span data-stu-id="11c83-170">-Ttl</span></span>
<span data-ttu-id="11c83-171">Especifica o valor do tempo de vida (TTL) do DNS.</span><span class="sxs-lookup"><span data-stu-id="11c83-171">Specifies the DNS Time to Live (TTL) value.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11c83-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11c83-172">CommonParameters</span></span>
<span data-ttu-id="11c83-173">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11c83-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11c83-174">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11c83-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11c83-175">SENSORES</span><span class="sxs-lookup"><span data-stu-id="11c83-175">INPUTS</span></span>

### <span data-ttu-id="11c83-176">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="11c83-176">None</span></span>
<span data-ttu-id="11c83-177">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="11c83-177">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="11c83-178">EXIBE</span><span class="sxs-lookup"><span data-stu-id="11c83-178">OUTPUTS</span></span>

### <span data-ttu-id="11c83-179">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="11c83-179">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="11c83-180">Esse cmdlet retorna um novo objeto TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="11c83-180">This cmdlet returns a new TrafficManagerProfile object.</span></span>

## <span data-ttu-id="11c83-181">INFORMA</span><span class="sxs-lookup"><span data-stu-id="11c83-181">NOTES</span></span>

## <span data-ttu-id="11c83-182">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="11c83-182">RELATED LINKS</span></span>

[<span data-ttu-id="11c83-183">Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="11c83-183">Add-AzureRmTrafficManagerEndpointConfig</span></span>](./Add-AzureRmTrafficManagerEndpointConfig.md)

[<span data-ttu-id="11c83-184">Disable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="11c83-184">Disable-AzureRmTrafficManagerProfile</span></span>](./Disable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="11c83-185">Enable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="11c83-185">Enable-AzureRmTrafficManagerProfile</span></span>](./Enable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="11c83-186">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="11c83-186">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="11c83-187">Remove-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="11c83-187">Remove-AzureRmTrafficManagerProfile</span></span>](./Remove-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="11c83-188">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="11c83-188">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


