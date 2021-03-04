---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/add-azdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzDelegation.md
ms.openlocfilehash: 779793bcc3df7ae62cc7ae7cc900ed863e8f4ee8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889775"
---
# <span data-ttu-id="744a3-101">Add-AzDelegation</span><span class="sxs-lookup"><span data-stu-id="744a3-101">Add-AzDelegation</span></span>

## <span data-ttu-id="744a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="744a3-102">SYNOPSIS</span></span>
<span data-ttu-id="744a3-103">Adiciona uma delegação a uma sub-rede.</span><span class="sxs-lookup"><span data-stu-id="744a3-103">Adds a delegation to a subnet.</span></span>

## <span data-ttu-id="744a3-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="744a3-104">SYNTAX</span></span>

```
Add-AzDelegation -Name <String> -ServiceName <String> -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="744a3-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="744a3-105">DESCRIPTION</span></span>
<span data-ttu-id="744a3-106">O cmdlet **Add-AzDelegation** adiciona uma delegação de serviço a uma sub-rede do Azure.</span><span class="sxs-lookup"><span data-stu-id="744a3-106">The **Add-AzDelegation** cmdlet adds a service delegation to an Azure subnet.</span></span>

## <span data-ttu-id="744a3-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="744a3-107">EXAMPLES</span></span>

### <span data-ttu-id="744a3-108">Exemplo 1: Adicionando uma delegação</span><span class="sxs-lookup"><span data-stu-id="744a3-108">Example 1: Adding a delegation</span></span>
```powershell
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet = Add-AzDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers" -Subnet $subnet
PS C:\> Set-AzVirtualNetwork $vnet
```

<span data-ttu-id="744a3-109">O primeiro comando recupera a rede virtual na qual a sub-rede está.</span><span class="sxs-lookup"><span data-stu-id="744a3-109">The first command retrieves the virtual network on which the subnet lies.</span></span> <span data-ttu-id="744a3-110">O segundo comando isola a sub-rede de interesse - a que você deseja delegar.</span><span class="sxs-lookup"><span data-stu-id="744a3-110">The second command isolates out the subnet of interest - the one which you want to delegate.</span></span> <span data-ttu-id="744a3-111">O terceiro comando adiciona uma delegação à sub-rede.</span><span class="sxs-lookup"><span data-stu-id="744a3-111">The third command adds a delegation to the subnet.</span></span> <span data-ttu-id="744a3-112">Este exemplo específico seria útil quando você deseja habilitar SQL criar pontos de extremidade da interface nesta sub-rede.</span><span class="sxs-lookup"><span data-stu-id="744a3-112">This particular example would be useful when you want to enable SQL to create interface endpoints in this subnet.</span></span> <span data-ttu-id="744a3-113">O comando final envia a sub-rede atualizada para o servidor para atualizar sua sub-rede.</span><span class="sxs-lookup"><span data-stu-id="744a3-113">The final command sends the updated subnet to the server to actually update your subnet.</span></span>

## <span data-ttu-id="744a3-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="744a3-114">PARAMETERS</span></span>

### <span data-ttu-id="744a3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="744a3-115">-DefaultProfile</span></span>
<span data-ttu-id="744a3-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="744a3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="744a3-117">-Name</span><span class="sxs-lookup"><span data-stu-id="744a3-117">-Name</span></span>
<span data-ttu-id="744a3-118">O nome da delegação</span><span class="sxs-lookup"><span data-stu-id="744a3-118">The name of the delegation</span></span>

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

### <span data-ttu-id="744a3-119">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="744a3-119">-ServiceName</span></span>
<span data-ttu-id="744a3-120">O nome do serviço ao qual a sub-rede deve ser delegada</span><span class="sxs-lookup"><span data-stu-id="744a3-120">The name of the service to which the subnet should be delegated</span></span>

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

### <span data-ttu-id="744a3-121">-Sub-rede</span><span class="sxs-lookup"><span data-stu-id="744a3-121">-Subnet</span></span>
<span data-ttu-id="744a3-122">A sub-rede</span><span class="sxs-lookup"><span data-stu-id="744a3-122">The subnet</span></span>

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

### <span data-ttu-id="744a3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="744a3-123">CommonParameters</span></span>
<span data-ttu-id="744a3-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="744a3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="744a3-125">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="744a3-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="744a3-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="744a3-126">INPUTS</span></span>

### <span data-ttu-id="744a3-127">System.String</span><span class="sxs-lookup"><span data-stu-id="744a3-127">System.String</span></span>

### <span data-ttu-id="744a3-128">Microsoft.Azure.Commands.Network.Models.PSSubnet</span><span class="sxs-lookup"><span data-stu-id="744a3-128">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="744a3-129">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="744a3-129">OUTPUTS</span></span>

### <span data-ttu-id="744a3-130">Microsoft.Azure.Commands.Network.Models.PSSubnet</span><span class="sxs-lookup"><span data-stu-id="744a3-130">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="744a3-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="744a3-131">NOTES</span></span>

## <span data-ttu-id="744a3-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="744a3-132">RELATED LINKS</span></span>

<span data-ttu-id="744a3-133">[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md) 
 [Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md) 
 [Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span><span class="sxs-lookup"><span data-stu-id="744a3-133">[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md)
[Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)
[Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span></span>