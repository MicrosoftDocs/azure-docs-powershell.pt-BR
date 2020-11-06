---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Update-AzureRmSqlSyncSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Update-AzureRmSqlSyncSchema.md
ms.openlocfilehash: 34aec11e5f4bd2ee0aef37a4287544081bb9a87a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432166"
---
# <span data-ttu-id="66136-101">Update-AzureRmSqlSyncSchema</span><span class="sxs-lookup"><span data-stu-id="66136-101">Update-AzureRmSqlSyncSchema</span></span>

## <span data-ttu-id="66136-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="66136-102">SYNOPSIS</span></span>
<span data-ttu-id="66136-103">Atualize o esquema de sincronização para um banco de dados de membro de sincronização ou um banco de dados Hub de sincronização.</span><span class="sxs-lookup"><span data-stu-id="66136-103">Update the sync schema for a sync member database or a sync hub database.</span></span>
<span data-ttu-id="66136-104">Ele receberá o esquema de banco de dados mais recente do banco de dados real e o usará atualizará o esquema armazenado em cache pelo banco de dados de metadados de sincronização.</span><span class="sxs-lookup"><span data-stu-id="66136-104">It will get the latest database schema from the real database and then use it refresh the schema cached by Sync metadata database.</span></span>
<span data-ttu-id="66136-105">Se "SyncMemberName" for especificado, o esquema de banco de dados membro será atualizado. caso contrário, o esquema de banco de dados Hub será atualizado.</span><span class="sxs-lookup"><span data-stu-id="66136-105">If "SyncMemberName" is specified, it will refresh the member database schema; if not, it will refresh the hub database schema.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66136-106">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="66136-106">SYNTAX</span></span>

```
Update-AzureRmSqlSyncSchema [-SyncGroupName] <String> [-SyncMemberName <String>] [-PassThru]
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66136-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="66136-107">DESCRIPTION</span></span>
<span data-ttu-id="66136-108">O cmdlet **Update-AzureRmSqlSyncSchema** atualiza o esquema de sincronização para um banco de dados de membro de sincronização ou um banco de dados Hub de sincronização.</span><span class="sxs-lookup"><span data-stu-id="66136-108">The **Update-AzureRmSqlSyncSchema** cmdlet updates the sync schema for a sync member database or a sync hub database.</span></span>

## <span data-ttu-id="66136-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="66136-109">EXAMPLES</span></span>

### <span data-ttu-id="66136-110">Exemplo 1: atualizar o esquema de sincronização de um banco de dados Hub</span><span class="sxs-lookup"><span data-stu-id="66136-110">Example 1: Update the sync schema for a hub database</span></span>
```
PS C:\>Update-AzureRmSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01"
```

<span data-ttu-id="66136-111">Esse comando atualiza o esquema de sincronização para o banco de dados de Hub no grupo de sincronização syncGroup01</span><span class="sxs-lookup"><span data-stu-id="66136-111">This command updates the sync schema for the hub database in the sync group syncGroup01</span></span>

### <span data-ttu-id="66136-112">Exemplo 2: atualizar o esquema de sincronização para um banco de dados membro</span><span class="sxs-lookup"><span data-stu-id="66136-112">Example 2: Update the sync schema for a member database</span></span>
```
PS C:\>Update-AzureRmSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01" -SyncMemberName "syncMember01"
```

<span data-ttu-id="66136-113">Esse comando atualiza o esquema de sincronização para o banco de dados membro no membro de sincronização syncMember01</span><span class="sxs-lookup"><span data-stu-id="66136-113">This command updates the sync schema for the member database in the sync member syncMember01</span></span>

## <span data-ttu-id="66136-114">OS</span><span class="sxs-lookup"><span data-stu-id="66136-114">PARAMETERS</span></span>

### <span data-ttu-id="66136-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="66136-115">-Confirm</span></span>
<span data-ttu-id="66136-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="66136-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66136-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="66136-117">-DatabaseName</span></span>
<span data-ttu-id="66136-118">O nome do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="66136-118">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="66136-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="66136-119">-PassThru</span></span>
<span data-ttu-id="66136-120">Define se retorna o grupo de sincronização em que este cmdlet funciona</span><span class="sxs-lookup"><span data-stu-id="66136-120">Defines Whether return the sync group this cmdlet works on</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66136-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66136-121">-ResourceGroupName</span></span>
<span data-ttu-id="66136-122">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="66136-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="66136-123">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="66136-123">-ServerName</span></span>
<span data-ttu-id="66136-124">O nome do Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="66136-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="66136-125">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="66136-125">-SyncGroupName</span></span>
<span data-ttu-id="66136-126">O nome do grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="66136-126">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66136-127">-SyncMemberName</span><span class="sxs-lookup"><span data-stu-id="66136-127">-SyncMemberName</span></span>
<span data-ttu-id="66136-128">O nome do membro de sincronização.</span><span class="sxs-lookup"><span data-stu-id="66136-128">The sync member name.</span></span>

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

### <span data-ttu-id="66136-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66136-129">-WhatIf</span></span>
<span data-ttu-id="66136-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="66136-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66136-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="66136-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66136-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66136-132">-DefaultProfile</span></span>
<span data-ttu-id="66136-133">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="66136-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66136-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66136-134">CommonParameters</span></span>
<span data-ttu-id="66136-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66136-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66136-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66136-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66136-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="66136-137">INPUTS</span></span>

## <span data-ttu-id="66136-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="66136-138">OUTPUTS</span></span>

### <span data-ttu-id="66136-139">Microsoft. Azure. Commands. Sql. datasync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="66136-139">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="66136-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="66136-140">NOTES</span></span>

## <span data-ttu-id="66136-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="66136-141">RELATED LINKS</span></span>

