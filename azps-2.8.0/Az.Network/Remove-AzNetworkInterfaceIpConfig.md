---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 015C7DB7-2B08-4033-9B6E-1738D4DDACDA
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: d532bbee77d028afb4af441dd511deafa6ebc016
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771523"
---
# <span data-ttu-id="0852e-101">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="0852e-101">Remove-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="0852e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0852e-102">SYNOPSIS</span></span>
<span data-ttu-id="0852e-103">Remove uma configuração de IP de interface de rede de uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="0852e-103">Removes a network interface IP configuration from a network interface.</span></span>

## <span data-ttu-id="0852e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0852e-104">SYNTAX</span></span>

```
Remove-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0852e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0852e-105">DESCRIPTION</span></span>
<span data-ttu-id="0852e-106">O cmdlet **Remove-AzNetworkInterfaceIpConfig** remove uma configuração de IP de interface de rede de uma interface de rede do Azure.</span><span class="sxs-lookup"><span data-stu-id="0852e-106">The **Remove-AzNetworkInterfaceIpConfig** cmdlet removes a network interface IP configuration from an Azure network interface.</span></span>

## <span data-ttu-id="0852e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0852e-107">EXAMPLES</span></span>

### <span data-ttu-id="0852e-108">1: excluir uma configuração de IP de uma interface de rede</span><span class="sxs-lookup"><span data-stu-id="0852e-108">1: Delete an IP configuration from a network interface</span></span>
```
$nic = Get-AzNetworkInterface -Name mynic -ResourceGroupName myrg

Remove-AzNetworkInterfaceIpConfig -Name IPConfig-1 -NetworkInterface $nic
```

<span data-ttu-id="0852e-109">O primeiro comando obtém uma interface de rede chamada mynic e a armazena na variável $nic.</span><span class="sxs-lookup"><span data-stu-id="0852e-109">The first command gets a network interface called mynic and stores it in the variable $nic.</span></span> <span data-ttu-id="0852e-110">O segundo comando Remove a configuração de IP chamada IPConfig-1 associada a essa interface de rede.</span><span class="sxs-lookup"><span data-stu-id="0852e-110">The second command removes the IP configuration called IPConfig-1 associated with this network interface.</span></span>

## <span data-ttu-id="0852e-111">OS</span><span class="sxs-lookup"><span data-stu-id="0852e-111">PARAMETERS</span></span>

### <span data-ttu-id="0852e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0852e-112">-DefaultProfile</span></span>
<span data-ttu-id="0852e-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0852e-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0852e-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="0852e-114">-Name</span></span>
<span data-ttu-id="0852e-115">Especifica o nome da configuração de IP da interface de rede a ser removida.</span><span class="sxs-lookup"><span data-stu-id="0852e-115">Specifies the name of the network interface IP configuration to remove.</span></span>

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

### <span data-ttu-id="0852e-116">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="0852e-116">-NetworkInterface</span></span>
<span data-ttu-id="0852e-117">Especifica um objeto **NetworkInterface** .</span><span class="sxs-lookup"><span data-stu-id="0852e-117">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="0852e-118">Esse objeto contém a configuração de IP da interface de rede a ser removida.</span><span class="sxs-lookup"><span data-stu-id="0852e-118">This object contains the network interface IP configuration to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterface
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0852e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0852e-119">CommonParameters</span></span>
<span data-ttu-id="0852e-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0852e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0852e-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0852e-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0852e-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0852e-122">INPUTS</span></span>

### <span data-ttu-id="0852e-123">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="0852e-123">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="0852e-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0852e-124">OUTPUTS</span></span>

### <span data-ttu-id="0852e-125">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="0852e-125">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="0852e-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0852e-126">NOTES</span></span>
* <span data-ttu-id="0852e-127">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede</span><span class="sxs-lookup"><span data-stu-id="0852e-127">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="0852e-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0852e-128">RELATED LINKS</span></span>

[<span data-ttu-id="0852e-129">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="0852e-129">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="0852e-130">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="0852e-130">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="0852e-131">New-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="0852e-131">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="0852e-132">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="0852e-132">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)


