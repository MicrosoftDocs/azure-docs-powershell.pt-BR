---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 5AEF7D44-624D-4794-86FF-156E6729BB56
online version: ''
schema: 2.0.0
ms.openlocfilehash: f8752766572975ef97094a3915446086c903a7fd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946295"
---
# <span data-ttu-id="502f2-101">Get-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="502f2-101">Get-AzureSqlDatabaseCopy</span></span>

## <span data-ttu-id="502f2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="502f2-102">SYNOPSIS</span></span>
<span data-ttu-id="502f2-103">Verifica o status das relações de cópia.</span><span class="sxs-lookup"><span data-stu-id="502f2-103">Checks the status of copy relationships.</span></span>

## <span data-ttu-id="502f2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="502f2-104">SYNTAX</span></span>

### <span data-ttu-id="502f2-105">ByServerNameOnly (padrão)</span><span class="sxs-lookup"><span data-stu-id="502f2-105">ByServerNameOnly (Default)</span></span>
```
Get-AzureSqlDatabaseCopy -ServerName <String> [-DatabaseName <String>] [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="502f2-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="502f2-106">ByInputObject</span></span>
```
Get-AzureSqlDatabaseCopy -ServerName <String> -DatabaseCopy <DatabaseCopy> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="502f2-107">ByDatabase</span><span class="sxs-lookup"><span data-stu-id="502f2-107">ByDatabase</span></span>
```
Get-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="502f2-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="502f2-108">DESCRIPTION</span></span>
<span data-ttu-id="502f2-109">O cmdlet **Get-AzureSqlDatabaseCopy** verifica o status de uma ou mais relações de cópia ativas.</span><span class="sxs-lookup"><span data-stu-id="502f2-109">The **Get-AzureSqlDatabaseCopy** cmdlet checks the status of one or more active copy relationships.</span></span>
<span data-ttu-id="502f2-110">Execute este cmdlet depois de executar o cmdlet Start-AzureSqlDatabaseCopy ou Stop-AzureSqlDatabaseCopy.</span><span class="sxs-lookup"><span data-stu-id="502f2-110">Run this cmdlet after you run the Start-AzureSqlDatabaseCopy or Stop-AzureSqlDatabaseCopy cmdlet.</span></span>
<span data-ttu-id="502f2-111">Você pode verificar uma relação de cópia específica, todas as relações de cópia ou uma lista filtrada de relações de cópia, como todas as cópias em um servidor de destino específico.</span><span class="sxs-lookup"><span data-stu-id="502f2-111">You can check a specific copy relationship, all copy relationships, or a filtered list of copy relationships, such as all copies on a specific target server.</span></span>
<span data-ttu-id="502f2-112">Você pode executar esse cmdlet no servidor que hospeda o banco de dados de origem ou de destino.</span><span class="sxs-lookup"><span data-stu-id="502f2-112">You can run this cmdlet on the server that hosts the source or target database.</span></span>

<span data-ttu-id="502f2-113">Este cmdlet é síncrono.</span><span class="sxs-lookup"><span data-stu-id="502f2-113">This cmdlet is synchronous.</span></span>
<span data-ttu-id="502f2-114">O cmdlet bloqueia o console do PowerShell do Azure até que ele retorne um objeto de status.</span><span class="sxs-lookup"><span data-stu-id="502f2-114">The cmdlet blocks the Azure PowerShell console until it returns a status object.</span></span>

<span data-ttu-id="502f2-115">Os parâmetros *PartnerServer* e *PartnerDatabase* são opcionais.</span><span class="sxs-lookup"><span data-stu-id="502f2-115">The *PartnerServer* and *PartnerDatabase* parameters are optional.</span></span>
<span data-ttu-id="502f2-116">Se você não especificar nenhum dos parâmetros, esse cmdlet retornará uma tabela de resultados.</span><span class="sxs-lookup"><span data-stu-id="502f2-116">If you do not specify either parameter, this cmdlet returns a table of results.</span></span>
<span data-ttu-id="502f2-117">Para ver o status de apenas um banco de dados específico, especifique ambos os parâmetros.</span><span class="sxs-lookup"><span data-stu-id="502f2-117">To see the status for only a particular database, specify both parameters.</span></span>

## <span data-ttu-id="502f2-118">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="502f2-118">EXAMPLES</span></span>

### <span data-ttu-id="502f2-119">Exemplo 1: obter o status da cópia de um banco de dados</span><span class="sxs-lookup"><span data-stu-id="502f2-119">Example 1: Get the copy status of a database</span></span>
```
PS C:\> Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf658"
```

<span data-ttu-id="502f2-120">Esse comando obtém o status do banco de dados chamado pedidos no servidor chamado lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="502f2-120">This command gets the status of the database named Orders on the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="502f2-121">O parâmetro *PartnerServer* restringe esse comando para o servidor bk0b8kf658.</span><span class="sxs-lookup"><span data-stu-id="502f2-121">The *PartnerServer* parameter restricts this command to the bk0b8kf658 server.</span></span>

### <span data-ttu-id="502f2-122">Exemplo 2: obter o status de todas as cópias em um serverGet o status de todas as cópias em um servidor</span><span class="sxs-lookup"><span data-stu-id="502f2-122">Example 2: Get the status of all copies on a serverGet the status of all copies on a server</span></span>
```
PS C:\> Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y"
```

<span data-ttu-id="502f2-123">Esse comando obtém o status de todas as cópias ativas no servidor chamado lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="502f2-123">This command gets the status of all active copies on the server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="502f2-124">OS</span><span class="sxs-lookup"><span data-stu-id="502f2-124">PARAMETERS</span></span>

### <span data-ttu-id="502f2-125">-Banco de dados</span><span class="sxs-lookup"><span data-stu-id="502f2-125">-Database</span></span>
<span data-ttu-id="502f2-126">Especifica um objeto que representa o banco de dados SQL de origem do Azure.</span><span class="sxs-lookup"><span data-stu-id="502f2-126">Specifies an object that represents the source Azure SQL Database.</span></span>
<span data-ttu-id="502f2-127">Esse cmdlet obtém o status da cópia do banco de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="502f2-127">This cmdlet gets the copy status of the database that this parameter specifies.</span></span>

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

### <span data-ttu-id="502f2-128">-DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="502f2-128">-DatabaseCopy</span></span>
<span data-ttu-id="502f2-129">Especifica um objeto que representa um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="502f2-129">Specifies an object that represents a database.</span></span>
<span data-ttu-id="502f2-130">Esse cmdlet obtém o status da cópia do banco de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="502f2-130">This cmdlet gets the copy status of the database that this parameter specifies.</span></span>
<span data-ttu-id="502f2-131">Esse parâmetro aceita entrada de pipeline.</span><span class="sxs-lookup"><span data-stu-id="502f2-131">This parameter accepts pipeline input.</span></span>

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

### <span data-ttu-id="502f2-132">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="502f2-132">-DatabaseName</span></span>
<span data-ttu-id="502f2-133">Especifica o nome do banco de dados de origem.</span><span class="sxs-lookup"><span data-stu-id="502f2-133">Specifies the name of the source database.</span></span>
<span data-ttu-id="502f2-134">Esse cmdlet obtém o status da cópia do banco de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="502f2-134">This cmdlet gets that copy status of the database that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByServerNameOnly
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="502f2-135">-PartnerDatabase</span><span class="sxs-lookup"><span data-stu-id="502f2-135">-PartnerDatabase</span></span>
<span data-ttu-id="502f2-136">Especifica o nome do banco de dados secundário.</span><span class="sxs-lookup"><span data-stu-id="502f2-136">Specifies name of the secondary database.</span></span>
<span data-ttu-id="502f2-137">Se esse banco de dados não for encontrado no modo de exibição de gerenciamento dinâmico sys.dm_database_copies, esse cmdlet retornará um objeto de status vazio.</span><span class="sxs-lookup"><span data-stu-id="502f2-137">If this database is not found in the sys.dm_database_copies dynamic management view, this cmdlet returns an empty status object.</span></span>

```yaml
Type: String
Parameter Sets: ByServerNameOnly, ByDatabase
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="502f2-138">-PartnerServer</span><span class="sxs-lookup"><span data-stu-id="502f2-138">-PartnerServer</span></span>
<span data-ttu-id="502f2-139">Especifica o nome do servidor que hospeda o banco de dados de destino.</span><span class="sxs-lookup"><span data-stu-id="502f2-139">Specifies the name of the server that hosts the target database.</span></span>
<span data-ttu-id="502f2-140">Se esse servidor não for encontrado no modo de exibição de gerenciamento dinâmico sys.dm_database_copies, esse cmdlet retornará um objeto de status vazio.</span><span class="sxs-lookup"><span data-stu-id="502f2-140">If this server is not found in the sys.dm_database_copies dynamic management view, this cmdlet returns an empty status object.</span></span>

