---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 700AC44E-4FD5-4516-80F3-B8C9E4DF6ABC
online version: ''
schema: 2.0.0
ms.openlocfilehash: d37397b4e0ce9f1d9878860eb5e7a431e58a20a9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945794"
---
# <span data-ttu-id="f6d27-101">Set-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f6d27-101">Set-AzureTrafficManagerProfile</span></span>

## <span data-ttu-id="f6d27-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f6d27-102">SYNOPSIS</span></span>
<span data-ttu-id="f6d27-103">Atualiza as propriedades de um perfil do Gerenciador de tráfego.</span><span class="sxs-lookup"><span data-stu-id="f6d27-103">Updates the properties of a Traffic Manager profile.</span></span>

## <span data-ttu-id="f6d27-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f6d27-104">SYNTAX</span></span>

```
Set-AzureTrafficManagerProfile [-Name <String>] [-LoadBalancingMethod <String>] [-MonitorPort <Int32>]
 [-MonitorProtocol <String>] [-MonitorRelativePath <String>] [-Ttl <Int32>]
 -TrafficManagerProfile <IProfileWithDefinition> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f6d27-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f6d27-105">DESCRIPTION</span></span>
<span data-ttu-id="f6d27-106">O cmdlet **set-AzureTrafficManagerProfile** atualiza as propriedades de um perfil do Gerenciador de tráfego do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f6d27-106">The **Set-AzureTrafficManagerProfile** cmdlet updates the properties of a Microsoft Azure Traffic Manager profile.</span></span>

<span data-ttu-id="f6d27-107">Para perfis para os quais você definiu o valor de *LoadBalancingMethod* como "failover", é possível determinar a ordem de failover dos pontos de extremidade que você adicionou ao seu perfil com o cmdlet Add-AzureTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="f6d27-107">For profiles for which you have set the *LoadBalancingMethod* value to "Failover", you can determine the failover order of the endpoints you have added to your profile with the Add-AzureTrafficManagerEndpoint cmdlet.</span></span>
<span data-ttu-id="f6d27-108">Para obter mais informações, consulte o exemplo 3 abaixo.</span><span class="sxs-lookup"><span data-stu-id="f6d27-108">For more information, see Example 3 below.</span></span>

## <span data-ttu-id="f6d27-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f6d27-109">EXAMPLES</span></span>

### <span data-ttu-id="f6d27-110">Exemplo 1: definir o TTL para um perfil do Gerenciador de tráfego</span><span class="sxs-lookup"><span data-stu-id="f6d27-110">Example 1: Set the TTL for a Traffic Manager profile</span></span>
```
PS C:\>Set-AzureTrafficManagerProfile -TrafficManagerProfile $MyTrafficManagerProfile -Ttl 60
```

<span data-ttu-id="f6d27-111">Esse comando define o TTL como 60 segundos para o objeto de perfil do Gerenciador de tráfego MyTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="f6d27-111">This command sets the TTL to 60 seconds for the Traffic Manager profile object MyTrafficManagerProfile.</span></span>

### <span data-ttu-id="f6d27-112">Exemplo 2: definir vários valores para um perfil</span><span class="sxs-lookup"><span data-stu-id="f6d27-112">Example 2: Set several values for a profile</span></span>
```
PS C:\>Get-AzureTrafficManagerProfile -Name "MyProfile" | Set-AzureTrafficManagerProfile -LoadBalancingMethod "RoundRobin" -Ttl 30 -MonitorProtocol "Http" -MonitorPort 80 -MonitorRelativePath "/"
```

<span data-ttu-id="f6d27-113">Esse comando obtém um perfil do Gerenciador de tráfego chamado MyProfile usando o cmdlet **Get-AzureTrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="f6d27-113">This command gets a Traffic Manager profile named MyProfile by using the **Get-AzureTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="f6d27-114">O perfil usa o método de balanceamento de carga RoundRobin, um TTL de 30 segundos, o protocolo de Monitor HTTP, a porta de monitor e o caminho relativo para um perfil do Gerenciador de tráfego.</span><span class="sxs-lookup"><span data-stu-id="f6d27-114">The profile uses the RoundRobin load balancing method, a TTL of 30 seconds,  the monitor protocol HTTP, the monitor port, and the relative path for a Traffic Manager profile.</span></span>

### <span data-ttu-id="f6d27-115">Exemplo 3: reordenar pontos de extremidade para a ordem de failover desejada</span><span class="sxs-lookup"><span data-stu-id="f6d27-115">Example 3: Reorder endpoints to desired failover order</span></span>
```
PS C:\>$Profile = Get-AzureTrafficManagerProfile -Name "MyProfile"
PS C:\> $Profile.Endpoints[0],$Profile.Endpoints[1] = $Profile.Endpoints[1],$Profile.Endpoints[0]
PS C:\> $Profile = Set-AzureTrafficManagerProfile
```

<span data-ttu-id="f6d27-116">Este exemplo reordena os pontos de extremidade adicionados ao MyProfile para a ordem de failover desejada.</span><span class="sxs-lookup"><span data-stu-id="f6d27-116">This example reorders the endpoints added to MyProfile to the desired failover order.</span></span>

<span data-ttu-id="f6d27-117">O primeiro comando obtém o objeto de perfil do Gerenciador de tráfego chamado MyProfile e armazena o objeto na variável $Profile.</span><span class="sxs-lookup"><span data-stu-id="f6d27-117">The first command gets the Traffic Manager profile object named MyProfile and stores the object in the $Profile variable.</span></span>

<span data-ttu-id="f6d27-118">O segundo comando re-ordena os pontos de extremidade da matriz de pontos de extremidade para a ordem em que o failover deve ocorrer.</span><span class="sxs-lookup"><span data-stu-id="f6d27-118">The second command re-orders the endpoints from  the endpoints array to the order in which failover should occur.</span></span>

<span data-ttu-id="f6d27-119">O último comando atualiza o perfil do Gerenciador de tráfego armazenado em $Profile com o novo pedido de ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="f6d27-119">The last command updates the Traffic Manager profile stored in $Profile with the new endpoint order.</span></span>

## <span data-ttu-id="f6d27-120">OS</span><span class="sxs-lookup"><span data-stu-id="f6d27-120">PARAMETERS</span></span>

### <span data-ttu-id="f6d27-121">-LoadBalancingMethod</span><span class="sxs-lookup"><span data-stu-id="f6d27-121">-LoadBalancingMethod</span></span>
<span data-ttu-id="f6d27-122">Especifica o método de balanceamento de carga a ser usado para distribuir a conexão.</span><span class="sxs-lookup"><span data-stu-id="f6d27-122">Specifies the load balancing method to use to distribute the connection.</span></span>
<span data-ttu-id="f6d27-123">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="f6d27-123">Valid values are:</span></span> 

- <span data-ttu-id="f6d27-124">Execução</span><span class="sxs-lookup"><span data-stu-id="f6d27-124">Performance</span></span>
- <span data-ttu-id="f6d27-125">Falhas</span><span class="sxs-lookup"><span data-stu-id="f6d27-125">Failover</span></span>
- <span data-ttu-id="f6d27-126">RoundRobin</span><span class="sxs-lookup"><span data-stu-id="f6d27-126">RoundRobin</span></span>

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

### <span data-ttu-id="f6d27-127">-MonitorPort</span><span class="sxs-lookup"><span data-stu-id="f6d27-127">-MonitorPort</span></span>
<span data-ttu-id="f6d27-128">Especifica a porta usada para monitorar a integridade do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="f6d27-128">Specifies the port used to monitor endpoint health.</span></span>
<span data-ttu-id="f6d27-129">Os valores válidos são valores inteiros superiores a 0 e menores que ou iguais a 65.535.</span><span class="sxs-lookup"><span data-stu-id="f6d27-129">Valid values are integer values greater than 0 and less than or equal to 65,535.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6d27-130">-MonitorProtocol</span><span class="sxs-lookup"><span data-stu-id="f6d27-130">-MonitorProtocol</span></span>
<span data-ttu-id="f6d27-131">Especifica o protocolo a ser usado para monitorar a integridade do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="f6d27-131">Specifies the protocol to use to monitor endpoint health.</span></span>
<span data-ttu-id="f6d27-132">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="f6d27-132">Valid values are:</span></span> 

- <span data-ttu-id="f6d27-133">Http</span><span class="sxs-lookup"><span data-stu-id="f6d27-133">Http</span></span>
- <span data-ttu-id="f6d27-134">Https</span><span class="sxs-lookup"><span data-stu-id="f6d27-134">Https</span></span>

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

### <span data-ttu-id="f6d27-135">-MonitorRelativePath</span><span class="sxs-lookup"><span data-stu-id="f6d27-135">-MonitorRelativePath</span></span>
<span data-ttu-id="f6d27-136">Especifica o caminho relativo ao nome do domínio do ponto de extremidade para investigar o estado de integridade.</span><span class="sxs-lookup"><span data-stu-id="f6d27-136">Specifies the path relative to the endpoint domain name to probe for health state.</span></span>
<span data-ttu-id="f6d27-137">O caminho deve atender às seguintes restrições:</span><span class="sxs-lookup"><span data-stu-id="f6d27-137">The path must meet the following restrictions:</span></span> 

- <span data-ttu-id="f6d27-138">O caminho deve ter entre 1 e 1000 caracteres.</span><span class="sxs-lookup"><span data-stu-id="f6d27-138">The path must be from 1 through 1000 characters.</span></span>
- <span data-ttu-id="f6d27-139">Ele deve começar com uma barra de encaminhamento/.</span><span class="sxs-lookup"><span data-stu-id="f6d27-139">It must start with a forward slash, /.</span></span>
- <span data-ttu-id="f6d27-140">Ele deve conter nenhum elemento XML \<\> .</span><span class="sxs-lookup"><span data-stu-id="f6d27-140">It must contain no XML elements, \<\>.</span></span>
- <span data-ttu-id="f6d27-141">Ele deve conter duas barras,//.</span><span class="sxs-lookup"><span data-stu-id="f6d27-141">It must contain no double slashes, //.</span></span>
- <span data-ttu-id="f6d27-142">Ele deve conter nenhum caractere de escape HTML inválidos.</span><span class="sxs-lookup"><span data-stu-id="f6d27-142">It must contain no invalid HTML escape characters.</span></span>
<span data-ttu-id="f6d27-143">Por exemplo,% XY.</span><span class="sxs-lookup"><span data-stu-id="f6d27-143">For example, %XY.</span></span>

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

### <span data-ttu-id="f6d27-144">-Nome</span><span class="sxs-lookup"><span data-stu-id="f6d27-144">-Name</span></span>
<span data-ttu-id="f6d27-145">Especifica o nome do perfil do Gerenciador de tráfego a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="f6d27-145">Specifies the name of the Traffic Manager profile to update.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6d27-146">-Perfil</span><span class="sxs-lookup"><span data-stu-id="f6d27-146">-Profile</span></span>
<span data-ttu-id="f6d27-147">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="f6d27-147">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="f6d27-148">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="f6d27-148">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f6d27-149">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f6d27-149">-TrafficManagerProfile</span></span>
<span data-ttu-id="f6d27-150">Especifica o objeto de perfil do Gerenciador de tráfego que você usa para definir o perfil.</span><span class="sxs-lookup"><span data-stu-id="f6d27-150">Specifies the Traffic Manager profile object you use to set the profile.</span></span>

```yaml
Type: IProfileWithDefinition
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f6d27-151">-TTL</span><span class="sxs-lookup"><span data-stu-id="f6d27-151">-Ttl</span></span>
<span data-ttu-id="f6d27-152">Especifica o tempo de vida útil (TTL) do DNS que informa os resolvedores DNS locais por quanto tempo armazenar em cache as entradas DNS.</span><span class="sxs-lookup"><span data-stu-id="f6d27-152">Specifies the DNS Time-to-Live (TTL) that informs the Local DNS resolvers how long to cache DNS entries.</span></span>
<span data-ttu-id="f6d27-153">Os valores válidos são um número inteiro de 30 a 999.999.</span><span class="sxs-lookup"><span data-stu-id="f6d27-153">Valid values are an integer from 30 through 999,999.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6d27-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6d27-154">CommonParameters</span></span>
<span data-ttu-id="f6d27-155">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6d27-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6d27-156">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6d27-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6d27-157">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f6d27-157">INPUTS</span></span>

