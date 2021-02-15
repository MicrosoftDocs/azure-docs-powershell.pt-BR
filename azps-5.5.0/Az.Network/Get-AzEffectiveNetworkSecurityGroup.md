---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B9409AD6-F761-4B80-8E08-DBB2356F567D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azeffectivenetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzEffectiveNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzEffectiveNetworkSecurityGroup.md
ms.openlocfilehash: c0f7d2692472316d018d4a11b6843264c8666fe2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114709"
---
# <span data-ttu-id="555e9-101">Get-AzEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="555e9-101">Get-AzEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="555e9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="555e9-102">SYNOPSIS</span></span>
<span data-ttu-id="555e9-103">Obtém o grupo de segurança de rede eficaz de uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="555e9-103">Gets the effective network security group of a network interface.</span></span>

## <span data-ttu-id="555e9-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="555e9-104">SYNTAX</span></span>

```
Get-AzEffectiveNetworkSecurityGroup -NetworkInterfaceName <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="555e9-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="555e9-105">DESCRIPTION</span></span>
<span data-ttu-id="555e9-106">O cmdlet **Get-AzEffectiveNetworkSecurityGroup** retorna o grupo de segurança de rede eficaz que é aplicado em uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="555e9-106">The **Get-AzEffectiveNetworkSecurityGroup** cmdlet returns the effective network security group that is applied on a network interface.</span></span>

## <span data-ttu-id="555e9-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="555e9-107">EXAMPLES</span></span>

### <span data-ttu-id="555e9-108">Exemplo 1: Obter o grupo de segurança de rede eficaz em uma interface de rede</span><span class="sxs-lookup"><span data-stu-id="555e9-108">Example 1: Get the effective network security group on a network interface</span></span>
```
PS C:\>Get-AzEffectiveNetworkSecurityGroup -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="555e9-109">Esse comando obtém todas as regras de segurança de rede eficazes associadas à interface de rede chamada MyNetworkInterface no grupo de recursos chamado myResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="555e9-109">This command gets all of the effective network security rules associated with the network interface named MyNetworkInterface in the resource group named myResourceGroup.</span></span>

## <span data-ttu-id="555e9-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="555e9-110">PARAMETERS</span></span>

### <span data-ttu-id="555e9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="555e9-111">-DefaultProfile</span></span>
<span data-ttu-id="555e9-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="555e9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="555e9-113">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="555e9-113">-NetworkInterfaceName</span></span>
<span data-ttu-id="555e9-114">Especificou o nome de uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="555e9-114">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="555e9-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="555e9-115">-ResourceGroupName</span></span>
<span data-ttu-id="555e9-116">Especifica o grupo de recursos de uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="555e9-116">Specifies the resource group of a network interface.</span></span>

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

### <span data-ttu-id="555e9-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="555e9-117">CommonParameters</span></span>
<span data-ttu-id="555e9-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="555e9-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="555e9-119">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="555e9-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="555e9-120">Entradas</span><span class="sxs-lookup"><span data-stu-id="555e9-120">INPUTS</span></span>

### <span data-ttu-id="555e9-121">System.String</span><span class="sxs-lookup"><span data-stu-id="555e9-121">System.String</span></span>

## <span data-ttu-id="555e9-122">Saídas</span><span class="sxs-lookup"><span data-stu-id="555e9-122">OUTPUTS</span></span>

### <span data-ttu-id="555e9-123">Microsoft.Azure.Commands.Network.Models.PSEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="555e9-123">Microsoft.Azure.Commands.Network.Models.PSEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="555e9-124">Notas</span><span class="sxs-lookup"><span data-stu-id="555e9-124">NOTES</span></span>

## <span data-ttu-id="555e9-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="555e9-125">RELATED LINKS</span></span>

[<span data-ttu-id="555e9-126">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="555e9-126">Get-AzEffectiveRouteTable</span></span>](./Get-AzEffectiveRouteTable.md)


