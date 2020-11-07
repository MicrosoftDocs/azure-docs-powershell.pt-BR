---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 7E40C4A2-8B9A-47E8-82AB-19208247349C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 893e03f8e59b3cd01e7d96ca2d04119ee6fb4c66
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945812"
---
# <span data-ttu-id="111af-101">Set-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="111af-101">Set-AzureSubnetRouteTable</span></span>

## <span data-ttu-id="111af-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="111af-102">SYNOPSIS</span></span>
<span data-ttu-id="111af-103">Associa uma tabela de rota a uma sub-rede.</span><span class="sxs-lookup"><span data-stu-id="111af-103">Associates a route table to a subnet.</span></span>

## <span data-ttu-id="111af-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="111af-104">SYNTAX</span></span>

```
Set-AzureSubnetRouteTable -VirtualNetworkName <String> -SubnetName <String> -RouteTableName <String>
 [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="111af-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="111af-105">DESCRIPTION</span></span>
<span data-ttu-id="111af-106">O cmdlet **set-AzureSubnetRouteTable** associa uma tabela de rota a uma sub-rede.</span><span class="sxs-lookup"><span data-stu-id="111af-106">The **Set-AzureSubnetRouteTable** cmdlet associates a route table to a subnet.</span></span>

## <span data-ttu-id="111af-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="111af-107">EXAMPLES</span></span>

### <span data-ttu-id="111af-108">Exemplo 1: associar uma tabela de rota a uma sub-rede</span><span class="sxs-lookup"><span data-stu-id="111af-108">Example 1: Associate a route table to a subnet</span></span>
```
PS C:\> Set-AzureSubnetRouteTable -VirtualNetworkName "VNetUSCentral" -SubnetName "ContosoSubnet" -RouteTableName "PublicRouteTable"
```

<span data-ttu-id="111af-109">Esse comando associa a tabela de rota chamada PublicRouteTable à sub-rede chamada ContosoSubnet.</span><span class="sxs-lookup"><span data-stu-id="111af-109">This command associates the route table named PublicRouteTable to the subnet named ContosoSubnet.</span></span>

## <span data-ttu-id="111af-110">OS</span><span class="sxs-lookup"><span data-stu-id="111af-110">PARAMETERS</span></span>

### <span data-ttu-id="111af-111">-PassThru</span><span class="sxs-lookup"><span data-stu-id="111af-111">-PassThru</span></span>
<span data-ttu-id="111af-112">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="111af-112">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="111af-113">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="111af-113">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="111af-114">-Perfil</span><span class="sxs-lookup"><span data-stu-id="111af-114">-Profile</span></span>
<span data-ttu-id="111af-115">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="111af-115">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="111af-116">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="111af-116">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="111af-117">-RouteTableName</span><span class="sxs-lookup"><span data-stu-id="111af-117">-RouteTableName</span></span>
<span data-ttu-id="111af-118">Especifica o nome da tabela de rota que este cmdlet associa a uma sub-rede.</span><span class="sxs-lookup"><span data-stu-id="111af-118">Specifies the name of the route table that this cmdlet associates with a subnet.</span></span>

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

### <span data-ttu-id="111af-119">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="111af-119">-SubnetName</span></span>
<span data-ttu-id="111af-120">Especifica a sub-rede para a qual esse cmdlet associa a tabela de rota.</span><span class="sxs-lookup"><span data-stu-id="111af-120">Specifies the subnet to which this cmdlet associates the route table.</span></span>

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

### <span data-ttu-id="111af-121">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="111af-121">-VirtualNetworkName</span></span>
<span data-ttu-id="111af-122">Especifica o nome de uma rede virtual que contém a sub-rede para a qual esse cmdlet associa a tabela de rota.</span><span class="sxs-lookup"><span data-stu-id="111af-122">Specifies the name of a virtual network that contains the subnet to which this cmdlet associates the route table.</span></span>

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

### <span data-ttu-id="111af-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="111af-123">CommonParameters</span></span>
<span data-ttu-id="111af-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="111af-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="111af-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="111af-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="111af-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="111af-126">INPUTS</span></span>

## <span data-ttu-id="111af-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="111af-127">OUTPUTS</span></span>

## <span data-ttu-id="111af-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="111af-128">NOTES</span></span>

## <span data-ttu-id="111af-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="111af-129">RELATED LINKS</span></span>

[<span data-ttu-id="111af-130">Get-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="111af-130">Get-AzureSubnetRouteTable</span></span>](./Get-AzureSubnetRouteTable.md)

[<span data-ttu-id="111af-131">Remove-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="111af-131">Remove-AzureSubnetRouteTable</span></span>](./Remove-AzureSubnetRouteTable.md)
