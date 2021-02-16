---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 5AEF7D44-624D-4794-86FF-156E6729BB56
online version: ''
schema: 2.0.0
ms.openlocfilehash: 95e276bf6af11698a4b3b82077175ec2ede2d7dc
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100402415"
---
# <span data-ttu-id="acd54-101">Get-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="acd54-101">Get-AzureSqlDatabaseCopy</span></span>

## <span data-ttu-id="acd54-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="acd54-102">SYNOPSIS</span></span>
<span data-ttu-id="acd54-103">Verifica o status das relações de cópia.</span><span class="sxs-lookup"><span data-stu-id="acd54-103">Checks the status of copy relationships.</span></span>

## <span data-ttu-id="acd54-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="acd54-104">SYNTAX</span></span>

### <span data-ttu-id="acd54-105">ByServerNameOnly (Padrão)</span><span class="sxs-lookup"><span data-stu-id="acd54-105">ByServerNameOnly (Default)</span></span>
```
Get-AzureSqlDatabaseCopy -ServerName <String> [-DatabaseName <String>] [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="acd54-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="acd54-106">ByInputObject</span></span>
```
Get-AzureSqlDatabaseCopy -ServerName <String> -DatabaseCopy <DatabaseCopy> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="acd54-107">ByDatabase</span><span class="sxs-lookup"><span data-stu-id="acd54-107">ByDatabase</span></span>
```
Get-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="acd54-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="acd54-108">DESCRIPTION</span></span>
<span data-ttu-id="acd54-109">O cmdlet **Get-AzureSqlDatabaseCopy** verifica o status de uma ou mais relações de cópia ativa.</span><span class="sxs-lookup"><span data-stu-id="acd54-109">The **Get-AzureSqlDatabaseCopy** cmdlet checks the status of one or more active copy relationships.</span></span>
<span data-ttu-id="acd54-110">Execute este cmdlet depois de executar o cmdlet Start-AzureSqlDatabaseCopy ou Stop-AzureSqlDatabaseCopy cmdlet.</span><span class="sxs-lookup"><span data-stu-id="acd54-110">Run this cmdlet after you run the Start-AzureSqlDatabaseCopy or Stop-AzureSqlDatabaseCopy cmdlet.</span></span>
<span data-ttu-id="acd54-111">Você pode verificar uma relação de cópia específica, todas as relações de cópia ou uma lista filtrada de relações de cópia, como todas as cópias em um servidor de destino específico.</span><span class="sxs-lookup"><span data-stu-id="acd54-111">You can check a specific copy relationship, all copy relationships, or a filtered list of copy relationships, such as all copies on a specific target server.</span></span>
<span data-ttu-id="acd54-112">Você pode executar esse cmdlet no servidor que hospeda o banco de dados de origem ou de destino.</span><span class="sxs-lookup"><span data-stu-id="acd54-112">You can run this cmdlet on the server that hosts the source or target database.</span></span>

<span data-ttu-id="acd54-113">Este cmdlet é sincronizado.</span><span class="sxs-lookup"><span data-stu-id="acd54-113">This cmdlet is synchronous.</span></span>
<span data-ttu-id="acd54-114">O cmdlet bloqueia o console do Azure PowerShell até que ele retorne um objeto de status.</span><span class="sxs-lookup"><span data-stu-id="acd54-114">The cmdlet blocks the Azure PowerShell console until it returns a status object.</span></span>

<span data-ttu-id="acd54-115">Os *parâmetros PartnerServer* *e PartnerDatabase* são opcionais.</span><span class="sxs-lookup"><span data-stu-id="acd54-115">The *PartnerServer* and *PartnerDatabase* parameters are optional.</span></span>
<span data-ttu-id="acd54-116">Se você não especificar um dos parâmetros, esse cmdlet retornará uma tabela de resultados.</span><span class="sxs-lookup"><span data-stu-id="acd54-116">If you do not specify either parameter, this cmdlet returns a table of results.</span></span>
<span data-ttu-id="acd54-117">Para ver o status de apenas um determinado banco de dados, especifique os dois parâmetros.</span><span class="sxs-lookup"><span data-stu-id="acd54-117">To see the status for only a particular database, specify both parameters.</span></span>

## <span data-ttu-id="acd54-118">Exemplos</span><span class="sxs-lookup"><span data-stu-id="acd54-118">EXAMPLES</span></span>

### <span data-ttu-id="acd54-119">Exemplo 1: Obter o status de cópia de um banco de dados</span><span class="sxs-lookup"><span data-stu-id="acd54-119">Example 1: Get the copy status of a database</span></span>
```
PS C:\> Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf658"
```

<span data-ttu-id="acd54-120">Esse comando obtém o status do banco de dados chamado Pedidos no servidor chamado lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="acd54-120">This command gets the status of the database named Orders on the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="acd54-121">O *parâmetro PartnerServer* restringe esse comando ao servidor bk0b8kf658.</span><span class="sxs-lookup"><span data-stu-id="acd54-121">The *PartnerServer* parameter restricts this command to the bk0b8kf658 server.</span></span>

### <span data-ttu-id="acd54-122">Exemplo 2: Obter o status de todas as cópias em um servidorGet o status de todas as cópias em um servidor</span><span class="sxs-lookup"><span data-stu-id="acd54-122">Example 2: Get the status of all copies on a serverGet the status of all copies on a server</span></span>
```
PS C:\> Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y"
```

<span data-ttu-id="acd54-123">Esse comando obtém o status de todas as cópias ativas no servidor chamado lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="acd54-123">This command gets the status of all active copies on the server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="acd54-124">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="acd54-124">PARAMETERS</span></span>

### <span data-ttu-id="acd54-125">-Banco de dados</span><span class="sxs-lookup"><span data-stu-id="acd54-125">-Database</span></span>
<span data-ttu-id="acd54-126">Especifica um objeto que representa o banco de dados SQL do Azure de origem.</span><span class="sxs-lookup"><span data-stu-id="acd54-126">Specifies an object that represents the source Azure SQL Database.</span></span>
<span data-ttu-id="acd54-127">Este cmdlet obtém o status de cópia do banco de dados especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="acd54-127">This cmdlet gets the copy status of the database that this parameter specifies.</span></span>

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

### <span data-ttu-id="acd54-128">-DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="acd54-128">-DatabaseCopy</span></span>
<span data-ttu-id="acd54-129">Especifica um objeto que representa um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="acd54-129">Specifies an object that represents a database.</span></span>
<span data-ttu-id="acd54-130">Este cmdlet obtém o status de cópia do banco de dados especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="acd54-130">This cmdlet gets the copy status of the database that this parameter specifies.</span></span>
<span data-ttu-id="acd54-131">Este parâmetro aceita a entrada de pipeline.</span><span class="sxs-lookup"><span data-stu-id="acd54-131">This parameter accepts pipeline input.</span></span>

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

### <span data-ttu-id="acd54-132">-Nomedo Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="acd54-132">-DatabaseName</span></span>
<span data-ttu-id="acd54-133">Especifica o nome do banco de dados de origem.</span><span class="sxs-lookup"><span data-stu-id="acd54-133">Specifies the name of the source database.</span></span>
<span data-ttu-id="acd54-134">Esse cmdlet obtém o status da cópia do banco de dados especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="acd54-134">This cmdlet gets that copy status of the database that this parameter specifies.</span></span>

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

### <span data-ttu-id="acd54-135">-PartnerDatabase</span><span class="sxs-lookup"><span data-stu-id="acd54-135">-PartnerDatabase</span></span>
<span data-ttu-id="acd54-136">Especifica o nome do banco de dados secundário.</span><span class="sxs-lookup"><span data-stu-id="acd54-136">Specifies name of the secondary database.</span></span>
<span data-ttu-id="acd54-137">Se esse banco de dados não for encontrado no modo sys.dm_database_copies de gerenciamento dinâmico, esse cmdlet retornará um objeto de status vazio.</span><span class="sxs-lookup"><span data-stu-id="acd54-137">If this database is not found in the sys.dm_database_copies dynamic management view, this cmdlet returns an empty status object.</span></span>

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

### <span data-ttu-id="acd54-138">-PartnerServer</span><span class="sxs-lookup"><span data-stu-id="acd54-138">-PartnerServer</span></span>
<span data-ttu-id="acd54-139">Especifica o nome do servidor que hospeda o banco de dados de destino.</span><span class="sxs-lookup"><span data-stu-id="acd54-139">Specifies the name of the server that hosts the target database.</span></span>
<span data-ttu-id="acd54-140">Se esse servidor não for encontrado no modo sys.dm_database_copies de gerenciamento dinâmico, esse cmdlet retornará um objeto de status vazio.</span><span class="sxs-lookup"><span data-stu-id="acd54-140">If this server is not found in the sys.dm_database_copies dynamic management view, this cmdlet returns an empty status object.</span></span>

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

### <span data-ttu-id="acd54-141">-Perfil</span><span class="sxs-lookup"><span data-stu-id="acd54-141">-Profile</span></span>
<span data-ttu-id="acd54-142">Especifica o perfil do Azure a partir do qual este cmdlet é lido.</span><span class="sxs-lookup"><span data-stu-id="acd54-142">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="acd54-143">Se você não especificar um perfil, esse cmdlet será lido do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="acd54-143">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="acd54-144">-ServerName</span><span class="sxs-lookup"><span data-stu-id="acd54-144">-ServerName</span></span>
<span data-ttu-id="acd54-145">Especifica o nome do servidor no qual reside a cópia do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="acd54-145">Specifies the name of the server on which the database copy resides.</span></span>

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

### <span data-ttu-id="acd54-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acd54-146">CommonParameters</span></span>
<span data-ttu-id="acd54-147">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="acd54-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acd54-148">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="acd54-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acd54-149">Entradas</span><span class="sxs-lookup"><span data-stu-id="acd54-149">INPUTS</span></span>

### <span data-ttu-id="acd54-150">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="acd54-150">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span></span>

### <span data-ttu-id="acd54-151">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span><span class="sxs-lookup"><span data-stu-id="acd54-151">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="acd54-152">Saídas</span><span class="sxs-lookup"><span data-stu-id="acd54-152">OUTPUTS</span></span>

### <span data-ttu-id="acd54-153">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="acd54-153">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span></span>

## <span data-ttu-id="acd54-154">Notas</span><span class="sxs-lookup"><span data-stu-id="acd54-154">NOTES</span></span>
* <span data-ttu-id="acd54-155">Autenticação: esse cmdlet requer autenticação baseada em certificado.</span><span class="sxs-lookup"><span data-stu-id="acd54-155">Authentication: This cmdlet requires certificate-based authentication.</span></span> <span data-ttu-id="acd54-156">Para ver um exemplo de como usar a autenticação baseada em certificado para definir a assinatura atual, consulte New-AzureSqlDatabaseServerContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="acd54-156">For an example of how to use certificate-based authentication to set the current subscription, see the New-AzureSqlDatabaseServerContext cmdlet.</span></span>

## <span data-ttu-id="acd54-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="acd54-157">RELATED LINKS</span></span>

[<span data-ttu-id="acd54-158">Banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="acd54-158">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="acd54-159">Operações para bancos de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="acd54-159">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)



[<span data-ttu-id="acd54-160">Start-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="acd54-160">Start-AzureSqlDatabaseCopy</span></span>](./Start-AzureSqlDatabaseCopy.md)

[<span data-ttu-id="acd54-161">Stop-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="acd54-161">Stop-AzureSqlDatabaseCopy</span></span>](./Stop-AzureSqlDatabaseCopy.md)