## <span data-ttu-id="f6d27-158">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f6d27-158">OUTPUTS</span></span>

### <span data-ttu-id="f6d27-159">Microsoft. WindowsAzure. Commands. Utilities. Trafficmanager. Models. IProfileWithDefinition</span><span class="sxs-lookup"><span data-stu-id="f6d27-159">Microsoft.WindowsAzure.Commands.Utilities.TrafficManager.Models.IProfileWithDefinition</span></span>
<span data-ttu-id="f6d27-160">Esse cmdlet gera um objeto de perfil do Gerenciador de tráfego.</span><span class="sxs-lookup"><span data-stu-id="f6d27-160">This cmdlet generates a Traffic Manager profile object.</span></span>

## <span data-ttu-id="f6d27-161">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f6d27-161">NOTES</span></span>

## <span data-ttu-id="f6d27-162">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f6d27-162">RELATED LINKS</span></span>

[<span data-ttu-id="f6d27-163">Disable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f6d27-163">Disable-AzureTrafficManagerProfile</span></span>](./Disable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="f6d27-164">Enable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f6d27-164">Enable-AzureTrafficManagerProfile</span></span>](./Enable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="f6d27-165">Get-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f6d27-165">Get-AzureTrafficManagerProfile</span></span>](./Get-AzureTrafficManagerProfile.md)

[<span data-ttu-id="f6d27-166">New-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f6d27-166">New-AzureTrafficManagerProfile</span></span>](./New-AzureTrafficManagerProfile.md)

[<span data-ttu-id="f6d27-167">Remove-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f6d27-167">Remove-AzureTrafficManagerProfile</span></span>](./Remove-AzureTrafficManagerProfile.md)


