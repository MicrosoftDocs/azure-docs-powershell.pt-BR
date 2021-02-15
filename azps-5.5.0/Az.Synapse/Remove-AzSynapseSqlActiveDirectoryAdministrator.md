---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsesqlactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlActiveDirectoryAdministrator.md
ms.openlocfilehash: 21d7169f18a999f84adbc568da18c90cb2aa2424
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112394"
---
# <span data-ttu-id="442f4-101">Remove-AzSynapseSqlActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="442f4-101">Remove-AzSynapseSqlActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="442f4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="442f4-102">SYNOPSIS</span></span>
<span data-ttu-id="442f4-103">Remove um administrador do Azure AD para o Espaço de Trabalho do Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="442f4-103">Removes an Azure AD administrator for Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="442f4-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="442f4-104">SYNTAX</span></span>

### <span data-ttu-id="442f4-105">RemoveByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="442f4-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlActiveDirectoryAdministrator [-ResourceGroupName <String>] -WorkspaceName <String>
 [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="442f4-106">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="442f4-106">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSqlActiveDirectoryAdministrator -InputObject <PSSynapseWorkspace> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="442f4-107">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="442f4-107">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSqlActiveDirectoryAdministrator -ResourceId <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="442f4-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="442f4-108">DESCRIPTION</span></span>
<span data-ttu-id="442f4-109">O cmdlet **Remove-AzSynapseSqlActiveDirectoryAdministrator** remove um administrador do Azure Active Directory (Azure AD) para o Espaço de Trabalho de Análise do Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="442f4-109">The **Remove-AzSynapseSqlActiveDirectoryAdministrator** cmdlet removes an Azure Active Directory (Azure AD) administrator for Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="442f4-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="442f4-110">EXAMPLES</span></span>

### <span data-ttu-id="442f4-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="442f4-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlActiveDirectoryAdministrator -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="442f4-112">Esse comando remove o administrador do Azure AD para o espaço de trabalho chamado ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="442f4-112">This command removes the Azure AD administrator for the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="442f4-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="442f4-113">PARAMETERS</span></span>

### <span data-ttu-id="442f4-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="442f4-114">-AsJob</span></span>
<span data-ttu-id="442f4-115">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="442f4-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="442f4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="442f4-116">-DefaultProfile</span></span>
<span data-ttu-id="442f4-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="442f4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="442f4-118">-Forçar</span><span class="sxs-lookup"><span data-stu-id="442f4-118">-Force</span></span>
<span data-ttu-id="442f4-119">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="442f4-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="442f4-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="442f4-120">-InputObject</span></span>
<span data-ttu-id="442f4-121">objeto de entrada de espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="442f4-121">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="442f4-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="442f4-122">-PassThru</span></span>
<span data-ttu-id="442f4-123">Este Cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="442f4-123">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="442f4-124">Se essa opção for especificada, ela retornará verdadeira se for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="442f4-124">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="442f4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="442f4-125">-ResourceGroupName</span></span>
<span data-ttu-id="442f4-126">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="442f4-126">Resource group name.</span></span>

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

### <span data-ttu-id="442f4-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="442f4-127">-ResourceId</span></span>
<span data-ttu-id="442f4-128">Identificador de recurso do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="442f4-128">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="442f4-129">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="442f4-129">-WorkspaceName</span></span>
<span data-ttu-id="442f4-130">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="442f4-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="442f4-131">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="442f4-131">-Confirm</span></span>
<span data-ttu-id="442f4-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="442f4-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="442f4-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="442f4-133">-WhatIf</span></span>
<span data-ttu-id="442f4-134">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="442f4-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="442f4-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="442f4-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="442f4-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="442f4-136">CommonParameters</span></span>
<span data-ttu-id="442f4-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="442f4-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="442f4-138">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="442f4-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="442f4-139">Entradas</span><span class="sxs-lookup"><span data-stu-id="442f4-139">INPUTS</span></span>

### <span data-ttu-id="442f4-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="442f4-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="442f4-141">Saídas</span><span class="sxs-lookup"><span data-stu-id="442f4-141">OUTPUTS</span></span>

### <span data-ttu-id="442f4-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="442f4-142">System.Boolean</span></span>

## <span data-ttu-id="442f4-143">Notas</span><span class="sxs-lookup"><span data-stu-id="442f4-143">NOTES</span></span>

## <span data-ttu-id="442f4-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="442f4-144">RELATED LINKS</span></span>
