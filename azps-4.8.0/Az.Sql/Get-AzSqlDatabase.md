---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 0C8AC52C-4E70-493C-A299-79CE32EC5EF1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabase.md
ms.openlocfilehash: 4f90d6d0c33874750bf2f32ae7f65bf32457f63c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94113271"
---
# <span data-ttu-id="499db-101">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="499db-101">Get-AzSqlDatabase</span></span>

## <span data-ttu-id="499db-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="499db-102">SYNOPSIS</span></span>
<span data-ttu-id="499db-103">Obtém um ou mais bancos de dados.</span><span class="sxs-lookup"><span data-stu-id="499db-103">Gets one or more databases.</span></span>

## <span data-ttu-id="499db-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="499db-104">SYNTAX</span></span>

```
Get-AzSqlDatabase [[-DatabaseName] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="499db-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="499db-105">DESCRIPTION</span></span>
<span data-ttu-id="499db-106">O cmdlet **Get-AzSqlDatabase** Obtém um ou mais bancos de dados SQL do Azure de um servidor de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="499db-106">The **Get-AzSqlDatabase** cmdlet gets one or more Azure SQL databases from an Azure SQL Database Server.</span></span>
<span data-ttu-id="499db-107">Esse cmdlet também é compatível com o serviço Stretch Database do SQL Server no Azure.</span><span class="sxs-lookup"><span data-stu-id="499db-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="499db-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="499db-108">EXAMPLES</span></span>

### <span data-ttu-id="499db-109">Exemplo 1: obter todos os bancos de dados em um servidor</span><span class="sxs-lookup"><span data-stu-id="499db-109">Example 1: Get all databases on a server</span></span>
```
PS C:\>Get-AzSqlDatabase -ResourceGroupName "resourcegroup01" -ServerName "server01"
ResourceGroupName             : resourcegroup01
ServerName                    : server01
DatabaseName                  : master
Location                      : Central US
DatabaseId                    : a2a7f2db-7526-4d86-a7b2-36276ee10dc6
Edition                       : None
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              : 
MaxSizeBytes                  : 5368709120
Status                        : Online
CreationDate                  : 7/3/2015 7:32:44 AM
CurrentServiceObjectiveId     : c99ac918-dbea-463f-a475-16ec020fdc12
CurrentServiceObjectiveName   : System1
RequestedServiceObjectiveId   : c99ac918-dbea-463f-a475-16ec020fdc12
RequestedServiceObjectiveName : 
ElasticPoolName               : 
EarliestRestoreDate           : 
Tags                          : 

ResourceGroupName             : resourcegroup01
ServerName                    : server01
DatabaseName                  : database01
Location                      : Central US
DatabaseId                    : a1e6bd1a-735a-4d48-8b98-afead5ef1218
Edition                       : Standard
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              : 
MaxSizeBytes                  : 268435456000
Status                        : Online
CreationDate                  : 7/3/2015 7:33:37 AM
CurrentServiceObjectiveId     : f1173c43-91bd-4aaa-973c-54e79e15235b
CurrentServiceObjectiveName   : S0
RequestedServiceObjectiveId   : f1173c43-91bd-4aaa-973c-54e79e15235b
RequestedServiceObjectiveName : 
ElasticPoolName               : 
EarliestRestoreDate           : 
Tags                          :
```

<span data-ttu-id="499db-110">Esse comando obtém todos os bancos de dados no servidor chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="499db-110">This command gets all databases on the server named server01.</span></span>

### <span data-ttu-id="499db-111">Exemplo 2: obter um banco de dados por nome em um servidor</span><span class="sxs-lookup"><span data-stu-id="499db-111">Example 2: Get a database by name on a server</span></span>
```
PS C:\>Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database02"
ResourceGroupName             : resourcegroup01
ServerName                    : server01
DatabaseName                  : database02
Location                      : Central US
DatabaseId                    : a1e6bd1a-735a-4d48-8b98-afead5ef1218
Edition                       : Standard
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              : 
MaxSizeBytes                  : 268435456000
Status                        : Online
CreationDate                  : 7/3/2015 7:33:37 AM
CurrentServiceObjectiveId     : f1173c43-91bd-4aaa-973c-54e79e15235b
CurrentServiceObjectiveName   : S0
RequestedServiceObjectiveId   : f1173c43-91bd-4aaa-973c-54e79e15235b
RequestedServiceObjectiveName : 
ElasticPoolName               : 
EarliestRestoreDate           : 
Tags                          :
```

<span data-ttu-id="499db-112">Esse comando obtém um banco de dados denominado Database02 de um servidor chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="499db-112">This command gets a database named Database02 from a server named Server01.</span></span>

### <span data-ttu-id="499db-113">Exemplo 3: obter todos os bancos de dados em um servidor usando a filtragem</span><span class="sxs-lookup"><span data-stu-id="499db-113">Example 3: Get all databases on a server using filtering</span></span>
```
PS C:\> Get-AzSqlDatabase -ResourceGroupName "resourcegroup01" -ServerName "server01" -DatabaseName "database*"
ResourceGroupName             : resourcegroup01
ServerName                    : server01
DatabaseName                  : database01
Location                      : Central US
DatabaseId                    : a2a7f2db-7526-4d86-a7b2-36276ee10dc6
Edition                       : None
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              : 
MaxSizeBytes                  : 5368709120
Status                        : Online
CreationDate                  : 7/3/2015 7:32:44 AM
CurrentServiceObjectiveId     : c99ac918-dbea-463f-a475-16ec020fdc12
CurrentServiceObjectiveName   : System1
RequestedServiceObjectiveId   : c99ac918-dbea-463f-a475-16ec020fdc12
RequestedServiceObjectiveName : 
ElasticPoolName               : 
EarliestRestoreDate           : 
Tags                          : 

