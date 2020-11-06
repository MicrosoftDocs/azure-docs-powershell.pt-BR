---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncAgentLinkedDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncAgentLinkedDatabase.md
ms.openlocfilehash: fe39df8c93a504b6a7c3ba9db4a3de18096dd820
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427759"
---
# <span data-ttu-id="f8584-101">Get-AzureRmSqlSyncAgentLinkedDatabase</span><span class="sxs-lookup"><span data-stu-id="f8584-101">Get-AzureRmSqlSyncAgentLinkedDatabase</span></span>

## <span data-ttu-id="f8584-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f8584-102">SYNOPSIS</span></span>
<span data-ttu-id="f8584-103">Retorna informações sobre bancos de dados do SQL Server vinculadas por um agente de sincronização.</span><span class="sxs-lookup"><span data-stu-id="f8584-103">Returns information about SQL Server databases linked by a sync agent.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f8584-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f8584-104">SYNTAX</span></span>

```
Get-AzureRmSqlSyncAgentLinkedDatabase [-ServerName] <String> [-SyncAgentName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8584-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f8584-105">DESCRIPTION</span></span>
<span data-ttu-id="f8584-106">O cmdlet **Get-AzureRmSqlSyncAgentLinkedDatabases** retorna informações sobre bancos de dados do SQL Server vinculados por um agente de sincronização.</span><span class="sxs-lookup"><span data-stu-id="f8584-106">The **Get-AzureRmSqlSyncAgentLinkedDatabases** cmdlet returns information about SQL Server databases linked by a sync agent.</span></span>

## <span data-ttu-id="f8584-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f8584-107">EXAMPLES</span></span>

### <span data-ttu-id="f8584-108">Exemplo 1: obter os bancos de dados do SQL Server vinculados para um agente de sincronização do SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="f8584-108">Example 1: Get the linked SQL Server databases for an Azure SQL sync agent.</span></span>
```
PS C:\> Get-AzureRmSqlSyncAgentLinkedDatabases -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -SyncAgentName "SyncAgent01" | Format-List
SeverName                 : sever01
DatabaseId                : databaseId
DatabaseName              : database01
DatabaseType              : SQLServerDatabase
Description               : 
UserName                  : myAccount
```

<span data-ttu-id="f8584-109">Esse comando retorna os bancos de dados vinculados do SQL Server vinculados por um agente de sincronização do SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="f8584-109">This command returns the linked SQL Server databases linked by an Azure SQL sync agent.</span></span>

## <span data-ttu-id="f8584-110">OS</span><span class="sxs-lookup"><span data-stu-id="f8584-110">PARAMETERS</span></span>

### <span data-ttu-id="f8584-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8584-111">-ResourceGroupName</span></span>
<span data-ttu-id="f8584-112">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f8584-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="f8584-113">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="f8584-113">-ServerName</span></span>
<span data-ttu-id="f8584-114">O nome do Azure SQL Server no qual o agente de sincronização se encontra.</span><span class="sxs-lookup"><span data-stu-id="f8584-114">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="f8584-115">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="f8584-115">-SyncAgentName</span></span>
<span data-ttu-id="f8584-116">O nome do agente de sincronização.</span><span class="sxs-lookup"><span data-stu-id="f8584-116">The sync agent name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8584-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8584-117">-DefaultProfile</span></span>
<span data-ttu-id="f8584-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f8584-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8584-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8584-119">CommonParameters</span></span>
<span data-ttu-id="f8584-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8584-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8584-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8584-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8584-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f8584-122">INPUTS</span></span>

## <span data-ttu-id="f8584-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f8584-123">OUTPUTS</span></span>

### <span data-ttu-id="f8584-124">Microsoft. Azure. Commands. Sql. datasync. Model. AzureSqlSyncAgentLinkedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="f8584-124">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentLinkedDatabaseModel</span></span>

## <span data-ttu-id="f8584-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f8584-125">NOTES</span></span>

## <span data-ttu-id="f8584-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f8584-126">RELATED LINKS</span></span>
