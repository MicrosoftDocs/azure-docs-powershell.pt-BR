---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewaysupportedvpndevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewaySupportedVpnDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewaySupportedVpnDevice.md
ms.openlocfilehash: f643b280e0777f3251380ecf36f4fcc070b545c1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112877"
---
# <span data-ttu-id="92278-101">Get-AzVirtualNetworkGatewaySupportedVpnDevice</span><span class="sxs-lookup"><span data-stu-id="92278-101">Get-AzVirtualNetworkGatewaySupportedVpnDevice</span></span>

## <span data-ttu-id="92278-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="92278-102">SYNOPSIS</span></span>
<span data-ttu-id="92278-103">Este commandlet retorna uma lista de marcas de dispositivo VPN com suporte, modelos e versões de firmware.</span><span class="sxs-lookup"><span data-stu-id="92278-103">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

## <span data-ttu-id="92278-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="92278-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewaySupportedVpnDevice -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92278-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="92278-105">DESCRIPTION</span></span>
<span data-ttu-id="92278-106">Este commandlet retorna uma lista de marcas de dispositivo VPN com suporte, modelos e versões de firmware.</span><span class="sxs-lookup"><span data-stu-id="92278-106">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

## <span data-ttu-id="92278-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="92278-107">EXAMPLES</span></span>

### <span data-ttu-id="92278-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="92278-108">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkGatewaySupportedVpnDevice -ResourceGroupName TestRG -Name TestGateway 
<?xml version="1.0" encoding="utf-8"?>
<RpVpnDeviceList version="1.0">
  <Vendor name="Cisco-Test">
    <DeviceFamily name="IOS-Test">
       <FirmwareVersion name="20" />
    </DeviceFamily>
  </Vendor>
</RpVpnDeviceList>
```

<span data-ttu-id="92278-109">Retorna uma lista de marcas de dispositivo VPN com suporte, modelos e versões de firmware:</span><span class="sxs-lookup"><span data-stu-id="92278-109">Returns list of supported VPN device brands, models and firmware versions:</span></span>
<?xml version="1.0" encoding="utf-8"?>
<RpVpnDeviceList version="1.0">
  <Vendor name="Cisco-Test">
    <DeviceFamily name="IOS-Test">
       <FirmwareVersion name="20" />
    </DeviceFamily>
  </Vendor>
</RpVpnDeviceList>

## <span data-ttu-id="92278-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="92278-110">PARAMETERS</span></span>

### <span data-ttu-id="92278-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92278-111">-DefaultProfile</span></span>
<span data-ttu-id="92278-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="92278-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92278-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="92278-113">-Name</span></span>
<span data-ttu-id="92278-114">O nome do gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="92278-114">The virtual network gateway name.</span></span>

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

### <span data-ttu-id="92278-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92278-115">-ResourceGroupName</span></span>
<span data-ttu-id="92278-116">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="92278-116">The resource group name.</span></span>

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

### <span data-ttu-id="92278-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92278-117">CommonParameters</span></span>
<span data-ttu-id="92278-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92278-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92278-119">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="92278-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92278-120">Entradas</span><span class="sxs-lookup"><span data-stu-id="92278-120">INPUTS</span></span>

### <span data-ttu-id="92278-121">System.String</span><span class="sxs-lookup"><span data-stu-id="92278-121">System.String</span></span>

## <span data-ttu-id="92278-122">Saídas</span><span class="sxs-lookup"><span data-stu-id="92278-122">OUTPUTS</span></span>

### <span data-ttu-id="92278-123">System.String</span><span class="sxs-lookup"><span data-stu-id="92278-123">System.String</span></span>

## <span data-ttu-id="92278-124">Notas</span><span class="sxs-lookup"><span data-stu-id="92278-124">NOTES</span></span>

## <span data-ttu-id="92278-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="92278-125">RELATED LINKS</span></span>
