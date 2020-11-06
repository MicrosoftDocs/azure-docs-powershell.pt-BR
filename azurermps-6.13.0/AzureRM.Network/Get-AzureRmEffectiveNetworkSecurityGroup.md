---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B9409AD6-F761-4B80-8E08-DBB2356F567D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermeffectivenetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmEffectiveNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmEffectiveNetworkSecurityGroup.md
ms.openlocfilehash: 565d0748104e537f448a40116a48f0cd34ebf16b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428070"
---
# <span data-ttu-id="2a432-101">Get-AzureRmEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="2a432-101">Get-AzureRmEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="2a432-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2a432-102">SYNOPSIS</span></span>
<span data-ttu-id="2a432-103">Obtém o grupo de segurança de rede efetivo de uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="2a432-103">Gets the effective network security group of a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2a432-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2a432-104">SYNTAX</span></span>

```
Get-AzureRmEffectiveNetworkSecurityGroup -NetworkInterfaceName <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2a432-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2a432-105">DESCRIPTION</span></span>
<span data-ttu-id="2a432-106">O cmdlet **Get-AzureRmEffectiveNetworkSecurityGroup** retorna o grupo de segurança de rede efetivo aplicado em uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="2a432-106">The **Get-AzureRmEffectiveNetworkSecurityGroup** cmdlet returns the effective network security group that is applied on a network interface.</span></span>

## <span data-ttu-id="2a432-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2a432-107">EXAMPLES</span></span>

### <span data-ttu-id="2a432-108">Exemplo 1: obter o grupo de segurança de rede efetivo em uma interface de rede</span><span class="sxs-lookup"><span data-stu-id="2a432-108">Example 1: Get the effective network security group on a network interface</span></span>
```
PS C:\>Get-AzureRmEffectiveNetworkSecurityGroup -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="2a432-109">Esse comando obtém todas as regras de segurança de rede efetivas associadas à interface de rede chamada mynetworkinterface no grupo de recursos chamado MyResource Group.</span><span class="sxs-lookup"><span data-stu-id="2a432-109">This command gets all of the effective network security rules associated with the network interface named MyNetworkInterface in the resource group named myResourceGroup.</span></span>

## <span data-ttu-id="2a432-110">OS</span><span class="sxs-lookup"><span data-stu-id="2a432-110">PARAMETERS</span></span>

### <span data-ttu-id="2a432-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a432-111">-DefaultProfile</span></span>
<span data-ttu-id="2a432-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2a432-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a432-113">-NetworkInterfacename</span><span class="sxs-lookup"><span data-stu-id="2a432-113">-NetworkInterfaceName</span></span>
<span data-ttu-id="2a432-114">Especificou o nome de uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="2a432-114">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="2a432-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a432-115">-ResourceGroupName</span></span>
<span data-ttu-id="2a432-116">Especifica o grupo de recursos de uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="2a432-116">Specifies the resource group of a network interface.</span></span>

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

### <span data-ttu-id="2a432-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a432-117">CommonParameters</span></span>
<span data-ttu-id="2a432-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a432-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a432-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a432-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a432-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2a432-120">INPUTS</span></span>

### <span data-ttu-id="2a432-121">System. String</span><span class="sxs-lookup"><span data-stu-id="2a432-121">System.String</span></span>

## <span data-ttu-id="2a432-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2a432-122">OUTPUTS</span></span>

### <span data-ttu-id="2a432-123">Microsoft. Azure. Commands. Network. Models. PSEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="2a432-123">Microsoft.Azure.Commands.Network.Models.PSEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="2a432-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2a432-124">NOTES</span></span>

## <span data-ttu-id="2a432-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2a432-125">RELATED LINKS</span></span>

[<span data-ttu-id="2a432-126">Get-AzureRmEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="2a432-126">Get-AzureRmEffectiveRouteTable</span></span>](./Get-AzureRmEffectiveRouteTable.md)


