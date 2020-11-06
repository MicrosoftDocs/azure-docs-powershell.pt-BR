---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B396388D-F91C-4BC9-A211-ABFF5DFC1693
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabase.md
ms.openlocfilehash: 200e53ef1f23c4b829380a2c8b7ca663443e5f7a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598864"
---
# <span data-ttu-id="5e74e-101">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5e74e-101">Remove-AzSqlDatabase</span></span>

## <span data-ttu-id="5e74e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5e74e-102">SYNOPSIS</span></span>
<span data-ttu-id="5e74e-103">Remove um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="5e74e-103">Removes an Azure SQL database.</span></span>

## <span data-ttu-id="5e74e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5e74e-104">SYNTAX</span></span>

```
Remove-AzSqlDatabase [-DatabaseName] <String> [-Force] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e74e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5e74e-105">DESCRIPTION</span></span>
<span data-ttu-id="5e74e-106">O cmdlet **Remove-AzSqlDatabase** remove um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="5e74e-106">The **Remove-AzSqlDatabase** cmdlet removes an Azure SQL database.</span></span>
<span data-ttu-id="5e74e-107">Esse cmdlet também é compatível com o serviço Stretch Database do SQL Server no Azure.</span><span class="sxs-lookup"><span data-stu-id="5e74e-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="5e74e-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5e74e-108">EXAMPLES</span></span>

### <span data-ttu-id="5e74e-109">Exemplo 1: remover um banco de dados de um SQL Server do Azure</span><span class="sxs-lookup"><span data-stu-id="5e74e-109">Example 1: Remove a database from an Azure SQL server</span></span>
```
PS C:\>Remove-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="5e74e-110">Esse comando Remove o banco de dados denominado Database01 do servidor Server01.</span><span class="sxs-lookup"><span data-stu-id="5e74e-110">This command removes the database named Database01 from server Server01.</span></span>

## <span data-ttu-id="5e74e-111">OS</span><span class="sxs-lookup"><span data-stu-id="5e74e-111">PARAMETERS</span></span>

### <span data-ttu-id="5e74e-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5e74e-112">-DatabaseName</span></span>
<span data-ttu-id="5e74e-113">Especifica o nome do banco de dados que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="5e74e-113">Specifies the name of the database that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e74e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e74e-114">-DefaultProfile</span></span>
<span data-ttu-id="5e74e-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="5e74e-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5e74e-116">-Force</span><span class="sxs-lookup"><span data-stu-id="5e74e-116">-Force</span></span>
<span data-ttu-id="5e74e-117">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="5e74e-117">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e74e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e74e-118">-ResourceGroupName</span></span>
<span data-ttu-id="5e74e-119">Especifica o nome do grupo de recursos do Azure ao qual o banco de dados está atribuído.</span><span class="sxs-lookup"><span data-stu-id="5e74e-119">Specifies the name of the Azure resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="5e74e-120">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="5e74e-120">-ServerName</span></span>
<span data-ttu-id="5e74e-121">Especifica o nome do servidor que hospeda o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="5e74e-121">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="5e74e-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5e74e-122">-Confirm</span></span>
<span data-ttu-id="5e74e-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e74e-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e74e-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e74e-124">-WhatIf</span></span>
<span data-ttu-id="5e74e-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5e74e-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e74e-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5e74e-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e74e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e74e-127">CommonParameters</span></span>
<span data-ttu-id="5e74e-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e74e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e74e-129">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5e74e-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e74e-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5e74e-130">INPUTS</span></span>

### <span data-ttu-id="5e74e-131">System. String</span><span class="sxs-lookup"><span data-stu-id="5e74e-131">System.String</span></span>

## <span data-ttu-id="5e74e-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5e74e-132">OUTPUTS</span></span>

### <span data-ttu-id="5e74e-133">Microsoft. Azure. Commands. Sql. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="5e74e-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="5e74e-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5e74e-134">NOTES</span></span>

## <span data-ttu-id="5e74e-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5e74e-135">RELATED LINKS</span></span>

[<span data-ttu-id="5e74e-136">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5e74e-136">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="5e74e-137">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5e74e-137">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="5e74e-138">Currículo-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5e74e-138">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="5e74e-139">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5e74e-139">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="5e74e-140">Suspender-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5e74e-140">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="5e74e-141">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="5e74e-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


