---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 383F36F3-3F52-4FC3-99F7-831096E6037D
online version: ''
schema: 2.0.0
ms.openlocfilehash: ff7c7cd50b06a4110b6af12611f3d91eaedfd227
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945426"
---
# <span data-ttu-id="2f905-101">Start-AzureSqlDatabaseRestore</span><span class="sxs-lookup"><span data-stu-id="2f905-101">Start-AzureSqlDatabaseRestore</span></span>

## <span data-ttu-id="2f905-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2f905-102">SYNOPSIS</span></span>
<span data-ttu-id="2f905-103">Executa uma restauração point-in-time de um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="2f905-103">Performs a point in time restore of a database.</span></span>

## <span data-ttu-id="2f905-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2f905-104">SYNTAX</span></span>

### <span data-ttu-id="2f905-105">BySourceDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="2f905-105">BySourceDatabaseObject</span></span>
```
Start-AzureSqlDatabaseRestore [-SourceServerName <String>] -SourceDatabase <Database>
 [-TargetServerName <String>] -TargetDatabaseName <String> [-PointInTime <DateTime>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="2f905-106">BySourceRestorableDroppedDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="2f905-106">BySourceRestorableDroppedDatabaseObject</span></span>
```
Start-AzureSqlDatabaseRestore [-SourceServerName <String>]
 -SourceRestorableDroppedDatabase <RestorableDroppedDatabase> [-TargetServerName <String>]
 -TargetDatabaseName <String> [-PointInTime <DateTime>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="2f905-107">BySourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="2f905-107">BySourceDatabaseName</span></span>
```
Start-AzureSqlDatabaseRestore -SourceServerName <String> -SourceDatabaseName <String>
 [-TargetServerName <String>] -TargetDatabaseName <String> [-PointInTime <DateTime>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="2f905-108">BySourceRestorableDroppedDatabaseName</span><span class="sxs-lookup"><span data-stu-id="2f905-108">BySourceRestorableDroppedDatabaseName</span></span>
```
Start-AzureSqlDatabaseRestore -SourceServerName <String> -SourceDatabaseName <String>
 -SourceDatabaseDeletionDate <DateTime> [-TargetServerName <String>] [-RestorableDropped]
 -TargetDatabaseName <String> [-PointInTime <DateTime>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="2f905-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2f905-109">DESCRIPTION</span></span>
<span data-ttu-id="2f905-110">O cmdlet **Start-AzureSqlDatabaseRestore** executa uma restauração point-in-time de um banco de dados básico, padrão ou Premium.</span><span class="sxs-lookup"><span data-stu-id="2f905-110">The **Start-AzureSqlDatabaseRestore** cmdlet performs a point in time restore of a Basic, Standard or Premium database.</span></span>
<span data-ttu-id="2f905-111">O banco de dados SQL do Azure retém backups básicos de banco de dados por 7 dias, padrão por 14 dias e Premium para 35 dias.</span><span class="sxs-lookup"><span data-stu-id="2f905-111">Azure SQL Database retains Basic database backups 7 days, Standard for 14 days, and Premium for 35 days.</span></span>
<span data-ttu-id="2f905-112">A operação de restauração cria um novo banco de dados.</span><span class="sxs-lookup"><span data-stu-id="2f905-112">The restore operation creates a new database.</span></span>
<span data-ttu-id="2f905-113">Se o banco de dados de origem não for excluído, o parâmetro *SourceDatabaseName* e *TargetDatabaseName* deverá ter valores diferentes.</span><span class="sxs-lookup"><span data-stu-id="2f905-113">If the source database is not deleted, the *SourceDatabaseName* and *TargetDatabaseName* parameter must have different values.</span></span>

<span data-ttu-id="2f905-114">No momento, o banco de dados SQL do Azure não é compatível com a restauração entre servidores.</span><span class="sxs-lookup"><span data-stu-id="2f905-114">Azure SQL Database does not currently support cross server restore.</span></span>
<span data-ttu-id="2f905-115">Os nomes dos servidores de origem e de destino devem ser iguais.</span><span class="sxs-lookup"><span data-stu-id="2f905-115">The source and target server names must be the same.</span></span>

## <span data-ttu-id="2f905-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2f905-116">EXAMPLES</span></span>

### <span data-ttu-id="2f905-117">Exemplo 1: restaurar um banco de dados especificado como um objeto para um point-in-time</span><span class="sxs-lookup"><span data-stu-id="2f905-117">Example 1: Restore a database specified as an object to a point in time</span></span>
```
PS C:\> $Database = Get-AzureSqlDatabase -ServerName "Server01" -DatabaseName "Database17" 
PS C:\> $Operation = Start-AzureSqlDatabaseRestore -SourceDatabase $Database -TargetDatabaseName "DatabaseRestored" -PointInTime "2013-01-01 06:00:00"
```

<span data-ttu-id="2f905-118">O primeiro comando obtém um objeto de banco de dados para o banco de dados chamado Database17 no servidor chamado Server01 e, em seguida, armazena-o na variável $Database.</span><span class="sxs-lookup"><span data-stu-id="2f905-118">The first command gets a database object for the database named Database17 on the server named Server01, and then stores it in the $Database variable.</span></span>

<span data-ttu-id="2f905-119">O segundo comando restaura o banco de dados para um point-in-time específico.</span><span class="sxs-lookup"><span data-stu-id="2f905-119">The second command restores the database to a specific point in time.</span></span>
<span data-ttu-id="2f905-120">O comando especifica o nome do novo banco de dados.</span><span class="sxs-lookup"><span data-stu-id="2f905-120">The command specifies at name for the new database.</span></span>

### <span data-ttu-id="2f905-121">Exemplo 2: restaurar um banco de dados especificado pelo nome para um point-in-time</span><span class="sxs-lookup"><span data-stu-id="2f905-121">Example 2: Restore a database specified by name to a point in time</span></span>
```
PS C:\> $Operation = Start-AzureSqlDatabaseRestore -SourceServerName "Server01" -SourceDatabaseName "Database17" -TargetDatabaseName "DatabaseRestored" -PointInTime "2013-01-01 06:00:00"
```

<span data-ttu-id="2f905-122">Esse comando restaura o banco de dados chamado Database17 a um point-in-time específico.</span><span class="sxs-lookup"><span data-stu-id="2f905-122">This command restores the database named Database17 to a specific point in time.</span></span>
<span data-ttu-id="2f905-123">O comando especifica o nome do novo banco de dados.</span><span class="sxs-lookup"><span data-stu-id="2f905-123">The command specifies at name for the new database.</span></span>

### <span data-ttu-id="2f905-124">Exemplo 3: restaurar um banco de dados Descartado especificado como um objeto para um ponto no tempo</span><span class="sxs-lookup"><span data-stu-id="2f905-124">Example 3: Restore a dropped database specified as an object to a point in time</span></span>
```
PS C:\> $Database = Get-AzureSqlDatabase -RestorableDropped -ServerName "Server01" -DatabaseName "Database01" -DatabaseDeletionDate "2012-11-09T22:59:43.000Z" 
PS C:\> $Operation = Start-AzureSqlDatabaseRestore -SourceRestorableDroppedDatabase $Database -TargetDatabaseName "DroppedDatabaseRestored"
```

<span data-ttu-id="2f905-125">O primeiro comando obtém um objeto de banco de dados para o banco de dados chamado Database01 no servidor chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="2f905-125">The first command gets a database object for the database named Database01 on the server named Server01.</span></span>
<span data-ttu-id="2f905-126">O comando especifica o parâmetro *RestorableDropped* .</span><span class="sxs-lookup"><span data-stu-id="2f905-126">The command specifies the *RestorableDropped* parameter.</span></span>
<span data-ttu-id="2f905-127">Portanto, o cmdlet obtém o banco de dados recuperável desconectado do ponto de restauração especificado.</span><span class="sxs-lookup"><span data-stu-id="2f905-127">Therefore, the cmdlet gets restorable dropped database the specified restore point.</span></span>
<span data-ttu-id="2f905-128">O comando armazena esse objeto de banco de dados na variável $Database.</span><span class="sxs-lookup"><span data-stu-id="2f905-128">The command stores that database object in the $Database variable.</span></span>

<span data-ttu-id="2f905-129">O segundo comando restaura o banco de dados ignorado especificado pela $Database.</span><span class="sxs-lookup"><span data-stu-id="2f905-129">The second command restores the dropped database specified by $Database.</span></span>
<span data-ttu-id="2f905-130">O comando especifica o nome do novo banco de dados.</span><span class="sxs-lookup"><span data-stu-id="2f905-130">The command specifies at name for the new database.</span></span>

## <span data-ttu-id="2f905-131">OS</span><span class="sxs-lookup"><span data-stu-id="2f905-131">PARAMETERS</span></span>

### <span data-ttu-id="2f905-132">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="2f905-132">-PointInTime</span></span>
<span data-ttu-id="2f905-133">Especifica o ponto de restauração no qual restaurar o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="2f905-133">Specifies the restore point to which to restore the database.</span></span>
<span data-ttu-id="2f905-134">Quando a operação de restauração termina, o banco de dados é restaurado para o estado em que se encontra na data e hora em que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="2f905-134">When the restore operation finishes, the database is restored to the state it was at the date and time that this parameter specifies.</span></span>
<span data-ttu-id="2f905-135">Por padrão, para um banco de dados dinâmico definido como a hora atual e para um banco de dados solto, esse cmdlet usa a hora em que o banco de dados foi Descartado.</span><span class="sxs-lookup"><span data-stu-id="2f905-135">By default, for a live database this set to the current time, and for a dropped database, this cmdlet uses the time when the database was dropped.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f905-136">-Perfil</span><span class="sxs-lookup"><span data-stu-id="2f905-136">-Profile</span></span>
<span data-ttu-id="2f905-137">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="2f905-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2f905-138">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="2f905-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f905-139">-RestorableDropped</span><span class="sxs-lookup"><span data-stu-id="2f905-139">-RestorableDropped</span></span>
<span data-ttu-id="2f905-140">Indica que esse cmdlet restaura um banco de dados recuperável removido.</span><span class="sxs-lookup"><span data-stu-id="2f905-140">Indicates that this cmdlet restores a restorable dropped database.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: BySourceRestorableDroppedDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f905-141">-SourceDatabase</span><span class="sxs-lookup"><span data-stu-id="2f905-141">-SourceDatabase</span></span>
<span data-ttu-id="2f905-142">Especifica o nome do banco de dados que este cmdlet restaura.</span><span class="sxs-lookup"><span data-stu-id="2f905-142">Specifies the name of the database that this cmdlet restores.</span></span>

```yaml
Type: Database
Parameter Sets: BySourceDatabaseObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2f905-143">-SourceDatabaseDeletionDate</span><span class="sxs-lookup"><span data-stu-id="2f905-143">-SourceDatabaseDeletionDate</span></span>
<span data-ttu-id="2f905-144">Especifica a data e a hora em que o banco de dados foi excluído.</span><span class="sxs-lookup"><span data-stu-id="2f905-144">Specifies the date and time when the database was deleted.</span></span>
<span data-ttu-id="2f905-145">Você deve incluir milissegundos quando especificar o tempo para corresponder ao tempo de exclusão do banco de dados real.</span><span class="sxs-lookup"><span data-stu-id="2f905-145">You must include milliseconds when you specify the time to match the actual database deletion time.</span></span>

```yaml
Type: DateTime
Parameter Sets: BySourceRestorableDroppedDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f905-146">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="2f905-146">-SourceDatabaseName</span></span>
<span data-ttu-id="2f905-147">Especifica o nome do banco de dados dinâmico que este cmdlet restaura.</span><span class="sxs-lookup"><span data-stu-id="2f905-147">Specifies the name of the live database that this cmdlet restores.</span></span>

```yaml
Type: String
Parameter Sets: BySourceDatabaseName, BySourceRestorableDroppedDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f905-148">-SourceRestorableDroppedDatabase</span><span class="sxs-lookup"><span data-stu-id="2f905-148">-SourceRestorableDroppedDatabase</span></span>
<span data-ttu-id="2f905-149">Especifica um objeto que representa o banco de dados recuperável ignorado que esse cmdlet restaura.</span><span class="sxs-lookup"><span data-stu-id="2f905-149">Specifies an object that represents the restorable dropped database that this cmdlet restores.</span></span>
<span data-ttu-id="2f905-150">Para obter um objeto **RestorableDroppedDatabase** , use o cmdlet Get-AzureSqlDatabase e especifique o parâmetro *RestorableDropped* .</span><span class="sxs-lookup"><span data-stu-id="2f905-150">To obtain a **RestorableDroppedDatabase** object, use the Get-AzureSqlDatabase cmdlet, and specify the *RestorableDropped* parameter.</span></span>

```yaml
Type: RestorableDroppedDatabase
Parameter Sets: BySourceRestorableDroppedDatabaseObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2f905-151">-SourceServerName</span><span class="sxs-lookup"><span data-stu-id="2f905-151">-SourceServerName</span></span>
<span data-ttu-id="2f905-152">Especifica o nome do servidor no qual o banco de dados de origem está em tempo real ou em execução, ou no qual o banco de dados de origem foi executado antes de ser excluído.</span><span class="sxs-lookup"><span data-stu-id="2f905-152">Specifies the name of the server on which the source database is live and running, or on which the source database ran before it was deleted.</span></span>

```yaml
Type: String
Parameter Sets: BySourceDatabaseObject, BySourceRestorableDroppedDatabaseObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: BySourceDatabaseName, BySourceRestorableDroppedDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f905-153">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="2f905-153">-TargetDatabaseName</span></span>
<span data-ttu-id="2f905-154">Especifica o nome do novo banco de dados que a operação de restauração cria.</span><span class="sxs-lookup"><span data-stu-id="2f905-154">Specifies the name of the new database that the restore operation creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f905-155">-TargetServerName</span><span class="sxs-lookup"><span data-stu-id="2f905-155">-TargetServerName</span></span>
<span data-ttu-id="2f905-156">Especifica o nome do servidor para o qual esse cmdlet restaura o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="2f905-156">Specifies the name of the server to which this cmdlet restores the database.</span></span>

<span data-ttu-id="2f905-157">No momento, o banco de dados SQL do Azure não é compatível com a restauração entre servidores.</span><span class="sxs-lookup"><span data-stu-id="2f905-157">Azure SQL Database does not currently support cross server restore.</span></span>
<span data-ttu-id="2f905-158">Os nomes dos servidores de origem e de destino devem ser iguais.</span><span class="sxs-lookup"><span data-stu-id="2f905-158">The source and target server names must be the same.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f905-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f905-159">CommonParameters</span></span>
<span data-ttu-id="2f905-160">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f905-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f905-161">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f905-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f905-162">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2f905-162">INPUTS</span></span>

### <span data-ttu-id="2f905-163">Microsoft. WindowsAzure. Commands. SQLDatabase. Services. Server. RestorableDroppedDatabase</span><span class="sxs-lookup"><span data-stu-id="2f905-163">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.RestorableDroppedDatabase</span></span>

### <span data-ttu-id="2f905-164">Microsoft. WindowsAzure. Commands. SQLDatabase. Services. Server. Database</span><span class="sxs-lookup"><span data-stu-id="2f905-164">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="2f905-165">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2f905-165">OUTPUTS</span></span>

### <span data-ttu-id="2f905-166">Microsoft. WindowsAzure. Commands. SQLDatabase. Services. Server. RestoreDatabaseOperation</span><span class="sxs-lookup"><span data-stu-id="2f905-166">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.RestoreDatabaseOperation</span></span>

## <span data-ttu-id="2f905-167">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2f905-167">NOTES</span></span>
* <span data-ttu-id="2f905-168">Você deve usar a autenticação baseada em certificado para executar esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2f905-168">You must use certificate based authentication to run this cmdlet.</span></span> <span data-ttu-id="2f905-169">Execute os seguintes comandos no computador onde executar este cmdlet:</span><span class="sxs-lookup"><span data-stu-id="2f905-169">Run the following commands on the computer where run this cmdlet:</span></span> 

`PS C:\\\> $subId = \<Subscription ID\>`
`PS C:\\\> $thumbprint = \<Certificate Thumbprint\>`
`PS C:\\\> $myCert = Get-Item Cert:\CurrentUser\My\$thumbprint`
`PS C:\\\> Set-AzureSubscription -SubscriptionName "mySubscription" -SubscriptionId $subId -Certificate $myCert`
`PS C:\\\> Select-AzureSubscription -SubscriptionName "mySubscription"`

## <span data-ttu-id="2f905-170">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2f905-170">RELATED LINKS</span></span>

[<span data-ttu-id="2f905-171">Banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="2f905-171">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="2f905-172">Criar solicitação de restauração de banco de dados</span><span class="sxs-lookup"><span data-stu-id="2f905-172">Create Database Restore Request</span></span>](https://msdn.microsoft.com/en-us/library/dn509571.aspx)

[<span data-ttu-id="2f905-173">Operações para bancos de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="2f905-173">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="2f905-174">Get-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="2f905-174">Get-AzureSqlDatabase</span></span>](./Get-AzureSqlDatabase.md)


