---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: A14F9105-1422-4073-96CF-E75CFC039E05
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7eaf1af2efe3f93f4e0a44d54e1f07ea52166942
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945829"
---
# <span data-ttu-id="ccfd6-101">Set-AzureNetworkSecurityGroupToSubnet</span><span class="sxs-lookup"><span data-stu-id="ccfd6-101">Set-AzureNetworkSecurityGroupToSubnet</span></span>

## <span data-ttu-id="ccfd6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ccfd6-102">SYNOPSIS</span></span>
<span data-ttu-id="ccfd6-103">Associa um grupo de segurança de rede a uma sub-rede.</span><span class="sxs-lookup"><span data-stu-id="ccfd6-103">Associates a network security group to a subnet.</span></span>

## <span data-ttu-id="ccfd6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ccfd6-104">SYNTAX</span></span>

```
Set-AzureNetworkSecurityGroupToSubnet -Name <String> -VirtualNetworkName <String> -SubnetName <String> [-Force]
 [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ccfd6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ccfd6-105">DESCRIPTION</span></span>
<span data-ttu-id="ccfd6-106">O cmdlet **set-AzureNetworkSecurityGroupToSubnet** associa um grupo de segurança de rede do Azure a uma sub-rede.</span><span class="sxs-lookup"><span data-stu-id="ccfd6-106">The **Set-AzureNetworkSecurityGroupToSubnet** cmdlet associates an Azure network security group to a subnet.</span></span>

## <span data-ttu-id="ccfd6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ccfd6-107">EXAMPLES</span></span>

## <span data-ttu-id="ccfd6-108">OS</span><span class="sxs-lookup"><span data-stu-id="ccfd6-108">PARAMETERS</span></span>

### <span data-ttu-id="ccfd6-109">-Force</span><span class="sxs-lookup"><span data-stu-id="ccfd6-109">-Force</span></span>
<span data-ttu-id="ccfd6-110">Indica que esse cmdlet não solicita que você confirme a remoção de um grupo de segurança de rede anterior da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="ccfd6-110">Indicates that this cmdlet does not prompt you to confirm the removal of a previous network security group from the subnet.</span></span>

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

### <span data-ttu-id="ccfd6-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="ccfd6-111">-Name</span></span>
<span data-ttu-id="ccfd6-112">Especifica o nome do grupo de segurança de rede que este cmdlet associa a uma sub-rede.</span><span class="sxs-lookup"><span data-stu-id="ccfd6-112">Specifies the name of the network security group that this cmdlet associates to a subnet.</span></span>

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

### <span data-ttu-id="ccfd6-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ccfd6-113">-PassThru</span></span>
<span data-ttu-id="ccfd6-114">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="ccfd6-114">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="ccfd6-115">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="ccfd6-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ccfd6-116">-Perfil</span><span class="sxs-lookup"><span data-stu-id="ccfd6-116">-Profile</span></span>
<span data-ttu-id="ccfd6-117">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="ccfd6-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="ccfd6-118">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="ccfd6-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ccfd6-119">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="ccfd6-119">-SubnetName</span></span>
<span data-ttu-id="ccfd6-120">Especifica o nome de uma sub-rede para a qual esse cmdlet associa um grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="ccfd6-120">Specifies the name of a subnet to which this cmdlet associates a network security group.</span></span>

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

### <span data-ttu-id="ccfd6-121">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="ccfd6-121">-VirtualNetworkName</span></span>
<span data-ttu-id="ccfd6-122">Especifica o nome de uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="ccfd6-122">Specifies the name of a virtual network.</span></span>
<span data-ttu-id="ccfd6-123">Este cmdlet associa um grupo de segurança de rede a uma sub-rede na rede virtual que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="ccfd6-123">This cmdlet associates a network security group to a subnet in the virtual network that this parameter specifies.</span></span>

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

### <span data-ttu-id="ccfd6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccfd6-124">CommonParameters</span></span>
<span data-ttu-id="ccfd6-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ccfd6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccfd6-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ccfd6-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccfd6-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ccfd6-127">INPUTS</span></span>

## <span data-ttu-id="ccfd6-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ccfd6-128">OUTPUTS</span></span>

## <span data-ttu-id="ccfd6-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ccfd6-129">NOTES</span></span>

## <span data-ttu-id="ccfd6-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ccfd6-130">RELATED LINKS</span></span>

[<span data-ttu-id="ccfd6-131">Get-AzureNetworkSecurityGroupForSubnet</span><span class="sxs-lookup"><span data-stu-id="ccfd6-131">Get-AzureNetworkSecurityGroupForSubnet</span></span>](./Get-AzureNetworkSecurityGroupForSubnet.md)

[<span data-ttu-id="ccfd6-132">Remove-AzureNetworkSecurityGroupFromSubnet</span><span class="sxs-lookup"><span data-stu-id="ccfd6-132">Remove-AzureNetworkSecurityGroupFromSubnet</span></span>](./Remove-AzureNetworkSecurityGroupFromSubnet.md)


