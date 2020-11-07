---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: CB601E21-424D-4B09-85E5-A4B2A5068267
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2b7674cb5b7abc489dc6aa6d3746f499b9686312
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946403"
---
# <span data-ttu-id="37540-101">Stop-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="37540-101">Stop-AzureSqlDatabaseCopy</span></span>

## <span data-ttu-id="37540-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="37540-102">SYNOPSIS</span></span>
<span data-ttu-id="37540-103">Finaliza uma relação de cópia contínua.</span><span class="sxs-lookup"><span data-stu-id="37540-103">Terminates a continuous copy relationship.</span></span>

## <span data-ttu-id="37540-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="37540-104">SYNTAX</span></span>

### <span data-ttu-id="37540-105">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="37540-105">ByInputObject</span></span>
```
Stop-AzureSqlDatabaseCopy -ServerName <String> -DatabaseCopy <DatabaseCopy> [-ForcedTermination] [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37540-106">ByDatabase</span><span class="sxs-lookup"><span data-stu-id="37540-106">ByDatabase</span></span>
```
Stop-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-ForcedTermination] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="37540-107">ByDatabaseName</span><span class="sxs-lookup"><span data-stu-id="37540-107">ByDatabaseName</span></span>
```
Stop-AzureSqlDatabaseCopy -ServerName <String> -DatabaseName <String> [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-ForcedTermination] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="37540-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="37540-108">DESCRIPTION</span></span>
<span data-ttu-id="37540-109">O cmdlet **Stop-AzureSqlDatabaseCopy** Finaliza uma relação de cópia contínua.</span><span class="sxs-lookup"><span data-stu-id="37540-109">The **Stop-AzureSqlDatabaseCopy** cmdlet terminates a continuous copy relationship.</span></span>
<span data-ttu-id="37540-110">Esse cmdlet interrompe a movimentação de dados entre o banco de dados de origem e o banco de dados secundário ou de destino e, em seguida, altera o estado do banco de dados secundário para ser um banco de dados online autônomo.</span><span class="sxs-lookup"><span data-stu-id="37540-110">This cmdlet stops the data movement between the source database and secondary or target database, and then changes the state of the secondary database to be a stand-alone online database.</span></span>

<span data-ttu-id="37540-111">Há duas maneiras de finalizar uma relação de cópia contínua, rescisão ou término planejado e rescisão forçado com possível perda de dados.</span><span class="sxs-lookup"><span data-stu-id="37540-111">There are two ways to end a continuous copy relationship, termination or planned termination and forced termination with possible data loss.</span></span>
<span data-ttu-id="37540-112">No servidor que hospeda o banco de dados de origem, você pode executar esse cmdlet no modo de término ou de término forçado.</span><span class="sxs-lookup"><span data-stu-id="37540-112">On the server that hosts the source database, you can run this cmdlet in termination or forced termination mode.</span></span>
<span data-ttu-id="37540-113">No servidor que hospeda o banco de dados secundário, você deve usar o modo de terminação forçado.</span><span class="sxs-lookup"><span data-stu-id="37540-113">On the server that hosts the secondary database, you must use forced termination mode.</span></span>

<span data-ttu-id="37540-114">Uma conclusão planejada aguarda até todas as transações confirmadas no banco de dados de origem, no momento em que você executar o cmdlet, foram duplicadas para o banco de dados secundário.</span><span class="sxs-lookup"><span data-stu-id="37540-114">A planned termination waits until all committed transactions on the source database, at the time that you run the cmdlet, have been replicated to the secondary database.</span></span>
<span data-ttu-id="37540-115">A rescisão forçada não aguarda a replicação de nenhuma transação confirmada pendente e pode causar possível perda de dados no banco de dados secundário.</span><span class="sxs-lookup"><span data-stu-id="37540-115">Forced termination does not wait for replication of any outstanding committed transactions, and can cause possible data loss in the secondary database.</span></span>

<span data-ttu-id="37540-116">Embora o status de replicação esteja pendente, somente a terminação forçada pode encerrar com êxito uma relação de cópia contínua.</span><span class="sxs-lookup"><span data-stu-id="37540-116">While replication status is PENDING, only forced termination can successfully end a continuous copy relationship.</span></span>
<span data-ttu-id="37540-117">Se o status de replicação estiver pendente, a rescisão não forçada não será aceita.</span><span class="sxs-lookup"><span data-stu-id="37540-117">If the replication status is PENDING, termination that is not forced is not supported.</span></span>

## <span data-ttu-id="37540-118">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="37540-118">EXAMPLES</span></span>

### <span data-ttu-id="37540-119">Exemplo 1: encerrar uma relação de cópia contínua</span><span class="sxs-lookup"><span data-stu-id="37540-119">Example 1: Terminate a continuous copy relationship</span></span>
```
PS C:\>Stop-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf658"
```

<span data-ttu-id="37540-120">Esse comando encerra a relação de cópia contínua do banco de dados chamado pedidos no servidor chamado lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="37540-120">This command terminates the continuous copy relationship of database named Orders on the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="37540-121">O servidor chamado bk0b8kf658 hospeda o banco de dados secundário.</span><span class="sxs-lookup"><span data-stu-id="37540-121">The server named bk0b8kf658 hosts the secondary database.</span></span>

### <span data-ttu-id="37540-122">Exemplo 2: finalizar forçosamente uma relação de cópia contínua</span><span class="sxs-lookup"><span data-stu-id="37540-122">Example 2: Forcibly terminate a continuous copy relationship</span></span>
```
PS C:\>$DatabaseCopy = Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders"
PS C:\> $DatabaseCopy | Stop-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -ForcedTermination
```

<span data-ttu-id="37540-123">O primeiro comando obtém a relação de cópia de banco de dados para o banco de dados chamado Orders no servidor chamado lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="37540-123">The first command gets the database copy relationship for the database named Orders on the server named lpqd0zbr8y.</span></span>

<span data-ttu-id="37540-124">O segundo comando finaliza forçosamente uma relação de cópia contínua do servidor que hospeda o banco de dados secundário.</span><span class="sxs-lookup"><span data-stu-id="37540-124">The second command forcibly terminates a continuous copy relationship from the server that hosts the secondary database.</span></span>

## <span data-ttu-id="37540-125">OS</span><span class="sxs-lookup"><span data-stu-id="37540-125">PARAMETERS</span></span>

### <span data-ttu-id="37540-126">-Banco de dados</span><span class="sxs-lookup"><span data-stu-id="37540-126">-Database</span></span>
<span data-ttu-id="37540-127">Especifica um objeto que representa o banco de dados SQL de origem do Azure.</span><span class="sxs-lookup"><span data-stu-id="37540-127">Specifies an object that represents the source Azure SQL Database.</span></span>
<span data-ttu-id="37540-128">Esse cmdlet termina a relação de cópia contínua do banco de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="37540-128">This cmdlet terminates the continuous copy relationship of the database that this parameter specifies.</span></span>

```yaml
Type: Database
Parameter Sets: ByDatabase
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="37540-129">-DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="37540-129">-DatabaseCopy</span></span>
<span data-ttu-id="37540-130">Especifica um objeto que representa um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="37540-130">Specifies an object that represents a database.</span></span>
<span data-ttu-id="37540-131">Esse cmdlet termina a relação de cópia contínua do banco de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="37540-131">This cmdlet terminates the continuous copy relationship of the database that this parameter specifies.</span></span>
<span data-ttu-id="37540-132">Esse parâmetro aceita entrada de pipeline.</span><span class="sxs-lookup"><span data-stu-id="37540-132">This parameter accepts pipeline input.</span></span>

