---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 97B96661-E60A-4505-AD06-D2A541DB820E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 19f7b09d26df88591e03acf8b01842efdead05e2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946052"
---
# <span data-ttu-id="b359e-101">Set-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="b359e-101">Set-AzureRemoteAppVNet</span></span>

## <span data-ttu-id="b359e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b359e-102">SYNOPSIS</span></span>
<span data-ttu-id="b359e-103">Define as propriedades de uma rede virtual do Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="b359e-103">Sets the properties of an Azure RemoteApp virtual network.</span></span>

## <span data-ttu-id="b359e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b359e-104">SYNTAX</span></span>

```
Set-AzureRemoteAppVNet -VNetName <String> [-VirtualNetworkAddressSpace <String[]>]
 [-LocalNetworkAddressSpace <String[]>] [-DnsServerIpAddress <String[]>] [-VpnDeviceIpAddress <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b359e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b359e-105">DESCRIPTION</span></span>
<span data-ttu-id="b359e-106">O cmdlet **set-AzureRemoteAppVNet** define as propriedades de uma rede virtual do Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="b359e-106">The **Set-AzureRemoteAppVNet** cmdlet sets the properties of an Azure RemoteApp virtual network.</span></span>

## <span data-ttu-id="b359e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b359e-107">EXAMPLES</span></span>

### <span data-ttu-id="b359e-108">Exemplo 1: definir as propriedades de uma rede virtual</span><span class="sxs-lookup"><span data-stu-id="b359e-108">Example 1: Set the properties of a virtual network</span></span>
```
PS C:\> Set-AzureRemoteAppVnet -VNetName "ContosoVNet" -DnsServerIpAddress "131.253.33.200" -LocalNetworkAddressSpace "192.168.0.0/24" -VirtualNetworkAddressSpace "10.10.0.0/24" -VpnDeviceIpAddress "131.253.33.200"
```

<span data-ttu-id="b359e-109">Este comando define as propriedades de uma rede virtual chamada ContosoVNet.</span><span class="sxs-lookup"><span data-stu-id="b359e-109">This command sets the properties of a virtual network named ContosoVNet.</span></span>

## <span data-ttu-id="b359e-110">OS</span><span class="sxs-lookup"><span data-stu-id="b359e-110">PARAMETERS</span></span>

### <span data-ttu-id="b359e-111">-DnsServerIpAddress</span><span class="sxs-lookup"><span data-stu-id="b359e-111">-DnsServerIpAddress</span></span>
<span data-ttu-id="b359e-112">Especifica os endereços IPv4 dos servidores DNS.</span><span class="sxs-lookup"><span data-stu-id="b359e-112">Specifies the IPv4 addresses of the DNS servers.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b359e-113">-LocalNetworkAddressSpace</span><span class="sxs-lookup"><span data-stu-id="b359e-113">-LocalNetworkAddressSpace</span></span>
<span data-ttu-id="b359e-114">Especifica o espaço de endereço de rede local, na notação de classe Inter-Domain roteamento (CIDR).</span><span class="sxs-lookup"><span data-stu-id="b359e-114">Specifies the local network address space, in Classes Inter-Domain Routing (CIDR) notation.</span></span>
<span data-ttu-id="b359e-115">Isso não deve sobrepor o espaço de endereço de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="b359e-115">This must not overlap the virtual network address space.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b359e-116">-Perfil</span><span class="sxs-lookup"><span data-stu-id="b359e-116">-Profile</span></span>
<span data-ttu-id="b359e-117">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="b359e-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b359e-118">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="b359e-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b359e-119">-VirtualNetworkAddressSpace</span><span class="sxs-lookup"><span data-stu-id="b359e-119">-VirtualNetworkAddressSpace</span></span>
<span data-ttu-id="b359e-120">Especifica o espaço de endereço de rede virtual na notação CIDR.</span><span class="sxs-lookup"><span data-stu-id="b359e-120">Specifies the virtual network address space in CIDR notation.</span></span>
<span data-ttu-id="b359e-121">Isso deve estar no intervalo de endereços IP privados e não pode sobrepor o espaço de endereço de rede local.</span><span class="sxs-lookup"><span data-stu-id="b359e-121">This must be in the private IP address range and cannot overlap the local network address space.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b359e-122">-VNetName</span><span class="sxs-lookup"><span data-stu-id="b359e-122">-VNetName</span></span>
<span data-ttu-id="b359e-123">Especifica o nome da rede virtual do Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="b359e-123">Specifies the name of the Azure RemoteApp virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b359e-124">-VpnDeviceIpAddress</span><span class="sxs-lookup"><span data-stu-id="b359e-124">-VpnDeviceIpAddress</span></span>
<span data-ttu-id="b359e-125">Especifica o endereço do dispositivo de rede virtual privada (VPN).</span><span class="sxs-lookup"><span data-stu-id="b359e-125">Specifies the address of the Virtual Private Network (VPN) device.</span></span>
<span data-ttu-id="b359e-126">Deve ser um endereço público.</span><span class="sxs-lookup"><span data-stu-id="b359e-126">This must be a public-facing address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b359e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b359e-127">CommonParameters</span></span>
<span data-ttu-id="b359e-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b359e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b359e-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b359e-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b359e-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b359e-130">INPUTS</span></span>

## <span data-ttu-id="b359e-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b359e-131">OUTPUTS</span></span>

## <span data-ttu-id="b359e-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b359e-132">NOTES</span></span>

## <span data-ttu-id="b359e-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b359e-133">RELATED LINKS</span></span>

[<span data-ttu-id="b359e-134">Get-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="b359e-134">Get-AzureRemoteAppVNet</span></span>](./Get-AzureRemoteAppVNet.md)


