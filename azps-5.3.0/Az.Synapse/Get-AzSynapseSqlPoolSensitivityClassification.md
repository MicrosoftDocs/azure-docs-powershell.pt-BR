---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlpoolsensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolSensitivityClassification.md
ms.openlocfilehash: 6affe94fdbfa7a698ad7d666d1847365fc8e25ac
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98272412"
---
# <span data-ttu-id="732ab-101">Get-AzSynapseSqlPoolSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="732ab-101">Get-AzSynapseSqlPoolSensitivityClassification</span></span>

## <span data-ttu-id="732ab-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="732ab-102">SYNOPSIS</span></span>
<span data-ttu-id="732ab-103">Obtém os tipos de informações atuais e os rótulos de sensibilidade de colunas no pool do SQL.</span><span class="sxs-lookup"><span data-stu-id="732ab-103">Gets the current information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="732ab-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="732ab-104">SYNTAX</span></span>

### <span data-ttu-id="732ab-105">SqlPoolObjectParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="732ab-105">SqlPoolObjectParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolSensitivityClassification -SqlPoolObject <PSSynapseSqlPool> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="732ab-106">SqlPoolParameterSet</span><span class="sxs-lookup"><span data-stu-id="732ab-106">SqlPoolParameterSet</span></span>
```
Get-AzSynapseSqlPoolSensitivityClassification [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SqlPoolName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="732ab-107">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="732ab-107">ColumnParameterSet</span></span>
```
Get-AzSynapseSqlPoolSensitivityClassification [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SqlPoolName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="732ab-108">SqlPoolObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="732ab-108">SqlPoolObjectColumnParameterSet</span></span>
```
Get-AzSynapseSqlPoolSensitivityClassification -SqlPoolObject <PSSynapseSqlPool> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="732ab-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="732ab-109">DESCRIPTION</span></span>
<span data-ttu-id="732ab-110">O cmdlet Get-AzSynapseSqlPoolSensitivityClassification retorna os tipos de informações atuais e rótulos de sensibilidade de colunas no pool do SQL do Synapse do Azure.</span><span class="sxs-lookup"><span data-stu-id="732ab-110">The Get-AzSynapseSqlPoolSensitivityClassification cmdlet returns the current information types and sensitivity labels of columns in the Azure Synapse SQL pool.</span></span>

## <span data-ttu-id="732ab-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="732ab-111">EXAMPLES</span></span>

### <span data-ttu-id="732ab-112">Exemplo 1: obter tipos de informações atuais e rótulos de sensibilidade de um pool do SQL do Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="732ab-112">Example 1: Get current information types and sensitivity labels of an Azure Synapse SQL pool.</span></span>
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

### <span data-ttu-id="732ab-113">Exemplo 2: obter tipos de informações atuais e rótulos de sensibilidade de um pool do SQL do Synapse do Azure com tubulação.</span><span class="sxs-lookup"><span data-stu-id="732ab-113">Example 2: Get current information types and sensitivity labels of an Azure Synapse SQL pool with Piping.</span></span>
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

### <span data-ttu-id="732ab-114">Exemplo 3: obter tipo de informação atual e rótulo de sensibilidade de uma coluna específica de um pool do SQL do Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="732ab-114">Example 3: Get current information type and sensitivity label of a specific column of an Azure Synapse SQL pool.</span></span>
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

### <span data-ttu-id="732ab-115">Exemplo 4: obter tipo de informação atual e rótulo de sensibilidade de uma coluna específica de um pool do SQL Synapse do Azure usando o encanamento.</span><span class="sxs-lookup"><span data-stu-id="732ab-115">Example 4: Get current information type and sensitivity label of a specific column of an Azure Synapse SQL pool using Piping.</span></span>
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

## <span data-ttu-id="732ab-116">OS</span><span class="sxs-lookup"><span data-stu-id="732ab-116">PARAMETERS</span></span>

### <span data-ttu-id="732ab-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="732ab-117">-AsJob</span></span>
<span data-ttu-id="732ab-118">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="732ab-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="732ab-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="732ab-119">-ColumnName</span></span>
<span data-ttu-id="732ab-120">Nome da coluna.</span><span class="sxs-lookup"><span data-stu-id="732ab-120">Name of column.</span></span>

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

### <span data-ttu-id="732ab-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="732ab-121">-DefaultProfile</span></span>
<span data-ttu-id="732ab-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="732ab-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="732ab-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="732ab-123">-ResourceGroupName</span></span>
<span data-ttu-id="732ab-124">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="732ab-124">Resource group name.</span></span>

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

### <span data-ttu-id="732ab-125">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="732ab-125">-SchemaName</span></span>
<span data-ttu-id="732ab-126">Nome do esquema.</span><span class="sxs-lookup"><span data-stu-id="732ab-126">Name of schema.</span></span>

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

### <span data-ttu-id="732ab-127">-Sqlpoolname</span><span class="sxs-lookup"><span data-stu-id="732ab-127">-SqlPoolName</span></span>
<span data-ttu-id="732ab-128">Nome do pool do SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="732ab-128">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="732ab-129">-Sqlpoolobject</span><span class="sxs-lookup"><span data-stu-id="732ab-129">-SqlPoolObject</span></span>
<span data-ttu-id="732ab-130">Objeto de entrada de pool SQL, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="732ab-130">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="732ab-131">-TableName</span><span class="sxs-lookup"><span data-stu-id="732ab-131">-TableName</span></span>
<span data-ttu-id="732ab-132">Nome da tabela.</span><span class="sxs-lookup"><span data-stu-id="732ab-132">Name of table.</span></span>

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

### <span data-ttu-id="732ab-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="732ab-133">-WorkspaceName</span></span>
<span data-ttu-id="732ab-134">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="732ab-134">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="732ab-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="732ab-135">CommonParameters</span></span>
<span data-ttu-id="732ab-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="732ab-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="732ab-137">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="732ab-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="732ab-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="732ab-138">INPUTS</span></span>

### <span data-ttu-id="732ab-139">System. String</span><span class="sxs-lookup"><span data-stu-id="732ab-139">System.String</span></span>

### <span data-ttu-id="732ab-140">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="732ab-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="732ab-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="732ab-141">OUTPUTS</span></span>

### <span data-ttu-id="732ab-142">Microsoft. Azure. Commands. Synapse. Models. dataclassation. SqlPoolSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="732ab-142">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span></span>

## <span data-ttu-id="732ab-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="732ab-143">NOTES</span></span>

## <span data-ttu-id="732ab-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="732ab-144">RELATED LINKS</span></span>
