---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B9409AD6-F761-4B80-8E08-DBB2356F567D
online version: https://docs.microsoft.com/powershell/module/az.network/get-azeffectivenetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzEffectiveNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzEffectiveNetworkSecurityGroup.md
ms.openlocfilehash: 38f7d6780b598606d0a0938178309ed67e602315
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887376"
---
# <span data-ttu-id="7ca19-101">Get-AzEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7ca19-101">Get-AzEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="7ca19-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ca19-102">SYNOPSIS</span></span>
<span data-ttu-id="7ca19-103">Obtém o grupo de segurança de rede efetivo de uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="7ca19-103">Gets the effective network security group of a network interface.</span></span>

## <span data-ttu-id="7ca19-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="7ca19-104">SYNTAX</span></span>

```
Get-AzEffectiveNetworkSecurityGroup -NetworkInterfaceName <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7ca19-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="7ca19-105">DESCRIPTION</span></span>
<span data-ttu-id="7ca19-106">O cmdlet **Get-AzEffectiveNetworkSecurityGroup** retorna o grupo de segurança de rede efetivo que é aplicado em uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="7ca19-106">The **Get-AzEffectiveNetworkSecurityGroup** cmdlet returns the effective network security group that is applied on a network interface.</span></span>

## <span data-ttu-id="7ca19-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7ca19-107">EXAMPLES</span></span>

### <span data-ttu-id="7ca19-108">Exemplo 1: Obter o grupo de segurança de rede efetivo em uma interface de rede</span><span class="sxs-lookup"><span data-stu-id="7ca19-108">Example 1: Get the effective network security group on a network interface</span></span>
```
PS C:\>Get-AzEffectiveNetworkSecurityGroup -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="7ca19-109">Este comando obtém todas as regras de segurança de rede efetivas associadas à interface de rede chamada MyNetworkInterface no grupo de recursos chamado myResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="7ca19-109">This command gets all of the effective network security rules associated with the network interface named MyNetworkInterface in the resource group named myResourceGroup.</span></span>

## <span data-ttu-id="7ca19-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="7ca19-110">PARAMETERS</span></span>

### <span data-ttu-id="7ca19-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ca19-111">-DefaultProfile</span></span>
<span data-ttu-id="7ca19-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="7ca19-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7ca19-113">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="7ca19-113">-NetworkInterfaceName</span></span>
<span data-ttu-id="7ca19-114">Especificou o nome de uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="7ca19-114">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="7ca19-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ca19-115">-ResourceGroupName</span></span>
<span data-ttu-id="7ca19-116">Especifica o grupo de recursos de uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="7ca19-116">Specifies the resource group of a network interface.</span></span>

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

### <span data-ttu-id="7ca19-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ca19-117">CommonParameters</span></span>
<span data-ttu-id="7ca19-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ca19-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ca19-119">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7ca19-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ca19-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7ca19-120">INPUTS</span></span>

### <span data-ttu-id="7ca19-121">System.String</span><span class="sxs-lookup"><span data-stu-id="7ca19-121">System.String</span></span>

## <span data-ttu-id="7ca19-122">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="7ca19-122">OUTPUTS</span></span>

### <span data-ttu-id="7ca19-123">Microsoft.Azure.Commands.Network.Models.PSEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7ca19-123">Microsoft.Azure.Commands.Network.Models.PSEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="7ca19-124">NOTES</span><span class="sxs-lookup"><span data-stu-id="7ca19-124">NOTES</span></span>

## <span data-ttu-id="7ca19-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7ca19-125">RELATED LINKS</span></span>

[<span data-ttu-id="7ca19-126">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="7ca19-126">Get-AzEffectiveRouteTable</span></span>](./Get-AzEffectiveRouteTable.md)


