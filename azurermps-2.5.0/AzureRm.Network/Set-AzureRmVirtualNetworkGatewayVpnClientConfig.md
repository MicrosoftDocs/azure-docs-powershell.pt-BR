---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: EFB0D7A6-0C8A-4514-873D-672641CCCAF3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworkgatewayvpnclientconfig
schema: 2.0.0
ms.openlocfilehash: 471ad0ba4126026960879e5babbb592f352d3bcc
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786066"
---
# <span data-ttu-id="3fb7c-101">Set-AzureRmVirtualNetworkGatewayVpnClientConfig</span><span class="sxs-lookup"><span data-stu-id="3fb7c-101">Set-AzureRmVirtualNetworkGatewayVpnClientConfig</span></span>

## <span data-ttu-id="3fb7c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3fb7c-102">SYNOPSIS</span></span>
<span data-ttu-id="3fb7c-103">Define o pool de endereços do cliente VPN para um gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="3fb7c-103">Sets the VPN client address pool for a virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3fb7c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3fb7c-104">SYNTAX</span></span>

### <span data-ttu-id="3fb7c-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="3fb7c-105">Default (Default)</span></span>
```
Set-AzureRmVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3fb7c-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="3fb7c-106">RadiusServerConfiguration</span></span>
```
Set-AzureRmVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -VpnClientAddressPool <System.Collections.Generic.List`1[System.String]> -RadiusServerAddress <String>
 -RadiusServerSecret <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3fb7c-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3fb7c-107">DESCRIPTION</span></span>
<span data-ttu-id="3fb7c-108">O cmdlet **set-AzureRmVirtualNetworkVpnClientConfig** configura o pool de endereços do cliente para um gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="3fb7c-108">The **Set-AzureRmVirtualNetworkVpnClientConfig** cmdlet configures the client address pool for a virtual network gateway.</span></span>
<span data-ttu-id="3fb7c-109">Os clientes de rede virtual privada (VPN) que se conectam a esse gateway recebem um endereço IP desse pool de endereços.</span><span class="sxs-lookup"><span data-stu-id="3fb7c-109">Virtual private network (VPN) clients that connect to this gateway will be assigned an IP address from this address pool.</span></span>

## <span data-ttu-id="3fb7c-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3fb7c-110">EXAMPLES</span></span>

### <span data-ttu-id="3fb7c-111">Exemplo 1: atribuir um pool de endereços de cliente VPN a um gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="3fb7c-111">Example 1: Assign a VPN client address pool to a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Set-AzureRmVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway $Gateway -VpnClientAddressPool "10.0.0.0/16"
```

<span data-ttu-id="3fb7c-112">Este exemplo atribui um pool de endereços de cliente VPN a um gateway de rede virtual chamado ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="3fb7c-112">This example assigns a VPN client address pool to a virtual network gateway named ContosoVirtualGateway.</span></span>

<span data-ttu-id="3fb7c-113">O primeiro comando cria uma referência de objeto para o gateway e o objeto é armazenado em uma variável chamada $Gateway.</span><span class="sxs-lookup"><span data-stu-id="3fb7c-113">The first command creates an object reference to the gateway and the object is stored in a variable named $Gateway.</span></span>

<span data-ttu-id="3fb7c-114">O segundo comando no exemplo usa o cmdlet **set-AzureRmVirtualNetworkGatewayVpnClientConfig** para atribuir o pool de endereços 10.0.0.0/16 ao ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="3fb7c-114">The second command in the example then uses the **Set-AzureRmVirtualNetworkGatewayVpnClientConfig** cmdlet to assign the address pool 10.0.0.0/16 to ContosoVirtualGateway.</span></span>

