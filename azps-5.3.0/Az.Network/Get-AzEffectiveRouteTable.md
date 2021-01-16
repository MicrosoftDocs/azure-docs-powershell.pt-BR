---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 84FDB0F7-E6DE-4E1B-BD71-89535EDC6AA1
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azeffectiveroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzEffectiveRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzEffectiveRouteTable.md
ms.openlocfilehash: e7d65e7797fb606306f0f0cc1e7c394fcf3d1d3d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98271890"
---
# <span data-ttu-id="4542f-101">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="4542f-101">Get-AzEffectiveRouteTable</span></span>

## <span data-ttu-id="4542f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4542f-102">SYNOPSIS</span></span>
<span data-ttu-id="4542f-103">Obtém a tabela de rotas efetivas de uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="4542f-103">Gets the effective route table of a network interface.</span></span>

## <span data-ttu-id="4542f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4542f-104">SYNTAX</span></span>

```
Get-AzEffectiveRouteTable -NetworkInterfaceName <String> [-ResourceGroupName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4542f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4542f-105">DESCRIPTION</span></span>
<span data-ttu-id="4542f-106">O cmdlet **Get-AzEffectiveRouteTable** retorna a tabela de rota efetiva que é aplicada em uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="4542f-106">The **Get-AzEffectiveRouteTable** cmdlet returns the effective route table that is applied on a network interface.</span></span>

## <span data-ttu-id="4542f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4542f-107">EXAMPLES</span></span>

### <span data-ttu-id="4542f-108">Exemplo 1: obter a tabela de rotas efetivas em uma interface de rede</span><span class="sxs-lookup"><span data-stu-id="4542f-108">Example 1: Get the effective route table on a network interface</span></span>
```
PS C:\>Get-AzEffectiveRouteTable -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="4542f-109">Esse comando obtém a tabela de rotas efetivas associada à interface de rede chamada mynetworkinterface no grupo de recursos chamado MyResource Group.</span><span class="sxs-lookup"><span data-stu-id="4542f-109">This command gets the effective route table associated with network interface named MyNetworkInterface in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="4542f-110">OS</span><span class="sxs-lookup"><span data-stu-id="4542f-110">PARAMETERS</span></span>

### <span data-ttu-id="4542f-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4542f-111">-AsJob</span></span>
<span data-ttu-id="4542f-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="4542f-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4542f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4542f-113">-DefaultProfile</span></span>
<span data-ttu-id="4542f-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4542f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4542f-115">-NetworkInterfacename</span><span class="sxs-lookup"><span data-stu-id="4542f-115">-NetworkInterfaceName</span></span>
<span data-ttu-id="4542f-116">Especificou o nome de uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="4542f-116">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="4542f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4542f-117">-ResourceGroupName</span></span>
<span data-ttu-id="4542f-118">Especifica o grupo de recursos de uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="4542f-118">Specifies the resource group of a network interface.</span></span>

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

### <span data-ttu-id="4542f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4542f-119">CommonParameters</span></span>
<span data-ttu-id="4542f-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4542f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4542f-121">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4542f-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4542f-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4542f-122">INPUTS</span></span>

### <span data-ttu-id="4542f-123">System. String</span><span class="sxs-lookup"><span data-stu-id="4542f-123">System.String</span></span>

## <span data-ttu-id="4542f-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4542f-124">OUTPUTS</span></span>

### <span data-ttu-id="4542f-125">Microsoft. Azure. Commands. Network. Models. PSEffectiveRoute</span><span class="sxs-lookup"><span data-stu-id="4542f-125">Microsoft.Azure.Commands.Network.Models.PSEffectiveRoute</span></span>

## <span data-ttu-id="4542f-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4542f-126">NOTES</span></span>

## <span data-ttu-id="4542f-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4542f-127">RELATED LINKS</span></span>

[<span data-ttu-id="4542f-128">Get-AzEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="4542f-128">Get-AzEffectiveNetworkSecurityGroup</span></span>](./Get-AzEffectiveNetworkSecurityGroup.md)


