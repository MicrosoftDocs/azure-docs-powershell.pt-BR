---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznatgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNatGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNatGateway.md
ms.openlocfilehash: 4940936a50156f8515885099a205a4fa3566a7b4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118284"
---
# <span data-ttu-id="02b3e-101">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="02b3e-101">Remove-AzNatGateway</span></span>

## <span data-ttu-id="02b3e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="02b3e-102">SYNOPSIS</span></span>
<span data-ttu-id="02b3e-103">Remover o recurso Nat Gateway.</span><span class="sxs-lookup"><span data-stu-id="02b3e-103">Remove Nat Gateway resource.</span></span>

## <span data-ttu-id="02b3e-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="02b3e-104">SYNTAX</span></span>

### <span data-ttu-id="02b3e-105">DeleteByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="02b3e-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzNatGateway -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02b3e-106">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="02b3e-106">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzNatGateway -InputObject <PSNatGateway> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02b3e-107">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="02b3e-107">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzNatGateway -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02b3e-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="02b3e-108">DESCRIPTION</span></span>
<span data-ttu-id="02b3e-109">Remover Recurso do Gateway Nat</span><span class="sxs-lookup"><span data-stu-id="02b3e-109">Remove Nat Gateway Resource</span></span>

## <span data-ttu-id="02b3e-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="02b3e-110">EXAMPLES</span></span>

### <span data-ttu-id="02b3e-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="02b3e-111">Example 1</span></span>
```powershell
PS C:> $nat = Get-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway"
PS C:> Remove-AzNatGateway -InputObject $nat
PS C:> Remove-AzNatGateway -ResourceId "/subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/natGateways/natgateway"
```

## <span data-ttu-id="02b3e-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="02b3e-112">PARAMETERS</span></span>

### <span data-ttu-id="02b3e-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="02b3e-113">-AsJob</span></span>
<span data-ttu-id="02b3e-114">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="02b3e-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="02b3e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02b3e-115">-DefaultProfile</span></span>
<span data-ttu-id="02b3e-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="02b3e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02b3e-117">-Forçar</span><span class="sxs-lookup"><span data-stu-id="02b3e-117">-Force</span></span>
<span data-ttu-id="02b3e-118">Não peça confirmação se quiser excluir o recurso.</span><span class="sxs-lookup"><span data-stu-id="02b3e-118">Do not ask for confirmation if you want to delete resource.</span></span>

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

### <span data-ttu-id="02b3e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="02b3e-119">-InputObject</span></span>
<span data-ttu-id="02b3e-120">Especifica o recurso Nat Gateway.</span><span class="sxs-lookup"><span data-stu-id="02b3e-120">Specifies the Nat Gateway resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNatGateway
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: NatGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="02b3e-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="02b3e-121">-Name</span></span>
<span data-ttu-id="02b3e-122">Nome do recurso Nat Gateway.</span><span class="sxs-lookup"><span data-stu-id="02b3e-122">Name of the Nat Gateway resource.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02b3e-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="02b3e-123">-PassThru</span></span>
<span data-ttu-id="02b3e-124">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="02b3e-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="02b3e-125">Por padrão, esse cmdlet não gera saída.</span><span class="sxs-lookup"><span data-stu-id="02b3e-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="02b3e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02b3e-126">-ResourceGroupName</span></span>
<span data-ttu-id="02b3e-127">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="02b3e-127">Name of the Resource Group.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02b3e-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="02b3e-128">-ResourceId</span></span>
<span data-ttu-id="02b3e-129">ID do Recurso associada ao Gateway Nat.</span><span class="sxs-lookup"><span data-stu-id="02b3e-129">Resource Id associated with the Nat Gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases: NatGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02b3e-130">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="02b3e-130">-Confirm</span></span>
<span data-ttu-id="02b3e-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02b3e-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02b3e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02b3e-132">-WhatIf</span></span>
<span data-ttu-id="02b3e-133">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="02b3e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02b3e-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="02b3e-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02b3e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02b3e-135">CommonParameters</span></span>
<span data-ttu-id="02b3e-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02b3e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02b3e-137">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="02b3e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02b3e-138">Entradas</span><span class="sxs-lookup"><span data-stu-id="02b3e-138">INPUTS</span></span>

### <span data-ttu-id="02b3e-139">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="02b3e-139">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

### <span data-ttu-id="02b3e-140">System.String</span><span class="sxs-lookup"><span data-stu-id="02b3e-140">System.String</span></span>

## <span data-ttu-id="02b3e-141">Saídas</span><span class="sxs-lookup"><span data-stu-id="02b3e-141">OUTPUTS</span></span>

### <span data-ttu-id="02b3e-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="02b3e-142">System.Boolean</span></span>

## <span data-ttu-id="02b3e-143">Notas</span><span class="sxs-lookup"><span data-stu-id="02b3e-143">NOTES</span></span>

## <span data-ttu-id="02b3e-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="02b3e-144">RELATED LINKS</span></span>
