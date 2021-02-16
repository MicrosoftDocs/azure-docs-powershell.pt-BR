---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/update-azsqlsyncschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncSchema.md
ms.openlocfilehash: 571bef6b10420f08e7b1a00bdfddd4415ba0e033
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113701"
---
# <span data-ttu-id="c74b3-101">Update-AzSqlSyncSchema</span><span class="sxs-lookup"><span data-stu-id="c74b3-101">Update-AzSqlSyncSchema</span></span>

## <span data-ttu-id="c74b3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c74b3-102">SYNOPSIS</span></span>
<span data-ttu-id="c74b3-103">Atualize o esquema de sincronização de um banco de dados de membro de sincronização ou um banco de dados do hub de sincronização.</span><span class="sxs-lookup"><span data-stu-id="c74b3-103">Update the sync schema for a sync member database or a sync hub database.</span></span>
<span data-ttu-id="c74b3-104">Ele obterá o esquema mais recente do banco de dados real e o usará para atualizar o esquema armazenado em cache pelo banco de dados sincronizar metadados.</span><span class="sxs-lookup"><span data-stu-id="c74b3-104">It will get the latest database schema from the real database and then use it refresh the schema cached by Sync metadata database.</span></span>
<span data-ttu-id="c74b3-105">Se "SyncMemberName" for especificado, ele atualizará o esquema de banco de dados do membro; caso não, ele atualizará o esquema de banco de dados do hub.</span><span class="sxs-lookup"><span data-stu-id="c74b3-105">If "SyncMemberName" is specified, it will refresh the member database schema; if not, it will refresh the hub database schema.</span></span>

## <span data-ttu-id="c74b3-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c74b3-106">SYNTAX</span></span>

```
Update-AzSqlSyncSchema [-SyncGroupName] <String> [-SyncMemberName <String>] [-PassThru] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c74b3-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="c74b3-107">DESCRIPTION</span></span>
<span data-ttu-id="c74b3-108">O cmdlet **Update-AzSqlSyncSchema** atualiza o esquema de sincronização de um banco de dados de membro de sincronização ou um banco de dados do hub de sincronização.</span><span class="sxs-lookup"><span data-stu-id="c74b3-108">The **Update-AzSqlSyncSchema** cmdlet updates the sync schema for a sync member database or a sync hub database.</span></span>

## <span data-ttu-id="c74b3-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c74b3-109">EXAMPLES</span></span>

### <span data-ttu-id="c74b3-110">Exemplo 1: Atualizar o esquema de sincronização de um banco de dados do hub</span><span class="sxs-lookup"><span data-stu-id="c74b3-110">Example 1: Update the sync schema for a hub database</span></span>
```
PS C:\>Update-AzSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01"
```

<span data-ttu-id="c74b3-111">Este comando atualiza o esquema de sincronização do banco de dados do hub no grupo de sincronização SyncGroup01</span><span class="sxs-lookup"><span data-stu-id="c74b3-111">This command updates the sync schema for the hub database in the sync group syncGroup01</span></span>

### <span data-ttu-id="c74b3-112">Exemplo 2: Atualizar o esquema de sincronização de um banco de dados de membro</span><span class="sxs-lookup"><span data-stu-id="c74b3-112">Example 2: Update the sync schema for a member database</span></span>
```
PS C:\>Update-AzSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01" -SyncMemberName "syncMember01"
```

<span data-ttu-id="c74b3-113">Este comando atualiza o esquema de sincronização do banco de dados do membro no membro de sincronização do membro de sincronização01</span><span class="sxs-lookup"><span data-stu-id="c74b3-113">This command updates the sync schema for the member database in the sync member syncMember01</span></span>

## <span data-ttu-id="c74b3-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c74b3-114">PARAMETERS</span></span>

### <span data-ttu-id="c74b3-115">-Nomedo Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="c74b3-115">-DatabaseName</span></span>
<span data-ttu-id="c74b3-116">O nome do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="c74b3-116">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="c74b3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c74b3-117">-DefaultProfile</span></span>
<span data-ttu-id="c74b3-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="c74b3-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c74b3-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c74b3-119">-PassThru</span></span>
<span data-ttu-id="c74b3-120">Define se o grupo de sincronização do return este cmdlet funciona</span><span class="sxs-lookup"><span data-stu-id="c74b3-120">Defines Whether return the sync group this cmdlet works on</span></span>

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

### <span data-ttu-id="c74b3-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c74b3-121">-ResourceGroupName</span></span>
<span data-ttu-id="c74b3-122">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c74b3-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="c74b3-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c74b3-123">-ServerName</span></span>
<span data-ttu-id="c74b3-124">O nome do SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="c74b3-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="c74b3-125">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="c74b3-125">-SyncGroupName</span></span>
<span data-ttu-id="c74b3-126">O nome do grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="c74b3-126">The sync group name.</span></span>

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

### <span data-ttu-id="c74b3-127">-SyncMemberName</span><span class="sxs-lookup"><span data-stu-id="c74b3-127">-SyncMemberName</span></span>
<span data-ttu-id="c74b3-128">O nome do membro de sincronização.</span><span class="sxs-lookup"><span data-stu-id="c74b3-128">The sync member name.</span></span>

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

### <span data-ttu-id="c74b3-129">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="c74b3-129">-Confirm</span></span>
<span data-ttu-id="c74b3-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c74b3-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c74b3-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c74b3-131">-WhatIf</span></span>
<span data-ttu-id="c74b3-132">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="c74b3-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c74b3-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c74b3-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c74b3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c74b3-134">CommonParameters</span></span>
<span data-ttu-id="c74b3-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c74b3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c74b3-136">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c74b3-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c74b3-137">Entradas</span><span class="sxs-lookup"><span data-stu-id="c74b3-137">INPUTS</span></span>

### <span data-ttu-id="c74b3-138">System.String</span><span class="sxs-lookup"><span data-stu-id="c74b3-138">System.String</span></span>

## <span data-ttu-id="c74b3-139">Saídas</span><span class="sxs-lookup"><span data-stu-id="c74b3-139">OUTPUTS</span></span>

### <span data-ttu-id="c74b3-140">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="c74b3-140">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="c74b3-141">Notas</span><span class="sxs-lookup"><span data-stu-id="c74b3-141">NOTES</span></span>

## <span data-ttu-id="c74b3-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c74b3-142">RELATED LINKS</span></span>
