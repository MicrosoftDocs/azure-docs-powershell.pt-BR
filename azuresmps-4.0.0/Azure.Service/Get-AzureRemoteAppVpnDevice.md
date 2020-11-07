---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: DF95285F-97F4-4064-8E27-EE6E93843E55
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0a14865c986bf6439df833a38f87835792a6e3c5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945626"
---
# <span data-ttu-id="84e30-101">Get-AzureRemoteAppVpnDevice</span><span class="sxs-lookup"><span data-stu-id="84e30-101">Get-AzureRemoteAppVpnDevice</span></span>

## <span data-ttu-id="84e30-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="84e30-102">SYNOPSIS</span></span>
<span data-ttu-id="84e30-103">Recupera informações sobre um dispositivo VPN.</span><span class="sxs-lookup"><span data-stu-id="84e30-103">Retrieves information about a VPN device.</span></span>

## <span data-ttu-id="84e30-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="84e30-104">SYNTAX</span></span>

```
Get-AzureRemoteAppVpnDevice [-VNetName] <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="84e30-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="84e30-105">DESCRIPTION</span></span>
<span data-ttu-id="84e30-106">O cmdlet **Get-AzureRemoteAppVpnDevice** recupera informações sobre um dispositivo de rede virtual privada (VPN).</span><span class="sxs-lookup"><span data-stu-id="84e30-106">The **Get-AzureRemoteAppVpnDevice** cmdlet retrieves information about a virtual private network (VPN) device.</span></span>

## <span data-ttu-id="84e30-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="84e30-107">EXAMPLES</span></span>

### <span data-ttu-id="84e30-108">Exemplo 1: retornar as configurações de dispositivo VPN disponíveis para uma rede virtual</span><span class="sxs-lookup"><span data-stu-id="84e30-108">Example 1: Return the available VPN device configurations for a virtual network</span></span>
```
PS C:\> Get-AzureRemoteVpnDevice -VNetName "ContosoVNet"


Name                   Platforms

----                   ---------

Cisco Systems, Inc.    {ASA 5500 Series Adaptive Security Appliances, ASR 1000 Series Aggregation Services Routers, ASR 1000 Series Aggregation Services Routers - Dynamic Routing, ISR Series Integrated Services Routers...} 

Juniper Networks, Inc. {SRX Series Routers, SRX Series Routers - Dynamic Routing, J Series Routers, J Series Routers - Dynamic Routing...} 

Microsoft Corporation  {RRAS}
```

<span data-ttu-id="84e30-109">Esse comando retorna as configurações de dispositivo VPN disponíveis para a rede virtual especificada.</span><span class="sxs-lookup"><span data-stu-id="84e30-109">This command returns the available VPN device configurations for the specified virtual network.</span></span>

## <span data-ttu-id="84e30-110">OS</span><span class="sxs-lookup"><span data-stu-id="84e30-110">PARAMETERS</span></span>

### <span data-ttu-id="84e30-111">-Perfil</span><span class="sxs-lookup"><span data-stu-id="84e30-111">-Profile</span></span>
<span data-ttu-id="84e30-112">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="84e30-112">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="84e30-113">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="84e30-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84e30-114">-VNetName</span><span class="sxs-lookup"><span data-stu-id="84e30-114">-VNetName</span></span>
<span data-ttu-id="84e30-115">Especifica o nome da rede virtual do Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="84e30-115">Specifies the name of the Azure RemoteApp virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="84e30-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84e30-116">CommonParameters</span></span>
<span data-ttu-id="84e30-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84e30-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84e30-118">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84e30-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84e30-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="84e30-119">INPUTS</span></span>

## <span data-ttu-id="84e30-120">EXIBE</span><span class="sxs-lookup"><span data-stu-id="84e30-120">OUTPUTS</span></span>

### <span data-ttu-id="84e30-121">System. String</span><span class="sxs-lookup"><span data-stu-id="84e30-121">System.String</span></span>

## <span data-ttu-id="84e30-122">INFORMA</span><span class="sxs-lookup"><span data-stu-id="84e30-122">NOTES</span></span>

## <span data-ttu-id="84e30-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="84e30-123">RELATED LINKS</span></span>

[<span data-ttu-id="84e30-124">Get-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="84e30-124">Get-AzureRemoteAppVNet</span></span>](./Get-AzureRemoteAppVNet.md)

[<span data-ttu-id="84e30-125">Get-AzureRemoteAppVpnDeviceConfigScript</span><span class="sxs-lookup"><span data-stu-id="84e30-125">Get-AzureRemoteAppVpnDeviceConfigScript</span></span>](./Get-AzureRemoteAppVpnDeviceConfigScript.md)


