---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsesqlpooltransparentdataencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlPoolTransparentDataEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlPoolTransparentDataEncryption.md
ms.openlocfilehash: 5a8dbd1f21d640d5d1cb38fa403ee05dec9cfc20
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116048"
---
# <span data-ttu-id="1ec1c-101">Set-AzSynapseSqlPoolTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="1ec1c-101">Set-AzSynapseSqlPoolTransparentDataEncryption</span></span>

## <span data-ttu-id="1ec1c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1ec1c-102">SYNOPSIS</span></span>
<span data-ttu-id="1ec1c-103">Modifica a propriedade TDE para um pool SQL.</span><span class="sxs-lookup"><span data-stu-id="1ec1c-103">Modifies TDE property for a SQL pool.</span></span>

## <span data-ttu-id="1ec1c-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1ec1c-104">SYNTAX</span></span>

### <span data-ttu-id="1ec1c-105">SetByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="1ec1c-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzSynapseSqlPoolTransparentDataEncryption [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> -State <TransparentDataEncryptionStateType> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ec1c-106">SetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ec1c-106">SetByParentObjectParameterSet</span></span>
```
Set-AzSynapseSqlPoolTransparentDataEncryption -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 -State <TransparentDataEncryptionStateType> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ec1c-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ec1c-107">SetByInputObjectParameterSet</span></span>
```
Set-AzSynapseSqlPoolTransparentDataEncryption -InputObject <PSSynapseSqlPool>
 -State <TransparentDataEncryptionStateType> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ec1c-108">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ec1c-108">SetByResourceIdParameterSet</span></span>
```
Set-AzSynapseSqlPoolTransparentDataEncryption -ResourceId <String> -State <TransparentDataEncryptionStateType>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ec1c-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="1ec1c-109">DESCRIPTION</span></span>
<span data-ttu-id="1ec1c-110">O cmdlet **Set-AzSynapseSqlPoolTransparentDataEncryption** modifica a propriedade TDE (Criptografia de Dados Transparentes) de um pool SQL do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="1ec1c-110">The **Set-AzSynapseSqlPoolTransparentDataEncryption** cmdlet modifies the Transparent Data Encryption (TDE) property of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="1ec1c-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1ec1c-111">EXAMPLES</span></span>

### <span data-ttu-id="1ec1c-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1ec1c-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseSqlPoolTransparentDataEncryption -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -State Enabled
```

<span data-ttu-id="1ec1c-113">Esse comando habilita o TDE para o pool SQL chamado ContosoSqlPool no espaço de trabalho chamado ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="1ec1c-113">This command enables TDE for the SQL pool named ContosoSqlPool under the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="1ec1c-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1ec1c-114">PARAMETERS</span></span>

### <span data-ttu-id="1ec1c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1ec1c-115">-AsJob</span></span>
<span data-ttu-id="1ec1c-116">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="1ec1c-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1ec1c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ec1c-117">-DefaultProfile</span></span>
<span data-ttu-id="1ec1c-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1ec1c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ec1c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1ec1c-119">-InputObject</span></span>
<span data-ttu-id="1ec1c-120">Objeto de entrada de pool SQL, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="1ec1c-120">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="1ec1c-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="1ec1c-121">-Name</span></span>
<span data-ttu-id="1ec1c-122">Nome do pool SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="1ec1c-122">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="1ec1c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ec1c-123">-ResourceGroupName</span></span>
<span data-ttu-id="1ec1c-124">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1ec1c-124">Resource group name.</span></span>

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

### <span data-ttu-id="1ec1c-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1ec1c-125">-ResourceId</span></span>
<span data-ttu-id="1ec1c-126">Identificador de recursos do Pool SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="1ec1c-126">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="1ec1c-127">-Estado</span><span class="sxs-lookup"><span data-stu-id="1ec1c-127">-State</span></span>
<span data-ttu-id="1ec1c-128">O estado de Criptografia de Dados Transparente do Pool de Dados do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="1ec1c-128">The Azure Synapse Analytics Sql Pool Transparent Data Encryption state.</span></span>

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

### <span data-ttu-id="1ec1c-129">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="1ec1c-129">-WorkspaceName</span></span>
<span data-ttu-id="1ec1c-130">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="1ec1c-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="1ec1c-131">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="1ec1c-131">-WorkspaceObject</span></span>
<span data-ttu-id="1ec1c-132">objeto de entrada de espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="1ec1c-132">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="1ec1c-133">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="1ec1c-133">-Confirm</span></span>
<span data-ttu-id="1ec1c-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ec1c-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ec1c-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ec1c-135">-WhatIf</span></span>
<span data-ttu-id="1ec1c-136">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="1ec1c-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ec1c-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1ec1c-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ec1c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ec1c-138">CommonParameters</span></span>
<span data-ttu-id="1ec1c-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ec1c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ec1c-140">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1ec1c-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ec1c-141">Entradas</span><span class="sxs-lookup"><span data-stu-id="1ec1c-141">INPUTS</span></span>

### <span data-ttu-id="1ec1c-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="1ec1c-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="1ec1c-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="1ec1c-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="1ec1c-144">Saídas</span><span class="sxs-lookup"><span data-stu-id="1ec1c-144">OUTPUTS</span></span>

### <span data-ttu-id="1ec1c-145">Microsoft.Azure.Commands.Synapse.Models.PSTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="1ec1c-145">Microsoft.Azure.Commands.Synapse.Models.PSTransparentDataEncryption</span></span>

## <span data-ttu-id="1ec1c-146">Notas</span><span class="sxs-lookup"><span data-stu-id="1ec1c-146">NOTES</span></span>

## <span data-ttu-id="1ec1c-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1ec1c-147">RELATED LINKS</span></span>
