---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: EFB0D7A6-0C8A-4514-873D-672641CCCAF3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworkgatewayvpnclientconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayVpnClientConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayVpnClientConfig.md
ms.openlocfilehash: 6d2830836fd29edea2843fad4be1892edfa7fbb8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429412"
---
# <span data-ttu-id="8cb5a-101">Set-AzureRmVirtualNetworkGatewayVpnClientConfig</span><span class="sxs-lookup"><span data-stu-id="8cb5a-101">Set-AzureRmVirtualNetworkGatewayVpnClientConfig</span></span>

## <span data-ttu-id="8cb5a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8cb5a-102">SYNOPSIS</span></span>
<span data-ttu-id="8cb5a-103">Define o pool de endereços do cliente VPN para um gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="8cb5a-103">Sets the VPN client address pool for a virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8cb5a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8cb5a-104">SYNTAX</span></span>

### <span data-ttu-id="8cb5a-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="8cb5a-105">Default (Default)</span></span>
```
Set-AzureRmVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8cb5a-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="8cb5a-106">RadiusServerConfiguration</span></span>
```
Set-AzureRmVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -VpnClientAddressPool <System.Collections.Generic.List`1[System.String]> -RadiusServerAddress <String>
 -RadiusServerSecret <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8cb5a-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8cb5a-107">DESCRIPTION</span></span>
<span data-ttu-id="8cb5a-108">O cmdlet **set-AzureRmVirtualNetworkVpnClientConfig** configura o pool de endereços do cliente para um gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="8cb5a-108">The **Set-AzureRmVirtualNetworkVpnClientConfig** cmdlet configures the client address pool for a virtual network gateway.</span></span>
<span data-ttu-id="8cb5a-109">Os clientes de rede virtual privada (VPN) que se conectam a esse gateway recebem um endereço IP desse pool de endereços.</span><span class="sxs-lookup"><span data-stu-id="8cb5a-109">Virtual private network (VPN) clients that connect to this gateway will be assigned an IP address from this address pool.</span></span>

## <span data-ttu-id="8cb5a-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8cb5a-110">EXAMPLES</span></span>

### <span data-ttu-id="8cb5a-111">Exemplo 1: atribuir um pool de endereços de cliente VPN a um gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="8cb5a-111">Example 1: Assign a VPN client address pool to a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Set-AzureRmVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway $Gateway -VpnClientAddressPool "10.0.0.0/16"
```

<span data-ttu-id="8cb5a-112">Este exemplo atribui um pool de endereços de cliente VPN a um gateway de rede virtual chamado ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="8cb5a-112">This example assigns a VPN client address pool to a virtual network gateway named ContosoVirtualGateway.</span></span>
<span data-ttu-id="8cb5a-113">O primeiro comando cria uma referência de objeto para o gateway e o objeto é armazenado em uma variável chamada $Gateway.</span><span class="sxs-lookup"><span data-stu-id="8cb5a-113">The first command creates an object reference to the gateway and the object is stored in a variable named $Gateway.</span></span>
<span data-ttu-id="8cb5a-114">O segundo comando no exemplo usa o cmdlet **set-AzureRmVirtualNetworkGatewayVpnClientConfig** para atribuir o pool de endereços 10.0.0.0/16 ao ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="8cb5a-114">The second command in the example then uses the **Set-AzureRmVirtualNetworkGatewayVpnClientConfig** cmdlet to assign the address pool 10.0.0.0/16 to ContosoVirtualGateway.</span></span>

