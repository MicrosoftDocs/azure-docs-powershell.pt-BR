---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 67A9BB67-CF17-4CAA-99D9-002D0D23178B
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaserestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseRestorePoint.md
ms.openlocfilehash: 9765afd55ea94bda672d5e1ce43ac3d8d535510d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941627"
---
# <span data-ttu-id="520d1-101">Get-AzSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="520d1-101">Get-AzSqlDatabaseRestorePoint</span></span>

## <span data-ttu-id="520d1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="520d1-102">SYNOPSIS</span></span>
<span data-ttu-id="520d1-103">Recupera os pontos de restauração distintos a partir dos quais um data warehouse do SQL pode ser restaurado.</span><span class="sxs-lookup"><span data-stu-id="520d1-103">Retrieves the distinct restore points from which a SQL Data Warehouse can be restored.</span></span>

## <span data-ttu-id="520d1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="520d1-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseRestorePoint [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="520d1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="520d1-105">DESCRIPTION</span></span>
<span data-ttu-id="520d1-106">O cmdlet **Get-AzSqlDatabaseRestorePoint** recupera os pontos de restauração distintos nos quais um SQL data warehouse do Azure pode ser restaurado.</span><span class="sxs-lookup"><span data-stu-id="520d1-106">The **Get-AzSqlDatabaseRestorePoint** cmdlet retrieves the distinct restore points that an Azure SQL Data Warehouse can be restored from.</span></span>
<span data-ttu-id="520d1-107">Para um banco de dados SQL do Azure, a janela restaurar é contínua.</span><span class="sxs-lookup"><span data-stu-id="520d1-107">For an Azure SQL Database, the restore window is continuous.</span></span>
<span data-ttu-id="520d1-108">Isso significa que qualquer point-in-time no período de retenção de backup do banco de dados pode ser usado como um ponto de restauração.</span><span class="sxs-lookup"><span data-stu-id="520d1-108">This means that any point in time in the backup retention period of the database can be used as a restore point.</span></span>
<span data-ttu-id="520d1-109">Esse cmdlet também é compatível com o serviço Stretch Database do SQL Server no Azure.</span><span class="sxs-lookup"><span data-stu-id="520d1-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="520d1-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="520d1-110">EXAMPLES</span></span>

### <span data-ttu-id="520d1-111">Exemplo 1: obter todos os pontos de restauração</span><span class="sxs-lookup"><span data-stu-id="520d1-111">Example 1: Get all restore points</span></span>
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

<span data-ttu-id="520d1-112">Esse comando retorna todos os pontos de restauração disponíveis para o banco de dados SQL do Azure chamado Database01.</span><span class="sxs-lookup"><span data-stu-id="520d1-112">This command returns all available restore points for the Azure SQL Database named Database01.</span></span>

## <span data-ttu-id="520d1-113">OS</span><span class="sxs-lookup"><span data-stu-id="520d1-113">PARAMETERS</span></span>

### <span data-ttu-id="520d1-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="520d1-114">-DatabaseName</span></span>
<span data-ttu-id="520d1-115">Especifica o nome do banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="520d1-115">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="520d1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="520d1-116">-DefaultProfile</span></span>
<span data-ttu-id="520d1-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="520d1-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="520d1-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="520d1-118">-ResourceGroupName</span></span>
<span data-ttu-id="520d1-119">Especifica o nome do grupo de recursos ao qual o banco de dados do SQL está atribuído.</span><span class="sxs-lookup"><span data-stu-id="520d1-119">Specifies the name of the resource group to which the SQL Database is assigned.</span></span>

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

### <span data-ttu-id="520d1-120">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="520d1-120">-ServerName</span></span>
<span data-ttu-id="520d1-121">Especifica o nome do servidor AzureSQL que hospeda o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="520d1-121">Specifies the name of the AzureSQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="520d1-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="520d1-122">-Confirm</span></span>
<span data-ttu-id="520d1-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="520d1-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="520d1-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="520d1-124">-WhatIf</span></span>
<span data-ttu-id="520d1-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="520d1-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="520d1-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="520d1-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="520d1-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="520d1-127">CommonParameters</span></span>
<span data-ttu-id="520d1-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="520d1-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="520d1-129">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="520d1-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="520d1-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="520d1-130">INPUTS</span></span>

### <span data-ttu-id="520d1-131">System. String</span><span class="sxs-lookup"><span data-stu-id="520d1-131">System.String</span></span>

## <span data-ttu-id="520d1-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="520d1-132">OUTPUTS</span></span>

### <span data-ttu-id="520d1-133">Microsoft. Azure. Commands. Sql. backup. Model. AzureSqlDatabaseRestorePointModel</span><span class="sxs-lookup"><span data-stu-id="520d1-133">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseRestorePointModel</span></span>

## <span data-ttu-id="520d1-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="520d1-134">NOTES</span></span>

## <span data-ttu-id="520d1-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="520d1-135">RELATED LINKS</span></span>
