---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 4D75240C-F2B5-4273-848C-107308DD6837
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3d56de5b27565f7bfdd90198ad45e2766da521f4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945638"
---
# <span data-ttu-id="c7b8d-101">Get-AzureNetworkSecurityGroupForSubnet</span><span class="sxs-lookup"><span data-stu-id="c7b8d-101">Get-AzureNetworkSecurityGroupForSubnet</span></span>

## <span data-ttu-id="c7b8d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c7b8d-102">SYNOPSIS</span></span>
<span data-ttu-id="c7b8d-103">Obtém o grupo de segurança de rede para uma sub-rede.</span><span class="sxs-lookup"><span data-stu-id="c7b8d-103">Gets the network security group for a subnet.</span></span>

## <span data-ttu-id="c7b8d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c7b8d-104">SYNTAX</span></span>

```
Get-AzureNetworkSecurityGroupForSubnet -VirtualNetworkName <String> -SubnetName <String> [-Detailed]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c7b8d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c7b8d-105">DESCRIPTION</span></span>
<span data-ttu-id="c7b8d-106">O cmdlet **Get-AzureNetworkSecurityGroupForSubnet** Obtém o grupo de segurança de rede associado a uma sub-rede.</span><span class="sxs-lookup"><span data-stu-id="c7b8d-106">The **Get-AzureNetworkSecurityGroupForSubnet** cmdlet gets the network security group that is associated to a subnet.</span></span>

## <span data-ttu-id="c7b8d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c7b8d-107">EXAMPLES</span></span>

## <span data-ttu-id="c7b8d-108">OS</span><span class="sxs-lookup"><span data-stu-id="c7b8d-108">PARAMETERS</span></span>

### <span data-ttu-id="c7b8d-109">-Detalhado</span><span class="sxs-lookup"><span data-stu-id="c7b8d-109">-Detailed</span></span>
<span data-ttu-id="c7b8d-110">Indica que esse cmdlet exibe as regras de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="c7b8d-110">Indicates that this cmdlet displays the network security rules.</span></span>

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

### <span data-ttu-id="c7b8d-111">-Perfil</span><span class="sxs-lookup"><span data-stu-id="c7b8d-111">-Profile</span></span>
<span data-ttu-id="c7b8d-112">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="c7b8d-112">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c7b8d-113">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="c7b8d-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7b8d-114">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="c7b8d-114">-SubnetName</span></span>
<span data-ttu-id="c7b8d-115">Especifica o nome de uma sub-rede para a qual esse cmdlet obtém um grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="c7b8d-115">Specifies the name of a subnet for which this cmdlet gets a network security group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7b8d-116">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="c7b8d-116">-VirtualNetworkName</span></span>
<span data-ttu-id="c7b8d-117">Especifica o nome de uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="c7b8d-117">Specifies the name of a virtual network.</span></span>
<span data-ttu-id="c7b8d-118">Esse cmdlet obtém um grupo de segurança de rede para uma sub-rede na rede virtual que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="c7b8d-118">This cmdlet gets a network security group for a subnet in the virtual network that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7b8d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7b8d-119">CommonParameters</span></span>
<span data-ttu-id="c7b8d-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7b8d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7b8d-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7b8d-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7b8d-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c7b8d-122">INPUTS</span></span>

## <span data-ttu-id="c7b8d-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c7b8d-123">OUTPUTS</span></span>

## <span data-ttu-id="c7b8d-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c7b8d-124">NOTES</span></span>

## <span data-ttu-id="c7b8d-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c7b8d-125">RELATED LINKS</span></span>

[<span data-ttu-id="c7b8d-126">Remove-AzureNetworkSecurityGroupFromSubnet</span><span class="sxs-lookup"><span data-stu-id="c7b8d-126">Remove-AzureNetworkSecurityGroupFromSubnet</span></span>](./Remove-AzureNetworkSecurityGroupFromSubnet.md)

[<span data-ttu-id="c7b8d-127">Set-AzureNetworkSecurityGroupToSubnet</span><span class="sxs-lookup"><span data-stu-id="c7b8d-127">Set-AzureNetworkSecurityGroupToSubnet</span></span>](./Set-AzureNetworkSecurityGroupToSubnet.md)
