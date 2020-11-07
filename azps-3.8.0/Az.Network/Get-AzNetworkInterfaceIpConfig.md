---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1B39809C-90DA-4ECB-B949-D4A9A54ED982
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 8152cf778cabed1c4a8a346ac86b708266058fc6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943323"
---
# <span data-ttu-id="f8b28-101">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="f8b28-101">Get-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="f8b28-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f8b28-102">SYNOPSIS</span></span>
<span data-ttu-id="f8b28-103">Obtém uma configuração de IP de interface de rede para uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="f8b28-103">Gets a network interface IP configuration for a network interface.</span></span>

## <span data-ttu-id="f8b28-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f8b28-104">SYNTAX</span></span>

```
Get-AzNetworkInterfaceIpConfig [-Name <String>] -NetworkInterface <PSNetworkInterface>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8b28-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f8b28-105">DESCRIPTION</span></span>
<span data-ttu-id="f8b28-106">O cmdlet **Get-AzNetworkInterfaceIPConfig** Obtém uma configuração de IP de interface de rede de uma interface de rede do Azure.</span><span class="sxs-lookup"><span data-stu-id="f8b28-106">The **Get-AzNetworkInterfaceIPConfig** cmdlet gets a network interface IP configuration from an Azure network interface.</span></span>

## <span data-ttu-id="f8b28-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f8b28-107">EXAMPLES</span></span>

### <span data-ttu-id="f8b28-108">1: obter uma configuração de IP de uma interface de rede</span><span class="sxs-lookup"><span data-stu-id="f8b28-108">1: Get an IP configuration of a network interface</span></span>
```
$nic1 = Get-AzNetworkInterface -Name mynic -ResourceGroupName $myrg
Get-AzNetworkInterfaceIpConfig -Name ipconfig1 -NetworkInterface $nic1
```

<span data-ttu-id="f8b28-109">O primeiro comando obtém uma interface de rede existente chamada mynic e a armazena na variável $nic 1.</span><span class="sxs-lookup"><span data-stu-id="f8b28-109">The first command gets an existing network interface called mynic and stores it in the variable $nic1.</span></span> <span data-ttu-id="f8b28-110">O segundo comando obtém a configuração de IP chamada ipconfig1 da interface de rede.</span><span class="sxs-lookup"><span data-stu-id="f8b28-110">The second command gets the IP configuration called ipconfig1 of this network interface.</span></span>
    

## <span data-ttu-id="f8b28-111">OS</span><span class="sxs-lookup"><span data-stu-id="f8b28-111">PARAMETERS</span></span>

### <span data-ttu-id="f8b28-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8b28-112">-DefaultProfile</span></span>
<span data-ttu-id="f8b28-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f8b28-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8b28-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="f8b28-114">-Name</span></span>
<span data-ttu-id="f8b28-115">Especifica o nome da configuração de IP de rede que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="f8b28-115">Specifies the name of the network IP configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f8b28-116">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="f8b28-116">-NetworkInterface</span></span>
<span data-ttu-id="f8b28-117">Especifica um objeto **NetworkInterface** que contém a configuração de IP de rede que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="f8b28-117">Specifies a **NetworkInterface** object that contains the network IP configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f8b28-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8b28-118">CommonParameters</span></span>
<span data-ttu-id="f8b28-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8b28-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8b28-120">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f8b28-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8b28-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f8b28-121">INPUTS</span></span>

### <span data-ttu-id="f8b28-122">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="f8b28-122">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="f8b28-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f8b28-123">OUTPUTS</span></span>

### <span data-ttu-id="f8b28-124">Microsoft. Azure. Commands. Network. Models. PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="f8b28-124">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span></span>

## <span data-ttu-id="f8b28-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f8b28-125">NOTES</span></span>
* <span data-ttu-id="f8b28-126">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede</span><span class="sxs-lookup"><span data-stu-id="f8b28-126">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="f8b28-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f8b28-127">RELATED LINKS</span></span>

[<span data-ttu-id="f8b28-128">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="f8b28-128">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="f8b28-129">New-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="f8b28-129">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="f8b28-130">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="f8b28-130">Remove-AzNetworkInterfaceIpConfig</span></span>](./Remove-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="f8b28-131">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="f8b28-131">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)


