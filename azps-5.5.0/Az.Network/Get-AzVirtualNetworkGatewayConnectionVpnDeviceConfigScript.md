---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayconnectionvpndeviceconfigscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript.md
ms.openlocfilehash: 5421c33c4858c99be4dd84ba7f0c1bff401e1182
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112878"
---
# <span data-ttu-id="34af2-101">Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript</span><span class="sxs-lookup"><span data-stu-id="34af2-101">Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript</span></span>

## <span data-ttu-id="34af2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="34af2-102">SYNOPSIS</span></span>
<span data-ttu-id="34af2-103">Esse commandlet assume o recurso de conexão, a marca do dispositivo VPN, o modelo, a versão do firmware e retorna o script de configuração correspondente que os clientes podem aplicar diretamente em seus dispositivos VPN locais.</span><span class="sxs-lookup"><span data-stu-id="34af2-103">This commandlet takes the connection resource, VPN device brand, model, firmware version, and return the corresponding configuration script that customers can apply directly on their on-premises VPN devices.</span></span> <span data-ttu-id="34af2-104">O script seguirá a sintaxe do dispositivo selecionado e preencherá os parâmetros necessários, como endereços IP públicos do gateway do Azure, prefixos de endereço de rede virtual, chave pré-compartilhada do túnel VPN, etc. para que os clientes possam simplesmente copiar e colar em suas configurações de dispositivo VPN.</span><span class="sxs-lookup"><span data-stu-id="34af2-104">The script will follow the syntax of the selected device, and fill in the necessary parameters such as Azure gateway public IP addresses, virtual network address prefixes, VPN tunnel pre-shared key, etc. so customers can simply copy-paste to their VPN device configurations.</span></span>

## <span data-ttu-id="34af2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="34af2-105">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript -Name <String> -ResourceGroupName <String>
 -DeviceVendor <String> -DeviceFamily <String> -FirmwareVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34af2-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="34af2-106">DESCRIPTION</span></span>
<span data-ttu-id="34af2-107">Esse commandlet assume o recurso de conexão, a marca do dispositivo VPN, o modelo, a versão do firmware e retorna o script de configuração correspondente que os clientes podem aplicar diretamente em seus dispositivos VPN locais.</span><span class="sxs-lookup"><span data-stu-id="34af2-107">This commandlet takes the connection resource, VPN device brand, model, firmware version, and return the corresponding configuration script that customers can apply directly on their on-premises VPN devices.</span></span> <span data-ttu-id="34af2-108">O script seguirá a sintaxe do dispositivo selecionado e preencherá os parâmetros necessários, como endereços IP públicos do gateway do Azure, prefixos de endereço de rede virtual, chave pré-compartilhada do túnel VPN, etc. para que os clientes possam simplesmente copiar e colar em suas configurações de dispositivo VPN.</span><span class="sxs-lookup"><span data-stu-id="34af2-108">The script will follow the syntax of the selected device, and fill in the necessary parameters such as Azure gateway public IP addresses, virtual network address prefixes, VPN tunnel pre-shared key, etc. so customers can simply copy-paste to their VPN device configurations.</span></span>

## <span data-ttu-id="34af2-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="34af2-109">EXAMPLES</span></span>

