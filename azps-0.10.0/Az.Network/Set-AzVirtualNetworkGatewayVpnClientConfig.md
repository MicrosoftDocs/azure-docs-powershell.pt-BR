---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EFB0D7A6-0C8A-4514-873D-672641CCCAF3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgatewayvpnclientconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetworkGatewayVpnClientConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetworkGatewayVpnClientConfig.md
ms.openlocfilehash: 1c85bc5e2a935378630728083b19544ace8670b4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776492"
---
# <span data-ttu-id="bdecf-101">Set-AzVirtualNetworkGatewayVpnClientConfig</span><span class="sxs-lookup"><span data-stu-id="bdecf-101">Set-AzVirtualNetworkGatewayVpnClientConfig</span></span>

## <span data-ttu-id="bdecf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bdecf-102">SYNOPSIS</span></span>
<span data-ttu-id="bdecf-103">Define o pool de endereços do cliente VPN para um gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="bdecf-103">Sets the VPN client address pool for a virtual network gateway.</span></span>

## <span data-ttu-id="bdecf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bdecf-104">SYNTAX</span></span>

### <span data-ttu-id="bdecf-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="bdecf-105">Default (Default)</span></span>
```
Set-AzVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bdecf-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="bdecf-106">RadiusServerConfiguration</span></span>
```
Set-AzVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -VpnClientAddressPool <System.Collections.Generic.List`1[System.String]> -RadiusServerAddress <String>
 -RadiusServerSecret <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bdecf-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bdecf-107">DESCRIPTION</span></span>
<span data-ttu-id="bdecf-108">O cmdlet **set-AzVirtualNetworkVpnClientConfig** configura o pool de endereços do cliente para um gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="bdecf-108">The **Set-AzVirtualNetworkVpnClientConfig** cmdlet configures the client address pool for a virtual network gateway.</span></span>
<span data-ttu-id="bdecf-109">Os clientes de rede virtual privada (VPN) que se conectam a esse gateway recebem um endereço IP desse pool de endereços.</span><span class="sxs-lookup"><span data-stu-id="bdecf-109">Virtual private network (VPN) clients that connect to this gateway will be assigned an IP address from this address pool.</span></span>

## <span data-ttu-id="bdecf-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bdecf-110">EXAMPLES</span></span>

### <span data-ttu-id="bdecf-111">Exemplo 1: atribuir um pool de endereços de cliente VPN a um gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="bdecf-111">Example 1: Assign a VPN client address pool to a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Set-AzVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway $Gateway -VpnClientAddressPool "10.0.0.0/16"
```

<span data-ttu-id="bdecf-112">Este exemplo atribui um pool de endereços de cliente VPN a um gateway de rede virtual chamado ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="bdecf-112">This example assigns a VPN client address pool to a virtual network gateway named ContosoVirtualGateway.</span></span>

<span data-ttu-id="bdecf-113">O primeiro comando cria uma referência de objeto para o gateway e o objeto é armazenado em uma variável chamada $Gateway.</span><span class="sxs-lookup"><span data-stu-id="bdecf-113">The first command creates an object reference to the gateway and the object is stored in a variable named $Gateway.</span></span>

<span data-ttu-id="bdecf-114">O segundo comando no exemplo usa o cmdlet **set-AzVirtualNetworkGatewayVpnClientConfig** para atribuir o pool de endereços 10.0.0.0/16 ao ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="bdecf-114">The second command in the example then uses the **Set-AzVirtualNetworkGatewayVpnClientConfig** cmdlet to assign the address pool 10.0.0.0/16 to ContosoVirtualGateway.</span></span>

