---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: B6881AEC-7DFD-43F8-92A9-7AB56323B86F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 36476b34f74c44facf84ba2246afd0b6d8e49007
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945994"
---
# <span data-ttu-id="fd682-101">New-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="fd682-101">New-AzureRemoteAppVNet</span></span>

## <span data-ttu-id="fd682-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fd682-102">SYNOPSIS</span></span>
<span data-ttu-id="fd682-103">Cria uma rede virtual do Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="fd682-103">Creates an Azure RemoteApp virtual network.</span></span>

## <span data-ttu-id="fd682-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fd682-104">SYNTAX</span></span>

```
New-AzureRemoteAppVNet -VNetName <String> -VirtualNetworkAddressSpace <String[]>
 -LocalNetworkAddressSpace <String[]> -DnsServerIpAddress <String[]> -VpnDeviceIpAddress <String>
 [-Location] <String> -GatewayType <GatewayType> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="fd682-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fd682-105">DESCRIPTION</span></span>
<span data-ttu-id="fd682-106">O cmdlet **New-AzureRemoteAppVNet** cria uma rede virtual do Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="fd682-106">The **New-AzureRemoteAppVNet** cmdlet creates an Azure RemoteApp virtual network.</span></span>

## <span data-ttu-id="fd682-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fd682-107">EXAMPLES</span></span>

### <span data-ttu-id="fd682-108">Exemplo 1: criar uma rede virtual</span><span class="sxs-lookup"><span data-stu-id="fd682-108">Example 1: Create a virtual network</span></span>
```
PS C:\> New-AzureRemoteAppVnet -VNetName "ContosoVNet" -DnsServerIpAddress "192.168.0.5" -LocalNetworkAddressSpace "192.168.0.0/24" -Location "Central US" -VirtualNetworkAddressSpace "10.10.0.0/24" -VpnDeviceIpAddress "131.107.33.200" -GatewayType StaticRouting

TrackingId

----------

