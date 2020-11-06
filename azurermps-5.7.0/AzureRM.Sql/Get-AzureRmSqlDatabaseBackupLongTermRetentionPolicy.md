---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: 0f43956dfa29dac2d7c6ca1869716400b8adad35
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432886"
---
# <span data-ttu-id="2be5f-101">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="2be5f-101">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="2be5f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2be5f-102">SYNOPSIS</span></span>
<span data-ttu-id="2be5f-103">Obtém uma política de retenção de longo prazo do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="2be5f-103">Gets a database long term retention policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2be5f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2be5f-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy [-Current] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2be5f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2be5f-105">DESCRIPTION</span></span>
<span data-ttu-id="2be5f-106">O cmdlet **Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy** Obtém a política de retenção de longo prazo registrada nesse banco de dados.</span><span class="sxs-lookup"><span data-stu-id="2be5f-106">The **Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy** cmdlet gets the long term retention policy registered to this database.</span></span>
<span data-ttu-id="2be5f-107">A política é um recurso de backup do Azure usado para definir a política de armazenamento de backup.</span><span class="sxs-lookup"><span data-stu-id="2be5f-107">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="2be5f-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2be5f-108">EXAMPLES</span></span>

### <span data-ttu-id="2be5f-109">Exemplo 1: obter a versão atual da política de retenção de longo prazo</span><span class="sxs-lookup"><span data-stu-id="2be5f-109">Example 1: Get the current version of the long term retention policy</span></span>
```powershell
PS C:\> Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -Current


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

<span data-ttu-id="2be5f-110">Este comando obtém a versão atual da política de retenção de longa duração para database01</span><span class="sxs-lookup"><span data-stu-id="2be5f-110">This command gets the current version of the long term retention policy for database01</span></span>

### <span data-ttu-id="2be5f-111">Exemplo 2: obter a versão herdada da política de retenção de longo prazo</span><span class="sxs-lookup"><span data-stu-id="2be5f-111">Example 2: Get the legacy version of the long term retention policy</span></span>
```powershell
PS C:\> Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        :
MonthlyRetention                       :
YearlyRetention                        :
WeekOfYear                             :
State                                  : Enabled
RecoveryServicesBackupPolicyResourceId : /subscriptions/4f2b42fc-4fc3-fd41-8ab8-5a382d8b30df/resourceGroups/resourcegroup01/providers/MicrosoftRecoveryServices/vaults/vault01/backupPolicies/policy01
Location                               : Southeast Asia
```

<span data-ttu-id="2be5f-112">Este comando obtém a versão herdada da política de retenção de longa duração para database01</span><span class="sxs-lookup"><span data-stu-id="2be5f-112">This command gets the legacy version of the long term retention policy for database01</span></span>

## <span data-ttu-id="2be5f-113">OS</span><span class="sxs-lookup"><span data-stu-id="2be5f-113">PARAMETERS</span></span>

### <span data-ttu-id="2be5f-114">-Atual</span><span class="sxs-lookup"><span data-stu-id="2be5f-114">-Current</span></span>
<span data-ttu-id="2be5f-115">Se não for fornecido, o comando retornará as informações herdadas da política de retenção de longo prazo.</span><span class="sxs-lookup"><span data-stu-id="2be5f-115">If not provided, the command returns the legacy Long Term Retention policy information.</span></span>
<span data-ttu-id="2be5f-116">Caso contrário, o comando retorna a versão atual da política de retenção de longo prazo.</span><span class="sxs-lookup"><span data-stu-id="2be5f-116">Otherwise, the command returns the current version of the Long Term Retention policy.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2be5f-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2be5f-117">-DatabaseName</span></span>
<span data-ttu-id="2be5f-118">O nome do banco de dados SQL do Azure a ser usado.</span><span class="sxs-lookup"><span data-stu-id="2be5f-118">The name of the Azure SQL Database to use.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2be5f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2be5f-119">-DefaultProfile</span></span>
<span data-ttu-id="2be5f-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2be5f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2be5f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2be5f-121">-ResourceGroupName</span></span>
<span data-ttu-id="2be5f-122">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2be5f-122">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2be5f-123">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="2be5f-123">-ServerName</span></span>
<span data-ttu-id="2be5f-124">O nome do Azure SQL Server no qual o banco de dados está.</span><span class="sxs-lookup"><span data-stu-id="2be5f-124">The name of the Azure SQL Server the database is in.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2be5f-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2be5f-125">-Confirm</span></span>
<span data-ttu-id="2be5f-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2be5f-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2be5f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2be5f-127">-WhatIf</span></span>
<span data-ttu-id="2be5f-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2be5f-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2be5f-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2be5f-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2be5f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2be5f-130">CommonParameters</span></span>
<span data-ttu-id="2be5f-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2be5f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="2be5f-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2be5f-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2be5f-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2be5f-133">INPUTS</span></span>

### <span data-ttu-id="2be5f-134">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="2be5f-134">None</span></span>
<span data-ttu-id="2be5f-135">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="2be5f-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2be5f-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2be5f-136">OUTPUTS</span></span>

### <span data-ttu-id="2be5f-137">Microsoft. Azure. Commands. Sql. backup. Model. AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="2be5f-137">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="2be5f-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2be5f-138">NOTES</span></span>

## <span data-ttu-id="2be5f-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2be5f-139">RELATED LINKS</span></span>

[<span data-ttu-id="2be5f-140">Get-AzureRmSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="2be5f-140">Get-AzureRmSqlDatabaseLongTermRetentionBackup</span></span>](./Get-AzureRmSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="2be5f-141">Remove-AzureRmSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="2be5f-141">Remove-AzureRmSqlDatabaseLongTermRetentionBackup</span></span>](./Remove-AzureRmSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="2be5f-142">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="2be5f-142">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="2be5f-143">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="2be5f-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)