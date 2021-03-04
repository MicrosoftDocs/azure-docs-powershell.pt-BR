---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/reset-azsynapsesqladvancedthreatprotectionsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 9b4e55f701b956fc653cf08cddb87997a998315e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889875"
---
# <span data-ttu-id="28e2c-101">Reset-AzSynapseSqlAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="28e2c-101">Reset-AzSynapseSqlAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="28e2c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28e2c-102">SYNOPSIS</span></span>
<span data-ttu-id="28e2c-103">Remove as configurações avançadas de proteção contra ameaças de um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="28e2c-103">Removes the advanced threat protection settings from a workspace.</span></span>

## <span data-ttu-id="28e2c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="28e2c-104">SYNTAX</span></span>

### <span data-ttu-id="28e2c-105">ClearByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="28e2c-105">ClearByNameParameterSet (Default)</span></span>
```
Reset-AzSynapseSqlAdvancedThreatProtectionSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28e2c-106">ClearByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="28e2c-106">ClearByInputObjectParameterSet</span></span>
```
Reset-AzSynapseSqlAdvancedThreatProtectionSetting -InputObject <PSSynapseWorkspace> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28e2c-107">ClearByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="28e2c-107">ClearByResourceIdParameterSet</span></span>
```
Reset-AzSynapseSqlAdvancedThreatProtectionSetting -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28e2c-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="28e2c-108">DESCRIPTION</span></span>
<span data-ttu-id="28e2c-109">O cmdlet **Reset-AzSynapseSqlAdvancedThreatProtectionSetting** remove as configurações avançadas de proteção contra ameaças de um Espaço de Trabalho de Análise do Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="28e2c-109">The **Reset-AzSynapseSqlAdvancedThreatProtectionSetting** cmdlet removes the advanced threat protection settings from an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="28e2c-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="28e2c-110">EXAMPLES</span></span>

### <span data-ttu-id="28e2c-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="28e2c-111">Example 1</span></span>
```powershell
PS C:\> Reset-AzSynapseSqlAdvancedThreatProtectionSetting -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="28e2c-112">Este comando remove as configurações avançadas de proteção contra ameaças de um espaço de trabalho chamado ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="28e2c-112">This command removes the advanced threat protection settings from a workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="28e2c-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="28e2c-113">PARAMETERS</span></span>

### <span data-ttu-id="28e2c-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="28e2c-114">-AsJob</span></span>
<span data-ttu-id="28e2c-115">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="28e2c-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="28e2c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28e2c-116">-DefaultProfile</span></span>
<span data-ttu-id="28e2c-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="28e2c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28e2c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="28e2c-118">-InputObject</span></span>
<span data-ttu-id="28e2c-119">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="28e2c-119">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="28e2c-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="28e2c-120">-PassThru</span></span>
<span data-ttu-id="28e2c-121">Este Cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="28e2c-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="28e2c-122">Se essa opção for especificada, ela retornará true se tiver êxito.</span><span class="sxs-lookup"><span data-stu-id="28e2c-122">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="28e2c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28e2c-123">-ResourceGroupName</span></span>
<span data-ttu-id="28e2c-124">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="28e2c-124">Resource group name.</span></span>

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

### <span data-ttu-id="28e2c-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="28e2c-125">-ResourceId</span></span>
<span data-ttu-id="28e2c-126">Identificador de recursos do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="28e2c-126">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="28e2c-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="28e2c-127">-WorkspaceName</span></span>
<span data-ttu-id="28e2c-128">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="28e2c-128">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="28e2c-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="28e2c-129">-Confirm</span></span>
<span data-ttu-id="28e2c-130">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="28e2c-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28e2c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28e2c-131">-WhatIf</span></span>
<span data-ttu-id="28e2c-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="28e2c-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28e2c-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="28e2c-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28e2c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28e2c-134">CommonParameters</span></span>
<span data-ttu-id="28e2c-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28e2c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28e2c-136">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="28e2c-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28e2c-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="28e2c-137">INPUTS</span></span>

### <span data-ttu-id="28e2c-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="28e2c-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="28e2c-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="28e2c-139">OUTPUTS</span></span>

### <span data-ttu-id="28e2c-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="28e2c-140">System.Boolean</span></span>

## <span data-ttu-id="28e2c-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="28e2c-141">NOTES</span></span>

## <span data-ttu-id="28e2c-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="28e2c-142">RELATED LINKS</span></span>
