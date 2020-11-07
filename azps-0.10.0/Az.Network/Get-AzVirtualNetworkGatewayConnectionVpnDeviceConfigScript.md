---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayconnectionvpndeviceconfigscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript.md
ms.openlocfilehash: 3d955b2133f4a262b69de1413c5a4bf4d8e719b9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775468"
---
# <span data-ttu-id="b07c1-101">Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript</span><span class="sxs-lookup"><span data-stu-id="b07c1-101">Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript</span></span>

## <span data-ttu-id="b07c1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b07c1-102">SYNOPSIS</span></span>
<span data-ttu-id="b07c1-103">Esse commandlet assume o recurso de conexão, a marca de dispositivo VPN, o modelo, a versão do firmware e retorna o script de configuração correspondente que os clientes podem aplicar diretamente em seus dispositivos VPN locais.</span><span class="sxs-lookup"><span data-stu-id="b07c1-103">This commandlet takes the connection resource, VPN device brand, model, firmware version, and return the corresponding configuration script that customers can apply directly on their on-premises VPN devices.</span></span> <span data-ttu-id="b07c1-104">O script acompanhará a sintaxe do dispositivo selecionado e preencherá os parâmetros necessários, como endereços IP públicos do gateway do Azure, prefixos de endereço de rede virtual, chave pré-compartilhada de encapsulamento VPN, etc. para que os clientes possam simplesmente copiar-colar para suas configurações de dispositivo VPN.</span><span class="sxs-lookup"><span data-stu-id="b07c1-104">The script will follow the syntax of the selected device, and fill in the necessary parameters such as Azure gateway public IP addresses, virtual network address prefixes, VPN tunnel pre-shared key, etc. so customers can simply copy-paste to their VPN device configurations.</span></span>

## <span data-ttu-id="b07c1-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b07c1-105">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript -Name <String> -ResourceGroupName <String>
 -DeviceVendor <String> -DeviceFamily <String> -FirmwareVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b07c1-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b07c1-106">DESCRIPTION</span></span>
<span data-ttu-id="b07c1-107">Esse commandlet assume o recurso de conexão, a marca de dispositivo VPN, o modelo, a versão do firmware e retorna o script de configuração correspondente que os clientes podem aplicar diretamente em seus dispositivos VPN locais.</span><span class="sxs-lookup"><span data-stu-id="b07c1-107">This commandlet takes the connection resource, VPN device brand, model, firmware version, and return the corresponding configuration script that customers can apply directly on their on-premises VPN devices.</span></span> <span data-ttu-id="b07c1-108">O script acompanhará a sintaxe do dispositivo selecionado e preencherá os parâmetros necessários, como endereços IP públicos do gateway do Azure, prefixos de endereço de rede virtual, chave pré-compartilhada de encapsulamento VPN, etc. para que os clientes possam simplesmente copiar-colar para suas configurações de dispositivo VPN.</span><span class="sxs-lookup"><span data-stu-id="b07c1-108">The script will follow the syntax of the selected device, and fill in the necessary parameters such as Azure gateway public IP addresses, virtual network address prefixes, VPN tunnel pre-shared key, etc. so customers can simply copy-paste to their VPN device configurations.</span></span>

## <span data-ttu-id="b07c1-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b07c1-109">EXAMPLES</span></span>

