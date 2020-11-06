---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabaseauditingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseAuditingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseAuditingPolicy.md
ms.openlocfilehash: a37bf2dd4e69352ff33a1f8c886750fec67e52f7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431885"
---
# <span data-ttu-id="141e7-101">Get-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="141e7-101">Get-AzureRmSqlDatabaseAuditingPolicy</span></span>

## <span data-ttu-id="141e7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="141e7-102">SYNOPSIS</span></span>
<span data-ttu-id="141e7-103">Obtém a política de auditoria de um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="141e7-103">Gets the auditing policy of a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="141e7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="141e7-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseAuditingPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="141e7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="141e7-105">DESCRIPTION</span></span>
<span data-ttu-id="141e7-106">O cmdlet **Get-AzureRmSqlDatabaseAuditingPolicy** Obtém a política de auditoria de um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="141e7-106">The **Get-AzureRmSqlDatabaseAuditingPolicy** cmdlet gets the auditing policy of an Azure SQL Database.</span></span>
<span data-ttu-id="141e7-107">Para usar o cmdlet, use os parâmetros *ResourceGroupName* , *ServerName* e *DatabaseName* para identificar o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="141e7-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>

## <span data-ttu-id="141e7-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="141e7-108">EXAMPLES</span></span>

### <span data-ttu-id="141e7-109">Exemplo 1: obter a política de auditoria de um banco de dados SQL do Azure com a auditoria de tabela definida</span><span class="sxs-lookup"><span data-stu-id="141e7-109">Example 1: Get the auditing policy of an Azure SQL database with Table auditing defined on it</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName           : database01
UseServerDefault       : Disabled
EventType              : {PlainSQL_Success, PlainSQL_Failure, ParameterizedSQL_Success, ParameterizedSQL_Failure...} 
TableIdentifier        : MyAuditTableName
FullAuditLogsTableName : SQLDBAuditLogsMyAuditTableName
ResourceGroupName      : resourcegroup01
ServerName             : server01
AuditType              : Table
AuditState             : Enabled
StorageAccountName     : mystorage
StorageKeyType         : Primary
RetentionInDays        : 0
```

### <span data-ttu-id="141e7-110">Exemplo 2: obter a política de auditoria de um banco de dados SQL do Azure com auditoria de blob definida</span><span class="sxs-lookup"><span data-stu-id="141e7-110">Example 2: Get the auditing policy of an Azure SQL database with Blob auditing defined on it</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName           : database01
AuditAction            : {}
AuditActionGroup       : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                          BATCH_COMPLETED_GROUP, ...} 
ResourceGroupName      : resourcegroup01
ServerName             : server01
AuditType              : Blob
AuditState             : Enabled
StorageAccountName     : mystorage
StorageKeyType         : Primary
RetentionInDays        : 0
```

## <span data-ttu-id="141e7-111">OS</span><span class="sxs-lookup"><span data-stu-id="141e7-111">PARAMETERS</span></span>

### <span data-ttu-id="141e7-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="141e7-112">-DatabaseName</span></span>
<span data-ttu-id="141e7-113">Especifica o nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="141e7-113">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="141e7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="141e7-114">-DefaultProfile</span></span>
<span data-ttu-id="141e7-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="141e7-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="141e7-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="141e7-116">-ResourceGroupName</span></span>
<span data-ttu-id="141e7-117">Especifica o nome do grupo de recursos ao qual o banco de dados está atribuído.</span><span class="sxs-lookup"><span data-stu-id="141e7-117">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="141e7-118">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="141e7-118">-ServerName</span></span>
<span data-ttu-id="141e7-119">Especifica o nome do servidor no qual o banco de dados está localizado.</span><span class="sxs-lookup"><span data-stu-id="141e7-119">Specifies the name of the server where the database is located.</span></span>

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

### <span data-ttu-id="141e7-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="141e7-120">-Confirm</span></span>
<span data-ttu-id="141e7-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="141e7-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="141e7-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="141e7-122">-WhatIf</span></span>
<span data-ttu-id="141e7-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="141e7-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="141e7-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="141e7-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="141e7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="141e7-125">CommonParameters</span></span>
<span data-ttu-id="141e7-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="141e7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="141e7-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="141e7-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="141e7-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="141e7-128">INPUTS</span></span>

### <span data-ttu-id="141e7-129">System. String</span><span class="sxs-lookup"><span data-stu-id="141e7-129">System.String</span></span>

## <span data-ttu-id="141e7-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="141e7-130">OUTPUTS</span></span>

### <span data-ttu-id="141e7-131">Microsoft. Azure. Commands. Sql. Auditing. Model. AuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="141e7-131">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditingPolicyModel</span></span>

## <span data-ttu-id="141e7-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="141e7-132">NOTES</span></span>

## <span data-ttu-id="141e7-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="141e7-133">RELATED LINKS</span></span>

[<span data-ttu-id="141e7-134">Remove-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="141e7-134">Remove-AzureRmSqlDatabaseAuditing</span></span>](./Remove-AzureRmSqlDatabaseAuditing.md)

[<span data-ttu-id="141e7-135">Set-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="141e7-135">Set-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Set-AzureRmSqlDatabaseAuditingPolicy.md)