### <span data-ttu-id="bdecf-115">Exemplo 2: configurar a autenticação baseada em RADIUS externa no gateway existente</span><span class="sxs-lookup"><span data-stu-id="bdecf-115">Example 2: Configure external radius based authentication on existing gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> $Secure_String_Pwd = ConvertTo-SecureString "TestRadiusServerPassword" -AsPlainText -Force
PS C:\> Set-AzVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway $Gateway -VpnClientAddressPool "10.0.0.0/16" -RadiusServerAddress "TestRadiusServer" -RadiusServerSecret $Secure_String_Pwd
```

<span data-ttu-id="bdecf-116">Este exemplo atribui um pool de endereços de cliente VPN a um gateway de rede virtual chamado ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="bdecf-116">This example assigns a VPN client address pool to a virtual network gateway named ContosoVirtualGateway.</span></span>

<span data-ttu-id="bdecf-117">O primeiro comando cria uma referência de objeto para o gateway e o objeto é armazenado em uma variável chamada $Gateway.</span><span class="sxs-lookup"><span data-stu-id="bdecf-117">The first command creates an object reference to the gateway and the object is stored in a variable named $Gateway.</span></span>

<span data-ttu-id="bdecf-118">O segundo comando no exemplo usa o cmdlet **set-AzVirtualNetworkGatewayVpnClientConfig** para atribuir o pool de endereços 10.0.0.0/16 ao ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="bdecf-118">The second command in the example then uses the **Set-AzVirtualNetworkGatewayVpnClientConfig** cmdlet to assign the address pool 10.0.0.0/16 to ContosoVirtualGateway.</span></span> <span data-ttu-id="bdecf-119">Ele também configura o servidor RADIUS externo "TestRadiusServer" para ser usado para autenticação para clientes VPN.</span><span class="sxs-lookup"><span data-stu-id="bdecf-119">It also configures the external radius server "TestRadiusServer" to be used for authentication for vpn clients.</span></span>

## <span data-ttu-id="bdecf-120">OS</span><span class="sxs-lookup"><span data-stu-id="bdecf-120">PARAMETERS</span></span>

### <span data-ttu-id="bdecf-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdecf-121">-DefaultProfile</span></span>
<span data-ttu-id="bdecf-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bdecf-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bdecf-123">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="bdecf-123">-RadiusServerAddress</span></span>
<span data-ttu-id="bdecf-124">P2S endereço do servidor RADIUS externo.</span><span class="sxs-lookup"><span data-stu-id="bdecf-124">P2S External Radius server address.</span></span>

```yaml
Type: String
Parameter Sets: RadiusServerConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bdecf-125">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="bdecf-125">-RadiusServerSecret</span></span>
<span data-ttu-id="bdecf-126">P2S segredo do servidor RADIUS externo.</span><span class="sxs-lookup"><span data-stu-id="bdecf-126">P2S External Radius server secret.</span></span>

```yaml
Type: SecureString
Parameter Sets: RadiusServerConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bdecf-127">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="bdecf-127">-VirtualNetworkGateway</span></span>
<span data-ttu-id="bdecf-128">Especifica uma referência de objeto ao gateway de rede virtual que contém as definições de configuração de cliente VPN que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="bdecf-128">Specifies an object reference to the virtual network gateway that contains the VPN client configuration settings that this cmdlet modifies.</span></span>
<span data-ttu-id="bdecf-129">Você pode criar uma referência de objeto para um gateway de rede virtual usando o Get-AzVirtualNetworkGateway e especificando o nome do gateway.</span><span class="sxs-lookup"><span data-stu-id="bdecf-129">You can create an object reference to a virtual network gateway by using the Get-AzVirtualNetworkGateway and specifying the name of the gateway.</span></span>

```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bdecf-130">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="bdecf-130">-VpnClientAddressPool</span></span>
<span data-ttu-id="bdecf-131">Especifica os endereços IP a serem atribuídos a clientes que se conectam a este gateway</span><span class="sxs-lookup"><span data-stu-id="bdecf-131">Specifies the IP addresses to be assigned to clients connecting to this gateway</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bdecf-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="bdecf-132">-Confirm</span></span>
<span data-ttu-id="bdecf-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bdecf-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdecf-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bdecf-134">-WhatIf</span></span>
<span data-ttu-id="bdecf-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bdecf-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bdecf-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bdecf-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdecf-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdecf-137">CommonParameters</span></span>
<span data-ttu-id="bdecf-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdecf-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdecf-139">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bdecf-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdecf-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bdecf-140">INPUTS</span></span>

###  
<span data-ttu-id="bdecf-141">Esse cmdlet aceita instâncias em pipeline do objeto **Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="bdecf-141">This cmdlet accepts pipelined instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="bdecf-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bdecf-142">OUTPUTS</span></span>

###  
<span data-ttu-id="bdecf-143">Esse cmdlet modifica instâncias existentes do objeto **Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="bdecf-143">This cmdlet modifies existing instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="bdecf-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bdecf-144">NOTES</span></span>

## <span data-ttu-id="bdecf-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bdecf-145">RELATED LINKS</span></span>

[<span data-ttu-id="bdecf-146">Get-AzVpnClientPackage</span><span class="sxs-lookup"><span data-stu-id="bdecf-146">Get-AzVpnClientPackage</span></span>](./Get-AzVpnClientPackage.md)

[<span data-ttu-id="bdecf-147">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="bdecf-147">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="bdecf-148">Redimensionar-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="bdecf-148">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)


