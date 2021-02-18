---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: CB601E21-424D-4B09-85E5-A4B2A5068267
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7716587787515221a6e016436a6e3d030c1ab0eb
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100405611"
---
# <span data-ttu-id="8b009-101">Stop-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="8b009-101">Stop-AzureSqlDatabaseCopy</span></span>

## <span data-ttu-id="8b009-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8b009-102">SYNOPSIS</span></span>
<span data-ttu-id="8b009-103">Termina uma relação de cópia contínua.</span><span class="sxs-lookup"><span data-stu-id="8b009-103">Terminates a continuous copy relationship.</span></span>

## <span data-ttu-id="8b009-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8b009-104">SYNTAX</span></span>

### <span data-ttu-id="8b009-105">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="8b009-105">ByInputObject</span></span>
```
Stop-AzureSqlDatabaseCopy -ServerName <String> -DatabaseCopy <DatabaseCopy> [-ForcedTermination] [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b009-106">ByDatabase</span><span class="sxs-lookup"><span data-stu-id="8b009-106">ByDatabase</span></span>
```
Stop-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-ForcedTermination] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8b009-107">ByDatabaseName</span><span class="sxs-lookup"><span data-stu-id="8b009-107">ByDatabaseName</span></span>
```
Stop-AzureSqlDatabaseCopy -ServerName <String> -DatabaseName <String> [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-ForcedTermination] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8b009-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="8b009-108">DESCRIPTION</span></span>
<span data-ttu-id="8b009-109">O cmdlet **Stop-AzureSqlDatabaseCopy** termina uma relação de cópia contínua.</span><span class="sxs-lookup"><span data-stu-id="8b009-109">The **Stop-AzureSqlDatabaseCopy** cmdlet terminates a continuous copy relationship.</span></span>
<span data-ttu-id="8b009-110">Esse cmdlet interrompe o movimento de dados entre o banco de dados de origem e o banco de dados secundário ou de destino e altera o estado do banco de dados secundário para ser um banco de dados online autônomo.</span><span class="sxs-lookup"><span data-stu-id="8b009-110">This cmdlet stops the data movement between the source database and secondary or target database, and then changes the state of the secondary database to be a stand-alone online database.</span></span>

<span data-ttu-id="8b009-111">Há duas maneiras de encerrar uma relação de cópia contínua, rescisão ou rescisão planejada e rescisão forçada com possível perda de dados.</span><span class="sxs-lookup"><span data-stu-id="8b009-111">There are two ways to end a continuous copy relationship, termination or planned termination and forced termination with possible data loss.</span></span>
<span data-ttu-id="8b009-112">No servidor que hospeda o banco de dados de origem, você pode executar esse cmdlet no modo de rescisão ou rescisão forçada.</span><span class="sxs-lookup"><span data-stu-id="8b009-112">On the server that hosts the source database, you can run this cmdlet in termination or forced termination mode.</span></span>
<span data-ttu-id="8b009-113">No servidor que hospeda o banco de dados secundário, você deve usar o modo de rescisão forçada.</span><span class="sxs-lookup"><span data-stu-id="8b009-113">On the server that hosts the secondary database, you must use forced termination mode.</span></span>

<span data-ttu-id="8b009-114">Uma rescisão planejada espera até que todas as transações comprometidas no banco de dados de origem, no momento em que você executar o cmdlet, tenham sido replicadas para o banco de dados secundário.</span><span class="sxs-lookup"><span data-stu-id="8b009-114">A planned termination waits until all committed transactions on the source database, at the time that you run the cmdlet, have been replicated to the secondary database.</span></span>
<span data-ttu-id="8b009-115">A rescisão forçada não espera a replicação de quaisquer transações pendentes comprometidas e pode causar uma possível perda de dados no banco de dados secundário.</span><span class="sxs-lookup"><span data-stu-id="8b009-115">Forced termination does not wait for replication of any outstanding committed transactions, and can cause possible data loss in the secondary database.</span></span>

<span data-ttu-id="8b009-116">Embora o status de replicação seja PENDENTE, somente a rescisão forçada pode encerrar com êxito uma relação de cópia contínua.</span><span class="sxs-lookup"><span data-stu-id="8b009-116">While replication status is PENDING, only forced termination can successfully end a continuous copy relationship.</span></span>
<span data-ttu-id="8b009-117">Se o status de replicação estiver PENDENTE, não há suporte para rescisão forçada.</span><span class="sxs-lookup"><span data-stu-id="8b009-117">If the replication status is PENDING, termination that is not forced is not supported.</span></span>

## <span data-ttu-id="8b009-118">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8b009-118">EXAMPLES</span></span>

### <span data-ttu-id="8b009-119">Exemplo 1: Encerrar uma relação de cópia contínua</span><span class="sxs-lookup"><span data-stu-id="8b009-119">Example 1: Terminate a continuous copy relationship</span></span>
```
PS C:\>Stop-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf658"
```

<span data-ttu-id="8b009-120">Esse comando encerra a relação de cópia contínua do banco de dados chamado Pedidos no servidor chamado lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="8b009-120">This command terminates the continuous copy relationship of database named Orders on the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="8b009-121">O servidor chamado bk0b8kf658 hospeda o banco de dados secundário.</span><span class="sxs-lookup"><span data-stu-id="8b009-121">The server named bk0b8kf658 hosts the secondary database.</span></span>

### <span data-ttu-id="8b009-122">Exemplo 2: encerrar uma relação de cópia contínua</span><span class="sxs-lookup"><span data-stu-id="8b009-122">Example 2: Forcibly terminate a continuous copy relationship</span></span>
```
PS C:\>$DatabaseCopy = Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders"
PS C:\> $DatabaseCopy | Stop-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -ForcedTermination
```

<span data-ttu-id="8b009-123">O primeiro comando obtém a relação de cópia de banco de dados do banco de dados chamado Pedidos no servidor chamado lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="8b009-123">The first command gets the database copy relationship for the database named Orders on the server named lpqd0zbr8y.</span></span>

<span data-ttu-id="8b009-124">O segundo comando encerrará uma relação de cópia contínua do servidor que hospeda o banco de dados secundário.</span><span class="sxs-lookup"><span data-stu-id="8b009-124">The second command forcibly terminates a continuous copy relationship from the server that hosts the secondary database.</span></span>

## <span data-ttu-id="8b009-125">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8b009-125">PARAMETERS</span></span>

### <span data-ttu-id="8b009-126">-Banco de dados</span><span class="sxs-lookup"><span data-stu-id="8b009-126">-Database</span></span>
<span data-ttu-id="8b009-127">Especifica um objeto que representa o banco de dados SQL do Azure de origem.</span><span class="sxs-lookup"><span data-stu-id="8b009-127">Specifies an object that represents the source Azure SQL Database.</span></span>
<span data-ttu-id="8b009-128">Este cmdlet encerra a relação de cópia contínua do banco de dados especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="8b009-128">This cmdlet terminates the continuous copy relationship of the database that this parameter specifies.</span></span>

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

### <span data-ttu-id="8b009-129">-DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="8b009-129">-DatabaseCopy</span></span>
<span data-ttu-id="8b009-130">Especifica um objeto que representa um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="8b009-130">Specifies an object that represents a database.</span></span>
<span data-ttu-id="8b009-131">Este cmdlet encerra a relação de cópia contínua do banco de dados especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="8b009-131">This cmdlet terminates the continuous copy relationship of the database that this parameter specifies.</span></span>
<span data-ttu-id="8b009-132">Este parâmetro aceita a entrada de pipeline.</span><span class="sxs-lookup"><span data-stu-id="8b009-132">This parameter accepts pipeline input.</span></span>

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

### <span data-ttu-id="8b009-133">-Nomedo Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="8b009-133">-DatabaseName</span></span>
<span data-ttu-id="8b009-134">Especifica o nome de um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="8b009-134">Specifies the name of a database.</span></span>
<span data-ttu-id="8b009-135">Este cmdlet encerra a relação de cópia contínua do banco de dados especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="8b009-135">This cmdlet terminates the continuous copy relationship of the database that this parameter specifies.</span></span>

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

### <span data-ttu-id="8b009-136">-Forçar</span><span class="sxs-lookup"><span data-stu-id="8b009-136">-Force</span></span>
<span data-ttu-id="8b009-137">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="8b009-137">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8b009-138">-ForcedTermination</span><span class="sxs-lookup"><span data-stu-id="8b009-138">-ForcedTermination</span></span>
<span data-ttu-id="8b009-139">Indica que esse cmdlet causa rescisão forçada da relação de cópia contínua.</span><span class="sxs-lookup"><span data-stu-id="8b009-139">Indicates that this cmdlet causes forced termination of the continuous copy relationship.</span></span>
<span data-ttu-id="8b009-140">A rescisão forçada pode causar perda de dados.</span><span class="sxs-lookup"><span data-stu-id="8b009-140">Forced termination may cause with data loss.</span></span>
<span data-ttu-id="8b009-141">Para executar esse cmdlet em um servidor que hospeda o banco de dados de destino, você deve especificar esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="8b009-141">To run this cmdlet on a server that hosts the target database, you must specify this parameter.</span></span>
<span data-ttu-id="8b009-142">Para executar esse cmdlet em um servidor que hospeda o banco de dados de origem, se o banco de dados secundário não estiver disponível, especifique esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="8b009-142">To run this cmdlet on a server that hosts the source database, if the secondary database is unavailable, you must specify this parameter.</span></span>

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

### <span data-ttu-id="8b009-143">-PartnerDatabase</span><span class="sxs-lookup"><span data-stu-id="8b009-143">-PartnerDatabase</span></span>
<span data-ttu-id="8b009-144">Especifica o nome do banco de dados secundário.</span><span class="sxs-lookup"><span data-stu-id="8b009-144">Specifies name of the secondary database.</span></span>
<span data-ttu-id="8b009-145">Se você especificar um nome, ele deverá corresponder ao nome do banco de dados de origem.</span><span class="sxs-lookup"><span data-stu-id="8b009-145">If you specify a name, it must match the name of the source database.</span></span>

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

### <span data-ttu-id="8b009-146">-PartnerServer</span><span class="sxs-lookup"><span data-stu-id="8b009-146">-PartnerServer</span></span>
<span data-ttu-id="8b009-147">Especifica o nome do servidor que hospeda o banco de dados de destino.</span><span class="sxs-lookup"><span data-stu-id="8b009-147">Specifies the name of the server that hosts the target database.</span></span>

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

### <span data-ttu-id="8b009-148">-Perfil</span><span class="sxs-lookup"><span data-stu-id="8b009-148">-Profile</span></span>
<span data-ttu-id="8b009-149">Especifica o perfil do Azure do qual este cmdlet é lido.</span><span class="sxs-lookup"><span data-stu-id="8b009-149">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8b009-150">Se você não especificar um perfil, esse cmdlet será lido do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="8b009-150">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8b009-151">-ServerName</span><span class="sxs-lookup"><span data-stu-id="8b009-151">-ServerName</span></span>
<span data-ttu-id="8b009-152">Especifica o nome do servidor no qual o banco de dados de origem reside.</span><span class="sxs-lookup"><span data-stu-id="8b009-152">Specifies the name of the server on which the source database resides.</span></span>

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

### <span data-ttu-id="8b009-153">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="8b009-153">-Confirm</span></span>
<span data-ttu-id="8b009-154">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b009-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b009-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b009-155">-WhatIf</span></span>
<span data-ttu-id="8b009-156">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="8b009-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b009-157">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8b009-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b009-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b009-158">CommonParameters</span></span>
<span data-ttu-id="8b009-159">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b009-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b009-160">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b009-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b009-161">Entradas</span><span class="sxs-lookup"><span data-stu-id="8b009-161">INPUTS</span></span>

### <span data-ttu-id="8b009-162">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="8b009-162">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span></span>

### <span data-ttu-id="8b009-163">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span><span class="sxs-lookup"><span data-stu-id="8b009-163">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="8b009-164">Saídas</span><span class="sxs-lookup"><span data-stu-id="8b009-164">OUTPUTS</span></span>

### <span data-ttu-id="8b009-165">Nenhum</span><span class="sxs-lookup"><span data-stu-id="8b009-165">None</span></span>

## <span data-ttu-id="8b009-166">Notas</span><span class="sxs-lookup"><span data-stu-id="8b009-166">NOTES</span></span>
* <span data-ttu-id="8b009-167">Autenticação: esse cmdlet requer autenticação baseada em certificado.</span><span class="sxs-lookup"><span data-stu-id="8b009-167">Authentication: This cmdlet requires certificate-based authentication.</span></span> <span data-ttu-id="8b009-168">Para ver um exemplo de como usar a autenticação baseada em certificado para definir a assinatura atual, consulte o cmdlet **New-AzureSqlDatabaseServerContext.**</span><span class="sxs-lookup"><span data-stu-id="8b009-168">For an example of how to use certificate-based authentication to set the current subscription, see the **New-AzureSqlDatabaseServerContext** cmdlet.</span></span>
* <span data-ttu-id="8b009-169">Restrições: no servidor que hospeda o banco de dados secundário, há suporte apenas para rescisão forçada.</span><span class="sxs-lookup"><span data-stu-id="8b009-169">Restrictions: On the server that hosts the secondary database, only forced termination is supported.</span></span>
* <span data-ttu-id="8b009-170">Impacto da rescisão no antigo banco de dados secundário: após a rescisão, o banco de dados secundário torna-se um banco de dados independente.</span><span class="sxs-lookup"><span data-stu-id="8b009-170">Impact of termination on the former secondary database: After termination, the secondary database becomes an independent database.</span></span> <span data-ttu-id="8b009-171">Se a semeação já tiver sido concluída no banco de dados secundário, após a rescisão, esse banco de dados será aberto para acesso total.</span><span class="sxs-lookup"><span data-stu-id="8b009-171">If seeding already completed on the secondary database, after termination this database is open for full access.</span></span> <span data-ttu-id="8b009-172">Se o banco de dados de origem for um banco de dados de leitura-gravação, o antigo banco de dados secundário também se tornará um banco de dados de leitura-gravação.</span><span class="sxs-lookup"><span data-stu-id="8b009-172">If the source database is a read-write database, the former secondary database becomes a read-write database, too.</span></span>

  <span data-ttu-id="8b009-173">Se o semeamento estiver em andamento, a semeação será cancelada e o antigo banco de dados secundário nunca ficará visível no servidor que hospeda o banco de dados secundário.</span><span class="sxs-lookup"><span data-stu-id="8b009-173">If seeding is currently in progress, seeding is aborted, and the former secondary database never becomes visible on the server that hosts the secondary database.</span></span>

* <span data-ttu-id="8b009-174">Você pode definir o banco de dados de origem para o modo somente leitura.</span><span class="sxs-lookup"><span data-stu-id="8b009-174">You can set the source database to read-only mode.</span></span> <span data-ttu-id="8b009-175">Isso garante que os bancos de dados de origem e secundários sejam sincronizados após a rescisão e garante que nenhuma transação seja comprometida durante a rescisão.</span><span class="sxs-lookup"><span data-stu-id="8b009-175">This guarantees that source and secondary databases are synchronized after termination, and makes sure that no transactions are committed during termination.</span></span> <span data-ttu-id="8b009-176">Quando a rescisão terminar, de definir a origem de volta para o modo de leitura e gravação.</span><span class="sxs-lookup"><span data-stu-id="8b009-176">Once the termination finishes, set the source back to read-write mode.</span></span> <span data-ttu-id="8b009-177">Opcionalmente, você também pode definir o antigo banco de dados secundário para o modo de leitura-gravação.</span><span class="sxs-lookup"><span data-stu-id="8b009-177">Optionally, you can also set the former secondary database to read-write mode.</span></span>
* <span data-ttu-id="8b009-178">Monitoramento: para verificar o status das operações na origem e no destino da relação de cópia contínua, use o cmdlet **Get-AzureSqlDatabaseOperation.**</span><span class="sxs-lookup"><span data-stu-id="8b009-178">Monitoring: To verify the status of the operations at both the source and target of the continuous copy relationship, use the **Get-AzureSqlDatabaseOperation** cmdlet.</span></span>

## <span data-ttu-id="8b009-179">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8b009-179">RELATED LINKS</span></span>

[<span data-ttu-id="8b009-180">Banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="8b009-180">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="8b009-181">Operações para bancos de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="8b009-181">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="8b009-182">Parar Cópia do Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="8b009-182">Stop Database Copy</span></span>](https://msdn.microsoft.com/en-us/library/dn509573.aspx)



[<span data-ttu-id="8b009-183">Get-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="8b009-183">Get-AzureSqlDatabaseCopy</span></span>](./Get-AzureSqlDatabaseCopy.md)

[<span data-ttu-id="8b009-184">Start-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="8b009-184">Start-AzureSqlDatabaseCopy</span></span>](./Start-AzureSqlDatabaseCopy.md)


