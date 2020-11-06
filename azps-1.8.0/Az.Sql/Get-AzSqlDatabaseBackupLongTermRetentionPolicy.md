---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: ce7bf498dc005f6cae8bfff28f0e470cacff71ad
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599043"
---
# <span data-ttu-id="b0f55-101">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="b0f55-101">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="b0f55-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b0f55-102">SYNOPSIS</span></span>
<span data-ttu-id="b0f55-103">Obtém uma política de retenção de longo prazo do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="b0f55-103">Gets a database long term retention policy.</span></span>

## <span data-ttu-id="b0f55-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b0f55-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseBackupLongTermRetentionPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b0f55-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b0f55-105">DESCRIPTION</span></span>
<span data-ttu-id="b0f55-106">O cmdlet **Get-AzSqlDatabaseBackupLongTermRetentionPolicy** Obtém a política de retenção de longo prazo registrada nesse banco de dados.</span><span class="sxs-lookup"><span data-stu-id="b0f55-106">The **Get-AzSqlDatabaseBackupLongTermRetentionPolicy** cmdlet gets the long term retention policy registered to this database.</span></span>
<span data-ttu-id="b0f55-107">A política é um recurso de backup do Azure usado para definir a política de armazenamento de backup.</span><span class="sxs-lookup"><span data-stu-id="b0f55-107">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="b0f55-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b0f55-108">EXAMPLES</span></span>

### <span data-ttu-id="b0f55-109">Exemplo 1: obter a versão atual da política de retenção de longo prazo</span><span class="sxs-lookup"><span data-stu-id="b0f55-109">Example 1: Get the current version of the long term retention policy</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : P2W
MonthlyRetention                       : PT0S
YearlyRetention                        : PT0S
WeekOfYear                             : 0
State                                  :
RecoveryServicesBackupPolicyResourceId :
Location                               :
```

<span data-ttu-id="b0f55-110">Este comando obtém a versão atual da política de retenção de longa duração para database01</span><span class="sxs-lookup"><span data-stu-id="b0f55-110">This command gets the current version of the long term retention policy for database01</span></span>

## <span data-ttu-id="b0f55-111">OS</span><span class="sxs-lookup"><span data-stu-id="b0f55-111">PARAMETERS</span></span>

### <span data-ttu-id="b0f55-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b0f55-112">-DatabaseName</span></span>
<span data-ttu-id="b0f55-113">O nome do banco de dados SQL do Azure a ser usado.</span><span class="sxs-lookup"><span data-stu-id="b0f55-113">The name of the Azure SQL Database to use.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0f55-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0f55-114">-DefaultProfile</span></span>
<span data-ttu-id="b0f55-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b0f55-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0f55-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0f55-116">-ResourceGroupName</span></span>
<span data-ttu-id="b0f55-117">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b0f55-117">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0f55-118">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="b0f55-118">-ServerName</span></span>
<span data-ttu-id="b0f55-119">O nome do Azure SQL Server no qual o banco de dados está.</span><span class="sxs-lookup"><span data-stu-id="b0f55-119">The name of the Azure SQL Server the database is in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0f55-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b0f55-120">-Confirm</span></span>
<span data-ttu-id="b0f55-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b0f55-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0f55-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0f55-122">-WhatIf</span></span>
<span data-ttu-id="b0f55-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b0f55-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0f55-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b0f55-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0f55-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0f55-125">CommonParameters</span></span>
<span data-ttu-id="b0f55-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0f55-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0f55-127">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b0f55-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0f55-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b0f55-128">INPUTS</span></span>

### <span data-ttu-id="b0f55-129">System. String</span><span class="sxs-lookup"><span data-stu-id="b0f55-129">System.String</span></span>

## <span data-ttu-id="b0f55-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b0f55-130">OUTPUTS</span></span>

### <span data-ttu-id="b0f55-131">Microsoft. Azure. Commands. Sql. backup. Model. AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="b0f55-131">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="b0f55-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b0f55-132">NOTES</span></span>

## <span data-ttu-id="b0f55-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b0f55-133">RELATED LINKS</span></span>

[<span data-ttu-id="b0f55-134">Get-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="b0f55-134">Get-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="b0f55-135">Remove-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="b0f55-135">Remove-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="b0f55-136">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="b0f55-136">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="b0f55-137">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="b0f55-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)