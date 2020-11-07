---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlsyncagentlinkeddatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncAgentLinkedDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncAgentLinkedDatabase.md
ms.openlocfilehash: 6ef3a84e84e001943cef1791c77f6c2a354da8ff
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773857"
---
# <span data-ttu-id="b050e-101">Get-AzSqlSyncAgentLinkedDatabase</span><span class="sxs-lookup"><span data-stu-id="b050e-101">Get-AzSqlSyncAgentLinkedDatabase</span></span>

## <span data-ttu-id="b050e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b050e-102">SYNOPSIS</span></span>
<span data-ttu-id="b050e-103">Retorna informações sobre bancos de dados do SQL Server vinculadas por um agente de sincronização.</span><span class="sxs-lookup"><span data-stu-id="b050e-103">Returns information about SQL Server databases linked by a sync agent.</span></span>

## <span data-ttu-id="b050e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b050e-104">SYNTAX</span></span>

```
Get-AzSqlSyncAgentLinkedDatabase [-ServerName] <String> [-SyncAgentName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b050e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b050e-105">DESCRIPTION</span></span>
<span data-ttu-id="b050e-106">O cmdlet **Get-AzSqlSyncAgentLinkedDatabases** retorna informações sobre bancos de dados do SQL Server vinculados por um agente de sincronização.</span><span class="sxs-lookup"><span data-stu-id="b050e-106">The **Get-AzSqlSyncAgentLinkedDatabases** cmdlet returns information about SQL Server databases linked by a sync agent.</span></span>

## <span data-ttu-id="b050e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b050e-107">EXAMPLES</span></span>

### <span data-ttu-id="b050e-108">Exemplo 1: obter os bancos de dados do SQL Server vinculados para um agente de sincronização do SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="b050e-108">Example 1: Get the linked SQL Server databases for an Azure SQL sync agent.</span></span>
```
PS C:\> Get-AzSqlSyncAgentLinkedDatabases -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -SyncAgentName "SyncAgent01" | Format-List
SeverName                 : sever01
DatabaseId                : databaseId
DatabaseName              : database01
DatabaseType              : SQLServerDatabase
Description               : 
UserName                  : myAccount
```

<span data-ttu-id="b050e-109">Esse comando retorna os bancos de dados vinculados do SQL Server vinculados por um agente de sincronização do SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="b050e-109">This command returns the linked SQL Server databases linked by an Azure SQL sync agent.</span></span>

## <span data-ttu-id="b050e-110">OS</span><span class="sxs-lookup"><span data-stu-id="b050e-110">PARAMETERS</span></span>

### <span data-ttu-id="b050e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b050e-111">-DefaultProfile</span></span>
<span data-ttu-id="b050e-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="b050e-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b050e-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b050e-113">-ResourceGroupName</span></span>
<span data-ttu-id="b050e-114">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b050e-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="b050e-115">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="b050e-115">-ServerName</span></span>
<span data-ttu-id="b050e-116">O nome do Azure SQL Server no qual o agente de sincronização se encontra.</span><span class="sxs-lookup"><span data-stu-id="b050e-116">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="b050e-117">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="b050e-117">-SyncAgentName</span></span>
<span data-ttu-id="b050e-118">O nome do agente de sincronização.</span><span class="sxs-lookup"><span data-stu-id="b050e-118">The sync agent name.</span></span>

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

### <span data-ttu-id="b050e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b050e-119">CommonParameters</span></span>
<span data-ttu-id="b050e-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b050e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b050e-121">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b050e-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b050e-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b050e-122">INPUTS</span></span>

### <span data-ttu-id="b050e-123">System. String</span><span class="sxs-lookup"><span data-stu-id="b050e-123">System.String</span></span>

## <span data-ttu-id="b050e-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b050e-124">OUTPUTS</span></span>

### <span data-ttu-id="b050e-125">Microsoft. Azure. Commands. Sql. datasync. Model. AzureSqlSyncAgentLinkedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="b050e-125">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentLinkedDatabaseModel</span></span>

## <span data-ttu-id="b050e-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b050e-126">NOTES</span></span>

## <span data-ttu-id="b050e-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b050e-127">RELATED LINKS</span></span>