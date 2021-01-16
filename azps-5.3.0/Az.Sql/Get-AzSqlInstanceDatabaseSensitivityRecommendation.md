---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Get-AzSqlInstanceDatabaseSensitivityRecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseSensitivityRecommendation.md
ms.openlocfilehash: cf9250080e0d8e079257a4996b7d263bd96a2093
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98428698"
---
# <span data-ttu-id="09cf6-101">Get-AzSqlInstanceDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="09cf6-101">Get-AzSqlInstanceDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="09cf6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="09cf6-102">SYNOPSIS</span></span>
<span data-ttu-id="09cf6-103">Obtém os tipos de informações recomendadas e os rótulos de sensibilidade de colunas no banco de dados de instância gerenciada do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="09cf6-103">Gets the recommended information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="09cf6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="09cf6-104">SYNTAX</span></span>

### <span data-ttu-id="09cf6-105">DatabaseObjectParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="09cf6-105">DatabaseObjectParameterSet (Default)</span></span>
```
Get-AzSqlInstanceDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlManagedDatabaseModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09cf6-106">DatabaseParameterSet</span><span class="sxs-lookup"><span data-stu-id="09cf6-106">DatabaseParameterSet</span></span>
```
Get-AzSqlInstanceDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="09cf6-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="09cf6-107">DESCRIPTION</span></span>
<span data-ttu-id="09cf6-108">O cmdlet Get-AzSqlInstanceDatabaseSensitivityRecommendation retorna os tipos de informações recomendadas e rótulos de sensibilidade de colunas no banco de dados instância gerenciada do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="09cf6-108">The Get-AzSqlInstanceDatabaseSensitivityRecommendation cmdlet returns the recommended information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="09cf6-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="09cf6-109">EXAMPLES</span></span>

### <span data-ttu-id="09cf6-110">Exemplo 1: obter tipos de informações recomendadas e rótulos de sensibilidade de um banco de dados de instância gerenciada do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="09cf6-110">Example 1: Get recommended information types and sensitivity labels of an Azure SQL managed instance database.</span></span>
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

### <span data-ttu-id="09cf6-111">Exemplo 2: obter tipos de informações recomendadas e rótulos de sensibilidade de um banco de dados de instância gerenciada do Azure SQL usando o encanamento.</span><span class="sxs-lookup"><span data-stu-id="09cf6-111">Example 2: Get recommended information types and sensitivity labels of an Azure SQL managed instance database using Piping.</span></span>
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

## <span data-ttu-id="09cf6-112">OS</span><span class="sxs-lookup"><span data-stu-id="09cf6-112">PARAMETERS</span></span>

### <span data-ttu-id="09cf6-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="09cf6-113">-AsJob</span></span>
<span data-ttu-id="09cf6-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="09cf6-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="09cf6-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="09cf6-115">-DatabaseName</span></span>
<span data-ttu-id="09cf6-116">O nome do banco de dados de instância gerenciada do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="09cf6-116">The name of the Azure SQL managed instance database.</span></span>

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

### <span data-ttu-id="09cf6-117">-Databaseobject</span><span class="sxs-lookup"><span data-stu-id="09cf6-117">-DatabaseObject</span></span>
<span data-ttu-id="09cf6-118">O objeto de banco de dados instância gerenciada SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="09cf6-118">The Azure SQL managed instance database object.</span></span>

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

### <span data-ttu-id="09cf6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09cf6-119">-DefaultProfile</span></span>
<span data-ttu-id="09cf6-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="09cf6-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09cf6-121">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="09cf6-121">-InstanceName</span></span>
<span data-ttu-id="09cf6-122">Nome da instância gerenciada SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="09cf6-122">Azure SQL managed instance name.</span></span>

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

### <span data-ttu-id="09cf6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09cf6-123">-ResourceGroupName</span></span>
<span data-ttu-id="09cf6-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="09cf6-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="09cf6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09cf6-125">CommonParameters</span></span>
<span data-ttu-id="09cf6-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09cf6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09cf6-127">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="09cf6-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09cf6-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="09cf6-128">INPUTS</span></span>

### <span data-ttu-id="09cf6-129">Microsoft. Azure. Commands. Sql. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="09cf6-129">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="09cf6-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="09cf6-130">OUTPUTS</span></span>

### <span data-ttu-id="09cf6-131">Microsoft. Azure. Commands. Sql. dataclassation. Model. ManagedDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="09cf6-131">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="09cf6-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="09cf6-132">NOTES</span></span>

## <span data-ttu-id="09cf6-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="09cf6-133">RELATED LINKS</span></span>

[<span data-ttu-id="09cf6-134">Saiba mais sobre a descoberta e a classificação de dados do banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="09cf6-134">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)
