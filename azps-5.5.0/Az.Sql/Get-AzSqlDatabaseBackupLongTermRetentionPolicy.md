---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: 0dd5f38f00e715141a967160cadc8ab075825ac6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116157"
---
# <span data-ttu-id="4d10c-101">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="4d10c-101">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="4d10c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4d10c-102">SYNOPSIS</span></span>
<span data-ttu-id="4d10c-103">Obtém uma política de retenção de longo prazo do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="4d10c-103">Gets a database long term retention policy.</span></span>

## <span data-ttu-id="4d10c-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4d10c-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseBackupLongTermRetentionPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4d10c-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="4d10c-105">DESCRIPTION</span></span>
<span data-ttu-id="4d10c-106">O cmdlet **Get-AzSqlDatabaseBackupLongTermRetentionPolicy** obtém a política de retenção de longo prazo registrada nesse banco de dados.</span><span class="sxs-lookup"><span data-stu-id="4d10c-106">The **Get-AzSqlDatabaseBackupLongTermRetentionPolicy** cmdlet gets the long term retention policy registered to this database.</span></span>
<span data-ttu-id="4d10c-107">A política é um recurso de Backup do Azure usado para definir a política de armazenamento de backup.</span><span class="sxs-lookup"><span data-stu-id="4d10c-107">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="4d10c-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4d10c-108">EXAMPLES</span></span>

### <span data-ttu-id="4d10c-109">Exemplo 1: Obter a versão atual da política de retenção de longo prazo</span><span class="sxs-lookup"><span data-stu-id="4d10c-109">Example 1: Get the current version of the long term retention policy</span></span>
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

<span data-ttu-id="4d10c-110">Esse comando obtém a versão atual da política de retenção de longo prazo para o banco de dados01</span><span class="sxs-lookup"><span data-stu-id="4d10c-110">This command gets the current version of the long term retention policy for database01</span></span>

## <span data-ttu-id="4d10c-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4d10c-111">PARAMETERS</span></span>

### <span data-ttu-id="4d10c-112">-Nomedo Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="4d10c-112">-DatabaseName</span></span>
<span data-ttu-id="4d10c-113">O nome do banco de dados SQL do Azure a ser usado.</span><span class="sxs-lookup"><span data-stu-id="4d10c-113">The name of the Azure SQL Database to use.</span></span>

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

### <span data-ttu-id="4d10c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d10c-114">-DefaultProfile</span></span>
<span data-ttu-id="4d10c-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4d10c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d10c-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d10c-116">-ResourceGroupName</span></span>
<span data-ttu-id="4d10c-117">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4d10c-117">The name of the resource group.</span></span>

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

### <span data-ttu-id="4d10c-118">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4d10c-118">-ServerName</span></span>
<span data-ttu-id="4d10c-119">O nome do SQL Server do Azure no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="4d10c-119">The name of the Azure SQL Server the database is in.</span></span>

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

### <span data-ttu-id="4d10c-120">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="4d10c-120">-Confirm</span></span>
<span data-ttu-id="4d10c-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d10c-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d10c-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d10c-122">-WhatIf</span></span>
<span data-ttu-id="4d10c-123">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="4d10c-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d10c-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4d10c-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d10c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d10c-125">CommonParameters</span></span>
<span data-ttu-id="4d10c-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d10c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d10c-127">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4d10c-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d10c-128">Entradas</span><span class="sxs-lookup"><span data-stu-id="4d10c-128">INPUTS</span></span>

### <span data-ttu-id="4d10c-129">System.String</span><span class="sxs-lookup"><span data-stu-id="4d10c-129">System.String</span></span>

## <span data-ttu-id="4d10c-130">Saídas</span><span class="sxs-lookup"><span data-stu-id="4d10c-130">OUTPUTS</span></span>

### <span data-ttu-id="4d10c-131">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="4d10c-131">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="4d10c-132">Notas</span><span class="sxs-lookup"><span data-stu-id="4d10c-132">NOTES</span></span>

## <span data-ttu-id="4d10c-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4d10c-133">RELATED LINKS</span></span>

[<span data-ttu-id="4d10c-134">Get-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="4d10c-134">Get-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="4d10c-135">Remove-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="4d10c-135">Remove-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="4d10c-136">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="4d10c-136">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="4d10c-137">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="4d10c-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)