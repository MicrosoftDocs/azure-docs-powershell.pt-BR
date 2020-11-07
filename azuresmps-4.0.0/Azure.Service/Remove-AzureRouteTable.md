---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 58329D8A-CB54-46FB-84A7-C31F00C13827
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6333430682de7693b6b87f9d037dea66725bfed8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946132"
---
# <span data-ttu-id="43fb8-101">Remove-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="43fb8-101">Remove-AzureRouteTable</span></span>

## <span data-ttu-id="43fb8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="43fb8-102">SYNOPSIS</span></span>
<span data-ttu-id="43fb8-103">Remove uma tabela de rota.</span><span class="sxs-lookup"><span data-stu-id="43fb8-103">Removes a route table.</span></span>

## <span data-ttu-id="43fb8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="43fb8-104">SYNTAX</span></span>

```
Remove-AzureRouteTable -Name <String> [-PassThru] [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="43fb8-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="43fb8-105">DESCRIPTION</span></span>
<span data-ttu-id="43fb8-106">O cmdlet **Remove-AzureRouteTable** remove uma tabela de rota da sua assinatura.</span><span class="sxs-lookup"><span data-stu-id="43fb8-106">The **Remove-AzureRouteTable** cmdlet removes a route table from your subscription.</span></span>
<span data-ttu-id="43fb8-107">Se uma tabela de rota estiver associada a uma sub-rede, você não poderá remover a tabela.</span><span class="sxs-lookup"><span data-stu-id="43fb8-107">If a route table is associated to a subnet, you cannot remove the table.</span></span>

## <span data-ttu-id="43fb8-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="43fb8-108">EXAMPLES</span></span>

### <span data-ttu-id="43fb8-109">Exemplo 1: remover uma tabela de rota</span><span class="sxs-lookup"><span data-stu-id="43fb8-109">Example 1: Remove a route table</span></span>
```
PS C:\> Remove-AzureRouteTable -Name "PublicRouteTable"
```

<span data-ttu-id="43fb8-110">Esse comando Remove a tabela de rota chamada PublicRouteTable.</span><span class="sxs-lookup"><span data-stu-id="43fb8-110">This command removes the route table named PublicRouteTable.</span></span>

## <span data-ttu-id="43fb8-111">OS</span><span class="sxs-lookup"><span data-stu-id="43fb8-111">PARAMETERS</span></span>

### <span data-ttu-id="43fb8-112">-Force</span><span class="sxs-lookup"><span data-stu-id="43fb8-112">-Force</span></span>
<span data-ttu-id="43fb8-113">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="43fb8-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="43fb8-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="43fb8-114">-Name</span></span>
<span data-ttu-id="43fb8-115">Especifica o nome da tabela de rota que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="43fb8-115">Specifies the name of the route table that this cmdlet removes.</span></span>

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

### <span data-ttu-id="43fb8-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="43fb8-116">-PassThru</span></span>
<span data-ttu-id="43fb8-117">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="43fb8-117">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="43fb8-118">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="43fb8-118">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="43fb8-119">-Perfil</span><span class="sxs-lookup"><span data-stu-id="43fb8-119">-Profile</span></span>
<span data-ttu-id="43fb8-120">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="43fb8-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="43fb8-121">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="43fb8-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="43fb8-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43fb8-122">CommonParameters</span></span>
<span data-ttu-id="43fb8-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43fb8-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43fb8-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43fb8-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43fb8-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="43fb8-125">INPUTS</span></span>

## <span data-ttu-id="43fb8-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="43fb8-126">OUTPUTS</span></span>

## <span data-ttu-id="43fb8-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="43fb8-127">NOTES</span></span>

## <span data-ttu-id="43fb8-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="43fb8-128">RELATED LINKS</span></span>

[<span data-ttu-id="43fb8-129">Get-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="43fb8-129">Get-AzureRouteTable</span></span>](./Get-AzureRouteTable.md)

[<span data-ttu-id="43fb8-130">New-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="43fb8-130">New-AzureRouteTable</span></span>](./New-AzureRouteTable.md)
