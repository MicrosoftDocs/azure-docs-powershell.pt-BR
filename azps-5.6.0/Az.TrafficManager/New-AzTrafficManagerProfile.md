---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: DE31891A-0EF7-44D7-B955-A3279D27CC21
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/new-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/New-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/New-AzTrafficManagerProfile.md
ms.openlocfilehash: a17f88a23399fda7f4775ca52fbe1d4aec35594d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885238"
---
# <span data-ttu-id="c7a0c-101">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c7a0c-101">New-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="c7a0c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7a0c-102">SYNOPSIS</span></span>
<span data-ttu-id="c7a0c-103">Cria um perfil do Gerenciador de Tráfego.</span><span class="sxs-lookup"><span data-stu-id="c7a0c-103">Creates a Traffic Manager profile.</span></span>

## <span data-ttu-id="c7a0c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c7a0c-104">SYNTAX</span></span>

```
New-AzTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-ProfileStatus <String>]
 -RelativeDnsName <String> -Ttl <UInt32> -TrafficRoutingMethod <String> -MonitorProtocol <String>
 -MonitorPort <UInt32> [-MonitorPath <String>] [-MonitorIntervalInSeconds <Int32>]
 [-MonitorTimeoutInSeconds <Int32>] [-MonitorToleratedNumberOfFailures <Int32>] [-MaxReturn <Int64>]
 [-Tag <Hashtable>]
 [-CustomHeader <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]>]
 [-ExpectedStatusCodeRange <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerExpectedStatusCodeRange]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7a0c-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c7a0c-105">DESCRIPTION</span></span>
<span data-ttu-id="c7a0c-106">O cmdlet **New-AzTrafficManagerProfile** cria um perfil do Gerenciador de Tráfego do Azure.</span><span class="sxs-lookup"><span data-stu-id="c7a0c-106">The **New-AzTrafficManagerProfile** cmdlet creates an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="c7a0c-107">*Especifique o parâmetro Name* e as configurações necessárias.</span><span class="sxs-lookup"><span data-stu-id="c7a0c-107">Specify the *Name* parameter and required settings.</span></span>
<span data-ttu-id="c7a0c-108">Este cmdlet retorna um objeto local que representa o novo perfil.</span><span class="sxs-lookup"><span data-stu-id="c7a0c-108">This cmdlet returns a local object that represents the new profile.</span></span>

<span data-ttu-id="c7a0c-109">Este cmdlet não configura pontos de extremidade do Gerenciador de Tráfego.</span><span class="sxs-lookup"><span data-stu-id="c7a0c-109">This cmdlet does not configure Traffic Manager endpoints.</span></span>
<span data-ttu-id="c7a0c-110">Você pode atualizar o objeto de perfil local usando o cmdlet Add-AzTrafficManagerEndpointConfig local.</span><span class="sxs-lookup"><span data-stu-id="c7a0c-110">You can update the local profile object by using the Add-AzTrafficManagerEndpointConfig cmdlet.</span></span>
<span data-ttu-id="c7a0c-111">Em seguida, carregue as alterações no Gerenciador de Tráfego usando Set-AzTrafficManagerProfile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c7a0c-111">Then upload changes to Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="c7a0c-112">Como alternativa, você pode adicionar pontos de extremidade usando o New-AzTrafficManagerEndpoint cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c7a0c-112">Alternatively, you can add endpoints by using the New-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="c7a0c-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c7a0c-113">EXAMPLES</span></span>

### <span data-ttu-id="c7a0c-114">Exemplo 1: Criar um perfil</span><span class="sxs-lookup"><span data-stu-id="c7a0c-114">Example 1: Create a profile</span></span>
```
PS C:\>New-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" -ProfileStatus Enabled -TrafficRoutingMethod Performance -RelativeDnsName "contosoapp" -TTL 30 -MonitorProtocol HTTP -MonitorPort 80 -MonitorPath "/default.aspx"
```

<span data-ttu-id="c7a0c-115">Este comando cria um perfil do Gerenciador de Tráfego do Azure chamado ContosoProfile no grupo de recursos ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="c7a0c-115">This command creates an Azure Traffic Manager profile named ContosoProfile in resource group ResourceGroup11.</span></span>
<span data-ttu-id="c7a0c-116">O FQDN DNS é contosoapp.trafficmanager.net.</span><span class="sxs-lookup"><span data-stu-id="c7a0c-116">The DNS FQDN is contosoapp.trafficmanager.net.</span></span>

## <span data-ttu-id="c7a0c-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c7a0c-117">PARAMETERS</span></span>

### <span data-ttu-id="c7a0c-118">-CustomHeader</span><span class="sxs-lookup"><span data-stu-id="c7a0c-118">-CustomHeader</span></span>
<span data-ttu-id="c7a0c-119">Lista de pares de nomes de header personalizados e valores para solicitações de sonda.</span><span class="sxs-lookup"><span data-stu-id="c7a0c-119">List of custom header name and value pairs for probe requests.</span></span>

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

### <span data-ttu-id="c7a0c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7a0c-120">-DefaultProfile</span></span>
<span data-ttu-id="c7a0c-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="c7a0c-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7a0c-122">-ExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="c7a0c-122">-ExpectedStatusCodeRange</span></span>
<span data-ttu-id="c7a0c-123">Lista de intervalos de código de status HTTP esperados para solicitações de sonda.</span><span class="sxs-lookup"><span data-stu-id="c7a0c-123">List of expected HTTP status code ranges for probe requests.</span></span>

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

### <span data-ttu-id="c7a0c-124">-MaxReturn</span><span class="sxs-lookup"><span data-stu-id="c7a0c-124">-MaxReturn</span></span>
<span data-ttu-id="c7a0c-125">O número máximo de respostas retornadas para perfis com um método de roteamento MultiValue.</span><span class="sxs-lookup"><span data-stu-id="c7a0c-125">The maximum number of answers returned for profiles with a MultiValue routing method.</span></span>

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

### <span data-ttu-id="c7a0c-126">-MonitorIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="c7a0c-126">-MonitorIntervalInSeconds</span></span>
<span data-ttu-id="c7a0c-127">O intervalo (em segundos) no qual o Gerenciador de Tráfego verificará a saúde de cada ponto de extremidade neste perfil.</span><span class="sxs-lookup"><span data-stu-id="c7a0c-127">The interval (in seconds) at which Traffic Manager will check the health of each endpoint in this profile.</span></span> <span data-ttu-id="c7a0c-128">O padrão é 30.</span><span class="sxs-lookup"><span data-stu-id="c7a0c-128">The default is 30.</span></span>

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

### <span data-ttu-id="c7a0c-129">-MonitorPath</span><span class="sxs-lookup"><span data-stu-id="c7a0c-129">-MonitorPath</span></span>
<span data-ttu-id="c7a0c-130">Especifica o caminho usado para monitorar a saúde do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="c7a0c-130">Specifies the path that is used to monitor endpoint health.</span></span>
<span data-ttu-id="c7a0c-131">Especifique um valor relativo ao nome de domínio do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="c7a0c-131">Specify a value relative to the endpoint domain name.</span></span>
<span data-ttu-id="c7a0c-132">Esse valor deve começar com uma barra (/).</span><span class="sxs-lookup"><span data-stu-id="c7a0c-132">This value must begin with a slash (/).</span></span>

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

### <span data-ttu-id="c7a0c-133">-MonitorPort</span><span class="sxs-lookup"><span data-stu-id="c7a0c-133">-MonitorPort</span></span>
<span data-ttu-id="c7a0c-134">Especifica a porta TCP usada para monitorar a saúde do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="c7a0c-134">Specifies the TCP port that is used to monitor endpoint health.</span></span>
<span data-ttu-id="c7a0c-135">Os valores válidos são inteiros de 1 a 65535.</span><span class="sxs-lookup"><span data-stu-id="c7a0c-135">Valid values are integers from 1 through 65535.</span></span>

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

### <span data-ttu-id="c7a0c-136">-MonitorProtocol</span><span class="sxs-lookup"><span data-stu-id="c7a0c-136">-MonitorProtocol</span></span>
<span data-ttu-id="c7a0c-137">Especifica o protocolo a ser usado para monitorar a saúde do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="c7a0c-137">Specifies the protocol to use to monitor endpoint health.</span></span>
<span data-ttu-id="c7a0c-138">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="c7a0c-138">Valid values are:</span></span>

- <span data-ttu-id="c7a0c-139">HTTP</span><span class="sxs-lookup"><span data-stu-id="c7a0c-139">HTTP</span></span>
- <span data-ttu-id="c7a0c-140">HTTPS</span><span class="sxs-lookup"><span data-stu-id="c7a0c-140">HTTPS</span></span>

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

### <span data-ttu-id="c7a0c-141">-MonitorTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="c7a0c-141">-MonitorTimeoutInSeconds</span></span>
<span data-ttu-id="c7a0c-142">O tempo (em segundos) que o Gerenciador de Tráfego permite que os pontos de extremidade neste perfil respondam à verificação de saúde.</span><span class="sxs-lookup"><span data-stu-id="c7a0c-142">The time (in seconds) that Traffic Manager allows endpoints in this profile to respond to the health check.</span></span> <span data-ttu-id="c7a0c-143">O padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="c7a0c-143">The default is 10.</span></span>

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

### <span data-ttu-id="c7a0c-144">-MonitorToleratedNumberOfFailures</span><span class="sxs-lookup"><span data-stu-id="c7a0c-144">-MonitorToleratedNumberOfFailures</span></span>
<span data-ttu-id="c7a0c-145">O número de verificações consecutivas de falhas de saúde que o Gerenciador de Tráfego tolera antes de declarar um ponto de extremidade neste perfil Degradado após a próxima verificação de saúde com falha consecutiva.</span><span class="sxs-lookup"><span data-stu-id="c7a0c-145">The number of consecutive failed health checks that Traffic Manager tolerates before declaring an endpoint in this profile Degraded after the next consecutive failed health check.</span></span> <span data-ttu-id="c7a0c-146">O padrão é 3.</span><span class="sxs-lookup"><span data-stu-id="c7a0c-146">The default is 3.</span></span>

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

### <span data-ttu-id="c7a0c-147">-Name</span><span class="sxs-lookup"><span data-stu-id="c7a0c-147">-Name</span></span>
<span data-ttu-id="c7a0c-148">Especifica um nome para o perfil do Gerenciador de Tráfego que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="c7a0c-148">Specifies a name for the Traffic Manager profile that this cmdlet creates.</span></span>

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

### <span data-ttu-id="c7a0c-149">-ProfileStatus</span><span class="sxs-lookup"><span data-stu-id="c7a0c-149">-ProfileStatus</span></span>
<span data-ttu-id="c7a0c-150">Especifica o status do perfil.</span><span class="sxs-lookup"><span data-stu-id="c7a0c-150">Specifies the status of the profile.</span></span>
<span data-ttu-id="c7a0c-151">Os valores válidos são: Habilitado e Desabilitado.</span><span class="sxs-lookup"><span data-stu-id="c7a0c-151">Valid values are: Enabled and Disabled.</span></span>

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

### <span data-ttu-id="c7a0c-152">-RelativeDnsName</span><span class="sxs-lookup"><span data-stu-id="c7a0c-152">-RelativeDnsName</span></span>
<span data-ttu-id="c7a0c-153">Especifica o nome DNS relativo que esse perfil do Gerenciador de Tráfego fornece.</span><span class="sxs-lookup"><span data-stu-id="c7a0c-153">Specifies the relative DNS name that this Traffic Manager profile provides.</span></span>
<span data-ttu-id="c7a0c-154">O Gerenciador de Tráfego combina esse valor e o nome de domínio DNS que o Gerenciador de Tráfego do Azure usa para formar o FQDN (nome de domínio totalmente qualificado) do perfil.</span><span class="sxs-lookup"><span data-stu-id="c7a0c-154">Traffic Manager combines this value and the DNS domain name that Azure Traffic Manager uses to form the fully qualified domain name (FQDN) of the profile.</span></span>

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

### <span data-ttu-id="c7a0c-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7a0c-155">-ResourceGroupName</span></span>
<span data-ttu-id="c7a0c-156">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c7a0c-156">Specifies the name of a resource group.</span></span>
<span data-ttu-id="c7a0c-157">Este cmdlet cria um perfil do Gerenciador de Tráfego no grupo especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="c7a0c-157">This cmdlet creates a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="c7a0c-158">-Tag</span><span class="sxs-lookup"><span data-stu-id="c7a0c-158">-Tag</span></span>
<span data-ttu-id="c7a0c-159">Pares de valores-chave na forma de um conjunto de tabelas de hash como marcas no servidor.</span><span class="sxs-lookup"><span data-stu-id="c7a0c-159">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="c7a0c-160">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="c7a0c-160">For example:</span></span>

<span data-ttu-id="c7a0c-161">@{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="c7a0c-161">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="c7a0c-162">-TrafficRoutingMethod</span><span class="sxs-lookup"><span data-stu-id="c7a0c-162">-TrafficRoutingMethod</span></span>
<span data-ttu-id="c7a0c-163">Especifica o método de roteamento de tráfego.</span><span class="sxs-lookup"><span data-stu-id="c7a0c-163">Specifies the traffic routing method.</span></span>
<span data-ttu-id="c7a0c-164">Este método determina qual ponto de extremidade o Gerenciador de Tráfego retorna em resposta às consultas DNS de entrada.</span><span class="sxs-lookup"><span data-stu-id="c7a0c-164">This method determines which endpoint Traffic Manager returns in response to incoming DNS queries.</span></span>
<span data-ttu-id="c7a0c-165">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="c7a0c-165">Valid values are:</span></span>

- <span data-ttu-id="c7a0c-166">Desempenho</span><span class="sxs-lookup"><span data-stu-id="c7a0c-166">Performance</span></span>
- <span data-ttu-id="c7a0c-167">Ponderado</span><span class="sxs-lookup"><span data-stu-id="c7a0c-167">Weighted</span></span>
- <span data-ttu-id="c7a0c-168">Prioridade</span><span class="sxs-lookup"><span data-stu-id="c7a0c-168">Priority</span></span>
- <span data-ttu-id="c7a0c-169">Geográfico</span><span class="sxs-lookup"><span data-stu-id="c7a0c-169">Geographic</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Performance, Weighted, Priority, Geographic, Subnet, MultiValue

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7a0c-170">-Ttl</span><span class="sxs-lookup"><span data-stu-id="c7a0c-170">-Ttl</span></span>
<span data-ttu-id="c7a0c-171">Especifica o valor DNS Time to Live (TTL).</span><span class="sxs-lookup"><span data-stu-id="c7a0c-171">Specifies the DNS Time to Live (TTL) value.</span></span>

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

### <span data-ttu-id="c7a0c-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7a0c-172">CommonParameters</span></span>
<span data-ttu-id="c7a0c-173">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7a0c-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7a0c-174">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7a0c-174">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7a0c-175">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c7a0c-175">INPUTS</span></span>

### <span data-ttu-id="c7a0c-176">Nenhum</span><span class="sxs-lookup"><span data-stu-id="c7a0c-176">None</span></span>

## <span data-ttu-id="c7a0c-177">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c7a0c-177">OUTPUTS</span></span>

### <span data-ttu-id="c7a0c-178">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c7a0c-178">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="c7a0c-179">NOTES</span><span class="sxs-lookup"><span data-stu-id="c7a0c-179">NOTES</span></span>

## <span data-ttu-id="c7a0c-180">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c7a0c-180">RELATED LINKS</span></span>

[<span data-ttu-id="c7a0c-181">Add-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="c7a0c-181">Add-AzTrafficManagerEndpointConfig</span></span>](./Add-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="c7a0c-182">Disable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c7a0c-182">Disable-AzTrafficManagerProfile</span></span>](./Disable-AzTrafficManagerProfile.md)

[<span data-ttu-id="c7a0c-183">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c7a0c-183">Enable-AzTrafficManagerProfile</span></span>](./Enable-AzTrafficManagerProfile.md)

[<span data-ttu-id="c7a0c-184">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c7a0c-184">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="c7a0c-185">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c7a0c-185">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)

[<span data-ttu-id="c7a0c-186">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c7a0c-186">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


