---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DDB38A77-E5C0-47DD-BADD-94488F661CD5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterface.md
ms.openlocfilehash: 9273c4cf6d23825b931dda696e1a2ef8513aa68d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771439"
---
# <span data-ttu-id="7ac97-101">Set-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="7ac97-101">Set-AzNetworkInterface</span></span>

## <span data-ttu-id="7ac97-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7ac97-102">SYNOPSIS</span></span>
<span data-ttu-id="7ac97-103">Atualiza uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="7ac97-103">Updates a network interface.</span></span>

## <span data-ttu-id="7ac97-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7ac97-104">SYNTAX</span></span>

```
Set-AzNetworkInterface -NetworkInterface <PSNetworkInterface> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7ac97-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7ac97-105">DESCRIPTION</span></span>
<span data-ttu-id="7ac97-106">O **set-AzNetworkInterface** atualiza uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="7ac97-106">The **Set-AzNetworkInterface** updates a network interface.</span></span>

## <span data-ttu-id="7ac97-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7ac97-107">EXAMPLES</span></span>

### <span data-ttu-id="7ac97-108">Exemplo 1: configurar uma interface de rede</span><span class="sxs-lookup"><span data-stu-id="7ac97-108">Example 1: Configure a network interface</span></span>
```
$Nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$Nic.IpConfigurations[0].PrivateIpAddress = "10.0.1.20"
$Nic.IpConfigurations[0].PrivateIpAllocationMethod = "Static"
$Nic.Tag = @{Name = "Name"; Value = "Value"}
Set-AzNetworkInterface -NetworkInterface $Nic
```

<span data-ttu-id="7ac97-109">Este exemplo configura uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="7ac97-109">This example configures a network interface.</span></span>
<span data-ttu-id="7ac97-110">O primeiro comando obtém uma interface de rede chamada NetworkInterface1 na ResourceGroup1 do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7ac97-110">The first command gets a network interface named NetworkInterface1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="7ac97-111">O segundo comando define o endereço IP privado da configuração de IP.</span><span class="sxs-lookup"><span data-stu-id="7ac97-111">The second command sets the private IP address of the IP configuration.</span></span>
<span data-ttu-id="7ac97-112">O terceiro comando define o método de alocação de IP particular como estático.</span><span class="sxs-lookup"><span data-stu-id="7ac97-112">The third command sets the private IP allocation method to Static.</span></span>
<span data-ttu-id="7ac97-113">O quarto comando define uma marca na interface de rede.</span><span class="sxs-lookup"><span data-stu-id="7ac97-113">The fourth command sets a tag on the network interface.</span></span>
<span data-ttu-id="7ac97-114">O quinto comando usa as informações armazenadas na variável $Nic para definir a interface de rede.</span><span class="sxs-lookup"><span data-stu-id="7ac97-114">The fifth command uses the information stored in the $Nic variable to set the network interface.</span></span>

### <span data-ttu-id="7ac97-115">Exemplo 2: alterar as configurações de DNS em uma interface de rede</span><span class="sxs-lookup"><span data-stu-id="7ac97-115">Example 2: Change DNS settings on a network interface</span></span>
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nic.DnsSettings.DnsServers.Add("192.168.1.100")
$nic | Set-AzNetworkInterface
```

<span data-ttu-id="7ac97-116">O primeiro comando obtém uma interface de rede chamada NetworkInterface1 que existe dentro do grupo de ResourceGroup1 de recursos.</span><span class="sxs-lookup"><span data-stu-id="7ac97-116">The first command gets a network interface named NetworkInterface1 that exists within resource group ResourceGroup1.</span></span> <span data-ttu-id="7ac97-117">O segundo comando adiciona o servidor DNS 192.168.1.100 a essa interface.</span><span class="sxs-lookup"><span data-stu-id="7ac97-117">The second command adds DNS server 192.168.1.100 to this interface.</span></span> <span data-ttu-id="7ac97-118">O terceiro comando aplica essas alterações à interface de rede.</span><span class="sxs-lookup"><span data-stu-id="7ac97-118">The third command applies these changes to the network interface.</span></span> <span data-ttu-id="7ac97-119">Para remover um servidor DNS, siga os comandos listados acima, mas substitua ". Adicionar "com". Remover "no segundo comando.</span><span class="sxs-lookup"><span data-stu-id="7ac97-119">To remove a DNS server, follow the commands listed above, but replace ".Add" with ".Remove" in the second command.</span></span>

