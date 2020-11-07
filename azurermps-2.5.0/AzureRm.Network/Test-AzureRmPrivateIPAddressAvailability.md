---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 0780CB09-9C3B-468A-A718-3A646FE3D152
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/test-azurermprivateipaddressavailability
schema: 2.0.0
ms.openlocfilehash: 73924c1d1308a4cf457033e27e49ad7f9e19392e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785434"
---
# <span data-ttu-id="59a91-101">Test-AzureRmPrivateIPAddressAvailability</span><span class="sxs-lookup"><span data-stu-id="59a91-101">Test-AzureRmPrivateIPAddressAvailability</span></span>

## <span data-ttu-id="59a91-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="59a91-102">SYNOPSIS</span></span>
<span data-ttu-id="59a91-103">Teste a disponibilidade de um endereço IP privado em uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="59a91-103">Test availability of a private IP address in a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="59a91-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="59a91-104">SYNTAX</span></span>

### <span data-ttu-id="59a91-105">TestByResource</span><span class="sxs-lookup"><span data-stu-id="59a91-105">TestByResource</span></span>
```
Test-AzureRmPrivateIPAddressAvailability -VirtualNetwork <PSVirtualNetwork> -IPAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="59a91-106">TestByResourceId</span><span class="sxs-lookup"><span data-stu-id="59a91-106">TestByResourceId</span></span>
```
Test-AzureRmPrivateIPAddressAvailability -ResourceGroupName <String> -VirtualNetworkName <String>
 -IPAddress <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59a91-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="59a91-107">DESCRIPTION</span></span>
<span data-ttu-id="59a91-108">O cmdlet **Test-AzureRmPrivateIPAddressAvailability** testa se um endereço IP privado especificado está disponível em uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="59a91-108">The **Test-AzureRmPrivateIPAddressAvailability** cmdlet tests whether a specified private IP address is available in a virtual network.</span></span>
<span data-ttu-id="59a91-109">Esse cmdlet retorna uma lista de endereços IP particulares disponíveis se o endereço IP particular solicitado for tirado.</span><span class="sxs-lookup"><span data-stu-id="59a91-109">This cmdlet returns a list of available private IP addresses if the requested private IP address is taken.</span></span>

## <span data-ttu-id="59a91-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="59a91-110">EXAMPLES</span></span>

### <span data-ttu-id="59a91-111">Exemplo 1: testar se um endereço IP está disponível usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="59a91-111">Example 1: Test whether an IP address is available using the pipeline</span></span>
```
PS C:\>Get-AzureRmVirtualNetwork -Name $vnetName -ResourceGroupName $rgname | Test-AzureRmPrivateIPAddressAvailability -IPAddress "10.0.1.10"
```

<span data-ttu-id="59a91-112">Este comando obtém uma rede virtual e usa o operador pipeline para passá-la para **Test-AzureRmPrivateIPAddressAvailability** , o que testa se o endereço IP privado especificado está disponível.</span><span class="sxs-lookup"><span data-stu-id="59a91-112">This command gets a virtual network and uses the pipeline operator to pass it to **Test-AzureRmPrivateIPAddressAvailability** , which tests whether the specified private IP address is available.</span></span>

## <span data-ttu-id="59a91-113">OS</span><span class="sxs-lookup"><span data-stu-id="59a91-113">PARAMETERS</span></span>

### <span data-ttu-id="59a91-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59a91-114">-DefaultProfile</span></span>
<span data-ttu-id="59a91-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="59a91-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="59a91-116">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="59a91-116">-IPAddress</span></span>
<span data-ttu-id="59a91-117">Especifica o endereço IP para testar.</span><span class="sxs-lookup"><span data-stu-id="59a91-117">Specifies the IP address to test.</span></span>

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

### <span data-ttu-id="59a91-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59a91-118">-ResourceGroupName</span></span>
<span data-ttu-id="59a91-119">Especifica o nome do grupo de recursos para a rede virtual.</span><span class="sxs-lookup"><span data-stu-id="59a91-119">Specifies the name of the resource group for the virtual network.</span></span>

```yaml
Type: String
Parameter Sets: TestByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59a91-120">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="59a91-120">-VirtualNetwork</span></span>
<span data-ttu-id="59a91-121">Especifica um objeto **PSVirtualNetwork** .</span><span class="sxs-lookup"><span data-stu-id="59a91-121">Specifies a **PSVirtualNetwork** object.</span></span>

```yaml
Type: PSVirtualNetwork
Parameter Sets: TestByResource
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="59a91-122">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="59a91-122">-VirtualNetworkName</span></span>
<span data-ttu-id="59a91-123">Especifica o nome da rede virtual.</span><span class="sxs-lookup"><span data-stu-id="59a91-123">Specifies the name of the virtual network.</span></span>

```yaml
Type: String
Parameter Sets: TestByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59a91-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59a91-124">CommonParameters</span></span>
<span data-ttu-id="59a91-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59a91-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59a91-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59a91-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59a91-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="59a91-127">INPUTS</span></span>

### <span data-ttu-id="59a91-128">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="59a91-128">PSVirtualNetwork</span></span>
<span data-ttu-id="59a91-129">O parâmetro ' VirtualNetwork ' aceita o valor do tipo ' PSVirtualNetwork ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="59a91-129">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="59a91-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="59a91-130">OUTPUTS</span></span>

### <span data-ttu-id="59a91-131">Microsoft. Azure. Commands. Network. Models. PSIPAddressAvailabilityResult</span><span class="sxs-lookup"><span data-stu-id="59a91-131">Microsoft.Azure.Commands.Network.Models.PSIPAddressAvailabilityResult</span></span>

## <span data-ttu-id="59a91-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="59a91-132">NOTES</span></span>

## <span data-ttu-id="59a91-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="59a91-133">RELATED LINKS</span></span>

[<span data-ttu-id="59a91-134">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="59a91-134">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)


