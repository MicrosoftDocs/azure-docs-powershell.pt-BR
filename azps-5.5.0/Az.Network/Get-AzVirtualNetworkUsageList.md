---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkusagelist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkUsageList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkUsageList.md
ms.openlocfilehash: 023eb245132a7b451fc6e30351db5751fb754cde
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112871"
---
# <span data-ttu-id="746cb-101">Get-AzVirtualNetworkUsageList</span><span class="sxs-lookup"><span data-stu-id="746cb-101">Get-AzVirtualNetworkUsageList</span></span>

## <span data-ttu-id="746cb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="746cb-102">SYNOPSIS</span></span>
<span data-ttu-id="746cb-103">Obtém o uso atual da rede virtual.</span><span class="sxs-lookup"><span data-stu-id="746cb-103">Gets virtual network current usage.</span></span>

## <span data-ttu-id="746cb-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="746cb-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkUsageList -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="746cb-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="746cb-105">DESCRIPTION</span></span>
<span data-ttu-id="746cb-106">O cmdlet **Get-AzVirtualNetworkUsageList** obtém o uso de sub-rede para a rede virtual especificada.</span><span class="sxs-lookup"><span data-stu-id="746cb-106">The **Get-AzVirtualNetworkUsageList** cmdlet gets per subnet usage for the specified virtual network.</span></span>

## <span data-ttu-id="746cb-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="746cb-107">EXAMPLES</span></span>

### <span data-ttu-id="746cb-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="746cb-108">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkUsageList -ResourceGroupName test -Name usagetest

Get-AzVirtualNetworkUsageList -ResourceGroupName test -Name usagetest

Name         : Subnet size and usage
Id           : /subscriptions/sub1/resourceGroups/test/providers/Microsoft.Network/virtualNetworks/usagetest/subnets/subnet
CurrentValue : 1
Limit        : 65531
Unit         : Count

Name         : Subnet size and usage
Id           : /subscriptions/sub1/resourceGroups/test/providers/Microsoft.Network/virtualNetworks/usagetest/subnets/subnet11
CurrentValue : 0
Limit        : 251
Unit         : Count
```

<span data-ttu-id="746cb-109">Obtém por sub-rede os valores atuais de uso para a rede virtual de teste de uso.</span><span class="sxs-lookup"><span data-stu-id="746cb-109">Gets per subnet current values of usage for usagetest virtual network.</span></span>

## <span data-ttu-id="746cb-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="746cb-110">PARAMETERS</span></span>

### <span data-ttu-id="746cb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="746cb-111">-DefaultProfile</span></span>
<span data-ttu-id="746cb-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="746cb-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="746cb-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="746cb-113">-Name</span></span>
<span data-ttu-id="746cb-114">Especifica o nome da rede virtual para o que mostrar os usos.</span><span class="sxs-lookup"><span data-stu-id="746cb-114">Specifies the name of the virtual network to show usages for.</span></span>

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

### <span data-ttu-id="746cb-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="746cb-115">-ResourceGroupName</span></span>
<span data-ttu-id="746cb-116">Especifica o nome do grupo de recursos ao que a rede virtual pertence.</span><span class="sxs-lookup"><span data-stu-id="746cb-116">Specifies the name of the resource group that virtual network belongs to.</span></span>

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

### <span data-ttu-id="746cb-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="746cb-117">CommonParameters</span></span>
<span data-ttu-id="746cb-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="746cb-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="746cb-119">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="746cb-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="746cb-120">Entradas</span><span class="sxs-lookup"><span data-stu-id="746cb-120">INPUTS</span></span>

### <span data-ttu-id="746cb-121">System.String</span><span class="sxs-lookup"><span data-stu-id="746cb-121">System.String</span></span>

## <span data-ttu-id="746cb-122">Saídas</span><span class="sxs-lookup"><span data-stu-id="746cb-122">OUTPUTS</span></span>

### <span data-ttu-id="746cb-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkUsage</span><span class="sxs-lookup"><span data-stu-id="746cb-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkUsage</span></span>

## <span data-ttu-id="746cb-124">Notas</span><span class="sxs-lookup"><span data-stu-id="746cb-124">NOTES</span></span>

## <span data-ttu-id="746cb-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="746cb-125">RELATED LINKS</span></span>
