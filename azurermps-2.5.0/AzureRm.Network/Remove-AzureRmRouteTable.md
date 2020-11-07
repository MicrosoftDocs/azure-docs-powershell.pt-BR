---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: FDA33633-EB2E-4095-8498-DF8910F1D434
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermroutetable
schema: 2.0.0
ms.openlocfilehash: f78b888e75db758f254924dee9fbf501050717b6
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786412"
---
# <span data-ttu-id="7408d-101">Remove-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="7408d-101">Remove-AzureRmRouteTable</span></span>

## <span data-ttu-id="7408d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7408d-102">SYNOPSIS</span></span>
<span data-ttu-id="7408d-103">Remove uma tabela de rota.</span><span class="sxs-lookup"><span data-stu-id="7408d-103">Removes a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7408d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7408d-104">SYNTAX</span></span>

```
Remove-AzureRmRouteTable -ResourceGroupName <String> -Name <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7408d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7408d-105">DESCRIPTION</span></span>
<span data-ttu-id="7408d-106">O cmdlet **Remove-AzureRmRouteTable** remove uma tabela de rota do Azure.</span><span class="sxs-lookup"><span data-stu-id="7408d-106">The **Remove-AzureRmRouteTable** cmdlet removes an Azure route table.</span></span>

## <span data-ttu-id="7408d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7408d-107">EXAMPLES</span></span>

### <span data-ttu-id="7408d-108">Exemplo 1: remover uma tabela de rota</span><span class="sxs-lookup"><span data-stu-id="7408d-108">Example 1: Remove a route table</span></span>
```
PS C:\>Remove-AzureRmRouteTable -ResourceGroupName "ResourceGroup11 -Name "RouteTable01"
Confirm
Are you sure you want to remove resource 'RouteTable01'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="7408d-109">Esse comando Remove a tabela de rota chamada RouteTable01 no grupo de recursos chamado ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="7408d-109">This command removes the route table named RouteTable01 in the resource group named ResourceGroup11.</span></span>
<span data-ttu-id="7408d-110">O cmdlet solicita confirmação antes de remover a tabela.</span><span class="sxs-lookup"><span data-stu-id="7408d-110">The cmdlet prompts you for confirmation before it removes the table.</span></span>

## <span data-ttu-id="7408d-111">OS</span><span class="sxs-lookup"><span data-stu-id="7408d-111">PARAMETERS</span></span>

### <span data-ttu-id="7408d-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7408d-112">-AsJob</span></span>
<span data-ttu-id="7408d-113">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="7408d-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7408d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7408d-114">-DefaultProfile</span></span>
<span data-ttu-id="7408d-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7408d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7408d-116">-Force</span><span class="sxs-lookup"><span data-stu-id="7408d-116">-Force</span></span>
<span data-ttu-id="7408d-117">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="7408d-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7408d-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="7408d-118">-Name</span></span>
<span data-ttu-id="7408d-119">Especifica o nome da tabela de rota que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="7408d-119">Specifies the name of the route table that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7408d-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7408d-120">-PassThru</span></span>
<span data-ttu-id="7408d-121">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="7408d-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="7408d-122">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="7408d-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7408d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7408d-123">-ResourceGroupName</span></span>
<span data-ttu-id="7408d-124">Especifica o nome do grupo de recursos que contém a tabela de rota que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="7408d-124">Specifies the name of the resource group that contains the route table that this cmdlet removes.</span></span>

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

### <span data-ttu-id="7408d-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7408d-125">-Confirm</span></span>
<span data-ttu-id="7408d-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7408d-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7408d-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7408d-127">-WhatIf</span></span>
<span data-ttu-id="7408d-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7408d-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7408d-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7408d-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7408d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7408d-130">CommonParameters</span></span>
<span data-ttu-id="7408d-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7408d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7408d-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7408d-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7408d-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7408d-133">INPUTS</span></span>

## <span data-ttu-id="7408d-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7408d-134">OUTPUTS</span></span>

## <span data-ttu-id="7408d-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7408d-135">NOTES</span></span>

## <span data-ttu-id="7408d-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7408d-136">RELATED LINKS</span></span>

[<span data-ttu-id="7408d-137">Get-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="7408d-137">Get-AzureRmRouteTable</span></span>](./Get-AzureRmRouteTable.md)

[<span data-ttu-id="7408d-138">New-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="7408d-138">New-AzureRmRouteTable</span></span>](./New-AzureRmRouteTable.md)

[<span data-ttu-id="7408d-139">Set-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="7408d-139">Set-AzureRmRouteTable</span></span>](./Set-AzureRmRouteTable.md)


