---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azipconfigurationbgppeeringaddressobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpConfigurationBgpPeeringAddressObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpConfigurationBgpPeeringAddressObject.md
ms.openlocfilehash: 2a31aa9db3264dd24c6d77bdad7b10d6ecad10b1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94111575"
---
# <span data-ttu-id="ec8f6-101">New-AzIpConfigurationBgpPeeringAddressObject</span><span class="sxs-lookup"><span data-stu-id="ec8f6-101">New-AzIpConfigurationBgpPeeringAddressObject</span></span>

## <span data-ttu-id="ec8f6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ec8f6-102">SYNOPSIS</span></span>
<span data-ttu-id="ec8f6-103">Cria um novo IpconfigurationBgpPeeringAddressObject</span><span class="sxs-lookup"><span data-stu-id="ec8f6-103">creates a new IpconfigurationBgpPeeringAddressObject</span></span>

## <span data-ttu-id="ec8f6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ec8f6-104">SYNTAX</span></span>

### <span data-ttu-id="ec8f6-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="ec8f6-105">Default (Default)</span></span>
```
New-AzIpConfigurationBgpPeeringAddressObject -IpConfigurationId <String>
 -CustomAddress <System.Collections.Generic.List`1[System.String]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```
## <span data-ttu-id="ec8f6-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ec8f6-106">DESCRIPTION</span></span>
<span data-ttu-id="ec8f6-107">O **New-AzIpConfigurationBgpPeeringAddressObject** cria um objeto IpConfigurationBgpPeeringAddressObject que representa a propriedade BgpPeeringAddresses em seu gateway de rede virtual bgpsettings.</span><span class="sxs-lookup"><span data-stu-id="ec8f6-107">The **New-AzIpConfigurationBgpPeeringAddressObject** creates a IpConfigurationBgpPeeringAddressObject object which represents BgpPeeringAddresses property in your virtual network gateway bgpsettings.</span></span>

## <span data-ttu-id="ec8f6-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ec8f6-108">EXAMPLES</span></span>

### <span data-ttu-id="ec8f6-109">1: criar um AzIpConfigurationBgpPeeringAddressObject</span><span class="sxs-lookup"><span data-stu-id="ec8f6-109">1: Create a AzIpConfigurationBgpPeeringAddressObject</span></span>
```
$ipconfigurationId1 = '/subscriptions/c886bc58-0000-4e01-993f-e01ba3702aaf/resourceGroups/testRg/providers/Microsoft.Network/virtualNetworkGateways/gw1/ipConfigurations/default'
$addresslist1 = @('169.254.21.5')
$gw1ipconfBgp1 = New-AzIpConfigurationBgpPeeringAddresses -IpConfigurationId $ipconfigurationId1 -CustomAddress $addresslist1
```

<span data-ttu-id="ec8f6-110">A seguir, você criará um IpConfigurationBgpPeeringAddressObject. esse novo objeto será gw1ipconfBgp1.</span><span class="sxs-lookup"><span data-stu-id="ec8f6-110">The above will create a IpConfigurationBgpPeeringAddressObject.This new object will be to gw1ipconfBgp1.</span></span>

## <span data-ttu-id="ec8f6-111">OS</span><span class="sxs-lookup"><span data-stu-id="ec8f6-111">PARAMETERS</span></span>

### <span data-ttu-id="ec8f6-112">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ec8f6-112">-Confirm</span></span>
<span data-ttu-id="ec8f6-113">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ec8f6-113">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec8f6-114">-CustomAddress</span><span class="sxs-lookup"><span data-stu-id="ec8f6-114">-CustomAddress</span></span>
<span data-ttu-id="ec8f6-115">A lista de CustomAddress do gateway de rede virtual para BgpPeeringAddresses.</span><span class="sxs-lookup"><span data-stu-id="ec8f6-115">The virtual network gateway CustomAddress List for BgpPeeringAddresses.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec8f6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec8f6-116">-DefaultProfile</span></span>
<span data-ttu-id="ec8f6-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ec8f6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec8f6-118">-IpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="ec8f6-118">-IpConfigurationId</span></span>
<span data-ttu-id="ec8f6-119">O gateway de rede virtual IpConfigurationId para BgpPeeringAddresses.</span><span class="sxs-lookup"><span data-stu-id="ec8f6-119">The virtual network gateway IpConfigurationId for BgpPeeringAddresses.</span></span>

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

### <span data-ttu-id="ec8f6-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec8f6-120">-WhatIf</span></span>
<span data-ttu-id="ec8f6-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ec8f6-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec8f6-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ec8f6-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec8f6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec8f6-123">CommonParameters</span></span>
<span data-ttu-id="ec8f6-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec8f6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec8f6-125">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ec8f6-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec8f6-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ec8f6-126">INPUTS</span></span>

### <span data-ttu-id="ec8f6-127">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="ec8f6-127">None</span></span>

## <span data-ttu-id="ec8f6-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ec8f6-128">OUTPUTS</span></span>

### <span data-ttu-id="ec8f6-129">Microsoft. Azure. Commands. Network. Models. PSIpConfigurationBgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="ec8f6-129">Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress</span></span>

## <span data-ttu-id="ec8f6-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ec8f6-130">NOTES</span></span>

## <span data-ttu-id="ec8f6-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ec8f6-131">RELATED LINKS</span></span>
