---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1B39809C-90DA-4ECB-B949-D4A9A54ED982
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 8152cf778cabed1c4a8a346ac86b708266058fc6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94116212"
---
# <span data-ttu-id="e4f30-101">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="e4f30-101">Get-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="e4f30-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e4f30-102">SYNOPSIS</span></span>
<span data-ttu-id="e4f30-103">Obtém uma configuração de IP de interface de rede para uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="e4f30-103">Gets a network interface IP configuration for a network interface.</span></span>

## <span data-ttu-id="e4f30-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e4f30-104">SYNTAX</span></span>

```
Get-AzNetworkInterfaceIpConfig [-Name <String>] -NetworkInterface <PSNetworkInterface>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e4f30-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e4f30-105">DESCRIPTION</span></span>
<span data-ttu-id="e4f30-106">O cmdlet **Get-AzNetworkInterfaceIPConfig** Obtém uma configuração de IP de interface de rede de uma interface de rede do Azure.</span><span class="sxs-lookup"><span data-stu-id="e4f30-106">The **Get-AzNetworkInterfaceIPConfig** cmdlet gets a network interface IP configuration from an Azure network interface.</span></span>

## <span data-ttu-id="e4f30-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e4f30-107">EXAMPLES</span></span>

### <span data-ttu-id="e4f30-108">1: obter uma configuração de IP de uma interface de rede</span><span class="sxs-lookup"><span data-stu-id="e4f30-108">1: Get an IP configuration of a network interface</span></span>
```
$nic1 = Get-AzNetworkInterface -Name mynic -ResourceGroupName $myrg
Get-AzNetworkInterfaceIpConfig -Name ipconfig1 -NetworkInterface $nic1
```

<span data-ttu-id="e4f30-109">O primeiro comando obtém uma interface de rede existente chamada mynic e a armazena na variável $nic 1.</span><span class="sxs-lookup"><span data-stu-id="e4f30-109">The first command gets an existing network interface called mynic and stores it in the variable $nic1.</span></span> <span data-ttu-id="e4f30-110">O segundo comando obtém a configuração de IP chamada ipconfig1 da interface de rede.</span><span class="sxs-lookup"><span data-stu-id="e4f30-110">The second command gets the IP configuration called ipconfig1 of this network interface.</span></span>
    

## <span data-ttu-id="e4f30-111">OS</span><span class="sxs-lookup"><span data-stu-id="e4f30-111">PARAMETERS</span></span>

### <span data-ttu-id="e4f30-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4f30-112">-DefaultProfile</span></span>
<span data-ttu-id="e4f30-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e4f30-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e4f30-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="e4f30-114">-Name</span></span>
<span data-ttu-id="e4f30-115">Especifica o nome da configuração de IP de rede que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="e4f30-115">Specifies the name of the network IP configuration that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4f30-116">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="e4f30-116">-NetworkInterface</span></span>
<span data-ttu-id="e4f30-117">Especifica um objeto **NetworkInterface** que contém a configuração de IP de rede que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="e4f30-117">Specifies a **NetworkInterface** object that contains the network IP configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="e4f30-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4f30-118">CommonParameters</span></span>
<span data-ttu-id="e4f30-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4f30-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4f30-120">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e4f30-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4f30-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e4f30-121">INPUTS</span></span>

### <span data-ttu-id="e4f30-122">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="e4f30-122">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="e4f30-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e4f30-123">OUTPUTS</span></span>

### <span data-ttu-id="e4f30-124">Microsoft. Azure. Commands. Network. Models. PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="e4f30-124">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span></span>

## <span data-ttu-id="e4f30-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e4f30-125">NOTES</span></span>
* <span data-ttu-id="e4f30-126">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede</span><span class="sxs-lookup"><span data-stu-id="e4f30-126">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="e4f30-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e4f30-127">RELATED LINKS</span></span>

[<span data-ttu-id="e4f30-128">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="e4f30-128">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="e4f30-129">New-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="e4f30-129">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="e4f30-130">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="e4f30-130">Remove-AzNetworkInterfaceIpConfig</span></span>](./Remove-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="e4f30-131">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="e4f30-131">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)