### <span data-ttu-id="b07c1-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b07c1-110">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkGatewaySupportedVpnDevice -ResourceGroupName TestRG -Name TestGateway
PS C:\> Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript -ResourceGroupName TestRG -Name TestConnection -DeviceVendor "Cisco-Test" -DeviceFamily "IOS-Test" -FirmwareVersion "20"
```

<span data-ttu-id="b07c1-111">O exemplo acima usa Get-AzVirtualNetworkGatewaySupportedVpnDevice para obter as marcas de dispositivo VPN, os modelos e as versões de firmware com suporte.</span><span class="sxs-lookup"><span data-stu-id="b07c1-111">The above example uses Get-AzVirtualNetworkGatewaySupportedVpnDevice to get the supported VPN Device brands, models, and firmware versions.</span></span>
<span data-ttu-id="b07c1-112">Em seguida, usa uma das informações de modelos retornados para gerar um script de configuração de dispositivo VPN para o VirtualNetworkGatewayConnection "TestConnection".</span><span class="sxs-lookup"><span data-stu-id="b07c1-112">Then uses one of the returned models information to generate a VPN Device configuration script for the VirtualNetworkGatewayConnection "TestConnection".</span></span> <span data-ttu-id="b07c1-113">O dispositivo usado neste exemplo tem o DeviceFamily "IOS-Test", DeviceVendor "Cisco-Test" e FirmwareVersion 20.</span><span class="sxs-lookup"><span data-stu-id="b07c1-113">The device used in this example has DeviceFamily "IOS-Test", DeviceVendor "Cisco-Test" and FirmwareVersion 20.</span></span>

## <span data-ttu-id="b07c1-114">OS</span><span class="sxs-lookup"><span data-stu-id="b07c1-114">PARAMETERS</span></span>

### <span data-ttu-id="b07c1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b07c1-115">-DefaultProfile</span></span>
<span data-ttu-id="b07c1-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b07c1-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b07c1-117">-DeviceFamily</span><span class="sxs-lookup"><span data-stu-id="b07c1-117">-DeviceFamily</span></span>
<span data-ttu-id="b07c1-118">Nome do modelo/família de dispositivo VPN.</span><span class="sxs-lookup"><span data-stu-id="b07c1-118">Name of the VPN device model/family.</span></span>

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

### <span data-ttu-id="b07c1-119">-DeviceVendor</span><span class="sxs-lookup"><span data-stu-id="b07c1-119">-DeviceVendor</span></span>
<span data-ttu-id="b07c1-120">Nome do fornecedor do dispositivo VPN.</span><span class="sxs-lookup"><span data-stu-id="b07c1-120">Name of the VPN device vendor.</span></span>

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

### <span data-ttu-id="b07c1-121">-FirmwareVersion</span><span class="sxs-lookup"><span data-stu-id="b07c1-121">-FirmwareVersion</span></span>
<span data-ttu-id="b07c1-122">Versão do firmware do dispositivo VPN.</span><span class="sxs-lookup"><span data-stu-id="b07c1-122">Firmware version of the VPN device.</span></span>

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

### <span data-ttu-id="b07c1-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="b07c1-123">-Name</span></span>
<span data-ttu-id="b07c1-124">O nome do recurso da conexão para a qual a configuração será gerada.</span><span class="sxs-lookup"><span data-stu-id="b07c1-124">The resource name of the connection for which the configuration is to be generated.</span></span>

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

### <span data-ttu-id="b07c1-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b07c1-125">-ResourceGroupName</span></span>
<span data-ttu-id="b07c1-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b07c1-126">The resource group name.</span></span>

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

### <span data-ttu-id="b07c1-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b07c1-127">-Confirm</span></span>
<span data-ttu-id="b07c1-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b07c1-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b07c1-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b07c1-129">-WhatIf</span></span>
<span data-ttu-id="b07c1-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b07c1-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b07c1-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b07c1-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b07c1-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b07c1-132">CommonParameters</span></span>
<span data-ttu-id="b07c1-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b07c1-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b07c1-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b07c1-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b07c1-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b07c1-135">INPUTS</span></span>

### <span data-ttu-id="b07c1-136">System. String</span><span class="sxs-lookup"><span data-stu-id="b07c1-136">System.String</span></span>

## <span data-ttu-id="b07c1-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b07c1-137">OUTPUTS</span></span>

### <span data-ttu-id="b07c1-138">System. String</span><span class="sxs-lookup"><span data-stu-id="b07c1-138">System.String</span></span>

## <span data-ttu-id="b07c1-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b07c1-139">NOTES</span></span>

## <span data-ttu-id="b07c1-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b07c1-140">RELATED LINKS</span></span>

