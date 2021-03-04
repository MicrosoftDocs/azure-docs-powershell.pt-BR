---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azfirewallpolicyrulecollectiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewallPolicyRuleCollectionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewallPolicyRuleCollectionGroup.md
ms.openlocfilehash: 50dd0f1b4f224b343d827ed3d07457d86352e96e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890773"
---
# <span data-ttu-id="ca98b-101">Remove-AzFirewallPolicyRuleCollectionGroup</span><span class="sxs-lookup"><span data-stu-id="ca98b-101">Remove-AzFirewallPolicyRuleCollectionGroup</span></span>

## <span data-ttu-id="ca98b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca98b-102">SYNOPSIS</span></span>
<span data-ttu-id="ca98b-103">Remove um Grupo de Conjunto de Regras de Política de Firewall do Azure em uma política de firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="ca98b-103">Removes a Azure Firewall Policy Rule Collection Group in a Azure firewall policy</span></span>

## <span data-ttu-id="ca98b-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ca98b-104">SYNTAX</span></span>

### <span data-ttu-id="ca98b-105">RemoveByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ca98b-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzFirewallPolicyRuleCollectionGroup -Name <String> -ResourceGroupName <String>
 -AzureFirewallPolicyName <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca98b-106">RemoveByParentInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca98b-106">RemoveByParentInputObjectParameterSet</span></span>
```
Remove-AzFirewallPolicyRuleCollectionGroup -Name <String> -FirewallPolicyObject <PSAzureFirewallPolicy>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ca98b-107">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca98b-107">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzFirewallPolicyRuleCollectionGroup -InputObject <PSAzureFirewallPolicyRuleCollectionGroupWrapper>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ca98b-108">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca98b-108">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzFirewallPolicyRuleCollectionGroup -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca98b-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ca98b-109">DESCRIPTION</span></span>
<span data-ttu-id="ca98b-110">O cmdlet **Remove-AzFirewallPolicyRuleCollectionGroup** remove um grupo de conjunto de regras de uma Política de Firewall do Azure.</span><span class="sxs-lookup"><span data-stu-id="ca98b-110">The **Remove-AzFirewallPolicyRuleCollectionGroup** cmdlet removes a rule collection group from an Azure Firewall Policy.</span></span>

## <span data-ttu-id="ca98b-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ca98b-111">EXAMPLES</span></span>

### <span data-ttu-id="ca98b-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ca98b-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzFirewallPolicyRuleCollectionGroup -Name testRcGroup -FirewallPolicyObject $fp
```

<span data-ttu-id="ca98b-113">Este exemplo remove o grupo de coleções de regras de política de firewall chamado "testRcGroup" no objeto de política de firewall $fp</span><span class="sxs-lookup"><span data-stu-id="ca98b-113">This example removes the firewall policy rule colelction group named "testRcGroup" in the firewall policy object $fp</span></span>

### <span data-ttu-id="ca98b-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="ca98b-114">Example 2</span></span>
```powershell
PS C:\> Remove-AzFirewallPolicyRuleCollectionGroup -Name testRcGroup -ResourceGroupName testRg -AzureFirewallPolicyName fpName 
```

<span data-ttu-id="ca98b-115">Este exemplo remove o grupo de coleções de regra de política de firewall chamado "testRcGroup" no firewall chamado "fpName" frpm os nomes de grupo de recursos "testRg"</span><span class="sxs-lookup"><span data-stu-id="ca98b-115">This example removes the firewall policy rule colelction group named "testRcGroup" in the firewall named "fpName" frpm the resourcegroup names "testRg"</span></span>

## <span data-ttu-id="ca98b-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ca98b-116">PARAMETERS</span></span>

### <span data-ttu-id="ca98b-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ca98b-117">-AsJob</span></span>
<span data-ttu-id="ca98b-118">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="ca98b-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ca98b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca98b-119">-DefaultProfile</span></span>
<span data-ttu-id="ca98b-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ca98b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca98b-121">-AzureFirewallPolicyName</span><span class="sxs-lookup"><span data-stu-id="ca98b-121">-AzureFirewallPolicyName</span></span>
<span data-ttu-id="ca98b-122">O nome da política de firewall</span><span class="sxs-lookup"><span data-stu-id="ca98b-122">The name of the firewall policy</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca98b-123">-FirewallPolicyObject</span><span class="sxs-lookup"><span data-stu-id="ca98b-123">-FirewallPolicyObject</span></span>
<span data-ttu-id="ca98b-124">Política de Firewall.</span><span class="sxs-lookup"><span data-stu-id="ca98b-124">Firewall Policy.</span></span>

```yaml
Type: PSAzureFirewallPolicy
Parameter Sets: RemoveByParentInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca98b-125">-Force</span><span class="sxs-lookup"><span data-stu-id="ca98b-125">-Force</span></span>
<span data-ttu-id="ca98b-126">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="ca98b-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="ca98b-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ca98b-127">-InputObject</span></span>
<span data-ttu-id="ca98b-128">Objeto do grupo de conjunto de regras de política de firewall</span><span class="sxs-lookup"><span data-stu-id="ca98b-128">Firewall Policy Rule collection group object</span></span>

```yaml
Type: PSAzureFirewallPolicyRuleCollectionGroupWrapper
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ca98b-129">-Name</span><span class="sxs-lookup"><span data-stu-id="ca98b-129">-Name</span></span>
<span data-ttu-id="ca98b-130">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="ca98b-130">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: RemoveByParentInputObjectParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca98b-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ca98b-131">-PassThru</span></span>
<span data-ttu-id="ca98b-132">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="ca98b-132">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ca98b-133">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="ca98b-133">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ca98b-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca98b-134">-ResourceGroupName</span></span>
<span data-ttu-id="ca98b-135">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ca98b-135">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca98b-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ca98b-136">-ResourceId</span></span>
<span data-ttu-id="ca98b-137">A ID de recurso do groupy da coleção Rule</span><span class="sxs-lookup"><span data-stu-id="ca98b-137">The resource Id of the Rule collection groupy</span></span>

```yaml
Type: String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca98b-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ca98b-138">-Confirm</span></span>
<span data-ttu-id="ca98b-139">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca98b-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca98b-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca98b-140">-WhatIf</span></span>
<span data-ttu-id="ca98b-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ca98b-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca98b-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ca98b-142">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca98b-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca98b-143">CommonParameters</span></span>
<span data-ttu-id="ca98b-144">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca98b-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca98b-145">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ca98b-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca98b-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ca98b-146">INPUTS</span></span>

### <span data-ttu-id="ca98b-147">System.String</span><span class="sxs-lookup"><span data-stu-id="ca98b-147">System.String</span></span>

### <span data-ttu-id="ca98b-148">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="ca98b-148">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

### <span data-ttu-id="ca98b-149">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyRuleCollectionGroupWrapper</span><span class="sxs-lookup"><span data-stu-id="ca98b-149">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyRuleCollectionGroupWrapper</span></span>

## <span data-ttu-id="ca98b-150">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ca98b-150">OUTPUTS</span></span>

### <span data-ttu-id="ca98b-151">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ca98b-151">System.Boolean</span></span>

## <span data-ttu-id="ca98b-152">NOTES</span><span class="sxs-lookup"><span data-stu-id="ca98b-152">NOTES</span></span>

## <span data-ttu-id="ca98b-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ca98b-153">RELATED LINKS</span></span>
