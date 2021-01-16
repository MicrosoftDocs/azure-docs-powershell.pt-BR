---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/enable-azsynapsesqladvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Enable-AzSynapseSqlAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Enable-AzSynapseSqlAdvancedDataSecurity.md
ms.openlocfilehash: dea0770af8cca14ebd523f67b69d7a12931183ec
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98272454"
---
# <span data-ttu-id="dea5f-101">Enable-AzSynapseSqlAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="dea5f-101">Enable-AzSynapseSqlAdvancedDataSecurity</span></span>

## <span data-ttu-id="dea5f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dea5f-102">SYNOPSIS</span></span>
<span data-ttu-id="dea5f-103">Habilita a segurança avançada de dados em um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="dea5f-103">Enables Advanced Data Security on a workspace.</span></span>

## <span data-ttu-id="dea5f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dea5f-104">SYNTAX</span></span>

### <span data-ttu-id="dea5f-105">EnableByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="dea5f-105">EnableByNameParameterSet (Default)</span></span>
```
Enable-AzSynapseSqlAdvancedDataSecurity [-ResourceGroupName <String>] -WorkspaceName <String>
 [-DoNotConfigureVulnerabilityAssessment] [-DeploymentName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dea5f-106">EnableByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dea5f-106">EnableByInputObjectParameterSet</span></span>
```
Enable-AzSynapseSqlAdvancedDataSecurity -InputObject <PSSynapseWorkspace>
 [-DoNotConfigureVulnerabilityAssessment] [-DeploymentName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dea5f-107">EnableByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dea5f-107">EnableByResourceIdParameterSet</span></span>
```
Enable-AzSynapseSqlAdvancedDataSecurity -ResourceId <String> [-DoNotConfigureVulnerabilityAssessment]
 [-DeploymentName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dea5f-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dea5f-108">DESCRIPTION</span></span>
<span data-ttu-id="dea5f-109">O cmdlet **Enable-AzSynapseSqlAdvancedDataSecurity** permite a segurança avançada de dados em um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="dea5f-109">The **Enable-AzSynapseSqlAdvancedDataSecurity** cmdlet enables Advanced Data Security on a workspace.</span></span> <span data-ttu-id="dea5f-110">A segurança avançada de dados é um pacote de segurança unificado que inclui classificação de dados, avaliação de vulnerabilidade e proteção avançada contra ameaças para o seu espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="dea5f-110">Advanced Data Security is a unified security package that includes Data Classification, Vulnerability Assessment and Advanced Threat Protection for your workspace.</span></span> <span data-ttu-id="dea5f-111">(Uma nova conta de armazenamento será criada automaticamente para salvar avaliações de vulnerabilidade.</span><span class="sxs-lookup"><span data-stu-id="dea5f-111">(A new storage account will automatically be created for saving vulnerability assessments.</span></span> <span data-ttu-id="dea5f-112">Se uma conta de armazenamento foi criada anteriormente para essa finalidade, ela será usada em vez disso.</span><span class="sxs-lookup"><span data-stu-id="dea5f-112">If a storage account was previously created for this purpose, it will be used instead)</span></span>

## <span data-ttu-id="dea5f-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dea5f-113">EXAMPLES</span></span>

### <span data-ttu-id="dea5f-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="dea5f-114">Example 1</span></span>
```powershell
PS C:\> Enable-AzSynapseSqlAdvancedDataSecurity -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="dea5f-115">Esse comando habilita a segurança de dados avançada do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="dea5f-115">This command enables workspace Advanced Data Security.</span></span>

### <span data-ttu-id="dea5f-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="dea5f-116">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace | Enable-AzSynapseSqlAdvancedDataSecurity
```

<span data-ttu-id="dea5f-117">Esse comando habilita a segurança de dados avançada do espaço de trabalho por meio do pipeline.</span><span class="sxs-lookup"><span data-stu-id="dea5f-117">This command enables workspace Advanced Data Security through pipeline.</span></span>

### <span data-ttu-id="dea5f-118">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="dea5f-118">Example 3</span></span>
```powershell
PS C:\> Enable-AzSynapseSqlAdvancedDataSecurity -WorkspaceName ContosoWorkspace -DoNotConfigureVulnerabilityAssessment
```

<span data-ttu-id="dea5f-119">Esse comando habilita a segurança de dados avançada do espaço de trabalho por meio do pipeline e não habilita a avaliação de vulnerabilidade automaticamente.</span><span class="sxs-lookup"><span data-stu-id="dea5f-119">This command enables workspace Advanced Data Security through pipeline and does not auto enable Vulnerability Assessment.</span></span>

## <span data-ttu-id="dea5f-120">OS</span><span class="sxs-lookup"><span data-stu-id="dea5f-120">PARAMETERS</span></span>

### <span data-ttu-id="dea5f-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dea5f-121">-AsJob</span></span>
<span data-ttu-id="dea5f-122">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="dea5f-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dea5f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dea5f-123">-DefaultProfile</span></span>
<span data-ttu-id="dea5f-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dea5f-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dea5f-125">-Deploymentname</span><span class="sxs-lookup"><span data-stu-id="dea5f-125">-DeploymentName</span></span>
<span data-ttu-id="dea5f-126">Forneça um nome personalizado para a implantação avançada de segurança de dados.</span><span class="sxs-lookup"><span data-stu-id="dea5f-126">Supply a custom name for Advanced Data Security deployment.</span></span>

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

### <span data-ttu-id="dea5f-127">-DoNotConfigureVulnerabilityAssessment</span><span class="sxs-lookup"><span data-stu-id="dea5f-127">-DoNotConfigureVulnerabilityAssessment</span></span>
<span data-ttu-id="dea5f-128">Não habilite a avaliação de vulnerabilidade automaticamente (isso não criará uma conta de armazenamento).</span><span class="sxs-lookup"><span data-stu-id="dea5f-128">Do not auto enable Vulnerability Assessment (This will not create a storage account).</span></span>

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

### <span data-ttu-id="dea5f-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dea5f-129">-InputObject</span></span>
<span data-ttu-id="dea5f-130">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="dea5f-130">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="dea5f-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dea5f-131">-ResourceGroupName</span></span>
<span data-ttu-id="dea5f-132">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="dea5f-132">Resource group name.</span></span>

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

### <span data-ttu-id="dea5f-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dea5f-133">-ResourceId</span></span>
<span data-ttu-id="dea5f-134">Identificador de recurso do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="dea5f-134">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="dea5f-135">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="dea5f-135">-WorkspaceName</span></span>
<span data-ttu-id="dea5f-136">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="dea5f-136">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="dea5f-137">-Confirme</span><span class="sxs-lookup"><span data-stu-id="dea5f-137">-Confirm</span></span>
<span data-ttu-id="dea5f-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dea5f-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dea5f-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dea5f-139">-WhatIf</span></span>
<span data-ttu-id="dea5f-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="dea5f-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dea5f-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="dea5f-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dea5f-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dea5f-142">CommonParameters</span></span>
<span data-ttu-id="dea5f-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dea5f-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dea5f-144">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dea5f-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dea5f-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dea5f-145">INPUTS</span></span>

### <span data-ttu-id="dea5f-146">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="dea5f-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="dea5f-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dea5f-147">OUTPUTS</span></span>

### <span data-ttu-id="dea5f-148">Microsoft. Azure. Commands. Synapse. Models. WorkspaceAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="dea5f-148">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="dea5f-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dea5f-149">NOTES</span></span>

## <span data-ttu-id="dea5f-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dea5f-150">RELATED LINKS</span></span>
