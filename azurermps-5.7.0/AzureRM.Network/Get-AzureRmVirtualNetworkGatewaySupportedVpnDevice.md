---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkgatewaysupportedvpndevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice.md
ms.openlocfilehash: 30937c856d1961a1f342c73588aa00c74790ec81
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602633"
---
# <span data-ttu-id="d373e-101">Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice</span><span class="sxs-lookup"><span data-stu-id="d373e-101">Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice</span></span>

## <span data-ttu-id="d373e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d373e-102">SYNOPSIS</span></span>
<span data-ttu-id="d373e-103">Este commandlet retorna uma lista de marcas de dispositivo VPN, modelos e versões de firmware com suporte.</span><span class="sxs-lookup"><span data-stu-id="d373e-103">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d373e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d373e-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d373e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d373e-105">DESCRIPTION</span></span>
<span data-ttu-id="d373e-106">Este commandlet retorna uma lista de marcas de dispositivo VPN, modelos e versões de firmware com suporte.</span><span class="sxs-lookup"><span data-stu-id="d373e-106">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

## <span data-ttu-id="d373e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d373e-107">EXAMPLES</span></span>

### <span data-ttu-id="d373e-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d373e-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice -ResourceGroupName TestRG -Name TestGateway 
<?xml version="1.0" encoding="utf-8"?>
<RpVpnDeviceList version="1.0">
  <Vendor name="Cisco-Test">
    <DeviceFamily name="IOS-Test">
       <FirmwareVersion name="20" />
    </DeviceFamily>
  </Vendor>
</RpVpnDeviceList>
```

<span data-ttu-id="d373e-109">Retorna a lista de marcas de dispositivo VPN, modelos e versões de firmware com suporte:</span><span class="sxs-lookup"><span data-stu-id="d373e-109">Returns list of supported VPN device brands, models and firmware versions:</span></span>
<?xml version="1.0" encoding="utf-8"?>
<RpVpnDeviceList version="1.0">
  <Vendor name="Cisco-Test">
    <DeviceFamily name="IOS-Test">
       <FirmwareVersion name="20" />
    </DeviceFamily>
  </Vendor>
</RpVpnDeviceList>

## <span data-ttu-id="d373e-110">OS</span><span class="sxs-lookup"><span data-stu-id="d373e-110">PARAMETERS</span></span>

### <span data-ttu-id="d373e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d373e-111">-DefaultProfile</span></span>
<span data-ttu-id="d373e-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d373e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d373e-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="d373e-113">-Name</span></span>
<span data-ttu-id="d373e-114">O nome do gateway da rede virtual.</span><span class="sxs-lookup"><span data-stu-id="d373e-114">The virtual network gateway name.</span></span>

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

### <span data-ttu-id="d373e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d373e-115">-ResourceGroupName</span></span>
<span data-ttu-id="d373e-116">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d373e-116">The resource group name.</span></span>

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

### <span data-ttu-id="d373e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d373e-117">CommonParameters</span></span>
<span data-ttu-id="d373e-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d373e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d373e-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d373e-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d373e-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d373e-120">INPUTS</span></span>

### <span data-ttu-id="d373e-121">System. String</span><span class="sxs-lookup"><span data-stu-id="d373e-121">System.String</span></span>

## <span data-ttu-id="d373e-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d373e-122">OUTPUTS</span></span>

### <span data-ttu-id="d373e-123">System. String</span><span class="sxs-lookup"><span data-stu-id="d373e-123">System.String</span></span>

## <span data-ttu-id="d373e-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d373e-124">NOTES</span></span>

## <span data-ttu-id="d373e-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d373e-125">RELATED LINKS</span></span>

