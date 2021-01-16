---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/reset-azsynapsesqlpoolauditsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlPoolAuditSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlPoolAuditSetting.md
ms.openlocfilehash: 77299e9424f0a194776b1114146b76ef2be3329f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98257566"
---
# <span data-ttu-id="cdd62-101">Reset-AzSynapseSqlPoolAuditSetting</span><span class="sxs-lookup"><span data-stu-id="cdd62-101">Reset-AzSynapseSqlPoolAuditSetting</span></span>

## <span data-ttu-id="cdd62-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cdd62-102">SYNOPSIS</span></span>
<span data-ttu-id="cdd62-103">Remove as configurações de auditoria de um pool SQL do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="cdd62-103">Removes the auditing settings of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="cdd62-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cdd62-104">SYNTAX</span></span>

### <span data-ttu-id="cdd62-105">RemoveByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="cdd62-105">RemoveByNameParameterSet (Default)</span></span>
```
Reset-AzSynapseSqlPoolAuditSetting [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cdd62-106">RemoveByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cdd62-106">RemoveByParentObjectParameterSet</span></span>
```
Reset-AzSynapseSqlPoolAuditSetting -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cdd62-107">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cdd62-107">RemoveByInputObjectParameterSet</span></span>
```
Reset-AzSynapseSqlPoolAuditSetting -InputObject <PSSynapseSqlPool> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cdd62-108">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cdd62-108">RemoveByResourceIdParameterSet</span></span>
```
Reset-AzSynapseSqlPoolAuditSetting -ResourceId <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cdd62-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cdd62-109">DESCRIPTION</span></span>
<span data-ttu-id="cdd62-110">O cmdlet **Reset-AzSynapseSqlPoolAuditSetting** remove as configurações de auditoria de um pool SQL do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="cdd62-110">The **Reset-AzSynapseSqlPoolAuditSetting** cmdlet removes the auditing settings of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="cdd62-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cdd62-111">EXAMPLES</span></span>

### <span data-ttu-id="cdd62-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="cdd62-112">Example 1</span></span>
```powershell
PS C:\> Reset-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="cdd62-113">Esse comando remove as configurações de auditoria de um pool SQL chamado ContosoSqlPool na ContosoWorkspace do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="cdd62-113">This command removes the auditing settings of a SQL pool called ContosoSqlPool in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="cdd62-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="cdd62-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Reset-AzSynapseSqlPoolAuditSetting
```

<span data-ttu-id="cdd62-115">Esse comando remove as configurações de auditoria de um pool SQL chamado ContosoSqlPool no espaço de trabalho ContosoWorkspace pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="cdd62-115">This command removes the auditing settings of a SQL pool called ContosoSqlPool in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="cdd62-116">OS</span><span class="sxs-lookup"><span data-stu-id="cdd62-116">PARAMETERS</span></span>

### <span data-ttu-id="cdd62-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cdd62-117">-AsJob</span></span>
<span data-ttu-id="cdd62-118">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="cdd62-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cdd62-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdd62-119">-DefaultProfile</span></span>
<span data-ttu-id="cdd62-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cdd62-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cdd62-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cdd62-121">-InputObject</span></span>
<span data-ttu-id="cdd62-122">Objeto de entrada de pool SQL, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="cdd62-122">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cdd62-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="cdd62-123">-Name</span></span>
<span data-ttu-id="cdd62-124">Nome do pool do SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="cdd62-124">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet, RemoveByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdd62-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cdd62-125">-PassThru</span></span>
<span data-ttu-id="cdd62-126">Esse cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="cdd62-126">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="cdd62-127">Se essa opção for especificada, retornará true se for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="cdd62-127">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="cdd62-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cdd62-128">-ResourceGroupName</span></span>
<span data-ttu-id="cdd62-129">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="cdd62-129">Resource group name.</span></span>

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

### <span data-ttu-id="cdd62-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cdd62-130">-ResourceId</span></span>
<span data-ttu-id="cdd62-131">Identificador de recurso do pool do SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="cdd62-131">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="cdd62-132">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="cdd62-132">-WorkspaceName</span></span>
<span data-ttu-id="cdd62-133">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="cdd62-133">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="cdd62-134">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="cdd62-134">-WorkspaceObject</span></span>
<span data-ttu-id="cdd62-135">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="cdd62-135">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RemoveByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cdd62-136">-Confirme</span><span class="sxs-lookup"><span data-stu-id="cdd62-136">-Confirm</span></span>
<span data-ttu-id="cdd62-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cdd62-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cdd62-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cdd62-138">-WhatIf</span></span>
<span data-ttu-id="cdd62-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cdd62-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cdd62-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cdd62-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cdd62-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdd62-141">CommonParameters</span></span>
<span data-ttu-id="cdd62-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cdd62-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdd62-143">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cdd62-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdd62-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cdd62-144">INPUTS</span></span>

### <span data-ttu-id="cdd62-145">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="cdd62-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="cdd62-146">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="cdd62-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="cdd62-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cdd62-147">OUTPUTS</span></span>

### <span data-ttu-id="cdd62-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cdd62-148">System.Boolean</span></span>

## <span data-ttu-id="cdd62-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cdd62-149">NOTES</span></span>

## <span data-ttu-id="cdd62-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cdd62-150">RELATED LINKS</span></span>
