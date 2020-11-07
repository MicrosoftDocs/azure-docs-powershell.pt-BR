---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkgatewayconnectionvpndeviceconfigscript
schema: 2.0.0
ms.openlocfilehash: 0565956d7f40a633bc1aa2c2049ef9a7d764d77e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786088"
---
# <span data-ttu-id="e7c19-101">Get-AzureRmVirtualNetworkGatewayConnectionVpnDeviceConfigScript</span><span class="sxs-lookup"><span data-stu-id="e7c19-101">Get-AzureRmVirtualNetworkGatewayConnectionVpnDeviceConfigScript</span></span>

## <span data-ttu-id="e7c19-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e7c19-102">SYNOPSIS</span></span>
<span data-ttu-id="e7c19-103">Esse commandlet assume o recurso de conexão, a marca de dispositivo VPN, o modelo, a versão do firmware e retorna o script de configuração correspondente que os clientes podem aplicar diretamente em seus dispositivos VPN locais.</span><span class="sxs-lookup"><span data-stu-id="e7c19-103">This commandlet takes the connection resource, VPN device brand, model, firmware version, and return the corresponding configuration script that customers can apply directly on their on-premises VPN devices.</span></span> <span data-ttu-id="e7c19-104">O script acompanhará a sintaxe do dispositivo selecionado e preencherá os parâmetros necessários, como endereços IP públicos do gateway do Azure, prefixos de endereço de rede virtual, chave pré-compartilhada de encapsulamento VPN, etc. para que os clientes possam simplesmente copiar-colar para suas configurações de dispositivo VPN.</span><span class="sxs-lookup"><span data-stu-id="e7c19-104">The script will follow the syntax of the selected device, and fill in the necessary parameters such as Azure gateway public IP addresses, virtual network address prefixes, VPN tunnel pre-shared key, etc. so customers can simply copy-paste to their VPN device configurations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e7c19-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e7c19-105">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGatewayConnectionVpnDeviceConfigScript -Name <String> -ResourceGroupName <String>
 -DeviceVendor <String> -DeviceFamily <String> -FirmwareVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7c19-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e7c19-106">DESCRIPTION</span></span>
<span data-ttu-id="e7c19-107">Esse commandlet assume o recurso de conexão, a marca de dispositivo VPN, o modelo, a versão do firmware e retorna o script de configuração correspondente que os clientes podem aplicar diretamente em seus dispositivos VPN locais.</span><span class="sxs-lookup"><span data-stu-id="e7c19-107">This commandlet takes the connection resource, VPN device brand, model, firmware version, and return the corresponding configuration script that customers can apply directly on their on-premises VPN devices.</span></span> <span data-ttu-id="e7c19-108">O script acompanhará a sintaxe do dispositivo selecionado e preencherá os parâmetros necessários, como endereços IP públicos do gateway do Azure, prefixos de endereço de rede virtual, chave pré-compartilhada de encapsulamento VPN, etc. para que os clientes possam simplesmente copiar-colar para suas configurações de dispositivo VPN.</span><span class="sxs-lookup"><span data-stu-id="e7c19-108">The script will follow the syntax of the selected device, and fill in the necessary parameters such as Azure gateway public IP addresses, virtual network address prefixes, VPN tunnel pre-shared key, etc. so customers can simply copy-paste to their VPN device configurations.</span></span>

## <span data-ttu-id="e7c19-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e7c19-109">EXAMPLES</span></span>

### <span data-ttu-id="e7c19-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e7c19-110">Example 1</span></span>
```
PS C:\> Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice -ResourceGroupName TestRG -Name TestGateway
PS C:\> Get-AzureRmVirtualNetworkGatewayConnectionVpnDeviceConfigScript -ResourceGroupName TestRG -Name TestConnection -DeviceVendor "Cisco-Test" -DeviceFamily "IOS-Test" -FirmwareVersion "20"
```

