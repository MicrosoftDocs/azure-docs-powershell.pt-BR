---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 84FDB0F7-E6DE-4E1B-BD71-89535EDC6AA1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmEffectiveRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmEffectiveRouteTable.md
ms.openlocfilehash: f42e378bb0bb5202f9f955dea1b844e343a0e037
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431111"
---
# <span data-ttu-id="9a5d7-101">Get-AzureRmEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="9a5d7-101">Get-AzureRmEffectiveRouteTable</span></span>

## <span data-ttu-id="9a5d7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9a5d7-102">SYNOPSIS</span></span>
<span data-ttu-id="9a5d7-103">Obtém a tabela de rotas efetivas de uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="9a5d7-103">Gets the effective route table of a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9a5d7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9a5d7-104">SYNTAX</span></span>

```
Get-AzureRmEffectiveRouteTable -NetworkInterfaceName <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9a5d7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9a5d7-105">DESCRIPTION</span></span>
<span data-ttu-id="9a5d7-106">O cmdlet **Get-AzureRmEffectiveRouteTable** retorna a tabela de rota efetiva que é aplicada em uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="9a5d7-106">The **Get-AzureRmEffectiveRouteTable** cmdlet returns the effective route table that is applied on a network interface.</span></span>

## <span data-ttu-id="9a5d7-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9a5d7-107">EXAMPLES</span></span>

### <span data-ttu-id="9a5d7-108">Exemplo 1: obter a tabela de rotas efetivas em uma interface de rede</span><span class="sxs-lookup"><span data-stu-id="9a5d7-108">Example 1: Get the effective route table on a network interface</span></span>
```
PS C:\>Get-AzureRmEffectiveRouteTable -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="9a5d7-109">Esse comando obtém a tabela de rotas efetivas associada à interface de rede chamada mynetworkinterface no grupo de recursos chamado MyResource Group.</span><span class="sxs-lookup"><span data-stu-id="9a5d7-109">This command gets the effective route table associated with network interface named MyNetworkInterface in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="9a5d7-110">OS</span><span class="sxs-lookup"><span data-stu-id="9a5d7-110">PARAMETERS</span></span>

### <span data-ttu-id="9a5d7-111">-NetworkInterfacename</span><span class="sxs-lookup"><span data-stu-id="9a5d7-111">-NetworkInterfaceName</span></span>
<span data-ttu-id="9a5d7-112">Especificou o nome de uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="9a5d7-112">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="9a5d7-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a5d7-113">-ResourceGroupName</span></span>
<span data-ttu-id="9a5d7-114">Especifica o grupo de recursos de uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="9a5d7-114">Specifies the resource group of a network interface.</span></span>

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

### <span data-ttu-id="9a5d7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a5d7-115">-DefaultProfile</span></span>
<span data-ttu-id="9a5d7-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9a5d7-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9a5d7-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a5d7-117">CommonParameters</span></span>
<span data-ttu-id="9a5d7-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a5d7-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a5d7-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a5d7-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a5d7-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9a5d7-120">INPUTS</span></span>

## <span data-ttu-id="9a5d7-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9a5d7-121">OUTPUTS</span></span>

### <span data-ttu-id="9a5d7-122">Microsoft. Azure. Commands. Network. Models. PSEffectiveRoute</span><span class="sxs-lookup"><span data-stu-id="9a5d7-122">Microsoft.Azure.Commands.Network.Models.PSEffectiveRoute</span></span>

## <span data-ttu-id="9a5d7-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9a5d7-123">NOTES</span></span>

## <span data-ttu-id="9a5d7-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9a5d7-124">RELATED LINKS</span></span>

[<span data-ttu-id="9a5d7-125">Get-AzureRmEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="9a5d7-125">Get-AzureRmEffectiveNetworkSecurityGroup</span></span>](./Get-AzureRmEffectiveNetworkSecurityGroup.md)