```yaml
Type: String
Parameter Sets: ByServerNameOnly, ByDatabase
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="502f2-141">-Perfil</span><span class="sxs-lookup"><span data-stu-id="502f2-141">-Profile</span></span>
<span data-ttu-id="502f2-142">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="502f2-142">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="502f2-143">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="502f2-143">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="502f2-144">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="502f2-144">-ServerName</span></span>
<span data-ttu-id="502f2-145">Especifica o nome do servidor no qual a cópia do banco de dados reside.</span><span class="sxs-lookup"><span data-stu-id="502f2-145">Specifies the name of the server on which the database copy resides.</span></span>

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

### <span data-ttu-id="502f2-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="502f2-146">CommonParameters</span></span>
<span data-ttu-id="502f2-147">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="502f2-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="502f2-148">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="502f2-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="502f2-149">SENSORES</span><span class="sxs-lookup"><span data-stu-id="502f2-149">INPUTS</span></span>

### <span data-ttu-id="502f2-150">Microsoft. WindowsAzure. Commands. SQLDatabase. Model. DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="502f2-150">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span></span>

### <span data-ttu-id="502f2-151">Microsoft. WindowsAzure. Commands. SQLDatabase. Services. Server. Database</span><span class="sxs-lookup"><span data-stu-id="502f2-151">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="502f2-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="502f2-152">OUTPUTS</span></span>

### <span data-ttu-id="502f2-153">Microsoft. WindowsAzure. Commands. SQLDatabase. Model. DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="502f2-153">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span></span>

## <span data-ttu-id="502f2-154">INFORMA</span><span class="sxs-lookup"><span data-stu-id="502f2-154">NOTES</span></span>
* <span data-ttu-id="502f2-155">Autenticação: esse cmdlet requer autenticação baseada em certificado.</span><span class="sxs-lookup"><span data-stu-id="502f2-155">Authentication: This cmdlet requires certificate-based authentication.</span></span> <span data-ttu-id="502f2-156">Para obter um exemplo de como usar a autenticação baseada em certificado para definir a assinatura atual, consulte o cmdlet New-AzureSqlDatabaseServerContext.</span><span class="sxs-lookup"><span data-stu-id="502f2-156">For an example of how to use certificate-based authentication to set the current subscription, see the New-AzureSqlDatabaseServerContext cmdlet.</span></span>

## <span data-ttu-id="502f2-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="502f2-157">RELATED LINKS</span></span>

[<span data-ttu-id="502f2-158">Banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="502f2-158">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="502f2-159">Operações para bancos de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="502f2-159">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="502f2-160">Cmdlets do banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="502f2-160">Azure SQL Database Cmdlets</span></span>](./Azure.SQLDatabase.md)

[<span data-ttu-id="502f2-161">Start-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="502f2-161">Start-AzureSqlDatabaseCopy</span></span>](./Start-AzureSqlDatabaseCopy.md)

[<span data-ttu-id="502f2-162">Parar-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="502f2-162">Stop-AzureSqlDatabaseCopy</span></span>](./Stop-AzureSqlDatabaseCopy.md)


