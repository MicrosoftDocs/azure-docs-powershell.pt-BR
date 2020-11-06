---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlSyncMember.md
ms.openlocfilehash: b96d125b2a4f608c54024619ca6259a136d2ed69
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428718"
---
# <span data-ttu-id="af0dc-101">Remove-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="af0dc-101">Remove-AzureRmSqlSyncMember</span></span>

## <span data-ttu-id="af0dc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="af0dc-102">SYNOPSIS</span></span>
<span data-ttu-id="af0dc-103">Remove um membro de sincronização do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="af0dc-103">Removes an Azure SQL Database Sync Member.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af0dc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="af0dc-104">SYNTAX</span></span>

```
Remove-AzureRmSqlSyncMember -Name <String> [-Force] [-PassThru] [-SyncGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af0dc-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="af0dc-105">DESCRIPTION</span></span>
<span data-ttu-id="af0dc-106">O cmdlet **Remove-AzureRmSqlSyncMember** remove um membro de sincronização do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="af0dc-106">The **Remove-AzureRmSqlSyncMember** cmdlet removes an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="af0dc-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="af0dc-107">EXAMPLES</span></span>

### <span data-ttu-id="af0dc-108">Exemplo 1: remover um membro de sincronização</span><span class="sxs-lookup"><span data-stu-id="af0dc-108">Example 1: Remove a sync member</span></span>
```
PS C:\>Remove-AzureRmSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01" -Name "syncMember01"
```

<span data-ttu-id="af0dc-109">Esse comando Remove o membro de sincronização do banco de dados SQL do Azure chamado syncMember01.</span><span class="sxs-lookup"><span data-stu-id="af0dc-109">This command removes the Azure SQL Database Sync Member named syncMember01.</span></span>

## <span data-ttu-id="af0dc-110">OS</span><span class="sxs-lookup"><span data-stu-id="af0dc-110">PARAMETERS</span></span>

### <span data-ttu-id="af0dc-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="af0dc-111">-DatabaseName</span></span>
<span data-ttu-id="af0dc-112">O nome do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="af0dc-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="af0dc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af0dc-113">-DefaultProfile</span></span>
<span data-ttu-id="af0dc-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="af0dc-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="af0dc-115">-Force</span><span class="sxs-lookup"><span data-stu-id="af0dc-115">-Force</span></span>
<span data-ttu-id="af0dc-116">Ignorar a mensagem de confirmação para executar a ação</span><span class="sxs-lookup"><span data-stu-id="af0dc-116">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="af0dc-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="af0dc-117">-Name</span></span>
<span data-ttu-id="af0dc-118">O nome do membro de sincronização.</span><span class="sxs-lookup"><span data-stu-id="af0dc-118">The sync member name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SyncMemberName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af0dc-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="af0dc-119">-PassThru</span></span>
<span data-ttu-id="af0dc-120">Define se retornar o membro de sincronização removido</span><span class="sxs-lookup"><span data-stu-id="af0dc-120">Defines Whether return the removed sync member</span></span>

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

### <span data-ttu-id="af0dc-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af0dc-121">-ResourceGroupName</span></span>
<span data-ttu-id="af0dc-122">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="af0dc-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="af0dc-123">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="af0dc-123">-ServerName</span></span>
<span data-ttu-id="af0dc-124">O nome do Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="af0dc-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="af0dc-125">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="af0dc-125">-SyncGroupName</span></span>
<span data-ttu-id="af0dc-126">O nome do grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="af0dc-126">The sync group name.</span></span>

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

### <span data-ttu-id="af0dc-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="af0dc-127">-Confirm</span></span>
<span data-ttu-id="af0dc-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af0dc-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af0dc-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af0dc-129">-WhatIf</span></span>
<span data-ttu-id="af0dc-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="af0dc-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af0dc-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="af0dc-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af0dc-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af0dc-132">CommonParameters</span></span>
<span data-ttu-id="af0dc-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af0dc-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af0dc-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af0dc-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af0dc-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="af0dc-135">INPUTS</span></span>

### <span data-ttu-id="af0dc-136">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="af0dc-136">None</span></span>
<span data-ttu-id="af0dc-137">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="af0dc-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="af0dc-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="af0dc-138">OUTPUTS</span></span>

### <span data-ttu-id="af0dc-139">Microsoft. Azure. Commands. Sql. datasync. Model. AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="af0dc-139">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="af0dc-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="af0dc-140">NOTES</span></span>

## <span data-ttu-id="af0dc-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="af0dc-141">RELATED LINKS</span></span>

[<span data-ttu-id="af0dc-142">New-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="af0dc-142">New-AzureRmSqlSyncMember</span></span>](./New-AzureRmSqlSyncMember.md)

[<span data-ttu-id="af0dc-143">Update-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="af0dc-143">Update-AzureRmSqlSyncMember</span></span>](./Update-AzureRmSqlSyncMember.md)

[<span data-ttu-id="af0dc-144">Get-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="af0dc-144">Get-AzureRmSqlSyncMember</span></span>](./Get-AzureRmSqlSyncMember.md)

