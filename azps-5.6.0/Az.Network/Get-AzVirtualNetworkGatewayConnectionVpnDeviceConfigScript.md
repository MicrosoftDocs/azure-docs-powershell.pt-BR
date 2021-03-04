---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualnetworkgatewayconnectionvpndeviceconfigscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript.md
ms.openlocfilehash: 967e45ce124ead583a7c2f3e36a80dedb80d4e20
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888672"
---
# <span data-ttu-id="fe31d-101">Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript</span><span class="sxs-lookup"><span data-stu-id="fe31d-101">Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript</span></span>

## <span data-ttu-id="fe31d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe31d-102">SYNOPSIS</span></span>
<span data-ttu-id="fe31d-103">Esse commandlet pega o recurso de conexão, a marca do dispositivo VPN, o modelo, a versão do firmware e retorna o script de configuração correspondente que os clientes podem aplicar diretamente em seus dispositivos VPN locais.</span><span class="sxs-lookup"><span data-stu-id="fe31d-103">This commandlet takes the connection resource, VPN device brand, model, firmware version, and return the corresponding configuration script that customers can apply directly on their on-premises VPN devices.</span></span> <span data-ttu-id="fe31d-104">O script seguirá a sintaxe do dispositivo selecionado e preencherá os parâmetros necessários, como endereços IP públicos do gateway do Azure, prefixos de endereço de rede virtual, chave pré-compartilhada do túnel VPN, etc. para que os clientes possam simplesmente copiar as configurações do dispositivo VPN.</span><span class="sxs-lookup"><span data-stu-id="fe31d-104">The script will follow the syntax of the selected device, and fill in the necessary parameters such as Azure gateway public IP addresses, virtual network address prefixes, VPN tunnel pre-shared key, etc. so customers can simply copy-paste to their VPN device configurations.</span></span>

## <span data-ttu-id="fe31d-105">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="fe31d-105">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript -Name <String> -ResourceGroupName <String>
 -DeviceVendor <String> -DeviceFamily <String> -FirmwareVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe31d-106">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="fe31d-106">DESCRIPTION</span></span>
<span data-ttu-id="fe31d-107">Esse commandlet pega o recurso de conexão, a marca do dispositivo VPN, o modelo, a versão do firmware e retorna o script de configuração correspondente que os clientes podem aplicar diretamente em seus dispositivos VPN locais.</span><span class="sxs-lookup"><span data-stu-id="fe31d-107">This commandlet takes the connection resource, VPN device brand, model, firmware version, and return the corresponding configuration script that customers can apply directly on their on-premises VPN devices.</span></span> <span data-ttu-id="fe31d-108">O script seguirá a sintaxe do dispositivo selecionado e preencherá os parâmetros necessários, como endereços IP públicos do gateway do Azure, prefixos de endereço de rede virtual, chave pré-compartilhada do túnel VPN, etc. para que os clientes possam simplesmente copiar as configurações do dispositivo VPN.</span><span class="sxs-lookup"><span data-stu-id="fe31d-108">The script will follow the syntax of the selected device, and fill in the necessary parameters such as Azure gateway public IP addresses, virtual network address prefixes, VPN tunnel pre-shared key, etc. so customers can simply copy-paste to their VPN device configurations.</span></span>

## <span data-ttu-id="fe31d-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fe31d-109">EXAMPLES</span></span>

