---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 952967EB-AEAD-4597-B837-6669CE73739E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseexpanded
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseExpanded.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseExpanded.md
ms.openlocfilehash: 9ff2284e602fe0bb9a7afea886385a02f89298a7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599038"
---
# <span data-ttu-id="83094-101">Get-AzSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="83094-101">Get-AzSqlDatabaseExpanded</span></span>

## <span data-ttu-id="83094-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="83094-102">SYNOPSIS</span></span>
<span data-ttu-id="83094-103">Obtém um banco de dados e seus valores de propriedade expandida.</span><span class="sxs-lookup"><span data-stu-id="83094-103">Gets a database and its expanded property values.</span></span>

## <span data-ttu-id="83094-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="83094-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseExpanded [-ServerName] <String> [[-DatabaseName] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83094-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="83094-105">DESCRIPTION</span></span>
<span data-ttu-id="83094-106">O cmdlet **Get-AzSqlDatabaseExpanded** Obtém um banco de dados e seus valores de propriedade expandida.</span><span class="sxs-lookup"><span data-stu-id="83094-106">The **Get-AzSqlDatabaseExpanded** cmdlet gets a database and its expanded property values.</span></span>
<span data-ttu-id="83094-107">Esse cmdlet também é compatível com o serviço Stretch Database do SQL Server no Azure.</span><span class="sxs-lookup"><span data-stu-id="83094-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="83094-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="83094-108">EXAMPLES</span></span>

### <span data-ttu-id="83094-109">Exemplo 1: obter objeto de banco de dados com informações do supervisor da camada de serviço</span><span class="sxs-lookup"><span data-stu-id="83094-109">Example 1: Get database object that has service tier advisor information</span></span>
```
PS C:\> Get-AzSqlDatabaseExpanded -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="83094-110">Esse comando retorna o banco de dados que tem propriedades expandidas que contêm as informações do supervisor da camada de serviço.</span><span class="sxs-lookup"><span data-stu-id="83094-110">This command returns the database that has expanded properties that contain the service tier advisor information.</span></span>

### <span data-ttu-id="83094-111">Exemplo 2: listar objetos do banco de dados usando filtragem</span><span class="sxs-lookup"><span data-stu-id="83094-111">Example 2: List database objects using filtering</span></span>
```
PS C:\> Get-AzSqlDatabaseExpanded -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database*"
```

<span data-ttu-id="83094-112">Esse comando retorna um objeto de banco de dados expandido para todos os bancos de dados no Server01 que começam com "banco de dados".</span><span class="sxs-lookup"><span data-stu-id="83094-112">This command returns expanded database object for all databases in Server01 that start with "Database".</span></span>

## <span data-ttu-id="83094-113">OS</span><span class="sxs-lookup"><span data-stu-id="83094-113">PARAMETERS</span></span>

### <span data-ttu-id="83094-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="83094-114">-DatabaseName</span></span>
<span data-ttu-id="83094-115">Especifica o nome do banco de dados a ser obtido.</span><span class="sxs-lookup"><span data-stu-id="83094-115">Specifies the name of the database to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="83094-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83094-116">-DefaultProfile</span></span>
<span data-ttu-id="83094-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="83094-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="83094-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83094-118">-ResourceGroupName</span></span>
<span data-ttu-id="83094-119">Especifica o nome do grupo de recursos ao qual o servidor está atribuído.</span><span class="sxs-lookup"><span data-stu-id="83094-119">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="83094-120">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="83094-120">-ServerName</span></span>
<span data-ttu-id="83094-121">Especifica o nome do servidor que hospeda o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="83094-121">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="83094-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="83094-122">-Confirm</span></span>
<span data-ttu-id="83094-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83094-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83094-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83094-124">-WhatIf</span></span>
<span data-ttu-id="83094-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="83094-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83094-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="83094-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83094-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83094-127">CommonParameters</span></span>
<span data-ttu-id="83094-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83094-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83094-129">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="83094-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83094-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="83094-130">INPUTS</span></span>

### <span data-ttu-id="83094-131">System. String</span><span class="sxs-lookup"><span data-stu-id="83094-131">System.String</span></span>

## <span data-ttu-id="83094-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="83094-132">OUTPUTS</span></span>

### <span data-ttu-id="83094-133">Microsoft. Azure. Commands. Sql. Database. Model. AzureSqlDatabaseModelExpanded</span><span class="sxs-lookup"><span data-stu-id="83094-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModelExpanded</span></span>

## <span data-ttu-id="83094-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="83094-134">NOTES</span></span>

## <span data-ttu-id="83094-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="83094-135">RELATED LINKS</span></span>

[<span data-ttu-id="83094-136">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="83094-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
