---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmDelegation.md
ms.openlocfilehash: 9912d41cd9e2600c55d378fbb88510a0defaaa85
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432296"
---
# <span data-ttu-id="cd9d4-101">New-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="cd9d4-101">New-AzureRmDelegation</span></span>

## <span data-ttu-id="cd9d4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cd9d4-102">SYNOPSIS</span></span>
<span data-ttu-id="cd9d4-103">Cria uma delegação de serviço.</span><span class="sxs-lookup"><span data-stu-id="cd9d4-103">Creates a service delegation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd9d4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cd9d4-104">SYNTAX</span></span>

```
New-AzureRmDelegation -Name <String> -ServiceName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cd9d4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cd9d4-105">DESCRIPTION</span></span>
<span data-ttu-id="cd9d4-106">O cmdlet **New-AzureRmDelegation** cria uma delegação de serviço que pode ser adicionada a uma sub-rede.</span><span class="sxs-lookup"><span data-stu-id="cd9d4-106">The **New-AzureRmDelegation** cmdlet creates a service delegation that can be added to a subnet.</span></span>

## <span data-ttu-id="cd9d4-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cd9d4-107">EXAMPLES</span></span>

### <span data-ttu-id="cd9d4-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="cd9d4-108">Example 1</span></span>
```powershell
PS C:\> $delegation = New-AzureRmDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers"
PS C:\> $vnet = Get-AzureRmVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet.Delegations.Add($delegation)
PS C:\> Set-AzureRmVirtualNetwork $vnet
```

<span data-ttu-id="cd9d4-109">O primeiro cmdlet cria uma delegação que pode ser adicionada a uma sub-rede e a armazena na variável $delegation.</span><span class="sxs-lookup"><span data-stu-id="cd9d4-109">The first cmdlet creates a delegation that can be added to a subnet, and stores it in the $delegation variable.</span></span> <span data-ttu-id="cd9d4-110">O segundo e terceiro cmdlets recuperam a sub-rede a ser delegada.</span><span class="sxs-lookup"><span data-stu-id="cd9d4-110">The second and third cmdlets retrieve the subnet to be delegated.</span></span> <span data-ttu-id="cd9d4-111">O quarto cmdlet adiciona a delegação criada à sub-rede de interesse, e o cmdlet final envia a configuração atualizada para o servidor.</span><span class="sxs-lookup"><span data-stu-id="cd9d4-111">The fourth cmdlet adds the created delegation to the subnet of interest, and the final cmdlet sends the updated configuration to the server.</span></span>

## <span data-ttu-id="cd9d4-112">OS</span><span class="sxs-lookup"><span data-stu-id="cd9d4-112">PARAMETERS</span></span>

### <span data-ttu-id="cd9d4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd9d4-113">-DefaultProfile</span></span>
<span data-ttu-id="cd9d4-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cd9d4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd9d4-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="cd9d4-115">-Name</span></span>
<span data-ttu-id="cd9d4-116">O nome da delegação</span><span class="sxs-lookup"><span data-stu-id="cd9d4-116">The name of the delegation</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd9d4-117">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="cd9d4-117">-ServiceName</span></span>
<span data-ttu-id="cd9d4-118">O nome do serviço para o qual a sub-rede deve ser delegada</span><span class="sxs-lookup"><span data-stu-id="cd9d4-118">The name of the service to which the subnet should be delegated</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd9d4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd9d4-119">CommonParameters</span></span>
<span data-ttu-id="cd9d4-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd9d4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="cd9d4-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd9d4-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd9d4-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cd9d4-122">INPUTS</span></span>

### <span data-ttu-id="cd9d4-123">System. String</span><span class="sxs-lookup"><span data-stu-id="cd9d4-123">System.String</span></span>

## <span data-ttu-id="cd9d4-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cd9d4-124">OUTPUTS</span></span>

### <span data-ttu-id="cd9d4-125">Microsoft.Azure.Commands.Network.Models.PSDelegation</span><span class="sxs-lookup"><span data-stu-id="cd9d4-125">Microsoft.Azure.Commands.Network.Models.PSDelegation</span></span>

## <span data-ttu-id="cd9d4-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cd9d4-126">NOTES</span></span>

## <span data-ttu-id="cd9d4-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cd9d4-127">RELATED LINKS</span></span>
<span data-ttu-id="cd9d4-128">[Add-AzureRmDelegation](./Add-AzureRmDelegation.md) 
 [Get-AzureRmDelegation](./Get-AzureRmDelegation.md) 
 [Remove-AzureRmDelegation](./Remove-AzureRmDelegation.md) 
 [Get-AzureRmVirtualNetwork](./Get-AzureRmVirtualNetwork.md) 
 [Get-AzureRmVirtualNetworkSubnetConfig](./Get-AzureRmVirtualNetworkSubnetConfig.md) 
 [Set-AzureRmVirtualNetwork](./Set-AzureRmVirtualNetwork.md)</span><span class="sxs-lookup"><span data-stu-id="cd9d4-128">[Add-AzureRmDelegation](./Add-AzureRmDelegation.md)
[Get-AzureRmDelegation](./Get-AzureRmDelegation.md)
[Remove-AzureRmDelegation](./Remove-AzureRmDelegation.md)
[Get-AzureRmVirtualNetwork](./Get-AzureRmVirtualNetwork.md)
[Get-AzureRmVirtualNetworkSubnetConfig](./Get-AzureRmVirtualNetworkSubnetConfig.md)
[Set-AzureRmVirtualNetwork](./Set-AzureRmVirtualNetwork.md)</span></span>
