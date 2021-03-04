---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 67A9BB67-EF14-4CAA-99D9-002D0D23178B
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqldatabaserestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseRestorePoint.md
ms.openlocfilehash: 476340114ae2bc6e436301f37a0a9aeaf9fa5e92
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886126"
---
# <span data-ttu-id="309c5-101">Remove-AzSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="309c5-101">Remove-AzSqlDatabaseRestorePoint</span></span>

## <span data-ttu-id="309c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="309c5-102">SYNOPSIS</span></span>
<span data-ttu-id="309c5-103">Remove determinado ponto de restauração de um banco de dados SQL Banco de Dados.</span><span class="sxs-lookup"><span data-stu-id="309c5-103">Removes given restore point from a SQL Database.</span></span>

## <span data-ttu-id="309c5-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="309c5-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseRestorePoint -RestorePointCreationDate <DateTime> [-PassThru] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="309c5-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="309c5-105">DESCRIPTION</span></span>
<span data-ttu-id="309c5-106">O cmdlet **Remove-AzSqlDatabaseRestorePoint** remove determinado ponto de restauração do Banco de Dados do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="309c5-106">The **Remove-AzSqlDatabaseRestorePoint** cmdlet removes given restore point from Azure SQL Database.</span></span>
<span data-ttu-id="309c5-107">Atualmente, esse cmdlet é suportado pelo serviço SQL Server Datawarehouse no Banco de Dados do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="309c5-107">This cmdlet is currently supported by the SQL Server Datawarehouse service on Azure SQL Database.</span></span>

## <span data-ttu-id="309c5-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="309c5-108">EXAMPLES</span></span>

### <span data-ttu-id="309c5-109">Exemplo 1: remove um ponto de restauração</span><span class="sxs-lookup"><span data-stu-id="309c5-109">Example 1: Removes a restore point</span></span>
```
PS C:\>$RestorePointCreationDate = Get-Date "3/11/2017 1:50:00 AM"
PS C:\>Remove-AzSqlDatabaseRestorePoint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -RestorePointCreationDate $RestorePointCreationDate
```

<span data-ttu-id="309c5-110">Este comando remove um ponto de restauração do Azure SQL Data de criação.</span><span class="sxs-lookup"><span data-stu-id="309c5-110">This command removes a restore point for Azure SQL Database given creation date.</span></span>

## <span data-ttu-id="309c5-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="309c5-111">PARAMETERS</span></span>

### <span data-ttu-id="309c5-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="309c5-112">-DatabaseName</span></span>
<span data-ttu-id="309c5-113">Especifica o nome do banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="309c5-113">Specifies the name of the SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="309c5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="309c5-114">-DefaultProfile</span></span>
<span data-ttu-id="309c5-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="309c5-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="309c5-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="309c5-116">-PassThru</span></span>
<span data-ttu-id="309c5-117">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="309c5-117">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="309c5-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="309c5-118">-ResourceGroupName</span></span>
<span data-ttu-id="309c5-119">Especifica o nome do grupo de recursos ao qual o banco de dados SQL é atribuído.</span><span class="sxs-lookup"><span data-stu-id="309c5-119">Specifies the name of the resource group to which the SQL Database is assigned.</span></span>

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

### <span data-ttu-id="309c5-120">-RestorePointCreationDate</span><span class="sxs-lookup"><span data-stu-id="309c5-120">-RestorePointCreationDate</span></span>
<span data-ttu-id="309c5-121">Especifica a data de criação do ponto de restauração.</span><span class="sxs-lookup"><span data-stu-id="309c5-121">Specifies the restore point creation date.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="309c5-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="309c5-122">-ServerName</span></span>
<span data-ttu-id="309c5-123">Especifica o nome do Servidor do AzureSQL que hospeda o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="309c5-123">Specifies the name of the AzureSQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="309c5-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="309c5-124">-Confirm</span></span>
<span data-ttu-id="309c5-125">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="309c5-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="309c5-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="309c5-126">-WhatIf</span></span>
<span data-ttu-id="309c5-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="309c5-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="309c5-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="309c5-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="309c5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="309c5-129">CommonParameters</span></span>
<span data-ttu-id="309c5-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="309c5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="309c5-131">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="309c5-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="309c5-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="309c5-132">INPUTS</span></span>

### <span data-ttu-id="309c5-133">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="309c5-133">System.DateTime</span></span>

### <span data-ttu-id="309c5-134">System.String</span><span class="sxs-lookup"><span data-stu-id="309c5-134">System.String</span></span>

## <span data-ttu-id="309c5-135">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="309c5-135">OUTPUTS</span></span>

### <span data-ttu-id="309c5-136">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseRestorePointModel</span><span class="sxs-lookup"><span data-stu-id="309c5-136">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseRestorePointModel</span></span>

## <span data-ttu-id="309c5-137">NOTES</span><span class="sxs-lookup"><span data-stu-id="309c5-137">NOTES</span></span>

## <span data-ttu-id="309c5-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="309c5-138">RELATED LINKS</span></span>
