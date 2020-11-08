---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznatgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNatGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNatGateway.md
ms.openlocfilehash: 4940936a50156f8515885099a205a4fa3566a7b4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110465"
---
# <span data-ttu-id="3db29-101">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="3db29-101">Remove-AzNatGateway</span></span>

## <span data-ttu-id="3db29-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3db29-102">SYNOPSIS</span></span>
<span data-ttu-id="3db29-103">Remova o recurso de gateway NAT.</span><span class="sxs-lookup"><span data-stu-id="3db29-103">Remove Nat Gateway resource.</span></span>

## <span data-ttu-id="3db29-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3db29-104">SYNTAX</span></span>

### <span data-ttu-id="3db29-105">DeleteByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="3db29-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzNatGateway -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3db29-106">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3db29-106">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzNatGateway -InputObject <PSNatGateway> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3db29-107">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3db29-107">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzNatGateway -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3db29-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3db29-108">DESCRIPTION</span></span>
<span data-ttu-id="3db29-109">Remover recurso de gateway NAT</span><span class="sxs-lookup"><span data-stu-id="3db29-109">Remove Nat Gateway Resource</span></span>

## <span data-ttu-id="3db29-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3db29-110">EXAMPLES</span></span>

### <span data-ttu-id="3db29-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3db29-111">Example 1</span></span>
```powershell
PS C:> $nat = Get-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway"
PS C:> Remove-AzNatGateway -InputObject $nat
PS C:> Remove-AzNatGateway -ResourceId "/subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/natGateways/natgateway"
```

## <span data-ttu-id="3db29-112">OS</span><span class="sxs-lookup"><span data-stu-id="3db29-112">PARAMETERS</span></span>

### <span data-ttu-id="3db29-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3db29-113">-AsJob</span></span>
<span data-ttu-id="3db29-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="3db29-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3db29-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3db29-115">-DefaultProfile</span></span>
<span data-ttu-id="3db29-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3db29-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3db29-117">-Force</span><span class="sxs-lookup"><span data-stu-id="3db29-117">-Force</span></span>
<span data-ttu-id="3db29-118">Não peça confirmação se quiser excluir o recurso.</span><span class="sxs-lookup"><span data-stu-id="3db29-118">Do not ask for confirmation if you want to delete resource.</span></span>

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

### <span data-ttu-id="3db29-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3db29-119">-InputObject</span></span>
<span data-ttu-id="3db29-120">Especifica o recurso de gateway NAT.</span><span class="sxs-lookup"><span data-stu-id="3db29-120">Specifies the Nat Gateway resource.</span></span>

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

### <span data-ttu-id="3db29-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="3db29-121">-Name</span></span>
<span data-ttu-id="3db29-122">Nome do recurso de gateway NAT.</span><span class="sxs-lookup"><span data-stu-id="3db29-122">Name of the Nat Gateway resource.</span></span>

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

### <span data-ttu-id="3db29-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3db29-123">-PassThru</span></span>
<span data-ttu-id="3db29-124">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="3db29-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3db29-125">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="3db29-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3db29-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3db29-126">-ResourceGroupName</span></span>
<span data-ttu-id="3db29-127">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3db29-127">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="3db29-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3db29-128">-ResourceId</span></span>
<span data-ttu-id="3db29-129">ID do recurso associada ao gateway NAT.</span><span class="sxs-lookup"><span data-stu-id="3db29-129">Resource Id associated with the Nat Gateway.</span></span>

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

### <span data-ttu-id="3db29-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3db29-130">-Confirm</span></span>
<span data-ttu-id="3db29-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3db29-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3db29-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3db29-132">-WhatIf</span></span>
<span data-ttu-id="3db29-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3db29-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3db29-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3db29-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3db29-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3db29-135">CommonParameters</span></span>
<span data-ttu-id="3db29-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3db29-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3db29-137">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3db29-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3db29-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3db29-138">INPUTS</span></span>

### <span data-ttu-id="3db29-139">Microsoft. Azure. Commands. Network. Models. PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="3db29-139">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

### <span data-ttu-id="3db29-140">System. String</span><span class="sxs-lookup"><span data-stu-id="3db29-140">System.String</span></span>

## <span data-ttu-id="3db29-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3db29-141">OUTPUTS</span></span>

### <span data-ttu-id="3db29-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3db29-142">System.Boolean</span></span>

## <span data-ttu-id="3db29-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3db29-143">NOTES</span></span>

## <span data-ttu-id="3db29-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3db29-144">RELATED LINKS</span></span>
