---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 0C8AC52C-4E70-493C-A299-79CE32EC5EF1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabase.md
ms.openlocfilehash: 9ae96035a4257826ac92dc6dbae75282debf08a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440937"
---
# <span data-ttu-id="cdcc1-101">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="cdcc1-101">Get-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="cdcc1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cdcc1-102">SYNOPSIS</span></span>
<span data-ttu-id="cdcc1-103">Obtém um ou mais bancos de dados.</span><span class="sxs-lookup"><span data-stu-id="cdcc1-103">Gets one or more databases.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cdcc1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cdcc1-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabase [[-DatabaseName] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cdcc1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cdcc1-105">DESCRIPTION</span></span>
<span data-ttu-id="cdcc1-106">O cmdlet **Get-AzureRmSqlDatabase** Obtém um ou mais bancos de dados SQL do Azure de um servidor de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="cdcc1-106">The **Get-AzureRmSqlDatabase** cmdlet gets one or more Azure SQL databases from an Azure SQL Database Server.</span></span>

<span data-ttu-id="cdcc1-107">Esse cmdlet também é compatível com o serviço Stretch Database do SQL Server no Azure.</span><span class="sxs-lookup"><span data-stu-id="cdcc1-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="cdcc1-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cdcc1-108">EXAMPLES</span></span>

### <span data-ttu-id="cdcc1-109">Exemplo 1: obter todos os bancos de dados em um servidor</span><span class="sxs-lookup"><span data-stu-id="cdcc1-109">Example 1: Get all databases on a server</span></span>
```
PS C:\>Get-AzureRmSqlDatabase -ResourceGroupName "resourcegroup01" -ServerName "server01"
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

<span data-ttu-id="cdcc1-110">Esse comando obtém todos os bancos de dados no servidor chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="cdcc1-110">This command gets all databases on the server named server01.</span></span>

### <span data-ttu-id="cdcc1-111">Exemplo 2: obter um banco de dados por nome em um servidor</span><span class="sxs-lookup"><span data-stu-id="cdcc1-111">Example 2: Get a database by name on a server</span></span>
```
PS C:\>Get-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database02"
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

<span data-ttu-id="cdcc1-112">Esse comando obtém um banco de dados denominado Database02 de um servidor chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="cdcc1-112">This command gets a database named Database02 from a server named Server01.</span></span>

## <span data-ttu-id="cdcc1-113">OS</span><span class="sxs-lookup"><span data-stu-id="cdcc1-113">PARAMETERS</span></span>

### <span data-ttu-id="cdcc1-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="cdcc1-114">-DatabaseName</span></span>
<span data-ttu-id="cdcc1-115">Especifica o nome do banco de dados a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="cdcc1-115">Specifies the name of the database to retrieve.</span></span>

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

### <span data-ttu-id="cdcc1-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cdcc1-116">-ResourceGroupName</span></span>
<span data-ttu-id="cdcc1-117">Especifica o nome do grupo de recursos ao qual o servidor de banco de dados está atribuído.</span><span class="sxs-lookup"><span data-stu-id="cdcc1-117">Specifies the name of the resource group to which the database server is assigned.</span></span>

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

### <span data-ttu-id="cdcc1-118">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="cdcc1-118">-ServerName</span></span>
<span data-ttu-id="cdcc1-119">Especifica o nome do servidor ao qual o banco de dados está atribuído.</span><span class="sxs-lookup"><span data-stu-id="cdcc1-119">Specifies the name of the server to which the database is assigned.</span></span>

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

### <span data-ttu-id="cdcc1-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="cdcc1-120">-Confirm</span></span>
<span data-ttu-id="cdcc1-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cdcc1-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cdcc1-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cdcc1-122">-WhatIf</span></span>
<span data-ttu-id="cdcc1-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cdcc1-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cdcc1-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cdcc1-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cdcc1-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdcc1-125">-DefaultProfile</span></span>
<span data-ttu-id="cdcc1-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cdcc1-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdcc1-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdcc1-127">CommonParameters</span></span>
<span data-ttu-id="cdcc1-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cdcc1-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdcc1-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cdcc1-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdcc1-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cdcc1-130">INPUTS</span></span>

## <span data-ttu-id="cdcc1-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cdcc1-131">OUTPUTS</span></span>

### <span data-ttu-id="cdcc1-132">Microsoft. Azure. Commands. Sql. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="cdcc1-132">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="cdcc1-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cdcc1-133">NOTES</span></span>

## <span data-ttu-id="cdcc1-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cdcc1-134">RELATED LINKS</span></span>

[<span data-ttu-id="cdcc1-135">New-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="cdcc1-135">New-AzureRmSqlDatabase</span></span>](./New-AzureRmSqlDatabase.md)

[<span data-ttu-id="cdcc1-136">Remove-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="cdcc1-136">Remove-AzureRmSqlDatabase</span></span>](./Remove-AzureRmSqlDatabase.md)

[<span data-ttu-id="cdcc1-137">Currículo-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="cdcc1-137">Resume-AzureRmSqlDatabase</span></span>](./Resume-AzureRmSqlDatabase.md)

[<span data-ttu-id="cdcc1-138">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="cdcc1-138">Set-AzureRmSqlDatabase</span></span>](./Set-AzureRmSqlDatabase.md)

[<span data-ttu-id="cdcc1-139">Suspender-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="cdcc1-139">Suspend-AzureRmSqlDatabase</span></span>](./Suspend-AzureRmSqlDatabase.md)


