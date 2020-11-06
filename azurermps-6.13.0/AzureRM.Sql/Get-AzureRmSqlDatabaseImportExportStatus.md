---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 5D4F13F9-57E7-446B-AA28-8C44B149E1CB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabaseimportexportstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseImportExportStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseImportExportStatus.md
ms.openlocfilehash: ad5e5bb73b3611c3c56c7340f740947134f72d39
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427157"
---
# <span data-ttu-id="5be3c-101">Get-AzureRmSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="5be3c-101">Get-AzureRmSqlDatabaseImportExportStatus</span></span>

## <span data-ttu-id="5be3c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5be3c-102">SYNOPSIS</span></span>
<span data-ttu-id="5be3c-103">Obtém os detalhes de uma importação ou exportação de um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="5be3c-103">Gets the details of an import or export of an Azure SQL Database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5be3c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5be3c-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseImportExportStatus [-OperationStatusLink] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5be3c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5be3c-105">DESCRIPTION</span></span>
<span data-ttu-id="5be3c-106">O cmdlet **Get-AzureRmSqlDatabaseImportExportStatus** Obtém detalhes de um arquivo bacpac importado de uma conta de armazenamento para um banco de dados SQL do Azure ou uma exportação de um banco de dados SQL do Azure como um arquivo bacpac para uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="5be3c-106">The **Get-AzureRmSqlDatabaseImportExportStatus** cmdlet gets details of a bacpac file import from a storage account to an Azure SQL Database or an export of an Azure SQL Database as a bacpac file to a storage account.</span></span>
<span data-ttu-id="5be3c-107">Esse cmdlet também é compatível com o serviço Stretch Database do SQL Server no Azure.</span><span class="sxs-lookup"><span data-stu-id="5be3c-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="5be3c-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5be3c-108">EXAMPLES</span></span>

### <span data-ttu-id="5be3c-109">Exemplo 1: obter o status de importação e exportação de um banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="5be3c-109">Example 1: Get the import and export status of a SQL database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseImportExportStatus -OperationStatusLink "https://management.contoso.com/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/resource01/providers/Microsoft.Sql/servers/server01/databases/database01/importExportOperationResults/00000000-000-0000-0000-000000000000?api-version=2014-04-01"
OperationStatusLink : 
ErrorMessage        : 
LastModifiedTime    : 4/15/2016 10:16:14 PM
QueuedTime          : 4/15/2016 10:16:13 PM
StatusMessage       : Running, Progress = 5.00 %
Status              : InProgress
```

<span data-ttu-id="5be3c-110">Esse comando obtém o status de uma solicitação de importação ou exportação de um banco de dados na URL especificada.</span><span class="sxs-lookup"><span data-stu-id="5be3c-110">This command gets the status of an import or export request for a database at the specified URL.</span></span>

## <span data-ttu-id="5be3c-111">OS</span><span class="sxs-lookup"><span data-stu-id="5be3c-111">PARAMETERS</span></span>

### <span data-ttu-id="5be3c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5be3c-112">-DefaultProfile</span></span>
<span data-ttu-id="5be3c-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="5be3c-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5be3c-114">-OperationStatusLink</span><span class="sxs-lookup"><span data-stu-id="5be3c-114">-OperationStatusLink</span></span>
<span data-ttu-id="5be3c-115">Especifica o link de status que é retornado dos cmdlets New-AzureRmSqlDatabaseExport ou New-AzureRmSqlDatabaseImport.</span><span class="sxs-lookup"><span data-stu-id="5be3c-115">Specifies the status link that is returned from the New-AzureRmSqlDatabaseExport or New-AzureRmSqlDatabaseImport cmdlets.</span></span>

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

### <span data-ttu-id="5be3c-116">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5be3c-116">-Confirm</span></span>
<span data-ttu-id="5be3c-117">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5be3c-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5be3c-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5be3c-118">-WhatIf</span></span>
<span data-ttu-id="5be3c-119">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5be3c-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5be3c-120">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5be3c-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5be3c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5be3c-121">CommonParameters</span></span>
<span data-ttu-id="5be3c-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5be3c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5be3c-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5be3c-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5be3c-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5be3c-124">INPUTS</span></span>

### <span data-ttu-id="5be3c-125">System. String</span><span class="sxs-lookup"><span data-stu-id="5be3c-125">System.String</span></span>

## <span data-ttu-id="5be3c-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5be3c-126">OUTPUTS</span></span>

### <span data-ttu-id="5be3c-127">Microsoft. Azure. Commands. Sql. ImportExport. Model. AzureSqlDatabaseImportExportStatusModel</span><span class="sxs-lookup"><span data-stu-id="5be3c-127">Microsoft.Azure.Commands.Sql.ImportExport.Model.AzureSqlDatabaseImportExportStatusModel</span></span>

## <span data-ttu-id="5be3c-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5be3c-128">NOTES</span></span>
* <span data-ttu-id="5be3c-129">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, SQL, Database, MSSQL</span><span class="sxs-lookup"><span data-stu-id="5be3c-129">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="5be3c-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5be3c-130">RELATED LINKS</span></span>

[<span data-ttu-id="5be3c-131">New-AzureRmSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="5be3c-131">New-AzureRmSqlDatabaseExport</span></span>](./New-AzureRmSqlDatabaseExport.md)

[<span data-ttu-id="5be3c-132">New-AzureRmSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="5be3c-132">New-AzureRmSqlDatabaseImport</span></span>](./New-AzureRmSqlDatabaseImport.md)

[<span data-ttu-id="5be3c-133">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="5be3c-133">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)