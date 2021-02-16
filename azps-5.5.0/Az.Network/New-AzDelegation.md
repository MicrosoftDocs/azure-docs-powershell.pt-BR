---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzDelegation.md
ms.openlocfilehash: 05ed0d27dc1d004c2d9a1c5221795af708b812d7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118327"
---
# <span data-ttu-id="a7810-101">New-AzDelegation</span><span class="sxs-lookup"><span data-stu-id="a7810-101">New-AzDelegation</span></span>

## <span data-ttu-id="a7810-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a7810-102">SYNOPSIS</span></span>
<span data-ttu-id="a7810-103">Cria uma delegação de serviços.</span><span class="sxs-lookup"><span data-stu-id="a7810-103">Creates a service delegation.</span></span>

## <span data-ttu-id="a7810-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a7810-104">SYNTAX</span></span>

```
New-AzDelegation -Name <String> -ServiceName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a7810-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="a7810-105">DESCRIPTION</span></span>
<span data-ttu-id="a7810-106">O **cmdlet New-AzDelegation** cria uma delegação de serviços que pode ser adicionada a uma sub-rede.</span><span class="sxs-lookup"><span data-stu-id="a7810-106">The **New-AzDelegation** cmdlet creates a service delegation that can be added to a subnet.</span></span>

## <span data-ttu-id="a7810-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a7810-107">EXAMPLES</span></span>

### <span data-ttu-id="a7810-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a7810-108">Example 1</span></span>
```powershell
PS C:\> $delegation = New-AzDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers"
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet.Delegations.Add($delegation)
PS C:\> Set-AzVirtualNetwork $vnet
```

<span data-ttu-id="a7810-109">O primeiro cmdlet cria uma delegação que pode ser adicionada a uma sub-rede e a armazena na variável $delegation dados.</span><span class="sxs-lookup"><span data-stu-id="a7810-109">The first cmdlet creates a delegation that can be added to a subnet, and stores it in the $delegation variable.</span></span> <span data-ttu-id="a7810-110">O segundo e o terceiro cmdlets recuperam a sub-rede para serem delegados.</span><span class="sxs-lookup"><span data-stu-id="a7810-110">The second and third cmdlets retrieve the subnet to be delegated.</span></span> <span data-ttu-id="a7810-111">O quarto cmdlet adiciona a delegação criada à sub-rede de interesse, e o cmdlet final envia a configuração atualizada para o servidor.</span><span class="sxs-lookup"><span data-stu-id="a7810-111">The fourth cmdlet adds the created delegation to the subnet of interest, and the final cmdlet sends the updated configuration to the server.</span></span>

## <span data-ttu-id="a7810-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a7810-112">PARAMETERS</span></span>

### <span data-ttu-id="a7810-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7810-113">-DefaultProfile</span></span>
<span data-ttu-id="a7810-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a7810-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7810-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="a7810-115">-Name</span></span>
<span data-ttu-id="a7810-116">O nome da delegação</span><span class="sxs-lookup"><span data-stu-id="a7810-116">The name of the delegation</span></span>

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

### <span data-ttu-id="a7810-117">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="a7810-117">-ServiceName</span></span>
<span data-ttu-id="a7810-118">O nome do serviço ao qual a sub-rede deve ser delegada</span><span class="sxs-lookup"><span data-stu-id="a7810-118">The name of the service to which the subnet should be delegated</span></span>

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

### <span data-ttu-id="a7810-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7810-119">CommonParameters</span></span>
<span data-ttu-id="a7810-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7810-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7810-121">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7810-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7810-122">Entradas</span><span class="sxs-lookup"><span data-stu-id="a7810-122">INPUTS</span></span>

### <span data-ttu-id="a7810-123">System.String</span><span class="sxs-lookup"><span data-stu-id="a7810-123">System.String</span></span>

## <span data-ttu-id="a7810-124">Saídas</span><span class="sxs-lookup"><span data-stu-id="a7810-124">OUTPUTS</span></span>

### <span data-ttu-id="a7810-125">Microsoft.Azure.Commands.Network.Models.PSDelegation</span><span class="sxs-lookup"><span data-stu-id="a7810-125">Microsoft.Azure.Commands.Network.Models.PSDelegation</span></span>

## <span data-ttu-id="a7810-126">Notas</span><span class="sxs-lookup"><span data-stu-id="a7810-126">NOTES</span></span>

## <span data-ttu-id="a7810-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a7810-127">RELATED LINKS</span></span>

<span data-ttu-id="a7810-128">[Add-AzDelegation](./Add-AzDelegation.md) 
 [Get-AzDelegation](./Get-AzDelegation.md) 
 [Remove-AzDelegation](./Remove-AzDelegation.md) 
 [Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md) 
 [Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md) 
 [Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span><span class="sxs-lookup"><span data-stu-id="a7810-128">[Add-AzDelegation](./Add-AzDelegation.md)
[Get-AzDelegation](./Get-AzDelegation.md)
[Remove-AzDelegation](./Remove-AzDelegation.md)
[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md)
[Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)
[Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span></span>