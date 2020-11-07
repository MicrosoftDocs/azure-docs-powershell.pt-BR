---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B9409AD6-F761-4B80-8E08-DBB2356F567D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermeffectivenetworksecuritygroup
schema: 2.0.0
ms.openlocfilehash: 214ab7f91791fa05453e2f4ef4238440d9c78a3d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785514"
---
# <span data-ttu-id="5ab4c-101">Get-AzureRmEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5ab4c-101">Get-AzureRmEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="5ab4c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5ab4c-102">SYNOPSIS</span></span>
<span data-ttu-id="5ab4c-103">Obtém o grupo de segurança de rede efetivo de uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="5ab4c-103">Gets the effective network security group of a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ab4c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5ab4c-104">SYNTAX</span></span>

```
Get-AzureRmEffectiveNetworkSecurityGroup -NetworkInterfaceName <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ab4c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5ab4c-105">DESCRIPTION</span></span>
<span data-ttu-id="5ab4c-106">O cmdlet **Get-AzureRmEffectiveNetworkSecurityGroup** retorna o grupo de segurança de rede efetivo aplicado em uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="5ab4c-106">The **Get-AzureRmEffectiveNetworkSecurityGroup** cmdlet returns the effective network security group that is applied on a network interface.</span></span>

## <span data-ttu-id="5ab4c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5ab4c-107">EXAMPLES</span></span>

### <span data-ttu-id="5ab4c-108">Exemplo 1: obter o grupo de segurança de rede efetivo em uma interface de rede</span><span class="sxs-lookup"><span data-stu-id="5ab4c-108">Example 1: Get the effective network security group on a network interface</span></span>
```
PS C:\>Get-AzureRmEffectiveNetworkSecurityGroup -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="5ab4c-109">Esse comando obtém todas as regras de segurança de rede efetivas associadas à interface de rede chamada mynetworkinterface no grupo de recursos chamado MyResource Group.</span><span class="sxs-lookup"><span data-stu-id="5ab4c-109">This command gets all of the effective network security rules associated with the network interface named MyNetworkInterface in the resource group named myResourceGroup.</span></span>

## <span data-ttu-id="5ab4c-110">OS</span><span class="sxs-lookup"><span data-stu-id="5ab4c-110">PARAMETERS</span></span>

### <span data-ttu-id="5ab4c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ab4c-111">-DefaultProfile</span></span>
<span data-ttu-id="5ab4c-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5ab4c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5ab4c-113">-NetworkInterfacename</span><span class="sxs-lookup"><span data-stu-id="5ab4c-113">-NetworkInterfaceName</span></span>
<span data-ttu-id="5ab4c-114">Especificou o nome de uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="5ab4c-114">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="5ab4c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ab4c-115">-ResourceGroupName</span></span>
<span data-ttu-id="5ab4c-116">Especifica o grupo de recursos de uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="5ab4c-116">Specifies the resource group of a network interface.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ab4c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ab4c-117">CommonParameters</span></span>
<span data-ttu-id="5ab4c-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ab4c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ab4c-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ab4c-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ab4c-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5ab4c-120">INPUTS</span></span>

## <span data-ttu-id="5ab4c-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5ab4c-121">OUTPUTS</span></span>

### <span data-ttu-id="5ab4c-122">Microsoft. Azure. Commands. Network. Models. PSEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5ab4c-122">Microsoft.Azure.Commands.Network.Models.PSEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="5ab4c-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5ab4c-123">NOTES</span></span>

## <span data-ttu-id="5ab4c-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5ab4c-124">RELATED LINKS</span></span>

[<span data-ttu-id="5ab4c-125">Get-AzureRmEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="5ab4c-125">Get-AzureRmEffectiveRouteTable</span></span>](./Get-AzureRmEffectiveRouteTable.md)


