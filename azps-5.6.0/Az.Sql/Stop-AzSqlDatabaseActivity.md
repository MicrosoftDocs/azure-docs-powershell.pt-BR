---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B5C909D7-6087-463A-83BF-99DD196B9862
online version: https://docs.microsoft.com/powershell/module/az.sql/stop-azsqldatabaseactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlDatabaseActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlDatabaseActivity.md
ms.openlocfilehash: 014cd61e53f002a2615153103ddcbb0b966751a7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892709"
---
# <span data-ttu-id="37f33-101">Stop-AzSqlDatabaseActivity</span><span class="sxs-lookup"><span data-stu-id="37f33-101">Stop-AzSqlDatabaseActivity</span></span>

## <span data-ttu-id="37f33-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37f33-102">SYNOPSIS</span></span>
<span data-ttu-id="37f33-103">Cancela a operação de atualizações assíncronas no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="37f33-103">Cancels the asynchronous updates operation on the database.</span></span>

## <span data-ttu-id="37f33-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="37f33-104">SYNTAX</span></span>

```
Stop-AzSqlDatabaseActivity [-ServerName] <String> [-ElasticPoolName <String>] -DatabaseName <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37f33-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="37f33-105">DESCRIPTION</span></span>
<span data-ttu-id="37f33-106">O cmdlet **Stop-AzSqlDatabaseActivity** cancela a operação de atualizações assíncronas no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="37f33-106">The **Stop-AzSqlDatabaseActivity** cmdlet cancels the asynchronous updates operation on the database.</span></span>

## <span data-ttu-id="37f33-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="37f33-107">EXAMPLES</span></span>

### <span data-ttu-id="37f33-108">Exemplo 1: Cancelar a operação de atualizações assíncronas no banco de dados</span><span class="sxs-lookup"><span data-stu-id="37f33-108">Example 1: Cancel the asynchronous updates operation on the database</span></span>
```
PS C:\>Stop-AzSqlDatabaseActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -OperationId af97005d-9243-4f8a-844e-402d1cc855f5

OperationId     : af97005d-9243-4f8a-844e-402d1cc855f5
ServerName      : Server01
DatabaseName    : Database01
State           : CANCELLED
Operation       : UpdateLogicalDatabase
ErrorCode       :
ErrorMessage    :
ErrorSeverity   :
StartTime       : 10/15/2017 02:49:42 PM
EndTime         : 10/15/2017 02:49:43 PM
PercentComplete : 
Properties      : Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel+DatabaseState
```

<span data-ttu-id="37f33-109">Esse comando cancela a operação de atualizações assíncronas no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="37f33-109">This command cancels the asynchronous updates operation on the database.</span></span>

## <span data-ttu-id="37f33-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="37f33-110">PARAMETERS</span></span>

### <span data-ttu-id="37f33-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="37f33-111">-DatabaseName</span></span>
<span data-ttu-id="37f33-112">Especifica o nome do banco de dados para o qual este cmdlet obtém status.</span><span class="sxs-lookup"><span data-stu-id="37f33-112">Specifies the name of the database for which this cmdlet gets status.</span></span>

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

### <span data-ttu-id="37f33-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37f33-113">-DefaultProfile</span></span>
<span data-ttu-id="37f33-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="37f33-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="37f33-115">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="37f33-115">-ElasticPoolName</span></span>
<span data-ttu-id="37f33-116">O nome do Pool Elástica do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="37f33-116">The name of the Azure SQL Elastic Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37f33-117">-OperationId</span><span class="sxs-lookup"><span data-stu-id="37f33-117">-OperationId</span></span>
<span data-ttu-id="37f33-118">Especifica a ID da operação que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="37f33-118">Specifies the ID of the operation that this cmdlet gets.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37f33-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37f33-119">-ResourceGroupName</span></span>
<span data-ttu-id="37f33-120">Especifica o nome do grupo de recursos ao qual o banco de dados é atribuído.</span><span class="sxs-lookup"><span data-stu-id="37f33-120">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="37f33-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="37f33-121">-ServerName</span></span>
<span data-ttu-id="37f33-122">Especifica o nome do Microsoft SQL Server que hospeda o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="37f33-122">Specifies the name of the Microsoft SQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="37f33-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="37f33-123">-Confirm</span></span>
<span data-ttu-id="37f33-124">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37f33-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37f33-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37f33-125">-WhatIf</span></span>
<span data-ttu-id="37f33-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="37f33-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37f33-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="37f33-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37f33-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37f33-128">CommonParameters</span></span>
<span data-ttu-id="37f33-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37f33-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37f33-130">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="37f33-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37f33-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="37f33-131">INPUTS</span></span>

### <span data-ttu-id="37f33-132">System.String</span><span class="sxs-lookup"><span data-stu-id="37f33-132">System.String</span></span>

### <span data-ttu-id="37f33-133">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="37f33-133">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="37f33-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="37f33-134">OUTPUTS</span></span>

### <span data-ttu-id="37f33-135">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel</span><span class="sxs-lookup"><span data-stu-id="37f33-135">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel</span></span>

## <span data-ttu-id="37f33-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="37f33-136">NOTES</span></span>

## <span data-ttu-id="37f33-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="37f33-137">RELATED LINKS</span></span>