### <span data-ttu-id="7ac97-120">Exemplo 3: habilitar o encaminhamento de IP em uma interface de rede</span><span class="sxs-lookup"><span data-stu-id="7ac97-120">Example 3: Enable IP forwarding on a network interface</span></span>
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nic.EnableIPForwarding = 1
$nic | Set-AzNetworkInterface
```

<span data-ttu-id="7ac97-121">O primeiro comando obtém uma interface de rede existente chamada NetworkInterface1 e a armazena na variável $nic.</span><span class="sxs-lookup"><span data-stu-id="7ac97-121">The first command gets an existing network interface called NetworkInterface1 and stores it in the $nic variable.</span></span> <span data-ttu-id="7ac97-122">O segundo comando altera o valor de encaminhamento de IP para true.</span><span class="sxs-lookup"><span data-stu-id="7ac97-122">The second command changes the IP forwarding value to true.</span></span> <span data-ttu-id="7ac97-123">Por fim, o terceiro comando aplica as alterações à interface de rede.</span><span class="sxs-lookup"><span data-stu-id="7ac97-123">Finally, the third command applies the changes to the network interface.</span></span> <span data-ttu-id="7ac97-124">Para desativar o encaminhamento de IP em uma interface de rede, siga o exemplo de exemplo, mas certifique-se de alterar o segundo comando para "$nic. EnableIPForwarding = 0 ".</span><span class="sxs-lookup"><span data-stu-id="7ac97-124">To disable IP forwarding on a network interface, follow the sample example, but be sure to change the second command to "$nic.EnableIPForwarding = 0".</span></span>

### <span data-ttu-id="7ac97-125">Exemplo 4: alterar a sub-rede de uma interface de rede</span><span class="sxs-lookup"><span data-stu-id="7ac97-125">Example 4: Change the subnet of a network interface</span></span>
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$vnet = Get-AzVirtualNetwork -Name VNet1 -ResourceGroupName crosssubcrossversionpeering
$subnet2 = Get-AzVirtualNetworkSubnetConfig -Name Subnet2 -VirtualNetwork $vnet
$nic.IpConfigurations[0].Subnet.Id = $subnet2.Id
$nic | Set-AzNetworkInterface
```

<span data-ttu-id="7ac97-126">O primeiro comando obtém a interface de rede NetworkInterface1 e a armazena na variável $nic.</span><span class="sxs-lookup"><span data-stu-id="7ac97-126">The first command gets the network interface NetworkInterface1 and stores it in the $nic variable.</span></span> <span data-ttu-id="7ac97-127">O segundo comando obtém a rede virtual associada à sub-rede à qual a interface de rede vai ser associada.</span><span class="sxs-lookup"><span data-stu-id="7ac97-127">The second command gets the virtual network associated with the subnet that the network interface is going to be associated with.</span></span> <span data-ttu-id="7ac97-128">O segundo comando obtém a sub-rede e a armazena na variável $subnet 2.</span><span class="sxs-lookup"><span data-stu-id="7ac97-128">The second command gets the subnet and stores it in the $subnet2 variable.</span></span> <span data-ttu-id="7ac97-129">O terceiro comando associado ao endereço IP privado primário da interface de rede com a nova sub-rede.</span><span class="sxs-lookup"><span data-stu-id="7ac97-129">The third command associated the primary private IP address of the network interface with the new subnet.</span></span> <span data-ttu-id="7ac97-130">Por fim, o último comando aplicou essas alterações na interface de rede.</span><span class="sxs-lookup"><span data-stu-id="7ac97-130">Finally the last command applied these changes on the network interface.</span></span>
>[!NOTE] 
><span data-ttu-id="7ac97-131">As configurações de IP devem ser dinâmicas para que você possa alterar a sub-rede.</span><span class="sxs-lookup"><span data-stu-id="7ac97-131">The IP configurations must be dynamic before you can change the subnet.</span></span> <span data-ttu-id="7ac97-132">Se você tiver configurações de IP estático, altere para dinâmico antes de prosseguir.</span><span class="sxs-lookup"><span data-stu-id="7ac97-132">If you have static IP configurations, change then to dynamic before proceeding.</span></span> 
>[!NOTE]
><span data-ttu-id="7ac97-133">Se a interface de rede tiver várias configurações de IP, o comando para trás deve ser feito para todas essas configurações de IP antes do comando Set-AzNetworkInterface final ser executado.</span><span class="sxs-lookup"><span data-stu-id="7ac97-133">If the network interface has multiple IP configurations, the forth command must be done for all these IP configurations before the final Set-AzNetworkInterface command is executed.</span></span> <span data-ttu-id="7ac97-134">Isso pode ser feito no comando em diante, mas substituindo "0" pelo número apropriado.</span><span class="sxs-lookup"><span data-stu-id="7ac97-134">This can be done as in the forth command but by replacing "0" with the appropriate number.</span></span> <span data-ttu-id="7ac97-135">Se uma interface de rede tem N configurações de IP, N-1 desses comandos devem existir.</span><span class="sxs-lookup"><span data-stu-id="7ac97-135">If a network interface has N IP configurations, then N-1 of these commands must exist.</span></span>

