---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 40674DC7-E35F-4C9F-8CE0-D1C6F524C9FB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerAuditingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerAuditingPolicy.md
ms.openlocfilehash: 34eedd81d5e8625ed957cba16d3cec1ea33a0c32
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430607"
---
# <span data-ttu-id="4f41b-101">Get-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="4f41b-101">Get-AzureRmSqlServerAuditingPolicy</span></span>

## <span data-ttu-id="4f41b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4f41b-102">SYNOPSIS</span></span>
<span data-ttu-id="4f41b-103">Obtém a política de auditoria de um SQL Server.</span><span class="sxs-lookup"><span data-stu-id="4f41b-103">Gets the auditing policy of a SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4f41b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4f41b-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerAuditingPolicy -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f41b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4f41b-105">DESCRIPTION</span></span>
<span data-ttu-id="4f41b-106">O cmdlet **Get-AzureRmSqlServerAuditingPolicy** Obtém a política de auditoria de um SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="4f41b-106">The **Get-AzureRmSqlServerAuditingPolicy** cmdlet gets the auditing policy of an Azure SQL server.</span></span>
<span data-ttu-id="4f41b-107">Especifique os parâmetros *ResourceGroupName* , *nome_do_servidor* e *DatabaseName* para identificar o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="4f41b-107">Specify the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="4f41b-108">Esse cmdlet retorna uma política que é usada pelos bancos de dados SQL do Azure que são definidos no SQL Server do Azure especificado e usam sua política de auditoria.</span><span class="sxs-lookup"><span data-stu-id="4f41b-108">This cmdlet returns a policy that is used by the Azure SQL databases that are both defined in the specified Azure SQL server and use its auditing policy.</span></span>

## <span data-ttu-id="4f41b-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4f41b-109">EXAMPLES</span></span>

### <span data-ttu-id="4f41b-110">Exemplo 1: obter a política de auditoria de um SQL Server do Azure com auditoria de tabela definida</span><span class="sxs-lookup"><span data-stu-id="4f41b-110">Example 1: Get the auditing policy of an Azure SQL server with Table auditing defined on it</span></span>
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

### <span data-ttu-id="4f41b-111">Exemplo 2: obter a política de auditoria de um SQL Server do Azure com auditoria de blob definida</span><span class="sxs-lookup"><span data-stu-id="4f41b-111">Example 2: Get the auditing policy of an Azure SQL server with Blob auditing defined on it</span></span>
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

## <span data-ttu-id="4f41b-112">OS</span><span class="sxs-lookup"><span data-stu-id="4f41b-112">PARAMETERS</span></span>

### <span data-ttu-id="4f41b-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f41b-113">-ResourceGroupName</span></span>
<span data-ttu-id="4f41b-114">Especifica o nome do grupo de recursos ao qual o SQL Server do Azure está atribuído.</span><span class="sxs-lookup"><span data-stu-id="4f41b-114">Specifies the name of the resource group to which the Azure SQL server is assigned.</span></span>

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

### <span data-ttu-id="4f41b-115">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="4f41b-115">-ServerName</span></span>
<span data-ttu-id="4f41b-116">Especifica o nome do Azure SQL Server para o qual esse cmdlet obtém a política de auditoria.</span><span class="sxs-lookup"><span data-stu-id="4f41b-116">Specifies the name of the Azure SQL server for which this cmdlet gets the auditing policy.</span></span>

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

### <span data-ttu-id="4f41b-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4f41b-117">-Confirm</span></span>
<span data-ttu-id="4f41b-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4f41b-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f41b-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f41b-119">-WhatIf</span></span>
<span data-ttu-id="4f41b-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4f41b-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f41b-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4f41b-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f41b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f41b-122">-DefaultProfile</span></span>
<span data-ttu-id="4f41b-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4f41b-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4f41b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f41b-124">CommonParameters</span></span>
<span data-ttu-id="4f41b-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f41b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f41b-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f41b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f41b-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4f41b-127">INPUTS</span></span>

## <span data-ttu-id="4f41b-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4f41b-128">OUTPUTS</span></span>

### <span data-ttu-id="4f41b-129">Microsoft. Azure. Commands. Sql. Security. Model. ServerAuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="4f41b-129">Microsoft.Azure.Commands.Sql.Security.Model.ServerAuditingPolicyModel</span></span>

## <span data-ttu-id="4f41b-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4f41b-130">NOTES</span></span>

## <span data-ttu-id="4f41b-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4f41b-131">RELATED LINKS</span></span>

[<span data-ttu-id="4f41b-132">Set-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="4f41b-132">Set-AzureRmSqlServerAuditingPolicy</span></span>](./Set-AzureRmSqlServerAuditingPolicy.md)

[<span data-ttu-id="4f41b-133">Use-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="4f41b-133">Use-AzureRmSqlServerAuditingPolicy</span></span>](./Use-AzureRmSqlServerAuditingPolicy.md)

[<span data-ttu-id="4f41b-134">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="4f41b-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


