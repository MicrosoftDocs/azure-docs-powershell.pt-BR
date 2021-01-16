---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/new-azpostgresqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlFirewallRule.md
ms.openlocfilehash: bafd0e20530198da87c1fa3ece36905e73307a42
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98262456"
---
# <span data-ttu-id="a810b-101">New-AzPostgreSqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="a810b-101">New-AzPostgreSqlFirewallRule</span></span>

## <span data-ttu-id="a810b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a810b-102">SYNOPSIS</span></span>
<span data-ttu-id="a810b-103">Cria uma nova regra de firewall ou atualiza uma regra de firewall existente.</span><span class="sxs-lookup"><span data-stu-id="a810b-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="a810b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a810b-104">SYNTAX</span></span>

### <span data-ttu-id="a810b-105">Createexpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="a810b-105">CreateExpanded (Default)</span></span>
```
New-AzPostgreSqlFirewallRule -ResourceGroupName <String> -ServerName <String> -EndIPAddress <String>
 -StartIPAddress <String> [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a810b-106">AllowAll</span><span class="sxs-lookup"><span data-stu-id="a810b-106">AllowAll</span></span>
```
New-AzPostgreSqlFirewallRule -ResourceGroupName <String> -ServerName <String> -AllowAll [-Name <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="a810b-107">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="a810b-107">ClientIPAddress</span></span>
```
New-AzPostgreSqlFirewallRule -ResourceGroupName <String> -ServerName <String> -ClientIPAddress <String>
 [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a810b-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a810b-108">DESCRIPTION</span></span>
<span data-ttu-id="a810b-109">Cria uma nova regra de firewall ou atualiza uma regra de firewall existente.</span><span class="sxs-lookup"><span data-stu-id="a810b-109">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="a810b-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a810b-110">EXAMPLES</span></span>

### <span data-ttu-id="a810b-111">Exemplo 1: criar uma nova regra de firewall do servidor PostgreSql</span><span class="sxs-lookup"><span data-stu-id="a810b-111">Example 1: Create a new PostgreSql server Firewall Rule</span></span>
```powershell
PS C:\> New-AzPostgreSqlFirewallRule -Name rule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -EndIPAddress 0.0.0.1 -StartIPAddress 0.0.0.0

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="a810b-112">Estes cmdlets criam uma regra de firewall do servidor PostgreSql.</span><span class="sxs-lookup"><span data-stu-id="a810b-112">This cmdlets create a PostgreSql server Firewall Rule.</span></span>

### <span data-ttu-id="a810b-113">Exemplo 2: criar uma nova regra de firewall do PostgreSql usando-ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="a810b-113">Example 2: Create a new PostgreSql Firewall Rule using -ClientIPAddress.</span></span>
```powershell
PS C:\> New-AzPostgreSqlFirewallRule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -ClientIPAddress 0.0.0.1

Name                                StartIPAddress EndIPAddress
----                                -------------- ------------
ClientIPAddress_2020-08-11_18-19-27 0.0.0.1        0.0.0.1
```

<span data-ttu-id="a810b-114">Estes cmdlets criam uma regra de firewall do PostgreSql usando-ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="a810b-114">This cmdlets create a PostgreSql Firewall Rule using -ClientIPAddress.</span></span>

### <span data-ttu-id="a810b-115">Exemplo 3: criar uma nova regra de firewall do PostgreSql para permitir todos os IPs</span><span class="sxs-lookup"><span data-stu-id="a810b-115">Example 3: Create a new PostgreSql Firewall Rule to allow all IPs</span></span>
```powershell
PS C:\> New-AzPostgreSqlFirewallRule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -AllowAll

Name                         StartIPAddress EndIPAddress
----                         -------------- ------------
AllowAll_2020-08-11_18-19-27 0.0.0.0        255.255.255.255
```

<span data-ttu-id="a810b-116">Esses cmdlets criam uma nova regra de firewall do PostgreSql para permitir todos os IPs.</span><span class="sxs-lookup"><span data-stu-id="a810b-116">This cmdlets create a new PostgreSql Firewall Rule to allow all IPs.</span></span>

## <span data-ttu-id="a810b-117">OS</span><span class="sxs-lookup"><span data-stu-id="a810b-117">PARAMETERS</span></span>

### <span data-ttu-id="a810b-118">-AllowAll</span><span class="sxs-lookup"><span data-stu-id="a810b-118">-AllowAll</span></span>
<span data-ttu-id="a810b-119">Apresentar para permitir todos os IPs de intervalo, de 0.0.0.0 a 255.255.255.255.</span><span class="sxs-lookup"><span data-stu-id="a810b-119">Present to allow all range IPs, from 0.0.0.0 to 255.255.255.255.</span></span>

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

### <span data-ttu-id="a810b-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a810b-120">-AsJob</span></span>
<span data-ttu-id="a810b-121">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="a810b-121">Run the command as a job</span></span>

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

### <span data-ttu-id="a810b-122">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="a810b-122">-ClientIPAddress</span></span>
<span data-ttu-id="a810b-123">Único IP especificado pelo cliente da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="a810b-123">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="a810b-124">Deve ser o formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="a810b-124">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="a810b-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a810b-125">-DefaultProfile</span></span>
<span data-ttu-id="a810b-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a810b-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a810b-127">-Endipaddress</span><span class="sxs-lookup"><span data-stu-id="a810b-127">-EndIPAddress</span></span>
<span data-ttu-id="a810b-128">O endereço IP final da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="a810b-128">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="a810b-129">Deve ser o formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="a810b-129">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="a810b-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="a810b-130">-Name</span></span>
<span data-ttu-id="a810b-131">O nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="a810b-131">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="a810b-132">-Nowait</span><span class="sxs-lookup"><span data-stu-id="a810b-132">-NoWait</span></span>
<span data-ttu-id="a810b-133">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="a810b-133">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a810b-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a810b-134">-ResourceGroupName</span></span>
<span data-ttu-id="a810b-135">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a810b-135">The name of the resource group.</span></span>
<span data-ttu-id="a810b-136">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="a810b-136">The name is case insensitive.</span></span>

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

### <span data-ttu-id="a810b-137">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="a810b-137">-ServerName</span></span>
<span data-ttu-id="a810b-138">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="a810b-138">The name of the server.</span></span>

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

### <span data-ttu-id="a810b-139">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="a810b-139">-StartIPAddress</span></span>
<span data-ttu-id="a810b-140">O endereço IP inicial da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="a810b-140">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="a810b-141">Deve ser o formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="a810b-141">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="a810b-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a810b-142">-SubscriptionId</span></span>
<span data-ttu-id="a810b-143">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="a810b-143">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="a810b-144">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a810b-144">-Confirm</span></span>
<span data-ttu-id="a810b-145">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a810b-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a810b-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a810b-146">-WhatIf</span></span>
<span data-ttu-id="a810b-147">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a810b-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a810b-148">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a810b-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a810b-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a810b-149">CommonParameters</span></span>
<span data-ttu-id="a810b-150">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a810b-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a810b-151">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a810b-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a810b-152">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a810b-152">INPUTS</span></span>

## <span data-ttu-id="a810b-153">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a810b-153">OUTPUTS</span></span>

### <span data-ttu-id="a810b-154">Microsoft. Azure. PowerShell. cmdlets. PostgreSql. Models. Api20171201. IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="a810b-154">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="a810b-155">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a810b-155">NOTES</span></span>

<span data-ttu-id="a810b-156">ALIASES</span><span class="sxs-lookup"><span data-stu-id="a810b-156">ALIASES</span></span>

## <span data-ttu-id="a810b-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a810b-157">RELATED LINKS</span></span>

