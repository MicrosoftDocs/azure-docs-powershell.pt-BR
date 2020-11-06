---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmDelegation.md
ms.openlocfilehash: f3e8ef97ab618df37ba7d5adae107d65676ed29f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432762"
---
# <span data-ttu-id="84648-101">Get-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="84648-101">Get-AzureRmDelegation</span></span>

## <span data-ttu-id="84648-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="84648-102">SYNOPSIS</span></span>
<span data-ttu-id="84648-103">Obter uma delegação (ou todas as delegações) em uma determinada sub-rede.</span><span class="sxs-lookup"><span data-stu-id="84648-103">Get a delegation (or all of the delegations) on a given subnet.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="84648-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="84648-104">SYNTAX</span></span>

```
Get-AzureRmDelegation [-Name <String>] -Subnet <PSSubnet> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="84648-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="84648-105">DESCRIPTION</span></span>
<span data-ttu-id="84648-106">O cmdlet **Get-AzureRmDelegation** Obtém a delegação nomeada de uma sub-rede.</span><span class="sxs-lookup"><span data-stu-id="84648-106">The **Get-AzureRmDelegation** cmdlet gets the named delegation from a subnet.</span></span> <span data-ttu-id="84648-107">Se nenhuma delegação for nomeada, ela retornará todas as delegações na sub-rede fornecida.</span><span class="sxs-lookup"><span data-stu-id="84648-107">If no delegation is named, it returns all of the delegations on the provided subnet.</span></span>

## <span data-ttu-id="84648-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="84648-108">EXAMPLES</span></span>

### <span data-ttu-id="84648-109">1: Recuperando uma delegação específica</span><span class="sxs-lookup"><span data-stu-id="84648-109">1: Retrieving a specific delegation</span></span>
```powershell
PS C:\> $subnet = Get-AzureRmVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup" | Get-AzureRmVirtualNetworkSubnetConfig -Name "mySubnet"
PS C:\> Get-AzureRmDelegation -Name "myDelegation" -Subnet $subnet

ProvisioningState : Succeeded
ServiceName       : Microsoft.Sql/servers
Actions           : {}
Name              : myDelegation
Etag              : "thisisaguid"
Id                : /subscriptions/subId/resourceGroups/rg/providers/Microsoft.Network/virtualNetworks/myvnet/subnets/mySubnet/delegations/myDelegation
```

<span data-ttu-id="84648-110">A primeira linha recupera a sub-rede de interesse.</span><span class="sxs-lookup"><span data-stu-id="84648-110">The first line retrieves the subnet of interest.</span></span> <span data-ttu-id="84648-111">A segunda linha mostra as informações de delegação da delegação chamada "mydelegation".</span><span class="sxs-lookup"><span data-stu-id="84648-111">The second line shows the delegation information for the delegation called "myDelegation."</span></span>

### <span data-ttu-id="84648-112">2: Recuperando todas as delegações de sub-rede</span><span class="sxs-lookup"><span data-stu-id="84648-112">2: Retrieving all subnet delegations</span></span>
```powershell
PS C:\> $vnet = Get-AzureRmVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup" | Get-AzureRmVirtualNetworkSubnetConfig -Name "mySubnet"
PS C:\> $delegations = Get-AzureRmDelegation -Subnet $subnet
```

<span data-ttu-id="84648-113">A primeira linha recupera a sub-rede de interesse.</span><span class="sxs-lookup"><span data-stu-id="84648-113">The first line retrieves the subnet of interest.</span></span> <span data-ttu-id="84648-114">A segunda linha armazena uma lista de todas as delegações em _Mysubnetry_ na variável $delegations.</span><span class="sxs-lookup"><span data-stu-id="84648-114">The second line stores a list of all of the delegations on _mySubnet_ in the $delegations variable.</span></span>

## <span data-ttu-id="84648-115">OS</span><span class="sxs-lookup"><span data-stu-id="84648-115">PARAMETERS</span></span>

### <span data-ttu-id="84648-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84648-116">-DefaultProfile</span></span>
<span data-ttu-id="84648-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="84648-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84648-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="84648-118">-Name</span></span>
<span data-ttu-id="84648-119">O nome da delegação</span><span class="sxs-lookup"><span data-stu-id="84648-119">The name of the delegation</span></span>

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

### <span data-ttu-id="84648-120">-Subnet</span><span class="sxs-lookup"><span data-stu-id="84648-120">-Subnet</span></span>
<span data-ttu-id="84648-121">A sub-rede</span><span class="sxs-lookup"><span data-stu-id="84648-121">The subnet</span></span>

```yaml
Type: PSSubnet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="84648-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84648-122">CommonParameters</span></span>
<span data-ttu-id="84648-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84648-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="84648-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84648-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84648-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="84648-125">INPUTS</span></span>

### <span data-ttu-id="84648-126">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="84648-126">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="84648-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="84648-127">OUTPUTS</span></span>

### <span data-ttu-id="84648-128">Microsoft.Azure.Commands.Network.Models.PSDelegation</span><span class="sxs-lookup"><span data-stu-id="84648-128">Microsoft.Azure.Commands.Network.Models.PSDelegation</span></span>

## <span data-ttu-id="84648-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="84648-129">NOTES</span></span>

## <span data-ttu-id="84648-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="84648-130">RELATED LINKS</span></span>
<span data-ttu-id="84648-131">[Add-AzureRmDelegation](./Add-AzureRmDelegation.md) 
 [New-AzureRmDelegation](./New-AzureRmDelegation.md) 
 [Remove-AzureRmDelegation](./Remove-AzureRmDelegation.md) 
 [Get-AzureRmVirtualNetwork](./Get-AzureRmVirtualNetwork.md) 
 [Get-AzureRmVirtualNetworkSubnetConfig](./Get-AzureRmVirtualNetworkSubnetConfig.md)</span><span class="sxs-lookup"><span data-stu-id="84648-131">[Add-AzureRmDelegation](./Add-AzureRmDelegation.md)
[New-AzureRmDelegation](./New-AzureRmDelegation.md)
[Remove-AzureRmDelegation](./Remove-AzureRmDelegation.md)
[Get-AzureRmVirtualNetwork](./Get-AzureRmVirtualNetwork.md)
[Get-AzureRmVirtualNetworkSubnetConfig](./Get-AzureRmVirtualNetworkSubnetConfig.md)</span></span>