ResourceGroupName             : resourcegroup01
ServerName                    : server01
DatabaseName                  : database02
Location                      : Central US
DatabaseId                    : a1e6bd1a-735a-4d48-8b98-afead5ef1218
Edition                       : Standard
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              : 
MaxSizeBytes                  : 268435456000
Status                        : Online
CreationDate                  : 7/3/2015 7:33:37 AM
CurrentServiceObjectiveId     : f1173c43-91bd-4aaa-973c-54e79e15235b
CurrentServiceObjectiveName   : S0
RequestedServiceObjectiveId   : f1173c43-91bd-4aaa-973c-54e79e15235b
RequestedServiceObjectiveName : 
ElasticPoolName               : 
EarliestRestoreDate           : 
Tags                          :
```

<span data-ttu-id="499db-114">Esse comando obtém todos os bancos de dados no servidor chamado Server01 que começam com "banco de dados".</span><span class="sxs-lookup"><span data-stu-id="499db-114">This command gets all databases on the server named server01 that start with "database".</span></span>

## <span data-ttu-id="499db-115">OS</span><span class="sxs-lookup"><span data-stu-id="499db-115">PARAMETERS</span></span>

### <span data-ttu-id="499db-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="499db-116">-DatabaseName</span></span>
<span data-ttu-id="499db-117">Especifica o nome do banco de dados a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="499db-117">Specifies the name of the database to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="499db-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="499db-118">-DefaultProfile</span></span>
<span data-ttu-id="499db-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="499db-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="499db-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="499db-120">-ResourceGroupName</span></span>
<span data-ttu-id="499db-121">Especifica o nome do grupo de recursos ao qual o servidor de banco de dados está atribuído.</span><span class="sxs-lookup"><span data-stu-id="499db-121">Specifies the name of the resource group to which the database server is assigned.</span></span>

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

### <span data-ttu-id="499db-122">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="499db-122">-ServerName</span></span>
<span data-ttu-id="499db-123">Especifica o nome do servidor ao qual o banco de dados está atribuído.</span><span class="sxs-lookup"><span data-stu-id="499db-123">Specifies the name of the server to which the database is assigned.</span></span>

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

### <span data-ttu-id="499db-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="499db-124">-Confirm</span></span>
<span data-ttu-id="499db-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="499db-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="499db-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="499db-126">-WhatIf</span></span>
<span data-ttu-id="499db-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="499db-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="499db-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="499db-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="499db-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="499db-129">CommonParameters</span></span>
<span data-ttu-id="499db-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="499db-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="499db-131">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="499db-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="499db-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="499db-132">INPUTS</span></span>

### <span data-ttu-id="499db-133">System. String</span><span class="sxs-lookup"><span data-stu-id="499db-133">System.String</span></span>

## <span data-ttu-id="499db-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="499db-134">OUTPUTS</span></span>

### <span data-ttu-id="499db-135">Microsoft. Azure. Commands. Sql. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="499db-135">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="499db-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="499db-136">NOTES</span></span>

## <span data-ttu-id="499db-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="499db-137">RELATED LINKS</span></span>

[<span data-ttu-id="499db-138">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="499db-138">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="499db-139">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="499db-139">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="499db-140">Currículo-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="499db-140">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="499db-141">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="499db-141">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="499db-142">Suspender-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="499db-142">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)


