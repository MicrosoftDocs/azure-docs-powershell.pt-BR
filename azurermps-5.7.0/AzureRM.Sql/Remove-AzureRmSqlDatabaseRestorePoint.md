---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 67A9BB67-EF14-4CAA-99D9-002D0D23178B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqldatabaserestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseRestorePoint.md
ms.openlocfilehash: 235165b178a721bf5e450a2430a6454eb3b2c1be
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432872"
---
# <span data-ttu-id="8e857-101">Remove-AzureRmSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="8e857-101">Remove-AzureRmSqlDatabaseRestorePoint</span></span>

## <span data-ttu-id="8e857-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8e857-102">SYNOPSIS</span></span>
<span data-ttu-id="8e857-103">Remove determinado ponto de restauração de um banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="8e857-103">Removes given restore point from a SQL Database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8e857-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8e857-104">SYNTAX</span></span>

```
Remove-AzureRmSqlDatabaseRestorePoint -RestorePointCreationDate <DateTime> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e857-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8e857-105">DESCRIPTION</span></span>
<span data-ttu-id="8e857-106">O cmdlet **Remove-AzureRmSqlDatabaseRestorePoint** remove um ponto de restauração fornecido do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="8e857-106">The **Remove-AzureRmSqlDatabaseRestorePoint** cmdlet removes given restore point from Azure SQL Database.</span></span>

<span data-ttu-id="8e857-107">No momento, esse cmdlet é compatível com o serviço SQL Server DataWarehouse no banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="8e857-107">This cmdlet is currently supported by the SQL Server Datawarehouse service on Azure SQL Database.</span></span>

## <span data-ttu-id="8e857-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8e857-108">EXAMPLES</span></span>

### <span data-ttu-id="8e857-109">Exemplo 1: Remove um ponto de restauração</span><span class="sxs-lookup"><span data-stu-id="8e857-109">Example 1: Removes a restore point</span></span>
```
PS C:\>$RestorePointCreationDate = Get-Date "3/11/2017 1:50:00 AM"
PS C:\>Remove-AzureRmSqlDatabaseRestorePoint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -RestorePointCreationDate $RestorePointCreationDate
```

<span data-ttu-id="8e857-110">Esse comando Remove um ponto de restauração para o banco de dados SQL do Azure determinada data de criação.</span><span class="sxs-lookup"><span data-stu-id="8e857-110">This command removes a restore point for Azure SQL Database given creation date.</span></span>

## <span data-ttu-id="8e857-111">OS</span><span class="sxs-lookup"><span data-stu-id="8e857-111">PARAMETERS</span></span>

### <span data-ttu-id="8e857-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8e857-112">-DatabaseName</span></span>
<span data-ttu-id="8e857-113">Especifica o nome do banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="8e857-113">Specifies the name of the SQL Database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e857-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e857-114">-DefaultProfile</span></span>
<span data-ttu-id="8e857-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="8e857-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e857-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e857-116">-ResourceGroupName</span></span>
<span data-ttu-id="8e857-117">Especifica o nome do grupo de recursos ao qual o banco de dados do SQL está atribuído.</span><span class="sxs-lookup"><span data-stu-id="8e857-117">Specifies the name of the resource group to which the SQL Database is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e857-118">-RestorePointCreationDate</span><span class="sxs-lookup"><span data-stu-id="8e857-118">-RestorePointCreationDate</span></span>
<span data-ttu-id="8e857-119">Especifica a data de criação do ponto de restauração.</span><span class="sxs-lookup"><span data-stu-id="8e857-119">Specifies the restore point creation date.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e857-120">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="8e857-120">-ServerName</span></span>
<span data-ttu-id="8e857-121">Especifica o nome do servidor AzureSQL que hospeda o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="8e857-121">Specifies the name of the AzureSQL Server that hosts the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e857-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8e857-122">-Confirm</span></span>
<span data-ttu-id="8e857-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e857-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e857-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e857-124">-WhatIf</span></span>
<span data-ttu-id="8e857-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8e857-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e857-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8e857-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e857-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e857-127">CommonParameters</span></span>
<span data-ttu-id="8e857-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e857-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e857-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e857-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e857-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8e857-130">INPUTS</span></span>

## <span data-ttu-id="8e857-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8e857-131">OUTPUTS</span></span>

## <span data-ttu-id="8e857-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8e857-132">NOTES</span></span>

## <span data-ttu-id="8e857-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8e857-133">RELATED LINKS</span></span>
