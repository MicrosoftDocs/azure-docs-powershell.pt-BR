---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabaseauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseAuditing.md
ms.openlocfilehash: b78bcf228012edd022f9551a5834c61cebc8d278
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431890"
---
# <span data-ttu-id="45db7-101">Get-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="45db7-101">Get-AzureRmSqlDatabaseAuditing</span></span>

## <span data-ttu-id="45db7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="45db7-102">SYNOPSIS</span></span>
<span data-ttu-id="45db7-103">Obtém as configurações de auditoria de um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="45db7-103">Gets the auditing settings of an Azure SQL database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="45db7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="45db7-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseAuditing [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45db7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="45db7-105">DESCRIPTION</span></span>
<span data-ttu-id="45db7-106">O cmdlet **Get-AzureRmSqlDatabaseAuditing** Obtém as configurações de auditoria de um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="45db7-106">The **Get-AzureRmSqlDatabaseAuditing** cmdlet gets the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="45db7-107">Para usar o cmdlet, use os parâmetros *ResourceGroupName* , *ServerName* e *DatabaseName* para identificar o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="45db7-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>

## <span data-ttu-id="45db7-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="45db7-108">EXAMPLES</span></span>

### <span data-ttu-id="45db7-109">Exemplo 1: obter as configurações de auditoria de um banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="45db7-109">Example 1: Get the auditing settings of an Azure SQL database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName                 : database01
AuditAction                  : {}
AuditActionGroup             : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                BATCH_COMPLETED_GROUP, ...}
ResourceGroupName            : resourcegroup01
ServerName                   : server01
AuditState                   : Enabled
StorageAccountName           : mystorage
StorageKeyType               : Primary
RetentionInDays              : 0
StorageAccountSubscriptionId : 7fe3301d-31d3-4668-af5e-211a890ba6e3
PredicateExpression          : statement <> 'select 1'
```

## <span data-ttu-id="45db7-110">OS</span><span class="sxs-lookup"><span data-stu-id="45db7-110">PARAMETERS</span></span>

### <span data-ttu-id="45db7-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="45db7-111">-DatabaseName</span></span>
<span data-ttu-id="45db7-112">Nome do banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="45db7-112">SQL Database name.</span></span>

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

### <span data-ttu-id="45db7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45db7-113">-DefaultProfile</span></span>
<span data-ttu-id="45db7-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="45db7-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="45db7-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45db7-115">-ResourceGroupName</span></span>
<span data-ttu-id="45db7-116">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="45db7-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="45db7-117">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="45db7-117">-ServerName</span></span>
<span data-ttu-id="45db7-118">Nome do servidor do banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="45db7-118">SQL Database server name.</span></span>

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

### <span data-ttu-id="45db7-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="45db7-119">-Confirm</span></span>
<span data-ttu-id="45db7-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45db7-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45db7-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45db7-121">-WhatIf</span></span>
<span data-ttu-id="45db7-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="45db7-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="45db7-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="45db7-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45db7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45db7-124">CommonParameters</span></span>
<span data-ttu-id="45db7-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45db7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45db7-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45db7-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45db7-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="45db7-127">INPUTS</span></span>

## <span data-ttu-id="45db7-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="45db7-128">OUTPUTS</span></span>

### <span data-ttu-id="45db7-129">Microsoft. Azure. Commands. Sql. Auditing. Model. DatabaseBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="45db7-129">Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="45db7-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="45db7-130">NOTES</span></span>

## <span data-ttu-id="45db7-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="45db7-131">RELATED LINKS</span></span>
