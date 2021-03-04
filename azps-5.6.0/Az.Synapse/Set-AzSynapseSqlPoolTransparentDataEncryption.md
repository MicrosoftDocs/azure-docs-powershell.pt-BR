---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/set-azsynapsesqlpooltransparentdataencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlPoolTransparentDataEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlPoolTransparentDataEncryption.md
ms.openlocfilehash: cdc72a2bb0e21873bd0fa2d82123afe8ed011378
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890535"
---
# <span data-ttu-id="015e3-101">Set-AzSynapseSqlPoolTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="015e3-101">Set-AzSynapseSqlPoolTransparentDataEncryption</span></span>

## <span data-ttu-id="015e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="015e3-102">SYNOPSIS</span></span>
<span data-ttu-id="015e3-103">Modifica a propriedade TDE para um SQL pool.</span><span class="sxs-lookup"><span data-stu-id="015e3-103">Modifies TDE property for a SQL pool.</span></span>

## <span data-ttu-id="015e3-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="015e3-104">SYNTAX</span></span>

### <span data-ttu-id="015e3-105">SetByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="015e3-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzSynapseSqlPoolTransparentDataEncryption [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> -State <TransparentDataEncryptionStateType> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="015e3-106">SetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="015e3-106">SetByParentObjectParameterSet</span></span>
```
Set-AzSynapseSqlPoolTransparentDataEncryption -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 -State <TransparentDataEncryptionStateType> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="015e3-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="015e3-107">SetByInputObjectParameterSet</span></span>
```
Set-AzSynapseSqlPoolTransparentDataEncryption -InputObject <PSSynapseSqlPool>
 -State <TransparentDataEncryptionStateType> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="015e3-108">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="015e3-108">SetByResourceIdParameterSet</span></span>
```
Set-AzSynapseSqlPoolTransparentDataEncryption -ResourceId <String> -State <TransparentDataEncryptionStateType>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="015e3-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="015e3-109">DESCRIPTION</span></span>
<span data-ttu-id="015e3-110">O cmdlet **Set-AzSynapseSqlPoolTransparentDataEncryption** modifica a propriedade TDE (Transparent Data Encryption) de um pool do Azure Synapse Analytics SQL.</span><span class="sxs-lookup"><span data-stu-id="015e3-110">The **Set-AzSynapseSqlPoolTransparentDataEncryption** cmdlet modifies the Transparent Data Encryption (TDE) property of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="015e3-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="015e3-111">EXAMPLES</span></span>

### <span data-ttu-id="015e3-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="015e3-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseSqlPoolTransparentDataEncryption -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -State Enabled
```

<span data-ttu-id="015e3-113">Este comando habilita o TDE para o pool SQL chamado ContosoSqlPool no espaço de trabalho chamado ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="015e3-113">This command enables TDE for the SQL pool named ContosoSqlPool under the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="015e3-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="015e3-114">PARAMETERS</span></span>

### <span data-ttu-id="015e3-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="015e3-115">-AsJob</span></span>
<span data-ttu-id="015e3-116">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="015e3-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="015e3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="015e3-117">-DefaultProfile</span></span>
<span data-ttu-id="015e3-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="015e3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="015e3-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="015e3-119">-InputObject</span></span>
<span data-ttu-id="015e3-120">SQL objeto de entrada do pool, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="015e3-120">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="015e3-121">-Name</span><span class="sxs-lookup"><span data-stu-id="015e3-121">-Name</span></span>
<span data-ttu-id="015e3-122">Nome do pool SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="015e3-122">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet, SetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="015e3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="015e3-123">-ResourceGroupName</span></span>
<span data-ttu-id="015e3-124">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="015e3-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="015e3-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="015e3-125">-ResourceId</span></span>
<span data-ttu-id="015e3-126">Identificador de recursos do Pool SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="015e3-126">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="015e3-127">-State</span><span class="sxs-lookup"><span data-stu-id="015e3-127">-State</span></span>
<span data-ttu-id="015e3-128">O estado de Criptografia de Dados Transparente do Sql Pool do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="015e3-128">The Azure Synapse Analytics Sql Pool Transparent Data Encryption state.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.TransparentDataEncryptionStateType
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="015e3-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="015e3-129">-WorkspaceName</span></span>
<span data-ttu-id="015e3-130">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="015e3-130">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="015e3-131">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="015e3-131">-WorkspaceObject</span></span>
<span data-ttu-id="015e3-132">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="015e3-132">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="015e3-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="015e3-133">-Confirm</span></span>
<span data-ttu-id="015e3-134">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="015e3-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="015e3-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="015e3-135">-WhatIf</span></span>
<span data-ttu-id="015e3-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="015e3-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="015e3-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="015e3-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="015e3-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="015e3-138">CommonParameters</span></span>
<span data-ttu-id="015e3-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="015e3-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="015e3-140">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="015e3-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="015e3-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="015e3-141">INPUTS</span></span>

### <span data-ttu-id="015e3-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="015e3-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="015e3-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="015e3-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="015e3-144">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="015e3-144">OUTPUTS</span></span>

### <span data-ttu-id="015e3-145">Microsoft.Azure.Commands.Synapse.Models.PSTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="015e3-145">Microsoft.Azure.Commands.Synapse.Models.PSTransparentDataEncryption</span></span>

## <span data-ttu-id="015e3-146">NOTES</span><span class="sxs-lookup"><span data-stu-id="015e3-146">NOTES</span></span>

## <span data-ttu-id="015e3-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="015e3-147">RELATED LINKS</span></span>