b0ca9d1b-d1b9-4f24-9a08-5e021926587f
```

<span data-ttu-id="fd682-109">Esse comando cria uma rede virtual chamada ContosoVNet.</span><span class="sxs-lookup"><span data-stu-id="fd682-109">This command creates a virtual network named ContosoVNet.</span></span>

<span data-ttu-id="fd682-110">Para determinar o status da operação, use o cmdlet **Get-AzureRemoteAppOperationResult** com a ID de rastreamento que este cmdlet retorna.</span><span class="sxs-lookup"><span data-stu-id="fd682-110">To determine the status of the operation, use the **Get-AzureRemoteAppOperationResult** cmdlet with the tracking ID that this cmdlet returns.</span></span>

## <span data-ttu-id="fd682-111">OS</span><span class="sxs-lookup"><span data-stu-id="fd682-111">PARAMETERS</span></span>

### <span data-ttu-id="fd682-112">-DnsServerIpAddress</span><span class="sxs-lookup"><span data-stu-id="fd682-112">-DnsServerIpAddress</span></span>
<span data-ttu-id="fd682-113">Especifica uma matriz dos endereços IPv4 dos servidores DNS.</span><span class="sxs-lookup"><span data-stu-id="fd682-113">Specifies an array of the IPv4 addresses of the DNS servers.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fd682-114">-Gatewaytype</span><span class="sxs-lookup"><span data-stu-id="fd682-114">-GatewayType</span></span>
<span data-ttu-id="fd682-115">Especifica o tipo de roteamento de gateway a ser usado.</span><span class="sxs-lookup"><span data-stu-id="fd682-115">Specifies the type of gateway routing to use.</span></span>
<span data-ttu-id="fd682-116">Os valores aceitáveis para esse parâmetro são: StaticRouting ou DynamicRouting.</span><span class="sxs-lookup"><span data-stu-id="fd682-116">The acceptable values for this parameter are:  StaticRouting or DynamicRouting.</span></span>

```yaml
Type: GatewayType
Parameter Sets: (All)
Aliases: 
Accepted values: StaticRouting, DynamicRouting

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fd682-117">-LocalNetworkAddressSpace</span><span class="sxs-lookup"><span data-stu-id="fd682-117">-LocalNetworkAddressSpace</span></span>
<span data-ttu-id="fd682-118">Especifica uma matriz de cadeias de caracteres que especificam o espaço de endereço de rede local, em notação de roteamento interdomain sem classe (CIDR).</span><span class="sxs-lookup"><span data-stu-id="fd682-118">Specifies an array of strings that specify the local network address space, in Classless Interdomain Routing (CIDR) notation.</span></span>
<span data-ttu-id="fd682-119">Esse espaço de endereço não deve sobrepor o espaço de endereço de rede virtual que o parâmetro *VirtualNetworkAddressSpace* especifica.</span><span class="sxs-lookup"><span data-stu-id="fd682-119">This address space must not overlap with the virtual network address space that the *VirtualNetworkAddressSpace* parameter specifies.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fd682-120">-Local</span><span class="sxs-lookup"><span data-stu-id="fd682-120">-Location</span></span>
<span data-ttu-id="fd682-121">Especifica o local no qual criar a rede virtual.</span><span class="sxs-lookup"><span data-stu-id="fd682-121">Specifies the location in which to create the virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fd682-122">-Perfil</span><span class="sxs-lookup"><span data-stu-id="fd682-122">-Profile</span></span>
<span data-ttu-id="fd682-123">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="fd682-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="fd682-124">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="fd682-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="fd682-125">-VirtualNetworkAddressSpace</span><span class="sxs-lookup"><span data-stu-id="fd682-125">-VirtualNetworkAddressSpace</span></span>
<span data-ttu-id="fd682-126">Especifica uma matriz de cadeia de caracteres que especifica o espaço de endereço de rede virtual na notação CIDR.</span><span class="sxs-lookup"><span data-stu-id="fd682-126">Specifies an array of string that specify the virtual network address space in CIDR notation.</span></span>
<span data-ttu-id="fd682-127">Isso deve estar no intervalo de endereços IP privados e não pode sobrepor-se com o espaço de endereço de rede local que o parâmetro *LocalNetworkAddressSpace* especifica.</span><span class="sxs-lookup"><span data-stu-id="fd682-127">This must be in the private IP address range and cannot overlap with the local network address space that the *LocalNetworkAddressSpace* parameter specifies.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fd682-128">-VNetName</span><span class="sxs-lookup"><span data-stu-id="fd682-128">-VNetName</span></span>
<span data-ttu-id="fd682-129">Especifica o nome da rede virtual do Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="fd682-129">Specifies the name of the Azure RemoteApp virtual network.</span></span>

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

### <span data-ttu-id="fd682-130">-VpnDeviceIpAddress</span><span class="sxs-lookup"><span data-stu-id="fd682-130">-VpnDeviceIpAddress</span></span>
<span data-ttu-id="fd682-131">Especifica o endereço do dispositivo de rede virtual privada (VPN).</span><span class="sxs-lookup"><span data-stu-id="fd682-131">Specifies the address of the virtual private network (VPN) device.</span></span>
<span data-ttu-id="fd682-132">Deve ser um endereço público.</span><span class="sxs-lookup"><span data-stu-id="fd682-132">This must be a public-facing address.</span></span>

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

### <span data-ttu-id="fd682-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd682-133">CommonParameters</span></span>
<span data-ttu-id="fd682-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd682-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd682-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd682-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd682-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fd682-136">INPUTS</span></span>

## <span data-ttu-id="fd682-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fd682-137">OUTPUTS</span></span>

## <span data-ttu-id="fd682-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fd682-138">NOTES</span></span>

## <span data-ttu-id="fd682-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fd682-139">RELATED LINKS</span></span>

[<span data-ttu-id="fd682-140">Get-AzureRemoteAppOperationResult</span><span class="sxs-lookup"><span data-stu-id="fd682-140">Get-AzureRemoteAppOperationResult</span></span>](./Get-AzureRemoteAppOperationResult.md)

[<span data-ttu-id="fd682-141">Get-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="fd682-141">Get-AzureRemoteAppVNet</span></span>](./Get-AzureRemoteAppVNet.md)

[<span data-ttu-id="fd682-142">Remove-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="fd682-142">Remove-AzureRemoteAppVNet</span></span>](./Remove-AzureRemoteAppVNet.md)

[<span data-ttu-id="fd682-143">Set-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="fd682-143">Set-AzureRemoteAppVNet</span></span>](./Set-AzureRemoteAppVNet.md)


