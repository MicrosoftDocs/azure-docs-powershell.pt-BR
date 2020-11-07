---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 84FDB0F7-E6DE-4E1B-BD71-89535EDC6AA1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermeffectiveroutetable
schema: 2.0.0
ms.openlocfilehash: 403a3d37418e022032988d5d7fccb40a1e79f449
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785513"
---
# <span data-ttu-id="4abbc-101">Get-AzureRmEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="4abbc-101">Get-AzureRmEffectiveRouteTable</span></span>

## <span data-ttu-id="4abbc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4abbc-102">SYNOPSIS</span></span>
<span data-ttu-id="4abbc-103">Obtém a tabela de rotas efetivas de uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="4abbc-103">Gets the effective route table of a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4abbc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4abbc-104">SYNTAX</span></span>

```
Get-AzureRmEffectiveRouteTable -NetworkInterfaceName <String> [-ResourceGroupName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4abbc-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4abbc-105">DESCRIPTION</span></span>
<span data-ttu-id="4abbc-106">O cmdlet **Get-AzureRmEffectiveRouteTable** retorna a tabela de rota efetiva que é aplicada em uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="4abbc-106">The **Get-AzureRmEffectiveRouteTable** cmdlet returns the effective route table that is applied on a network interface.</span></span>

## <span data-ttu-id="4abbc-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4abbc-107">EXAMPLES</span></span>

### <span data-ttu-id="4abbc-108">Exemplo 1: obter a tabela de rotas efetivas em uma interface de rede</span><span class="sxs-lookup"><span data-stu-id="4abbc-108">Example 1: Get the effective route table on a network interface</span></span>
```
PS C:\>Get-AzureRmEffectiveRouteTable -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="4abbc-109">Esse comando obtém a tabela de rotas efetivas associada à interface de rede chamada mynetworkinterface no grupo de recursos chamado MyResource Group.</span><span class="sxs-lookup"><span data-stu-id="4abbc-109">This command gets the effective route table associated with network interface named MyNetworkInterface in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="4abbc-110">OS</span><span class="sxs-lookup"><span data-stu-id="4abbc-110">PARAMETERS</span></span>

### <span data-ttu-id="4abbc-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4abbc-111">-AsJob</span></span>
<span data-ttu-id="4abbc-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="4abbc-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4abbc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4abbc-113">-DefaultProfile</span></span>
<span data-ttu-id="4abbc-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4abbc-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4abbc-115">-NetworkInterfacename</span><span class="sxs-lookup"><span data-stu-id="4abbc-115">-NetworkInterfaceName</span></span>
<span data-ttu-id="4abbc-116">Especificou o nome de uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="4abbc-116">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="4abbc-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4abbc-117">-ResourceGroupName</span></span>
<span data-ttu-id="4abbc-118">Especifica o grupo de recursos de uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="4abbc-118">Specifies the resource group of a network interface.</span></span>

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

### <span data-ttu-id="4abbc-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4abbc-119">CommonParameters</span></span>
<span data-ttu-id="4abbc-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4abbc-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4abbc-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4abbc-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4abbc-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4abbc-122">INPUTS</span></span>

## <span data-ttu-id="4abbc-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4abbc-123">OUTPUTS</span></span>

### <span data-ttu-id="4abbc-124">Microsoft. Azure. Commands. Network. Models. PSEffectiveRoute</span><span class="sxs-lookup"><span data-stu-id="4abbc-124">Microsoft.Azure.Commands.Network.Models.PSEffectiveRoute</span></span>

## <span data-ttu-id="4abbc-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4abbc-125">NOTES</span></span>

## <span data-ttu-id="4abbc-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4abbc-126">RELATED LINKS</span></span>

[<span data-ttu-id="4abbc-127">Get-AzureRmEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="4abbc-127">Get-AzureRmEffectiveNetworkSecurityGroup</span></span>](./Get-AzureRmEffectiveNetworkSecurityGroup.md)


