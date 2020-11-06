---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerAuditing.md
ms.openlocfilehash: 636b3602c6dafc2c00e02e19aa35d0e91c278137
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428745"
---
# <span data-ttu-id="90d62-101">Get-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="90d62-101">Get-AzureRmSqlServerAuditing</span></span>

## <span data-ttu-id="90d62-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="90d62-102">SYNOPSIS</span></span>
<span data-ttu-id="90d62-103">Obtém as configurações de auditoria de um SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="90d62-103">Gets the auditing settings of an Azure SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="90d62-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="90d62-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerAuditing [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90d62-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="90d62-105">DESCRIPTION</span></span>
<span data-ttu-id="90d62-106">O cmdlet **Get-AzureRmSqlServerAuditing** Obtém a política de auditoria de blob de um SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="90d62-106">The **Get-AzureRmSqlServerAuditing** cmdlet gets the blob auditing policy of an Azure SQL server.</span></span>
<span data-ttu-id="90d62-107">Especifique os parâmetros *ResourceGroupName* e *nomedoservidor* para identificar o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="90d62-107">Specify the *ResourceGroupName* and *ServerName* parameters to identify the database.</span></span>
<span data-ttu-id="90d62-108">Esse cmdlet retorna uma política que é usada pelos bancos de dados SQL do Azure definidos no SQL Server do Azure especificado.</span><span class="sxs-lookup"><span data-stu-id="90d62-108">This cmdlet returns a policy that is used by the Azure SQL databases that are defined in the specified Azure SQL server.</span></span>

## <span data-ttu-id="90d62-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="90d62-109">EXAMPLES</span></span>

### <span data-ttu-id="90d62-110">Exemplo 1: obter as configurações de auditoria de um SQL Server do Azure</span><span class="sxs-lookup"><span data-stu-id="90d62-110">Example 1: Get the auditing settings of an Azure SQL server</span></span>
```
PS C:\>Get-AzureRmSqlServerAuditing -ResourceGroupName "resourcegroup01" -ServerName "server01"
AuditActionGroup       : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                          BATCH_COMPLETED_GROUP, ...}
ResourceGroupName      : resourcegroup01
ServerName             : server01
AuditState             : Enabled
StorageAccountName     : mystorage
StorageKeyType         : Primary
RetentionInDays        : 0
```

## <span data-ttu-id="90d62-111">OS</span><span class="sxs-lookup"><span data-stu-id="90d62-111">PARAMETERS</span></span>

### <span data-ttu-id="90d62-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90d62-112">-DefaultProfile</span></span>
<span data-ttu-id="90d62-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="90d62-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90d62-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90d62-114">-ResourceGroupName</span></span>
<span data-ttu-id="90d62-115">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="90d62-115">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90d62-116">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="90d62-116">-ServerName</span></span>
<span data-ttu-id="90d62-117">Nome do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="90d62-117">SQL server name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90d62-118">-Confirme</span><span class="sxs-lookup"><span data-stu-id="90d62-118">-Confirm</span></span>
<span data-ttu-id="90d62-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="90d62-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90d62-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90d62-120">-WhatIf</span></span>
<span data-ttu-id="90d62-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="90d62-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="90d62-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="90d62-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90d62-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90d62-123">CommonParameters</span></span>
<span data-ttu-id="90d62-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90d62-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90d62-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90d62-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90d62-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="90d62-126">INPUTS</span></span>

### <span data-ttu-id="90d62-127">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="90d62-127">None</span></span>
<span data-ttu-id="90d62-128">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="90d62-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="90d62-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="90d62-129">OUTPUTS</span></span>

### <span data-ttu-id="90d62-130">Microsoft. Azure. Commands. Sql. Security. Model. ServerBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="90d62-130">Microsoft.Azure.Commands.Sql.Security.Model.ServerBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="90d62-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="90d62-131">NOTES</span></span>

## <span data-ttu-id="90d62-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="90d62-132">RELATED LINKS</span></span>
