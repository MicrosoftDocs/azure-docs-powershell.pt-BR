---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsesqlactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlActiveDirectoryAdministrator.md
ms.openlocfilehash: 21d7169f18a999f84adbc568da18c90cb2aa2424
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98272350"
---
# <span data-ttu-id="69df7-101">Remove-AzSynapseSqlActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="69df7-101">Remove-AzSynapseSqlActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="69df7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="69df7-102">SYNOPSIS</span></span>
<span data-ttu-id="69df7-103">Remove um administrador do Azure AD para Synapse de espaço de trabalho analítico.</span><span class="sxs-lookup"><span data-stu-id="69df7-103">Removes an Azure AD administrator for Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="69df7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="69df7-104">SYNTAX</span></span>

### <span data-ttu-id="69df7-105">RemoveByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="69df7-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlActiveDirectoryAdministrator [-ResourceGroupName <String>] -WorkspaceName <String>
 [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="69df7-106">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="69df7-106">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSqlActiveDirectoryAdministrator -InputObject <PSSynapseWorkspace> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69df7-107">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="69df7-107">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSqlActiveDirectoryAdministrator -ResourceId <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69df7-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="69df7-108">DESCRIPTION</span></span>
<span data-ttu-id="69df7-109">O cmdlet **Remove-AzSynapseSqlActiveDirectoryAdministrator** remove um administrador do Azure Active Directory (Azure AD) para o Azure Synapse espaço de trabalho de análise.</span><span class="sxs-lookup"><span data-stu-id="69df7-109">The **Remove-AzSynapseSqlActiveDirectoryAdministrator** cmdlet removes an Azure Active Directory (Azure AD) administrator for Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="69df7-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="69df7-110">EXAMPLES</span></span>

### <span data-ttu-id="69df7-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="69df7-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlActiveDirectoryAdministrator -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="69df7-112">Esse comando Remove o administrador do Azure AD para o espaço de trabalho chamado ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="69df7-112">This command removes the Azure AD administrator for the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="69df7-113">OS</span><span class="sxs-lookup"><span data-stu-id="69df7-113">PARAMETERS</span></span>

### <span data-ttu-id="69df7-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="69df7-114">-AsJob</span></span>
<span data-ttu-id="69df7-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="69df7-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="69df7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69df7-116">-DefaultProfile</span></span>
<span data-ttu-id="69df7-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="69df7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69df7-118">-Force</span><span class="sxs-lookup"><span data-stu-id="69df7-118">-Force</span></span>
<span data-ttu-id="69df7-119">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="69df7-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="69df7-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="69df7-120">-InputObject</span></span>
<span data-ttu-id="69df7-121">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="69df7-121">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="69df7-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="69df7-122">-PassThru</span></span>
<span data-ttu-id="69df7-123">Esse cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="69df7-123">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="69df7-124">Se essa opção for especificada, retornará true se for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="69df7-124">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="69df7-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69df7-125">-ResourceGroupName</span></span>
<span data-ttu-id="69df7-126">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="69df7-126">Resource group name.</span></span>

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

### <span data-ttu-id="69df7-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="69df7-127">-ResourceId</span></span>
<span data-ttu-id="69df7-128">Identificador de recurso do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="69df7-128">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="69df7-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="69df7-129">-WorkspaceName</span></span>
<span data-ttu-id="69df7-130">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="69df7-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="69df7-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="69df7-131">-Confirm</span></span>
<span data-ttu-id="69df7-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69df7-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69df7-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69df7-133">-WhatIf</span></span>
<span data-ttu-id="69df7-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="69df7-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69df7-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="69df7-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69df7-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69df7-136">CommonParameters</span></span>
<span data-ttu-id="69df7-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69df7-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69df7-138">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="69df7-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69df7-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="69df7-139">INPUTS</span></span>

### <span data-ttu-id="69df7-140">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="69df7-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="69df7-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="69df7-141">OUTPUTS</span></span>

### <span data-ttu-id="69df7-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="69df7-142">System.Boolean</span></span>

## <span data-ttu-id="69df7-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="69df7-143">NOTES</span></span>

## <span data-ttu-id="69df7-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="69df7-144">RELATED LINKS</span></span>