### <span data-ttu-id="8cb5a-115">Exemplo 2: configurar a autenticação baseada em RADIUS externa no gateway existente</span><span class="sxs-lookup"><span data-stu-id="8cb5a-115">Example 2: Configure external radius based authentication on existing gateway</span></span>
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> $Secure_String_Pwd = ConvertTo-SecureString "TestRadiusServerPassword" -AsPlainText -Force
PS C:\> Set-AzureRmVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway $Gateway -VpnClientAddressPool "10.0.0.0/16" -RadiusServerAddress "TestRadiusServer" -RadiusServerSecret $Secure_String_Pwd
```

<span data-ttu-id="8cb5a-116">Este exemplo atribui um pool de endereços de cliente VPN a um gateway de rede virtual chamado ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="8cb5a-116">This example assigns a VPN client address pool to a virtual network gateway named ContosoVirtualGateway.</span></span>
<span data-ttu-id="8cb5a-117">O primeiro comando cria uma referência de objeto para o gateway e o objeto é armazenado em uma variável chamada $Gateway.</span><span class="sxs-lookup"><span data-stu-id="8cb5a-117">The first command creates an object reference to the gateway and the object is stored in a variable named $Gateway.</span></span>
<span data-ttu-id="8cb5a-118">O segundo comando no exemplo usa o cmdlet **set-AzureRmVirtualNetworkGatewayVpnClientConfig** para atribuir o pool de endereços 10.0.0.0/16 ao ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="8cb5a-118">The second command in the example then uses the **Set-AzureRmVirtualNetworkGatewayVpnClientConfig** cmdlet to assign the address pool 10.0.0.0/16 to ContosoVirtualGateway.</span></span> <span data-ttu-id="8cb5a-119">Ele também configura o servidor RADIUS externo "TestRadiusServer" para ser usado para autenticação para clientes VPN.</span><span class="sxs-lookup"><span data-stu-id="8cb5a-119">It also configures the external radius server "TestRadiusServer" to be used for authentication for vpn clients.</span></span>

## <span data-ttu-id="8cb5a-120">OS</span><span class="sxs-lookup"><span data-stu-id="8cb5a-120">PARAMETERS</span></span>

### <span data-ttu-id="8cb5a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cb5a-121">-DefaultProfile</span></span>
<span data-ttu-id="8cb5a-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8cb5a-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8cb5a-123">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="8cb5a-123">-RadiusServerAddress</span></span>
<span data-ttu-id="8cb5a-124">P2S endereço do servidor RADIUS externo.</span><span class="sxs-lookup"><span data-stu-id="8cb5a-124">P2S External Radius server address.</span></span>

```yaml
Type: System.String
Parameter Sets: RadiusServerConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cb5a-125">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="8cb5a-125">-RadiusServerSecret</span></span>
<span data-ttu-id="8cb5a-126">P2S segredo do servidor RADIUS externo.</span><span class="sxs-lookup"><span data-stu-id="8cb5a-126">P2S External Radius server secret.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: RadiusServerConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cb5a-127">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8cb5a-127">-VirtualNetworkGateway</span></span>
<span data-ttu-id="8cb5a-128">Especifica uma referência de objeto ao gateway de rede virtual que contém as definições de configuração de cliente VPN que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="8cb5a-128">Specifies an object reference to the virtual network gateway that contains the VPN client configuration settings that this cmdlet modifies.</span></span>
<span data-ttu-id="8cb5a-129">Você pode criar uma referência de objeto para um gateway de rede virtual usando o Get-AzureRmVirtualNetworkGateway e especificando o nome do gateway.</span><span class="sxs-lookup"><span data-stu-id="8cb5a-129">You can create an object reference to a virtual network gateway by using the Get-AzureRmVirtualNetworkGateway and specifying the name of the gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8cb5a-130">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="8cb5a-130">-VpnClientAddressPool</span></span>
<span data-ttu-id="8cb5a-131">Especifica os endereços IP a serem atribuídos a clientes que se conectam a este gateway</span><span class="sxs-lookup"><span data-stu-id="8cb5a-131">Specifies the IP addresses to be assigned to clients connecting to this gateway</span></span>

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

### <span data-ttu-id="8cb5a-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8cb5a-132">-Confirm</span></span>
<span data-ttu-id="8cb5a-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8cb5a-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cb5a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8cb5a-134">-WhatIf</span></span>
<span data-ttu-id="8cb5a-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8cb5a-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8cb5a-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8cb5a-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cb5a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cb5a-137">CommonParameters</span></span>
<span data-ttu-id="8cb5a-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8cb5a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cb5a-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8cb5a-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cb5a-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8cb5a-140">INPUTS</span></span>

### <span data-ttu-id="8cb5a-141">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8cb5a-141">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>
<span data-ttu-id="8cb5a-142">Parâmetros: VirtualNetworkGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8cb5a-142">Parameters: VirtualNetworkGateway (ByValue)</span></span>

### <span data-ttu-id="8cb5a-143">System. Collections. Generic. List ' 1 [System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="8cb5a-143">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="8cb5a-144">System. String</span><span class="sxs-lookup"><span data-stu-id="8cb5a-144">System.String</span></span>

### <span data-ttu-id="8cb5a-145">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="8cb5a-145">System.Security.SecureString</span></span>

## <span data-ttu-id="8cb5a-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8cb5a-146">OUTPUTS</span></span>

### <span data-ttu-id="8cb5a-147">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8cb5a-147">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="8cb5a-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8cb5a-148">NOTES</span></span>

## <span data-ttu-id="8cb5a-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8cb5a-149">RELATED LINKS</span></span>

[<span data-ttu-id="8cb5a-150">Get-AzureRmVpnClientPackage</span><span class="sxs-lookup"><span data-stu-id="8cb5a-150">Get-AzureRmVpnClientPackage</span></span>](./Get-AzureRmVpnClientPackage.md)

[<span data-ttu-id="8cb5a-151">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8cb5a-151">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="8cb5a-152">Redimensionar-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8cb5a-152">Resize-AzureRmVirtualNetworkGateway</span></span>](./Resize-AzureRmVirtualNetworkGateway.md)


