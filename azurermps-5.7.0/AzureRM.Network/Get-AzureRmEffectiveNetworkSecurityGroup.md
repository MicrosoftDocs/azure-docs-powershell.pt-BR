---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B9409AD6-F761-4B80-8E08-DBB2356F567D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermeffectivenetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmEffectiveNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmEffectiveNetworkSecurityGroup.md
ms.openlocfilehash: a7c131db8ce5a3489bc2a869e31b0ef7ab89f3c2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93603014"
---
# <span data-ttu-id="9fa66-101">Get-AzureRmEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="9fa66-101">Get-AzureRmEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="9fa66-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9fa66-102">SYNOPSIS</span></span>
<span data-ttu-id="9fa66-103">Obtém o grupo de segurança de rede efetivo de uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="9fa66-103">Gets the effective network security group of a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9fa66-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9fa66-104">SYNTAX</span></span>

```
Get-AzureRmEffectiveNetworkSecurityGroup -NetworkInterfaceName <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9fa66-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9fa66-105">DESCRIPTION</span></span>
<span data-ttu-id="9fa66-106">O cmdlet **Get-AzureRmEffectiveNetworkSecurityGroup** retorna o grupo de segurança de rede efetivo aplicado em uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="9fa66-106">The **Get-AzureRmEffectiveNetworkSecurityGroup** cmdlet returns the effective network security group that is applied on a network interface.</span></span>

## <span data-ttu-id="9fa66-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9fa66-107">EXAMPLES</span></span>

### <span data-ttu-id="9fa66-108">Exemplo 1: obter o grupo de segurança de rede efetivo em uma interface de rede</span><span class="sxs-lookup"><span data-stu-id="9fa66-108">Example 1: Get the effective network security group on a network interface</span></span>
```
PS C:\>Get-AzureRmEffectiveNetworkSecurityGroup -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="9fa66-109">Esse comando obtém todas as regras de segurança de rede efetivas associadas à interface de rede chamada mynetworkinterface no grupo de recursos chamado MyResource Group.</span><span class="sxs-lookup"><span data-stu-id="9fa66-109">This command gets all of the effective network security rules associated with the network interface named MyNetworkInterface in the resource group named myResourceGroup.</span></span>

## <span data-ttu-id="9fa66-110">OS</span><span class="sxs-lookup"><span data-stu-id="9fa66-110">PARAMETERS</span></span>

### <span data-ttu-id="9fa66-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fa66-111">-DefaultProfile</span></span>
<span data-ttu-id="9fa66-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9fa66-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9fa66-113">-NetworkInterfacename</span><span class="sxs-lookup"><span data-stu-id="9fa66-113">-NetworkInterfaceName</span></span>
<span data-ttu-id="9fa66-114">Especificou o nome de uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="9fa66-114">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="9fa66-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9fa66-115">-ResourceGroupName</span></span>
<span data-ttu-id="9fa66-116">Especifica o grupo de recursos de uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="9fa66-116">Specifies the resource group of a network interface.</span></span>

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

### <span data-ttu-id="9fa66-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fa66-117">CommonParameters</span></span>
<span data-ttu-id="9fa66-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9fa66-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fa66-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9fa66-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fa66-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9fa66-120">INPUTS</span></span>

### <span data-ttu-id="9fa66-121">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="9fa66-121">None</span></span>
<span data-ttu-id="9fa66-122">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="9fa66-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9fa66-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9fa66-123">OUTPUTS</span></span>

### <span data-ttu-id="9fa66-124">Microsoft. Azure. Commands. Network. Models. PSEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="9fa66-124">Microsoft.Azure.Commands.Network.Models.PSEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="9fa66-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9fa66-125">NOTES</span></span>

## <span data-ttu-id="9fa66-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9fa66-126">RELATED LINKS</span></span>

[<span data-ttu-id="9fa66-127">Get-AzureRmEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="9fa66-127">Get-AzureRmEffectiveRouteTable</span></span>](./Get-AzureRmEffectiveRouteTable.md)


