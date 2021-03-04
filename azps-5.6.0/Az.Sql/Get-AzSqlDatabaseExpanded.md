---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 952967EB-AEAD-4597-B837-6669CE73739E
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldatabaseexpanded
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseExpanded.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseExpanded.md
ms.openlocfilehash: d7eb52a9da5866b4aed280f1ac35651800c67a25
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891076"
---
# <span data-ttu-id="582ef-101">Get-AzSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="582ef-101">Get-AzSqlDatabaseExpanded</span></span>

## <span data-ttu-id="582ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="582ef-102">SYNOPSIS</span></span>
<span data-ttu-id="582ef-103">Obtém um banco de dados e seus valores de propriedade expandida.</span><span class="sxs-lookup"><span data-stu-id="582ef-103">Gets a database and its expanded property values.</span></span>

## <span data-ttu-id="582ef-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="582ef-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseExpanded [-ServerName] <String> [[-DatabaseName] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="582ef-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="582ef-105">DESCRIPTION</span></span>
<span data-ttu-id="582ef-106">O cmdlet **Get-AzSqlDatabaseExpanded** obtém um banco de dados e seus valores de propriedade expandidos.</span><span class="sxs-lookup"><span data-stu-id="582ef-106">The **Get-AzSqlDatabaseExpanded** cmdlet gets a database and its expanded property values.</span></span>
<span data-ttu-id="582ef-107">Esse cmdlet também é suportado pelo serviço SQL Server Banco de Dados de Extensão no Azure.</span><span class="sxs-lookup"><span data-stu-id="582ef-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="582ef-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="582ef-108">EXAMPLES</span></span>

### <span data-ttu-id="582ef-109">Exemplo 1: Obter objeto database que tenha informações de consultor de camada de serviço</span><span class="sxs-lookup"><span data-stu-id="582ef-109">Example 1: Get database object that has service tier advisor information</span></span>
```
PS C:\> Get-AzSqlDatabaseExpanded -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="582ef-110">Este comando retorna o banco de dados que tem propriedades expandidas que contêm as informações do consultor de camada de serviço.</span><span class="sxs-lookup"><span data-stu-id="582ef-110">This command returns the database that has expanded properties that contain the service tier advisor information.</span></span>

### <span data-ttu-id="582ef-111">Exemplo 2: Listar objetos de banco de dados usando filtragem</span><span class="sxs-lookup"><span data-stu-id="582ef-111">Example 2: List database objects using filtering</span></span>
```
PS C:\> Get-AzSqlDatabaseExpanded -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database*"
```

<span data-ttu-id="582ef-112">Este comando retorna o objeto de banco de dados expandido para todos os bancos de dados no Server01 que começam com "Database".</span><span class="sxs-lookup"><span data-stu-id="582ef-112">This command returns expanded database object for all databases in Server01 that start with "Database".</span></span>

## <span data-ttu-id="582ef-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="582ef-113">PARAMETERS</span></span>

### <span data-ttu-id="582ef-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="582ef-114">-DatabaseName</span></span>
<span data-ttu-id="582ef-115">Especifica o nome do banco de dados a ser obter.</span><span class="sxs-lookup"><span data-stu-id="582ef-115">Specifies the name of the database to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="582ef-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="582ef-116">-DefaultProfile</span></span>
<span data-ttu-id="582ef-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="582ef-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="582ef-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="582ef-118">-ResourceGroupName</span></span>
<span data-ttu-id="582ef-119">Especifica o nome do grupo de recursos ao qual o servidor é atribuído.</span><span class="sxs-lookup"><span data-stu-id="582ef-119">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="582ef-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="582ef-120">-ServerName</span></span>
<span data-ttu-id="582ef-121">Especifica o nome do servidor que hospeda o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="582ef-121">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="582ef-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="582ef-122">-Confirm</span></span>
<span data-ttu-id="582ef-123">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="582ef-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="582ef-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="582ef-124">-WhatIf</span></span>
<span data-ttu-id="582ef-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="582ef-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="582ef-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="582ef-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="582ef-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="582ef-127">CommonParameters</span></span>
<span data-ttu-id="582ef-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="582ef-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="582ef-129">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="582ef-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="582ef-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="582ef-130">INPUTS</span></span>

### <span data-ttu-id="582ef-131">System.String</span><span class="sxs-lookup"><span data-stu-id="582ef-131">System.String</span></span>

## <span data-ttu-id="582ef-132">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="582ef-132">OUTPUTS</span></span>

### <span data-ttu-id="582ef-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModelExpanded</span><span class="sxs-lookup"><span data-stu-id="582ef-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModelExpanded</span></span>

## <span data-ttu-id="582ef-134">NOTES</span><span class="sxs-lookup"><span data-stu-id="582ef-134">NOTES</span></span>

## <span data-ttu-id="582ef-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="582ef-135">RELATED LINKS</span></span>

[<span data-ttu-id="582ef-136">SQL documentação do banco de dados</span><span class="sxs-lookup"><span data-stu-id="582ef-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
