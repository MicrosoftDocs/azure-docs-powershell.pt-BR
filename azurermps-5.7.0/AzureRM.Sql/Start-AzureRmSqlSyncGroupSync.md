---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/start-azurermsqlsyncgroupsync
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Start-AzureRmSqlSyncGroupSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Start-AzureRmSqlSyncGroupSync.md
ms.openlocfilehash: 040b08e328cb06629e706350fa14752fa6918954
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429649"
---
# <span data-ttu-id="5ee05-101">Start-AzureRmSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="5ee05-101">Start-AzureRmSqlSyncGroupSync</span></span>

## <span data-ttu-id="5ee05-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5ee05-102">SYNOPSIS</span></span>
<span data-ttu-id="5ee05-103">Inicia uma sincronização de grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="5ee05-103">Starts a sync group synchronization.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ee05-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5ee05-104">SYNTAX</span></span>

```
Start-AzureRmSqlSyncGroupSync [-SyncGroupName] <String> [-PassThru] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ee05-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5ee05-105">DESCRIPTION</span></span>
<span data-ttu-id="5ee05-106">O cmdlet **Start-AzureRmSqlSyncGroupSync** inicia uma sincronização de grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="5ee05-106">The **Start-AzureRmSqlSyncGroupSync** cmdlet starts a sync group synchronization.</span></span>

## <span data-ttu-id="5ee05-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5ee05-107">EXAMPLES</span></span>

### <span data-ttu-id="5ee05-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5ee05-108">Example 1</span></span>
```
PS C:\> Start-AzureRmSqlSyncGroupSync -SyncGroupName mysg [-ServerName] mysrv [-DatabaseName] mydb [-ResourceGroupName] myrg
```

<span data-ttu-id="5ee05-109">Esse comando inicia uma arredondamento de sincronização para o grupo de sincronização mysg.</span><span class="sxs-lookup"><span data-stu-id="5ee05-109">This command starts a round of synchronization for the sync group mysg.</span></span>

## <span data-ttu-id="5ee05-110">OS</span><span class="sxs-lookup"><span data-stu-id="5ee05-110">PARAMETERS</span></span>

### <span data-ttu-id="5ee05-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5ee05-111">-DatabaseName</span></span>
<span data-ttu-id="5ee05-112">O nome do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="5ee05-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="5ee05-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ee05-113">-DefaultProfile</span></span>
<span data-ttu-id="5ee05-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="5ee05-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5ee05-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5ee05-115">-PassThru</span></span>
<span data-ttu-id="5ee05-116">Define se retornar o grupo de sincronização</span><span class="sxs-lookup"><span data-stu-id="5ee05-116">Defines Whether return the sync group</span></span>

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

### <span data-ttu-id="5ee05-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ee05-117">-ResourceGroupName</span></span>
<span data-ttu-id="5ee05-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5ee05-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="5ee05-119">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="5ee05-119">-ServerName</span></span>
<span data-ttu-id="5ee05-120">O nome do Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="5ee05-120">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="5ee05-121">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="5ee05-121">-SyncGroupName</span></span>
<span data-ttu-id="5ee05-122">O nome do grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="5ee05-122">The sync group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ee05-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5ee05-123">-Confirm</span></span>
<span data-ttu-id="5ee05-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ee05-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ee05-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ee05-125">-WhatIf</span></span>
<span data-ttu-id="5ee05-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5ee05-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ee05-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5ee05-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ee05-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ee05-128">CommonParameters</span></span>
<span data-ttu-id="5ee05-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ee05-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ee05-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ee05-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ee05-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5ee05-131">INPUTS</span></span>

### <span data-ttu-id="5ee05-132">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="5ee05-132">None</span></span>
<span data-ttu-id="5ee05-133">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="5ee05-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5ee05-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5ee05-134">OUTPUTS</span></span>

### <span data-ttu-id="5ee05-135">Microsoft. Azure. Commands. Sql. datasync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="5ee05-135">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="5ee05-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5ee05-136">NOTES</span></span>

## <span data-ttu-id="5ee05-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5ee05-137">RELATED LINKS</span></span>

[<span data-ttu-id="5ee05-138">Parar-AzureRmSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="5ee05-138">Stop-AzureRmSqlSyncGroupSync</span></span>](./Stop-AzureRmSqlSyncGroupSync.md)

