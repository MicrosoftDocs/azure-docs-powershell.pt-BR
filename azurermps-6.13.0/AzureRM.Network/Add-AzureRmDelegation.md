---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmDelegation.md
ms.openlocfilehash: 0306d327bf7e93eedd040979912622b2dcbc09d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433218"
---
# <span data-ttu-id="4446b-101">Add-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="4446b-101">Add-AzureRmDelegation</span></span>

## <span data-ttu-id="4446b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4446b-102">SYNOPSIS</span></span>
<span data-ttu-id="4446b-103">Adiciona uma delegação a uma sub-rede.</span><span class="sxs-lookup"><span data-stu-id="4446b-103">Adds a delegation to a subnet.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4446b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4446b-104">SYNTAX</span></span>

```
Add-AzureRmDelegation -Name <String> -ServiceName <String> -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4446b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4446b-105">DESCRIPTION</span></span>
<span data-ttu-id="4446b-106">O cmdlet **Add-AzureRmDelegation** adiciona uma delegação de serviço a uma sub-rede do Azure.</span><span class="sxs-lookup"><span data-stu-id="4446b-106">The **Add-AzureRmDelegation** cmdlet adds a service delegation to an Azure subnet.</span></span>

## <span data-ttu-id="4446b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4446b-107">EXAMPLES</span></span>

### <span data-ttu-id="4446b-108">1: adicionando uma delegação</span><span class="sxs-lookup"><span data-stu-id="4446b-108">1: Adding a delegation</span></span>
```powershell
PS C:\> $vnet = Get-AzureRmVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet = Add-AzureRmDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers" -Subnet $subnet
PS C:\> Set-AzureRmVirtualNetwork $vnet
```

<span data-ttu-id="4446b-109">O primeiro comando recupera a rede virtual na qual a sub-rede se encontra.</span><span class="sxs-lookup"><span data-stu-id="4446b-109">The first command retrieves the virtual network on which the subnet lies.</span></span> <span data-ttu-id="4446b-110">O segundo comando isola a sub-rede de interesse-aquela que você deseja delegar.</span><span class="sxs-lookup"><span data-stu-id="4446b-110">The second command isolates out the subnet of interest - the one which you want to delegate.</span></span> <span data-ttu-id="4446b-111">O terceiro comando adiciona uma delegação à sub-rede.</span><span class="sxs-lookup"><span data-stu-id="4446b-111">The third command adds a delegation to the subnet.</span></span> <span data-ttu-id="4446b-112">Esse exemplo específico seria útil quando você quiser habilitar o SQL para criar pontos de extremidade de interface nessa sub-rede.</span><span class="sxs-lookup"><span data-stu-id="4446b-112">This particular example would be useful when you want to enable SQL to create interface endpoints in this subnet.</span></span> <span data-ttu-id="4446b-113">O comando final envia a sub-rede atualizada ao servidor para realmente atualizar sua sub-rede.</span><span class="sxs-lookup"><span data-stu-id="4446b-113">The final command sends the updated subnet to the server to actually update your subnet.</span></span>

## <span data-ttu-id="4446b-114">OS</span><span class="sxs-lookup"><span data-stu-id="4446b-114">PARAMETERS</span></span>

### <span data-ttu-id="4446b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4446b-115">-DefaultProfile</span></span>
<span data-ttu-id="4446b-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4446b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4446b-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="4446b-117">-Name</span></span>
<span data-ttu-id="4446b-118">O nome da delegação</span><span class="sxs-lookup"><span data-stu-id="4446b-118">The name of the delegation</span></span>

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

### <span data-ttu-id="4446b-119">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="4446b-119">-ServiceName</span></span>
<span data-ttu-id="4446b-120">O nome do serviço para o qual a sub-rede deve ser delegada</span><span class="sxs-lookup"><span data-stu-id="4446b-120">The name of the service to which the subnet should be delegated</span></span>

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

### <span data-ttu-id="4446b-121">-Subnet</span><span class="sxs-lookup"><span data-stu-id="4446b-121">-Subnet</span></span>
<span data-ttu-id="4446b-122">A sub-rede</span><span class="sxs-lookup"><span data-stu-id="4446b-122">The subnet</span></span>

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

### <span data-ttu-id="4446b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4446b-123">CommonParameters</span></span>
<span data-ttu-id="4446b-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4446b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="4446b-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4446b-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4446b-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4446b-126">INPUTS</span></span>

### <span data-ttu-id="4446b-127">System. String</span><span class="sxs-lookup"><span data-stu-id="4446b-127">System.String</span></span>

### <span data-ttu-id="4446b-128">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="4446b-128">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="4446b-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4446b-129">OUTPUTS</span></span>

### <span data-ttu-id="4446b-130">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="4446b-130">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="4446b-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4446b-131">NOTES</span></span>

## <span data-ttu-id="4446b-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4446b-132">RELATED LINKS</span></span>
<span data-ttu-id="4446b-133">[Get-AzureRmVirtualNetwork](./Get-AzureRmVirtualNetwork.md) 
 [Get-AzureRmVirtualNetworkSubnetConfig](./Get-AzureRmVirtualNetworkSubnetConfig.md) 
 [Set-AzureRmVirtualNetwork](./Set-AzureRmVirtualNetwork.md)</span><span class="sxs-lookup"><span data-stu-id="4446b-133">[Get-AzureRmVirtualNetwork](./Get-AzureRmVirtualNetwork.md)
[Get-AzureRmVirtualNetworkSubnetConfig](./Get-AzureRmVirtualNetworkSubnetConfig.md)
[Set-AzureRmVirtualNetwork](./Set-AzureRmVirtualNetwork.md)</span></span>