<span data-ttu-id="e7c19-111">O exemplo acima usa Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice para obter as marcas de dispositivo VPN, os modelos e as versões de firmware com suporte.</span><span class="sxs-lookup"><span data-stu-id="e7c19-111">The above example uses Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice to get the supported VPN Device brands, models, and firmware versions.</span></span>
<span data-ttu-id="e7c19-112">Em seguida, usa uma das informações de modelos retornados para gerar um script de configuração de dispositivo VPN para o VirtualNetworkGatewayConnection "TestConnection".</span><span class="sxs-lookup"><span data-stu-id="e7c19-112">Then uses one of the returned models information to generate a VPN Device configuration script for the VirtualNetworkGatewayConnection "TestConnection".</span></span> <span data-ttu-id="e7c19-113">O dispositivo usado neste exemplo tem o DeviceFamily "IOS-Test", DeviceVendor "Cisco-Test" e FirmwareVersion 20.</span><span class="sxs-lookup"><span data-stu-id="e7c19-113">The device used in this example has DeviceFamily "IOS-Test", DeviceVendor "Cisco-Test" and FirmwareVersion 20.</span></span>

## <span data-ttu-id="e7c19-114">OS</span><span class="sxs-lookup"><span data-stu-id="e7c19-114">PARAMETERS</span></span>

### <span data-ttu-id="e7c19-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7c19-115">-DefaultProfile</span></span>
<span data-ttu-id="e7c19-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e7c19-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e7c19-117">-DeviceFamily</span><span class="sxs-lookup"><span data-stu-id="e7c19-117">-DeviceFamily</span></span>
<span data-ttu-id="e7c19-118">Nome do modelo/família de dispositivo VPN.</span><span class="sxs-lookup"><span data-stu-id="e7c19-118">Name of the VPN device model/family.</span></span>

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

### <span data-ttu-id="e7c19-119">-DeviceVendor</span><span class="sxs-lookup"><span data-stu-id="e7c19-119">-DeviceVendor</span></span>
<span data-ttu-id="e7c19-120">Nome do fornecedor do dispositivo VPN.</span><span class="sxs-lookup"><span data-stu-id="e7c19-120">Name of the VPN device vendor.</span></span>

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

### <span data-ttu-id="e7c19-121">-FirmwareVersion</span><span class="sxs-lookup"><span data-stu-id="e7c19-121">-FirmwareVersion</span></span>
<span data-ttu-id="e7c19-122">Versão do firmware do dispositivo VPN.</span><span class="sxs-lookup"><span data-stu-id="e7c19-122">Firmware version of the VPN device.</span></span>

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

### <span data-ttu-id="e7c19-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="e7c19-123">-Name</span></span>
<span data-ttu-id="e7c19-124">O nome do recurso da conexão para a qual a configuração será gerada.</span><span class="sxs-lookup"><span data-stu-id="e7c19-124">The resource name of the connection for which the configuration is to be generated.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7c19-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7c19-125">-ResourceGroupName</span></span>
<span data-ttu-id="e7c19-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e7c19-126">The resource group name.</span></span>

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

### <span data-ttu-id="e7c19-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e7c19-127">-Confirm</span></span>
<span data-ttu-id="e7c19-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7c19-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7c19-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7c19-129">-WhatIf</span></span>
<span data-ttu-id="e7c19-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e7c19-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7c19-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e7c19-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7c19-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7c19-132">CommonParameters</span></span>
<span data-ttu-id="e7c19-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7c19-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7c19-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7c19-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7c19-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e7c19-135">INPUTS</span></span>

### <span data-ttu-id="e7c19-136">System. String</span><span class="sxs-lookup"><span data-stu-id="e7c19-136">System.String</span></span>

## <span data-ttu-id="e7c19-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e7c19-137">OUTPUTS</span></span>

### <span data-ttu-id="e7c19-138">System. String</span><span class="sxs-lookup"><span data-stu-id="e7c19-138">System.String</span></span>

## <span data-ttu-id="e7c19-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e7c19-139">NOTES</span></span>

## <span data-ttu-id="e7c19-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e7c19-140">RELATED LINKS</span></span>

