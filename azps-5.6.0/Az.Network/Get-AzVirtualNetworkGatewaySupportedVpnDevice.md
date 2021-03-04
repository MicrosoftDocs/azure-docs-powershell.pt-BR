---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualnetworkgatewaysupportedvpndevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewaySupportedVpnDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewaySupportedVpnDevice.md
ms.openlocfilehash: 45cb703d6fdc87238f4d1ed35ada90aadeed501b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889923"
---
# <span data-ttu-id="e7e75-101">Get-AzVirtualNetworkGatewaySupportedVpnDevice</span><span class="sxs-lookup"><span data-stu-id="e7e75-101">Get-AzVirtualNetworkGatewaySupportedVpnDevice</span></span>

## <span data-ttu-id="e7e75-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7e75-102">SYNOPSIS</span></span>
<span data-ttu-id="e7e75-103">Este commandlet retorna uma lista de marcas de dispositivos VPN com suporte, modelos e versões de firmware.</span><span class="sxs-lookup"><span data-stu-id="e7e75-103">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

## <span data-ttu-id="e7e75-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e7e75-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewaySupportedVpnDevice -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e7e75-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e7e75-105">DESCRIPTION</span></span>
<span data-ttu-id="e7e75-106">Este commandlet retorna uma lista de marcas de dispositivos VPN com suporte, modelos e versões de firmware.</span><span class="sxs-lookup"><span data-stu-id="e7e75-106">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

## <span data-ttu-id="e7e75-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e7e75-107">EXAMPLES</span></span>

### <span data-ttu-id="e7e75-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e7e75-108">Example 1</span></span>
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

<span data-ttu-id="e7e75-109">Retorna a lista de marcas de dispositivos VPN com suporte, modelos e versões de firmware:</span><span class="sxs-lookup"><span data-stu-id="e7e75-109">Returns list of supported VPN device brands, models and firmware versions:</span></span>
<?xml version="1.0" encoding="utf-8"?>
<RpVpnDeviceList version="1.0">
  <Vendor name="Cisco-Test">
    <DeviceFamily name="IOS-Test">
       <FirmwareVersion name="20" />
    </DeviceFamily>
  </Vendor>
</RpVpnDeviceList>

## <span data-ttu-id="e7e75-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e7e75-110">PARAMETERS</span></span>

### <span data-ttu-id="e7e75-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7e75-111">-DefaultProfile</span></span>
<span data-ttu-id="e7e75-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="e7e75-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e7e75-113">-Name</span><span class="sxs-lookup"><span data-stu-id="e7e75-113">-Name</span></span>
<span data-ttu-id="e7e75-114">O nome do gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="e7e75-114">The virtual network gateway name.</span></span>

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

### <span data-ttu-id="e7e75-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7e75-115">-ResourceGroupName</span></span>
<span data-ttu-id="e7e75-116">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e7e75-116">The resource group name.</span></span>

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

### <span data-ttu-id="e7e75-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7e75-117">CommonParameters</span></span>
<span data-ttu-id="e7e75-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7e75-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7e75-119">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e7e75-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7e75-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e7e75-120">INPUTS</span></span>

### <span data-ttu-id="e7e75-121">System.String</span><span class="sxs-lookup"><span data-stu-id="e7e75-121">System.String</span></span>

## <span data-ttu-id="e7e75-122">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e7e75-122">OUTPUTS</span></span>

### <span data-ttu-id="e7e75-123">System.String</span><span class="sxs-lookup"><span data-stu-id="e7e75-123">System.String</span></span>

## <span data-ttu-id="e7e75-124">NOTES</span><span class="sxs-lookup"><span data-stu-id="e7e75-124">NOTES</span></span>

## <span data-ttu-id="e7e75-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e7e75-125">RELATED LINKS</span></span>
