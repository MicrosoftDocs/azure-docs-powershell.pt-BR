---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/disable-azsynapsesqladvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Disable-AzSynapseSqlAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Disable-AzSynapseSqlAdvancedDataSecurity.md
ms.openlocfilehash: 58b2aa2f62de5cc47a9319c9cf36b0d2c8d55975
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886528"
---
# <span data-ttu-id="0d6b7-101">Disable-AzSynapseSqlAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="0d6b7-101">Disable-AzSynapseSqlAdvancedDataSecurity</span></span>

## <span data-ttu-id="0d6b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d6b7-102">SYNOPSIS</span></span>
<span data-ttu-id="0d6b7-103">Desabilita a Segurança Avançada de Dados em um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="0d6b7-103">Disables Advanced Data Security on a workspace.</span></span>

## <span data-ttu-id="0d6b7-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="0d6b7-104">SYNTAX</span></span>

### <span data-ttu-id="0d6b7-105">DisableByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="0d6b7-105">DisableByNameParameterSet (Default)</span></span>
```
Disable-AzSynapseSqlAdvancedDataSecurity [-ResourceGroupName <String>] -WorkspaceName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d6b7-106">DisableByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d6b7-106">DisableByInputObjectParameterSet</span></span>
```
Disable-AzSynapseSqlAdvancedDataSecurity -InputObject <PSSynapseWorkspace> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d6b7-107">DisableByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d6b7-107">DisableByResourceIdParameterSet</span></span>
```
Disable-AzSynapseSqlAdvancedDataSecurity -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d6b7-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="0d6b7-108">DESCRIPTION</span></span>
<span data-ttu-id="0d6b7-109">O cmdlet **Disable-AzSynapseSqlAdvancedDataSecurity** desabilita a Segurança Avançada de Dados em um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="0d6b7-109">The **Disable-AzSynapseSqlAdvancedDataSecurity** cmdlet disables Advanced Data Security on a workspace.</span></span>

## <span data-ttu-id="0d6b7-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0d6b7-110">EXAMPLES</span></span>

### <span data-ttu-id="0d6b7-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0d6b7-111">Example 1</span></span>
```powershell
PS C:\> Disable-AzSynapseSqlAdvancedDataSecurity -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="0d6b7-112">Este comando desabilita a Segurança Avançada de Dados no espaço de trabalho chamado ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="0d6b7-112">This command disables Advanced Data Security on the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="0d6b7-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0d6b7-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace | Disable-AzSynapseSqlAdvancedDataSecurity
```

<span data-ttu-id="0d6b7-114">Este comando desabilita a Segurança Avançada de Dados no espaço de trabalho chamado ContosoWorkspace por meio de pipeline.</span><span class="sxs-lookup"><span data-stu-id="0d6b7-114">This command disables Advanced Data Security on the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="0d6b7-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="0d6b7-115">PARAMETERS</span></span>

### <span data-ttu-id="0d6b7-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0d6b7-116">-AsJob</span></span>
<span data-ttu-id="0d6b7-117">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="0d6b7-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0d6b7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d6b7-118">-DefaultProfile</span></span>
<span data-ttu-id="0d6b7-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0d6b7-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d6b7-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0d6b7-120">-InputObject</span></span>
<span data-ttu-id="0d6b7-121">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="0d6b7-121">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: DisableByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0d6b7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d6b7-122">-ResourceGroupName</span></span>
<span data-ttu-id="0d6b7-123">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0d6b7-123">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DisableByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d6b7-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0d6b7-124">-ResourceId</span></span>
<span data-ttu-id="0d6b7-125">Identificador de recursos do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="0d6b7-125">Resource identifier of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: DisableByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d6b7-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="0d6b7-126">-WorkspaceName</span></span>
<span data-ttu-id="0d6b7-127">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="0d6b7-127">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: DisableByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d6b7-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0d6b7-128">-Confirm</span></span>
<span data-ttu-id="0d6b7-129">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0d6b7-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d6b7-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d6b7-130">-WhatIf</span></span>
<span data-ttu-id="0d6b7-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0d6b7-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d6b7-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0d6b7-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d6b7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d6b7-133">CommonParameters</span></span>
<span data-ttu-id="0d6b7-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d6b7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d6b7-135">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0d6b7-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d6b7-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0d6b7-136">INPUTS</span></span>

### <span data-ttu-id="0d6b7-137">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="0d6b7-137">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="0d6b7-138">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="0d6b7-138">OUTPUTS</span></span>

### <span data-ttu-id="0d6b7-139">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="0d6b7-139">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="0d6b7-140">NOTES</span><span class="sxs-lookup"><span data-stu-id="0d6b7-140">NOTES</span></span>

## <span data-ttu-id="0d6b7-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0d6b7-141">RELATED LINKS</span></span>
