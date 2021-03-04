---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azipconfigurationbgppeeringaddressobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpConfigurationBgpPeeringAddressObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpConfigurationBgpPeeringAddressObject.md
ms.openlocfilehash: ba713650670abdeb9c64242109b30f47d99724f1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891790"
---
# <span data-ttu-id="9f3ef-101">New-AzIpConfigurationBgpPeeringAddressObject</span><span class="sxs-lookup"><span data-stu-id="9f3ef-101">New-AzIpConfigurationBgpPeeringAddressObject</span></span>

## <span data-ttu-id="9f3ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f3ef-102">SYNOPSIS</span></span>
<span data-ttu-id="9f3ef-103">cria um novo IpconfigurationBgpPeeringAddressObject</span><span class="sxs-lookup"><span data-stu-id="9f3ef-103">creates a new IpconfigurationBgpPeeringAddressObject</span></span>

## <span data-ttu-id="9f3ef-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="9f3ef-104">SYNTAX</span></span>

### <span data-ttu-id="9f3ef-105">Padrão (Padrão)</span><span class="sxs-lookup"><span data-stu-id="9f3ef-105">Default (Default)</span></span>
```
New-AzIpConfigurationBgpPeeringAddressObject -IpConfigurationId <String>
 -CustomAddress <System.Collections.Generic.List`1[System.String]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```
## <span data-ttu-id="9f3ef-106">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="9f3ef-106">DESCRIPTION</span></span>
<span data-ttu-id="9f3ef-107">O **Objeto New-AzIpConfigurationBgpPeeringAddressObject** cria um objeto IpConfigurationBgpPeeringAddressObject que representa a propriedade BgpPeeringAddresses no gateway de rede virtual bgpsettings.</span><span class="sxs-lookup"><span data-stu-id="9f3ef-107">The **New-AzIpConfigurationBgpPeeringAddressObject** creates a IpConfigurationBgpPeeringAddressObject object which represents BgpPeeringAddresses property in your virtual network gateway bgpsettings.</span></span>

## <span data-ttu-id="9f3ef-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9f3ef-108">EXAMPLES</span></span>

### <span data-ttu-id="9f3ef-109">1: Criar um AzIpConfigurationBgpPeeringAddressObject</span><span class="sxs-lookup"><span data-stu-id="9f3ef-109">1: Create a AzIpConfigurationBgpPeeringAddressObject</span></span>
```
$ipconfigurationId1 = '/subscriptions/c886bc58-0000-4e01-993f-e01ba3702aaf/resourceGroups/testRg/providers/Microsoft.Network/virtualNetworkGateways/gw1/ipConfigurations/default'
$addresslist1 = @('169.254.21.5')
$gw1ipconfBgp1 = New-AzIpConfigurationBgpPeeringAddresses -IpConfigurationId $ipconfigurationId1 -CustomAddress $addresslist1
```

<span data-ttu-id="9f3ef-110">O acima criará um IpConfigurationBgpPeeringAddressObject.Este novo objeto será para gw1ipconfBgp1.</span><span class="sxs-lookup"><span data-stu-id="9f3ef-110">The above will create a IpConfigurationBgpPeeringAddressObject.This new object will be to gw1ipconfBgp1.</span></span>

## <span data-ttu-id="9f3ef-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="9f3ef-111">PARAMETERS</span></span>

### <span data-ttu-id="9f3ef-112">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9f3ef-112">-Confirm</span></span>
<span data-ttu-id="9f3ef-113">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9f3ef-113">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f3ef-114">-CustomAddress</span><span class="sxs-lookup"><span data-stu-id="9f3ef-114">-CustomAddress</span></span>
<span data-ttu-id="9f3ef-115">O gateway de rede virtual CustomAddress List para BgpPeeringAddresses.</span><span class="sxs-lookup"><span data-stu-id="9f3ef-115">The virtual network gateway CustomAddress List for BgpPeeringAddresses.</span></span>

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

### <span data-ttu-id="9f3ef-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f3ef-116">-DefaultProfile</span></span>
<span data-ttu-id="9f3ef-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9f3ef-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f3ef-118">-IpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="9f3ef-118">-IpConfigurationId</span></span>
<span data-ttu-id="9f3ef-119">O gateway de rede virtual IpConfigurationId para BgpPeeringAddresses.</span><span class="sxs-lookup"><span data-stu-id="9f3ef-119">The virtual network gateway IpConfigurationId for BgpPeeringAddresses.</span></span>

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

### <span data-ttu-id="9f3ef-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f3ef-120">-WhatIf</span></span>
<span data-ttu-id="9f3ef-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9f3ef-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f3ef-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9f3ef-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f3ef-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f3ef-123">CommonParameters</span></span>
<span data-ttu-id="9f3ef-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f3ef-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f3ef-125">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9f3ef-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f3ef-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9f3ef-126">INPUTS</span></span>

### <span data-ttu-id="9f3ef-127">Nenhum</span><span class="sxs-lookup"><span data-stu-id="9f3ef-127">None</span></span>

## <span data-ttu-id="9f3ef-128">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="9f3ef-128">OUTPUTS</span></span>

### <span data-ttu-id="9f3ef-129">Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="9f3ef-129">Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress</span></span>

## <span data-ttu-id="9f3ef-130">NOTES</span><span class="sxs-lookup"><span data-stu-id="9f3ef-130">NOTES</span></span>

## <span data-ttu-id="9f3ef-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9f3ef-131">RELATED LINKS</span></span>
