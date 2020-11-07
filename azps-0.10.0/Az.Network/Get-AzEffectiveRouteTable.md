---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 84FDB0F7-E6DE-4E1B-BD71-89535EDC6AA1
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azeffectiveroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzEffectiveRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzEffectiveRouteTable.md
ms.openlocfilehash: 37c9827f2af970c0c376c31f4d67ba7723e02e99
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775562"
---
# <span data-ttu-id="d92e5-101">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="d92e5-101">Get-AzEffectiveRouteTable</span></span>

## <span data-ttu-id="d92e5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d92e5-102">SYNOPSIS</span></span>
<span data-ttu-id="d92e5-103">Obtém a tabela de rotas efetivas de uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="d92e5-103">Gets the effective route table of a network interface.</span></span>

## <span data-ttu-id="d92e5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d92e5-104">SYNTAX</span></span>

```
Get-AzEffectiveRouteTable -NetworkInterfaceName <String> [-ResourceGroupName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d92e5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d92e5-105">DESCRIPTION</span></span>
<span data-ttu-id="d92e5-106">O cmdlet **Get-AzEffectiveRouteTable** retorna a tabela de rota efetiva que é aplicada em uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="d92e5-106">The **Get-AzEffectiveRouteTable** cmdlet returns the effective route table that is applied on a network interface.</span></span>

## <span data-ttu-id="d92e5-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d92e5-107">EXAMPLES</span></span>

### <span data-ttu-id="d92e5-108">Exemplo 1: obter a tabela de rotas efetivas em uma interface de rede</span><span class="sxs-lookup"><span data-stu-id="d92e5-108">Example 1: Get the effective route table on a network interface</span></span>
```
PS C:\>Get-AzEffectiveRouteTable -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="d92e5-109">Esse comando obtém a tabela de rotas efetivas associada à interface de rede chamada mynetworkinterface no grupo de recursos chamado MyResource Group.</span><span class="sxs-lookup"><span data-stu-id="d92e5-109">This command gets the effective route table associated with network interface named MyNetworkInterface in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="d92e5-110">OS</span><span class="sxs-lookup"><span data-stu-id="d92e5-110">PARAMETERS</span></span>

### <span data-ttu-id="d92e5-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d92e5-111">-AsJob</span></span>
<span data-ttu-id="d92e5-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="d92e5-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d92e5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d92e5-113">-DefaultProfile</span></span>
<span data-ttu-id="d92e5-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d92e5-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d92e5-115">-NetworkInterfacename</span><span class="sxs-lookup"><span data-stu-id="d92e5-115">-NetworkInterfaceName</span></span>
<span data-ttu-id="d92e5-116">Especificou o nome de uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="d92e5-116">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="d92e5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d92e5-117">-ResourceGroupName</span></span>
<span data-ttu-id="d92e5-118">Especifica o grupo de recursos de uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="d92e5-118">Specifies the resource group of a network interface.</span></span>

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

### <span data-ttu-id="d92e5-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d92e5-119">CommonParameters</span></span>
<span data-ttu-id="d92e5-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d92e5-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d92e5-121">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d92e5-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d92e5-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d92e5-122">INPUTS</span></span>

## <span data-ttu-id="d92e5-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d92e5-123">OUTPUTS</span></span>

### <span data-ttu-id="d92e5-124">Microsoft. Azure. Commands. Network. Models. PSEffectiveRoute</span><span class="sxs-lookup"><span data-stu-id="d92e5-124">Microsoft.Azure.Commands.Network.Models.PSEffectiveRoute</span></span>

## <span data-ttu-id="d92e5-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d92e5-125">NOTES</span></span>

## <span data-ttu-id="d92e5-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d92e5-126">RELATED LINKS</span></span>

[<span data-ttu-id="d92e5-127">Get-AzEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="d92e5-127">Get-AzEffectiveNetworkSecurityGroup</span></span>](./Get-AzEffectiveNetworkSecurityGroup.md)

