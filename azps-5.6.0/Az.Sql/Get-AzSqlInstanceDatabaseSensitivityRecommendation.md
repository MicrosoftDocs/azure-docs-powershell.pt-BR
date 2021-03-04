---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/powershell/module/az.sql/Get-AzSqlInstanceDatabaseSensitivityRecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseSensitivityRecommendation.md
ms.openlocfilehash: 0d40e03b26481b5e974b294533566549646ba628
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891577"
---
# <span data-ttu-id="534ab-101">Get-AzSqlInstanceDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="534ab-101">Get-AzSqlInstanceDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="534ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="534ab-102">SYNOPSIS</span></span>
<span data-ttu-id="534ab-103">Obtém os tipos de informações recomendados e rótulos de sensibilidade de colunas no banco de dados de instância gerenciada do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="534ab-103">Gets the recommended information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="534ab-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="534ab-104">SYNTAX</span></span>

### <span data-ttu-id="534ab-105">DatabaseObjectParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="534ab-105">DatabaseObjectParameterSet (Default)</span></span>
```
Get-AzSqlInstanceDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlManagedDatabaseModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="534ab-106">DatabaseParameterSet</span><span class="sxs-lookup"><span data-stu-id="534ab-106">DatabaseParameterSet</span></span>
```
Get-AzSqlInstanceDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="534ab-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="534ab-107">DESCRIPTION</span></span>
<span data-ttu-id="534ab-108">O Get-AzSqlInstanceDatabaseSensitivityRecommendation cmdlet retorna os tipos de informações recomendados e os rótulos de sensibilidade das colunas no banco de dados de instância gerenciada do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="534ab-108">The Get-AzSqlInstanceDatabaseSensitivityRecommendation cmdlet returns the recommended information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="534ab-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="534ab-109">EXAMPLES</span></span>

### <span data-ttu-id="534ab-110">Exemplo 1: Obter tipos de informações recomendados e rótulos de sensibilidade de um banco de dados de instância SQL instância gerenciada do Azure.</span><span class="sxs-lookup"><span data-stu-id="534ab-110">Example 1: Get recommended information types and sensitivity labels of an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database

ResourceGroupName : resourceGroup
InstanceName      : managedInstance
DatabaseName      : database
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

### <span data-ttu-id="534ab-111">Exemplo 2: Obter tipos de informações recomendados e rótulos de sensibilidade de um banco de dados de instância gerenciada do Azure SQL usando Piping.</span><span class="sxs-lookup"><span data-stu-id="534ab-111">Example 2: Get recommended information types and sensitivity labels of an Azure SQL managed instance database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -Name database | Get-AzSqlInstanceDatabaseSensitivityRecommendation

ResourceGroupName : resourceGroup
InstanceName      : managedInstance
DatabaseName      : database
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

## <span data-ttu-id="534ab-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="534ab-112">PARAMETERS</span></span>

### <span data-ttu-id="534ab-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="534ab-113">-AsJob</span></span>
<span data-ttu-id="534ab-114">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="534ab-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="534ab-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="534ab-115">-DatabaseName</span></span>
<span data-ttu-id="534ab-116">O nome do banco de dados de instância gerenciada do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="534ab-116">The name of the Azure SQL managed instance database.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="534ab-117">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="534ab-117">-DatabaseObject</span></span>
<span data-ttu-id="534ab-118">O objeto de banco de dados SQL instância gerenciada do Azure.</span><span class="sxs-lookup"><span data-stu-id="534ab-118">The Azure SQL managed instance database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel
Parameter Sets: DatabaseObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="534ab-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="534ab-119">-DefaultProfile</span></span>
<span data-ttu-id="534ab-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="534ab-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="534ab-121">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="534ab-121">-InstanceName</span></span>
<span data-ttu-id="534ab-122">O Azure SQL nome da instância gerenciada.</span><span class="sxs-lookup"><span data-stu-id="534ab-122">Azure SQL managed instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="534ab-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="534ab-123">-ResourceGroupName</span></span>
<span data-ttu-id="534ab-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="534ab-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="534ab-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="534ab-125">CommonParameters</span></span>
<span data-ttu-id="534ab-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="534ab-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="534ab-127">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="534ab-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="534ab-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="534ab-128">INPUTS</span></span>

### <span data-ttu-id="534ab-129">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="534ab-129">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="534ab-130">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="534ab-130">OUTPUTS</span></span>

### <span data-ttu-id="534ab-131">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="534ab-131">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="534ab-132">NOTES</span><span class="sxs-lookup"><span data-stu-id="534ab-132">NOTES</span></span>

## <span data-ttu-id="534ab-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="534ab-133">RELATED LINKS</span></span>

[<span data-ttu-id="534ab-134">Saiba mais sobre a descoberta e classificação de dados SQL banco de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="534ab-134">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/azure/sql-database/sql-database-data-discovery-and-classification)
