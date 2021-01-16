---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/start-azsqlsyncgroupsync
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlSyncGroupSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlSyncGroupSync.md
ms.openlocfilehash: e35187bf22015f3398a9fd95ce60a1cd597f7c22
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260117"
---
# <span data-ttu-id="037f8-101">Start-AzSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="037f8-101">Start-AzSqlSyncGroupSync</span></span>

## <span data-ttu-id="037f8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="037f8-102">SYNOPSIS</span></span>
<span data-ttu-id="037f8-103">Inicia uma sincronização de grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="037f8-103">Starts a sync group synchronization.</span></span>

## <span data-ttu-id="037f8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="037f8-104">SYNTAX</span></span>

```
Start-AzSqlSyncGroupSync [-SyncGroupName] <String> [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="037f8-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="037f8-105">DESCRIPTION</span></span>
<span data-ttu-id="037f8-106">O cmdlet **Start-AzSqlSyncGroupSync** inicia uma sincronização de grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="037f8-106">The **Start-AzSqlSyncGroupSync** cmdlet starts a sync group synchronization.</span></span>

## <span data-ttu-id="037f8-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="037f8-107">EXAMPLES</span></span>

### <span data-ttu-id="037f8-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="037f8-108">Example 1</span></span>
```
PS C:\> Start-AzSqlSyncGroupSync -SyncGroupName mysg [-ServerName] mysrv [-DatabaseName] mydb [-ResourceGroupName] myrg
```

<span data-ttu-id="037f8-109">Esse comando inicia uma arredondamento de sincronização para o grupo de sincronização mysg.</span><span class="sxs-lookup"><span data-stu-id="037f8-109">This command starts a round of synchronization for the sync group mysg.</span></span>

## <span data-ttu-id="037f8-110">OS</span><span class="sxs-lookup"><span data-stu-id="037f8-110">PARAMETERS</span></span>

### <span data-ttu-id="037f8-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="037f8-111">-DatabaseName</span></span>
<span data-ttu-id="037f8-112">O nome do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="037f8-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="037f8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="037f8-113">-DefaultProfile</span></span>
<span data-ttu-id="037f8-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="037f8-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="037f8-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="037f8-115">-PassThru</span></span>
<span data-ttu-id="037f8-116">Define se retornar o grupo de sincronização</span><span class="sxs-lookup"><span data-stu-id="037f8-116">Defines Whether return the sync group</span></span>

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

### <span data-ttu-id="037f8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="037f8-117">-ResourceGroupName</span></span>
<span data-ttu-id="037f8-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="037f8-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="037f8-119">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="037f8-119">-ServerName</span></span>
<span data-ttu-id="037f8-120">O nome do Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="037f8-120">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="037f8-121">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="037f8-121">-SyncGroupName</span></span>
<span data-ttu-id="037f8-122">O nome do grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="037f8-122">The sync group name.</span></span>

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

### <span data-ttu-id="037f8-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="037f8-123">-Confirm</span></span>
<span data-ttu-id="037f8-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="037f8-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="037f8-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="037f8-125">-WhatIf</span></span>
<span data-ttu-id="037f8-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="037f8-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="037f8-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="037f8-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="037f8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="037f8-128">CommonParameters</span></span>
<span data-ttu-id="037f8-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="037f8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="037f8-130">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="037f8-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="037f8-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="037f8-131">INPUTS</span></span>

### <span data-ttu-id="037f8-132">System. String</span><span class="sxs-lookup"><span data-stu-id="037f8-132">System.String</span></span>

## <span data-ttu-id="037f8-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="037f8-133">OUTPUTS</span></span>

### <span data-ttu-id="037f8-134">Microsoft. Azure. Commands. Sql. datasync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="037f8-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="037f8-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="037f8-135">NOTES</span></span>

## <span data-ttu-id="037f8-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="037f8-136">RELATED LINKS</span></span>

[<span data-ttu-id="037f8-137">Parar-AzSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="037f8-137">Stop-AzSqlSyncGroupSync</span></span>](./Stop-AzSqlSyncGroupSync.md)

