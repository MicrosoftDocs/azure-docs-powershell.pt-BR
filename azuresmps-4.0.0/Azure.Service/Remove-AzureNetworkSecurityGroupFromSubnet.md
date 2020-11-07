---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: BABA5142-541F-40C8-AFF5-20E4283BE147
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7a718e2f675b4a5e204610a2d4f1fb1aac4c5478
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946150"
---
# <span data-ttu-id="41b96-101">Remove-AzureNetworkSecurityGroupFromSubnet</span><span class="sxs-lookup"><span data-stu-id="41b96-101">Remove-AzureNetworkSecurityGroupFromSubnet</span></span>

## <span data-ttu-id="41b96-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="41b96-102">SYNOPSIS</span></span>
<span data-ttu-id="41b96-103">Dissocia um grupo de segurança de rede de uma sub-rede.</span><span class="sxs-lookup"><span data-stu-id="41b96-103">Dissociates a network security group from a subnet.</span></span>

## <span data-ttu-id="41b96-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="41b96-104">SYNTAX</span></span>

```
Remove-AzureNetworkSecurityGroupFromSubnet -Name <String> -VirtualNetworkName <String> -SubnetName <String>
 [-Force] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="41b96-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="41b96-105">DESCRIPTION</span></span>
<span data-ttu-id="41b96-106">O cmdlet **Remove-AzureNetworkSecurityGroupFromSubnet** dissocia um grupo de segurança de rede do Azure de uma sub-rede.</span><span class="sxs-lookup"><span data-stu-id="41b96-106">The **Remove-AzureNetworkSecurityGroupFromSubnet** cmdlet dissociates an Azure network security group from a subnet.</span></span>

## <span data-ttu-id="41b96-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="41b96-107">EXAMPLES</span></span>

## <span data-ttu-id="41b96-108">OS</span><span class="sxs-lookup"><span data-stu-id="41b96-108">PARAMETERS</span></span>

### <span data-ttu-id="41b96-109">-Force</span><span class="sxs-lookup"><span data-stu-id="41b96-109">-Force</span></span>
<span data-ttu-id="41b96-110">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="41b96-110">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="41b96-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="41b96-111">-Name</span></span>
<span data-ttu-id="41b96-112">Especifica o nome do grupo de segurança de rede que esse cmdlet dissocia de uma sub-rede.</span><span class="sxs-lookup"><span data-stu-id="41b96-112">Specifies the name of the network security group that this cmdlet dissociates from a subnet.</span></span>

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

### <span data-ttu-id="41b96-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="41b96-113">-PassThru</span></span>
<span data-ttu-id="41b96-114">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="41b96-114">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="41b96-115">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="41b96-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="41b96-116">-Perfil</span><span class="sxs-lookup"><span data-stu-id="41b96-116">-Profile</span></span>
<span data-ttu-id="41b96-117">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="41b96-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="41b96-118">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="41b96-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="41b96-119">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="41b96-119">-SubnetName</span></span>
<span data-ttu-id="41b96-120">Especifica o nome de uma sub-rede na qual esse cmdlet dissocia um grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="41b96-120">Specifies the name of a subnet from which this cmdlet dissociates a network security group.</span></span>

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

### <span data-ttu-id="41b96-121">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="41b96-121">-VirtualNetworkName</span></span>
<span data-ttu-id="41b96-122">Especifica o nome de uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="41b96-122">Specifies the name of a virtual network.</span></span>
<span data-ttu-id="41b96-123">Esse cmdlet Desassocia um grupo de segurança de rede de uma sub-rede na rede virtual que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="41b96-123">This cmdlet disassociates a network security group from a subnet in the virtual network that this parameter specifies.</span></span>

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

### <span data-ttu-id="41b96-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41b96-124">CommonParameters</span></span>
<span data-ttu-id="41b96-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41b96-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41b96-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41b96-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41b96-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="41b96-127">INPUTS</span></span>

## <span data-ttu-id="41b96-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="41b96-128">OUTPUTS</span></span>

## <span data-ttu-id="41b96-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="41b96-129">NOTES</span></span>

## <span data-ttu-id="41b96-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="41b96-130">RELATED LINKS</span></span>

[<span data-ttu-id="41b96-131">Get-AzureNetworkSecurityGroupForSubnet</span><span class="sxs-lookup"><span data-stu-id="41b96-131">Get-AzureNetworkSecurityGroupForSubnet</span></span>](./Get-AzureNetworkSecurityGroupForSubnet.md)

[<span data-ttu-id="41b96-132">Set-AzureNetworkSecurityGroupToSubnet</span><span class="sxs-lookup"><span data-stu-id="41b96-132">Set-AzureNetworkSecurityGroupToSubnet</span></span>](./Set-AzureNetworkSecurityGroupToSubnet.md)


