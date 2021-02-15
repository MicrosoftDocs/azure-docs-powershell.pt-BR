---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1B39809C-90DA-4ECB-B949-D4A9A54ED982
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 8152cf778cabed1c4a8a346ac86b708266058fc6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114151"
---
# <span data-ttu-id="bbf49-101">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="bbf49-101">Get-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="bbf49-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bbf49-102">SYNOPSIS</span></span>
<span data-ttu-id="bbf49-103">Obtém uma configuração IP de interface de rede para uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="bbf49-103">Gets a network interface IP configuration for a network interface.</span></span>

## <span data-ttu-id="bbf49-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bbf49-104">SYNTAX</span></span>

```
Get-AzNetworkInterfaceIpConfig [-Name <String>] -NetworkInterface <PSNetworkInterface>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bbf49-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="bbf49-105">DESCRIPTION</span></span>
<span data-ttu-id="bbf49-106">O cmdlet **Get-AzNetworkInterfaceIPConfig obtém** uma configuração IP de interface de rede de uma interface de rede do Azure.</span><span class="sxs-lookup"><span data-stu-id="bbf49-106">The **Get-AzNetworkInterfaceIPConfig** cmdlet gets a network interface IP configuration from an Azure network interface.</span></span>

## <span data-ttu-id="bbf49-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="bbf49-107">EXAMPLES</span></span>

### <span data-ttu-id="bbf49-108">1: Obter uma configuração IP de uma interface de rede</span><span class="sxs-lookup"><span data-stu-id="bbf49-108">1: Get an IP configuration of a network interface</span></span>
```
$nic1 = Get-AzNetworkInterface -Name mynic -ResourceGroupName $myrg
Get-AzNetworkInterfaceIpConfig -Name ipconfig1 -NetworkInterface $nic1
```

<span data-ttu-id="bbf49-109">O primeiro comando obtém uma interface de rede existente chamada mynic e a armazena na variável $nic 1.</span><span class="sxs-lookup"><span data-stu-id="bbf49-109">The first command gets an existing network interface called mynic and stores it in the variable $nic1.</span></span> <span data-ttu-id="bbf49-110">O segundo comando obtém a configuração IP chamada ipconfig1 desta interface de rede.</span><span class="sxs-lookup"><span data-stu-id="bbf49-110">The second command gets the IP configuration called ipconfig1 of this network interface.</span></span>
    

## <span data-ttu-id="bbf49-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bbf49-111">PARAMETERS</span></span>

### <span data-ttu-id="bbf49-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbf49-112">-DefaultProfile</span></span>
<span data-ttu-id="bbf49-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="bbf49-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bbf49-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="bbf49-114">-Name</span></span>
<span data-ttu-id="bbf49-115">Especifica o nome da configuração ip de rede que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="bbf49-115">Specifies the name of the network IP configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="bbf49-116">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="bbf49-116">-NetworkInterface</span></span>
<span data-ttu-id="bbf49-117">Especifica um objeto **NetworkInterface** que contém a configuração de IP de rede que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="bbf49-117">Specifies a **NetworkInterface** object that contains the network IP configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="bbf49-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbf49-118">CommonParameters</span></span>
<span data-ttu-id="bbf49-119">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bbf49-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbf49-120">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bbf49-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbf49-121">Entradas</span><span class="sxs-lookup"><span data-stu-id="bbf49-121">INPUTS</span></span>

### <span data-ttu-id="bbf49-122">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="bbf49-122">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="bbf49-123">Saídas</span><span class="sxs-lookup"><span data-stu-id="bbf49-123">OUTPUTS</span></span>

### <span data-ttu-id="bbf49-124">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="bbf49-124">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span></span>

## <span data-ttu-id="bbf49-125">Notas</span><span class="sxs-lookup"><span data-stu-id="bbf49-125">NOTES</span></span>
* <span data-ttu-id="bbf49-126">Palavras-chave: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="bbf49-126">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="bbf49-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bbf49-127">RELATED LINKS</span></span>

[<span data-ttu-id="bbf49-128">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="bbf49-128">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="bbf49-129">New-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="bbf49-129">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="bbf49-130">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="bbf49-130">Remove-AzNetworkInterfaceIpConfig</span></span>](./Remove-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="bbf49-131">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="bbf49-131">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)


