---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlSyncGroup.md
ms.openlocfilehash: 99892ee748de030a045bd9d0a022051206236198
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610983"
---
# <span data-ttu-id="d7958-101">Remove-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="d7958-101">Remove-AzureRmSqlSyncGroup</span></span>

## <span data-ttu-id="d7958-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d7958-102">SYNOPSIS</span></span>
<span data-ttu-id="d7958-103">Remove um grupo de sincronização do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="d7958-103">Removes an Azure SQL Database Sync Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7958-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d7958-104">SYNTAX</span></span>

```
Remove-AzureRmSqlSyncGroup [-Name] <String> [-Force] [-PassThru] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7958-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d7958-105">DESCRIPTION</span></span>
<span data-ttu-id="d7958-106">O cmdlet **Remove-AzureRmSqlSyncGroup** remove um grupo de sincronização do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="d7958-106">The **Remove-AzureRmSqlSyncGroup** cmdlet removes an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="d7958-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d7958-107">EXAMPLES</span></span>

### <span data-ttu-id="d7958-108">Exemplo 1: remover um grupo de sincronização</span><span class="sxs-lookup"><span data-stu-id="d7958-108">Example 1: Remove a sync group</span></span>
```
PS C:\>Remove-AzureRmSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -Name "syncGroup01"
```

<span data-ttu-id="d7958-109">Esse comando Remove o grupo de sincronização do banco de dados SQL do Azure chamado syncGroup01.</span><span class="sxs-lookup"><span data-stu-id="d7958-109">This command removes the Azure SQL Database Sync Group named syncGroup01.</span></span>

## <span data-ttu-id="d7958-110">OS</span><span class="sxs-lookup"><span data-stu-id="d7958-110">PARAMETERS</span></span>

### <span data-ttu-id="d7958-111">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d7958-111">-Confirm</span></span>
<span data-ttu-id="d7958-112">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7958-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7958-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d7958-113">-DatabaseName</span></span>
<span data-ttu-id="d7958-114">O nome do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="d7958-114">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="d7958-115">-Force</span><span class="sxs-lookup"><span data-stu-id="d7958-115">-Force</span></span>
<span data-ttu-id="d7958-116">Ignorar a mensagem de confirmação para executar a ação</span><span class="sxs-lookup"><span data-stu-id="d7958-116">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="d7958-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="d7958-117">-Name</span></span>
<span data-ttu-id="d7958-118">O nome do grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="d7958-118">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7958-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d7958-119">-PassThru</span></span>
<span data-ttu-id="d7958-120">Define se retorna o grupo de sincronização removido</span><span class="sxs-lookup"><span data-stu-id="d7958-120">Defines Whether return the removed sync group</span></span>

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

### <span data-ttu-id="d7958-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7958-121">-ResourceGroupName</span></span>
<span data-ttu-id="d7958-122">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d7958-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="d7958-123">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="d7958-123">-ServerName</span></span>
<span data-ttu-id="d7958-124">O nome do Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="d7958-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="d7958-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7958-125">-WhatIf</span></span>
<span data-ttu-id="d7958-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d7958-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7958-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d7958-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7958-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7958-128">-DefaultProfile</span></span>
<span data-ttu-id="d7958-129">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d7958-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d7958-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7958-130">CommonParameters</span></span>
<span data-ttu-id="d7958-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7958-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7958-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7958-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7958-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d7958-133">INPUTS</span></span>

## <span data-ttu-id="d7958-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d7958-134">OUTPUTS</span></span>

### <span data-ttu-id="d7958-135">Microsoft. Azure. Commands. Sql. datasync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="d7958-135">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="d7958-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d7958-136">NOTES</span></span>

## <span data-ttu-id="d7958-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d7958-137">RELATED LINKS</span></span>

[<span data-ttu-id="d7958-138">New-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="d7958-138">New-AzureRmSqlSyncGroup</span></span>](./New-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="d7958-139">Update-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="d7958-139">Update-AzureRmSqlSyncGroup</span></span>](./Update-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="d7958-140">Get-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="d7958-140">Get-AzureRmSqlSyncGroup</span></span>](./Get-AzureRmSqlSyncGroup.md)

