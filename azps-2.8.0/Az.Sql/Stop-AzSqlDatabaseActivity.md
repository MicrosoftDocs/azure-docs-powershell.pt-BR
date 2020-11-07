---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B5C909D7-6087-463A-83BF-99DD196B9862
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/stop-azsqldatabaseactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlDatabaseActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlDatabaseActivity.md
ms.openlocfilehash: f4f3b935aa9303ab38888d6f28f0a89bbdeb6c23
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773939"
---
# <span data-ttu-id="29dc4-101">Stop-AzSqlDatabaseActivity</span><span class="sxs-lookup"><span data-stu-id="29dc4-101">Stop-AzSqlDatabaseActivity</span></span>

## <span data-ttu-id="29dc4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="29dc4-102">SYNOPSIS</span></span>
<span data-ttu-id="29dc4-103">Cancela a operação de atualizações assíncronas no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="29dc4-103">Cancels the asynchronous updates operation on the database.</span></span>

## <span data-ttu-id="29dc4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="29dc4-104">SYNTAX</span></span>

```
Stop-AzSqlDatabaseActivity [-ServerName] <String> [-ElasticPoolName <String>] -DatabaseName <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29dc4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="29dc4-105">DESCRIPTION</span></span>
<span data-ttu-id="29dc4-106">O cmdlet **Stop-AzSqlDatabaseActivity** cancela a operação de atualizações assíncronas no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="29dc4-106">The **Stop-AzSqlDatabaseActivity** cmdlet cancels the asynchronous updates operation on the database.</span></span>

## <span data-ttu-id="29dc4-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="29dc4-107">EXAMPLES</span></span>

### <span data-ttu-id="29dc4-108">Exemplo 1: cancelar a operação de atualizações assíncronas no banco de dados</span><span class="sxs-lookup"><span data-stu-id="29dc4-108">Example 1: Cancel the asynchronous updates operation on the database</span></span>
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

<span data-ttu-id="29dc4-109">Esse comando cancela a operação de atualizações assíncronas no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="29dc4-109">This command cancels the asynchronous updates operation on the database.</span></span>

## <span data-ttu-id="29dc4-110">OS</span><span class="sxs-lookup"><span data-stu-id="29dc4-110">PARAMETERS</span></span>

### <span data-ttu-id="29dc4-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="29dc4-111">-DatabaseName</span></span>
<span data-ttu-id="29dc4-112">Especifica o nome do banco de dados para o qual esse cmdlet obtém o status.</span><span class="sxs-lookup"><span data-stu-id="29dc4-112">Specifies the name of the database for which this cmdlet gets status.</span></span>

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

### <span data-ttu-id="29dc4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29dc4-113">-DefaultProfile</span></span>
<span data-ttu-id="29dc4-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="29dc4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="29dc4-115">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="29dc4-115">-ElasticPoolName</span></span>
<span data-ttu-id="29dc4-116">O nome do pool elástico do SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="29dc4-116">The name of the Azure SQL Elastic Pool.</span></span>

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

### <span data-ttu-id="29dc4-117">-OperationId</span><span class="sxs-lookup"><span data-stu-id="29dc4-117">-OperationId</span></span>
<span data-ttu-id="29dc4-118">Especifica a ID da operação que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="29dc4-118">Specifies the ID of the operation that this cmdlet gets.</span></span>

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

### <span data-ttu-id="29dc4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29dc4-119">-ResourceGroupName</span></span>
<span data-ttu-id="29dc4-120">Especifica o nome do grupo de recursos ao qual o banco de dados está atribuído.</span><span class="sxs-lookup"><span data-stu-id="29dc4-120">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="29dc4-121">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="29dc4-121">-ServerName</span></span>
<span data-ttu-id="29dc4-122">Especifica o nome do Microsoft SQL Server que hospeda o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="29dc4-122">Specifies the name of the Microsoft SQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="29dc4-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="29dc4-123">-Confirm</span></span>
<span data-ttu-id="29dc4-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="29dc4-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29dc4-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29dc4-125">-WhatIf</span></span>
<span data-ttu-id="29dc4-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="29dc4-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29dc4-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="29dc4-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29dc4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29dc4-128">CommonParameters</span></span>
<span data-ttu-id="29dc4-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29dc4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29dc4-130">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="29dc4-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29dc4-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="29dc4-131">INPUTS</span></span>

### <span data-ttu-id="29dc4-132">System. String</span><span class="sxs-lookup"><span data-stu-id="29dc4-132">System.String</span></span>

### <span data-ttu-id="29dc4-133">System. Nullable ' 1 [[System. GUID, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="29dc4-133">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="29dc4-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="29dc4-134">OUTPUTS</span></span>

### <span data-ttu-id="29dc4-135">Microsoft. Azure. Commands. Sql. Database. Model. AzureSqlDatabaseActivityModel</span><span class="sxs-lookup"><span data-stu-id="29dc4-135">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel</span></span>

## <span data-ttu-id="29dc4-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="29dc4-136">NOTES</span></span>

## <span data-ttu-id="29dc4-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="29dc4-137">RELATED LINKS</span></span>
