---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/start-azsqlsyncgroupsync
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlSyncGroupSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlSyncGroupSync.md
ms.openlocfilehash: 6e6f0279f8cf3e0ea4481e31b06c42c25d0a0180
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773943"
---
# <span data-ttu-id="4ae95-101">Start-AzSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="4ae95-101">Start-AzSqlSyncGroupSync</span></span>

## <span data-ttu-id="4ae95-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4ae95-102">SYNOPSIS</span></span>
<span data-ttu-id="4ae95-103">Inicia uma sincronização de grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="4ae95-103">Starts a sync group synchronization.</span></span>

## <span data-ttu-id="4ae95-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4ae95-104">SYNTAX</span></span>

```
Start-AzSqlSyncGroupSync [-SyncGroupName] <String> [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4ae95-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4ae95-105">DESCRIPTION</span></span>
<span data-ttu-id="4ae95-106">O cmdlet **Start-AzSqlSyncGroupSync** inicia uma sincronização de grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="4ae95-106">The **Start-AzSqlSyncGroupSync** cmdlet starts a sync group synchronization.</span></span>

## <span data-ttu-id="4ae95-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4ae95-107">EXAMPLES</span></span>

### <span data-ttu-id="4ae95-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4ae95-108">Example 1</span></span>
```
PS C:\> Start-AzSqlSyncGroupSync -SyncGroupName mysg [-ServerName] mysrv [-DatabaseName] mydb [-ResourceGroupName] myrg
```

<span data-ttu-id="4ae95-109">Esse comando inicia uma arredondamento de sincronização para o grupo de sincronização mysg.</span><span class="sxs-lookup"><span data-stu-id="4ae95-109">This command starts a round of synchronization for the sync group mysg.</span></span>

## <span data-ttu-id="4ae95-110">OS</span><span class="sxs-lookup"><span data-stu-id="4ae95-110">PARAMETERS</span></span>

### <span data-ttu-id="4ae95-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4ae95-111">-DatabaseName</span></span>
<span data-ttu-id="4ae95-112">O nome do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="4ae95-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="4ae95-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ae95-113">-DefaultProfile</span></span>
<span data-ttu-id="4ae95-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="4ae95-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4ae95-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4ae95-115">-PassThru</span></span>
<span data-ttu-id="4ae95-116">Define se retornar o grupo de sincronização</span><span class="sxs-lookup"><span data-stu-id="4ae95-116">Defines Whether return the sync group</span></span>

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

### <span data-ttu-id="4ae95-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ae95-117">-ResourceGroupName</span></span>
<span data-ttu-id="4ae95-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4ae95-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="4ae95-119">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="4ae95-119">-ServerName</span></span>
<span data-ttu-id="4ae95-120">O nome do Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="4ae95-120">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="4ae95-121">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="4ae95-121">-SyncGroupName</span></span>
<span data-ttu-id="4ae95-122">O nome do grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="4ae95-122">The sync group name.</span></span>

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

### <span data-ttu-id="4ae95-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4ae95-123">-Confirm</span></span>
<span data-ttu-id="4ae95-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ae95-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ae95-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ae95-125">-WhatIf</span></span>
<span data-ttu-id="4ae95-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4ae95-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ae95-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4ae95-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ae95-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ae95-128">CommonParameters</span></span>
<span data-ttu-id="4ae95-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ae95-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ae95-130">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4ae95-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ae95-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4ae95-131">INPUTS</span></span>

### <span data-ttu-id="4ae95-132">System. String</span><span class="sxs-lookup"><span data-stu-id="4ae95-132">System.String</span></span>

## <span data-ttu-id="4ae95-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4ae95-133">OUTPUTS</span></span>

### <span data-ttu-id="4ae95-134">Microsoft. Azure. Commands. Sql. datasync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="4ae95-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="4ae95-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4ae95-135">NOTES</span></span>

## <span data-ttu-id="4ae95-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4ae95-136">RELATED LINKS</span></span>

[<span data-ttu-id="4ae95-137">Parar-AzSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="4ae95-137">Stop-AzSqlSyncGroupSync</span></span>](./Stop-AzSqlSyncGroupSync.md)
