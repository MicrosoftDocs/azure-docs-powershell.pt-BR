---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 67A9BB67-CF17-4CAA-99D9-002D0D23178B
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqldatabaserestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseRestorePoint.md
ms.openlocfilehash: 8fb320c2caa4993b7880ef719a3d9ea0e0e8c811
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885959"
---
# <span data-ttu-id="a9ec4-101">New-AzSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="a9ec4-101">New-AzSqlDatabaseRestorePoint</span></span>

## <span data-ttu-id="a9ec4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9ec4-102">SYNOPSIS</span></span>
<span data-ttu-id="a9ec4-103">Cria um novo ponto de restauração a partir do qual um banco de dados SQL pode ser restaurado.</span><span class="sxs-lookup"><span data-stu-id="a9ec4-103">Creates a new restore point from which a SQL Database can be restored.</span></span>

## <span data-ttu-id="a9ec4-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a9ec4-104">SYNTAX</span></span>

```
New-AzSqlDatabaseRestorePoint -RestorePointLabel <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a9ec4-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a9ec4-105">DESCRIPTION</span></span>
<span data-ttu-id="a9ec4-106">O cmdlet **New-AzSqlDatabaseRestorePoint** cria um novo ponto de restauração do SQL Data Warehouse do Azure.</span><span class="sxs-lookup"><span data-stu-id="a9ec4-106">The **New-AzSqlDatabaseRestorePoint** cmdlet creates a new restore point that an Azure SQL Data Warehouse can be restored from.</span></span>
<span data-ttu-id="a9ec4-107">Atualmente, esse cmdlet tem suporte para o Azure SQL Data Warehouse.</span><span class="sxs-lookup"><span data-stu-id="a9ec4-107">This cmdlet is currently supported for Azure SQL Data Warehouse.</span></span>

## <span data-ttu-id="a9ec4-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a9ec4-108">EXAMPLES</span></span>

### <span data-ttu-id="a9ec4-109">Exemplo 1: Criar um ponto de restauração</span><span class="sxs-lookup"><span data-stu-id="a9ec4-109">Example 1: Create a restore point</span></span>
```
PS C:\>New-AzSqlDatabaseRestorePoint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -RestorePointLabel "RestorePoint01"
ResourceGroupName        : resourcegroup01
ServerName               : server01
DatabaseName             : database01
Location                 : Central US
RestorePointType         : DISCRETE
RestorePointCreationDate : 8/12/2015 12:00:00 AM
EarliestRestoreDate      : 
RestorePointLabel        : RestorePoint01
```

<span data-ttu-id="a9ec4-110">Este comando cria um ponto de restauração para o Azure SQL Data Warehouse e retorna os detalhes do ponto de restauração.</span><span class="sxs-lookup"><span data-stu-id="a9ec4-110">This command creates a restore point for Azure SQL Data Warehouse and returns the details of the restore point.</span></span>

## <span data-ttu-id="a9ec4-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a9ec4-111">PARAMETERS</span></span>

### <span data-ttu-id="a9ec4-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a9ec4-112">-DatabaseName</span></span>
<span data-ttu-id="a9ec4-113">Especifica o nome do banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="a9ec4-113">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="a9ec4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9ec4-114">-DefaultProfile</span></span>
<span data-ttu-id="a9ec4-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="a9ec4-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a9ec4-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9ec4-116">-ResourceGroupName</span></span>
<span data-ttu-id="a9ec4-117">Especifica o nome do grupo de recursos ao qual o banco de dados SQL é atribuído.</span><span class="sxs-lookup"><span data-stu-id="a9ec4-117">Specifies the name of the resource group to which the SQL Database is assigned.</span></span>

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

### <span data-ttu-id="a9ec4-118">-RestorePointLabel</span><span class="sxs-lookup"><span data-stu-id="a9ec4-118">-RestorePointLabel</span></span>
<span data-ttu-id="a9ec4-119">Especifica o rótulo do ponto de restauração para facilitar a identificação.</span><span class="sxs-lookup"><span data-stu-id="a9ec4-119">Specifies the label of the restore point for easy identification.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9ec4-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a9ec4-120">-ServerName</span></span>
<span data-ttu-id="a9ec4-121">Especifica o nome do Servidor do AzureSQL que hospeda o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="a9ec4-121">Specifies the name of the AzureSQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="a9ec4-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a9ec4-122">-Confirm</span></span>
<span data-ttu-id="a9ec4-123">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9ec4-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9ec4-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9ec4-124">-WhatIf</span></span>
<span data-ttu-id="a9ec4-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a9ec4-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9ec4-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a9ec4-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9ec4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9ec4-127">CommonParameters</span></span>
<span data-ttu-id="a9ec4-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9ec4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9ec4-129">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a9ec4-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9ec4-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a9ec4-130">INPUTS</span></span>

### <span data-ttu-id="a9ec4-131">System.String</span><span class="sxs-lookup"><span data-stu-id="a9ec4-131">System.String</span></span>

## <span data-ttu-id="a9ec4-132">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a9ec4-132">OUTPUTS</span></span>

### <span data-ttu-id="a9ec4-133">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseRestorePointModel</span><span class="sxs-lookup"><span data-stu-id="a9ec4-133">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseRestorePointModel</span></span>

## <span data-ttu-id="a9ec4-134">NOTES</span><span class="sxs-lookup"><span data-stu-id="a9ec4-134">NOTES</span></span>

## <span data-ttu-id="a9ec4-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a9ec4-135">RELATED LINKS</span></span>
