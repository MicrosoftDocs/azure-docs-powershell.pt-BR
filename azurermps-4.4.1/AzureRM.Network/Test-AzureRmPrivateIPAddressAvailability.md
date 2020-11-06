---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 0780CB09-9C3B-468A-A718-3A646FE3D152
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmPrivateIPAddressAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmPrivateIPAddressAvailability.md
ms.openlocfilehash: 880e079d5facec2edc20f38d7d1e1d4c9ba41e41
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430716"
---
# <span data-ttu-id="e38fe-101">Test-AzureRmPrivateIPAddressAvailability</span><span class="sxs-lookup"><span data-stu-id="e38fe-101">Test-AzureRmPrivateIPAddressAvailability</span></span>

## <span data-ttu-id="e38fe-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e38fe-102">SYNOPSIS</span></span>
<span data-ttu-id="e38fe-103">Teste a disponibilidade de um endereço IP privado em uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="e38fe-103">Test availability of a private IP address in a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e38fe-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e38fe-104">SYNTAX</span></span>

### <span data-ttu-id="e38fe-105">TestByResource</span><span class="sxs-lookup"><span data-stu-id="e38fe-105">TestByResource</span></span>
```
Test-AzureRmPrivateIPAddressAvailability -VirtualNetwork <PSVirtualNetwork> -IPAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e38fe-106">TestByResourceId</span><span class="sxs-lookup"><span data-stu-id="e38fe-106">TestByResourceId</span></span>
```
Test-AzureRmPrivateIPAddressAvailability -ResourceGroupName <String> -VirtualNetworkName <String>
 -IPAddress <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e38fe-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e38fe-107">DESCRIPTION</span></span>
<span data-ttu-id="e38fe-108">O cmdlet **Test-AzureRmPrivateIPAddressAvailability** testa se um endereço IP privado especificado está disponível em uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="e38fe-108">The **Test-AzureRmPrivateIPAddressAvailability** cmdlet tests whether a specified private IP address is available in a virtual network.</span></span>
<span data-ttu-id="e38fe-109">Esse cmdlet retorna uma lista de endereços IP particulares disponíveis se o endereço IP particular solicitado for tirado.</span><span class="sxs-lookup"><span data-stu-id="e38fe-109">This cmdlet returns a list of available private IP addresses if the requested private IP address is taken.</span></span>

## <span data-ttu-id="e38fe-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e38fe-110">EXAMPLES</span></span>

### <span data-ttu-id="e38fe-111">Exemplo 1: testar se um endereço IP está disponível usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="e38fe-111">Example 1: Test whether an IP address is available using the pipeline</span></span>
```
PS C:\>Get-AzureRmVirtualNetwork -Name $vnetName -ResourceGroupName $rgname | Test-AzureRmPrivateIPAddressAvailability -IPAddress "10.0.1.10"
```

<span data-ttu-id="e38fe-112">Este comando obtém uma rede virtual e usa o operador pipeline para passá-la para **Test-AzureRmPrivateIPAddressAvailability** , o que testa se o endereço IP privado especificado está disponível.</span><span class="sxs-lookup"><span data-stu-id="e38fe-112">This command gets a virtual network and uses the pipeline operator to pass it to **Test-AzureRmPrivateIPAddressAvailability** , which tests whether the specified private IP address is available.</span></span>

## <span data-ttu-id="e38fe-113">OS</span><span class="sxs-lookup"><span data-stu-id="e38fe-113">PARAMETERS</span></span>

### <span data-ttu-id="e38fe-114">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="e38fe-114">-IPAddress</span></span>
<span data-ttu-id="e38fe-115">Especifica o endereço IP para testar.</span><span class="sxs-lookup"><span data-stu-id="e38fe-115">Specifies the IP address to test.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e38fe-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e38fe-116">-ResourceGroupName</span></span>
<span data-ttu-id="e38fe-117">Especifica o nome do grupo de recursos para a rede virtual.</span><span class="sxs-lookup"><span data-stu-id="e38fe-117">Specifies the name of the resource group for the virtual network.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e38fe-118">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e38fe-118">-VirtualNetwork</span></span>
<span data-ttu-id="e38fe-119">Especifica um objeto **PSVirtualNetwork** .</span><span class="sxs-lookup"><span data-stu-id="e38fe-119">Specifies a **PSVirtualNetwork** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork
Parameter Sets: TestByResource
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e38fe-120">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="e38fe-120">-VirtualNetworkName</span></span>
<span data-ttu-id="e38fe-121">Especifica o nome da rede virtual.</span><span class="sxs-lookup"><span data-stu-id="e38fe-121">Specifies the name of the virtual network.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e38fe-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e38fe-122">-DefaultProfile</span></span>
<span data-ttu-id="e38fe-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e38fe-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e38fe-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e38fe-124">CommonParameters</span></span>
<span data-ttu-id="e38fe-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e38fe-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e38fe-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e38fe-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e38fe-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e38fe-127">INPUTS</span></span>

### <span data-ttu-id="e38fe-128">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e38fe-128">PSVirtualNetwork</span></span>
<span data-ttu-id="e38fe-129">O parâmetro ' VirtualNetwork ' aceita o valor do tipo ' PSVirtualNetwork ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="e38fe-129">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="e38fe-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e38fe-130">OUTPUTS</span></span>

### <span data-ttu-id="e38fe-131">Microsoft. Azure. Commands. Network. Models. PSIPAddressAvailabilityResult</span><span class="sxs-lookup"><span data-stu-id="e38fe-131">Microsoft.Azure.Commands.Network.Models.PSIPAddressAvailabilityResult</span></span>

## <span data-ttu-id="e38fe-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e38fe-132">NOTES</span></span>

## <span data-ttu-id="e38fe-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e38fe-133">RELATED LINKS</span></span>

[<span data-ttu-id="e38fe-134">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e38fe-134">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)


