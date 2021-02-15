---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: FDA33633-EB2E-4095-8498-DF8910F1D434
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteTable.md
ms.openlocfilehash: 8c899d975669404045aa40bee45ad287a26f8749
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115082"
---
# <span data-ttu-id="fa19d-101">Remove-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="fa19d-101">Remove-AzRouteTable</span></span>

## <span data-ttu-id="fa19d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fa19d-102">SYNOPSIS</span></span>
<span data-ttu-id="fa19d-103">Remove uma tabela de rota.</span><span class="sxs-lookup"><span data-stu-id="fa19d-103">Removes a route table.</span></span>

## <span data-ttu-id="fa19d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fa19d-104">SYNTAX</span></span>

```
Remove-AzRouteTable -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa19d-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="fa19d-105">DESCRIPTION</span></span>
<span data-ttu-id="fa19d-106">O **cmdlet Remove-AzRouteTable** remove uma tabela de rota do Azure.</span><span class="sxs-lookup"><span data-stu-id="fa19d-106">The **Remove-AzRouteTable** cmdlet removes an Azure route table.</span></span>

## <span data-ttu-id="fa19d-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="fa19d-107">EXAMPLES</span></span>

### <span data-ttu-id="fa19d-108">Exemplo 1: Remover uma tabela de rota</span><span class="sxs-lookup"><span data-stu-id="fa19d-108">Example 1: Remove a route table</span></span>
```
PS C:\>Remove-AzRouteTable -ResourceGroupName "ResourceGroup11 -Name "RouteTable01"
Confirm
Are you sure you want to remove resource 'RouteTable01'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="fa19d-109">Esse comando remove a tabela de rota chamada Roteamento01 no grupo de recursos chamado ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="fa19d-109">This command removes the route table named RouteTable01 in the resource group named ResourceGroup11.</span></span>
<span data-ttu-id="fa19d-110">O cmdlet solicita confirmação antes de remover a tabela.</span><span class="sxs-lookup"><span data-stu-id="fa19d-110">The cmdlet prompts you for confirmation before it removes the table.</span></span>

## <span data-ttu-id="fa19d-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fa19d-111">PARAMETERS</span></span>

### <span data-ttu-id="fa19d-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fa19d-112">-AsJob</span></span>
<span data-ttu-id="fa19d-113">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="fa19d-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fa19d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa19d-114">-DefaultProfile</span></span>
<span data-ttu-id="fa19d-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="fa19d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fa19d-116">-Forçar</span><span class="sxs-lookup"><span data-stu-id="fa19d-116">-Force</span></span>
<span data-ttu-id="fa19d-117">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="fa19d-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="fa19d-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="fa19d-118">-Name</span></span>
<span data-ttu-id="fa19d-119">Especifica o nome da tabela de rota que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="fa19d-119">Specifies the name of the route table that this cmdlet removes.</span></span>

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

### <span data-ttu-id="fa19d-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fa19d-120">-PassThru</span></span>
<span data-ttu-id="fa19d-121">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="fa19d-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="fa19d-122">Por padrão, esse cmdlet não gera saída.</span><span class="sxs-lookup"><span data-stu-id="fa19d-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="fa19d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa19d-123">-ResourceGroupName</span></span>
<span data-ttu-id="fa19d-124">Especifica o nome do grupo de recursos que contém a tabela de rota que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="fa19d-124">Specifies the name of the resource group that contains the route table that this cmdlet removes.</span></span>

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

### <span data-ttu-id="fa19d-125">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="fa19d-125">-Confirm</span></span>
<span data-ttu-id="fa19d-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fa19d-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa19d-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa19d-127">-WhatIf</span></span>
<span data-ttu-id="fa19d-128">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="fa19d-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa19d-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fa19d-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa19d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa19d-130">CommonParameters</span></span>
<span data-ttu-id="fa19d-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa19d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa19d-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa19d-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa19d-133">Entradas</span><span class="sxs-lookup"><span data-stu-id="fa19d-133">INPUTS</span></span>

### <span data-ttu-id="fa19d-134">System.String</span><span class="sxs-lookup"><span data-stu-id="fa19d-134">System.String</span></span>

## <span data-ttu-id="fa19d-135">Saídas</span><span class="sxs-lookup"><span data-stu-id="fa19d-135">OUTPUTS</span></span>

### <span data-ttu-id="fa19d-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fa19d-136">System.Boolean</span></span>

## <span data-ttu-id="fa19d-137">Notas</span><span class="sxs-lookup"><span data-stu-id="fa19d-137">NOTES</span></span>

## <span data-ttu-id="fa19d-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fa19d-138">RELATED LINKS</span></span>

[<span data-ttu-id="fa19d-139">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="fa19d-139">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="fa19d-140">New-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="fa19d-140">New-AzRouteTable</span></span>](./New-AzRouteTable.md)

[<span data-ttu-id="fa19d-141">Set-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="fa19d-141">Set-AzRouteTable</span></span>](./Set-AzRouteTable.md)


