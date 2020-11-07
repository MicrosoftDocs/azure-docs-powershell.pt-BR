---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: AA2F2793-03A5-41D9-8021-D18BE98DB044
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9bf26bd23ecc3dcb9e6973baf4c5eecf3d544402
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946456"
---
# <span data-ttu-id="c19e9-101">Remove-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="c19e9-101">Remove-AzureSubnetRouteTable</span></span>

## <span data-ttu-id="c19e9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c19e9-102">SYNOPSIS</span></span>
<span data-ttu-id="c19e9-103">Remove uma associação de tabela de rota de uma sub-rede.</span><span class="sxs-lookup"><span data-stu-id="c19e9-103">Removes a route table association from a subnet.</span></span>

## <span data-ttu-id="c19e9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c19e9-104">SYNTAX</span></span>

```
Remove-AzureSubnetRouteTable -VirtualNetworkName <String> -SubnetName <String> [-Force] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c19e9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c19e9-105">DESCRIPTION</span></span>
<span data-ttu-id="c19e9-106">O cmdlet **Remove-AzureSubnetRouteTable** remove uma associação de tabela de rota de uma sub-rede.</span><span class="sxs-lookup"><span data-stu-id="c19e9-106">The **Remove-AzureSubnetRouteTable** cmdlet removes a route table association from a subnet.</span></span>

## <span data-ttu-id="c19e9-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c19e9-107">EXAMPLES</span></span>

### <span data-ttu-id="c19e9-108">Exemplo 1: remover uma associação entre uma tabela de rota e uma sub-rede</span><span class="sxs-lookup"><span data-stu-id="c19e9-108">Example 1: Remove an association between a route table and a subnet</span></span>
```
PS C:\> Remove-AzureSubnetRouteTable -VirtualNetworkName "VNetUSCentral" -SubnetName "ContosoSubnet"
```

<span data-ttu-id="c19e9-109">Esse comando Remove a associação da tabela de rota chamada PublicRouteTable para a sub-rede chamada ContosoSubnet.</span><span class="sxs-lookup"><span data-stu-id="c19e9-109">This command removes the association of the route table named PublicRouteTable to the subnet named ContosoSubnet.</span></span>

## <span data-ttu-id="c19e9-110">OS</span><span class="sxs-lookup"><span data-stu-id="c19e9-110">PARAMETERS</span></span>

### <span data-ttu-id="c19e9-111">-Force</span><span class="sxs-lookup"><span data-stu-id="c19e9-111">-Force</span></span>
<span data-ttu-id="c19e9-112">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="c19e9-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c19e9-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c19e9-113">-PassThru</span></span>
<span data-ttu-id="c19e9-114">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="c19e9-114">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="c19e9-115">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="c19e9-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c19e9-116">-Perfil</span><span class="sxs-lookup"><span data-stu-id="c19e9-116">-Profile</span></span>
<span data-ttu-id="c19e9-117">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="c19e9-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="c19e9-118">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="c19e9-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c19e9-119">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="c19e9-119">-SubnetName</span></span>
<span data-ttu-id="c19e9-120">Especifica a sub-rede para a qual esse cmdlet Remove a tabela de rota.</span><span class="sxs-lookup"><span data-stu-id="c19e9-120">Specifies the subnet for which this cmdlet removes the route table.</span></span>

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

### <span data-ttu-id="c19e9-121">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="c19e9-121">-VirtualNetworkName</span></span>
<span data-ttu-id="c19e9-122">Especifica o nome de uma rede virtual que contém a sub-rede para a qual esse cmdlet Remove a tabela de rota.</span><span class="sxs-lookup"><span data-stu-id="c19e9-122">Specifies the name of a virtual network that contains the subnet for which this cmdlet removes the route table.</span></span>

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

### <span data-ttu-id="c19e9-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c19e9-123">CommonParameters</span></span>
<span data-ttu-id="c19e9-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c19e9-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c19e9-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c19e9-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c19e9-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c19e9-126">INPUTS</span></span>

## <span data-ttu-id="c19e9-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c19e9-127">OUTPUTS</span></span>

## <span data-ttu-id="c19e9-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c19e9-128">NOTES</span></span>

## <span data-ttu-id="c19e9-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c19e9-129">RELATED LINKS</span></span>

[<span data-ttu-id="c19e9-130">Get-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="c19e9-130">Get-AzureSubnetRouteTable</span></span>](./Get-AzureSubnetRouteTable.md)

[<span data-ttu-id="c19e9-131">Set-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="c19e9-131">Set-AzureSubnetRouteTable</span></span>](./Set-AzureSubnetRouteTable.md)


