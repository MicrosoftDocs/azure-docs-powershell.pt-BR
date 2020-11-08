---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 015C7DB7-2B08-4033-9B6E-1738D4DDACDA
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 2aa9792c632a7e615091a69182c87bc06b565c18
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94117254"
---
# <span data-ttu-id="f9a58-101">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="f9a58-101">Remove-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="f9a58-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f9a58-102">SYNOPSIS</span></span>
<span data-ttu-id="f9a58-103">Remove uma configuração de IP de interface de rede de uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="f9a58-103">Removes a network interface IP configuration from a network interface.</span></span>

## <span data-ttu-id="f9a58-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f9a58-104">SYNTAX</span></span>

```
Remove-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f9a58-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f9a58-105">DESCRIPTION</span></span>
<span data-ttu-id="f9a58-106">O cmdlet **Remove-AzNetworkInterfaceIpConfig** remove uma configuração de IP de interface de rede de uma interface de rede do Azure.</span><span class="sxs-lookup"><span data-stu-id="f9a58-106">The **Remove-AzNetworkInterfaceIpConfig** cmdlet removes a network interface IP configuration from an Azure network interface.</span></span>

## <span data-ttu-id="f9a58-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f9a58-107">EXAMPLES</span></span>

### <span data-ttu-id="f9a58-108">Exemplo 1: excluir uma configuração de IP de uma interface de rede</span><span class="sxs-lookup"><span data-stu-id="f9a58-108">Example 1: Delete an IP configuration from a network interface</span></span>
```powershell
$nic = Get-AzNetworkInterface -Name mynic -ResourceGroupName myrg

Remove-AzNetworkInterfaceIpConfig -Name IPConfig-1 -NetworkInterface $nic

Set-AzNetworkInterface -NetworkInterface $nic
```

<span data-ttu-id="f9a58-109">O primeiro comando obtém uma interface de rede chamada mynic e a armazena na variável $nic.</span><span class="sxs-lookup"><span data-stu-id="f9a58-109">The first command gets a network interface called mynic and stores it in the variable $nic.</span></span> <span data-ttu-id="f9a58-110">O segundo comando Remove a configuração de IP chamada IPConfig-1 associada a essa interface de rede.</span><span class="sxs-lookup"><span data-stu-id="f9a58-110">The second command removes the IP configuration called IPConfig-1 associated with this network interface.</span></span> <span data-ttu-id="f9a58-111">O terceiro comando define as alterações feitas na interface de rede.</span><span class="sxs-lookup"><span data-stu-id="f9a58-111">The third command sets changes made to the network interface.</span></span>

## <span data-ttu-id="f9a58-112">OS</span><span class="sxs-lookup"><span data-stu-id="f9a58-112">PARAMETERS</span></span>

### <span data-ttu-id="f9a58-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9a58-113">-DefaultProfile</span></span>
<span data-ttu-id="f9a58-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f9a58-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f9a58-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="f9a58-115">-Name</span></span>
<span data-ttu-id="f9a58-116">Especifica o nome da configuração de IP da interface de rede a ser removida.</span><span class="sxs-lookup"><span data-stu-id="f9a58-116">Specifies the name of the network interface IP configuration to remove.</span></span>

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

### <span data-ttu-id="f9a58-117">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="f9a58-117">-NetworkInterface</span></span>
<span data-ttu-id="f9a58-118">Especifica um objeto **NetworkInterface** .</span><span class="sxs-lookup"><span data-stu-id="f9a58-118">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="f9a58-119">Esse objeto contém a configuração de IP da interface de rede a ser removida.</span><span class="sxs-lookup"><span data-stu-id="f9a58-119">This object contains the network interface IP configuration to remove.</span></span>

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

### <span data-ttu-id="f9a58-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9a58-120">CommonParameters</span></span>
<span data-ttu-id="f9a58-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9a58-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9a58-122">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9a58-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9a58-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f9a58-123">INPUTS</span></span>

### <span data-ttu-id="f9a58-124">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="f9a58-124">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="f9a58-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f9a58-125">OUTPUTS</span></span>

### <span data-ttu-id="f9a58-126">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="f9a58-126">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="f9a58-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f9a58-127">NOTES</span></span>
* <span data-ttu-id="f9a58-128">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede</span><span class="sxs-lookup"><span data-stu-id="f9a58-128">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="f9a58-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f9a58-129">RELATED LINKS</span></span>

[<span data-ttu-id="f9a58-130">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="f9a58-130">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="f9a58-131">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="f9a58-131">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="f9a58-132">New-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="f9a58-132">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="f9a58-133">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="f9a58-133">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)


