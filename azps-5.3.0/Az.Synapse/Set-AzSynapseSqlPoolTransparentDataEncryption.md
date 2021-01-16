---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsesqlpooltransparentdataencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlPoolTransparentDataEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlPoolTransparentDataEncryption.md
ms.openlocfilehash: 5a8dbd1f21d640d5d1cb38fa403ee05dec9cfc20
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98429610"
---
# <span data-ttu-id="556e4-101">Set-AzSynapseSqlPoolTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="556e4-101">Set-AzSynapseSqlPoolTransparentDataEncryption</span></span>

## <span data-ttu-id="556e4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="556e4-102">SYNOPSIS</span></span>
<span data-ttu-id="556e4-103">Modifica a propriedade TDE de um pool SQL.</span><span class="sxs-lookup"><span data-stu-id="556e4-103">Modifies TDE property for a SQL pool.</span></span>

## <span data-ttu-id="556e4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="556e4-104">SYNTAX</span></span>

### <span data-ttu-id="556e4-105">SetByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="556e4-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzSynapseSqlPoolTransparentDataEncryption [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> -State <TransparentDataEncryptionStateType> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="556e4-106">SetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="556e4-106">SetByParentObjectParameterSet</span></span>
```
Set-AzSynapseSqlPoolTransparentDataEncryption -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 -State <TransparentDataEncryptionStateType> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="556e4-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="556e4-107">SetByInputObjectParameterSet</span></span>
```
Set-AzSynapseSqlPoolTransparentDataEncryption -InputObject <PSSynapseSqlPool>
 -State <TransparentDataEncryptionStateType> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="556e4-108">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="556e4-108">SetByResourceIdParameterSet</span></span>
```
Set-AzSynapseSqlPoolTransparentDataEncryption -ResourceId <String> -State <TransparentDataEncryptionStateType>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="556e4-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="556e4-109">DESCRIPTION</span></span>
<span data-ttu-id="556e4-110">O cmdlet **set-AzSynapseSqlPoolTransparentDataEncryption** modifica a propriedade de criptografia de dados transparente (TDE) de um pool SQL do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="556e4-110">The **Set-AzSynapseSqlPoolTransparentDataEncryption** cmdlet modifies the Transparent Data Encryption (TDE) property of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="556e4-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="556e4-111">EXAMPLES</span></span>

### <span data-ttu-id="556e4-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="556e4-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseSqlPoolTransparentDataEncryption -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -State Enabled
```

<span data-ttu-id="556e4-113">Esse comando habilita TDE para o pool SQL chamado ContosoSqlPool no espaço de trabalho chamado ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="556e4-113">This command enables TDE for the SQL pool named ContosoSqlPool under the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="556e4-114">OS</span><span class="sxs-lookup"><span data-stu-id="556e4-114">PARAMETERS</span></span>

### <span data-ttu-id="556e4-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="556e4-115">-AsJob</span></span>
<span data-ttu-id="556e4-116">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="556e4-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="556e4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="556e4-117">-DefaultProfile</span></span>
<span data-ttu-id="556e4-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="556e4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="556e4-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="556e4-119">-InputObject</span></span>
<span data-ttu-id="556e4-120">Objeto de entrada de pool SQL, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="556e4-120">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="556e4-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="556e4-121">-Name</span></span>
<span data-ttu-id="556e4-122">Nome do pool do SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="556e4-122">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="556e4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="556e4-123">-ResourceGroupName</span></span>
<span data-ttu-id="556e4-124">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="556e4-124">Resource group name.</span></span>

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

### <span data-ttu-id="556e4-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="556e4-125">-ResourceId</span></span>
<span data-ttu-id="556e4-126">Identificador de recurso do pool do SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="556e4-126">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="556e4-127">-Estado</span><span class="sxs-lookup"><span data-stu-id="556e4-127">-State</span></span>
<span data-ttu-id="556e4-128">O estado de criptografia de dados transparente do pool do SQL do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="556e4-128">The Azure Synapse Analytics Sql Pool Transparent Data Encryption state.</span></span>

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

### <span data-ttu-id="556e4-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="556e4-129">-WorkspaceName</span></span>
<span data-ttu-id="556e4-130">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="556e4-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="556e4-131">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="556e4-131">-WorkspaceObject</span></span>
<span data-ttu-id="556e4-132">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="556e4-132">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="556e4-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="556e4-133">-Confirm</span></span>
<span data-ttu-id="556e4-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="556e4-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="556e4-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="556e4-135">-WhatIf</span></span>
<span data-ttu-id="556e4-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="556e4-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="556e4-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="556e4-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="556e4-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="556e4-138">CommonParameters</span></span>
<span data-ttu-id="556e4-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="556e4-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="556e4-140">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="556e4-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="556e4-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="556e4-141">INPUTS</span></span>

### <span data-ttu-id="556e4-142">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="556e4-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="556e4-143">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="556e4-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="556e4-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="556e4-144">OUTPUTS</span></span>

### <span data-ttu-id="556e4-145">Microsoft. Azure. Commands. Synapse. Models. PSTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="556e4-145">Microsoft.Azure.Commands.Synapse.Models.PSTransparentDataEncryption</span></span>

## <span data-ttu-id="556e4-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="556e4-146">NOTES</span></span>

## <span data-ttu-id="556e4-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="556e4-147">RELATED LINKS</span></span>
