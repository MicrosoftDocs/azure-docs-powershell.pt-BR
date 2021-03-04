---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/new-azpostgresqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlFirewallRule.md
ms.openlocfilehash: 7ba5a72d161f07ae55669ddfa9d0e399d7cf81ab
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892060"
---
# <span data-ttu-id="ffa51-101">New-AzPostgreSqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ffa51-101">New-AzPostgreSqlFirewallRule</span></span>

## <span data-ttu-id="ffa51-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ffa51-102">SYNOPSIS</span></span>
<span data-ttu-id="ffa51-103">Cria uma nova regra de firewall ou atualiza uma regra de firewall existente.</span><span class="sxs-lookup"><span data-stu-id="ffa51-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="ffa51-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ffa51-104">SYNTAX</span></span>

### <span data-ttu-id="ffa51-105">CreateExpanded (Default)</span><span class="sxs-lookup"><span data-stu-id="ffa51-105">CreateExpanded (Default)</span></span>
```
New-AzPostgreSqlFirewallRule -ResourceGroupName <String> -ServerName <String> -EndIPAddress <String>
 -StartIPAddress <String> [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ffa51-106">AllowAll</span><span class="sxs-lookup"><span data-stu-id="ffa51-106">AllowAll</span></span>
```
New-AzPostgreSqlFirewallRule -ResourceGroupName <String> -ServerName <String> -AllowAll [-Name <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="ffa51-107">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="ffa51-107">ClientIPAddress</span></span>
```
New-AzPostgreSqlFirewallRule -ResourceGroupName <String> -ServerName <String> -ClientIPAddress <String>
 [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ffa51-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ffa51-108">DESCRIPTION</span></span>
<span data-ttu-id="ffa51-109">Cria uma nova regra de firewall ou atualiza uma regra de firewall existente.</span><span class="sxs-lookup"><span data-stu-id="ffa51-109">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="ffa51-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ffa51-110">EXAMPLES</span></span>

### <span data-ttu-id="ffa51-111">Exemplo 1: Criar uma nova Regra de Firewall do servidor PostgreSql</span><span class="sxs-lookup"><span data-stu-id="ffa51-111">Example 1: Create a new PostgreSql server Firewall Rule</span></span>
```powershell
PS C:\> New-AzPostgreSqlFirewallRule -Name rule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -EndIPAddress 0.0.0.1 -StartIPAddress 0.0.0.0

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="ffa51-112">Este cmdlets criam uma Regra de Firewall do servidor PostgreSql.</span><span class="sxs-lookup"><span data-stu-id="ffa51-112">This cmdlets create a PostgreSql server Firewall Rule.</span></span>

### <span data-ttu-id="ffa51-113">Exemplo 2: Criar uma nova Regra de Firewall PostgreSql usando -ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="ffa51-113">Example 2: Create a new PostgreSql Firewall Rule using -ClientIPAddress.</span></span>
```powershell
PS C:\> New-AzPostgreSqlFirewallRule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -ClientIPAddress 0.0.0.1

Name                                StartIPAddress EndIPAddress
----                                -------------- ------------
ClientIPAddress_2020-08-11_18-19-27 0.0.0.1        0.0.0.1
```

<span data-ttu-id="ffa51-114">Este cmdlets criam uma Regra de Firewall PostgreSql usando -ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="ffa51-114">This cmdlets create a PostgreSql Firewall Rule using -ClientIPAddress.</span></span>

### <span data-ttu-id="ffa51-115">Exemplo 3: Criar uma nova Regra de Firewall PostgreSql para permitir que todos os IPs</span><span class="sxs-lookup"><span data-stu-id="ffa51-115">Example 3: Create a new PostgreSql Firewall Rule to allow all IPs</span></span>
```powershell
PS C:\> New-AzPostgreSqlFirewallRule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -AllowAll

Name                         StartIPAddress EndIPAddress
----                         -------------- ------------
AllowAll_2020-08-11_18-19-27 0.0.0.0        255.255.255.255
```

<span data-ttu-id="ffa51-116">Esses cmdlets criam uma nova Regra de Firewall PostgreSql para permitir todos os IPs.</span><span class="sxs-lookup"><span data-stu-id="ffa51-116">This cmdlets create a new PostgreSql Firewall Rule to allow all IPs.</span></span>

## <span data-ttu-id="ffa51-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ffa51-117">PARAMETERS</span></span>

### <span data-ttu-id="ffa51-118">-AllowAll</span><span class="sxs-lookup"><span data-stu-id="ffa51-118">-AllowAll</span></span>
<span data-ttu-id="ffa51-119">Presente para permitir todos os IPs de intervalo, de 0,0.0.0 a 255.255.255.255.</span><span class="sxs-lookup"><span data-stu-id="ffa51-119">Present to allow all range IPs, from 0.0.0.0 to 255.255.255.255.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AllowAll
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffa51-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ffa51-120">-AsJob</span></span>
<span data-ttu-id="ffa51-121">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="ffa51-121">Run the command as a job</span></span>

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

### <span data-ttu-id="ffa51-122">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="ffa51-122">-ClientIPAddress</span></span>
<span data-ttu-id="ffa51-123">IP único especificado pelo cliente da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="ffa51-123">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="ffa51-124">Deve ser formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="ffa51-124">Must be IPv4 format.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientIPAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffa51-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffa51-125">-DefaultProfile</span></span>
<span data-ttu-id="ffa51-126">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ffa51-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ffa51-127">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="ffa51-127">-EndIPAddress</span></span>
<span data-ttu-id="ffa51-128">O endereço IP final da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="ffa51-128">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="ffa51-129">Deve ser formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="ffa51-129">Must be IPv4 format.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffa51-130">-Name</span><span class="sxs-lookup"><span data-stu-id="ffa51-130">-Name</span></span>
<span data-ttu-id="ffa51-131">O nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="ffa51-131">The name of the server firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: FirewallRuleName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffa51-132">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ffa51-132">-NoWait</span></span>
<span data-ttu-id="ffa51-133">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="ffa51-133">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ffa51-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ffa51-134">-ResourceGroupName</span></span>
<span data-ttu-id="ffa51-135">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ffa51-135">The name of the resource group.</span></span>
<span data-ttu-id="ffa51-136">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="ffa51-136">The name is case insensitive.</span></span>

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

### <span data-ttu-id="ffa51-137">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ffa51-137">-ServerName</span></span>
<span data-ttu-id="ffa51-138">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="ffa51-138">The name of the server.</span></span>

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

### <span data-ttu-id="ffa51-139">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="ffa51-139">-StartIPAddress</span></span>
<span data-ttu-id="ffa51-140">O endereço IP inicial da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="ffa51-140">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="ffa51-141">Deve ser formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="ffa51-141">Must be IPv4 format.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffa51-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ffa51-142">-SubscriptionId</span></span>
<span data-ttu-id="ffa51-143">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="ffa51-143">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="ffa51-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ffa51-144">-Confirm</span></span>
<span data-ttu-id="ffa51-145">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ffa51-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ffa51-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ffa51-146">-WhatIf</span></span>
<span data-ttu-id="ffa51-147">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ffa51-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ffa51-148">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ffa51-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ffa51-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffa51-149">CommonParameters</span></span>
<span data-ttu-id="ffa51-150">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ffa51-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffa51-151">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ffa51-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffa51-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ffa51-152">INPUTS</span></span>

## <span data-ttu-id="ffa51-153">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ffa51-153">OUTPUTS</span></span>

### <span data-ttu-id="ffa51-154">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ffa51-154">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="ffa51-155">NOTES</span><span class="sxs-lookup"><span data-stu-id="ffa51-155">NOTES</span></span>

<span data-ttu-id="ffa51-156">ALIASES</span><span class="sxs-lookup"><span data-stu-id="ffa51-156">ALIASES</span></span>

## <span data-ttu-id="ffa51-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ffa51-157">RELATED LINKS</span></span>

