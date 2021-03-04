---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 84FDB0F7-E6DE-4E1B-BD71-89535EDC6AA1
online version: https://docs.microsoft.com/powershell/module/az.network/get-azeffectiveroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzEffectiveRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzEffectiveRouteTable.md
ms.openlocfilehash: 28ec38b9f2dfbb658203aa46fe0d8225aca08a5e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887375"
---
# <span data-ttu-id="14978-101">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="14978-101">Get-AzEffectiveRouteTable</span></span>

## <span data-ttu-id="14978-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14978-102">SYNOPSIS</span></span>
<span data-ttu-id="14978-103">Obtém a tabela de rota eficaz de uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="14978-103">Gets the effective route table of a network interface.</span></span>

## <span data-ttu-id="14978-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="14978-104">SYNTAX</span></span>

```
Get-AzEffectiveRouteTable -NetworkInterfaceName <String> [-ResourceGroupName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14978-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="14978-105">DESCRIPTION</span></span>
<span data-ttu-id="14978-106">O cmdlet **Get-AzEffectiveRouteTable** retorna a tabela de rota efetiva aplicada em uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="14978-106">The **Get-AzEffectiveRouteTable** cmdlet returns the effective route table that is applied on a network interface.</span></span>

## <span data-ttu-id="14978-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="14978-107">EXAMPLES</span></span>

### <span data-ttu-id="14978-108">Exemplo 1: Obter a tabela de rota eficaz em uma interface de rede</span><span class="sxs-lookup"><span data-stu-id="14978-108">Example 1: Get the effective route table on a network interface</span></span>
```
PS C:\>Get-AzEffectiveRouteTable -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="14978-109">Este comando obtém a tabela de rota efetiva associada à interface de rede chamada MyNetworkInterface no grupo de recursos chamado MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="14978-109">This command gets the effective route table associated with network interface named MyNetworkInterface in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="14978-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="14978-110">PARAMETERS</span></span>

### <span data-ttu-id="14978-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="14978-111">-AsJob</span></span>
<span data-ttu-id="14978-112">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="14978-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="14978-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14978-113">-DefaultProfile</span></span>
<span data-ttu-id="14978-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="14978-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="14978-115">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="14978-115">-NetworkInterfaceName</span></span>
<span data-ttu-id="14978-116">Especificou o nome de uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="14978-116">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="14978-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14978-117">-ResourceGroupName</span></span>
<span data-ttu-id="14978-118">Especifica o grupo de recursos de uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="14978-118">Specifies the resource group of a network interface.</span></span>

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

### <span data-ttu-id="14978-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14978-119">CommonParameters</span></span>
<span data-ttu-id="14978-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14978-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14978-121">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="14978-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14978-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="14978-122">INPUTS</span></span>

### <span data-ttu-id="14978-123">System.String</span><span class="sxs-lookup"><span data-stu-id="14978-123">System.String</span></span>

## <span data-ttu-id="14978-124">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="14978-124">OUTPUTS</span></span>

### <span data-ttu-id="14978-125">Microsoft.Azure.Commands.Network.Models.PSEffectiveRoute</span><span class="sxs-lookup"><span data-stu-id="14978-125">Microsoft.Azure.Commands.Network.Models.PSEffectiveRoute</span></span>

## <span data-ttu-id="14978-126">NOTES</span><span class="sxs-lookup"><span data-stu-id="14978-126">NOTES</span></span>

## <span data-ttu-id="14978-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="14978-127">RELATED LINKS</span></span>

[<span data-ttu-id="14978-128">Get-AzEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="14978-128">Get-AzEffectiveNetworkSecurityGroup</span></span>](./Get-AzEffectiveNetworkSecurityGroup.md)


