---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: B5C909D7-6087-463A-83BF-99DD196B9862
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/stop-azurermsqldatabaseactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlDatabaseActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlDatabaseActivity.md
ms.openlocfilehash: af2f10b371eb21558a4b675331ec97f797611d26
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429286"
---
# <span data-ttu-id="4b1a8-101">Stop-AzureRmSqlDatabaseActivity</span><span class="sxs-lookup"><span data-stu-id="4b1a8-101">Stop-AzureRmSqlDatabaseActivity</span></span>

## <span data-ttu-id="4b1a8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4b1a8-102">SYNOPSIS</span></span>
<span data-ttu-id="4b1a8-103">Cancela a operação de atualizações assíncronas no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="4b1a8-103">Cancels the asynchronous updates operation on the database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4b1a8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4b1a8-104">SYNTAX</span></span>

```
Stop-AzureRmSqlDatabaseActivity [-ServerName] <String> [-ElasticPoolName <String>] -DatabaseName <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b1a8-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4b1a8-105">DESCRIPTION</span></span>
<span data-ttu-id="4b1a8-106">O cmdlet **Stop-AzureRmSqlDatabaseActivity** cancela a operação de atualizações assíncronas no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="4b1a8-106">The **Stop-AzureRmSqlDatabaseActivity** cmdlet cancels the asynchronous updates operation on the database.</span></span>

## <span data-ttu-id="4b1a8-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4b1a8-107">EXAMPLES</span></span>

### <span data-ttu-id="4b1a8-108">Exemplo 1: cancelar a operação de atualizações assíncronas no banco de dados</span><span class="sxs-lookup"><span data-stu-id="4b1a8-108">Example 1: Cancel the asynchronous updates operation on the database</span></span>
```
PS C:\>Stop-AzureRmSqlDatabaseActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -OperationId af97005d-9243-4f8a-844e-402d1cc855f5

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

<span data-ttu-id="4b1a8-109">Esse comando cancela a operação de atualizações assíncronas no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="4b1a8-109">This command cancels the asynchronous updates operation on the database.</span></span>

## <span data-ttu-id="4b1a8-110">OS</span><span class="sxs-lookup"><span data-stu-id="4b1a8-110">PARAMETERS</span></span>

### <span data-ttu-id="4b1a8-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4b1a8-111">-DatabaseName</span></span>
<span data-ttu-id="4b1a8-112">Especifica o nome do banco de dados para o qual esse cmdlet obtém o status.</span><span class="sxs-lookup"><span data-stu-id="4b1a8-112">Specifies the name of the database for which this cmdlet gets status.</span></span>

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

### <span data-ttu-id="4b1a8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b1a8-113">-DefaultProfile</span></span>
<span data-ttu-id="4b1a8-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4b1a8-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4b1a8-115">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="4b1a8-115">-ElasticPoolName</span></span>
<span data-ttu-id="4b1a8-116">O nome do pool elástico do SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="4b1a8-116">The name of the Azure SQL Elastic Pool.</span></span>

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

### <span data-ttu-id="4b1a8-117">-OperationId</span><span class="sxs-lookup"><span data-stu-id="4b1a8-117">-OperationId</span></span>
<span data-ttu-id="4b1a8-118">Especifica a ID da operação que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="4b1a8-118">Specifies the ID of the operation that this cmdlet gets.</span></span>

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

### <span data-ttu-id="4b1a8-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b1a8-119">-ResourceGroupName</span></span>
<span data-ttu-id="4b1a8-120">Especifica o nome do grupo de recursos ao qual o banco de dados está atribuído.</span><span class="sxs-lookup"><span data-stu-id="4b1a8-120">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="4b1a8-121">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="4b1a8-121">-ServerName</span></span>
<span data-ttu-id="4b1a8-122">Especifica o nome do Microsoft SQL Server que hospeda o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="4b1a8-122">Specifies the name of the Microsoft SQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="4b1a8-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4b1a8-123">-Confirm</span></span>
<span data-ttu-id="4b1a8-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4b1a8-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b1a8-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b1a8-125">-WhatIf</span></span>
<span data-ttu-id="4b1a8-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4b1a8-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b1a8-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4b1a8-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b1a8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b1a8-128">CommonParameters</span></span>
<span data-ttu-id="4b1a8-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b1a8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b1a8-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b1a8-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b1a8-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4b1a8-131">INPUTS</span></span>

### <span data-ttu-id="4b1a8-132">System. String</span><span class="sxs-lookup"><span data-stu-id="4b1a8-132">System.String</span></span>

### <span data-ttu-id="4b1a8-133">System. Nullable ' 1 [[System. GUID, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="4b1a8-133">System.Nullable\`1[[System.Guid, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="4b1a8-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4b1a8-134">OUTPUTS</span></span>

### <span data-ttu-id="4b1a8-135">Microsoft. Azure. Commands. Sql. Database. Model. AzureSqlDatabaseActivityModel</span><span class="sxs-lookup"><span data-stu-id="4b1a8-135">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel</span></span>

## <span data-ttu-id="4b1a8-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4b1a8-136">NOTES</span></span>

## <span data-ttu-id="4b1a8-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4b1a8-137">RELATED LINKS</span></span>
