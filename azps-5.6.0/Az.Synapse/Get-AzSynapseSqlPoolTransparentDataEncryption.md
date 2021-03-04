---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsesqlpooltransparentdataencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolTransparentDataEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolTransparentDataEncryption.md
ms.openlocfilehash: cee34e8437048f0cc59df3463b0b7f3cf2de6ed6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889592"
---
# <span data-ttu-id="c7182-101">Get-AzSynapseSqlPoolTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="c7182-101">Get-AzSynapseSqlPoolTransparentDataEncryption</span></span>

## <span data-ttu-id="c7182-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7182-102">SYNOPSIS</span></span>
<span data-ttu-id="c7182-103">Obtém o estado TDE de um pool de SQL.</span><span class="sxs-lookup"><span data-stu-id="c7182-103">Gets the TDE state for a SQL pool.</span></span>

## <span data-ttu-id="c7182-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c7182-104">SYNTAX</span></span>

### <span data-ttu-id="c7182-105">GetByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="c7182-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolTransparentDataEncryption [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c7182-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7182-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolTransparentDataEncryption -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c7182-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7182-107">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolTransparentDataEncryption -InputObject <PSSynapseSqlPool>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c7182-108">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7182-108">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlPoolTransparentDataEncryption -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c7182-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c7182-109">DESCRIPTION</span></span>
<span data-ttu-id="c7182-110">O cmdlet **Get-AzSynapseSqlPoolTransparentDataEncryption** obtém o estado de Criptografia de Dados Transparentes (TDE) para um pool do Azure Synapse Analytics SQL.</span><span class="sxs-lookup"><span data-stu-id="c7182-110">The **Get-AzSynapseSqlPoolTransparentDataEncryption** cmdlet gets the state of Transparent Data Encryption (TDE) for an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="c7182-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c7182-111">EXAMPLES</span></span>

### <span data-ttu-id="c7182-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c7182-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolTransparentDataEncryption -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="c7182-113">Este comando obtém o status de TDE para o pool SQL chamado ContosoSqlPool no espaço de trabalho chamado ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="c7182-113">This command gets the status of TDE for the SQL pool named ContosoSqlPool under the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="c7182-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c7182-114">PARAMETERS</span></span>

### <span data-ttu-id="c7182-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7182-115">-DefaultProfile</span></span>
<span data-ttu-id="c7182-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c7182-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7182-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c7182-117">-InputObject</span></span>
<span data-ttu-id="c7182-118">SQL objeto de entrada do pool, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="c7182-118">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: GetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c7182-119">-Name</span><span class="sxs-lookup"><span data-stu-id="c7182-119">-Name</span></span>
<span data-ttu-id="c7182-120">Nome do pool SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="c7182-120">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7182-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7182-121">-ResourceGroupName</span></span>
<span data-ttu-id="c7182-122">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c7182-122">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7182-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c7182-123">-ResourceId</span></span>
<span data-ttu-id="c7182-124">Identificador de recursos do Pool SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="c7182-124">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7182-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c7182-125">-WorkspaceName</span></span>
<span data-ttu-id="c7182-126">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="c7182-126">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7182-127">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="c7182-127">-WorkspaceObject</span></span>
<span data-ttu-id="c7182-128">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="c7182-128">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c7182-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7182-129">CommonParameters</span></span>
<span data-ttu-id="c7182-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7182-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7182-131">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c7182-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7182-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c7182-132">INPUTS</span></span>

### <span data-ttu-id="c7182-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="c7182-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="c7182-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="c7182-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="c7182-135">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c7182-135">OUTPUTS</span></span>

### <span data-ttu-id="c7182-136">Microsoft.Azure.Commands.Synapse.Models.PSTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="c7182-136">Microsoft.Azure.Commands.Synapse.Models.PSTransparentDataEncryption</span></span>

## <span data-ttu-id="c7182-137">NOTES</span><span class="sxs-lookup"><span data-stu-id="c7182-137">NOTES</span></span>

## <span data-ttu-id="c7182-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c7182-138">RELATED LINKS</span></span>