```yaml
Type: DatabaseCopy
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="37540-133">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="37540-133">-DatabaseName</span></span>
<span data-ttu-id="37540-134">Especifica o nome de um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="37540-134">Specifies the name of a database.</span></span>
<span data-ttu-id="37540-135">Esse cmdlet termina a relação de cópia contínua do banco de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="37540-135">This cmdlet terminates the continuous copy relationship of the database that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37540-136">-Force</span><span class="sxs-lookup"><span data-stu-id="37540-136">-Force</span></span>
<span data-ttu-id="37540-137">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="37540-137">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37540-138">-ForcedTermination</span><span class="sxs-lookup"><span data-stu-id="37540-138">-ForcedTermination</span></span>
<span data-ttu-id="37540-139">Indica que esse cmdlet causa o encerramento forçado da relação de cópia contínua.</span><span class="sxs-lookup"><span data-stu-id="37540-139">Indicates that this cmdlet causes forced termination of the continuous copy relationship.</span></span>
<span data-ttu-id="37540-140">A rescisão forçada pode causar perda de dados.</span><span class="sxs-lookup"><span data-stu-id="37540-140">Forced termination may cause with data loss.</span></span>
<span data-ttu-id="37540-141">Para executar esse cmdlet em um servidor que hospeda o banco de dados de destino, você deve especificar esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="37540-141">To run this cmdlet on a server that hosts the target database, you must specify this parameter.</span></span>
<span data-ttu-id="37540-142">Para executar esse cmdlet em um servidor que hospeda o banco de dados de origem, se o banco de dados secundário estiver indisponível, você deve especificar esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="37540-142">To run this cmdlet on a server that hosts the source database, if the secondary database is unavailable, you must specify this parameter.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37540-143">-PartnerDatabase</span><span class="sxs-lookup"><span data-stu-id="37540-143">-PartnerDatabase</span></span>
<span data-ttu-id="37540-144">Especifica o nome do banco de dados secundário.</span><span class="sxs-lookup"><span data-stu-id="37540-144">Specifies name of the secondary database.</span></span>
<span data-ttu-id="37540-145">Se você especificar um nome, ele deve corresponder ao nome do banco de dados de origem.</span><span class="sxs-lookup"><span data-stu-id="37540-145">If you specify a name, it must match the name of the source database.</span></span>

```yaml
Type: String
Parameter Sets: ByDatabase, ByDatabaseName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37540-146">-PartnerServer</span><span class="sxs-lookup"><span data-stu-id="37540-146">-PartnerServer</span></span>
<span data-ttu-id="37540-147">Especifica o nome do servidor que hospeda o banco de dados de destino.</span><span class="sxs-lookup"><span data-stu-id="37540-147">Specifies the name of the server that hosts the target database.</span></span>

