---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B3813F54-E5B7-4605-BB1C-67417FDDB076
online version: ''
schema: 2.0.0
ms.openlocfilehash: a3f9817ebe556bc80364d012040387cca72c56c4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946108"
---
# <span data-ttu-id="bfc2b-101">Remove-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="bfc2b-101">Remove-AzureSqlDatabase</span></span>

## <span data-ttu-id="bfc2b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bfc2b-102">SYNOPSIS</span></span>
<span data-ttu-id="bfc2b-103">Exclui um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="bfc2b-103">Deletes an Azure SQL Database.</span></span>

## <span data-ttu-id="bfc2b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bfc2b-104">SYNTAX</span></span>

### <span data-ttu-id="bfc2b-105">ByNameWithConnectionContext</span><span class="sxs-lookup"><span data-stu-id="bfc2b-105">ByNameWithConnectionContext</span></span>
```
Remove-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> -DatabaseName <String> [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bfc2b-106">ByObjectWithConnectionContext</span><span class="sxs-lookup"><span data-stu-id="bfc2b-106">ByObjectWithConnectionContext</span></span>
```
Remove-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> -Database <Database> [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bfc2b-107">ByNameWithServerName</span><span class="sxs-lookup"><span data-stu-id="bfc2b-107">ByNameWithServerName</span></span>
```
Remove-AzureSqlDatabase -ServerName <String> -DatabaseName <String> [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bfc2b-108">ByObjectWithServerName</span><span class="sxs-lookup"><span data-stu-id="bfc2b-108">ByObjectWithServerName</span></span>
```
Remove-AzureSqlDatabase -ServerName <String> -Database <Database> [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bfc2b-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bfc2b-109">DESCRIPTION</span></span>
<span data-ttu-id="bfc2b-110">O cmdlet **Remove-AzureSqlDatabase** exclui um banco de dados SQL do Azure por contexto de conexão do servidor ou nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="bfc2b-110">The **Remove-AzureSqlDatabase** cmdlet deletes an Azure SQL Database by server connection context or server name.</span></span>
<span data-ttu-id="bfc2b-111">Você pode criar um contexto de conexão do servidor de banco de dados SQL do Azure usando o cmdlet **New-AzureSqlDatabaseServerContext** e, em seguida, usá-lo com este cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bfc2b-111">You can create an Azure SQL Database server connection context using the **New-AzureSqlDatabaseServerContext** cmdlet, and then use it with this cmdlet.</span></span>

<span data-ttu-id="bfc2b-112">Quando você exclui um banco de dados especificando um nome de servidor de banco de dados SQL do Azure, o cmdlet **Remove-AzureSqlDatabase** usa o nome e as informações de assinatura atuais do Azure para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="bfc2b-112">When you delete a database by specifying an Azure SQL Database server name, the **Remove-AzureSqlDatabase** cmdlet uses the name and the current Azure subscription information to perform the operation.</span></span>

## <span data-ttu-id="bfc2b-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bfc2b-113">EXAMPLES</span></span>

### <span data-ttu-id="bfc2b-114">Exemplo 1: remover um banco de dados</span><span class="sxs-lookup"><span data-stu-id="bfc2b-114">Example 1: Remove a database</span></span>
```
PS C:\> Remove-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database01"
```

<span data-ttu-id="bfc2b-115">Esse comando Remove o banco de dados chamado Database01 do contexto de conexão do servidor de banco de dados SQL do Azure $Context.</span><span class="sxs-lookup"><span data-stu-id="bfc2b-115">This command removes the database named Database01 from the Azure SQL Database server connection context $Context.</span></span>

### <span data-ttu-id="bfc2b-116">Exemplo 2: remover um banco de dados usando um nome de servidor</span><span class="sxs-lookup"><span data-stu-id="bfc2b-116">Example 2: Remove a database by using a server name</span></span>
```
PS C:\> Remove-AzureSqlDatabase -ServerName "lpqd0zbr8y" -DatabaseName "Database01"
```

<span data-ttu-id="bfc2b-117">Esse comando Remove o banco de dados chamado Database01 do servidor de banco de dados SQL do Azure chamado lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="bfc2b-117">This command removes the database named Database01 from the Azure SQL Database server named lpqd0zbr8y.</span></span>

### <span data-ttu-id="bfc2b-118">Exemplo 3: remover um banco de dados usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="bfc2b-118">Example 3: Remove a database by using the pipeline</span></span>
```
PS C:\> $Database01 | Remove-AzureSqlDatabase -ConnectionContext $Context
PS C:\> $Database01 | Remove-AzureSqlDatabase -ServerName "lpqd0zbr8y"
```

<span data-ttu-id="bfc2b-119">Este exemplo demonstra o método alternativo para passar o objeto de banco de dados pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="bfc2b-119">This example demonstrates the alternative method of passing the database object through the pipeline.</span></span>

## <span data-ttu-id="bfc2b-120">OS</span><span class="sxs-lookup"><span data-stu-id="bfc2b-120">PARAMETERS</span></span>

### <span data-ttu-id="bfc2b-121">-ConnectionContext</span><span class="sxs-lookup"><span data-stu-id="bfc2b-121">-ConnectionContext</span></span>
<span data-ttu-id="bfc2b-122">Especifica o contexto de conexão de um servidor do qual esse cmdlet Remove um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="bfc2b-122">Specifies the connection context of a server from which this cmdlet removes a database.</span></span>

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByNameWithConnectionContext, ByObjectWithConnectionContext
Aliases: Context

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfc2b-123">-Banco de dados</span><span class="sxs-lookup"><span data-stu-id="bfc2b-123">-Database</span></span>
<span data-ttu-id="bfc2b-124">Especifica um objeto que representa o banco de dados que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="bfc2b-124">Specifies an object that represents the database that this cmdlet removes.</span></span>

```yaml
Type: Database
Parameter Sets: ByObjectWithConnectionContext, ByObjectWithServerName
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bfc2b-125">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="bfc2b-125">-DatabaseName</span></span>
<span data-ttu-id="bfc2b-126">Especifica o nome do banco de dados que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="bfc2b-126">Specifies the name of the database that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: ByNameWithConnectionContext, ByNameWithServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfc2b-127">-Force</span><span class="sxs-lookup"><span data-stu-id="bfc2b-127">-Force</span></span>
<span data-ttu-id="bfc2b-128">Permite a conclusão da ação sem solicitar confirmação ao usuário.</span><span class="sxs-lookup"><span data-stu-id="bfc2b-128">Allows the action to complete without prompting the user for confirmation.</span></span>

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

### <span data-ttu-id="bfc2b-129">-Perfil</span><span class="sxs-lookup"><span data-stu-id="bfc2b-129">-Profile</span></span>
<span data-ttu-id="bfc2b-130">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="bfc2b-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="bfc2b-131">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="bfc2b-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="bfc2b-132">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="bfc2b-132">-ServerName</span></span>
<span data-ttu-id="bfc2b-133">Especifica o nome do servidor em que esse cmdlet exclui o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="bfc2b-133">Specifies the name of the server on which this cmdlet deletes the database.</span></span>

```yaml
Type: String
Parameter Sets: ByNameWithServerName, ByObjectWithServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfc2b-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="bfc2b-134">-Confirm</span></span>
<span data-ttu-id="bfc2b-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bfc2b-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bfc2b-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bfc2b-136">-WhatIf</span></span>
<span data-ttu-id="bfc2b-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bfc2b-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bfc2b-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bfc2b-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bfc2b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfc2b-139">CommonParameters</span></span>
<span data-ttu-id="bfc2b-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bfc2b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfc2b-141">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bfc2b-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfc2b-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bfc2b-142">INPUTS</span></span>

### <span data-ttu-id="bfc2b-143">Microsoft. WindowsAzure. Commands. SQLDatabase. Services. Server. Database</span><span class="sxs-lookup"><span data-stu-id="bfc2b-143">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="bfc2b-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bfc2b-144">OUTPUTS</span></span>

## <span data-ttu-id="bfc2b-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bfc2b-145">NOTES</span></span>
* <span data-ttu-id="bfc2b-146">Por causa da severidade da operação, por padrão, esse cmdlet solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="bfc2b-146">Because of the severity of the operation, by default, this cmdlet prompts you for confirmation.</span></span> <span data-ttu-id="bfc2b-147">Para ignorar a confirmação, especifique o parâmetro *Force* .</span><span class="sxs-lookup"><span data-stu-id="bfc2b-147">To skip confirmation, specify the *Force* parameter.</span></span>

## <span data-ttu-id="bfc2b-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bfc2b-148">RELATED LINKS</span></span>

[<span data-ttu-id="bfc2b-149">Banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="bfc2b-149">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="bfc2b-150">Excluir banco de dados</span><span class="sxs-lookup"><span data-stu-id="bfc2b-150">Delete Database</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505705.aspx)

[<span data-ttu-id="bfc2b-151">Operações para bancos de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="bfc2b-151">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="bfc2b-152">Get-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="bfc2b-152">Get-AzureSqlDatabase</span></span>](./Get-AzureSqlDatabase.md)

[<span data-ttu-id="bfc2b-153">New-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="bfc2b-153">New-AzureSqlDatabase</span></span>](./New-AzureSqlDatabase.md)

[<span data-ttu-id="bfc2b-154">New-AzureSqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="bfc2b-154">New-AzureSqlDatabaseServerContext</span></span>](./New-AzureSqlDatabaseServerContext.md)

[<span data-ttu-id="bfc2b-155">Set-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="bfc2b-155">Set-AzureSqlDatabase</span></span>](./Set-AzureSqlDatabase.md)


