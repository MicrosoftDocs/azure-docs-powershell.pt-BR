---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 67A9BB67-CF17-4CAA-99D9-002D0D23178B
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldatabaserestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseRestorePoint.md
ms.openlocfilehash: aefcbe869dd8564e2225d478e95980558ba67bb3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901420"
---
# <span data-ttu-id="8c862-101">Get-AzSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="8c862-101">Get-AzSqlDatabaseRestorePoint</span></span>

## <span data-ttu-id="8c862-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c862-102">SYNOPSIS</span></span>
<span data-ttu-id="8c862-103">Recupera os pontos de restauração distintos dos quais um Data Warehouse SQL pode ser restaurado.</span><span class="sxs-lookup"><span data-stu-id="8c862-103">Retrieves the distinct restore points from which a SQL Data Warehouse can be restored.</span></span>

## <span data-ttu-id="8c862-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="8c862-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseRestorePoint [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c862-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="8c862-105">DESCRIPTION</span></span>
<span data-ttu-id="8c862-106">O cmdlet **Get-AzSqlDatabaseRestorePoint** recupera os pontos de restauração distintos dos que um Data Warehouse do Azure SQL pode ser restaurado.</span><span class="sxs-lookup"><span data-stu-id="8c862-106">The **Get-AzSqlDatabaseRestorePoint** cmdlet retrieves the distinct restore points that an Azure SQL Data Warehouse can be restored from.</span></span>
<span data-ttu-id="8c862-107">Para um banco de dados do Azure SQL, a janela de restauração é contínua.</span><span class="sxs-lookup"><span data-stu-id="8c862-107">For an Azure SQL Database, the restore window is continuous.</span></span>
<span data-ttu-id="8c862-108">Isso significa que qualquer ponto no tempo no período de retenção de backup do banco de dados pode ser usado como um ponto de restauração.</span><span class="sxs-lookup"><span data-stu-id="8c862-108">This means that any point in time in the backup retention period of the database can be used as a restore point.</span></span>
<span data-ttu-id="8c862-109">Esse cmdlet também é suportado pelo serviço SQL Server Banco de Dados de Extensão no Azure.</span><span class="sxs-lookup"><span data-stu-id="8c862-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="8c862-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8c862-110">EXAMPLES</span></span>

### <span data-ttu-id="8c862-111">Exemplo 1: Obter todos os pontos de restauração</span><span class="sxs-lookup"><span data-stu-id="8c862-111">Example 1: Get all restore points</span></span>
```
PS C:\>Get-AzSqlDatabaseRestorePoint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
ResourceGroupName        : resourcegroup01
ServerName               : server01
DatabaseName             : database01
Location                 : Central US
RestorePointType         : CONTINUOUS
RestorePointCreationDate : 
EarliestRestoreDate      : 8/12/2015 12:00:00 AM
RestorePointLabel        : RestorePoint01
```

<span data-ttu-id="8c862-112">Este comando retorna todos os pontos de restauração disponíveis para o banco de dados SQL do Azure chamado Database01.</span><span class="sxs-lookup"><span data-stu-id="8c862-112">This command returns all available restore points for the Azure SQL Database named Database01.</span></span>

## <span data-ttu-id="8c862-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="8c862-113">PARAMETERS</span></span>

### <span data-ttu-id="8c862-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8c862-114">-DatabaseName</span></span>
<span data-ttu-id="8c862-115">Especifica o nome do banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="8c862-115">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="8c862-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c862-116">-DefaultProfile</span></span>
<span data-ttu-id="8c862-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="8c862-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8c862-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c862-118">-ResourceGroupName</span></span>
<span data-ttu-id="8c862-119">Especifica o nome do grupo de recursos ao qual o banco de dados SQL é atribuído.</span><span class="sxs-lookup"><span data-stu-id="8c862-119">Specifies the name of the resource group to which the SQL Database is assigned.</span></span>

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

### <span data-ttu-id="8c862-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="8c862-120">-ServerName</span></span>
<span data-ttu-id="8c862-121">Especifica o nome do Servidor do AzureSQL que hospeda o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="8c862-121">Specifies the name of the AzureSQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="8c862-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8c862-122">-Confirm</span></span>
<span data-ttu-id="8c862-123">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8c862-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c862-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c862-124">-WhatIf</span></span>
<span data-ttu-id="8c862-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8c862-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c862-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8c862-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c862-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c862-127">CommonParameters</span></span>
<span data-ttu-id="8c862-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c862-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c862-129">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8c862-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c862-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8c862-130">INPUTS</span></span>

### <span data-ttu-id="8c862-131">System.String</span><span class="sxs-lookup"><span data-stu-id="8c862-131">System.String</span></span>

## <span data-ttu-id="8c862-132">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="8c862-132">OUTPUTS</span></span>

### <span data-ttu-id="8c862-133">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseRestorePointModel</span><span class="sxs-lookup"><span data-stu-id="8c862-133">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseRestorePointModel</span></span>

## <span data-ttu-id="8c862-134">NOTES</span><span class="sxs-lookup"><span data-stu-id="8c862-134">NOTES</span></span>

## <span data-ttu-id="8c862-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8c862-135">RELATED LINKS</span></span>
