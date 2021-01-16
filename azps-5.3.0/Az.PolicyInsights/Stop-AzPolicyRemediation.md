---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/stop-azpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Stop-AzPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Stop-AzPolicyRemediation.md
ms.openlocfilehash: 9dfb3ff2f50df7a858ab8194ec86fa312501dcff
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98271655"
---
# <span data-ttu-id="c41b0-101">Stop-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="c41b0-101">Stop-AzPolicyRemediation</span></span>

## <span data-ttu-id="c41b0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c41b0-102">SYNOPSIS</span></span>
<span data-ttu-id="c41b0-103">Cancela uma remediação de política em andamento.</span><span class="sxs-lookup"><span data-stu-id="c41b0-103">Cancels an in-progress policy remediation.</span></span>

## <span data-ttu-id="c41b0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c41b0-104">SYNTAX</span></span>

### <span data-ttu-id="c41b0-105">ByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="c41b0-105">ByName (Default)</span></span>
```
Stop-AzPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c41b0-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c41b0-106">ByResourceId</span></span>
```
Stop-AzPolicyRemediation -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c41b0-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="c41b0-107">ByInputObject</span></span>
```
Stop-AzPolicyRemediation -InputObject <PSRemediation> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c41b0-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c41b0-108">DESCRIPTION</span></span>
<span data-ttu-id="c41b0-109">O cmdlet **Stop-AzPolicyRemediation** cancela uma remediação em andamento da política.</span><span class="sxs-lookup"><span data-stu-id="c41b0-109">The **Stop-AzPolicyRemediation** cmdlet cancels an in-progress policy remediation.</span></span> <span data-ttu-id="c41b0-110">Implantações ativas serão canceladas e nenhuma nova implantação será criada.</span><span class="sxs-lookup"><span data-stu-id="c41b0-110">Active deployments will be canceled and no new deployments will be created.</span></span>

## <span data-ttu-id="c41b0-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c41b0-111">EXAMPLES</span></span>

### <span data-ttu-id="c41b0-112">Exemplo 1: cancelar uma correção de política em escopo do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="c41b0-112">Example 1: Cancel a policy remediation at resource group scope</span></span>
```
PS C:\> Stop-AzPolicyRemediation -ResourceGroupName "myRG" -Name "remediation1"
```

<span data-ttu-id="c41b0-113">Este comando cancela a correção chamada "remediation1" no grupo de recursos "myRG".</span><span class="sxs-lookup"><span data-stu-id="c41b0-113">This command cancels the remediation named 'remediation1' in resource group 'myRG'.</span></span>

### <span data-ttu-id="c41b0-114">Exemplo 2: cancelar uma correção de grupo de gerenciamento via tubulação</span><span class="sxs-lookup"><span data-stu-id="c41b0-114">Example 2: Cancel a management group remediation via piping</span></span>
```
PS C:\> $remediation = Get-AzPolicyRemediation -ManagementGroupName "mg1" -Name "remediation1"
PS C:\> $remediation | Stop-AzPolicyRemediation
```

<span data-ttu-id="c41b0-115">Este comando cancela a correção chamada ' remediation1 ' no grupo de gerenciamento ' MG1 '.</span><span class="sxs-lookup"><span data-stu-id="c41b0-115">This command cancels the remediation named 'remediation1' in management group 'mg1'.</span></span>

## <span data-ttu-id="c41b0-116">OS</span><span class="sxs-lookup"><span data-stu-id="c41b0-116">PARAMETERS</span></span>

### <span data-ttu-id="c41b0-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c41b0-117">-AsJob</span></span>
<span data-ttu-id="c41b0-118">Execute o cmdlet em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="c41b0-118">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="c41b0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c41b0-119">-DefaultProfile</span></span>
<span data-ttu-id="c41b0-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c41b0-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c41b0-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c41b0-121">-InputObject</span></span>
<span data-ttu-id="c41b0-122">O objeto remediate.</span><span class="sxs-lookup"><span data-stu-id="c41b0-122">The Remediation object.</span></span>

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

### <span data-ttu-id="c41b0-123">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="c41b0-123">-ManagementGroupName</span></span>
<span data-ttu-id="c41b0-124">ID do grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="c41b0-124">Management group ID.</span></span>

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

### <span data-ttu-id="c41b0-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="c41b0-125">-Name</span></span>
<span data-ttu-id="c41b0-126">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="c41b0-126">Resource name.</span></span>

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

### <span data-ttu-id="c41b0-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c41b0-127">-PassThru</span></span>
<span data-ttu-id="c41b0-128">Retorne true se o comando for concluído com êxito.</span><span class="sxs-lookup"><span data-stu-id="c41b0-128">Return True if the command completes successfully.</span></span>

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

### <span data-ttu-id="c41b0-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c41b0-129">-ResourceGroupName</span></span>
<span data-ttu-id="c41b0-130">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c41b0-130">Resource group name.</span></span>

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

### <span data-ttu-id="c41b0-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c41b0-131">-ResourceId</span></span>
<span data-ttu-id="c41b0-132">ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="c41b0-132">Resource ID.</span></span>

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

### <span data-ttu-id="c41b0-133">-Escopo</span><span class="sxs-lookup"><span data-stu-id="c41b0-133">-Scope</span></span>
<span data-ttu-id="c41b0-134">Escopo do recurso.</span><span class="sxs-lookup"><span data-stu-id="c41b0-134">Scope of the resource.</span></span>
<span data-ttu-id="c41b0-135">:.</span><span class="sxs-lookup"><span data-stu-id="c41b0-135">E.g.</span></span>
<span data-ttu-id="c41b0-136">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span><span class="sxs-lookup"><span data-stu-id="c41b0-136">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

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

### <span data-ttu-id="c41b0-137">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c41b0-137">-Confirm</span></span>
<span data-ttu-id="c41b0-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c41b0-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c41b0-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c41b0-139">-WhatIf</span></span>
<span data-ttu-id="c41b0-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c41b0-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c41b0-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c41b0-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c41b0-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c41b0-142">CommonParameters</span></span>
<span data-ttu-id="c41b0-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c41b0-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c41b0-144">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c41b0-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c41b0-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c41b0-145">INPUTS</span></span>

### <span data-ttu-id="c41b0-146">System. String</span><span class="sxs-lookup"><span data-stu-id="c41b0-146">System.String</span></span>

### <span data-ttu-id="c41b0-147">Microsoft. Azure. Commands. PolicyInsights. Models. remediation. PSRemediation</span><span class="sxs-lookup"><span data-stu-id="c41b0-147">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="c41b0-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c41b0-148">OUTPUTS</span></span>

### <span data-ttu-id="c41b0-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c41b0-149">System.Boolean</span></span>

## <span data-ttu-id="c41b0-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c41b0-150">NOTES</span></span>

## <span data-ttu-id="c41b0-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c41b0-151">RELATED LINKS</span></span>
