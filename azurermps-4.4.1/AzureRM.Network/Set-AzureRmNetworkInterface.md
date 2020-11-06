---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: DDB38A77-E5C0-47DD-BADD-94488F661CD5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkInterface.md
ms.openlocfilehash: 8403a2e26bbc149db35c9c20cdea3075adb88492
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429231"
---
# <span data-ttu-id="de343-101">Set-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="de343-101">Set-AzureRmNetworkInterface</span></span>

## <span data-ttu-id="de343-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="de343-102">SYNOPSIS</span></span>
<span data-ttu-id="de343-103">Define o estado da meta para uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="de343-103">Sets the goal state for a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="de343-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="de343-104">SYNTAX</span></span>

```
Set-AzureRmNetworkInterface -NetworkInterface <PSNetworkInterface> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="de343-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="de343-105">DESCRIPTION</span></span>
<span data-ttu-id="de343-106">O **set-AzureRmNetworkInterface** define o estado da meta para uma interface de rede do Azure.</span><span class="sxs-lookup"><span data-stu-id="de343-106">The **Set-AzureRmNetworkInterface** sets the goal state for an Azure network interface.</span></span>

## <span data-ttu-id="de343-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="de343-107">EXAMPLES</span></span>

### <span data-ttu-id="de343-108">Exemplo 1: configurar uma interface de rede</span><span class="sxs-lookup"><span data-stu-id="de343-108">Example 1: Configure a network interface</span></span>
```
$Nic = Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$Nic.IpConfigurations[0].PrivateIpAddress = "10.0.1.20"
$Nic.IpConfigurations[0].PrivateIpAllocationMethod = "Static"
$Nic.Tag = @{Name = "Name"; Value = "Value"}
Set-AzureRmNetworkInterface -NetworkInterface $Nic
```

<span data-ttu-id="de343-109">Este exemplo configura uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="de343-109">This example configures a network interface.</span></span>
<span data-ttu-id="de343-110">O primeiro comando obtém uma interface de rede chamada NetworkInterface1 na ResourceGroup1 do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="de343-110">The first command gets a network interface named NetworkInterface1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="de343-111">O segundo comando define o endereço IP privado da configuração de IP.</span><span class="sxs-lookup"><span data-stu-id="de343-111">The second command sets the private IP address of the IP configuration.</span></span>
<span data-ttu-id="de343-112">O terceiro comando define o método de alocação de IP particular como estático.</span><span class="sxs-lookup"><span data-stu-id="de343-112">The third command sets the private IP allocation method to Static.</span></span>
<span data-ttu-id="de343-113">O quarto comando define uma marca na interface de rede.</span><span class="sxs-lookup"><span data-stu-id="de343-113">The fourth command sets a tag on the network interface.</span></span>
<span data-ttu-id="de343-114">O quinto comando usa as informações armazenadas na variável $Nic para definir a interface de rede.</span><span class="sxs-lookup"><span data-stu-id="de343-114">The fifth command uses the information stored in the $Nic variable to set the network interface.</span></span>

### <span data-ttu-id="de343-115">Exemplo 2: alterar as configurações de DNS em uma interface de rede</span><span class="sxs-lookup"><span data-stu-id="de343-115">Example 2: Change DNS settings on a network interface</span></span>
```
$nic = Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nic.DnsSettings.DnsServers.Add("192.168.1.100")
$nic | Set-AzureRmNetworkInterface
```

<span data-ttu-id="de343-116">O primeiro comando obtém uma interface de rede chamada NetworkInterface1 que existe dentro do grupo de ResourceGroup1 de recursos.</span><span class="sxs-lookup"><span data-stu-id="de343-116">The first command gets a network interface named NetworkInterface1 that exists within resource group ResourceGroup1.</span></span> <span data-ttu-id="de343-117">O segundo comando adiciona o servidor DNS 192.168.1.100 a essa interface.</span><span class="sxs-lookup"><span data-stu-id="de343-117">The second command adds DNS server 192.168.1.100 to this interface.</span></span> <span data-ttu-id="de343-118">O terceiro comando aplica essas alterações à interface de rede.</span><span class="sxs-lookup"><span data-stu-id="de343-118">The third command applies these changes to the network interface.</span></span> <span data-ttu-id="de343-119">Para remover um servidor DNS, siga os comandos listados acima, mas substitua ". Adicionar "com". Remover "no segundo comando.</span><span class="sxs-lookup"><span data-stu-id="de343-119">To remove a DNS server, follow the commands listed above, but replace ".Add" with ".Remove" in the second command.</span></span>

### <span data-ttu-id="de343-120">Exemplo 3: ativar o IP forwading em uma interface de rede</span><span class="sxs-lookup"><span data-stu-id="de343-120">Example 3: Enable IP forwading on a network interface</span></span>
```
$nic = Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nic.EnableIPForwarding = 1
$nic | Set-AzureRmNetworkInterface
```

<span data-ttu-id="de343-121">O primeiro comando obtém uma interface de rede existente chamada NetworkInterface1 e a armazena na variável $nic.</span><span class="sxs-lookup"><span data-stu-id="de343-121">The first command gets an existing network interface called NetworkInterface1 and stores it in the $nic variable.</span></span> <span data-ttu-id="de343-122">O segundo comando altera o valor de encaminhamento de IP para true.</span><span class="sxs-lookup"><span data-stu-id="de343-122">The second command changes the IP forwarding value to true.</span></span> <span data-ttu-id="de343-123">Por fim, o terceiro comando aplica as alterações à interface de rede.</span><span class="sxs-lookup"><span data-stu-id="de343-123">Finally, the third command applies the changes to the network interface.</span></span> <span data-ttu-id="de343-124">Para desativar o encaminhamento de IP em uma interface de rede, siga o exemplo de exemplo, mas certifique-se de alterar o segundo comando para "$nic. EnableIPForwarding = 0 ".</span><span class="sxs-lookup"><span data-stu-id="de343-124">To disable IP forwarding on a network interface, follow the sample example, but be sure to change the second command to "$nic.EnableIPForwarding = 0".</span></span>

### <span data-ttu-id="de343-125">Exemplo 4: alterar a sub-rede de uma interface de rede</span><span class="sxs-lookup"><span data-stu-id="de343-125">Example 4: Change the subnet of a network interface</span></span>
```
$nic = Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$vnet = Get-AzureRmVirtualNetwork -Name VNet1 -ResourceGroupName crosssubcrossversionpeering
$subnet2 = Get-AzureRmVirtualNetworkSubnetConfig -Name Subnet2 -VirtualNetwork $vnet
$nic.IpConfigurations[0].Subnet.Id = $subnet2.Id
$nic | Set-AzureRmNetworkInterface
```

<span data-ttu-id="de343-126">O primeiro comando obtém a interface de rede NetworkInterface1 e a armazena na variável $nic.</span><span class="sxs-lookup"><span data-stu-id="de343-126">The first command gets the network interface NetworkInterface1 and stores it in the $nic variable.</span></span> <span data-ttu-id="de343-127">O segundo comando obtém a rede virtual associada à sub-rede à qual a interface de rede vai ser associada.</span><span class="sxs-lookup"><span data-stu-id="de343-127">The second command gets the virtual network associated with the subnet that the network interface is going to be associated with.</span></span> <span data-ttu-id="de343-128">O segundo comando obtém a sub-rede e a armazena na variável $subnet 2.</span><span class="sxs-lookup"><span data-stu-id="de343-128">The second command gets the subnet and stores it in the $subnet2 variable.</span></span> <span data-ttu-id="de343-129">O terceiro comando associado ao endereço IP privado primário da interface de rede com a nova sub-rede.</span><span class="sxs-lookup"><span data-stu-id="de343-129">The third command associated the primary private IP address of the network interface with the new subnet.</span></span> <span data-ttu-id="de343-130">Por fim, o último comando aplicou essas alterações na interface de rede.</span><span class="sxs-lookup"><span data-stu-id="de343-130">Finally the last command applied these changes on the network interface.</span></span>

>[!NOTE] 
><span data-ttu-id="de343-131">As configurações de IP devem ser dinâmicas para que você possa alterar a sub-rede.</span><span class="sxs-lookup"><span data-stu-id="de343-131">The IP configurations must be dynamic before you can change the subnet.</span></span> <span data-ttu-id="de343-132">Se você tiver configurações de IP estático, altere para dinâmico antes de prosseguir.</span><span class="sxs-lookup"><span data-stu-id="de343-132">If you have static IP configurations, change then to dynamic before proceeding.</span></span> 

>[!NOTE]
><span data-ttu-id="de343-133">Se a interface de rede tiver várias configurações de IP, o comando para trás deve ser feito para todas essas configurações de IP antes do comando Set-AzureRmNetworkInterface final ser executado.</span><span class="sxs-lookup"><span data-stu-id="de343-133">If the network interface has multiple IP configurations, the forth command must be done for all these IP configurations before the final Set-AzureRmNetworkInterface command is executed.</span></span> <span data-ttu-id="de343-134">Isso pode ser feito no comando em diante, mas substituindo "0" pelo número apropriado.</span><span class="sxs-lookup"><span data-stu-id="de343-134">This can be done as in the forth command but by replacing "0" with the appropriate number.</span></span> <span data-ttu-id="de343-135">Se uma interface de rede tem N configurações de IP, N-1 desses comandos devem existir.</span><span class="sxs-lookup"><span data-stu-id="de343-135">If a network interface has N IP configurations, then N-1 of these commands must exist.</span></span>

### <span data-ttu-id="de343-136">Exemplo 5: associar/dissociar um grupo de segurança de rede a uma interface de rede</span><span class="sxs-lookup"><span data-stu-id="de343-136">Example 5: Associate/Dissociate a Network Security Group to a network interface</span></span>
```
$nic = Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nsg = Get-AzureRmNetworkSecurityGroup -ResourceGroupName "ResourceGroup1" -Name "MyNSG"
$nic.NetworkSecurityGroup = $nsg
$nic | Set-AzureRmNetworkInterface
```

<span data-ttu-id="de343-137">O primeiro comando obtém uma interface de rede existente chamada NetworkInterface1 e a armazena na variável $nic.</span><span class="sxs-lookup"><span data-stu-id="de343-137">The first command gets an existing network interface called NetworkInterface1 and stores it in the $nic variable.</span></span> <span data-ttu-id="de343-138">O segundo comando obtém um grupo de segurança de rede existente chamado MyNSG e o armazena na variável $nsg.</span><span class="sxs-lookup"><span data-stu-id="de343-138">The second command gets an existing network security group called MyNSG and stores it in the $nsg variable.</span></span> <span data-ttu-id="de343-139">O comando avançar atribui a $nsg à $nic.</span><span class="sxs-lookup"><span data-stu-id="de343-139">The forth command assigns the $nsg to the $nic.</span></span> <span data-ttu-id="de343-140">Por fim, o quinto comando aplica as alterações à interface de rede.</span><span class="sxs-lookup"><span data-stu-id="de343-140">Finally, the fifth command applies the changes to the Network interface.</span></span> <span data-ttu-id="de343-141">Para dissociar grupos de segurança de rede de uma interface de rede, $nsg de substituição simples no comando por diante com $null.</span><span class="sxs-lookup"><span data-stu-id="de343-141">To dissociate network security groups from a network interface, simple replace $nsg in the forth command with $null.</span></span>

## <span data-ttu-id="de343-142">OS</span><span class="sxs-lookup"><span data-stu-id="de343-142">PARAMETERS</span></span>

### <span data-ttu-id="de343-143">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="de343-143">-NetworkInterface</span></span>
<span data-ttu-id="de343-144">Especifica um objeto **NetworkInterface** que representa o estado da meta para uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="de343-144">Specifies a **NetworkInterface** object that represents the goal state for a network interface.</span></span>

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

### <span data-ttu-id="de343-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de343-145">-DefaultProfile</span></span>
<span data-ttu-id="de343-146">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="de343-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="de343-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de343-147">CommonParameters</span></span>
<span data-ttu-id="de343-148">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de343-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de343-149">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de343-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de343-150">SENSORES</span><span class="sxs-lookup"><span data-stu-id="de343-150">INPUTS</span></span>

### <span data-ttu-id="de343-151">PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="de343-151">PSNetworkInterface</span></span>
<span data-ttu-id="de343-152">O parâmetro ' NetworkInterface ' aceita o valor do tipo ' PSNetworkInterface ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="de343-152">Parameter 'NetworkInterface' accepts value of type 'PSNetworkInterface' from the pipeline</span></span>

## <span data-ttu-id="de343-153">EXIBE</span><span class="sxs-lookup"><span data-stu-id="de343-153">OUTPUTS</span></span>

### <span data-ttu-id="de343-154">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="de343-154">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="de343-155">INFORMA</span><span class="sxs-lookup"><span data-stu-id="de343-155">NOTES</span></span>

## <span data-ttu-id="de343-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="de343-156">RELATED LINKS</span></span>

[<span data-ttu-id="de343-157">Get-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="de343-157">Get-AzureRmNetworkInterface</span></span>](./Get-AzureRmNetworkInterface.md)

[<span data-ttu-id="de343-158">Get-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="de343-158">Get-AzureRmNetworkInterface</span></span>](./Get-AzureRmNetworkInterface.md)

[<span data-ttu-id="de343-159">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="de343-159">New-AzureRmNetworkInterface</span></span>](./New-AzureRmNetworkInterface.md)

[<span data-ttu-id="de343-160">Remove-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="de343-160">Remove-AzureRmNetworkInterface</span></span>](./Remove-AzureRmNetworkInterface.md)
