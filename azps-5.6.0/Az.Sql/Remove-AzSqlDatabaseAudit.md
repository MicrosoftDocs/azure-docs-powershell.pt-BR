---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/powershell/module/az.sql/Remove-AzSqlDatabaseAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseAudit.md
ms.openlocfilehash: 9688475a1d8bae19b10bc5626dca643ac947156d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886562"
---
# <span data-ttu-id="a0091-101">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="a0091-101">Remove-AzSqlDatabaseAudit</span></span>

## <span data-ttu-id="a0091-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0091-102">SYNOPSIS</span></span>
<span data-ttu-id="a0091-103">Remove as configurações de auditoria de um banco de dados SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="a0091-103">Removes the auditing settings of an Azure SQL database.</span></span>

## <span data-ttu-id="a0091-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a0091-104">SYNTAX</span></span>

### <span data-ttu-id="a0091-105">DatabaseParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a0091-105">DatabaseParameterSet (Default)</span></span>
```
Remove-AzSqlDatabaseAudit [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0091-106">DatabaseObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0091-106">DatabaseObjectParameterSet</span></span>
```
Remove-AzSqlDatabaseAudit -DatabaseObject <AzureSqlDatabaseModel> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0091-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a0091-107">DESCRIPTION</span></span>
<span data-ttu-id="a0091-108">O cmdlet **Remove-AzSqlDatabaseAudit** remove as configurações de auditoria de um banco de dados do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="a0091-108">The **Remove-AzSqlDatabaseAudit** cmdlet removes the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="a0091-109">Para usar o cmdlet, use os *parâmetros ResourceGroupName,* *ServerName* e *DatabaseName* para identificar o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="a0091-109">To use the cmdlet, use the *ResourceGroupName*, *ServerName*, and *DatabaseName* parameters to identify the database.</span></span>

## <span data-ttu-id="a0091-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a0091-110">EXAMPLES</span></span>

### <span data-ttu-id="a0091-111">Exemplo 1: Remover as configurações de auditoria de um banco de dados SQL Azure</span><span class="sxs-lookup"><span data-stu-id="a0091-111">Example 1: Remove the auditing settings of an Azure SQL database</span></span>
```
PS C:\>Remove-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

### <span data-ttu-id="a0091-112">Exemplo 2: Remover, por pipeline, as configurações de auditoria de um banco de dados SQL Azure</span><span class="sxs-lookup"><span data-stu-id="a0091-112">Example 2: Remove, through pipeline, the auditing settings of an Azure SQL database</span></span>
```
PS C:\> Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" | Remove-AzSqlDatabaseAudit
```

## <span data-ttu-id="a0091-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a0091-113">PARAMETERS</span></span>

### <span data-ttu-id="a0091-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a0091-114">-DatabaseName</span></span>
<span data-ttu-id="a0091-115">SQL Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="a0091-115">SQL Database name.</span></span>

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

### <span data-ttu-id="a0091-116">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="a0091-116">-DatabaseObject</span></span>
<span data-ttu-id="a0091-117">O objeto database para gerenciar sua política de auditoria.</span><span class="sxs-lookup"><span data-stu-id="a0091-117">The database object to manage its audit policy.</span></span>

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

### <span data-ttu-id="a0091-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0091-118">-DefaultProfile</span></span>
<span data-ttu-id="a0091-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a0091-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0091-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0091-120">-ResourceGroupName</span></span>
<span data-ttu-id="a0091-121">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a0091-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="a0091-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a0091-122">-ServerName</span></span>
<span data-ttu-id="a0091-123">SQL nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="a0091-123">SQL server name.</span></span>

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

### <span data-ttu-id="a0091-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a0091-124">-Confirm</span></span>
<span data-ttu-id="a0091-125">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0091-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0091-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0091-126">-WhatIf</span></span>
<span data-ttu-id="a0091-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a0091-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a0091-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a0091-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0091-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0091-129">CommonParameters</span></span>
<span data-ttu-id="a0091-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0091-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0091-131">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a0091-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0091-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a0091-132">INPUTS</span></span>

### <span data-ttu-id="a0091-133">System.String</span><span class="sxs-lookup"><span data-stu-id="a0091-133">System.String</span></span>

### <span data-ttu-id="a0091-134">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="a0091-134">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="a0091-135">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a0091-135">OUTPUTS</span></span>

### <span data-ttu-id="a0091-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a0091-136">System.Boolean</span></span>

## <span data-ttu-id="a0091-137">NOTES</span><span class="sxs-lookup"><span data-stu-id="a0091-137">NOTES</span></span>

## <span data-ttu-id="a0091-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a0091-138">RELATED LINKS</span></span>
