---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azfirewallpolicyrulecollectiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewallPolicyRuleCollectionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewallPolicyRuleCollectionGroup.md
ms.openlocfilehash: 3c9b307b34d07ff6c9331dc8d72c1149c83ef374
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98263128"
---
# <span data-ttu-id="ec658-101">Remove-AzFirewallPolicyRuleCollectionGroup</span><span class="sxs-lookup"><span data-stu-id="ec658-101">Remove-AzFirewallPolicyRuleCollectionGroup</span></span>

## <span data-ttu-id="ec658-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ec658-102">SYNOPSIS</span></span>
<span data-ttu-id="ec658-103">Remove um grupo de regras de política de firewall do Azure em uma política de firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="ec658-103">Removes a Azure Firewall Policy Rule Collection Group in a Azure firewall policy</span></span>

## <span data-ttu-id="ec658-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ec658-104">SYNTAX</span></span>

### <span data-ttu-id="ec658-105">RemoveByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="ec658-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzFirewallPolicyRuleCollectionGroup -Name <String> -ResourceGroupName <String>
 -AzureFirewallPolicyName <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec658-106">RemoveByParentInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ec658-106">RemoveByParentInputObjectParameterSet</span></span>
```
Remove-AzFirewallPolicyRuleCollectionGroup -Name <String> -FirewallPolicyObject <PSAzureFirewallPolicy>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ec658-107">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ec658-107">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzFirewallPolicyRuleCollectionGroup -InputObject <PSAzureFirewallPolicyRuleCollectionGroupWrapper>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ec658-108">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ec658-108">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzFirewallPolicyRuleCollectionGroup -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec658-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ec658-109">DESCRIPTION</span></span>
<span data-ttu-id="ec658-110">O cmdlet **Remove-AzFirewallPolicyRuleCollectionGroup** remove um grupo de coleção de regras de uma política de firewall do Azure.</span><span class="sxs-lookup"><span data-stu-id="ec658-110">The **Remove-AzFirewallPolicyRuleCollectionGroup** cmdlet removes a rule collection group from an Azure Firewall Policy.</span></span>

## <span data-ttu-id="ec658-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ec658-111">EXAMPLES</span></span>

### <span data-ttu-id="ec658-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ec658-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzFirewallPolicyRuleCollectionGroup -Name testRcGroup -FirewallPolicyObject $fp
```

<span data-ttu-id="ec658-113">Este exemplo remove a regra de política de firewall colelction o grupo chamado "testRcGroup" no objeto de política de firewall $fp</span><span class="sxs-lookup"><span data-stu-id="ec658-113">This example removes the firewall policy rule colelction group named "testRcGroup" in the firewall policy object $fp</span></span>

### <span data-ttu-id="ec658-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="ec658-114">Example 2</span></span>
```powershell
PS C:\> Remove-AzFirewallPolicyRuleCollectionGroup -Name testRcGroup -ResourceGroupName testRg -AzureFirewallPolicyName fpName 
```

<span data-ttu-id="ec658-115">Este exemplo remove a regra de política de firewall colelction o grupo chamado "testRcGroup" no firewall chamado "fpName" Frpm os nomes de grupo de "testRg"</span><span class="sxs-lookup"><span data-stu-id="ec658-115">This example removes the firewall policy rule colelction group named "testRcGroup" in the firewall named "fpName" frpm the resourcegroup names "testRg"</span></span>

## <span data-ttu-id="ec658-116">OS</span><span class="sxs-lookup"><span data-stu-id="ec658-116">PARAMETERS</span></span>

### <span data-ttu-id="ec658-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ec658-117">-AsJob</span></span>
<span data-ttu-id="ec658-118">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="ec658-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ec658-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec658-119">-DefaultProfile</span></span>
<span data-ttu-id="ec658-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ec658-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec658-121">-AzureFirewallPolicyName</span><span class="sxs-lookup"><span data-stu-id="ec658-121">-AzureFirewallPolicyName</span></span>
<span data-ttu-id="ec658-122">O nome da política de firewall</span><span class="sxs-lookup"><span data-stu-id="ec658-122">The name of the firewall policy</span></span>

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

### <span data-ttu-id="ec658-123">-FirewallPolicyObject</span><span class="sxs-lookup"><span data-stu-id="ec658-123">-FirewallPolicyObject</span></span>
<span data-ttu-id="ec658-124">Política de firewall.</span><span class="sxs-lookup"><span data-stu-id="ec658-124">Firewall Policy.</span></span>

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

### <span data-ttu-id="ec658-125">-Force</span><span class="sxs-lookup"><span data-stu-id="ec658-125">-Force</span></span>
<span data-ttu-id="ec658-126">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="ec658-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="ec658-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ec658-127">-InputObject</span></span>
<span data-ttu-id="ec658-128">Objeto do grupo coleção de regras de política do firewall</span><span class="sxs-lookup"><span data-stu-id="ec658-128">Firewall Policy Rule collection group object</span></span>

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

### <span data-ttu-id="ec658-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="ec658-129">-Name</span></span>
<span data-ttu-id="ec658-130">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="ec658-130">The resource name.</span></span>

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

### <span data-ttu-id="ec658-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ec658-131">-PassThru</span></span>
<span data-ttu-id="ec658-132">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="ec658-132">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ec658-133">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="ec658-133">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ec658-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec658-134">-ResourceGroupName</span></span>
<span data-ttu-id="ec658-135">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ec658-135">The resource group name.</span></span>

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

### <span data-ttu-id="ec658-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ec658-136">-ResourceId</span></span>
<span data-ttu-id="ec658-137">A ID do recurso do agrupamento da coleção de regras</span><span class="sxs-lookup"><span data-stu-id="ec658-137">The resource Id of the Rule collection groupy</span></span>

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

### <span data-ttu-id="ec658-138">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ec658-138">-Confirm</span></span>
<span data-ttu-id="ec658-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ec658-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec658-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec658-140">-WhatIf</span></span>
<span data-ttu-id="ec658-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ec658-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec658-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ec658-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec658-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec658-143">CommonParameters</span></span>
<span data-ttu-id="ec658-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec658-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec658-145">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ec658-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec658-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ec658-146">INPUTS</span></span>

### <span data-ttu-id="ec658-147">System. String</span><span class="sxs-lookup"><span data-stu-id="ec658-147">System.String</span></span>

### <span data-ttu-id="ec658-148">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="ec658-148">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

### <span data-ttu-id="ec658-149">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallPolicyRuleCollectionGroupWrapper</span><span class="sxs-lookup"><span data-stu-id="ec658-149">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyRuleCollectionGroupWrapper</span></span>

## <span data-ttu-id="ec658-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ec658-150">OUTPUTS</span></span>

### <span data-ttu-id="ec658-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ec658-151">System.Boolean</span></span>

## <span data-ttu-id="ec658-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ec658-152">NOTES</span></span>

## <span data-ttu-id="ec658-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ec658-153">RELATED LINKS</span></span>
