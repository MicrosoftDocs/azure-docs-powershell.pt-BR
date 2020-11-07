---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 36DA2BF9-091E-4A2C-B5E1-07B4D2E482FC
online version: ''
schema: 2.0.0
ms.openlocfilehash: b73626681e4d089b3b4f20c72080159c31b1bf81
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946187"
---
# <span data-ttu-id="c1fb1-101">New-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="c1fb1-101">New-AzureVNetGateway</span></span>

## <span data-ttu-id="c1fb1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c1fb1-102">SYNOPSIS</span></span>
<span data-ttu-id="c1fb1-103">Cria um gateway VPN em uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="c1fb1-103">Creates a VPN gateway in a virtual network.</span></span>

## <span data-ttu-id="c1fb1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c1fb1-104">SYNTAX</span></span>

```
New-AzureVNetGateway -VNetName <String> [-GatewayType <String>] [-GatewaySKU <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c1fb1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c1fb1-105">DESCRIPTION</span></span>
<span data-ttu-id="c1fb1-106">O cmdlet **New-AzureVNetGateway** cria um gateway de rede virtual privada (VPN) em uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="c1fb1-106">The **New-AzureVNetGateway** cmdlet creates a virtual private network (VPN) gateway in a virtual network.</span></span>
<span data-ttu-id="c1fb1-107">Você também pode especificar a SKU do gateway, seja padrão, padrão ou HighPerformance.</span><span class="sxs-lookup"><span data-stu-id="c1fb1-107">You can also specify the SKU of the gateway, either Default, Standard, or HighPerformance.</span></span>
<span data-ttu-id="c1fb1-108">Você pode especificar o tipo, ou StaticRouting ou DynamicRouting.</span><span class="sxs-lookup"><span data-stu-id="c1fb1-108">You can specify the type, either StaticRouting or DynamicRouting.</span></span>

## <span data-ttu-id="c1fb1-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c1fb1-109">EXAMPLES</span></span>

### <span data-ttu-id="c1fb1-110">Exemplo 1: criar um gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="c1fb1-110">Example 1: Create a virtual network gateway</span></span>
```
PS C:\> New-AzureVNetGateway -VNetName "ContosoVN07" -GatewayType "DynamicRouting" -GatewaySKU "Default"
```

<span data-ttu-id="c1fb1-111">Esse comando cria um gateway de rede virtual para a rede virtual chamada ContosoVN07.</span><span class="sxs-lookup"><span data-stu-id="c1fb1-111">This command creates a virtual network gateway for the virtual network named ContosoVN07.</span></span>
<span data-ttu-id="c1fb1-112">O gateway é o SKU padrão e usa o roteamento dinâmico.</span><span class="sxs-lookup"><span data-stu-id="c1fb1-112">The gateway is the Default SKU and uses dynamic routing.</span></span>

## <span data-ttu-id="c1fb1-113">OS</span><span class="sxs-lookup"><span data-stu-id="c1fb1-113">PARAMETERS</span></span>

### <span data-ttu-id="c1fb1-114">-GatewaySKU</span><span class="sxs-lookup"><span data-stu-id="c1fb1-114">-GatewaySKU</span></span>
<span data-ttu-id="c1fb1-115">Especifica a SKU do gateway de rede virtual que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="c1fb1-115">Specifies the SKU of the virtual network gateway that this cmdlet creates.</span></span>
<span data-ttu-id="c1fb1-116">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="c1fb1-116">Valid values are:</span></span> 

- <span data-ttu-id="c1fb1-117">Assume</span><span class="sxs-lookup"><span data-stu-id="c1fb1-117">Default</span></span> 
- <span data-ttu-id="c1fb1-118">Oficial</span><span class="sxs-lookup"><span data-stu-id="c1fb1-118">Standard</span></span> 
- <span data-ttu-id="c1fb1-119">HighPerformance</span><span class="sxs-lookup"><span data-stu-id="c1fb1-119">HighPerformance</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1fb1-120">-Gatewaytype</span><span class="sxs-lookup"><span data-stu-id="c1fb1-120">-GatewayType</span></span>
<span data-ttu-id="c1fb1-121">Especifica o tipo de gateway que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="c1fb1-121">Specifies the type of gateway that this cmdlet creates.</span></span>
<span data-ttu-id="c1fb1-122">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="c1fb1-122">Valid values are:</span></span> 

- <span data-ttu-id="c1fb1-123">StaticRouting</span><span class="sxs-lookup"><span data-stu-id="c1fb1-123">StaticRouting</span></span> 
- <span data-ttu-id="c1fb1-124">DynamicRouting</span><span class="sxs-lookup"><span data-stu-id="c1fb1-124">DynamicRouting</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1fb1-125">-Perfil</span><span class="sxs-lookup"><span data-stu-id="c1fb1-125">-Profile</span></span>
<span data-ttu-id="c1fb1-126">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="c1fb1-126">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="c1fb1-127">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="c1fb1-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c1fb1-128">-VNetName</span><span class="sxs-lookup"><span data-stu-id="c1fb1-128">-VNetName</span></span>
<span data-ttu-id="c1fb1-129">Especifica a rede virtual na qual esse cmdlet adiciona um gateway virtual de rede.</span><span class="sxs-lookup"><span data-stu-id="c1fb1-129">Specifies the virtual network in which this cmdlet adds a virtual network gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1fb1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1fb1-130">CommonParameters</span></span>
<span data-ttu-id="c1fb1-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1fb1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1fb1-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1fb1-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1fb1-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c1fb1-133">INPUTS</span></span>

## <span data-ttu-id="c1fb1-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c1fb1-134">OUTPUTS</span></span>

## <span data-ttu-id="c1fb1-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c1fb1-135">NOTES</span></span>

## <span data-ttu-id="c1fb1-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c1fb1-136">RELATED LINKS</span></span>

[<span data-ttu-id="c1fb1-137">Get-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="c1fb1-137">Get-AzureVNetGateway</span></span>](./Get-AzureVNetGateway.md)

[<span data-ttu-id="c1fb1-138">Remove-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="c1fb1-138">Remove-AzureVNetGateway</span></span>](./Remove-AzureVNetGateway.md)

[<span data-ttu-id="c1fb1-139">Reset-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="c1fb1-139">Reset-AzureVNetGateway</span></span>](./Reset-AzureVNetGateway.md)

[<span data-ttu-id="c1fb1-140">Redimensionar-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="c1fb1-140">Resize-AzureVNetGateway</span></span>](./Resize-AzureVNetGateway.md)

[<span data-ttu-id="c1fb1-141">Set-AzureVNetGatewayKey</span><span class="sxs-lookup"><span data-stu-id="c1fb1-141">Set-AzureVNetGatewayKey</span></span>](./Set-AzureVNetGatewayKey.md)


