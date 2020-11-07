---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 5765F6BD-38BC-451B-85C5-F5D1A5AF2831
online version: ''
schema: 2.0.0
ms.openlocfilehash: 91e5e226cfe4fc4cb27d2df73eb4da4c12045510
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946087"
---
# <span data-ttu-id="9971c-101">Resize-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="9971c-101">Resize-AzureVNetGateway</span></span>

## <span data-ttu-id="9971c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9971c-102">SYNOPSIS</span></span>
<span data-ttu-id="9971c-103">Redimensiona um gateway VPN.</span><span class="sxs-lookup"><span data-stu-id="9971c-103">Resizes a VPN gateway.</span></span>

## <span data-ttu-id="9971c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9971c-104">SYNTAX</span></span>

```
Resize-AzureVNetGateway -VNetName <String> -GatewaySKU <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="9971c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9971c-105">DESCRIPTION</span></span>
<span data-ttu-id="9971c-106">O cmdlet **Resize-AzureVNetGateway** redimensiona um gateway de rede virtual privada (VPN) de rede virtual para um SKU diferente.</span><span class="sxs-lookup"><span data-stu-id="9971c-106">The **Resize-AzureVNetGateway** cmdlet resizes a virtual network virtual private network (VPN) gateway to a different SKU.</span></span>
<span data-ttu-id="9971c-107">Os SKUs válidos para um gateway de rede virtual são padrão, padrão e HighPerformance.</span><span class="sxs-lookup"><span data-stu-id="9971c-107">Valid SKUs for a virtual network gateway are Default, Standard, and HighPerformance.</span></span>

## <span data-ttu-id="9971c-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9971c-108">EXAMPLES</span></span>

### <span data-ttu-id="9971c-109">Exemplo 1: alterar a SKU de um gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="9971c-109">Example 1: Change the SKU for a virtual network gateway</span></span>
```
PS C:\> Resize-AzureVNetGateway -VNetName "ContosoVN07" -GatewaySKU "HighPerformance"
```

<span data-ttu-id="9971c-110">Esse comando altera a SKU do gateway de rede virtual para a rede virtual chamada ContosoVN07 para HighPerformance.</span><span class="sxs-lookup"><span data-stu-id="9971c-110">This command changes the SKU of the virtual network gateway for the virtual network named ContosoVN07 to HighPerformance.</span></span>

## <span data-ttu-id="9971c-111">OS</span><span class="sxs-lookup"><span data-stu-id="9971c-111">PARAMETERS</span></span>

### <span data-ttu-id="9971c-112">-GatewaySKU</span><span class="sxs-lookup"><span data-stu-id="9971c-112">-GatewaySKU</span></span>
<span data-ttu-id="9971c-113">Especifica a SKU para a qual esse cmdlet redimensiona o gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="9971c-113">Specifies the SKU to which this cmdlet resizes virtual network gateway.</span></span>
<span data-ttu-id="9971c-114">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="9971c-114">Valid values are:</span></span> 

- <span data-ttu-id="9971c-115">Assume</span><span class="sxs-lookup"><span data-stu-id="9971c-115">Default</span></span> 
- <span data-ttu-id="9971c-116">Oficial</span><span class="sxs-lookup"><span data-stu-id="9971c-116">Standard</span></span> 
- <span data-ttu-id="9971c-117">HighPerformance</span><span class="sxs-lookup"><span data-stu-id="9971c-117">HighPerformance</span></span>

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

### <span data-ttu-id="9971c-118">-Perfil</span><span class="sxs-lookup"><span data-stu-id="9971c-118">-Profile</span></span>
<span data-ttu-id="9971c-119">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="9971c-119">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="9971c-120">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="9971c-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9971c-121">-VNetName</span><span class="sxs-lookup"><span data-stu-id="9971c-121">-VNetName</span></span>
<span data-ttu-id="9971c-122">Especifica a rede virtual na qual esse cmdlet redimensiona um gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="9971c-122">Specifies the virtual network in which this cmdlet resizes a virtual network gateway.</span></span>

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

### <span data-ttu-id="9971c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9971c-123">CommonParameters</span></span>
<span data-ttu-id="9971c-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9971c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9971c-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9971c-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9971c-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9971c-126">INPUTS</span></span>

## <span data-ttu-id="9971c-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9971c-127">OUTPUTS</span></span>

## <span data-ttu-id="9971c-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9971c-128">NOTES</span></span>

## <span data-ttu-id="9971c-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9971c-129">RELATED LINKS</span></span>

[<span data-ttu-id="9971c-130">Get-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="9971c-130">Get-AzureVNetGateway</span></span>](./Get-AzureVNetGateway.md)

[<span data-ttu-id="9971c-131">New-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="9971c-131">New-AzureVNetGateway</span></span>](./New-AzureVNetGateway.md)

[<span data-ttu-id="9971c-132">Remove-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="9971c-132">Remove-AzureVNetGateway</span></span>](./Remove-AzureVNetGateway.md)

[<span data-ttu-id="9971c-133">Reset-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="9971c-133">Reset-AzureVNetGateway</span></span>](./Reset-AzureVNetGateway.md)

[<span data-ttu-id="9971c-134">Set-AzureVNetGatewayKey</span><span class="sxs-lookup"><span data-stu-id="9971c-134">Set-AzureVNetGatewayKey</span></span>](./Set-AzureVNetGatewayKey.md)


