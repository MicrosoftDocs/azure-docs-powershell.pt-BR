---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 40674DC7-E35F-4C9F-8CE0-D1C6F524C9FB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverauditingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerAuditingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerAuditingPolicy.md
ms.openlocfilehash: 1b4f72a5d57884975d6beb0d4676a0cbe5863681
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431877"
---
# <span data-ttu-id="4c26d-101">Get-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="4c26d-101">Get-AzureRmSqlServerAuditingPolicy</span></span>

## <span data-ttu-id="4c26d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4c26d-102">SYNOPSIS</span></span>
<span data-ttu-id="4c26d-103">Obtém a política de auditoria de um SQL Server.</span><span class="sxs-lookup"><span data-stu-id="4c26d-103">Gets the auditing policy of a SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4c26d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4c26d-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerAuditingPolicy -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c26d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4c26d-105">DESCRIPTION</span></span>
<span data-ttu-id="4c26d-106">O cmdlet **Get-AzureRmSqlServerAuditingPolicy** Obtém a política de auditoria de um SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="4c26d-106">The **Get-AzureRmSqlServerAuditingPolicy** cmdlet gets the auditing policy of an Azure SQL server.</span></span>
<span data-ttu-id="4c26d-107">Especifique os parâmetros *ResourceGroupName* , *nome_do_servidor* e *DatabaseName* para identificar o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="4c26d-107">Specify the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="4c26d-108">Esse cmdlet retorna uma política que é usada pelos bancos de dados SQL do Azure que são definidos no SQL Server do Azure especificado e usam sua política de auditoria.</span><span class="sxs-lookup"><span data-stu-id="4c26d-108">This cmdlet returns a policy that is used by the Azure SQL databases that are both defined in the specified Azure SQL server and use its auditing policy.</span></span>

## <span data-ttu-id="4c26d-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4c26d-109">EXAMPLES</span></span>

### <span data-ttu-id="4c26d-110">Exemplo 1: obter a política de auditoria de um SQL Server do Azure com auditoria de tabela definida</span><span class="sxs-lookup"><span data-stu-id="4c26d-110">Example 1: Get the auditing policy of an Azure SQL server with Table auditing defined on it</span></span>
```
PS C:\>Get-AzureRmSqlServerAuditingPolicy -ResourceGroupName "resourcegroup01" -ServerName "server01"
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

### <span data-ttu-id="4c26d-111">Exemplo 2: obter a política de auditoria de um SQL Server do Azure com auditoria de blob definida</span><span class="sxs-lookup"><span data-stu-id="4c26d-111">Example 2: Get the auditing policy of an Azure SQL server with Blob auditing defined on it</span></span>
```
PS C:\>Get-AzureRmSqlServerAuditingPolicy -ResourceGroupName "resourcegroup01" -ServerName "server01"
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

## <span data-ttu-id="4c26d-112">OS</span><span class="sxs-lookup"><span data-stu-id="4c26d-112">PARAMETERS</span></span>

### <span data-ttu-id="4c26d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c26d-113">-DefaultProfile</span></span>
<span data-ttu-id="4c26d-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="4c26d-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4c26d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c26d-115">-ResourceGroupName</span></span>
<span data-ttu-id="4c26d-116">Especifica o nome do grupo de recursos ao qual o SQL Server do Azure está atribuído.</span><span class="sxs-lookup"><span data-stu-id="4c26d-116">Specifies the name of the resource group to which the Azure SQL server is assigned.</span></span>

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

### <span data-ttu-id="4c26d-117">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="4c26d-117">-ServerName</span></span>
<span data-ttu-id="4c26d-118">Especifica o nome do Azure SQL Server para o qual esse cmdlet obtém a política de auditoria.</span><span class="sxs-lookup"><span data-stu-id="4c26d-118">Specifies the name of the Azure SQL server for which this cmdlet gets the auditing policy.</span></span>

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

### <span data-ttu-id="4c26d-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4c26d-119">-Confirm</span></span>
<span data-ttu-id="4c26d-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c26d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c26d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c26d-121">-WhatIf</span></span>
<span data-ttu-id="4c26d-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4c26d-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c26d-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4c26d-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c26d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c26d-124">CommonParameters</span></span>
<span data-ttu-id="4c26d-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c26d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c26d-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c26d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c26d-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4c26d-127">INPUTS</span></span>

### <span data-ttu-id="4c26d-128">System. String</span><span class="sxs-lookup"><span data-stu-id="4c26d-128">System.String</span></span>

## <span data-ttu-id="4c26d-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4c26d-129">OUTPUTS</span></span>

### <span data-ttu-id="4c26d-130">Microsoft. Azure. Commands. Sql. Auditing. Model. AuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="4c26d-130">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditingPolicyModel</span></span>

## <span data-ttu-id="4c26d-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4c26d-131">NOTES</span></span>

## <span data-ttu-id="4c26d-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4c26d-132">RELATED LINKS</span></span>

[<span data-ttu-id="4c26d-133">Set-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="4c26d-133">Set-AzureRmSqlServerAuditingPolicy</span></span>](./Set-AzureRmSqlServerAuditingPolicy.md)

[<span data-ttu-id="4c26d-134">Use-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="4c26d-134">Use-AzureRmSqlServerAuditingPolicy</span></span>](./Use-AzureRmSqlServerAuditingPolicy.md)

[<span data-ttu-id="4c26d-135">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="4c26d-135">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


