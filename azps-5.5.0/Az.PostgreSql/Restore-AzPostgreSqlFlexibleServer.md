---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/restore-azpostgresqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Restore-AzPostgreSqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Restore-AzPostgreSqlFlexibleServer.md
ms.openlocfilehash: e8554f0ac88cf3d69e36282b7e310cc92b41d6db
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111488"
---
# <span data-ttu-id="57121-101">Restore-AzPostgreSqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="57121-101">Restore-AzPostgreSqlFlexibleServer</span></span>

## <span data-ttu-id="57121-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="57121-102">SYNOPSIS</span></span>
<span data-ttu-id="57121-103">Restaurar um servidor flexível PostgreSQL de um backup existente</span><span class="sxs-lookup"><span data-stu-id="57121-103">Restore a PostgreSQL flexible server from an existing backup</span></span>

## <span data-ttu-id="57121-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="57121-104">SYNTAX</span></span>

```
Restore-AzPostgreSqlFlexibleServer -Name <String> -ResourceGroupName <String> -SourceServerName <String>
 -Location <String> -RestorePointInTime <DateTime> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="57121-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="57121-105">DESCRIPTION</span></span>
<span data-ttu-id="57121-106">Restaurar um servidor de um backup existente</span><span class="sxs-lookup"><span data-stu-id="57121-106">Restore a server from an existing backup</span></span>

## <span data-ttu-id="57121-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="57121-107">EXAMPLES</span></span>

### <span data-ttu-id="57121-108">Exemplo 1: Restaurar o servidor PostgreSql usando a Restauração do PointInTime</span><span class="sxs-lookup"><span data-stu-id="57121-108">Example 1: Restore PostgreSql server using PointInTime Restore</span></span>
```powershell
PS C:\> $restorePointInTime = (Get-Date).AddMinutes(-10)
PS C:\> Restore-AzPostgreSqlFlexibleServer -Name pg-restore -ResourceGroupName PowershellPostgreSqlTest -SourceServerName postgresql-test -Location eastus -RestorePointInTime $restorePointInTime 

Name       Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier       
----       -------- ------------------ ------- ----------------------- -------          -------       
pg-restore eastus   postgresql_test         12     131072              Standard_D2s_v3 GeneralPurpose
```

<span data-ttu-id="57121-109">Esses cmdlets restauram o servidor PostgreSql usando a Restauração do PointInTime.</span><span class="sxs-lookup"><span data-stu-id="57121-109">These cmdlets restore PostgreSql server using PointInTime Restore.</span></span>

## <span data-ttu-id="57121-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="57121-110">PARAMETERS</span></span>

### <span data-ttu-id="57121-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="57121-111">-AsJob</span></span>
<span data-ttu-id="57121-112">Execute o comando como um trabalho.</span><span class="sxs-lookup"><span data-stu-id="57121-112">Run the command as a job.</span></span>

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

### <span data-ttu-id="57121-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57121-113">-DefaultProfile</span></span>
<span data-ttu-id="57121-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="57121-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57121-115">-Local</span><span class="sxs-lookup"><span data-stu-id="57121-115">-Location</span></span>
<span data-ttu-id="57121-116">O local em que o recurso reside.</span><span class="sxs-lookup"><span data-stu-id="57121-116">The location the resource resides in.</span></span>

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

### <span data-ttu-id="57121-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="57121-117">-Name</span></span>
<span data-ttu-id="57121-118">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="57121-118">The name of the server.</span></span>

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

### <span data-ttu-id="57121-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="57121-119">-NoWait</span></span>
<span data-ttu-id="57121-120">Execute o comando assíncrona.</span><span class="sxs-lookup"><span data-stu-id="57121-120">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="57121-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57121-121">-ResourceGroupName</span></span>
<span data-ttu-id="57121-122">O nome do grupo de recursos que contém o recurso, Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="57121-122">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="57121-123">-RestorePointInTime</span><span class="sxs-lookup"><span data-stu-id="57121-123">-RestorePointInTime</span></span>
<span data-ttu-id="57121-124">O ponto a ser restaurado (formato ISO8601), por exemplo, 2017-04-26T02:10:00+08:00.</span><span class="sxs-lookup"><span data-stu-id="57121-124">The point in time to restore from (ISO8601 format), e.g., 2017-04-26T02:10:00+08:00.</span></span>

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

### <span data-ttu-id="57121-125">-SourceServerName</span><span class="sxs-lookup"><span data-stu-id="57121-125">-SourceServerName</span></span>
<span data-ttu-id="57121-126">O nome do servidor de origem.</span><span class="sxs-lookup"><span data-stu-id="57121-126">The name of the source server.</span></span>

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

### <span data-ttu-id="57121-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="57121-127">-SubscriptionId</span></span>
<span data-ttu-id="57121-128">A ID da assinatura que identifica uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="57121-128">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="57121-129">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="57121-129">-Confirm</span></span>
<span data-ttu-id="57121-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57121-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57121-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57121-131">-WhatIf</span></span>
<span data-ttu-id="57121-132">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="57121-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57121-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="57121-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57121-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57121-134">CommonParameters</span></span>
<span data-ttu-id="57121-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57121-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57121-136">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="57121-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57121-137">Entradas</span><span class="sxs-lookup"><span data-stu-id="57121-137">INPUTS</span></span>

## <span data-ttu-id="57121-138">Saídas</span><span class="sxs-lookup"><span data-stu-id="57121-138">OUTPUTS</span></span>

### <span data-ttu-id="57121-139">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IServerAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="57121-139">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IServerAutoGenerated</span></span>

## <span data-ttu-id="57121-140">Notas</span><span class="sxs-lookup"><span data-stu-id="57121-140">NOTES</span></span>

<span data-ttu-id="57121-141">Aliases</span><span class="sxs-lookup"><span data-stu-id="57121-141">ALIASES</span></span>

## <span data-ttu-id="57121-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="57121-142">RELATED LINKS</span></span>