### <span data-ttu-id="fe31d-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fe31d-110">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkGatewaySupportedVpnDevice -ResourceGroupName TestRG -Name TestGateway
PS C:\> Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript -ResourceGroupName TestRG -Name TestConnection -DeviceVendor "Cisco-Test" -DeviceFamily "IOS-Test" -FirmwareVersion "20"
```

<span data-ttu-id="fe31d-111">O exemplo acima usa Get-AzVirtualNetworkGatewaySupportedVpnDevice para obter as marcas, os modelos e as versões de firmware do Dispositivo VPN com suporte.</span><span class="sxs-lookup"><span data-stu-id="fe31d-111">The above example uses Get-AzVirtualNetworkGatewaySupportedVpnDevice to get the supported VPN Device brands, models, and firmware versions.</span></span>
<span data-ttu-id="fe31d-112">Em seguida, usa uma das informações de modelos retornados para gerar um script de configuração do Dispositivo VPN para o VirtualNetworkGatewayConnection "TestConnection".</span><span class="sxs-lookup"><span data-stu-id="fe31d-112">Then uses one of the returned models information to generate a VPN Device configuration script for the VirtualNetworkGatewayConnection "TestConnection".</span></span> <span data-ttu-id="fe31d-113">O dispositivo usado neste exemplo tem DeviceFamily "IOS-Test", DeviceVendor "Cisco-Test" e FirmwareVersion 20.</span><span class="sxs-lookup"><span data-stu-id="fe31d-113">The device used in this example has DeviceFamily "IOS-Test", DeviceVendor "Cisco-Test" and FirmwareVersion 20.</span></span>

## <span data-ttu-id="fe31d-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="fe31d-114">PARAMETERS</span></span>

### <span data-ttu-id="fe31d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe31d-115">-DefaultProfile</span></span>
<span data-ttu-id="fe31d-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="fe31d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fe31d-117">-DeviceFamily</span><span class="sxs-lookup"><span data-stu-id="fe31d-117">-DeviceFamily</span></span>
<span data-ttu-id="fe31d-118">Nome do modelo de dispositivo VPN/família.</span><span class="sxs-lookup"><span data-stu-id="fe31d-118">Name of the VPN device model/family.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe31d-119">-DeviceVendor</span><span class="sxs-lookup"><span data-stu-id="fe31d-119">-DeviceVendor</span></span>
<span data-ttu-id="fe31d-120">Nome do fornecedor de dispositivo VPN.</span><span class="sxs-lookup"><span data-stu-id="fe31d-120">Name of the VPN device vendor.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe31d-121">-FirmwareVersion</span><span class="sxs-lookup"><span data-stu-id="fe31d-121">-FirmwareVersion</span></span>
<span data-ttu-id="fe31d-122">Versão de firmware do dispositivo VPN.</span><span class="sxs-lookup"><span data-stu-id="fe31d-122">Firmware version of the VPN device.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe31d-123">-Name</span><span class="sxs-lookup"><span data-stu-id="fe31d-123">-Name</span></span>
<span data-ttu-id="fe31d-124">O nome do recurso da conexão para a qual a configuração deve ser gerada.</span><span class="sxs-lookup"><span data-stu-id="fe31d-124">The resource name of the connection for which the configuration is to be generated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe31d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe31d-125">-ResourceGroupName</span></span>
<span data-ttu-id="fe31d-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="fe31d-126">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe31d-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fe31d-127">-Confirm</span></span>
<span data-ttu-id="fe31d-128">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe31d-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe31d-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe31d-129">-WhatIf</span></span>
<span data-ttu-id="fe31d-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fe31d-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe31d-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fe31d-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe31d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe31d-132">CommonParameters</span></span>
<span data-ttu-id="fe31d-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe31d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe31d-134">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fe31d-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe31d-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fe31d-135">INPUTS</span></span>

### <span data-ttu-id="fe31d-136">System.String</span><span class="sxs-lookup"><span data-stu-id="fe31d-136">System.String</span></span>

## <span data-ttu-id="fe31d-137">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="fe31d-137">OUTPUTS</span></span>

### <span data-ttu-id="fe31d-138">System.String</span><span class="sxs-lookup"><span data-stu-id="fe31d-138">System.String</span></span>

## <span data-ttu-id="fe31d-139">NOTES</span><span class="sxs-lookup"><span data-stu-id="fe31d-139">NOTES</span></span>

## <span data-ttu-id="fe31d-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fe31d-140">RELATED LINKS</span></span>
