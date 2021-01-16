---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Remove-AzSqlDatabaseAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseAudit.md
ms.openlocfilehash: caca08a5a9390d3e80fdef8309244a8a4d29aec0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98257401"
---
# <span data-ttu-id="3fd24-101">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="3fd24-101">Remove-AzSqlDatabaseAudit</span></span>

## <span data-ttu-id="3fd24-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3fd24-102">SYNOPSIS</span></span>
<span data-ttu-id="3fd24-103">Remove as configurações de auditoria de um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="3fd24-103">Removes the auditing settings of an Azure SQL database.</span></span>

## <span data-ttu-id="3fd24-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3fd24-104">SYNTAX</span></span>

### <span data-ttu-id="3fd24-105">DatabaseParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="3fd24-105">DatabaseParameterSet (Default)</span></span>
```
Remove-AzSqlDatabaseAudit [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3fd24-106">DatabaseObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3fd24-106">DatabaseObjectParameterSet</span></span>
```
Remove-AzSqlDatabaseAudit -DatabaseObject <AzureSqlDatabaseModel> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3fd24-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3fd24-107">DESCRIPTION</span></span>
<span data-ttu-id="3fd24-108">O cmdlet **Remove-AzSqlDatabaseAudit** remove as configurações de auditoria de um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="3fd24-108">The **Remove-AzSqlDatabaseAudit** cmdlet removes the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="3fd24-109">Para usar o cmdlet, use os parâmetros *ResourceGroupName*, *ServerName* e *DatabaseName* para identificar o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="3fd24-109">To use the cmdlet, use the *ResourceGroupName*, *ServerName*, and *DatabaseName* parameters to identify the database.</span></span>

## <span data-ttu-id="3fd24-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3fd24-110">EXAMPLES</span></span>

### <span data-ttu-id="3fd24-111">Exemplo 1: remover as configurações de auditoria de um banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="3fd24-111">Example 1: Remove the auditing settings of an Azure SQL database</span></span>
```
PS C:\>Remove-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

### <span data-ttu-id="3fd24-112">Exemplo 2: remover, por meio de pipeline, as configurações de auditoria de um banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="3fd24-112">Example 2: Remove, through pipeline, the auditing settings of an Azure SQL database</span></span>
```
PS C:\> Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" | Remove-AzSqlDatabaseAudit
```

## <span data-ttu-id="3fd24-113">OS</span><span class="sxs-lookup"><span data-stu-id="3fd24-113">PARAMETERS</span></span>

### <span data-ttu-id="3fd24-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3fd24-114">-DatabaseName</span></span>
<span data-ttu-id="3fd24-115">Nome do banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="3fd24-115">SQL Database name.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fd24-116">-Databaseobject</span><span class="sxs-lookup"><span data-stu-id="3fd24-116">-DatabaseObject</span></span>
<span data-ttu-id="3fd24-117">O objeto de banco de dados para gerenciar sua política de auditoria.</span><span class="sxs-lookup"><span data-stu-id="3fd24-117">The database object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: DatabaseObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3fd24-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fd24-118">-DefaultProfile</span></span>
<span data-ttu-id="3fd24-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3fd24-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3fd24-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3fd24-120">-ResourceGroupName</span></span>
<span data-ttu-id="3fd24-121">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3fd24-121">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fd24-122">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="3fd24-122">-ServerName</span></span>
<span data-ttu-id="3fd24-123">Nome do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="3fd24-123">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fd24-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3fd24-124">-Confirm</span></span>
<span data-ttu-id="3fd24-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3fd24-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fd24-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3fd24-126">-WhatIf</span></span>
<span data-ttu-id="3fd24-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3fd24-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3fd24-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3fd24-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fd24-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fd24-129">CommonParameters</span></span>
<span data-ttu-id="3fd24-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3fd24-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fd24-131">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3fd24-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fd24-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3fd24-132">INPUTS</span></span>

### <span data-ttu-id="3fd24-133">System. String</span><span class="sxs-lookup"><span data-stu-id="3fd24-133">System.String</span></span>

### <span data-ttu-id="3fd24-134">Microsoft. Azure. Commands. Sql. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="3fd24-134">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="3fd24-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3fd24-135">OUTPUTS</span></span>

### <span data-ttu-id="3fd24-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3fd24-136">System.Boolean</span></span>

## <span data-ttu-id="3fd24-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3fd24-137">NOTES</span></span>

## <span data-ttu-id="3fd24-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3fd24-138">RELATED LINKS</span></span>
