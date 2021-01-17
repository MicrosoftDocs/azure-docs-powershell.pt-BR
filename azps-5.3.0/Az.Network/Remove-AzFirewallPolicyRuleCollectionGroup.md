---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azfirewallpolicyrulecollectiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewallPolicyRuleCollectionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewallPolicyRuleCollectionGroup.md
ms.openlocfilehash: 3c9b307b34d07ff6c9331dc8d72c1149c83ef374
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98428933"
---
# <span data-ttu-id="b1b63-101">Remove-AzFirewallPolicyRuleCollectionGroup</span><span class="sxs-lookup"><span data-stu-id="b1b63-101">Remove-AzFirewallPolicyRuleCollectionGroup</span></span>

## <span data-ttu-id="b1b63-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b1b63-102">SYNOPSIS</span></span>
<span data-ttu-id="b1b63-103">Remove um grupo de regras de política de firewall do Azure em uma política de firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="b1b63-103">Removes a Azure Firewall Policy Rule Collection Group in a Azure firewall policy</span></span>

## <span data-ttu-id="b1b63-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b1b63-104">SYNTAX</span></span>

### <span data-ttu-id="b1b63-105">RemoveByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="b1b63-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzFirewallPolicyRuleCollectionGroup -Name <String> -ResourceGroupName <String>
 -AzureFirewallPolicyName <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1b63-106">RemoveByParentInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1b63-106">RemoveByParentInputObjectParameterSet</span></span>
```
Remove-AzFirewallPolicyRuleCollectionGroup -Name <String> -FirewallPolicyObject <PSAzureFirewallPolicy>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b1b63-107">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1b63-107">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzFirewallPolicyRuleCollectionGroup -InputObject <PSAzureFirewallPolicyRuleCollectionGroupWrapper>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b1b63-108">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1b63-108">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzFirewallPolicyRuleCollectionGroup -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1b63-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b1b63-109">DESCRIPTION</span></span>
<span data-ttu-id="b1b63-110">O cmdlet **Remove-AzFirewallPolicyRuleCollectionGroup** remove um grupo de coleção de regras de uma política de firewall do Azure.</span><span class="sxs-lookup"><span data-stu-id="b1b63-110">The **Remove-AzFirewallPolicyRuleCollectionGroup** cmdlet removes a rule collection group from an Azure Firewall Policy.</span></span>

## <span data-ttu-id="b1b63-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b1b63-111">EXAMPLES</span></span>

### <span data-ttu-id="b1b63-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b1b63-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzFirewallPolicyRuleCollectionGroup -Name testRcGroup -FirewallPolicyObject $fp
```

<span data-ttu-id="b1b63-113">Este exemplo remove a regra de política de firewall colelction o grupo chamado "testRcGroup" no objeto de política de firewall $fp</span><span class="sxs-lookup"><span data-stu-id="b1b63-113">This example removes the firewall policy rule colelction group named "testRcGroup" in the firewall policy object $fp</span></span>

### <span data-ttu-id="b1b63-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="b1b63-114">Example 2</span></span>
```powershell
PS C:\> Remove-AzFirewallPolicyRuleCollectionGroup -Name testRcGroup -ResourceGroupName testRg -AzureFirewallPolicyName fpName 
```

<span data-ttu-id="b1b63-115">Este exemplo remove a regra de política de firewall colelction o grupo chamado "testRcGroup" no firewall chamado "fpName" Frpm os nomes de grupo de "testRg"</span><span class="sxs-lookup"><span data-stu-id="b1b63-115">This example removes the firewall policy rule colelction group named "testRcGroup" in the firewall named "fpName" frpm the resourcegroup names "testRg"</span></span>

## <span data-ttu-id="b1b63-116">OS</span><span class="sxs-lookup"><span data-stu-id="b1b63-116">PARAMETERS</span></span>

### <span data-ttu-id="b1b63-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b1b63-117">-AsJob</span></span>
<span data-ttu-id="b1b63-118">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="b1b63-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b1b63-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1b63-119">-DefaultProfile</span></span>
<span data-ttu-id="b1b63-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b1b63-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1b63-121">-AzureFirewallPolicyName</span><span class="sxs-lookup"><span data-stu-id="b1b63-121">-AzureFirewallPolicyName</span></span>
<span data-ttu-id="b1b63-122">O nome da política de firewall</span><span class="sxs-lookup"><span data-stu-id="b1b63-122">The name of the firewall policy</span></span>

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

### <span data-ttu-id="b1b63-123">-FirewallPolicyObject</span><span class="sxs-lookup"><span data-stu-id="b1b63-123">-FirewallPolicyObject</span></span>
<span data-ttu-id="b1b63-124">Política de firewall.</span><span class="sxs-lookup"><span data-stu-id="b1b63-124">Firewall Policy.</span></span>

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

### <span data-ttu-id="b1b63-125">-Force</span><span class="sxs-lookup"><span data-stu-id="b1b63-125">-Force</span></span>
<span data-ttu-id="b1b63-126">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="b1b63-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="b1b63-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b1b63-127">-InputObject</span></span>
<span data-ttu-id="b1b63-128">Objeto do grupo coleção de regras de política do firewall</span><span class="sxs-lookup"><span data-stu-id="b1b63-128">Firewall Policy Rule collection group object</span></span>

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

### <span data-ttu-id="b1b63-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="b1b63-129">-Name</span></span>
<span data-ttu-id="b1b63-130">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="b1b63-130">The resource name.</span></span>

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

### <span data-ttu-id="b1b63-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b1b63-131">-PassThru</span></span>
<span data-ttu-id="b1b63-132">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="b1b63-132">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b1b63-133">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="b1b63-133">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b1b63-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1b63-134">-ResourceGroupName</span></span>
<span data-ttu-id="b1b63-135">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b1b63-135">The resource group name.</span></span>

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

### <span data-ttu-id="b1b63-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b1b63-136">-ResourceId</span></span>
<span data-ttu-id="b1b63-137">A ID do recurso do agrupamento da coleção de regras</span><span class="sxs-lookup"><span data-stu-id="b1b63-137">The resource Id of the Rule collection groupy</span></span>

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

### <span data-ttu-id="b1b63-138">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b1b63-138">-Confirm</span></span>
<span data-ttu-id="b1b63-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1b63-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1b63-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1b63-140">-WhatIf</span></span>
<span data-ttu-id="b1b63-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b1b63-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1b63-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b1b63-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1b63-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1b63-143">CommonParameters</span></span>
<span data-ttu-id="b1b63-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1b63-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1b63-145">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b1b63-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1b63-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b1b63-146">INPUTS</span></span>

### <span data-ttu-id="b1b63-147">System. String</span><span class="sxs-lookup"><span data-stu-id="b1b63-147">System.String</span></span>

### <span data-ttu-id="b1b63-148">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="b1b63-148">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

### <span data-ttu-id="b1b63-149">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallPolicyRuleCollectionGroupWrapper</span><span class="sxs-lookup"><span data-stu-id="b1b63-149">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyRuleCollectionGroupWrapper</span></span>

## <span data-ttu-id="b1b63-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b1b63-150">OUTPUTS</span></span>

### <span data-ttu-id="b1b63-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b1b63-151">System.Boolean</span></span>

## <span data-ttu-id="b1b63-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b1b63-152">NOTES</span></span>

## <span data-ttu-id="b1b63-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b1b63-153">RELATED LINKS</span></span>