### <span data-ttu-id="7ac97-136">Exemplo 5: associar/dissociar um grupo de segurança de rede a uma interface de rede</span><span class="sxs-lookup"><span data-stu-id="7ac97-136">Example 5: Associate/Dissociate a Network Security Group to a network interface</span></span>
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nsg = Get-AzNetworkSecurityGroup -ResourceGroupName "ResourceGroup1" -Name "MyNSG"
$nic.NetworkSecurityGroup = $nsg
$nic | Set-AzNetworkInterface
```

<span data-ttu-id="7ac97-137">O primeiro comando obtém uma interface de rede existente chamada NetworkInterface1 e a armazena na variável $nic.</span><span class="sxs-lookup"><span data-stu-id="7ac97-137">The first command gets an existing network interface called NetworkInterface1 and stores it in the $nic variable.</span></span> <span data-ttu-id="7ac97-138">O segundo comando obtém um grupo de segurança de rede existente chamado MyNSG e o armazena na variável $nsg.</span><span class="sxs-lookup"><span data-stu-id="7ac97-138">The second command gets an existing network security group called MyNSG and stores it in the $nsg variable.</span></span> <span data-ttu-id="7ac97-139">O terceiro comando atribui $nsg à $nic.</span><span class="sxs-lookup"><span data-stu-id="7ac97-139">The third command assigns the $nsg to the $nic.</span></span> <span data-ttu-id="7ac97-140">Por fim, o comando avançar aplica as alterações à interface de rede.</span><span class="sxs-lookup"><span data-stu-id="7ac97-140">Finally, the forth command applies the changes to the Network interface.</span></span> <span data-ttu-id="7ac97-141">Para dissociar grupos de segurança de rede de uma interface de rede, $nsg simples substituir no terceiro comando por $null.</span><span class="sxs-lookup"><span data-stu-id="7ac97-141">To dissociate network security groups from a network interface, simple replace $nsg in the third command with $null.</span></span>

## <span data-ttu-id="7ac97-142">OS</span><span class="sxs-lookup"><span data-stu-id="7ac97-142">PARAMETERS</span></span>

### <span data-ttu-id="7ac97-143">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7ac97-143">-AsJob</span></span>
<span data-ttu-id="7ac97-144">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="7ac97-144">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ac97-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ac97-145">-DefaultProfile</span></span>
<span data-ttu-id="7ac97-146">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7ac97-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7ac97-147">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="7ac97-147">-NetworkInterface</span></span>
<span data-ttu-id="7ac97-148">Especifica um objeto de interface de rede que representa o estado para o qual a interface de rede deve ser definida.</span><span class="sxs-lookup"><span data-stu-id="7ac97-148">Specifies a network interface object representing the state to which the network interface should be set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterface
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7ac97-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ac97-149">CommonParameters</span></span>
<span data-ttu-id="7ac97-150">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ac97-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ac97-151">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ac97-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ac97-152">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7ac97-152">INPUTS</span></span>

### <span data-ttu-id="7ac97-153">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="7ac97-153">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="7ac97-154">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7ac97-154">OUTPUTS</span></span>

### <span data-ttu-id="7ac97-155">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="7ac97-155">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="7ac97-156">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7ac97-156">NOTES</span></span>

## <span data-ttu-id="7ac97-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7ac97-157">RELATED LINKS</span></span>

[<span data-ttu-id="7ac97-158">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="7ac97-158">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="7ac97-159">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="7ac97-159">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="7ac97-160">New-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="7ac97-160">New-AzNetworkInterface</span></span>](./New-AzNetworkInterface.md)

[<span data-ttu-id="7ac97-161">Remove-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="7ac97-161">Remove-AzNetworkInterface</span></span>](./Remove-AzNetworkInterface.md)
