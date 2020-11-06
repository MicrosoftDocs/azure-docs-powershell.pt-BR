---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlSyncGroupSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlSyncGroupSync.md
ms.openlocfilehash: 8a472307c475e093de6f8e6071c137afda5ec1f1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610147"
---
# <span data-ttu-id="4581f-101">Stop-AzureRmSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="4581f-101">Stop-AzureRmSqlSyncGroupSync</span></span>

## <span data-ttu-id="4581f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4581f-102">SYNOPSIS</span></span>
<span data-ttu-id="4581f-103">Interrompe a sincronização de um grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="4581f-103">Stops a sync group synchronization.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4581f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4581f-104">SYNTAX</span></span>

```
Stop-AzureRmSqlSyncGroupSync [-SyncGroupName] <String> [-PassThru] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4581f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4581f-105">DESCRIPTION</span></span>
<span data-ttu-id="4581f-106">O cmdlet **Stop-AzureRmSqlSyncGroupSync** interrompe uma sincronização de grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="4581f-106">The **Stop-AzureRmSqlSyncGroupSync** cmdlet stops a sync group synchronization.</span></span>

## <span data-ttu-id="4581f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4581f-107">EXAMPLES</span></span>

### <span data-ttu-id="4581f-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4581f-108">Example 1</span></span>
```
PS C:\> Stop-AzureRmSqlSyncGroupSync -SyncGroupName mysg [-ServerName] mysrv [-DatabaseName] mydb [-ResourceGroupName] myrg
```

<span data-ttu-id="4581f-109">Esse comando interrompe a sincronização que está em andamento para o grupo de sincronização mysg.</span><span class="sxs-lookup"><span data-stu-id="4581f-109">This command stops the synchronization which is ongoing for the sync group mysg.</span></span>

## <span data-ttu-id="4581f-110">OS</span><span class="sxs-lookup"><span data-stu-id="4581f-110">PARAMETERS</span></span>

### <span data-ttu-id="4581f-111">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4581f-111">-Confirm</span></span>
<span data-ttu-id="4581f-112">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4581f-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4581f-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4581f-113">-DatabaseName</span></span>
<span data-ttu-id="4581f-114">O nome do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="4581f-114">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="4581f-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4581f-115">-PassThru</span></span>
<span data-ttu-id="4581f-116">Define se retornar o grupo de sincronização</span><span class="sxs-lookup"><span data-stu-id="4581f-116">Defines Whether return the sync group</span></span>

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

### <span data-ttu-id="4581f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4581f-117">-ResourceGroupName</span></span>
<span data-ttu-id="4581f-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4581f-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="4581f-119">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="4581f-119">-ServerName</span></span>
<span data-ttu-id="4581f-120">O nome do Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="4581f-120">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="4581f-121">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="4581f-121">-SyncGroupName</span></span>
<span data-ttu-id="4581f-122">O nome do grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="4581f-122">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4581f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4581f-123">-WhatIf</span></span>
<span data-ttu-id="4581f-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4581f-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4581f-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4581f-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4581f-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4581f-126">-DefaultProfile</span></span>
<span data-ttu-id="4581f-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4581f-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4581f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4581f-128">CommonParameters</span></span>
<span data-ttu-id="4581f-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4581f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4581f-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4581f-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4581f-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4581f-131">INPUTS</span></span>

## <span data-ttu-id="4581f-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4581f-132">OUTPUTS</span></span>

### <span data-ttu-id="4581f-133">Microsoft. Azure. Commands. Sql. datasync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="4581f-133">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="4581f-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4581f-134">NOTES</span></span>

## <span data-ttu-id="4581f-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4581f-135">RELATED LINKS</span></span>

[<span data-ttu-id="4581f-136">Start-AzureRmSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="4581f-136">Start-AzureRmSqlSyncGroupSync</span></span>](./Start-AzureRmSqlSyncGroupSync.md)

