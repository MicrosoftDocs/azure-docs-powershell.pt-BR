---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 7F8C2223-5F82-4E4E-8057-44B72F7D5803
online version: ''
schema: 2.0.0
ms.openlocfilehash: a02d80d46696ff635da95c6bc29875f697f65fd4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946313"
---
# <span data-ttu-id="bfb31-101">Get-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="bfb31-101">Get-AzureRouteTable</span></span>

## <span data-ttu-id="bfb31-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bfb31-102">SYNOPSIS</span></span>
<span data-ttu-id="bfb31-103">Obtém uma tabela de rota.</span><span class="sxs-lookup"><span data-stu-id="bfb31-103">Gets a route table.</span></span>

## <span data-ttu-id="bfb31-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bfb31-104">SYNTAX</span></span>

```
Get-AzureRouteTable [-Name <String>] [-Detailed] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="bfb31-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bfb31-105">DESCRIPTION</span></span>
<span data-ttu-id="bfb31-106">O cmdlet **Get-AzureRouteTable** Obtém uma tabela de rota.</span><span class="sxs-lookup"><span data-stu-id="bfb31-106">The **Get-AzureRouteTable** cmdlet gets a route table.</span></span>
<span data-ttu-id="bfb31-107">Especifique o parâmetro *detalhado* para listar as rotas na tabela de rota.</span><span class="sxs-lookup"><span data-stu-id="bfb31-107">Specify the *Detailed* parameter to list the routes in the route table.</span></span>

## <span data-ttu-id="bfb31-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bfb31-108">EXAMPLES</span></span>

### <span data-ttu-id="bfb31-109">Exemplo 1: obter detalhes de uma tabela de rota</span><span class="sxs-lookup"><span data-stu-id="bfb31-109">Example 1: Get details of a route table</span></span>
```
PS C:\> Get-AzureRouteTable -Name "ApplianceRouteTable" -Detailed
Routes                        Name                          Location                      Label
------                        ----                          --------                      -----
{approute}                    ApplianceRouteTable           Central US                    Appliance Route Table
```

<span data-ttu-id="bfb31-110">Esse comando obtém os detalhes de uma tabela de rota chamada ApplianceRouteTable.</span><span class="sxs-lookup"><span data-stu-id="bfb31-110">This command gets the details of a route table named ApplianceRouteTable.</span></span>

## <span data-ttu-id="bfb31-111">OS</span><span class="sxs-lookup"><span data-stu-id="bfb31-111">PARAMETERS</span></span>

### <span data-ttu-id="bfb31-112">-Detalhado</span><span class="sxs-lookup"><span data-stu-id="bfb31-112">-Detailed</span></span>
<span data-ttu-id="bfb31-113">Indica que esse cmdlet exibe as rotas na tabela de rota.</span><span class="sxs-lookup"><span data-stu-id="bfb31-113">Indicates that this cmdlet displays the routes in the route table.</span></span>

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

### <span data-ttu-id="bfb31-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="bfb31-114">-Name</span></span>
<span data-ttu-id="bfb31-115">Especifica o nome da tabela de rota obtida por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bfb31-115">Specifies the name of the route table that this cmdlet gets.</span></span>

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

### <span data-ttu-id="bfb31-116">-Perfil</span><span class="sxs-lookup"><span data-stu-id="bfb31-116">-Profile</span></span>
<span data-ttu-id="bfb31-117">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="bfb31-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="bfb31-118">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="bfb31-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="bfb31-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfb31-119">CommonParameters</span></span>
<span data-ttu-id="bfb31-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bfb31-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfb31-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bfb31-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfb31-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bfb31-122">INPUTS</span></span>

## <span data-ttu-id="bfb31-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bfb31-123">OUTPUTS</span></span>

## <span data-ttu-id="bfb31-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bfb31-124">NOTES</span></span>

## <span data-ttu-id="bfb31-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bfb31-125">RELATED LINKS</span></span>

[<span data-ttu-id="bfb31-126">New-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="bfb31-126">New-AzureRouteTable</span></span>](./New-AzureRouteTable.md)

[<span data-ttu-id="bfb31-127">Remove-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="bfb31-127">Remove-AzureRouteTable</span></span>](./Remove-AzureRouteTable.md)


