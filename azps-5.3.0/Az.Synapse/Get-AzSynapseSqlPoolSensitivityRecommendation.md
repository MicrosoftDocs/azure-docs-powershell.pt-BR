---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlpoolsensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolSensitivityRecommendation.md
ms.openlocfilehash: 89b9b5df2f8233254d4c1cb430a80f0a8a91c13b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98272409"
---
# <span data-ttu-id="78399-101">Get-AzSynapseSqlPoolSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="78399-101">Get-AzSynapseSqlPoolSensitivityRecommendation</span></span>

## <span data-ttu-id="78399-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="78399-102">SYNOPSIS</span></span>
<span data-ttu-id="78399-103">Obtém os tipos de informações recomendadas e rótulos de sensibilidade de colunas no pool do SQL.</span><span class="sxs-lookup"><span data-stu-id="78399-103">Gets the recommended information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="78399-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="78399-104">SYNTAX</span></span>

### <span data-ttu-id="78399-105">SqlPoolObjectParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="78399-105">SqlPoolObjectParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolSensitivityRecommendation -SqlPoolObject <PSSynapseSqlPool> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78399-106">SqlPoolParameterSet</span><span class="sxs-lookup"><span data-stu-id="78399-106">SqlPoolParameterSet</span></span>
```
Get-AzSynapseSqlPoolSensitivityRecommendation [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SqlPoolName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="78399-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="78399-107">DESCRIPTION</span></span>
<span data-ttu-id="78399-108">O cmdlet Get-AzSynapseSqlPoolSensitivityRecommendation retorna os tipos de informações recomendadas e rótulos de sensibilidade de colunas no pool do SQL.</span><span class="sxs-lookup"><span data-stu-id="78399-108">The Get-AzSynapseSqlPoolSensitivityRecommendation cmdlet returns the recommended information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="78399-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="78399-109">EXAMPLES</span></span>

### <span data-ttu-id="78399-110">Exemplo 1: obter os tipos de informações recomendadas e rótulos de sensibilidade de um pool do SQL do Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="78399-110">Example 1: Get recommended information types and sensitivity labels of an Azure Synapse SQL pool.</span></span>
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

### <span data-ttu-id="78399-111">Exemplo 2: obter tipos de informações recomendadas e rótulos de sensibilidade de um pool SQL do Synapse do Azure usando o encanamento.</span><span class="sxs-lookup"><span data-stu-id="78399-111">Example 2: Get recommended information types and sensitivity labels of an Azure Synapse SQL pool using Piping.</span></span>
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

## <span data-ttu-id="78399-112">OS</span><span class="sxs-lookup"><span data-stu-id="78399-112">PARAMETERS</span></span>

### <span data-ttu-id="78399-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="78399-113">-AsJob</span></span>
<span data-ttu-id="78399-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="78399-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="78399-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78399-115">-DefaultProfile</span></span>
<span data-ttu-id="78399-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="78399-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78399-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78399-117">-ResourceGroupName</span></span>
<span data-ttu-id="78399-118">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="78399-118">Resource group name.</span></span>

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

### <span data-ttu-id="78399-119">-Sqlpoolname</span><span class="sxs-lookup"><span data-stu-id="78399-119">-SqlPoolName</span></span>
<span data-ttu-id="78399-120">Nome do pool do SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="78399-120">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="78399-121">-Sqlpoolobject</span><span class="sxs-lookup"><span data-stu-id="78399-121">-SqlPoolObject</span></span>
<span data-ttu-id="78399-122">Objeto de entrada de pool SQL, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="78399-122">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="78399-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="78399-123">-WorkspaceName</span></span>
<span data-ttu-id="78399-124">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="78399-124">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="78399-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78399-125">CommonParameters</span></span>
<span data-ttu-id="78399-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78399-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78399-127">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="78399-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78399-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="78399-128">INPUTS</span></span>

### <span data-ttu-id="78399-129">System. String</span><span class="sxs-lookup"><span data-stu-id="78399-129">System.String</span></span>

### <span data-ttu-id="78399-130">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="78399-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="78399-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="78399-131">OUTPUTS</span></span>

### <span data-ttu-id="78399-132">Microsoft. Azure. Commands. Synapse. Models. dataclassation. SqlPoolSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="78399-132">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span></span>

## <span data-ttu-id="78399-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="78399-133">NOTES</span></span>

## <span data-ttu-id="78399-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="78399-134">RELATED LINKS</span></span>
