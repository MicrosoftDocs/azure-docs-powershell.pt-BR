---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 015C7DB7-2B08-4033-9B6E-1738D4DDACDA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkInterfaceIpConfig.md
ms.openlocfilehash: c912d32c39380ee3d653fa228632a4d01f0e3049
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430142"
---
# <span data-ttu-id="3f81b-101">Remove-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="3f81b-101">Remove-AzureRmNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="3f81b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3f81b-102">SYNOPSIS</span></span>
<span data-ttu-id="3f81b-103">Remove uma configuração de IP de interface de rede de uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="3f81b-103">Removes a network interface IP configuration from a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3f81b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3f81b-104">SYNTAX</span></span>

```
Remove-AzureRmNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3f81b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3f81b-105">DESCRIPTION</span></span>
<span data-ttu-id="3f81b-106">O cmdlet **Remove-AzureRmNetworkInterfaceIpConfig** remove uma configuração de IP de interface de rede de uma interface de rede do Azure.</span><span class="sxs-lookup"><span data-stu-id="3f81b-106">The **Remove-AzureRmNetworkInterfaceIpConfig** cmdlet removes a network interface IP configuration from an Azure network interface.</span></span>

## <span data-ttu-id="3f81b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3f81b-107">EXAMPLES</span></span>

### <span data-ttu-id="3f81b-108">1: excluir uma configuração de IP de uma interface de rede</span><span class="sxs-lookup"><span data-stu-id="3f81b-108">1: Delete an IP configuration from a network interface</span></span>
```
$nic = Get-AzureRmNetworkInterface -Name mynic -ResourceGroupName myrg

Remove-AzureRmNetworkInterfaceIpConfig -Name IPConfig-1 -NetworkInterface $nic
```

<span data-ttu-id="3f81b-109">O primeiro comando obtém uma interface de rede chamada mynic e a armazena na variável $nic.</span><span class="sxs-lookup"><span data-stu-id="3f81b-109">The first command gets a network interface called mynic and stores it in the variable $nic.</span></span> <span data-ttu-id="3f81b-110">O segundo comando Remove a configuração de IP chamada IPConfig-1 associada a essa interface de rede.</span><span class="sxs-lookup"><span data-stu-id="3f81b-110">The second command removes the IP configuration called IPConfig-1 associated with this network interface.</span></span>

## <span data-ttu-id="3f81b-111">OS</span><span class="sxs-lookup"><span data-stu-id="3f81b-111">PARAMETERS</span></span>

### <span data-ttu-id="3f81b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f81b-112">-DefaultProfile</span></span>
<span data-ttu-id="3f81b-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3f81b-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3f81b-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="3f81b-114">-Name</span></span>
<span data-ttu-id="3f81b-115">Especifica o nome da configuração de IP da interface de rede a ser removida.</span><span class="sxs-lookup"><span data-stu-id="3f81b-115">Specifies the name of the network interface IP configuration to remove.</span></span>

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

### <span data-ttu-id="3f81b-116">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="3f81b-116">-NetworkInterface</span></span>
<span data-ttu-id="3f81b-117">Especifica um objeto **NetworkInterface** .</span><span class="sxs-lookup"><span data-stu-id="3f81b-117">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="3f81b-118">Esse objeto contém a configuração de IP da interface de rede a ser removida.</span><span class="sxs-lookup"><span data-stu-id="3f81b-118">This object contains the network interface IP configuration to remove.</span></span>

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

### <span data-ttu-id="3f81b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f81b-119">CommonParameters</span></span>
<span data-ttu-id="3f81b-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f81b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f81b-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f81b-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f81b-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3f81b-122">INPUTS</span></span>

### <span data-ttu-id="3f81b-123">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="3f81b-123">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>
<span data-ttu-id="3f81b-124">Parâmetros: NetworkInterface (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3f81b-124">Parameters: NetworkInterface (ByValue)</span></span>

## <span data-ttu-id="3f81b-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3f81b-125">OUTPUTS</span></span>

### <span data-ttu-id="3f81b-126">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="3f81b-126">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="3f81b-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3f81b-127">NOTES</span></span>
* <span data-ttu-id="3f81b-128">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede</span><span class="sxs-lookup"><span data-stu-id="3f81b-128">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="3f81b-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3f81b-129">RELATED LINKS</span></span>

[<span data-ttu-id="3f81b-130">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="3f81b-130">Add-AzureRmNetworkInterfaceIpConfig</span></span>](./Add-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="3f81b-131">Get-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="3f81b-131">Get-AzureRmNetworkInterfaceIpConfig</span></span>](./Get-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="3f81b-132">New-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="3f81b-132">New-AzureRmNetworkInterfaceIpConfig</span></span>](./New-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="3f81b-133">Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="3f81b-133">Set-AzureRmNetworkInterfaceIpConfig</span></span>](./Set-AzureRmNetworkInterfaceIpConfig.md)

