---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsesqlpoolsensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolSensitivityClassification.md
ms.openlocfilehash: 0942373dc3ad741f10d5a87d7b4713413f9db4f3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892919"
---
# <span data-ttu-id="7b9d5-101">Get-AzSynapseSqlPoolSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="7b9d5-101">Get-AzSynapseSqlPoolSensitivityClassification</span></span>

## <span data-ttu-id="7b9d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b9d5-102">SYNOPSIS</span></span>
<span data-ttu-id="7b9d5-103">Obtém os tipos de informações atuais e os rótulos de sensibilidade das colunas no pool SQL de dados.</span><span class="sxs-lookup"><span data-stu-id="7b9d5-103">Gets the current information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="7b9d5-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="7b9d5-104">SYNTAX</span></span>

### <span data-ttu-id="7b9d5-105">SqlPoolObjectParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="7b9d5-105">SqlPoolObjectParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolSensitivityClassification -SqlPoolObject <PSSynapseSqlPool> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7b9d5-106">SqlPoolParameterSet</span><span class="sxs-lookup"><span data-stu-id="7b9d5-106">SqlPoolParameterSet</span></span>
```
Get-AzSynapseSqlPoolSensitivityClassification [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SqlPoolName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7b9d5-107">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="7b9d5-107">ColumnParameterSet</span></span>
```
Get-AzSynapseSqlPoolSensitivityClassification [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SqlPoolName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7b9d5-108">SqlPoolObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="7b9d5-108">SqlPoolObjectColumnParameterSet</span></span>
```
Get-AzSynapseSqlPoolSensitivityClassification -SqlPoolObject <PSSynapseSqlPool> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7b9d5-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="7b9d5-109">DESCRIPTION</span></span>
<span data-ttu-id="7b9d5-110">O Get-AzSynapseSqlPoolSensitivityClassification cmdlet retorna os tipos de informações atuais e rótulos de sensibilidade de colunas no pool de SQL do Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="7b9d5-110">The Get-AzSynapseSqlPoolSensitivityClassification cmdlet returns the current information types and sensitivity labels of columns in the Azure Synapse SQL pool.</span></span>

## <span data-ttu-id="7b9d5-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7b9d5-111">EXAMPLES</span></span>

### <span data-ttu-id="7b9d5-112">Exemplo 1: Obter tipos de informações atuais e rótulos de sensibilidade de um pool de SQL Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="7b9d5-112">Example 1: Get current information types and sensitivity labels of an Azure Synapse SQL pool.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolSensitivityClassification -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool

ResourceGroupName : ContosoResourceGroup
WorkspaceName        : ContosoWorkspace
SqlPoolName      : ContosoSqlPool
SensitivityLabels : {{
                        SchemaName: dbo,
                        TableName: Report,
                        ColumnName: ReportEmailBody,
                        InformationType: Contact Info
                    }, {
                        SchemaName: dbo,
                        TableName: Report,
                        ColumnName: ReportEmailSubject,
                        SensitivityLabel: Confidential,
                        Rank: Medium
                    }, {
                        SchemaName: dbo,
                        TableName: EMailLog,
                        ColumnName: BounceEmailSubject,
                        SensitivityLabel: Confidential,
                        InformationType: Contact Info,
                        Rank: Medium
                    }}
```

### <span data-ttu-id="7b9d5-113">Exemplo 2: Obter tipos de informações atuais e rótulos de sensibilidade de um pool de SQL Synapse do Azure com Piping.</span><span class="sxs-lookup"><span data-stu-id="7b9d5-113">Example 2: Get current information types and sensitivity labels of an Azure Synapse SQL pool with Piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool | Get-AzSynapseSqlPoolSensitivityClassification

ResourceGroupName : ContosoResourceGroup
WorkspaceName        : ContosoWorkspace
SqlPoolName      : ContosoSqlPool
SensitivityLabels : {{
                        SchemaName: dbo,
                        TableName: Report,
                        ColumnName: ReportEmailBody,
                        InformationType: Contact Info
                    }, {
                        SchemaName: dbo,
                        TableName: Report,
                        ColumnName: ReportEmailSubject,
                        SensitivityLabel: Confidential,
                        Rank: Medium
                    }, {
                        SchemaName: dbo,
                        TableName: EMailLog,
                        ColumnName: BounceEmailSubject,
                        SensitivityLabel: Confidential,
                        InformationType: Contact Info,
                        Rank: Medium
                    }}
```

### <span data-ttu-id="7b9d5-114">Exemplo 3: obter o tipo de informação atual e o rótulo de sensibilidade de uma coluna específica de um pool SQL Synapse do Azure.</span><span class="sxs-lookup"><span data-stu-id="7b9d5-114">Example 3: Get current information type and sensitivity label of a specific column of an Azure Synapse SQL pool.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolSensitivityClassification -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool -SchemaName dbo -TableName EMailLog -ColumnName BounceEmailSubject

ResourceGroupName : ContosoResourceGroup
WorkspaceName        : ContosoWorkspace
SqlPoolName      : ContosoSqlPool
SensitivityLabels : {{
                        SchemaName: dbo,
                        TableName: EMailLog,
                        ColumnName: BounceEmailSubject,
                        SensitivityLabel: Confidential,
                        InformationType: Contact Info,
                        Rank: Medium
                    }}
```

### <span data-ttu-id="7b9d5-115">Exemplo 4: obter o tipo de informação atual e o rótulo de sensibilidade de uma coluna específica de um pool SQL Synapse do Azure usando Piping.</span><span class="sxs-lookup"><span data-stu-id="7b9d5-115">Example 4: Get current information type and sensitivity label of a specific column of an Azure Synapse SQL pool using Piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Get-AzSynapseSqlPoolSensitivityClassification -SchemaName dbo -TableName EMailLog -ColumnName BounceEmailSubject

ResourceGroupName : ContosoResourceGroup
WorkspaceName        : ContosoWorkspace
SqlPoolName      : ContosoSqlPool
SensitivityLabels : {{
                        SchemaName: dbo,
                        TableName: EMailLog,
                        ColumnName: BounceEmailSubject,
                        SensitivityLabel: Confidential,
                        InformationType: Contact Info,
                        Rank: Medium
                    }}
```

## <span data-ttu-id="7b9d5-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="7b9d5-116">PARAMETERS</span></span>

### <span data-ttu-id="7b9d5-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7b9d5-117">-AsJob</span></span>
<span data-ttu-id="7b9d5-118">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="7b9d5-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7b9d5-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="7b9d5-119">-ColumnName</span></span>
<span data-ttu-id="7b9d5-120">Nome da coluna.</span><span class="sxs-lookup"><span data-stu-id="7b9d5-120">Name of column.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, SqlPoolObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b9d5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b9d5-121">-DefaultProfile</span></span>
<span data-ttu-id="7b9d5-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7b9d5-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b9d5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b9d5-123">-ResourceGroupName</span></span>
<span data-ttu-id="7b9d5-124">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7b9d5-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlPoolParameterSet, ColumnParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b9d5-125">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="7b9d5-125">-SchemaName</span></span>
<span data-ttu-id="7b9d5-126">Nome do esquema.</span><span class="sxs-lookup"><span data-stu-id="7b9d5-126">Name of schema.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, SqlPoolObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b9d5-127">-SqlPoolName</span><span class="sxs-lookup"><span data-stu-id="7b9d5-127">-SqlPoolName</span></span>
<span data-ttu-id="7b9d5-128">Nome do pool SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="7b9d5-128">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlPoolParameterSet, ColumnParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b9d5-129">-SqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="7b9d5-129">-SqlPoolObject</span></span>
<span data-ttu-id="7b9d5-130">SQL objeto de entrada do pool, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="7b9d5-130">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: SqlPoolObjectParameterSet, SqlPoolObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7b9d5-131">-TableName</span><span class="sxs-lookup"><span data-stu-id="7b9d5-131">-TableName</span></span>
<span data-ttu-id="7b9d5-132">Nome da tabela.</span><span class="sxs-lookup"><span data-stu-id="7b9d5-132">Name of table.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, SqlPoolObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b9d5-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="7b9d5-133">-WorkspaceName</span></span>
<span data-ttu-id="7b9d5-134">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="7b9d5-134">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlPoolParameterSet, ColumnParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b9d5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b9d5-135">CommonParameters</span></span>
<span data-ttu-id="7b9d5-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b9d5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b9d5-137">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7b9d5-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b9d5-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7b9d5-138">INPUTS</span></span>

### <span data-ttu-id="7b9d5-139">System.String</span><span class="sxs-lookup"><span data-stu-id="7b9d5-139">System.String</span></span>

### <span data-ttu-id="7b9d5-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="7b9d5-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="7b9d5-141">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="7b9d5-141">OUTPUTS</span></span>

### <span data-ttu-id="7b9d5-142">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="7b9d5-142">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span></span>

## <span data-ttu-id="7b9d5-143">NOTES</span><span class="sxs-lookup"><span data-stu-id="7b9d5-143">NOTES</span></span>

## <span data-ttu-id="7b9d5-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7b9d5-144">RELATED LINKS</span></span>
