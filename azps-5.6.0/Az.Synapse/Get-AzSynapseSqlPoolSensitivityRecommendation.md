---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsesqlpoolsensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolSensitivityRecommendation.md
ms.openlocfilehash: d2949bf2d366dc64b0e55b82d0c90979042ea294
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889594"
---
# <span data-ttu-id="8a2e9-101">Get-AzSynapseSqlPoolSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="8a2e9-101">Get-AzSynapseSqlPoolSensitivityRecommendation</span></span>

## <span data-ttu-id="8a2e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a2e9-102">SYNOPSIS</span></span>
<span data-ttu-id="8a2e9-103">Obtém os tipos de informações recomendados e os rótulos de sensibilidade das colunas no pool SQL de dados.</span><span class="sxs-lookup"><span data-stu-id="8a2e9-103">Gets the recommended information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="8a2e9-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="8a2e9-104">SYNTAX</span></span>

### <span data-ttu-id="8a2e9-105">SqlPoolObjectParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="8a2e9-105">SqlPoolObjectParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolSensitivityRecommendation -SqlPoolObject <PSSynapseSqlPool> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8a2e9-106">SqlPoolParameterSet</span><span class="sxs-lookup"><span data-stu-id="8a2e9-106">SqlPoolParameterSet</span></span>
```
Get-AzSynapseSqlPoolSensitivityRecommendation [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SqlPoolName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8a2e9-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="8a2e9-107">DESCRIPTION</span></span>
<span data-ttu-id="8a2e9-108">O Get-AzSynapseSqlPoolSensitivityRecommendation cmdlet retorna os tipos de informações recomendados e os rótulos de sensibilidade das colunas no pool SQL.</span><span class="sxs-lookup"><span data-stu-id="8a2e9-108">The Get-AzSynapseSqlPoolSensitivityRecommendation cmdlet returns the recommended information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="8a2e9-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8a2e9-109">EXAMPLES</span></span>

### <span data-ttu-id="8a2e9-110">Exemplo 1: Obter tipos de informações recomendados e rótulos de sensibilidade de um pool do Azure Synapse SQL pool.</span><span class="sxs-lookup"><span data-stu-id="8a2e9-110">Example 1: Get recommended information types and sensitivity labels of an Azure Synapse SQL pool.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolSensitivityRecommendation -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool

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

### <span data-ttu-id="8a2e9-111">Exemplo 2: Obter tipos de informações recomendados e rótulos de sensibilidade de um pool SQL Azure Synapse usando Piping.</span><span class="sxs-lookup"><span data-stu-id="8a2e9-111">Example 2: Get recommended information types and sensitivity labels of an Azure Synapse SQL pool using Piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Get-AzSynapseSqlPoolSensitivityRecommendation

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

## <span data-ttu-id="8a2e9-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="8a2e9-112">PARAMETERS</span></span>

### <span data-ttu-id="8a2e9-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8a2e9-113">-AsJob</span></span>
<span data-ttu-id="8a2e9-114">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="8a2e9-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8a2e9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a2e9-115">-DefaultProfile</span></span>
<span data-ttu-id="8a2e9-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8a2e9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a2e9-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a2e9-117">-ResourceGroupName</span></span>
<span data-ttu-id="8a2e9-118">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8a2e9-118">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlPoolParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a2e9-119">-SqlPoolName</span><span class="sxs-lookup"><span data-stu-id="8a2e9-119">-SqlPoolName</span></span>
<span data-ttu-id="8a2e9-120">Nome do pool SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="8a2e9-120">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlPoolParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a2e9-121">-SqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="8a2e9-121">-SqlPoolObject</span></span>
<span data-ttu-id="8a2e9-122">SQL objeto de entrada do pool, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="8a2e9-122">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: SqlPoolObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8a2e9-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="8a2e9-123">-WorkspaceName</span></span>
<span data-ttu-id="8a2e9-124">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="8a2e9-124">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlPoolParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a2e9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a2e9-125">CommonParameters</span></span>
<span data-ttu-id="8a2e9-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a2e9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a2e9-127">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8a2e9-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a2e9-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8a2e9-128">INPUTS</span></span>

### <span data-ttu-id="8a2e9-129">System.String</span><span class="sxs-lookup"><span data-stu-id="8a2e9-129">System.String</span></span>

### <span data-ttu-id="8a2e9-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="8a2e9-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="8a2e9-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="8a2e9-131">OUTPUTS</span></span>

### <span data-ttu-id="8a2e9-132">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="8a2e9-132">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span></span>

## <span data-ttu-id="8a2e9-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="8a2e9-133">NOTES</span></span>

## <span data-ttu-id="8a2e9-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8a2e9-134">RELATED LINKS</span></span>
