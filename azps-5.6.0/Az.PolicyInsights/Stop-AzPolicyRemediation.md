---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/powershell/module/az.policyinsights/stop-azpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Stop-AzPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Stop-AzPolicyRemediation.md
ms.openlocfilehash: 2eb9d5a11b160a1061bbd769f337cf053b6ad805
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890102"
---
# <span data-ttu-id="f1a20-101">Stop-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="f1a20-101">Stop-AzPolicyRemediation</span></span>

## <span data-ttu-id="f1a20-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1a20-102">SYNOPSIS</span></span>
<span data-ttu-id="f1a20-103">Cancela uma correção de política em andamento.</span><span class="sxs-lookup"><span data-stu-id="f1a20-103">Cancels an in-progress policy remediation.</span></span>

## <span data-ttu-id="f1a20-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f1a20-104">SYNTAX</span></span>

### <span data-ttu-id="f1a20-105">ByName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="f1a20-105">ByName (Default)</span></span>
```
Stop-AzPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1a20-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="f1a20-106">ByResourceId</span></span>
```
Stop-AzPolicyRemediation -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1a20-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="f1a20-107">ByInputObject</span></span>
```
Stop-AzPolicyRemediation -InputObject <PSRemediation> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1a20-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f1a20-108">DESCRIPTION</span></span>
<span data-ttu-id="f1a20-109">O cmdlet **Stop-AzPolicyRemediation** cancela uma correção de política em andamento.</span><span class="sxs-lookup"><span data-stu-id="f1a20-109">The **Stop-AzPolicyRemediation** cmdlet cancels an in-progress policy remediation.</span></span> <span data-ttu-id="f1a20-110">As implantações ativas serão canceladas e nenhuma nova implantação será criada.</span><span class="sxs-lookup"><span data-stu-id="f1a20-110">Active deployments will be canceled and no new deployments will be created.</span></span>

## <span data-ttu-id="f1a20-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f1a20-111">EXAMPLES</span></span>

### <span data-ttu-id="f1a20-112">Exemplo 1: Cancelar uma correção de política no escopo do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="f1a20-112">Example 1: Cancel a policy remediation at resource group scope</span></span>
```
PS C:\> Stop-AzPolicyRemediation -ResourceGroupName "myRG" -Name "remediation1"
```

<span data-ttu-id="f1a20-113">Esse comando cancela a correção chamada 'correção1' no grupo de recursos 'myRG'.</span><span class="sxs-lookup"><span data-stu-id="f1a20-113">This command cancels the remediation named 'remediation1' in resource group 'myRG'.</span></span>

### <span data-ttu-id="f1a20-114">Exemplo 2: Cancelar uma correção de grupo de gerenciamento por meio de canalização</span><span class="sxs-lookup"><span data-stu-id="f1a20-114">Example 2: Cancel a management group remediation via piping</span></span>
```
PS C:\> $remediation = Get-AzPolicyRemediation -ManagementGroupName "mg1" -Name "remediation1"
PS C:\> $remediation | Stop-AzPolicyRemediation
```

<span data-ttu-id="f1a20-115">Este comando cancela a correção chamada 'correção1' no grupo de gerenciamento 'mg1'.</span><span class="sxs-lookup"><span data-stu-id="f1a20-115">This command cancels the remediation named 'remediation1' in management group 'mg1'.</span></span>

## <span data-ttu-id="f1a20-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f1a20-116">PARAMETERS</span></span>

### <span data-ttu-id="f1a20-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f1a20-117">-AsJob</span></span>
<span data-ttu-id="f1a20-118">Execute o cmdlet em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="f1a20-118">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="f1a20-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1a20-119">-DefaultProfile</span></span>
<span data-ttu-id="f1a20-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f1a20-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1a20-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f1a20-121">-InputObject</span></span>
<span data-ttu-id="f1a20-122">O objeto Remediation.</span><span class="sxs-lookup"><span data-stu-id="f1a20-122">The Remediation object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f1a20-123">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="f1a20-123">-ManagementGroupName</span></span>
<span data-ttu-id="f1a20-124">ID do grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="f1a20-124">Management group ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1a20-125">-Name</span><span class="sxs-lookup"><span data-stu-id="f1a20-125">-Name</span></span>
<span data-ttu-id="f1a20-126">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="f1a20-126">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1a20-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f1a20-127">-PassThru</span></span>
<span data-ttu-id="f1a20-128">Retornar True se o comando for concluído com êxito.</span><span class="sxs-lookup"><span data-stu-id="f1a20-128">Return True if the command completes successfully.</span></span>

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

### <span data-ttu-id="f1a20-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1a20-129">-ResourceGroupName</span></span>
<span data-ttu-id="f1a20-130">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f1a20-130">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1a20-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f1a20-131">-ResourceId</span></span>
<span data-ttu-id="f1a20-132">ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="f1a20-132">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1a20-133">-Scope</span><span class="sxs-lookup"><span data-stu-id="f1a20-133">-Scope</span></span>
<span data-ttu-id="f1a20-134">Escopo do recurso.</span><span class="sxs-lookup"><span data-stu-id="f1a20-134">Scope of the resource.</span></span>
<span data-ttu-id="f1a20-135">Por exemplo,</span><span class="sxs-lookup"><span data-stu-id="f1a20-135">E.g.</span></span>
<span data-ttu-id="f1a20-136">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span><span class="sxs-lookup"><span data-stu-id="f1a20-136">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1a20-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f1a20-137">-Confirm</span></span>
<span data-ttu-id="f1a20-138">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f1a20-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1a20-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1a20-139">-WhatIf</span></span>
<span data-ttu-id="f1a20-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f1a20-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1a20-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f1a20-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1a20-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1a20-142">CommonParameters</span></span>
<span data-ttu-id="f1a20-143">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1a20-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1a20-144">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f1a20-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1a20-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f1a20-145">INPUTS</span></span>

### <span data-ttu-id="f1a20-146">System.String</span><span class="sxs-lookup"><span data-stu-id="f1a20-146">System.String</span></span>

### <span data-ttu-id="f1a20-147">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span><span class="sxs-lookup"><span data-stu-id="f1a20-147">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="f1a20-148">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f1a20-148">OUTPUTS</span></span>

### <span data-ttu-id="f1a20-149">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f1a20-149">System.Boolean</span></span>

## <span data-ttu-id="f1a20-150">NOTES</span><span class="sxs-lookup"><span data-stu-id="f1a20-150">NOTES</span></span>

## <span data-ttu-id="f1a20-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f1a20-151">RELATED LINKS</span></span>
