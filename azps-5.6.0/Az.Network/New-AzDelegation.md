---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzDelegation.md
ms.openlocfilehash: d383ddc5c7e0cf1b4ddb618fa11089883049d327
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886206"
---
# <span data-ttu-id="fb2d5-101">New-AzDelegation</span><span class="sxs-lookup"><span data-stu-id="fb2d5-101">New-AzDelegation</span></span>

## <span data-ttu-id="fb2d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb2d5-102">SYNOPSIS</span></span>
<span data-ttu-id="fb2d5-103">Cria uma delegação de serviço.</span><span class="sxs-lookup"><span data-stu-id="fb2d5-103">Creates a service delegation.</span></span>

## <span data-ttu-id="fb2d5-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="fb2d5-104">SYNTAX</span></span>

```
New-AzDelegation -Name <String> -ServiceName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fb2d5-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="fb2d5-105">DESCRIPTION</span></span>
<span data-ttu-id="fb2d5-106">O cmdlet **New-AzDelegation** cria uma delegação de serviço que pode ser adicionada a uma sub-rede.</span><span class="sxs-lookup"><span data-stu-id="fb2d5-106">The **New-AzDelegation** cmdlet creates a service delegation that can be added to a subnet.</span></span>

## <span data-ttu-id="fb2d5-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fb2d5-107">EXAMPLES</span></span>

### <span data-ttu-id="fb2d5-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fb2d5-108">Example 1</span></span>
```powershell
PS C:\> $delegation = New-AzDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers"
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet.Delegations.Add($delegation)
PS C:\> Set-AzVirtualNetwork $vnet
```

<span data-ttu-id="fb2d5-109">O primeiro cmdlet cria uma delegação que pode ser adicionada a uma sub-rede e a armazena na $delegation variável.</span><span class="sxs-lookup"><span data-stu-id="fb2d5-109">The first cmdlet creates a delegation that can be added to a subnet, and stores it in the $delegation variable.</span></span> <span data-ttu-id="fb2d5-110">O segundo e o terceiro cmdlets recuperam a sub-rede a ser delegada.</span><span class="sxs-lookup"><span data-stu-id="fb2d5-110">The second and third cmdlets retrieve the subnet to be delegated.</span></span> <span data-ttu-id="fb2d5-111">O quarto cmdlet adiciona a delegação criada à sub-rede de interesse, e o cmdlet final envia a configuração atualizada para o servidor.</span><span class="sxs-lookup"><span data-stu-id="fb2d5-111">The fourth cmdlet adds the created delegation to the subnet of interest, and the final cmdlet sends the updated configuration to the server.</span></span>

## <span data-ttu-id="fb2d5-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="fb2d5-112">PARAMETERS</span></span>

### <span data-ttu-id="fb2d5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb2d5-113">-DefaultProfile</span></span>
<span data-ttu-id="fb2d5-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fb2d5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb2d5-115">-Name</span><span class="sxs-lookup"><span data-stu-id="fb2d5-115">-Name</span></span>
<span data-ttu-id="fb2d5-116">O nome da delegação</span><span class="sxs-lookup"><span data-stu-id="fb2d5-116">The name of the delegation</span></span>

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

### <span data-ttu-id="fb2d5-117">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="fb2d5-117">-ServiceName</span></span>
<span data-ttu-id="fb2d5-118">O nome do serviço ao qual a sub-rede deve ser delegada</span><span class="sxs-lookup"><span data-stu-id="fb2d5-118">The name of the service to which the subnet should be delegated</span></span>

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

### <span data-ttu-id="fb2d5-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb2d5-119">CommonParameters</span></span>
<span data-ttu-id="fb2d5-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb2d5-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb2d5-121">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb2d5-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb2d5-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fb2d5-122">INPUTS</span></span>

### <span data-ttu-id="fb2d5-123">System.String</span><span class="sxs-lookup"><span data-stu-id="fb2d5-123">System.String</span></span>

## <span data-ttu-id="fb2d5-124">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="fb2d5-124">OUTPUTS</span></span>

### <span data-ttu-id="fb2d5-125">Microsoft.Azure.Commands.Network.Models.PSDelegation</span><span class="sxs-lookup"><span data-stu-id="fb2d5-125">Microsoft.Azure.Commands.Network.Models.PSDelegation</span></span>

## <span data-ttu-id="fb2d5-126">NOTES</span><span class="sxs-lookup"><span data-stu-id="fb2d5-126">NOTES</span></span>

## <span data-ttu-id="fb2d5-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fb2d5-127">RELATED LINKS</span></span>

<span data-ttu-id="fb2d5-128">[Add-AzDelegation](./Add-AzDelegation.md) 
 [Get-AzDelegation](./Get-AzDelegation.md) 
 [Remove-AzDelegation](./Remove-AzDelegation.md) 
 [Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md) 
 [Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md) 
 [Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span><span class="sxs-lookup"><span data-stu-id="fb2d5-128">[Add-AzDelegation](./Add-AzDelegation.md)
[Get-AzDelegation](./Get-AzDelegation.md)
[Remove-AzDelegation](./Remove-AzDelegation.md)
[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md)
[Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)
[Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span></span>