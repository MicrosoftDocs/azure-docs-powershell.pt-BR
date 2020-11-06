---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: FDA33633-EB2E-4095-8498-DF8910F1D434
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteTable.md
ms.openlocfilehash: 161b97ffd032c8a6f7aca6b40c719a45b7e6a935
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93600124"
---
# <span data-ttu-id="69305-101">Remove-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="69305-101">Remove-AzRouteTable</span></span>

## <span data-ttu-id="69305-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="69305-102">SYNOPSIS</span></span>
<span data-ttu-id="69305-103">Remove uma tabela de rota.</span><span class="sxs-lookup"><span data-stu-id="69305-103">Removes a route table.</span></span>

## <span data-ttu-id="69305-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="69305-104">SYNTAX</span></span>

```
Remove-AzRouteTable -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69305-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="69305-105">DESCRIPTION</span></span>
<span data-ttu-id="69305-106">O cmdlet **Remove-AzRouteTable** remove uma tabela de rota do Azure.</span><span class="sxs-lookup"><span data-stu-id="69305-106">The **Remove-AzRouteTable** cmdlet removes an Azure route table.</span></span>

## <span data-ttu-id="69305-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="69305-107">EXAMPLES</span></span>

### <span data-ttu-id="69305-108">Exemplo 1: remover uma tabela de rota</span><span class="sxs-lookup"><span data-stu-id="69305-108">Example 1: Remove a route table</span></span>
```
PS C:\>Remove-AzRouteTable -ResourceGroupName "ResourceGroup11 -Name "RouteTable01"
Confirm
Are you sure you want to remove resource 'RouteTable01'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="69305-109">Esse comando Remove a tabela de rota chamada RouteTable01 no grupo de recursos chamado ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="69305-109">This command removes the route table named RouteTable01 in the resource group named ResourceGroup11.</span></span>
<span data-ttu-id="69305-110">O cmdlet solicita confirmação antes de remover a tabela.</span><span class="sxs-lookup"><span data-stu-id="69305-110">The cmdlet prompts you for confirmation before it removes the table.</span></span>

## <span data-ttu-id="69305-111">OS</span><span class="sxs-lookup"><span data-stu-id="69305-111">PARAMETERS</span></span>

### <span data-ttu-id="69305-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="69305-112">-AsJob</span></span>
<span data-ttu-id="69305-113">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="69305-113">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69305-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69305-114">-DefaultProfile</span></span>
<span data-ttu-id="69305-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="69305-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69305-116">-Force</span><span class="sxs-lookup"><span data-stu-id="69305-116">-Force</span></span>
<span data-ttu-id="69305-117">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="69305-117">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69305-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="69305-118">-Name</span></span>
<span data-ttu-id="69305-119">Especifica o nome da tabela de rota que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="69305-119">Specifies the name of the route table that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69305-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="69305-120">-PassThru</span></span>
<span data-ttu-id="69305-121">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="69305-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="69305-122">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="69305-122">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69305-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69305-123">-ResourceGroupName</span></span>
<span data-ttu-id="69305-124">Especifica o nome do grupo de recursos que contém a tabela de rota que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="69305-124">Specifies the name of the resource group that contains the route table that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69305-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="69305-125">-Confirm</span></span>
<span data-ttu-id="69305-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69305-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69305-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69305-127">-WhatIf</span></span>
<span data-ttu-id="69305-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="69305-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69305-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="69305-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69305-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69305-130">CommonParameters</span></span>
<span data-ttu-id="69305-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69305-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69305-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69305-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69305-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="69305-133">INPUTS</span></span>

### <span data-ttu-id="69305-134">System. String</span><span class="sxs-lookup"><span data-stu-id="69305-134">System.String</span></span>

## <span data-ttu-id="69305-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="69305-135">OUTPUTS</span></span>

### <span data-ttu-id="69305-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="69305-136">System.Boolean</span></span>

## <span data-ttu-id="69305-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="69305-137">NOTES</span></span>

## <span data-ttu-id="69305-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="69305-138">RELATED LINKS</span></span>

[<span data-ttu-id="69305-139">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="69305-139">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="69305-140">New-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="69305-140">New-AzRouteTable</span></span>](./New-AzRouteTable.md)

[<span data-ttu-id="69305-141">Set-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="69305-141">Set-AzRouteTable</span></span>](./Set-AzRouteTable.md)


