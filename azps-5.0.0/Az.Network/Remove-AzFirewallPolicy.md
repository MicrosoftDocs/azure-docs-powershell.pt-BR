---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewallPolicy.md
ms.openlocfilehash: a6539d1569d3dc4f0d12190b6b1d0670b036c30a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94116089"
---
# <span data-ttu-id="1dc96-101">Remove-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="1dc96-101">Remove-AzFirewallPolicy</span></span>

## <span data-ttu-id="1dc96-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1dc96-102">SYNOPSIS</span></span>
<span data-ttu-id="1dc96-103">Remove uma política de firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="1dc96-103">Removes an Azure Firewall Policy</span></span>

## <span data-ttu-id="1dc96-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1dc96-104">SYNTAX</span></span>

### <span data-ttu-id="1dc96-105">RemoveByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1dc96-105">RemoveByNameParameterSet</span></span>
```
Remove-AzFirewallPolicy -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1dc96-106">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1dc96-106">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzFirewallPolicy [-Force] [-PassThru] [-AsJob] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1dc96-107">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1dc96-107">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzFirewallPolicy [-Force] [-PassThru] [-AsJob] -InputObject <PSAzureFirewallPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1dc96-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1dc96-108">DESCRIPTION</span></span>
<span data-ttu-id="1dc96-109">O cmdlet **Remove-AzFirewallPolicy** remove uma política de firewall do Azure.</span><span class="sxs-lookup"><span data-stu-id="1dc96-109">The **Remove-AzFirewallPolicy** cmdlet removes an Azure Firewall Policy.</span></span>

## <span data-ttu-id="1dc96-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1dc96-110">EXAMPLES</span></span>

### <span data-ttu-id="1dc96-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1dc96-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzFirewallPolicy -Name firewallpolicy -ResourceGroupName TestRg
```

<span data-ttu-id="1dc96-112">Este exemplo remove a política de firewall chamada "firewallpolicy" no TestRg ".</span><span class="sxs-lookup"><span data-stu-id="1dc96-112">This example removes the firewall policy named "firewallpolicy" in the resourcegroup "TestRg"</span></span>

### <span data-ttu-id="1dc96-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="1dc96-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzFirewallPolicy -Name firewallpolicy -ResourceId "/subscriptions/12345/resourceGroups/TestRg/providers/Microsoft.Network/firewallpolicies/firewallPolicy1"
```

<span data-ttu-id="1dc96-114">Este exemplo remove a política de firewall pela ID.</span><span class="sxs-lookup"><span data-stu-id="1dc96-114">This example removes the firewall policy by the Id.</span></span>

### <span data-ttu-id="1dc96-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="1dc96-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzFirewallPolicy -InputObject $fp
```

<span data-ttu-id="1dc96-116">Este exemplo remove a política de firewall $fp</span><span class="sxs-lookup"><span data-stu-id="1dc96-116">This example removes the firewall policy $fp</span></span>

## <span data-ttu-id="1dc96-117">OS</span><span class="sxs-lookup"><span data-stu-id="1dc96-117">PARAMETERS</span></span>

### <span data-ttu-id="1dc96-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1dc96-118">-AsJob</span></span>
<span data-ttu-id="1dc96-119">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="1dc96-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1dc96-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dc96-120">-DefaultProfile</span></span>
<span data-ttu-id="1dc96-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1dc96-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1dc96-122">-Force</span><span class="sxs-lookup"><span data-stu-id="1dc96-122">-Force</span></span>
<span data-ttu-id="1dc96-123">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="1dc96-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="1dc96-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1dc96-124">-InputObject</span></span>
<span data-ttu-id="1dc96-125">A política AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="1dc96-125">The AzureFirewall Policy</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1dc96-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="1dc96-126">-Name</span></span>
<span data-ttu-id="1dc96-127">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="1dc96-127">The resource name.</span></span>

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

### <span data-ttu-id="1dc96-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1dc96-128">-PassThru</span></span>
<span data-ttu-id="1dc96-129">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="1dc96-129">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="1dc96-130">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="1dc96-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1dc96-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1dc96-131">-ResourceGroupName</span></span>
<span data-ttu-id="1dc96-132">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1dc96-132">The resource group name.</span></span>

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

### <span data-ttu-id="1dc96-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1dc96-133">-ResourceId</span></span>
<span data-ttu-id="1dc96-134">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="1dc96-134">The resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dc96-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1dc96-135">-Confirm</span></span>
<span data-ttu-id="1dc96-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1dc96-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1dc96-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1dc96-137">-WhatIf</span></span>
<span data-ttu-id="1dc96-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1dc96-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1dc96-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1dc96-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1dc96-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dc96-140">CommonParameters</span></span>
<span data-ttu-id="1dc96-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1dc96-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dc96-142">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1dc96-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dc96-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1dc96-143">INPUTS</span></span>

### <span data-ttu-id="1dc96-144">System. String</span><span class="sxs-lookup"><span data-stu-id="1dc96-144">System.String</span></span>

### <span data-ttu-id="1dc96-145">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="1dc96-145">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

## <span data-ttu-id="1dc96-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1dc96-146">OUTPUTS</span></span>

### <span data-ttu-id="1dc96-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1dc96-147">System.Boolean</span></span>

## <span data-ttu-id="1dc96-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1dc96-148">NOTES</span></span>

## <span data-ttu-id="1dc96-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1dc96-149">RELATED LINKS</span></span>
