---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: FFC02A5D-A12F-494D-8542-76A5B89E32DC
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldatabasedatamaskingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseDataMaskingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseDataMaskingPolicy.md
ms.openlocfilehash: d84a954fc6ca6531f1f485baf2cd8006c8a509bb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885510"
---
# <span data-ttu-id="5ac57-101">Get-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="5ac57-101">Get-AzSqlDatabaseDataMaskingPolicy</span></span>

## <span data-ttu-id="5ac57-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ac57-102">SYNOPSIS</span></span>
<span data-ttu-id="5ac57-103">Obtém a política de mascaramento de dados para um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="5ac57-103">Gets the data masking policy for a database.</span></span>

## <span data-ttu-id="5ac57-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="5ac57-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseDataMaskingPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5ac57-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="5ac57-105">DESCRIPTION</span></span>
<span data-ttu-id="5ac57-106">O cmdlet **Get-AzSqlDatabaseDataMaskingPolicy** obtém a política de mascaramento de dados de um banco de dados do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="5ac57-106">The **Get-AzSqlDatabaseDataMaskingPolicy** cmdlet gets the data masking policy of an Azure SQL database.</span></span>
<span data-ttu-id="5ac57-107">Para usar esse cmdlet, use os *parâmetros ResourceGroupName,* *ServerName* e *DatabaseName* para identificar o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="5ac57-107">To use this cmdlet, use the *ResourceGroupName*, *ServerName*, and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="5ac57-108">Esse cmdlet também é suportado pelo serviço SQL Server Banco de Dados de Extensão no Azure.</span><span class="sxs-lookup"><span data-stu-id="5ac57-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="5ac57-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5ac57-109">EXAMPLES</span></span>

### <span data-ttu-id="5ac57-110">Exemplo 1: Obter a política de mascaramento de dados para um banco de dados SQL Azure</span><span class="sxs-lookup"><span data-stu-id="5ac57-110">Example 1: Get the data masking policy for an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseDataMaskingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName      : Database01
ResourceGroupName : ResourceGroup01
ServerName        : Server01
DataMaskingState  : Enabled
PrivilegedUsers  :
```

<span data-ttu-id="5ac57-111">Este comando obtém a política de mascaramento de dados do banco de dados01 no grupo de recursos ResourceGroup01 no servidor Server01.</span><span class="sxs-lookup"><span data-stu-id="5ac57-111">This command gets the data masking policy from database Database01 in resource group ResourceGroup01 on server Server01.</span></span>

## <span data-ttu-id="5ac57-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="5ac57-112">PARAMETERS</span></span>

### <span data-ttu-id="5ac57-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5ac57-113">-DatabaseName</span></span>
<span data-ttu-id="5ac57-114">Especifica o nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="5ac57-114">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="5ac57-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ac57-115">-DefaultProfile</span></span>
<span data-ttu-id="5ac57-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="5ac57-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5ac57-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ac57-117">-ResourceGroupName</span></span>
<span data-ttu-id="5ac57-118">Especifica o nome do grupo de recursos ao qual o banco de dados é atribuído.</span><span class="sxs-lookup"><span data-stu-id="5ac57-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="5ac57-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5ac57-119">-ServerName</span></span>
<span data-ttu-id="5ac57-120">Especifica o nome do servidor onde o banco de dados está localizado.</span><span class="sxs-lookup"><span data-stu-id="5ac57-120">Specifies the name of the server where the database is located.</span></span>

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

### <span data-ttu-id="5ac57-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5ac57-121">-Confirm</span></span>
<span data-ttu-id="5ac57-122">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ac57-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ac57-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ac57-123">-WhatIf</span></span>
<span data-ttu-id="5ac57-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5ac57-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ac57-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5ac57-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ac57-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ac57-126">CommonParameters</span></span>
<span data-ttu-id="5ac57-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ac57-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ac57-128">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5ac57-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ac57-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5ac57-129">INPUTS</span></span>

### <span data-ttu-id="5ac57-130">System.String</span><span class="sxs-lookup"><span data-stu-id="5ac57-130">System.String</span></span>

## <span data-ttu-id="5ac57-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="5ac57-131">OUTPUTS</span></span>

### <span data-ttu-id="5ac57-132">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="5ac57-132">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingPolicyModel</span></span>

## <span data-ttu-id="5ac57-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="5ac57-133">NOTES</span></span>

## <span data-ttu-id="5ac57-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5ac57-134">RELATED LINKS</span></span>

[<span data-ttu-id="5ac57-135">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="5ac57-135">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="5ac57-136">New-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="5ac57-136">New-AzSqlDatabaseDataMaskingRule</span></span>](./New-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="5ac57-137">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="5ac57-137">Remove-AzSqlDatabaseDataMaskingRule</span></span>](./Remove-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="5ac57-138">Set-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="5ac57-138">Set-AzSqlDatabaseDataMaskingPolicy</span></span>](./Set-AzSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="5ac57-139">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="5ac57-139">Set-AzSqlDatabaseDataMaskingRule</span></span>](./Set-AzSqlDatabaseDataMaskingRule.md)


