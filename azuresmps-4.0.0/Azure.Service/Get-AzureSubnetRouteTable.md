---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: AEFC9094-144F-4E29-AC5A-DBFDA175A920
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8e56496c1fdf04b5227121f5ac39193938a2214e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945542"
---
# <span data-ttu-id="d6f52-101">Get-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="d6f52-101">Get-AzureSubnetRouteTable</span></span>

## <span data-ttu-id="d6f52-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d6f52-102">SYNOPSIS</span></span>
<span data-ttu-id="d6f52-103">Obtém uma tabela de rota para uma sub-rede.</span><span class="sxs-lookup"><span data-stu-id="d6f52-103">Gets a route table for a subnet.</span></span>

## <span data-ttu-id="d6f52-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d6f52-104">SYNTAX</span></span>

```
Get-AzureSubnetRouteTable -VirtualNetworkName <String> -SubnetName <String> [-Detailed]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d6f52-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d6f52-105">DESCRIPTION</span></span>
<span data-ttu-id="d6f52-106">O cmdlet **Get-AzureSubnetRouteTable** Obtém a tabela de rotas associada a uma sub-rede.</span><span class="sxs-lookup"><span data-stu-id="d6f52-106">The **Get-AzureSubnetRouteTable** cmdlet gets the route table that is associated with a subnet.</span></span>

## <span data-ttu-id="d6f52-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d6f52-107">EXAMPLES</span></span>

### <span data-ttu-id="d6f52-108">Exemplo 1: Exibir rotas para uma sub-rede</span><span class="sxs-lookup"><span data-stu-id="d6f52-108">Example 1: Display routes for a subnet</span></span>
```
PS C:\> Get-AzureSubnetRouteTable -VirtualNetworkName "VNetUSCentral" -SubnetName "ContosoSubnet" -Detailed
Routes                        Name                          Location                      Label
------                        ----                          --------                      -----
{internetroute}               PublicRT                      Central US                    Sample RT in Central US
```

<span data-ttu-id="d6f52-109">Esse comando exibe as rotas no nome da tabela de rota que está associado à sub-rede chamada ContosoSubnet.</span><span class="sxs-lookup"><span data-stu-id="d6f52-109">This command displays the routes in the route table name that is associated with subnet named ContosoSubnet.</span></span>

## <span data-ttu-id="d6f52-110">OS</span><span class="sxs-lookup"><span data-stu-id="d6f52-110">PARAMETERS</span></span>

### <span data-ttu-id="d6f52-111">-Detalhado</span><span class="sxs-lookup"><span data-stu-id="d6f52-111">-Detailed</span></span>
<span data-ttu-id="d6f52-112">Indica que esse cmdlet exibe as rotas na tabela de rota que está associada à sub-rede.</span><span class="sxs-lookup"><span data-stu-id="d6f52-112">Indicates that this cmdlet displays the routes in the route table that is associated with the subnet.</span></span>

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

### <span data-ttu-id="d6f52-113">-Perfil</span><span class="sxs-lookup"><span data-stu-id="d6f52-113">-Profile</span></span>
<span data-ttu-id="d6f52-114">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="d6f52-114">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="d6f52-115">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="d6f52-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d6f52-116">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="d6f52-116">-SubnetName</span></span>
<span data-ttu-id="d6f52-117">Especifica a sub-rede para a qual esse cmdlet obtém a tabela de rota.</span><span class="sxs-lookup"><span data-stu-id="d6f52-117">Specifies the subnet for which this cmdlet gets the route table.</span></span>

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

### <span data-ttu-id="d6f52-118">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="d6f52-118">-VirtualNetworkName</span></span>
<span data-ttu-id="d6f52-119">Especifica o nome de uma rede virtual que contém a sub-rede para a qual esse cmdlet obtém a tabela de rota.</span><span class="sxs-lookup"><span data-stu-id="d6f52-119">Specifies the name of a virtual network that contains the subnet for which this cmdlet gets the route table.</span></span>

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

### <span data-ttu-id="d6f52-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6f52-120">CommonParameters</span></span>
<span data-ttu-id="d6f52-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6f52-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6f52-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6f52-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6f52-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d6f52-123">INPUTS</span></span>

## <span data-ttu-id="d6f52-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d6f52-124">OUTPUTS</span></span>

## <span data-ttu-id="d6f52-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d6f52-125">NOTES</span></span>

## <span data-ttu-id="d6f52-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d6f52-126">RELATED LINKS</span></span>

[<span data-ttu-id="d6f52-127">Remove-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="d6f52-127">Remove-AzureSubnetRouteTable</span></span>](./Remove-AzureSubnetRouteTable.md)

[<span data-ttu-id="d6f52-128">Set-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="d6f52-128">Set-AzureSubnetRouteTable</span></span>](./Set-AzureSubnetRouteTable.md)


