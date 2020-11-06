---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1B39809C-90DA-4ECB-B949-D4A9A54ED982
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkInterfaceIpConfig.md
ms.openlocfilehash: 3d3185762c6bb60d59ef15a129b4055939b49213
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441315"
---
# <span data-ttu-id="bfd8f-101">Get-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="bfd8f-101">Get-AzureRmNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="bfd8f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bfd8f-102">SYNOPSIS</span></span>
<span data-ttu-id="bfd8f-103">Obtém uma configuração de IP de interface de rede para uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="bfd8f-103">Gets a network interface IP configuration for a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bfd8f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bfd8f-104">SYNTAX</span></span>

```
Get-AzureRmNetworkInterfaceIpConfig [-Name <String>] -NetworkInterface <PSNetworkInterface>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bfd8f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bfd8f-105">DESCRIPTION</span></span>
<span data-ttu-id="bfd8f-106">O cmdlet **Get-AzureRmNetworkInterfaceIPConfig** Obtém uma configuração de IP de interface de rede de uma interface de rede do Azure.</span><span class="sxs-lookup"><span data-stu-id="bfd8f-106">The **Get-AzureRmNetworkInterfaceIPConfig** cmdlet gets a network interface IP configuration from an Azure network interface.</span></span>

## <span data-ttu-id="bfd8f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bfd8f-107">EXAMPLES</span></span>

### <span data-ttu-id="bfd8f-108">1: obter uma configuração de IP de uma interface de rede</span><span class="sxs-lookup"><span data-stu-id="bfd8f-108">1: Get an IP configuration of a network interface</span></span>
```
$nic1 = Get-AzureRmNetworkInterface -Name mynic -ResourceGroupName $myrg
Get-AzureRmNetworkInterfaceIpConfig -Name ipconfig1 -NetworkInterface $nic1
```

<span data-ttu-id="bfd8f-109">O primeiro comando obtém uma interface de rede existente chamada mynic e a armazena na variável $nic 1.</span><span class="sxs-lookup"><span data-stu-id="bfd8f-109">The first command gets an existing network interface called mynic and stores it in the variable $nic1.</span></span> <span data-ttu-id="bfd8f-110">O segundo comando obtém a configuração de IP chamada ipconfig1 da interface de rede.</span><span class="sxs-lookup"><span data-stu-id="bfd8f-110">The second command gets the IP configuration called ipconfig1 of this network interface.</span></span>
    

## <span data-ttu-id="bfd8f-111">OS</span><span class="sxs-lookup"><span data-stu-id="bfd8f-111">PARAMETERS</span></span>

### <span data-ttu-id="bfd8f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfd8f-112">-DefaultProfile</span></span>
<span data-ttu-id="bfd8f-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bfd8f-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bfd8f-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="bfd8f-114">-Name</span></span>
<span data-ttu-id="bfd8f-115">Especifica o nome da configuração de IP de rede que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="bfd8f-115">Specifies the name of the network IP configuration that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfd8f-116">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="bfd8f-116">-NetworkInterface</span></span>
<span data-ttu-id="bfd8f-117">Especifica um objeto **NetworkInterface** que contém a configuração de IP de rede que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="bfd8f-117">Specifies a **NetworkInterface** object that contains the network IP configuration that this cmdlet gets.</span></span>

```yaml
Type: PSNetworkInterface
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bfd8f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfd8f-118">CommonParameters</span></span>
<span data-ttu-id="bfd8f-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bfd8f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfd8f-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bfd8f-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfd8f-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bfd8f-121">INPUTS</span></span>

### <span data-ttu-id="bfd8f-122">PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="bfd8f-122">PSNetworkInterface</span></span>
<span data-ttu-id="bfd8f-123">O parâmetro ' NetworkInterface ' aceita o valor do tipo ' PSNetworkInterface ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="bfd8f-123">Parameter 'NetworkInterface' accepts value of type 'PSNetworkInterface' from the pipeline</span></span>

## <span data-ttu-id="bfd8f-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bfd8f-124">OUTPUTS</span></span>

### <span data-ttu-id="bfd8f-125">Microsoft. Azure. Commands. Network. Models. PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="bfd8f-125">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span></span>

## <span data-ttu-id="bfd8f-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bfd8f-126">NOTES</span></span>
* <span data-ttu-id="bfd8f-127">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede</span><span class="sxs-lookup"><span data-stu-id="bfd8f-127">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="bfd8f-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bfd8f-128">RELATED LINKS</span></span>

[<span data-ttu-id="bfd8f-129">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="bfd8f-129">Add-AzureRmNetworkInterfaceIpConfig</span></span>](./Add-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="bfd8f-130">New-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="bfd8f-130">New-AzureRmNetworkInterfaceIpConfig</span></span>](./New-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="bfd8f-131">Remove-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="bfd8f-131">Remove-AzureRmNetworkInterfaceIpConfig</span></span>](./Remove-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="bfd8f-132">Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="bfd8f-132">Set-AzureRmNetworkInterfaceIpConfig</span></span>](./Set-AzureRmNetworkInterfaceIpConfig.md)