```yaml
Type: String
Parameter Sets: ByDatabase, ByDatabaseName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37540-148">-Perfil</span><span class="sxs-lookup"><span data-stu-id="37540-148">-Profile</span></span>
<span data-ttu-id="37540-149">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="37540-149">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="37540-150">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="37540-150">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="37540-151">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="37540-151">-ServerName</span></span>
<span data-ttu-id="37540-152">Especifica o nome do servidor no qual o banco de dados de origem reside.</span><span class="sxs-lookup"><span data-stu-id="37540-152">Specifies the name of the server on which the source database resides.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="37540-153">-Confirme</span><span class="sxs-lookup"><span data-stu-id="37540-153">-Confirm</span></span>
<span data-ttu-id="37540-154">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37540-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37540-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37540-155">-WhatIf</span></span>
<span data-ttu-id="37540-156">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="37540-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37540-157">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="37540-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37540-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37540-158">CommonParameters</span></span>
<span data-ttu-id="37540-159">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37540-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37540-160">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37540-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37540-161">SENSORES</span><span class="sxs-lookup"><span data-stu-id="37540-161">INPUTS</span></span>

### <span data-ttu-id="37540-162">Microsoft. WindowsAzure. Commands. SQLDatabase. Model. DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="37540-162">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span></span>

### <span data-ttu-id="37540-163">Microsoft. WindowsAzure. Commands. SQLDatabase. Services. Server. Database</span><span class="sxs-lookup"><span data-stu-id="37540-163">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="37540-164">EXIBE</span><span class="sxs-lookup"><span data-stu-id="37540-164">OUTPUTS</span></span>

### <span data-ttu-id="37540-165">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="37540-165">None</span></span>

## <span data-ttu-id="37540-166">INFORMA</span><span class="sxs-lookup"><span data-stu-id="37540-166">NOTES</span></span>
* <span data-ttu-id="37540-167">Autenticação: esse cmdlet requer autenticação baseada em certificado.</span><span class="sxs-lookup"><span data-stu-id="37540-167">Authentication: This cmdlet requires certificate-based authentication.</span></span> <span data-ttu-id="37540-168">Para obter um exemplo de como usar a autenticação baseada em certificado para definir a assinatura atual, consulte o cmdlet **New-AzureSqlDatabaseServerContext** .</span><span class="sxs-lookup"><span data-stu-id="37540-168">For an example of how to use certificate-based authentication to set the current subscription, see the **New-AzureSqlDatabaseServerContext** cmdlet.</span></span>
* <span data-ttu-id="37540-169">Restrições: no servidor que hospeda o banco de dados secundário, há suporte somente para encerramento forçado.</span><span class="sxs-lookup"><span data-stu-id="37540-169">Restrictions: On the server that hosts the secondary database, only forced termination is supported.</span></span>
* <span data-ttu-id="37540-170">Impacto da rescisão no antigo banco de dados secundário: após a rescisão, o banco de dados secundário se torna um banco de dados independente.</span><span class="sxs-lookup"><span data-stu-id="37540-170">Impact of termination on the former secondary database: After termination, the secondary database becomes an independent database.</span></span> <span data-ttu-id="37540-171">Se a propagação já estiver concluída no banco de dados secundário, após o término, este banco de dados está aberto para acesso total.</span><span class="sxs-lookup"><span data-stu-id="37540-171">If seeding already completed on the secondary database, after termination this database is open for full access.</span></span> <span data-ttu-id="37540-172">Se o banco de dados de origem for um banco de dados de leitura e gravação, o primeiro banco de dados secundário se tornará um banco de dados de leitura-gravação.</span><span class="sxs-lookup"><span data-stu-id="37540-172">If the source database is a read-write database, the former secondary database becomes a read-write database, too.</span></span>

  <span data-ttu-id="37540-173">Se a propagação estiver em andamento, a propagação será abortada, e o antigo banco de dados secundário nunca se tornará visível no servidor que hospeda o banco de dados secundário.</span><span class="sxs-lookup"><span data-stu-id="37540-173">If seeding is currently in progress, seeding is aborted, and the former secondary database never becomes visible on the server that hosts the secondary database.</span></span>

* <span data-ttu-id="37540-174">Você pode definir o banco de dados de origem como modo somente leitura.</span><span class="sxs-lookup"><span data-stu-id="37540-174">You can set the source database to read-only mode.</span></span> <span data-ttu-id="37540-175">Isso garante que os bancos de dados secundários e de origem sejam sincronizados após a rescisão e certifique-se de que nenhuma transação seja comprometida durante a rescisão.</span><span class="sxs-lookup"><span data-stu-id="37540-175">This guarantees that source and secondary databases are synchronized after termination, and makes sure that no transactions are committed during termination.</span></span> <span data-ttu-id="37540-176">Quando o encerramento terminar, defina a fonte de volta para o modo de leitura-gravação.</span><span class="sxs-lookup"><span data-stu-id="37540-176">Once the termination finishes, set the source back to read-write mode.</span></span> <span data-ttu-id="37540-177">Opcionalmente, você também pode definir o antigo banco de dados secundário para o modo de leitura-gravação.</span><span class="sxs-lookup"><span data-stu-id="37540-177">Optionally, you can also set the former secondary database to read-write mode.</span></span>
* <span data-ttu-id="37540-178">Monitoramento: para verificar o status das operações na origem e no destino da relação de cópia contínua, use o cmdlet **Get-AzureSqlDatabaseOperation** .</span><span class="sxs-lookup"><span data-stu-id="37540-178">Monitoring: To verify the status of the operations at both the source and target of the continuous copy relationship, use the **Get-AzureSqlDatabaseOperation** cmdlet.</span></span>

## <span data-ttu-id="37540-179">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="37540-179">RELATED LINKS</span></span>

[<span data-ttu-id="37540-180">Banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="37540-180">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="37540-181">Operações para bancos de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="37540-181">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="37540-182">Parar cópia do banco de dados</span><span class="sxs-lookup"><span data-stu-id="37540-182">Stop Database Copy</span></span>](https://msdn.microsoft.com/en-us/library/dn509573.aspx)

[<span data-ttu-id="37540-183">Cmdlets do banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="37540-183">Azure SQL Database Cmdlets</span></span>](./Azure.SQLDatabase.md)

[<span data-ttu-id="37540-184">Get-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="37540-184">Get-AzureSqlDatabaseCopy</span></span>](./Get-AzureSqlDatabaseCopy.md)

[<span data-ttu-id="37540-185">Start-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="37540-185">Start-AzureSqlDatabaseCopy</span></span>](./Start-AzureSqlDatabaseCopy.md)


