---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/reset-azsynapsesqladvancedthreatprotectionsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 420b95d8d20d21758e4f42db6c31e2d1ead557ac
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118885"
---
# <span data-ttu-id="787c8-101">Reset-AzSynapseSqlAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="787c8-101">Reset-AzSynapseSqlAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="787c8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="787c8-102">SYNOPSIS</span></span>
<span data-ttu-id="787c8-103">Remove as configurações avançadas de proteção contra ameaças de um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="787c8-103">Removes the advanced threat protection settings from a workspace.</span></span>

## <span data-ttu-id="787c8-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="787c8-104">SYNTAX</span></span>

### <span data-ttu-id="787c8-105">ClearByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="787c8-105">ClearByNameParameterSet (Default)</span></span>
```
Reset-AzSynapseSqlAdvancedThreatProtectionSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="787c8-106">ClearByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="787c8-106">ClearByInputObjectParameterSet</span></span>
```
Reset-AzSynapseSqlAdvancedThreatProtectionSetting -InputObject <PSSynapseWorkspace> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="787c8-107">ClearByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="787c8-107">ClearByResourceIdParameterSet</span></span>
```
Reset-AzSynapseSqlAdvancedThreatProtectionSetting -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="787c8-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="787c8-108">DESCRIPTION</span></span>
<span data-ttu-id="787c8-109">O cmdlet **Reset-AzSynapseSqlAdvancedThreatProtectionSetting** remove as configurações avançadas de proteção contra ameaças de um Espaço de Trabalho de Análise do Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="787c8-109">The **Reset-AzSynapseSqlAdvancedThreatProtectionSetting** cmdlet removes the advanced threat protection settings from an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="787c8-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="787c8-110">EXAMPLES</span></span>

### <span data-ttu-id="787c8-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="787c8-111">Example 1</span></span>
```powershell
PS C:\> Reset-AzSynapseSqlAdvancedThreatProtectionSetting -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="787c8-112">Esse comando remove as configurações avançadas de proteção contra ameaças de um espaço de trabalho chamado ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="787c8-112">This command removes the advanced threat protection settings from a workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="787c8-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="787c8-113">PARAMETERS</span></span>

### <span data-ttu-id="787c8-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="787c8-114">-AsJob</span></span>
<span data-ttu-id="787c8-115">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="787c8-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="787c8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="787c8-116">-DefaultProfile</span></span>
<span data-ttu-id="787c8-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="787c8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="787c8-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="787c8-118">-InputObject</span></span>
<span data-ttu-id="787c8-119">objeto de entrada de espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="787c8-119">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: ClearByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="787c8-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="787c8-120">-PassThru</span></span>
<span data-ttu-id="787c8-121">Este Cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="787c8-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="787c8-122">Se essa opção for especificada, ela retornará verdadeira se for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="787c8-122">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="787c8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="787c8-123">-ResourceGroupName</span></span>
<span data-ttu-id="787c8-124">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="787c8-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ClearByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="787c8-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="787c8-125">-ResourceId</span></span>
<span data-ttu-id="787c8-126">Identificador de recurso do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="787c8-126">Resource identifier of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: ClearByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="787c8-127">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="787c8-127">-WorkspaceName</span></span>
<span data-ttu-id="787c8-128">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="787c8-128">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: ClearByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="787c8-129">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="787c8-129">-Confirm</span></span>
<span data-ttu-id="787c8-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="787c8-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="787c8-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="787c8-131">-WhatIf</span></span>
<span data-ttu-id="787c8-132">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="787c8-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="787c8-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="787c8-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="787c8-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="787c8-134">CommonParameters</span></span>
<span data-ttu-id="787c8-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="787c8-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="787c8-136">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="787c8-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="787c8-137">Entradas</span><span class="sxs-lookup"><span data-stu-id="787c8-137">INPUTS</span></span>

### <span data-ttu-id="787c8-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="787c8-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="787c8-139">Saídas</span><span class="sxs-lookup"><span data-stu-id="787c8-139">OUTPUTS</span></span>

### <span data-ttu-id="787c8-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="787c8-140">System.Boolean</span></span>

## <span data-ttu-id="787c8-141">Notas</span><span class="sxs-lookup"><span data-stu-id="787c8-141">NOTES</span></span>

## <span data-ttu-id="787c8-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="787c8-142">RELATED LINKS</span></span>
