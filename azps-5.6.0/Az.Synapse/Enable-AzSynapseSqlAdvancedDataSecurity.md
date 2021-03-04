---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/enable-azsynapsesqladvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Enable-AzSynapseSqlAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Enable-AzSynapseSqlAdvancedDataSecurity.md
ms.openlocfilehash: 2b937f147eebecd8a2aac7e2a70de1af4aa20c4f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889120"
---
# <span data-ttu-id="019e9-101">Enable-AzSynapseSqlAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="019e9-101">Enable-AzSynapseSqlAdvancedDataSecurity</span></span>

## <span data-ttu-id="019e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="019e9-102">SYNOPSIS</span></span>
<span data-ttu-id="019e9-103">Habilita a Segurança Avançada de Dados em um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="019e9-103">Enables Advanced Data Security on a workspace.</span></span>

## <span data-ttu-id="019e9-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="019e9-104">SYNTAX</span></span>

### <span data-ttu-id="019e9-105">EnableByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="019e9-105">EnableByNameParameterSet (Default)</span></span>
```
Enable-AzSynapseSqlAdvancedDataSecurity [-ResourceGroupName <String>] -WorkspaceName <String>
 [-DoNotConfigureVulnerabilityAssessment] [-DeploymentName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="019e9-106">EnableByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="019e9-106">EnableByInputObjectParameterSet</span></span>
```
Enable-AzSynapseSqlAdvancedDataSecurity -InputObject <PSSynapseWorkspace>
 [-DoNotConfigureVulnerabilityAssessment] [-DeploymentName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="019e9-107">EnableByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="019e9-107">EnableByResourceIdParameterSet</span></span>
```
Enable-AzSynapseSqlAdvancedDataSecurity -ResourceId <String> [-DoNotConfigureVulnerabilityAssessment]
 [-DeploymentName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="019e9-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="019e9-108">DESCRIPTION</span></span>
<span data-ttu-id="019e9-109">O cmdlet **Enable-AzSynapseSqlAdvancedDataSecurity** habilita a Segurança Avançada de Dados em um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="019e9-109">The **Enable-AzSynapseSqlAdvancedDataSecurity** cmdlet enables Advanced Data Security on a workspace.</span></span> <span data-ttu-id="019e9-110">A Segurança Avançada de Dados é um pacote de segurança unificado que inclui Classificação de Dados, Avaliação de Vulnerabilidade e Proteção Avançada contra Ameaças para seu espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="019e9-110">Advanced Data Security is a unified security package that includes Data Classification, Vulnerability Assessment and Advanced Threat Protection for your workspace.</span></span> <span data-ttu-id="019e9-111">(Uma nova conta de armazenamento será criada automaticamente para salvar avaliações de vulnerabilidade.</span><span class="sxs-lookup"><span data-stu-id="019e9-111">(A new storage account will automatically be created for saving vulnerability assessments.</span></span> <span data-ttu-id="019e9-112">Se uma conta de armazenamento tiver sido criada anteriormente para essa finalidade, ela será usada em vez disso)</span><span class="sxs-lookup"><span data-stu-id="019e9-112">If a storage account was previously created for this purpose, it will be used instead)</span></span>

## <span data-ttu-id="019e9-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="019e9-113">EXAMPLES</span></span>

### <span data-ttu-id="019e9-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="019e9-114">Example 1</span></span>
```powershell
PS C:\> Enable-AzSynapseSqlAdvancedDataSecurity -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="019e9-115">Este comando habilita o espaço de trabalho Segurança Avançada de Dados.</span><span class="sxs-lookup"><span data-stu-id="019e9-115">This command enables workspace Advanced Data Security.</span></span>

### <span data-ttu-id="019e9-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="019e9-116">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace | Enable-AzSynapseSqlAdvancedDataSecurity
```

<span data-ttu-id="019e9-117">Este comando habilita o espaço de trabalho Segurança Avançada de Dados por meio do pipeline.</span><span class="sxs-lookup"><span data-stu-id="019e9-117">This command enables workspace Advanced Data Security through pipeline.</span></span>

### <span data-ttu-id="019e9-118">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="019e9-118">Example 3</span></span>
```powershell
PS C:\> Enable-AzSynapseSqlAdvancedDataSecurity -WorkspaceName ContosoWorkspace -DoNotConfigureVulnerabilityAssessment
```

<span data-ttu-id="019e9-119">Esse comando habilita o espaço de trabalho Segurança Avançada de Dados por meio do pipeline e não habilita automaticamente a Avaliação de Vulnerabilidade.</span><span class="sxs-lookup"><span data-stu-id="019e9-119">This command enables workspace Advanced Data Security through pipeline and does not auto enable Vulnerability Assessment.</span></span>

## <span data-ttu-id="019e9-120">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="019e9-120">PARAMETERS</span></span>

### <span data-ttu-id="019e9-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="019e9-121">-AsJob</span></span>
<span data-ttu-id="019e9-122">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="019e9-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="019e9-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="019e9-123">-DefaultProfile</span></span>
<span data-ttu-id="019e9-124">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="019e9-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="019e9-125">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="019e9-125">-DeploymentName</span></span>
<span data-ttu-id="019e9-126">Fornecer um nome personalizado para implantação avançada de Segurança de Dados.</span><span class="sxs-lookup"><span data-stu-id="019e9-126">Supply a custom name for Advanced Data Security deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="019e9-127">-DoNotConfigureVulnerabilityAssessment</span><span class="sxs-lookup"><span data-stu-id="019e9-127">-DoNotConfigureVulnerabilityAssessment</span></span>
<span data-ttu-id="019e9-128">Não habilitar automaticamente a Avaliação de Vulnerabilidade (Isso não criará uma conta de armazenamento).</span><span class="sxs-lookup"><span data-stu-id="019e9-128">Do not auto enable Vulnerability Assessment (This will not create a storage account).</span></span>

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

### <span data-ttu-id="019e9-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="019e9-129">-InputObject</span></span>
<span data-ttu-id="019e9-130">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="019e9-130">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: EnableByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="019e9-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="019e9-131">-ResourceGroupName</span></span>
<span data-ttu-id="019e9-132">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="019e9-132">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="019e9-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="019e9-133">-ResourceId</span></span>
<span data-ttu-id="019e9-134">Identificador de recursos do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="019e9-134">Resource identifier of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="019e9-135">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="019e9-135">-WorkspaceName</span></span>
<span data-ttu-id="019e9-136">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="019e9-136">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="019e9-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="019e9-137">-Confirm</span></span>
<span data-ttu-id="019e9-138">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="019e9-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="019e9-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="019e9-139">-WhatIf</span></span>
<span data-ttu-id="019e9-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="019e9-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="019e9-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="019e9-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="019e9-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="019e9-142">CommonParameters</span></span>
<span data-ttu-id="019e9-143">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="019e9-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="019e9-144">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="019e9-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="019e9-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="019e9-145">INPUTS</span></span>

### <span data-ttu-id="019e9-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="019e9-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="019e9-147">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="019e9-147">OUTPUTS</span></span>

### <span data-ttu-id="019e9-148">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="019e9-148">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="019e9-149">NOTES</span><span class="sxs-lookup"><span data-stu-id="019e9-149">NOTES</span></span>

## <span data-ttu-id="019e9-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="019e9-150">RELATED LINKS</span></span>
