---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/reset-azsynapsesqlauditsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlAuditSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlAuditSetting.md
ms.openlocfilehash: b25ca2a026cf5d82aa25f69868ca8605fd75bced
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118883"
---
# <span data-ttu-id="1f773-101">Reset-AzSynapseSqlAuditSetting</span><span class="sxs-lookup"><span data-stu-id="1f773-101">Reset-AzSynapseSqlAuditSetting</span></span>

## <span data-ttu-id="1f773-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1f773-102">SYNOPSIS</span></span>
<span data-ttu-id="1f773-103">Remove as configurações de auditoria de um Espaço de Trabalho do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="1f773-103">Removes the auditing settings of an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="1f773-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1f773-104">SYNTAX</span></span>

### <span data-ttu-id="1f773-105">RemoveByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="1f773-105">RemoveByNameParameterSet (Default)</span></span>
```
Reset-AzSynapseSqlAuditSetting [-ResourceGroupName <String>] -WorkspaceName <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f773-106">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f773-106">RemoveByInputObjectParameterSet</span></span>
```
Reset-AzSynapseSqlAuditSetting -InputObject <PSSynapseWorkspace> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f773-107">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f773-107">RemoveByResourceIdParameterSet</span></span>
```
Reset-AzSynapseSqlAuditSetting -ResourceId <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f773-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="1f773-108">DESCRIPTION</span></span>
<span data-ttu-id="1f773-109">O cmdlet **Reset-AzSynapseSqlAuditSetting** remove as configurações de auditoria de um Espaço de Trabalho de Análise do Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="1f773-109">The **Reset-AzSynapseSqlAuditSetting** cmdlet removes the auditing settings of an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="1f773-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1f773-110">EXAMPLES</span></span>

### <span data-ttu-id="1f773-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1f773-111">Example 1</span></span>
```powershell
PS C:\> Reset-AzSynapseSqlAuditSetting -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="1f773-112">Esse comando remove as configurações de auditoria de um Espaço de Trabalho do Azure Synapse Analytics chamado ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="1f773-112">This command removes the auditing settings of an Azure Synapse Analytics Workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="1f773-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="1f773-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace | Reset-AzSynapseSqlAuditSetting
```

<span data-ttu-id="1f773-114">Esse comando remove as configurações de auditoria de um Espaço de Trabalho do Azure Synapse Analytics chamado ContosoWorkspace por meio de pipeline.</span><span class="sxs-lookup"><span data-stu-id="1f773-114">This command removes the auditing settings of an Azure Synapse Analytics Workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="1f773-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1f773-115">PARAMETERS</span></span>

### <span data-ttu-id="1f773-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1f773-116">-AsJob</span></span>
<span data-ttu-id="1f773-117">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="1f773-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1f773-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f773-118">-DefaultProfile</span></span>
<span data-ttu-id="1f773-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1f773-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f773-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1f773-120">-InputObject</span></span>
<span data-ttu-id="1f773-121">objeto de entrada de espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="1f773-121">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1f773-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1f773-122">-PassThru</span></span>
<span data-ttu-id="1f773-123">Este Cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="1f773-123">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="1f773-124">Se essa opção for especificada, ela retornará verdadeira se for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="1f773-124">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="1f773-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f773-125">-ResourceGroupName</span></span>
<span data-ttu-id="1f773-126">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1f773-126">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f773-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1f773-127">-ResourceId</span></span>
<span data-ttu-id="1f773-128">Identificador de recurso do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="1f773-128">Resource identifier of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f773-129">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="1f773-129">-WorkspaceName</span></span>
<span data-ttu-id="1f773-130">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="1f773-130">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f773-131">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="1f773-131">-Confirm</span></span>
<span data-ttu-id="1f773-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f773-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f773-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f773-133">-WhatIf</span></span>
<span data-ttu-id="1f773-134">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="1f773-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f773-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1f773-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f773-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f773-136">CommonParameters</span></span>
<span data-ttu-id="1f773-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f773-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f773-138">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1f773-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f773-139">Entradas</span><span class="sxs-lookup"><span data-stu-id="1f773-139">INPUTS</span></span>

### <span data-ttu-id="1f773-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="1f773-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="1f773-141">Saídas</span><span class="sxs-lookup"><span data-stu-id="1f773-141">OUTPUTS</span></span>

### <span data-ttu-id="1f773-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1f773-142">System.Boolean</span></span>

## <span data-ttu-id="1f773-143">Notas</span><span class="sxs-lookup"><span data-stu-id="1f773-143">NOTES</span></span>

## <span data-ttu-id="1f773-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1f773-144">RELATED LINKS</span></span>
