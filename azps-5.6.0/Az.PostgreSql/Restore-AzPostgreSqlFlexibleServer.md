---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/restore-azpostgresqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Restore-AzPostgreSqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Restore-AzPostgreSqlFlexibleServer.md
ms.openlocfilehash: 503d20a8473c83a9b2ca7ca1ec19deab6db7103c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885586"
---
# <span data-ttu-id="b0dda-101">Restore-AzPostgreSqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="b0dda-101">Restore-AzPostgreSqlFlexibleServer</span></span>

## <span data-ttu-id="b0dda-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0dda-102">SYNOPSIS</span></span>
<span data-ttu-id="b0dda-103">Restaurar um servidor flexível PostgreSQL de um backup existente</span><span class="sxs-lookup"><span data-stu-id="b0dda-103">Restore a PostgreSQL flexible server from an existing backup</span></span>

## <span data-ttu-id="b0dda-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b0dda-104">SYNTAX</span></span>

```
Restore-AzPostgreSqlFlexibleServer -Name <String> -ResourceGroupName <String> -SourceServerName <String>
 -Location <String> -RestorePointInTime <DateTime> [-SubscriptionId <String>] [-Zone <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b0dda-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b0dda-105">DESCRIPTION</span></span>
<span data-ttu-id="b0dda-106">Restaurar um servidor de um backup existente</span><span class="sxs-lookup"><span data-stu-id="b0dda-106">Restore a server from an existing backup</span></span>

## <span data-ttu-id="b0dda-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b0dda-107">EXAMPLES</span></span>

### <span data-ttu-id="b0dda-108">Exemplo 1: Restaurar servidor PostgreSql usando a Restauração pointintime</span><span class="sxs-lookup"><span data-stu-id="b0dda-108">Example 1: Restore PostgreSql server using PointInTime Restore</span></span>
```powershell
PS C:\> $restorePointInTime = (Get-Date).AddMinutes(-10)
PS C:\> Restore-AzPostgreSqlFlexibleServer -Name pg-restore -ResourceGroupName PowershellPostgreSqlTest -SourceServerName postgresql-test -Location eastus -RestorePointInTime $restorePointInTime 

Name       Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier       
----       -------- ------------------ ------- ----------------------- -------          -------       
pg-restore eastus   postgresql_test         12     131072              Standard_D2s_v3 GeneralPurpose
```

<span data-ttu-id="b0dda-109">Esses cmdlets restauram o servidor PostgreSql usando a Restauração pointInTime.</span><span class="sxs-lookup"><span data-stu-id="b0dda-109">These cmdlets restore PostgreSql server using PointInTime Restore.</span></span>

## <span data-ttu-id="b0dda-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b0dda-110">PARAMETERS</span></span>

### <span data-ttu-id="b0dda-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b0dda-111">-AsJob</span></span>
<span data-ttu-id="b0dda-112">Execute o comando como um trabalho.</span><span class="sxs-lookup"><span data-stu-id="b0dda-112">Run the command as a job.</span></span>

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

### <span data-ttu-id="b0dda-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0dda-113">-DefaultProfile</span></span>
<span data-ttu-id="b0dda-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b0dda-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0dda-115">-Location</span><span class="sxs-lookup"><span data-stu-id="b0dda-115">-Location</span></span>
<span data-ttu-id="b0dda-116">O local em que o recurso reside.</span><span class="sxs-lookup"><span data-stu-id="b0dda-116">The location the resource resides in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0dda-117">-Name</span><span class="sxs-lookup"><span data-stu-id="b0dda-117">-Name</span></span>
<span data-ttu-id="b0dda-118">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="b0dda-118">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0dda-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="b0dda-119">-NoWait</span></span>
<span data-ttu-id="b0dda-120">Execute o comando de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="b0dda-120">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="b0dda-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0dda-121">-ResourceGroupName</span></span>
<span data-ttu-id="b0dda-122">O nome do grupo de recursos que contém o recurso, Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="b0dda-122">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0dda-123">-RestorePointInTime</span><span class="sxs-lookup"><span data-stu-id="b0dda-123">-RestorePointInTime</span></span>
<span data-ttu-id="b0dda-124">O ponto no tempo a ser restaurado (formato ISO8601), por exemplo, 2017-04-26T02:10:00+08:00.</span><span class="sxs-lookup"><span data-stu-id="b0dda-124">The point in time to restore from (ISO8601 format), e.g., 2017-04-26T02:10:00+08:00.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0dda-125">-SourceServerName</span><span class="sxs-lookup"><span data-stu-id="b0dda-125">-SourceServerName</span></span>
<span data-ttu-id="b0dda-126">O nome do servidor de origem.</span><span class="sxs-lookup"><span data-stu-id="b0dda-126">The name of the source server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0dda-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b0dda-127">-SubscriptionId</span></span>
<span data-ttu-id="b0dda-128">A ID da assinatura que identifica uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="b0dda-128">The subscription ID that identifies an Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0dda-129">-Zone</span><span class="sxs-lookup"><span data-stu-id="b0dda-129">-Zone</span></span>
<span data-ttu-id="b0dda-130">Zona de disponibilidade na qual provisionar o recurso.</span><span class="sxs-lookup"><span data-stu-id="b0dda-130">Availability zone into which to provision the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0dda-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b0dda-131">-Confirm</span></span>
<span data-ttu-id="b0dda-132">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b0dda-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0dda-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0dda-133">-WhatIf</span></span>
<span data-ttu-id="b0dda-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b0dda-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0dda-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b0dda-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0dda-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0dda-136">CommonParameters</span></span>
<span data-ttu-id="b0dda-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0dda-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0dda-138">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b0dda-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0dda-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b0dda-139">INPUTS</span></span>

## <span data-ttu-id="b0dda-140">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b0dda-140">OUTPUTS</span></span>

### <span data-ttu-id="b0dda-141">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IServerAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="b0dda-141">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IServerAutoGenerated</span></span>

## <span data-ttu-id="b0dda-142">NOTES</span><span class="sxs-lookup"><span data-stu-id="b0dda-142">NOTES</span></span>

<span data-ttu-id="b0dda-143">ALIASES</span><span class="sxs-lookup"><span data-stu-id="b0dda-143">ALIASES</span></span>

## <span data-ttu-id="b0dda-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b0dda-144">RELATED LINKS</span></span>

