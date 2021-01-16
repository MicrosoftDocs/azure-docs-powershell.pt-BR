---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzDelegation.md
ms.openlocfilehash: 9d5f7960bb8f47a1f0d617cd4ba43db565ae2c79
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98262157"
---
# <span data-ttu-id="8c79f-101">Remove-AzDelegation</span><span class="sxs-lookup"><span data-stu-id="8c79f-101">Remove-AzDelegation</span></span>

## <span data-ttu-id="8c79f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8c79f-102">SYNOPSIS</span></span>
<span data-ttu-id="8c79f-103">Remove uma delegação de serviço da sub-rede fornecida.</span><span class="sxs-lookup"><span data-stu-id="8c79f-103">Removes a service delegation from the provided subnet.</span></span>

## <span data-ttu-id="8c79f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8c79f-104">SYNTAX</span></span>

```
Remove-AzDelegation -Name <String> -Subnet <PSSubnet> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8c79f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8c79f-105">DESCRIPTION</span></span>
<span data-ttu-id="8c79f-106">O cmdlet **Remove-AzDelegation** leva em uma sub-rede com delegações e remove a delegação nomeada dessa sub-rede.</span><span class="sxs-lookup"><span data-stu-id="8c79f-106">The **Remove-AzDelegation** cmdlet takes in a Subnet with delegations and removes the named delegation from that subnet.</span></span>

## <span data-ttu-id="8c79f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8c79f-107">EXAMPLES</span></span>

### <span data-ttu-id="8c79f-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8c79f-108">Example 1</span></span>
```powershell
# Add a delegation to an existing subnet
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet = Add-AzDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers" -Subnet $subnet
PS C:\> Set-AzVirtualNetwork $vnet

# Remove the delegation
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet = Remove-AzDelegation -Name "myDelegation" -Subnet $subnet
PS C:\> Set-AzVirtualNetwork $vnet
```

<span data-ttu-id="8c79f-109">Neste exemplo, a primeira metade (encontrada em _"Adicionar delegação a uma sub-rede existente"_) é idêntica a [Add-AzDelegation](./Add-AzDelegation.md).</span><span class="sxs-lookup"><span data-stu-id="8c79f-109">In this example, the first half (found under _"Add a delegation to an existing subnet"_) is identical to [Add-AzDelegation](./Add-AzDelegation.md).</span></span> <span data-ttu-id="8c79f-110">Na segunda metade, os dois primeiros cmdlets recuperam a sub-rede do interesse, atualizando a cópia local com o que há no servidor.</span><span class="sxs-lookup"><span data-stu-id="8c79f-110">In the second half, the first two cmdlets retrieve the subnet of interest, refreshing the local copy with what's on the server.</span></span> <span data-ttu-id="8c79f-111">O terceiro cmdlet Remove a delegação que foi criada na primeira metade de _mysubnet_ e armazena a sub-rede atualizada em _$subnet_.</span><span class="sxs-lookup"><span data-stu-id="8c79f-111">The third cmdlet removes the delegation that was created in the first half from _mySubnet_ and stores the updated subnet in _$subnet_.</span></span> <span data-ttu-id="8c79f-112">O cmdlet final atualiza o servidor com a delegação removida.</span><span class="sxs-lookup"><span data-stu-id="8c79f-112">The final cmdlet updates the server with the removed delegation.</span></span>

## <span data-ttu-id="8c79f-113">OS</span><span class="sxs-lookup"><span data-stu-id="8c79f-113">PARAMETERS</span></span>

### <span data-ttu-id="8c79f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c79f-114">-DefaultProfile</span></span>
<span data-ttu-id="8c79f-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8c79f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8c79f-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="8c79f-116">-Name</span></span>
<span data-ttu-id="8c79f-117">O nome da delegação</span><span class="sxs-lookup"><span data-stu-id="8c79f-117">The name of the delegation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c79f-118">-Subnet</span><span class="sxs-lookup"><span data-stu-id="8c79f-118">-Subnet</span></span>
<span data-ttu-id="8c79f-119">A sub-rede da qual você deseja remover a delegação</span><span class="sxs-lookup"><span data-stu-id="8c79f-119">The subnet from which to remove the delegation</span></span>

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

### <span data-ttu-id="8c79f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c79f-120">CommonParameters</span></span>
<span data-ttu-id="8c79f-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c79f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c79f-122">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c79f-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c79f-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8c79f-123">INPUTS</span></span>

### <span data-ttu-id="8c79f-124">System. String</span><span class="sxs-lookup"><span data-stu-id="8c79f-124">System.String</span></span>

### <span data-ttu-id="8c79f-125">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="8c79f-125">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="8c79f-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8c79f-126">OUTPUTS</span></span>

### <span data-ttu-id="8c79f-127">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="8c79f-127">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="8c79f-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8c79f-128">NOTES</span></span>

## <span data-ttu-id="8c79f-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8c79f-129">RELATED LINKS</span></span>

<span data-ttu-id="8c79f-130">[Add-AzDelegation](./Add-AzDelegation.md) 
 [Get-AzDelegation](./Get-AzDelegation.md) 
 [New-AzDelegation](./New-AzDelegation.md) 
 [Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md) 
 [Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md) 
 [Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span><span class="sxs-lookup"><span data-stu-id="8c79f-130">[Add-AzDelegation](./Add-AzDelegation.md)
[Get-AzDelegation](./Get-AzDelegation.md)
[New-AzDelegation](./New-AzDelegation.md)
[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md)
[Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)
[Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span></span>