### <span data-ttu-id="3fb7c-115">Exemplo 2: configurar a autenticação baseada em RADIUS externa no gateway existente</span><span class="sxs-lookup"><span data-stu-id="3fb7c-115">Example 2: Configure external radius based authentication on existing gateway</span></span>
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> $Secure_String_Pwd = ConvertTo-SecureString "TestRadiusServerPassword" -AsPlainText -Force
PS C:\> Set-AzureRmVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway $Gateway -VpnClientAddressPool "10.0.0.0/16" -RadiusServerAddress "TestRadiusServer" -RadiusServerSecret $Secure_String_Pwd
```

<span data-ttu-id="3fb7c-116">Este exemplo atribui um pool de endereços de cliente VPN a um gateway de rede virtual chamado ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="3fb7c-116">This example assigns a VPN client address pool to a virtual network gateway named ContosoVirtualGateway.</span></span>

<span data-ttu-id="3fb7c-117">O primeiro comando cria uma referência de objeto para o gateway e o objeto é armazenado em uma variável chamada $Gateway.</span><span class="sxs-lookup"><span data-stu-id="3fb7c-117">The first command creates an object reference to the gateway and the object is stored in a variable named $Gateway.</span></span>

<span data-ttu-id="3fb7c-118">O segundo comando no exemplo usa o cmdlet **set-AzureRmVirtualNetworkGatewayVpnClientConfig** para atribuir o pool de endereços 10.0.0.0/16 ao ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="3fb7c-118">The second command in the example then uses the **Set-AzureRmVirtualNetworkGatewayVpnClientConfig** cmdlet to assign the address pool 10.0.0.0/16 to ContosoVirtualGateway.</span></span> <span data-ttu-id="3fb7c-119">Ele também configura o servidor RADIUS externo "TestRadiusServer" para ser usado para autenticação para clientes VPN.</span><span class="sxs-lookup"><span data-stu-id="3fb7c-119">It also configures the external radius server "TestRadiusServer" to be used for authentication for vpn clients.</span></span>

## <span data-ttu-id="3fb7c-120">OS</span><span class="sxs-lookup"><span data-stu-id="3fb7c-120">PARAMETERS</span></span>

### <span data-ttu-id="3fb7c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fb7c-121">-DefaultProfile</span></span>
<span data-ttu-id="3fb7c-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3fb7c-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3fb7c-123">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="3fb7c-123">-RadiusServerAddress</span></span>
<span data-ttu-id="3fb7c-124">P2S endereço do servidor RADIUS externo.</span><span class="sxs-lookup"><span data-stu-id="3fb7c-124">P2S External Radius server address.</span></span>

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

### <span data-ttu-id="3fb7c-125">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="3fb7c-125">-RadiusServerSecret</span></span>
<span data-ttu-id="3fb7c-126">P2S segredo do servidor RADIUS externo.</span><span class="sxs-lookup"><span data-stu-id="3fb7c-126">P2S External Radius server secret.</span></span>

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

### <span data-ttu-id="3fb7c-127">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3fb7c-127">-VirtualNetworkGateway</span></span>
<span data-ttu-id="3fb7c-128">Especifica uma referência de objeto ao gateway de rede virtual que contém as definições de configuração de cliente VPN que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="3fb7c-128">Specifies an object reference to the virtual network gateway that contains the VPN client configuration settings that this cmdlet modifies.</span></span>
<span data-ttu-id="3fb7c-129">Você pode criar uma referência de objeto para um gateway de rede virtual usando o Get-AzureRmVirtualNetworkGateway e especificando o nome do gateway.</span><span class="sxs-lookup"><span data-stu-id="3fb7c-129">You can create an object reference to a virtual network gateway by using the Get-AzureRmVirtualNetworkGateway and specifying the name of the gateway.</span></span>

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

### <span data-ttu-id="3fb7c-130">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="3fb7c-130">-VpnClientAddressPool</span></span>
<span data-ttu-id="3fb7c-131">Especifica os endereços IP a serem atribuídos a clientes que se conectam a este gateway</span><span class="sxs-lookup"><span data-stu-id="3fb7c-131">Specifies the IP addresses to be assigned to clients connecting to this gateway</span></span>

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

### <span data-ttu-id="3fb7c-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3fb7c-132">-Confirm</span></span>
<span data-ttu-id="3fb7c-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3fb7c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3fb7c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3fb7c-134">-WhatIf</span></span>
<span data-ttu-id="3fb7c-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3fb7c-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3fb7c-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3fb7c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3fb7c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fb7c-137">CommonParameters</span></span>
<span data-ttu-id="3fb7c-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3fb7c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fb7c-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3fb7c-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fb7c-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3fb7c-140">INPUTS</span></span>

###  
<span data-ttu-id="3fb7c-141">Esse cmdlet aceita instâncias em pipeline do objeto **Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="3fb7c-141">This cmdlet accepts pipelined instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="3fb7c-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3fb7c-142">OUTPUTS</span></span>

###  
<span data-ttu-id="3fb7c-143">Esse cmdlet modifica instâncias existentes do objeto **Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="3fb7c-143">This cmdlet modifies existing instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="3fb7c-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3fb7c-144">NOTES</span></span>

## <span data-ttu-id="3fb7c-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3fb7c-145">RELATED LINKS</span></span>

[<span data-ttu-id="3fb7c-146">Get-AzureRmVpnClientPackage</span><span class="sxs-lookup"><span data-stu-id="3fb7c-146">Get-AzureRmVpnClientPackage</span></span>](./Get-AzureRmVpnClientPackage.md)

[<span data-ttu-id="3fb7c-147">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3fb7c-147">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="3fb7c-148">Redimensionar-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3fb7c-148">Resize-AzureRmVirtualNetworkGateway</span></span>](./Resize-AzureRmVirtualNetworkGateway.md)


