---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: F4BADE88-28A2-42FB-9578-93D65148709E
online version: ''
schema: 2.0.0
ms.openlocfilehash: f73e47ec25d44d3965279066de98585ae2cbaee7
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945989"
---
# <span data-ttu-id="4380a-101">New-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="4380a-101">New-AzureRouteTable</span></span>

## <span data-ttu-id="4380a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4380a-102">SYNOPSIS</span></span>
<span data-ttu-id="4380a-103">Cria uma tabela de rota.</span><span class="sxs-lookup"><span data-stu-id="4380a-103">Creates a route table.</span></span>

## <span data-ttu-id="4380a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4380a-104">SYNTAX</span></span>

```
New-AzureRouteTable -Name <String> -Location <String> [-Label <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="4380a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4380a-105">DESCRIPTION</span></span>
<span data-ttu-id="4380a-106">O cmdlet **New-AzureRouteTable** cria uma tabela de rota em um local especificado.</span><span class="sxs-lookup"><span data-stu-id="4380a-106">The **New-AzureRouteTable** cmdlet creates a route table in a specified location.</span></span>
<span data-ttu-id="4380a-107">Você pode adicionar rotas definidas pelo usuário à tabela de rota.</span><span class="sxs-lookup"><span data-stu-id="4380a-107">You can add user-defined routes to the route table.</span></span>
<span data-ttu-id="4380a-108">Você pode associar a tabela de rota a uma sub-rede em uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="4380a-108">You can associate the route table to a subnet in a virtual network.</span></span>

## <span data-ttu-id="4380a-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4380a-109">EXAMPLES</span></span>

## <span data-ttu-id="4380a-110">OS</span><span class="sxs-lookup"><span data-stu-id="4380a-110">PARAMETERS</span></span>

### <span data-ttu-id="4380a-111">-Rótulo</span><span class="sxs-lookup"><span data-stu-id="4380a-111">-Label</span></span>
<span data-ttu-id="4380a-112">Especifica uma descrição para a nova tabela de rotas.</span><span class="sxs-lookup"><span data-stu-id="4380a-112">Specifies a description for the new route table.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4380a-113">-Local</span><span class="sxs-lookup"><span data-stu-id="4380a-113">-Location</span></span>
<span data-ttu-id="4380a-114">Especifica o local em que esse cmdlet cria a tabela de rota.</span><span class="sxs-lookup"><span data-stu-id="4380a-114">Specifies the location in which this cmdlet creates the route table.</span></span>

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

### <span data-ttu-id="4380a-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="4380a-115">-Name</span></span>
<span data-ttu-id="4380a-116">Especifica um nome para a tabela de rota que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="4380a-116">Specifies a name for the route table that this cmdlet creates.</span></span>

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

### <span data-ttu-id="4380a-117">-Perfil</span><span class="sxs-lookup"><span data-stu-id="4380a-117">-Profile</span></span>
<span data-ttu-id="4380a-118">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="4380a-118">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="4380a-119">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="4380a-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4380a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4380a-120">CommonParameters</span></span>
<span data-ttu-id="4380a-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4380a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4380a-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4380a-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4380a-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4380a-123">INPUTS</span></span>

## <span data-ttu-id="4380a-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4380a-124">OUTPUTS</span></span>

## <span data-ttu-id="4380a-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4380a-125">NOTES</span></span>

## <span data-ttu-id="4380a-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4380a-126">RELATED LINKS</span></span>

[<span data-ttu-id="4380a-127">Get-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="4380a-127">Get-AzureRouteTable</span></span>](./Get-AzureRouteTable.md)

[<span data-ttu-id="4380a-128">Remove-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="4380a-128">Remove-AzureRouteTable</span></span>](./Remove-AzureRouteTable.md)


