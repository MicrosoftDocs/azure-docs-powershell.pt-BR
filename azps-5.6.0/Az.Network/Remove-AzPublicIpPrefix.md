---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPublicIpPrefix.md
ms.openlocfilehash: f3072871caa5449606afe18093a463fea58c6dfa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888464"
---
# <span data-ttu-id="28cdd-101">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="28cdd-101">Remove-AzPublicIpPrefix</span></span>

## <span data-ttu-id="28cdd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28cdd-102">SYNOPSIS</span></span>
<span data-ttu-id="28cdd-103">Remove um prefixo IP público</span><span class="sxs-lookup"><span data-stu-id="28cdd-103">Removes a public IP prefix</span></span>

## <span data-ttu-id="28cdd-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="28cdd-104">SYNTAX</span></span>

### <span data-ttu-id="28cdd-105">RemoveByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="28cdd-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzPublicIpPrefix -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28cdd-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="28cdd-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzPublicIpPrefix -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28cdd-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="28cdd-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzPublicIpPrefix -InputObject <PSPublicIpPrefix> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28cdd-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="28cdd-108">DESCRIPTION</span></span>
<span data-ttu-id="28cdd-109">O cmdlet **Remove-AzPublicIpPrefix** remove um prefixo IP público do Azure, desde que não haja endereços IP públicos alocados dele.</span><span class="sxs-lookup"><span data-stu-id="28cdd-109">The **Remove-AzPublicIpPrefix** cmdlet removes an Azure public IP prefix as long as there are no public IP addresses allocated from it.</span></span>

## <span data-ttu-id="28cdd-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="28cdd-110">EXAMPLES</span></span>

### <span data-ttu-id="28cdd-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="28cdd-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName
```

<span data-ttu-id="28cdd-112">Remove o prefixo IP público com Nome $prefixName do grupo de recursos $rgName</span><span class="sxs-lookup"><span data-stu-id="28cdd-112">Removes the public IP prefix with Name $prefixName from resource group $rgName</span></span>

## <span data-ttu-id="28cdd-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="28cdd-113">PARAMETERS</span></span>

### <span data-ttu-id="28cdd-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="28cdd-114">-AsJob</span></span>
<span data-ttu-id="28cdd-115">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="28cdd-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="28cdd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28cdd-116">-DefaultProfile</span></span>
<span data-ttu-id="28cdd-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="28cdd-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28cdd-118">-Force</span><span class="sxs-lookup"><span data-stu-id="28cdd-118">-Force</span></span>
<span data-ttu-id="28cdd-119">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="28cdd-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="28cdd-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="28cdd-120">-InputObject</span></span>
<span data-ttu-id="28cdd-121">Um objeto PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="28cdd-121">A PublicIpPrefix object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="28cdd-122">-Name</span><span class="sxs-lookup"><span data-stu-id="28cdd-122">-Name</span></span>
<span data-ttu-id="28cdd-123">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="28cdd-123">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28cdd-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="28cdd-124">-PassThru</span></span>
<span data-ttu-id="28cdd-125">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="28cdd-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="28cdd-126">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="28cdd-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="28cdd-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28cdd-127">-ResourceGroupName</span></span>
<span data-ttu-id="28cdd-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="28cdd-128">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28cdd-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="28cdd-129">-ResourceId</span></span>
<span data-ttu-id="28cdd-130">O resourceId do recurso a ser removido</span><span class="sxs-lookup"><span data-stu-id="28cdd-130">The resourceId for the resource to remove</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28cdd-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="28cdd-131">-Confirm</span></span>
<span data-ttu-id="28cdd-132">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="28cdd-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28cdd-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28cdd-133">-WhatIf</span></span>
<span data-ttu-id="28cdd-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="28cdd-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28cdd-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="28cdd-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28cdd-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28cdd-136">CommonParameters</span></span>
<span data-ttu-id="28cdd-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28cdd-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28cdd-138">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28cdd-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28cdd-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="28cdd-139">INPUTS</span></span>

### <span data-ttu-id="28cdd-140">System.String</span><span class="sxs-lookup"><span data-stu-id="28cdd-140">System.String</span></span>

### <span data-ttu-id="28cdd-141">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="28cdd-141">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="28cdd-142">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="28cdd-142">OUTPUTS</span></span>

### <span data-ttu-id="28cdd-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="28cdd-143">System.Boolean</span></span>

## <span data-ttu-id="28cdd-144">NOTES</span><span class="sxs-lookup"><span data-stu-id="28cdd-144">NOTES</span></span>

## <span data-ttu-id="28cdd-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="28cdd-145">RELATED LINKS</span></span>

[<span data-ttu-id="28cdd-146">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="28cdd-146">Get-AzPublicIpPrefix</span></span>](./Get-AzPublicIpPrefix.md)

[<span data-ttu-id="28cdd-147">New-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="28cdd-147">New-AzPublicIpPrefix</span></span>](./New-AzPublicIpPrefix.md)

[<span data-ttu-id="28cdd-148">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="28cdd-148">Set-AzPublicIpPrefix</span></span>](./Set-AzPublicIpPrefix.md)
