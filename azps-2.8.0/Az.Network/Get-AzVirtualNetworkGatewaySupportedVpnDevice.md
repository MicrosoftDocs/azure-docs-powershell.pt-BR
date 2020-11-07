---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewaysupportedvpndevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewaySupportedVpnDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewaySupportedVpnDevice.md
ms.openlocfilehash: 0ff95b3e212e61b3d8c9d01b0ad745963d7b24e7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771701"
---
# <span data-ttu-id="db1e4-101">Get-AzVirtualNetworkGatewaySupportedVpnDevice</span><span class="sxs-lookup"><span data-stu-id="db1e4-101">Get-AzVirtualNetworkGatewaySupportedVpnDevice</span></span>

## <span data-ttu-id="db1e4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="db1e4-102">SYNOPSIS</span></span>
<span data-ttu-id="db1e4-103">Este commandlet retorna uma lista de marcas de dispositivo VPN, modelos e versões de firmware com suporte.</span><span class="sxs-lookup"><span data-stu-id="db1e4-103">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

## <span data-ttu-id="db1e4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="db1e4-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewaySupportedVpnDevice -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="db1e4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="db1e4-105">DESCRIPTION</span></span>
<span data-ttu-id="db1e4-106">Este commandlet retorna uma lista de marcas de dispositivo VPN, modelos e versões de firmware com suporte.</span><span class="sxs-lookup"><span data-stu-id="db1e4-106">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

## <span data-ttu-id="db1e4-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="db1e4-107">EXAMPLES</span></span>

### <span data-ttu-id="db1e4-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="db1e4-108">Example 1</span></span>
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

<span data-ttu-id="db1e4-109">Retorna a lista de marcas de dispositivo VPN, modelos e versões de firmware com suporte:</span><span class="sxs-lookup"><span data-stu-id="db1e4-109">Returns list of supported VPN device brands, models and firmware versions:</span></span>
<?xml version="1.0" encoding="utf-8"?>
<RpVpnDeviceList version="1.0">
  <Vendor name="Cisco-Test">
    <DeviceFamily name="IOS-Test">
       <FirmwareVersion name="20" />
    </DeviceFamily>
  </Vendor>
</RpVpnDeviceList>

## <span data-ttu-id="db1e4-110">OS</span><span class="sxs-lookup"><span data-stu-id="db1e4-110">PARAMETERS</span></span>

### <span data-ttu-id="db1e4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db1e4-111">-DefaultProfile</span></span>
<span data-ttu-id="db1e4-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="db1e4-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db1e4-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="db1e4-113">-Name</span></span>
<span data-ttu-id="db1e4-114">O nome do gateway da rede virtual.</span><span class="sxs-lookup"><span data-stu-id="db1e4-114">The virtual network gateway name.</span></span>

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

### <span data-ttu-id="db1e4-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db1e4-115">-ResourceGroupName</span></span>
<span data-ttu-id="db1e4-116">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="db1e4-116">The resource group name.</span></span>

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

### <span data-ttu-id="db1e4-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db1e4-117">CommonParameters</span></span>
<span data-ttu-id="db1e4-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db1e4-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db1e4-119">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="db1e4-119">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db1e4-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="db1e4-120">INPUTS</span></span>

### <span data-ttu-id="db1e4-121">System. String</span><span class="sxs-lookup"><span data-stu-id="db1e4-121">System.String</span></span>

## <span data-ttu-id="db1e4-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="db1e4-122">OUTPUTS</span></span>

### <span data-ttu-id="db1e4-123">System. String</span><span class="sxs-lookup"><span data-stu-id="db1e4-123">System.String</span></span>

## <span data-ttu-id="db1e4-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="db1e4-124">NOTES</span></span>

## <span data-ttu-id="db1e4-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="db1e4-125">RELATED LINKS</span></span>
