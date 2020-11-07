---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 2287E103-442D-47FB-8279-0AE5936412C9
online version: ''
schema: 2.0.0
ms.openlocfilehash: f6a12f0e74964e096577b5a4fec0a46fd41d7872
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946202"
---
# <span data-ttu-id="c3c8d-101">New-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c3c8d-101">New-AzureTrafficManagerProfile</span></span>

## <span data-ttu-id="c3c8d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c3c8d-102">SYNOPSIS</span></span>
<span data-ttu-id="c3c8d-103">Cria um perfil do Gerenciador de tráfego.</span><span class="sxs-lookup"><span data-stu-id="c3c8d-103">Creates a Traffic Manager profile.</span></span>

## <span data-ttu-id="c3c8d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c3c8d-104">SYNTAX</span></span>

```
New-AzureTrafficManagerProfile -Name <String> -DomainName <String> -LoadBalancingMethod <String>
 -MonitorPort <Int32> -MonitorProtocol <String> -MonitorRelativePath <String> -Ttl <Int32>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c3c8d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c3c8d-105">DESCRIPTION</span></span>
<span data-ttu-id="c3c8d-106">O cmdlet **New-AzureTrafficManagerProfile** cria um perfil do Gerenciador de tráfego do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c3c8d-106">The **New-AzureTrafficManagerProfile** cmdlet creates a Microsoft Azure Traffic Manager profile.</span></span>

<span data-ttu-id="c3c8d-107">Depois de criar um perfil no qual você define o valor de *LoadBalancingMethod* como "failover", é possível determinar a ordem de failover dos pontos de extremidade adicionados ao seu perfil com o cmdlet Add-AzureTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="c3c8d-107">After you create a profile where you set the *LoadBalancingMethod* value to "Failover", you can determine the failover order of the endpoints you add to your profile with the Add-AzureTrafficManagerEndpoint cmdlet.</span></span>
<span data-ttu-id="c3c8d-108">Para obter mais informações, consulte o exemplo 2 abaixo.</span><span class="sxs-lookup"><span data-stu-id="c3c8d-108">For more information, see Example 2 below.</span></span>

## <span data-ttu-id="c3c8d-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c3c8d-109">EXAMPLES</span></span>

### <span data-ttu-id="c3c8d-110">Exemplo 1: criar um perfil do Gerenciador de tráfego</span><span class="sxs-lookup"><span data-stu-id="c3c8d-110">Example 1: Create a Traffic Manager profile</span></span>
```
PS C:\>New-AzureTrafficManagerProfile -Name "MyProfile" -DomainName "My.profile.trafficmanager.net" -LoadBalancingMethod "RoundRobin" -Ttl 30 -MonitorProtocol "Http" -MonitorPort 80 -MonitorRelativePath "/"
```

<span data-ttu-id="c3c8d-111">Esse comando cria um perfil do Gerenciador de tráfego chamado MyProfile no domínio do Gerenciador de tráfego especificado com um método de balanceamento de carga de rodízio, um TTL de 30 segundos, protocolo de monitoramento HTTP, monitorando a porta 80 e com o caminho especificado.</span><span class="sxs-lookup"><span data-stu-id="c3c8d-111">This command creates a Traffic Manager profile named MyProfile in the specified Traffic Manager domain with a Round Robin load balancing method, a TTL of 30 seconds, HTTP monitoring protocol, monitoring port 80, and with the specified path.</span></span>

### <span data-ttu-id="c3c8d-112">Exemplo 2: reordenar pontos de extremidade para a ordem de failover desejada</span><span class="sxs-lookup"><span data-stu-id="c3c8d-112">Example 2: Reorder endpoints to desired failover order</span></span>
```
PS C:\>$Profile = Get-AzureTrafficManagerProfile -Name "MyProfile"
PS C:\> $Profile.Endpoints[0],$Profile.Endpoints[1] = $Profile.Endpoints[1],$Profile.Endpoints[0]
PS C:\> $Profile = Set-AzureTrafficManagerProfile
```

<span data-ttu-id="c3c8d-113">Este exemplo reordena os pontos de extremidade adicionados ao MyProfile para a ordem de failover desejada.</span><span class="sxs-lookup"><span data-stu-id="c3c8d-113">This example reorders the endpoints added to MyProfile to the desired failover order.</span></span>

<span data-ttu-id="c3c8d-114">O primeiro comando obtém o objeto de perfil do Gerenciador de tráfego chamado MyProfile e armazena o objeto na variável $Profile.</span><span class="sxs-lookup"><span data-stu-id="c3c8d-114">The first command gets the Traffic Manager profile object named MyProfile and stores the object in the $Profile variable.</span></span>

<span data-ttu-id="c3c8d-115">O segundo comando re-ordena os pontos de extremidade da matriz de pontos de extremidade para a ordem em que o failover deve ocorrer.</span><span class="sxs-lookup"><span data-stu-id="c3c8d-115">The second command re-orders the endpoints from  the endpoints array to the order in which failover should occur.</span></span>

<span data-ttu-id="c3c8d-116">O último comando atualiza o perfil do Gerenciador de tráfego armazenado em $Profile com o novo pedido de ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="c3c8d-116">The last command updates the Traffic Manager profile stored in $Profile with the new endpoint order.</span></span>

## <span data-ttu-id="c3c8d-117">OS</span><span class="sxs-lookup"><span data-stu-id="c3c8d-117">PARAMETERS</span></span>

### <span data-ttu-id="c3c8d-118">-DomainName</span><span class="sxs-lookup"><span data-stu-id="c3c8d-118">-DomainName</span></span>
<span data-ttu-id="c3c8d-119">Especifica o nome de domínio do perfil do Gerenciador de tráfego.</span><span class="sxs-lookup"><span data-stu-id="c3c8d-119">Specifies the domain name of the Traffic Manager profile.</span></span>
<span data-ttu-id="c3c8d-120">Deve ser um subdomínio de trafficmanager.net.</span><span class="sxs-lookup"><span data-stu-id="c3c8d-120">This must be a subdomain of trafficmanager.net.</span></span>

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

### <span data-ttu-id="c3c8d-121">-LoadBalancingMethod</span><span class="sxs-lookup"><span data-stu-id="c3c8d-121">-LoadBalancingMethod</span></span>
<span data-ttu-id="c3c8d-122">Especifica o método de balanceamento de carga a ser usado para distribuir a conexão.</span><span class="sxs-lookup"><span data-stu-id="c3c8d-122">Specifies the load balancing method to use to distribute the connection.</span></span>
<span data-ttu-id="c3c8d-123">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="c3c8d-123">Valid values are:</span></span> 

- <span data-ttu-id="c3c8d-124">Execução</span><span class="sxs-lookup"><span data-stu-id="c3c8d-124">Performance</span></span>
- <span data-ttu-id="c3c8d-125">Falhas</span><span class="sxs-lookup"><span data-stu-id="c3c8d-125">Failover</span></span>
- <span data-ttu-id="c3c8d-126">RoundRobin</span><span class="sxs-lookup"><span data-stu-id="c3c8d-126">RoundRobin</span></span>

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

### <span data-ttu-id="c3c8d-127">-MonitorPort</span><span class="sxs-lookup"><span data-stu-id="c3c8d-127">-MonitorPort</span></span>
<span data-ttu-id="c3c8d-128">Especifica a porta usada para monitorar a integridade do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="c3c8d-128">Specifies the port used to monitor endpoint health.</span></span>
<span data-ttu-id="c3c8d-129">Os valores válidos são valores inteiros superiores a 0 e menores que ou iguais a 65.535.</span><span class="sxs-lookup"><span data-stu-id="c3c8d-129">Valid values are integer values greater than 0 and less than or equal to 65,535.</span></span>

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

### <span data-ttu-id="c3c8d-130">-MonitorProtocol</span><span class="sxs-lookup"><span data-stu-id="c3c8d-130">-MonitorProtocol</span></span>
<span data-ttu-id="c3c8d-131">Especifica o protocolo a ser usado para monitorar a integridade do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="c3c8d-131">Specifies the protocol to use to monitor endpoint health.</span></span>
<span data-ttu-id="c3c8d-132">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="c3c8d-132">Valid values are:</span></span> 

- <span data-ttu-id="c3c8d-133">Http</span><span class="sxs-lookup"><span data-stu-id="c3c8d-133">Http</span></span>

- <span data-ttu-id="c3c8d-134">Https</span><span class="sxs-lookup"><span data-stu-id="c3c8d-134">Https</span></span>

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

### <span data-ttu-id="c3c8d-135">-MonitorRelativePath</span><span class="sxs-lookup"><span data-stu-id="c3c8d-135">-MonitorRelativePath</span></span>
<span data-ttu-id="c3c8d-136">Especifica o caminho relativo ao nome do domínio do ponto de extremidade para investigar o estado de integridade.</span><span class="sxs-lookup"><span data-stu-id="c3c8d-136">Specifies the path relative to the endpoint domain name to probe for health state.</span></span>
<span data-ttu-id="c3c8d-137">O caminho deve atender às seguintes restrições:</span><span class="sxs-lookup"><span data-stu-id="c3c8d-137">The path must meet the following restrictions:</span></span> 

- <span data-ttu-id="c3c8d-138">O caminho deve ter entre 1 e 1000 caracteres.</span><span class="sxs-lookup"><span data-stu-id="c3c8d-138">The path must be from 1 through 1000 characters.</span></span>

- <span data-ttu-id="c3c8d-139">Ele deve começar com uma barra de encaminhamento/.</span><span class="sxs-lookup"><span data-stu-id="c3c8d-139">It must start with a forward slash, /.</span></span>

- <span data-ttu-id="c3c8d-140">Ele deve conter nenhum elemento XML \<\> .</span><span class="sxs-lookup"><span data-stu-id="c3c8d-140">It must contain no XML elements, \<\>.</span></span>

- <span data-ttu-id="c3c8d-141">Ele deve conter duas barras,//.</span><span class="sxs-lookup"><span data-stu-id="c3c8d-141">It must contain no double slashes, //.</span></span>

- <span data-ttu-id="c3c8d-142">Ele deve conter nenhum caractere de escape HTML inválidos.</span><span class="sxs-lookup"><span data-stu-id="c3c8d-142">It must contain no invalid HTML escape characters.</span></span>
<span data-ttu-id="c3c8d-143">Por exemplo,% XY.</span><span class="sxs-lookup"><span data-stu-id="c3c8d-143">For example, %XY.</span></span>

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

### <span data-ttu-id="c3c8d-144">-Nome</span><span class="sxs-lookup"><span data-stu-id="c3c8d-144">-Name</span></span>
<span data-ttu-id="c3c8d-145">Especifica o nome do perfil do Gerenciador de tráfego a ser criado.</span><span class="sxs-lookup"><span data-stu-id="c3c8d-145">Specifies the name of the Traffic Manager profile to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3c8d-146">-Perfil</span><span class="sxs-lookup"><span data-stu-id="c3c8d-146">-Profile</span></span>
<span data-ttu-id="c3c8d-147">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="c3c8d-147">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="c3c8d-148">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="c3c8d-148">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3c8d-149">-TTL</span><span class="sxs-lookup"><span data-stu-id="c3c8d-149">-Ttl</span></span>
<span data-ttu-id="c3c8d-150">Especifica o tempo de vida útil (TTL) do DNS que informa os resolvedores DNS locais por quanto tempo armazenar em cache as entradas DNS.</span><span class="sxs-lookup"><span data-stu-id="c3c8d-150">Specifies the DNS Time-to-Live (TTL) that informs the Local DNS resolvers how long to cache DNS entries.</span></span>
<span data-ttu-id="c3c8d-151">Os valores válidos são inteiros de 30 a 999.999.</span><span class="sxs-lookup"><span data-stu-id="c3c8d-151">Valid values are integers from 30 through 999,999.</span></span>

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

### <span data-ttu-id="c3c8d-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3c8d-152">CommonParameters</span></span>
<span data-ttu-id="c3c8d-153">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3c8d-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3c8d-154">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3c8d-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3c8d-155">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c3c8d-155">INPUTS</span></span>

## <span data-ttu-id="c3c8d-156">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c3c8d-156">OUTPUTS</span></span>

### <span data-ttu-id="c3c8d-157">Microsoft. WindowsAzure. Commands. Utilities. Trafficmanager. Models. IProfileWithDefinition</span><span class="sxs-lookup"><span data-stu-id="c3c8d-157">Microsoft.WindowsAzure.Commands.Utilities.TrafficManager.Models.IProfileWithDefinition</span></span>
<span data-ttu-id="c3c8d-158">Esse cmdlet gera um objeto de perfil do Gerenciador de tráfego.</span><span class="sxs-lookup"><span data-stu-id="c3c8d-158">This cmdlet generates a Traffic Manager profile object.</span></span>

## <span data-ttu-id="c3c8d-159">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c3c8d-159">NOTES</span></span>

## <span data-ttu-id="c3c8d-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c3c8d-160">RELATED LINKS</span></span>

[<span data-ttu-id="c3c8d-161">Disable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c3c8d-161">Disable-AzureTrafficManagerProfile</span></span>](./Disable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="c3c8d-162">Enable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c3c8d-162">Enable-AzureTrafficManagerProfile</span></span>](./Enable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="c3c8d-163">Get-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c3c8d-163">Get-AzureTrafficManagerProfile</span></span>](./Get-AzureTrafficManagerProfile.md)

[<span data-ttu-id="c3c8d-164">Remove-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c3c8d-164">Remove-AzureTrafficManagerProfile</span></span>](./Remove-AzureTrafficManagerProfile.md)

[<span data-ttu-id="c3c8d-165">Set-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c3c8d-165">Set-AzureTrafficManagerProfile</span></span>](./Set-AzureTrafficManagerProfile.md)


