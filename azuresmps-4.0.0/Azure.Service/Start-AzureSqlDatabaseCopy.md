---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B7F07494-FBCA-4A77-92BF-E0A2D7ACCD21
online version: ''
schema: 2.0.0
ms.openlocfilehash: fc350cdf117ebbf72b023f64895f4c563e73566b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945845"
---
# <span data-ttu-id="879e8-101">Start-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="879e8-101">Start-AzureSqlDatabaseCopy</span></span>

## <span data-ttu-id="879e8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="879e8-102">SYNOPSIS</span></span>
<span data-ttu-id="879e8-103">Inicia uma operação de cópia de um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="879e8-103">Starts a copy operation of an Azure SQL Database.</span></span>

## <span data-ttu-id="879e8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="879e8-104">SYNTAX</span></span>

### <span data-ttu-id="879e8-105">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="879e8-105">ByInputObject</span></span>
```
Start-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> [-PartnerServer <String>]
 -PartnerDatabase <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="879e8-106">ByInputObjectContinuous</span><span class="sxs-lookup"><span data-stu-id="879e8-106">ByInputObjectContinuous</span></span>
```
Start-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> -PartnerServer <String>
 [-PartnerDatabase <String>] [-ContinuousCopy] [-OfflineSecondary] [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="879e8-107">ByDatabaseName</span><span class="sxs-lookup"><span data-stu-id="879e8-107">ByDatabaseName</span></span>
```
Start-AzureSqlDatabaseCopy -ServerName <String> -DatabaseName <String> [-PartnerServer <String>]
 -PartnerDatabase <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="879e8-108">ByDatabaseNameContinuous</span><span class="sxs-lookup"><span data-stu-id="879e8-108">ByDatabaseNameContinuous</span></span>
```
Start-AzureSqlDatabaseCopy -ServerName <String> -DatabaseName <String> -PartnerServer <String>
 [-PartnerDatabase <String>] [-ContinuousCopy] [-OfflineSecondary] [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="879e8-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="879e8-109">DESCRIPTION</span></span>
<span data-ttu-id="879e8-110">O cmdlet **Start-AzureSqlDatabaseCopy** inicia uma operação única de cópia ou uma operação de cópia contínua de um banco de dados SQL específico do Azure.</span><span class="sxs-lookup"><span data-stu-id="879e8-110">The **Start-AzureSqlDatabaseCopy** cmdlet starts a one-time copy operation or a continuous copy operation of a specific Azure SQL Database.</span></span>
<span data-ttu-id="879e8-111">Este cmdlet não é Transactional.</span><span class="sxs-lookup"><span data-stu-id="879e8-111">This cmdlet is not transactional.</span></span>

<span data-ttu-id="879e8-112">O banco de dados original é o banco de dados de origem.</span><span class="sxs-lookup"><span data-stu-id="879e8-112">The original database is the source database.</span></span>
<span data-ttu-id="879e8-113">A cópia é o banco de dados secundário ou de destino.</span><span class="sxs-lookup"><span data-stu-id="879e8-113">The copy is the secondary or target database.</span></span>
<span data-ttu-id="879e8-114">Para uma cópia contínua, os bancos de dados de origem e de destino não podem residir no mesmo servidor e os servidores que hospedam os bancos de dados de origem e de destino devem fazer parte da mesma assinatura.</span><span class="sxs-lookup"><span data-stu-id="879e8-114">For a continuous copy, the source and target databases cannot reside on the same server, and the servers that host the source and target databases must be part of the same subscription.</span></span>

<span data-ttu-id="879e8-115">Se você não especificar o parâmetro *ContinuousCopy* , esse cmdlet criará uma cópia única do banco de dados de origem.</span><span class="sxs-lookup"><span data-stu-id="879e8-115">If you do not specify the *ContinuousCopy* parameter, this cmdlet creates a one-time copy of the source database.</span></span>
<span data-ttu-id="879e8-116">Quando a resposta é recebida, a operação ainda pode estar em andamento.</span><span class="sxs-lookup"><span data-stu-id="879e8-116">When the response is received, the operation can still be in progress.</span></span>
<span data-ttu-id="879e8-117">Você pode monitorar a operação usando o cmdlet Get-AzureSqlDatabaseCopy ou Get-AzureSqlDatabaseOperation.</span><span class="sxs-lookup"><span data-stu-id="879e8-117">You can monitor the operation by using the Get-AzureSqlDatabaseCopy or Get-AzureSqlDatabaseOperation cmdlet.</span></span>

<span data-ttu-id="879e8-118">Se você especificar *ContinuousCopy* , esse cmdlet criará uma cópia contínua do banco de dados de origem.</span><span class="sxs-lookup"><span data-stu-id="879e8-118">If you specify *ContinuousCopy* , this cmdlet creates a continuous copy of the source database.</span></span>
<span data-ttu-id="879e8-119">Quando a resposta é recebida, a operação estará em andamento.</span><span class="sxs-lookup"><span data-stu-id="879e8-119">When the response is received, the operation will be in progress.</span></span>
<span data-ttu-id="879e8-120">Você pode monitorar a operação usando **Get-AzureSqlDatabaseCopy** ou **Get-AzureSqlDatabaseOperation**.</span><span class="sxs-lookup"><span data-stu-id="879e8-120">You can monitor the operation by using **Get-AzureSqlDatabaseCopy** or **Get-AzureSqlDatabaseOperation**.</span></span>

<span data-ttu-id="879e8-121">Você pode criar uma cópia contínua como um banco de dados online ou offline.</span><span class="sxs-lookup"><span data-stu-id="879e8-121">You can create a continuous copy as an online or offline database.</span></span>
<span data-ttu-id="879e8-122">A cópia contínua online é usada para configurar o Active Geo-Replication para o banco de dados SQL do Azure https://azure.microsoft.com/en-us/documentation/articles/sql-database-geo-replication-overview/ .</span><span class="sxs-lookup"><span data-stu-id="879e8-122">The online continuous copy is used to configure Active Geo-Replication for Azure SQL Databasehttps://azure.microsoft.com/en-us/documentation/articles/sql-database-geo-replication-overview/.</span></span>
<span data-ttu-id="879e8-123">A cópia contínua offline é usada para configurar o Geo-Replication padrão para o banco de dados SQL do Azure https://azure.microsoft.com/en-us/documentation/articles/sql-database-business-continuity-scenarios/ .</span><span class="sxs-lookup"><span data-stu-id="879e8-123">The offline continuous copy is used to configure Standard Geo-Replication for Azure SQL Databasehttps://azure.microsoft.com/en-us/documentation/articles/sql-database-business-continuity-scenarios/.</span></span>

## <span data-ttu-id="879e8-124">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="879e8-124">EXAMPLES</span></span>

### <span data-ttu-id="879e8-125">Exemplo 1: agendar uma cópia contínua do banco de dados</span><span class="sxs-lookup"><span data-stu-id="879e8-125">Example 1: Schedule a continuous database copy</span></span>
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf65" -ContinuousCopy
```

<span data-ttu-id="879e8-126">Esse comando agenda uma cópia contínua do banco de dados chamado Orders no servidor chamado lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="879e8-126">This command schedules a continuous copy of the database named Orders on the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="879e8-127">O comando cria um banco de dados de destino no servidor chamado bk0b8kf658.</span><span class="sxs-lookup"><span data-stu-id="879e8-127">The command creates a target database on the server named bk0b8kf658.</span></span>

### <span data-ttu-id="879e8-128">Exemplo 2: criar uma cópia única no mesmo servidor</span><span class="sxs-lookup"><span data-stu-id="879e8-128">Example 2: Create a one-time copy on the same server</span></span>
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerDatabase "OrdersCopy"
```

<span data-ttu-id="879e8-129">Esse comando cria uma cópia única do banco de dados chamada Orders no servidor chamado lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="879e8-129">This command creates a one-time copy of the database named Orders on the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="879e8-130">O comando cria uma cópia chamada OrdersCopy no mesmo servidor.</span><span class="sxs-lookup"><span data-stu-id="879e8-130">The command creates a copy named OrdersCopy on the same server.</span></span>

### <span data-ttu-id="879e8-131">Exemplo 3: agendar uma cópia contínua do banco de dados offline</span><span class="sxs-lookup"><span data-stu-id="879e8-131">Example 3: Schedule a continuous offline database copy</span></span>
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf65" -ContinuousCopy -OfflineSecondary
```

<span data-ttu-id="879e8-132">Esse comando agenda uma cópia contínua do banco de dados chamado Orders no servidor chamado lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="879e8-132">This command schedules a continuous copy of the database named Orders on the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="879e8-133">Esse comando cria um banco de dados de destino offline no servidor chamado bk0b8kf658.</span><span class="sxs-lookup"><span data-stu-id="879e8-133">This command creates an offline target database on the server named bk0b8kf658.</span></span>

## <span data-ttu-id="879e8-134">OS</span><span class="sxs-lookup"><span data-stu-id="879e8-134">PARAMETERS</span></span>

### <span data-ttu-id="879e8-135">-ContinuousCopy</span><span class="sxs-lookup"><span data-stu-id="879e8-135">-ContinuousCopy</span></span>
<span data-ttu-id="879e8-136">Indica que a cópia do banco de dados será uma cópia contínua (um banco de dados de réplica).</span><span class="sxs-lookup"><span data-stu-id="879e8-136">Indicates that the database copy will be a continuous-copy (a replica database).</span></span>
<span data-ttu-id="879e8-137">Não há suporte para cópia contínua no mesmo servidor.</span><span class="sxs-lookup"><span data-stu-id="879e8-137">Continuous copy is not supported within the same server.</span></span>
<span data-ttu-id="879e8-138">Se esse parâmetro não for especificado, será executada uma cópia única.</span><span class="sxs-lookup"><span data-stu-id="879e8-138">If this parameter is not specified, then a one-time copy is performed.</span></span>
<span data-ttu-id="879e8-139">Para uma cópia única, os bancos de dados de origem e parceiro devem estar no mesmo servidor.</span><span class="sxs-lookup"><span data-stu-id="879e8-139">For a one-time copy, the source and partner databases must be on the same server.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByInputObjectContinuous, ByDatabaseNameContinuous
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="879e8-140">-Banco de dados</span><span class="sxs-lookup"><span data-stu-id="879e8-140">-Database</span></span>
<span data-ttu-id="879e8-141">Especifica um objeto que representa o banco de dados SQL de origem do Azure.</span><span class="sxs-lookup"><span data-stu-id="879e8-141">Specifies an object that represents the source Azure SQL Database.</span></span>
<span data-ttu-id="879e8-142">Esse parâmetro aceita entrada de pipeline.</span><span class="sxs-lookup"><span data-stu-id="879e8-142">This parameter accepts pipeline input.</span></span>

```yaml
Type: Database
Parameter Sets: ByInputObject, ByInputObjectContinuous
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="879e8-143">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="879e8-143">-DatabaseName</span></span>
<span data-ttu-id="879e8-144">Especifica o nome do banco de dados de origem.</span><span class="sxs-lookup"><span data-stu-id="879e8-144">Specifies the name of the source database.</span></span>

```yaml
Type: String
Parameter Sets: ByDatabaseName, ByDatabaseNameContinuous
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="879e8-145">-Force</span><span class="sxs-lookup"><span data-stu-id="879e8-145">-Force</span></span>
<span data-ttu-id="879e8-146">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="879e8-146">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="879e8-147">-OfflineSecondary</span><span class="sxs-lookup"><span data-stu-id="879e8-147">-OfflineSecondary</span></span>
<span data-ttu-id="879e8-148">Especifica que uma cópia contínua é uma cópia passiva em vez de uma cópia ativa.</span><span class="sxs-lookup"><span data-stu-id="879e8-148">Specifies that a continuous copy is a passive copy rather than an active copy.</span></span>
<span data-ttu-id="879e8-149">Se o banco de dados de origem for um banco de dados de edição padrão, este parâmetro será necessário.</span><span class="sxs-lookup"><span data-stu-id="879e8-149">If the source database is a Standard edition database, then this parameter is required.</span></span>
<span data-ttu-id="879e8-150">Se esse parâmetro for especificado, *ContinuousCopy* também deverá ser especificado.</span><span class="sxs-lookup"><span data-stu-id="879e8-150">If this parameter is specified then *ContinuousCopy* must also be specified.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByInputObjectContinuous, ByDatabaseNameContinuous
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="879e8-151">-PartnerDatabase</span><span class="sxs-lookup"><span data-stu-id="879e8-151">-PartnerDatabase</span></span>
<span data-ttu-id="879e8-152">Especifica o nome do banco de dados de destino.</span><span class="sxs-lookup"><span data-stu-id="879e8-152">Specifies name of the target database.</span></span>
<span data-ttu-id="879e8-153">Se você especificar o parâmetro *ContinuousCopy* , o valor de *PartnerDatabase* deverá coincidir com o nome do banco de dados de origem.</span><span class="sxs-lookup"><span data-stu-id="879e8-153">If you specify the *ContinuousCopy* parameter, the value for *PartnerDatabase* must match the name of the source database.</span></span>
<span data-ttu-id="879e8-154">Se você não especificar *ContinuousCopy* , deverá especificar um nome para o banco de dados de destino, que pode ser diferente do nome do banco de dados de origem.</span><span class="sxs-lookup"><span data-stu-id="879e8-154">If you do not specify *ContinuousCopy* , you must specify a name for the target database, which can be different from the source database name.</span></span>

```yaml
Type: String
Parameter Sets: ByInputObject, ByDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByInputObjectContinuous, ByDatabaseNameContinuous
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="879e8-155">-PartnerServer</span><span class="sxs-lookup"><span data-stu-id="879e8-155">-PartnerServer</span></span>
<span data-ttu-id="879e8-156">Especifica o nome do servidor que hospeda o banco de dados de destino.</span><span class="sxs-lookup"><span data-stu-id="879e8-156">Specifies the name of the server that hosts the target database.</span></span>
<span data-ttu-id="879e8-157">Esse servidor deve estar na mesma assinatura do Azure que o servidor de banco de dados de origem.</span><span class="sxs-lookup"><span data-stu-id="879e8-157">This server must be in the same Azure subscription as the source database server.</span></span>

```yaml
Type: String
Parameter Sets: ByInputObject, ByDatabaseName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByInputObjectContinuous, ByDatabaseNameContinuous
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="879e8-158">-Perfil</span><span class="sxs-lookup"><span data-stu-id="879e8-158">-Profile</span></span>
<span data-ttu-id="879e8-159">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="879e8-159">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="879e8-160">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="879e8-160">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="879e8-161">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="879e8-161">-ServerName</span></span>
<span data-ttu-id="879e8-162">Especifica o nome do servidor no qual o banco de dados de origem reside.</span><span class="sxs-lookup"><span data-stu-id="879e8-162">Specifies the name of the server on which the source database resides.</span></span>

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

### <span data-ttu-id="879e8-163">-Confirme</span><span class="sxs-lookup"><span data-stu-id="879e8-163">-Confirm</span></span>
<span data-ttu-id="879e8-164">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="879e8-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="879e8-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="879e8-165">-WhatIf</span></span>
<span data-ttu-id="879e8-166">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="879e8-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="879e8-167">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="879e8-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="879e8-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="879e8-168">CommonParameters</span></span>
<span data-ttu-id="879e8-169">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="879e8-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="879e8-170">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="879e8-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="879e8-171">SENSORES</span><span class="sxs-lookup"><span data-stu-id="879e8-171">INPUTS</span></span>

### <span data-ttu-id="879e8-172">Microsoft. WindowsAzure. Commands. SQLDatabase. Services. Server. Database</span><span class="sxs-lookup"><span data-stu-id="879e8-172">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="879e8-173">EXIBE</span><span class="sxs-lookup"><span data-stu-id="879e8-173">OUTPUTS</span></span>

### <span data-ttu-id="879e8-174">Microsoft. WindowsAzure. Commands. SQLDatabase. Model. DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="879e8-174">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span></span>

## <span data-ttu-id="879e8-175">INFORMA</span><span class="sxs-lookup"><span data-stu-id="879e8-175">NOTES</span></span>
* <span data-ttu-id="879e8-176">Autenticação: esse cmdlet requer autenticação baseada em certificado.</span><span class="sxs-lookup"><span data-stu-id="879e8-176">Authentication: This cmdlet requires certificate-based authentication.</span></span> <span data-ttu-id="879e8-177">Para obter um exemplo de como usar a autenticação baseada em certificado para definir a assinatura atual, consulte New-AzureSqlDatabaseServerContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="879e8-177">For an example of how to use certificate-based authentication to set the current subscription, see New-AzureSqlDatabaseServerContext cmdlet.</span></span>
* <span data-ttu-id="879e8-178">Monitoramento: para verificar o status de uma ou mais relações de cópia contínua ativas no servidor, use o cmdlet **Get-AzureSqlDatabaseCopy** .</span><span class="sxs-lookup"><span data-stu-id="879e8-178">Monitoring: To check for the status of one or more continuous copy relationships that are active on the server, use the **Get-AzureSqlDatabaseCopy** cmdlet.</span></span> <span data-ttu-id="879e8-179">Para verificar o status das operações na origem e no destino da relação de cópia contínua, use o cmdlet **Get-AzureSqlDatabaseOperation** .</span><span class="sxs-lookup"><span data-stu-id="879e8-179">To verify the status of the operations at both the source and target of the continuous copy relationship, use the **Get-AzureSqlDatabaseOperation** cmdlet.</span></span>

## <span data-ttu-id="879e8-180">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="879e8-180">RELATED LINKS</span></span>

[<span data-ttu-id="879e8-181">Banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="879e8-181">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="879e8-182">Operações para bancos de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="879e8-182">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="879e8-183">Iniciar cópia de banco de dados</span><span class="sxs-lookup"><span data-stu-id="879e8-183">Start Database Copy</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn509576.aspx)

[<span data-ttu-id="879e8-184">Cmdlets do banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="879e8-184">Azure SQL Database Cmdlets</span></span>](./Azure.SQLDatabase.md)

[<span data-ttu-id="879e8-185">Get-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="879e8-185">Get-AzureSqlDatabaseCopy</span></span>](./Get-AzureSqlDatabaseCopy.md)

[<span data-ttu-id="879e8-186">Parar-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="879e8-186">Stop-AzureSqlDatabaseCopy</span></span>](./Stop-AzureSqlDatabaseCopy.md)


