---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 67A9BB67-CF17-4CAA-99D9-002D0D23178B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabaserestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseRestorePoint.md
ms.openlocfilehash: dad714b617f6b3c493d19b2275dcf7eeef14a2d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431296"
---
# <span data-ttu-id="ad99a-101">New-AzureRmSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="ad99a-101">New-AzureRmSqlDatabaseRestorePoint</span></span>

## <span data-ttu-id="ad99a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ad99a-102">SYNOPSIS</span></span>
<span data-ttu-id="ad99a-103">Cria um novo ponto de restauração a partir do qual um banco de dados SQL pode ser restaurado.</span><span class="sxs-lookup"><span data-stu-id="ad99a-103">Creates a new restore point from which a SQL Database can be restored.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad99a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ad99a-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseRestorePoint -RestorePointLabel <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ad99a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ad99a-105">DESCRIPTION</span></span>
<span data-ttu-id="ad99a-106">O cmdlet **New-AzureRmSqlDatabaseRestorePoint** cria um novo ponto de restauração no qual um SQL data warehouse do Azure pode ser restaurado.</span><span class="sxs-lookup"><span data-stu-id="ad99a-106">The **New-AzureRmSqlDatabaseRestorePoint** cmdlet creates a new restore point that an Azure SQL Data Warehouse can be restored from.</span></span>
<span data-ttu-id="ad99a-107">Este cmdlet tem suporte no momento para SQL data warehouse do Azure.</span><span class="sxs-lookup"><span data-stu-id="ad99a-107">This cmdlet is currently supported for Azure SQL Data Warehouse.</span></span>

## <span data-ttu-id="ad99a-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ad99a-108">EXAMPLES</span></span>

### <span data-ttu-id="ad99a-109">Exemplo 1: criar um ponto de restauração</span><span class="sxs-lookup"><span data-stu-id="ad99a-109">Example 1: Create a restore point</span></span>
```
PS C:\>New-AzureRmSqlDatabaseRestorePoint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -RestorePointLabel "RestorePoint01"
ResourceGroupName        : resourcegroup01
ServerName               : server01
DatabaseName             : database01
Location                 : Central US
RestorePointType         : DISCRETE
RestorePointCreationDate : 8/12/2015 12:00:00 AM
EarliestRestoreDate      : 
RestorePointLabel        : RestorePoint01
```

<span data-ttu-id="ad99a-110">Esse comando cria um ponto de restauração para o SQL data warehouse do Azure e retorna os detalhes do ponto de restauração.</span><span class="sxs-lookup"><span data-stu-id="ad99a-110">This command creates a restore point for Azure SQL Data Warehouse and returns the details of the restore point.</span></span>

## <span data-ttu-id="ad99a-111">OS</span><span class="sxs-lookup"><span data-stu-id="ad99a-111">PARAMETERS</span></span>

### <span data-ttu-id="ad99a-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ad99a-112">-DatabaseName</span></span>
<span data-ttu-id="ad99a-113">Especifica o nome do banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="ad99a-113">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="ad99a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad99a-114">-DefaultProfile</span></span>
<span data-ttu-id="ad99a-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="ad99a-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ad99a-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad99a-116">-ResourceGroupName</span></span>
<span data-ttu-id="ad99a-117">Especifica o nome do grupo de recursos ao qual o banco de dados do SQL está atribuído.</span><span class="sxs-lookup"><span data-stu-id="ad99a-117">Specifies the name of the resource group to which the SQL Database is assigned.</span></span>

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

### <span data-ttu-id="ad99a-118">-RestorePointLabel</span><span class="sxs-lookup"><span data-stu-id="ad99a-118">-RestorePointLabel</span></span>
<span data-ttu-id="ad99a-119">Especifica o rótulo do ponto de restauração para facilitar a identificação.</span><span class="sxs-lookup"><span data-stu-id="ad99a-119">Specifies the label of the restore point for easy identification.</span></span>

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

### <span data-ttu-id="ad99a-120">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="ad99a-120">-ServerName</span></span>
<span data-ttu-id="ad99a-121">Especifica o nome do servidor AzureSQL que hospeda o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="ad99a-121">Specifies the name of the AzureSQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="ad99a-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ad99a-122">-Confirm</span></span>
<span data-ttu-id="ad99a-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad99a-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad99a-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad99a-124">-WhatIf</span></span>
<span data-ttu-id="ad99a-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ad99a-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad99a-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ad99a-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad99a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad99a-127">CommonParameters</span></span>
<span data-ttu-id="ad99a-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad99a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad99a-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad99a-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad99a-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ad99a-130">INPUTS</span></span>

### <span data-ttu-id="ad99a-131">System. String</span><span class="sxs-lookup"><span data-stu-id="ad99a-131">System.String</span></span>

## <span data-ttu-id="ad99a-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ad99a-132">OUTPUTS</span></span>

### <span data-ttu-id="ad99a-133">Microsoft. Azure. Commands. Sql. backup. Model. AzureSqlDatabaseRestorePointModel</span><span class="sxs-lookup"><span data-stu-id="ad99a-133">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseRestorePointModel</span></span>

## <span data-ttu-id="ad99a-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ad99a-134">NOTES</span></span>

## <span data-ttu-id="ad99a-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ad99a-135">RELATED LINKS</span></span>