### <span data-ttu-id="34af2-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="34af2-110">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkGatewaySupportedVpnDevice -ResourceGroupName TestRG -Name TestGateway
PS C:\> Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript -ResourceGroupName TestRG -Name TestConnection -DeviceVendor "Cisco-Test" -DeviceFamily "IOS-Test" -FirmwareVersion "20"
```

<span data-ttu-id="34af2-111">O exemplo acima usa Get-AzVirtualNetworkGatewaySupportedVpnDevice para obter as marcas, modelos e versões de firmware de dispositivo VPN com suporte.</span><span class="sxs-lookup"><span data-stu-id="34af2-111">The above example uses Get-AzVirtualNetworkGatewaySupportedVpnDevice to get the supported VPN Device brands, models, and firmware versions.</span></span>
<span data-ttu-id="34af2-112">Em seguida, usa uma das informações de modelos retornados para gerar um script de configuração de dispositivo VPN para o virtualNetworkGatewayConnection "TestConnection".</span><span class="sxs-lookup"><span data-stu-id="34af2-112">Then uses one of the returned models information to generate a VPN Device configuration script for the VirtualNetworkGatewayConnection "TestConnection".</span></span> <span data-ttu-id="34af2-113">O dispositivo usado neste exemplo tem DeviceFamily "Teste IOS", DeviceVendor "Cisco-Test" e FirmwareVersion 20.</span><span class="sxs-lookup"><span data-stu-id="34af2-113">The device used in this example has DeviceFamily "IOS-Test", DeviceVendor "Cisco-Test" and FirmwareVersion 20.</span></span>

## <span data-ttu-id="34af2-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="34af2-114">PARAMETERS</span></span>

### <span data-ttu-id="34af2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34af2-115">-DefaultProfile</span></span>
<span data-ttu-id="34af2-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="34af2-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34af2-117">-DeviceFamily</span><span class="sxs-lookup"><span data-stu-id="34af2-117">-DeviceFamily</span></span>
<span data-ttu-id="34af2-118">Nome do modelo de dispositivo VPN/família.</span><span class="sxs-lookup"><span data-stu-id="34af2-118">Name of the VPN device model/family.</span></span>

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

### <span data-ttu-id="34af2-119">-DeviceVendor</span><span class="sxs-lookup"><span data-stu-id="34af2-119">-DeviceVendor</span></span>
<span data-ttu-id="34af2-120">Nome do fornecedor de dispositivo VPN.</span><span class="sxs-lookup"><span data-stu-id="34af2-120">Name of the VPN device vendor.</span></span>

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

### <span data-ttu-id="34af2-121">-FirmwareVersion</span><span class="sxs-lookup"><span data-stu-id="34af2-121">-FirmwareVersion</span></span>
<span data-ttu-id="34af2-122">Versão de firmware do dispositivo VPN.</span><span class="sxs-lookup"><span data-stu-id="34af2-122">Firmware version of the VPN device.</span></span>

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

### <span data-ttu-id="34af2-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="34af2-123">-Name</span></span>
<span data-ttu-id="34af2-124">O nome do recurso da conexão para a qual a configuração deve ser gerada.</span><span class="sxs-lookup"><span data-stu-id="34af2-124">The resource name of the connection for which the configuration is to be generated.</span></span>

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

### <span data-ttu-id="34af2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34af2-125">-ResourceGroupName</span></span>
<span data-ttu-id="34af2-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="34af2-126">The resource group name.</span></span>

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

### <span data-ttu-id="34af2-127">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="34af2-127">-Confirm</span></span>
<span data-ttu-id="34af2-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34af2-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34af2-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34af2-129">-WhatIf</span></span>
<span data-ttu-id="34af2-130">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="34af2-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34af2-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="34af2-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34af2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34af2-132">CommonParameters</span></span>
<span data-ttu-id="34af2-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34af2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34af2-134">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="34af2-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34af2-135">Entradas</span><span class="sxs-lookup"><span data-stu-id="34af2-135">INPUTS</span></span>

### <span data-ttu-id="34af2-136">System.String</span><span class="sxs-lookup"><span data-stu-id="34af2-136">System.String</span></span>

## <span data-ttu-id="34af2-137">Saídas</span><span class="sxs-lookup"><span data-stu-id="34af2-137">OUTPUTS</span></span>

### <span data-ttu-id="34af2-138">System.String</span><span class="sxs-lookup"><span data-stu-id="34af2-138">System.String</span></span>

## <span data-ttu-id="34af2-139">Notas</span><span class="sxs-lookup"><span data-stu-id="34af2-139">NOTES</span></span>

## <span data-ttu-id="34af2-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="34af2-140">RELATED LINKS</span></span>
