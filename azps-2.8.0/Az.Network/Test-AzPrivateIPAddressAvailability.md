---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0780CB09-9C3B-468A-A718-3A646FE3D152
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-azprivateipaddressavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzPrivateIPAddressAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzPrivateIPAddressAvailability.md
ms.openlocfilehash: 3130aec4a5032fd62423aa35dec73d7acd6e14b2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772694"
---
# <span data-ttu-id="0043a-101">Test-AzPrivateIPAddressAvailability</span><span class="sxs-lookup"><span data-stu-id="0043a-101">Test-AzPrivateIPAddressAvailability</span></span>

## <span data-ttu-id="0043a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0043a-102">SYNOPSIS</span></span>
<span data-ttu-id="0043a-103">Teste a disponibilidade de um endereço IP privado em uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="0043a-103">Test availability of a private IP address in a virtual network.</span></span>

## <span data-ttu-id="0043a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0043a-104">SYNTAX</span></span>

### <span data-ttu-id="0043a-105">TestByResource</span><span class="sxs-lookup"><span data-stu-id="0043a-105">TestByResource</span></span>
```
Test-AzPrivateIPAddressAvailability -VirtualNetwork <PSVirtualNetwork> -IPAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0043a-106">TestByResourceId</span><span class="sxs-lookup"><span data-stu-id="0043a-106">TestByResourceId</span></span>
```
Test-AzPrivateIPAddressAvailability -ResourceGroupName <String> -VirtualNetworkName <String>
 -IPAddress <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0043a-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0043a-107">DESCRIPTION</span></span>
<span data-ttu-id="0043a-108">O cmdlet **Test-AzPrivateIPAddressAvailability** testa se um endereço IP privado especificado está disponível em uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="0043a-108">The **Test-AzPrivateIPAddressAvailability** cmdlet tests whether a specified private IP address is available in a virtual network.</span></span>
<span data-ttu-id="0043a-109">Esse cmdlet retorna uma lista de endereços IP particulares disponíveis se o endereço IP particular solicitado for tirado.</span><span class="sxs-lookup"><span data-stu-id="0043a-109">This cmdlet returns a list of available private IP addresses if the requested private IP address is taken.</span></span>

## <span data-ttu-id="0043a-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0043a-110">EXAMPLES</span></span>

### <span data-ttu-id="0043a-111">Exemplo 1: testar se um endereço IP está disponível usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="0043a-111">Example 1: Test whether an IP address is available using the pipeline</span></span>
```
PS C:\>Get-AzVirtualNetwork -Name $vnetName -ResourceGroupName $rgname | Test-AzPrivateIPAddressAvailability -IPAddress "10.0.1.10"
```

<span data-ttu-id="0043a-112">Este comando obtém uma rede virtual e usa o operador pipeline para passá-la para **Test-AzPrivateIPAddressAvailability** , o que testa se o endereço IP privado especificado está disponível.</span><span class="sxs-lookup"><span data-stu-id="0043a-112">This command gets a virtual network and uses the pipeline operator to pass it to **Test-AzPrivateIPAddressAvailability** , which tests whether the specified private IP address is available.</span></span>

## <span data-ttu-id="0043a-113">OS</span><span class="sxs-lookup"><span data-stu-id="0043a-113">PARAMETERS</span></span>

### <span data-ttu-id="0043a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0043a-114">-DefaultProfile</span></span>
<span data-ttu-id="0043a-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0043a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0043a-116">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="0043a-116">-IPAddress</span></span>
<span data-ttu-id="0043a-117">Especifica o endereço IP para testar.</span><span class="sxs-lookup"><span data-stu-id="0043a-117">Specifies the IP address to test.</span></span>

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

### <span data-ttu-id="0043a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0043a-118">-ResourceGroupName</span></span>
<span data-ttu-id="0043a-119">Especifica o nome do grupo de recursos para a rede virtual.</span><span class="sxs-lookup"><span data-stu-id="0043a-119">Specifies the name of the resource group for the virtual network.</span></span>

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

### <span data-ttu-id="0043a-120">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="0043a-120">-VirtualNetwork</span></span>
<span data-ttu-id="0043a-121">Especifica um objeto **PSVirtualNetwork** .</span><span class="sxs-lookup"><span data-stu-id="0043a-121">Specifies a **PSVirtualNetwork** object.</span></span>

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

### <span data-ttu-id="0043a-122">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="0043a-122">-VirtualNetworkName</span></span>
<span data-ttu-id="0043a-123">Especifica o nome da rede virtual.</span><span class="sxs-lookup"><span data-stu-id="0043a-123">Specifies the name of the virtual network.</span></span>

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

### <span data-ttu-id="0043a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0043a-124">CommonParameters</span></span>
<span data-ttu-id="0043a-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0043a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0043a-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0043a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0043a-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0043a-127">INPUTS</span></span>

### <span data-ttu-id="0043a-128">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="0043a-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="0043a-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0043a-129">OUTPUTS</span></span>

### <span data-ttu-id="0043a-130">Microsoft. Azure. Commands. Network. Models. PSIPAddressAvailabilityResult</span><span class="sxs-lookup"><span data-stu-id="0043a-130">Microsoft.Azure.Commands.Network.Models.PSIPAddressAvailabilityResult</span></span>

## <span data-ttu-id="0043a-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0043a-131">NOTES</span></span>

## <span data-ttu-id="0043a-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0043a-132">RELATED LINKS</span></span>

[<span data-ttu-id="0043a-133">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="0043a-133">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)


