---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewaysupportedvpndevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkGatewaySupportedVpnDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkGatewaySupportedVpnDevice.md
ms.openlocfilehash: 794f432b06c693d6758603975a98ca6b2f5e3511
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775466"
---
# <span data-ttu-id="a52d2-101">Get-AzVirtualNetworkGatewaySupportedVpnDevice</span><span class="sxs-lookup"><span data-stu-id="a52d2-101">Get-AzVirtualNetworkGatewaySupportedVpnDevice</span></span>

## <span data-ttu-id="a52d2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a52d2-102">SYNOPSIS</span></span>
<span data-ttu-id="a52d2-103">Este commandlet retorna uma lista de marcas de dispositivo VPN, modelos e versões de firmware com suporte.</span><span class="sxs-lookup"><span data-stu-id="a52d2-103">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

## <span data-ttu-id="a52d2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a52d2-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewaySupportedVpnDevice -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a52d2-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a52d2-105">DESCRIPTION</span></span>
<span data-ttu-id="a52d2-106">Este commandlet retorna uma lista de marcas de dispositivo VPN, modelos e versões de firmware com suporte.</span><span class="sxs-lookup"><span data-stu-id="a52d2-106">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

## <span data-ttu-id="a52d2-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a52d2-107">EXAMPLES</span></span>

### <span data-ttu-id="a52d2-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a52d2-108">Example 1</span></span>
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

<span data-ttu-id="a52d2-109">Retorna a lista de marcas de dispositivo VPN, modelos e versões de firmware com suporte:</span><span class="sxs-lookup"><span data-stu-id="a52d2-109">Returns list of supported VPN device brands, models and firmware versions:</span></span>
<?xml version="1.0" encoding="utf-8"?>
<RpVpnDeviceList version="1.0">
  <Vendor name="Cisco-Test">
    <DeviceFamily name="IOS-Test">
       <FirmwareVersion name="20" />
    </DeviceFamily>
  </Vendor>
</RpVpnDeviceList>

## <span data-ttu-id="a52d2-110">OS</span><span class="sxs-lookup"><span data-stu-id="a52d2-110">PARAMETERS</span></span>

### <span data-ttu-id="a52d2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a52d2-111">-DefaultProfile</span></span>
<span data-ttu-id="a52d2-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a52d2-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a52d2-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="a52d2-113">-Name</span></span>
<span data-ttu-id="a52d2-114">O nome do gateway da rede virtual.</span><span class="sxs-lookup"><span data-stu-id="a52d2-114">The virtual network gateway name.</span></span>

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

### <span data-ttu-id="a52d2-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a52d2-115">-ResourceGroupName</span></span>
<span data-ttu-id="a52d2-116">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a52d2-116">The resource group name.</span></span>

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

### <span data-ttu-id="a52d2-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a52d2-117">CommonParameters</span></span>
<span data-ttu-id="a52d2-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a52d2-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a52d2-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a52d2-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a52d2-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a52d2-120">INPUTS</span></span>

### <span data-ttu-id="a52d2-121">System. String</span><span class="sxs-lookup"><span data-stu-id="a52d2-121">System.String</span></span>

## <span data-ttu-id="a52d2-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a52d2-122">OUTPUTS</span></span>

### <span data-ttu-id="a52d2-123">System. String</span><span class="sxs-lookup"><span data-stu-id="a52d2-123">System.String</span></span>

## <span data-ttu-id="a52d2-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a52d2-124">NOTES</span></span>

## <span data-ttu-id="a52d2-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a52d2-125">RELATED LINKS</span></span>

