---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/update-azurermsqlsyncschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Update-AzureRmSqlSyncSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Update-AzureRmSqlSyncSchema.md
ms.openlocfilehash: a78e22c66e5099ec3987fb98d1b354906c11a8d4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609882"
---
# <span data-ttu-id="49ffc-101">Update-AzureRmSqlSyncSchema</span><span class="sxs-lookup"><span data-stu-id="49ffc-101">Update-AzureRmSqlSyncSchema</span></span>

## <span data-ttu-id="49ffc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="49ffc-102">SYNOPSIS</span></span>
<span data-ttu-id="49ffc-103">Atualize o esquema de sincronização para um banco de dados de membro de sincronização ou um banco de dados Hub de sincronização.</span><span class="sxs-lookup"><span data-stu-id="49ffc-103">Update the sync schema for a sync member database or a sync hub database.</span></span>
<span data-ttu-id="49ffc-104">Ele receberá o esquema de banco de dados mais recente do banco de dados real e o usará atualizará o esquema armazenado em cache pelo banco de dados de metadados de sincronização.</span><span class="sxs-lookup"><span data-stu-id="49ffc-104">It will get the latest database schema from the real database and then use it refresh the schema cached by Sync metadata database.</span></span>
<span data-ttu-id="49ffc-105">Se "SyncMemberName" for especificado, o esquema de banco de dados membro será atualizado. caso contrário, o esquema de banco de dados Hub será atualizado.</span><span class="sxs-lookup"><span data-stu-id="49ffc-105">If "SyncMemberName" is specified, it will refresh the member database schema; if not, it will refresh the hub database schema.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="49ffc-106">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="49ffc-106">SYNTAX</span></span>

```
Update-AzureRmSqlSyncSchema [-SyncGroupName] <String> [-SyncMemberName <String>] [-PassThru]
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49ffc-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="49ffc-107">DESCRIPTION</span></span>
<span data-ttu-id="49ffc-108">O cmdlet **Update-AzureRmSqlSyncSchema** atualiza o esquema de sincronização para um banco de dados de membro de sincronização ou um banco de dados Hub de sincronização.</span><span class="sxs-lookup"><span data-stu-id="49ffc-108">The **Update-AzureRmSqlSyncSchema** cmdlet updates the sync schema for a sync member database or a sync hub database.</span></span>

## <span data-ttu-id="49ffc-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="49ffc-109">EXAMPLES</span></span>

### <span data-ttu-id="49ffc-110">Exemplo 1: atualizar o esquema de sincronização de um banco de dados Hub</span><span class="sxs-lookup"><span data-stu-id="49ffc-110">Example 1: Update the sync schema for a hub database</span></span>
```
PS C:\>Update-AzureRmSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01"
```

<span data-ttu-id="49ffc-111">Esse comando atualiza o esquema de sincronização para o banco de dados de Hub no grupo de sincronização syncGroup01</span><span class="sxs-lookup"><span data-stu-id="49ffc-111">This command updates the sync schema for the hub database in the sync group syncGroup01</span></span>

### <span data-ttu-id="49ffc-112">Exemplo 2: atualizar o esquema de sincronização para um banco de dados membro</span><span class="sxs-lookup"><span data-stu-id="49ffc-112">Example 2: Update the sync schema for a member database</span></span>
```
PS C:\>Update-AzureRmSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01" -SyncMemberName "syncMember01"
```

<span data-ttu-id="49ffc-113">Esse comando atualiza o esquema de sincronização para o banco de dados membro no membro de sincronização syncMember01</span><span class="sxs-lookup"><span data-stu-id="49ffc-113">This command updates the sync schema for the member database in the sync member syncMember01</span></span>

## <span data-ttu-id="49ffc-114">OS</span><span class="sxs-lookup"><span data-stu-id="49ffc-114">PARAMETERS</span></span>

### <span data-ttu-id="49ffc-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="49ffc-115">-DatabaseName</span></span>
<span data-ttu-id="49ffc-116">O nome do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="49ffc-116">The name of the Azure SQL Database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49ffc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49ffc-117">-DefaultProfile</span></span>
<span data-ttu-id="49ffc-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="49ffc-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="49ffc-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="49ffc-119">-PassThru</span></span>
<span data-ttu-id="49ffc-120">Define se retorna o grupo de sincronização em que este cmdlet funciona</span><span class="sxs-lookup"><span data-stu-id="49ffc-120">Defines Whether return the sync group this cmdlet works on</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49ffc-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49ffc-121">-ResourceGroupName</span></span>
<span data-ttu-id="49ffc-122">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="49ffc-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="49ffc-123">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="49ffc-123">-ServerName</span></span>
<span data-ttu-id="49ffc-124">O nome do Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="49ffc-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="49ffc-125">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="49ffc-125">-SyncGroupName</span></span>
<span data-ttu-id="49ffc-126">O nome do grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="49ffc-126">The sync group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49ffc-127">-SyncMemberName</span><span class="sxs-lookup"><span data-stu-id="49ffc-127">-SyncMemberName</span></span>
<span data-ttu-id="49ffc-128">O nome do membro de sincronização.</span><span class="sxs-lookup"><span data-stu-id="49ffc-128">The sync member name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49ffc-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="49ffc-129">-Confirm</span></span>
<span data-ttu-id="49ffc-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49ffc-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49ffc-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49ffc-131">-WhatIf</span></span>
<span data-ttu-id="49ffc-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="49ffc-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49ffc-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="49ffc-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49ffc-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49ffc-134">CommonParameters</span></span>
<span data-ttu-id="49ffc-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49ffc-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49ffc-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49ffc-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49ffc-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="49ffc-137">INPUTS</span></span>

### <span data-ttu-id="49ffc-138">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="49ffc-138">None</span></span>
<span data-ttu-id="49ffc-139">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="49ffc-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="49ffc-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="49ffc-140">OUTPUTS</span></span>

### <span data-ttu-id="49ffc-141">Microsoft. Azure. Commands. Sql. datasync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="49ffc-141">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="49ffc-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="49ffc-142">NOTES</span></span>

## <span data-ttu-id="49ffc-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="49ffc-143">RELATED LINKS</span></span>
