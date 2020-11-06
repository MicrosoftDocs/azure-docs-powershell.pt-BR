---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmDelegation.md
ms.openlocfilehash: 1daa68e021646d91a2ab1b45382b137771411325
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610280"
---
# <span data-ttu-id="4a2ae-101">Remove-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="4a2ae-101">Remove-AzureRmDelegation</span></span>

## <span data-ttu-id="4a2ae-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4a2ae-102">SYNOPSIS</span></span>
<span data-ttu-id="4a2ae-103">Remove uma delegação de serviço da sub-rede fornecida.</span><span class="sxs-lookup"><span data-stu-id="4a2ae-103">Removes a service delegation from the provided subnet.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4a2ae-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4a2ae-104">SYNTAX</span></span>

```
Remove-AzureRmDelegation -Name <String> -Subnet <PSSubnet> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4a2ae-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4a2ae-105">DESCRIPTION</span></span>
<span data-ttu-id="4a2ae-106">O cmdlet **Remove-AzureRmDelegation** leva em uma sub-rede com delegações e remove a delegação nomeada dessa sub-rede.</span><span class="sxs-lookup"><span data-stu-id="4a2ae-106">The **Remove-AzureRmDelegation** cmdlet takes in a Subnet with delegations and removes the named delegation from that subnet.</span></span>

## <span data-ttu-id="4a2ae-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4a2ae-107">EXAMPLES</span></span>

### <span data-ttu-id="4a2ae-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4a2ae-108">Example 1</span></span>
```powershell
# Add a delegation to an existing subnet
PS C:\> $vnet = Get-AzureRmVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet = Add-AzureRmDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers" -Subnet $subnet
PS C:\> Set-AzureRmVirtualNetwork $vnet

# Remove the delegation
PS C:\> $vnet = Get-AzureRmVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet = Remove-AzureRmDelegation -Name "myDelegation" -Subnet $subnet
PS C:\> Set-AzureRmVirtualNetwork $vnet
```

<span data-ttu-id="4a2ae-109">Neste exemplo, a primeira metade (encontrada em _"Adicionar delegação a uma sub-rede existente"_ ) é idêntica a [Add-AzureRmDelegation](./Add-AzureRmDelegation.md).</span><span class="sxs-lookup"><span data-stu-id="4a2ae-109">In this example, the first half (found under _"Add a delegation to an existing subnet"_ ) is identical to [Add-AzureRmDelegation](./Add-AzureRmDelegation.md).</span></span> <span data-ttu-id="4a2ae-110">Na segunda metade, os dois primeiros cmdlets recuperam a sub-rede do interesse, atualizando a cópia local com o que há no servidor.</span><span class="sxs-lookup"><span data-stu-id="4a2ae-110">In the second half, the first two cmdlets retrieve the subnet of interest, refreshing the local copy with what's on the server.</span></span> <span data-ttu-id="4a2ae-111">O terceiro cmdlet Remove a delegação que foi criada na primeira metade de _mysubnet_ e armazena a sub-rede atualizada em _$subnet_.</span><span class="sxs-lookup"><span data-stu-id="4a2ae-111">The third cmdlet removes the delegation that was created in the first half from _mySubnet_ and stores the updated subnet in _$subnet_.</span></span> <span data-ttu-id="4a2ae-112">O cmdlet final atualiza o servidor com a delegação removida.</span><span class="sxs-lookup"><span data-stu-id="4a2ae-112">The final cmdlet updates the server with the removed delegation.</span></span>

## <span data-ttu-id="4a2ae-113">OS</span><span class="sxs-lookup"><span data-stu-id="4a2ae-113">PARAMETERS</span></span>

### <span data-ttu-id="4a2ae-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a2ae-114">-DefaultProfile</span></span>
<span data-ttu-id="4a2ae-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4a2ae-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a2ae-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="4a2ae-116">-Name</span></span>
<span data-ttu-id="4a2ae-117">O nome da delegação</span><span class="sxs-lookup"><span data-stu-id="4a2ae-117">The name of the delegation</span></span>

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

### <span data-ttu-id="4a2ae-118">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="4a2ae-118">-ServiceName</span></span>
<span data-ttu-id="4a2ae-119">O nome do serviço para o qual a sub-rede deve ser delegada</span><span class="sxs-lookup"><span data-stu-id="4a2ae-119">The name of the service to which the subnet should be delegated</span></span>

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

### <span data-ttu-id="4a2ae-120">-Subnet</span><span class="sxs-lookup"><span data-stu-id="4a2ae-120">-Subnet</span></span>
<span data-ttu-id="4a2ae-121">A sub-rede da qual você deseja remover a delegação</span><span class="sxs-lookup"><span data-stu-id="4a2ae-121">The subnet from which to remove the delegation</span></span>

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

### <span data-ttu-id="4a2ae-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a2ae-122">CommonParameters</span></span>
<span data-ttu-id="4a2ae-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a2ae-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a2ae-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a2ae-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a2ae-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4a2ae-125">INPUTS</span></span>

### <span data-ttu-id="4a2ae-126">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="4a2ae-126">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>
### <span data-ttu-id="4a2ae-127">System. String</span><span class="sxs-lookup"><span data-stu-id="4a2ae-127">System.String</span></span>
## <span data-ttu-id="4a2ae-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4a2ae-128">OUTPUTS</span></span>

### <span data-ttu-id="4a2ae-129">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="4a2ae-129">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>
## <span data-ttu-id="4a2ae-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4a2ae-130">NOTES</span></span>

## <span data-ttu-id="4a2ae-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4a2ae-131">RELATED LINKS</span></span>

<span data-ttu-id="4a2ae-132">[Add-AzureRmDelegation](./Add-AzureRmDelegation.md) 
 [Get-AzureRmDelegation](./Get-AzureRmDelegation.md) 
 [New-AzureRmDelegation](./New-AzureRmDelegation.md) 
 [Get-AzureRmVirtualNetwork](./Get-AzureRmVirtualNetwork.md) 
 [Get-AzureRmVirtualNetworkSubnetConfig](./Get-AzureRmVirtualNetworkSubnetConfig.md) 
 [Set-AzureRmVirtualNetwork](./Set-AzureRmVirtualNetwork.md)</span><span class="sxs-lookup"><span data-stu-id="4a2ae-132">[Add-AzureRmDelegation](./Add-AzureRmDelegation.md)
[Get-AzureRmDelegation](./Get-AzureRmDelegation.md)
[New-AzureRmDelegation](./New-AzureRmDelegation.md)
[Get-AzureRmVirtualNetwork](./Get-AzureRmVirtualNetwork.md)
[Get-AzureRmVirtualNetworkSubnetConfig](./Get-AzureRmVirtualNetworkSubnetConfig.md)
[Set-AzureRmVirtualNetwork](./Set-AzureRmVirtualNetwork.md)</span></span>
