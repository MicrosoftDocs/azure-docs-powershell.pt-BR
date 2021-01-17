---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzDelegation.md
ms.openlocfilehash: f32b06e9b162a4d142d6d6fff9b7cdca34e0b30b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98434722"
---
# <span data-ttu-id="fc20b-101">Get-AzDelegation</span><span class="sxs-lookup"><span data-stu-id="fc20b-101">Get-AzDelegation</span></span>

## <span data-ttu-id="fc20b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fc20b-102">SYNOPSIS</span></span>
<span data-ttu-id="fc20b-103">Obter uma delegação (ou todas as delegações) em uma determinada sub-rede.</span><span class="sxs-lookup"><span data-stu-id="fc20b-103">Get a delegation (or all of the delegations) on a given subnet.</span></span>

## <span data-ttu-id="fc20b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fc20b-104">SYNTAX</span></span>

```
Get-AzDelegation [-Name <String>] -Subnet <PSSubnet> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fc20b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fc20b-105">DESCRIPTION</span></span>
<span data-ttu-id="fc20b-106">O cmdlet **Get-AzDelegation** Obtém a delegação nomeada de uma sub-rede.</span><span class="sxs-lookup"><span data-stu-id="fc20b-106">The **Get-AzDelegation** cmdlet gets the named delegation from a subnet.</span></span> <span data-ttu-id="fc20b-107">Se nenhuma delegação for nomeada, ela retornará todas as delegações na sub-rede fornecida.</span><span class="sxs-lookup"><span data-stu-id="fc20b-107">If no delegation is named, it returns all of the delegations on the provided subnet.</span></span>

## <span data-ttu-id="fc20b-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fc20b-108">EXAMPLES</span></span>

### <span data-ttu-id="fc20b-109">1: Recuperando uma delegação específica</span><span class="sxs-lookup"><span data-stu-id="fc20b-109">1: Retrieving a specific delegation</span></span>
```powershell
PS C:\> $subnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup" | Get-AzVirtualNetworkSubnetConfig -Name "mySubnet"
PS C:\> Get-AzDelegation -Name "myDelegation" -Subnet $subnet

ProvisioningState : Succeeded
ServiceName       : Microsoft.Sql/servers
Actions           : {}
Name              : myDelegation
Etag              : "thisisaguid"
Id                : /subscriptions/subId/resourceGroups/rg/providers/Microsoft.Network/virtualNetworks/myvnet/subnets/mySubnet/delegations/myDelegation
```

<span data-ttu-id="fc20b-110">A primeira linha recupera a sub-rede de interesse.</span><span class="sxs-lookup"><span data-stu-id="fc20b-110">The first line retrieves the subnet of interest.</span></span> <span data-ttu-id="fc20b-111">A segunda linha mostra as informações de delegação da delegação chamada "mydelegation".</span><span class="sxs-lookup"><span data-stu-id="fc20b-111">The second line shows the delegation information for the delegation called "myDelegation."</span></span>

### <span data-ttu-id="fc20b-112">2: Recuperando todas as delegações de sub-rede</span><span class="sxs-lookup"><span data-stu-id="fc20b-112">2: Retrieving all subnet delegations</span></span>
```powershell
PS C:\> $subnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup" | Get-AzVirtualNetworkSubnetConfig -Name "mySubnet"
PS C:\> $delegations = Get-AzDelegation -Subnet $subnet
```

<span data-ttu-id="fc20b-113">A primeira linha recupera a sub-rede de interesse.</span><span class="sxs-lookup"><span data-stu-id="fc20b-113">The first line retrieves the subnet of interest.</span></span> <span data-ttu-id="fc20b-114">A segunda linha armazena uma lista de todas as delegações em _Mysubnetry_ na variável $delegations.</span><span class="sxs-lookup"><span data-stu-id="fc20b-114">The second line stores a list of all of the delegations on _mySubnet_ in the $delegations variable.</span></span>

## <span data-ttu-id="fc20b-115">OS</span><span class="sxs-lookup"><span data-stu-id="fc20b-115">PARAMETERS</span></span>

### <span data-ttu-id="fc20b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc20b-116">-DefaultProfile</span></span>
<span data-ttu-id="fc20b-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fc20b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc20b-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="fc20b-118">-Name</span></span>
<span data-ttu-id="fc20b-119">O nome da delegação</span><span class="sxs-lookup"><span data-stu-id="fc20b-119">The name of the delegation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc20b-120">-Subnet</span><span class="sxs-lookup"><span data-stu-id="fc20b-120">-Subnet</span></span>
<span data-ttu-id="fc20b-121">A sub-rede</span><span class="sxs-lookup"><span data-stu-id="fc20b-121">The subnet</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fc20b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc20b-122">CommonParameters</span></span>
<span data-ttu-id="fc20b-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc20b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc20b-124">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fc20b-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc20b-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fc20b-125">INPUTS</span></span>

### <span data-ttu-id="fc20b-126">System. String</span><span class="sxs-lookup"><span data-stu-id="fc20b-126">System.String</span></span>

### <span data-ttu-id="fc20b-127">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="fc20b-127">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="fc20b-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fc20b-128">OUTPUTS</span></span>

### <span data-ttu-id="fc20b-129">Microsoft.Azure.Commands.Network.Models.PSDelegation</span><span class="sxs-lookup"><span data-stu-id="fc20b-129">Microsoft.Azure.Commands.Network.Models.PSDelegation</span></span>

## <span data-ttu-id="fc20b-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fc20b-130">NOTES</span></span>

## <span data-ttu-id="fc20b-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fc20b-131">RELATED LINKS</span></span>

<span data-ttu-id="fc20b-132">[Add-AzDelegation](./Add-AzDelegation.md) 
 [New-AzDelegation](./New-AzDelegation.md) 
 [Remove-AzDelegation](./Remove-AzDelegation.md) 
 [Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md) 
 [Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)</span><span class="sxs-lookup"><span data-stu-id="fc20b-132">[Add-AzDelegation](./Add-AzDelegation.md)
[New-AzDelegation](./New-AzDelegation.md)
[Remove-AzDelegation](./Remove-AzDelegation.md)
[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md)
[Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)</span></span>
