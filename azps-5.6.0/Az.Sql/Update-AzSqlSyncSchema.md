---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/update-azsqlsyncschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncSchema.md
ms.openlocfilehash: 394ae4d82437795f62e19b4d0f7a536cdd893da9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890557"
---
# <span data-ttu-id="05952-101">Update-AzSqlSyncSchema</span><span class="sxs-lookup"><span data-stu-id="05952-101">Update-AzSqlSyncSchema</span></span>

## <span data-ttu-id="05952-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05952-102">SYNOPSIS</span></span>
<span data-ttu-id="05952-103">Atualize o esquema de sincronização para um banco de dados de membro de sincronização ou um banco de dados de hub de sincronização.</span><span class="sxs-lookup"><span data-stu-id="05952-103">Update the sync schema for a sync member database or a sync hub database.</span></span>
<span data-ttu-id="05952-104">Ele obterá o esquema de banco de dados mais recente do banco de dados real e o usará para atualizar o esquema armazenado em cache pelo banco de dados de metadados sync.</span><span class="sxs-lookup"><span data-stu-id="05952-104">It will get the latest database schema from the real database and then use it refresh the schema cached by Sync metadata database.</span></span>
<span data-ttu-id="05952-105">Se "SyncMemberName" for especificado, ele atualizará o esquema de banco de dados membro; caso não seja, ele atualizará o esquema de banco de dados do hub.</span><span class="sxs-lookup"><span data-stu-id="05952-105">If "SyncMemberName" is specified, it will refresh the member database schema; if not, it will refresh the hub database schema.</span></span>

## <span data-ttu-id="05952-106">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="05952-106">SYNTAX</span></span>

```
Update-AzSqlSyncSchema [-SyncGroupName] <String> [-SyncMemberName <String>] [-PassThru] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05952-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="05952-107">DESCRIPTION</span></span>
<span data-ttu-id="05952-108">O cmdlet **Update-AzSqlSyncSchema** atualiza o esquema de sincronização para um banco de dados de membro de sincronização ou um banco de dados de hub de sincronização.</span><span class="sxs-lookup"><span data-stu-id="05952-108">The **Update-AzSqlSyncSchema** cmdlet updates the sync schema for a sync member database or a sync hub database.</span></span>

## <span data-ttu-id="05952-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="05952-109">EXAMPLES</span></span>

### <span data-ttu-id="05952-110">Exemplo 1: atualizar o esquema de sincronização para um banco de dados de hub</span><span class="sxs-lookup"><span data-stu-id="05952-110">Example 1: Update the sync schema for a hub database</span></span>
```
PS C:\>Update-AzSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01"
```

<span data-ttu-id="05952-111">Este comando atualiza o esquema de sincronização do banco de dados de hub na sincronização do grupo de sincronizaçãoGroup01</span><span class="sxs-lookup"><span data-stu-id="05952-111">This command updates the sync schema for the hub database in the sync group syncGroup01</span></span>

### <span data-ttu-id="05952-112">Exemplo 2: atualizar o esquema de sincronização de um banco de dados membro</span><span class="sxs-lookup"><span data-stu-id="05952-112">Example 2: Update the sync schema for a member database</span></span>
```
PS C:\>Update-AzSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01" -SyncMemberName "syncMember01"
```

<span data-ttu-id="05952-113">Este comando atualiza o esquema de sincronização do banco de dados membro na sincronização de membros de sincronizaçãoMember01</span><span class="sxs-lookup"><span data-stu-id="05952-113">This command updates the sync schema for the member database in the sync member syncMember01</span></span>

## <span data-ttu-id="05952-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="05952-114">PARAMETERS</span></span>

### <span data-ttu-id="05952-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="05952-115">-DatabaseName</span></span>
<span data-ttu-id="05952-116">O nome do banco de dados do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="05952-116">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="05952-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05952-117">-DefaultProfile</span></span>
<span data-ttu-id="05952-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="05952-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="05952-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="05952-119">-PassThru</span></span>
<span data-ttu-id="05952-120">Define se o grupo de sincronização no qual esse cmdlet funciona</span><span class="sxs-lookup"><span data-stu-id="05952-120">Defines Whether return the sync group this cmdlet works on</span></span>

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

### <span data-ttu-id="05952-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05952-121">-ResourceGroupName</span></span>
<span data-ttu-id="05952-122">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="05952-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="05952-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="05952-123">-ServerName</span></span>
<span data-ttu-id="05952-124">O nome do Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="05952-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="05952-125">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="05952-125">-SyncGroupName</span></span>
<span data-ttu-id="05952-126">O nome do grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="05952-126">The sync group name.</span></span>

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

### <span data-ttu-id="05952-127">-SyncMemberName</span><span class="sxs-lookup"><span data-stu-id="05952-127">-SyncMemberName</span></span>
<span data-ttu-id="05952-128">O nome do membro de sincronização.</span><span class="sxs-lookup"><span data-stu-id="05952-128">The sync member name.</span></span>

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

### <span data-ttu-id="05952-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="05952-129">-Confirm</span></span>
<span data-ttu-id="05952-130">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="05952-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05952-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05952-131">-WhatIf</span></span>
<span data-ttu-id="05952-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="05952-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05952-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="05952-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05952-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05952-134">CommonParameters</span></span>
<span data-ttu-id="05952-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05952-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05952-136">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="05952-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05952-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="05952-137">INPUTS</span></span>

### <span data-ttu-id="05952-138">System.String</span><span class="sxs-lookup"><span data-stu-id="05952-138">System.String</span></span>

## <span data-ttu-id="05952-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="05952-139">OUTPUTS</span></span>

### <span data-ttu-id="05952-140">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="05952-140">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="05952-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="05952-141">NOTES</span></span>

## <span data-ttu-id="05952-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="05952-142">RELATED LINKS</span></span>
