---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerAuditing.md
ms.openlocfilehash: 18117a109448ec219364ee6563191683a1fbc8a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429956"
---
# <span data-ttu-id="92345-101">Get-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="92345-101">Get-AzureRmSqlServerAuditing</span></span>

## <span data-ttu-id="92345-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="92345-102">SYNOPSIS</span></span>
<span data-ttu-id="92345-103">Obtém as configurações de auditoria de um SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="92345-103">Gets the auditing settings of an Azure SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="92345-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="92345-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerAuditing [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92345-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="92345-105">DESCRIPTION</span></span>
<span data-ttu-id="92345-106">O cmdlet **Get-AzureRmSqlServerAuditing** Obtém a política de auditoria de blob de um SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="92345-106">The **Get-AzureRmSqlServerAuditing** cmdlet gets the blob auditing policy of an Azure SQL server.</span></span>
<span data-ttu-id="92345-107">Especifique os parâmetros *ResourceGroupName* e *nomedoservidor* para identificar o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="92345-107">Specify the *ResourceGroupName* and *ServerName* parameters to identify the database.</span></span>
<span data-ttu-id="92345-108">Esse cmdlet retorna uma política que é usada pelos bancos de dados SQL do Azure definidos no SQL Server do Azure especificado.</span><span class="sxs-lookup"><span data-stu-id="92345-108">This cmdlet returns a policy that is used by the Azure SQL databases that are defined in the specified Azure SQL server.</span></span>

## <span data-ttu-id="92345-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="92345-109">EXAMPLES</span></span>

### <span data-ttu-id="92345-110">Exemplo 1: obter as configurações de auditoria de um SQL Server do Azure</span><span class="sxs-lookup"><span data-stu-id="92345-110">Example 1: Get the auditing settings of an Azure SQL server</span></span>
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

## <span data-ttu-id="92345-111">OS</span><span class="sxs-lookup"><span data-stu-id="92345-111">PARAMETERS</span></span>

### <span data-ttu-id="92345-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92345-112">-ResourceGroupName</span></span>
<span data-ttu-id="92345-113">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="92345-113">The name of the resource group.</span></span>

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

### <span data-ttu-id="92345-114">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="92345-114">-ServerName</span></span>
<span data-ttu-id="92345-115">Nome do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="92345-115">SQL server name.</span></span>

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

### <span data-ttu-id="92345-116">-Confirme</span><span class="sxs-lookup"><span data-stu-id="92345-116">-Confirm</span></span>
<span data-ttu-id="92345-117">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92345-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92345-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92345-118">-WhatIf</span></span>
<span data-ttu-id="92345-119">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="92345-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="92345-120">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="92345-120">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92345-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92345-121">-DefaultProfile</span></span>
<span data-ttu-id="92345-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="92345-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92345-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92345-123">CommonParameters</span></span>
<span data-ttu-id="92345-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92345-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92345-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92345-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92345-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="92345-126">INPUTS</span></span>

## <span data-ttu-id="92345-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="92345-127">OUTPUTS</span></span>

### <span data-ttu-id="92345-128">Microsoft. Azure. Commands. Sql. Security. Model. ServerBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="92345-128">Microsoft.Azure.Commands.Sql.Security.Model.ServerBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="92345-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="92345-129">NOTES</span></span>

## <span data-ttu-id="92345-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="92345-130">RELATED LINKS</span></span>

