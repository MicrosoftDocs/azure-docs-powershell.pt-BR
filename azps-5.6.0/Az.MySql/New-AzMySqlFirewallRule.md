---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/new-azmysqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFirewallRule.md
ms.openlocfilehash: 84c5e5e49d80c04bcbfe3f7ec72e018ac7984bec
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886219"
---
# <span data-ttu-id="6e6ff-101">New-AzMySqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="6e6ff-101">New-AzMySqlFirewallRule</span></span>

## <span data-ttu-id="6e6ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e6ff-102">SYNOPSIS</span></span>
<span data-ttu-id="6e6ff-103">Cria uma nova regra de firewall ou atualiza uma regra de firewall existente.</span><span class="sxs-lookup"><span data-stu-id="6e6ff-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="6e6ff-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="6e6ff-104">SYNTAX</span></span>

### <span data-ttu-id="6e6ff-105">CreateExpanded (Default)</span><span class="sxs-lookup"><span data-stu-id="6e6ff-105">CreateExpanded (Default)</span></span>
```
New-AzMySqlFirewallRule -ResourceGroupName <String> -ServerName <String> -EndIPAddress <String>
 -StartIPAddress <String> [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6e6ff-106">AllowAll</span><span class="sxs-lookup"><span data-stu-id="6e6ff-106">AllowAll</span></span>
```
New-AzMySqlFirewallRule -ResourceGroupName <String> -ServerName <String> -AllowAll [-Name <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="6e6ff-107">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="6e6ff-107">ClientIPAddress</span></span>
```
New-AzMySqlFirewallRule -ResourceGroupName <String> -ServerName <String> -ClientIPAddress <String>
 [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6e6ff-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="6e6ff-108">DESCRIPTION</span></span>
<span data-ttu-id="6e6ff-109">Cria uma nova regra de firewall ou atualiza uma regra de firewall existente.</span><span class="sxs-lookup"><span data-stu-id="6e6ff-109">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="6e6ff-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6e6ff-110">EXAMPLES</span></span>

### <span data-ttu-id="6e6ff-111">Exemplo 1: Criar uma nova Regra de Firewall do servidor MySql</span><span class="sxs-lookup"><span data-stu-id="6e6ff-111">Example 1: Create a new MySql server Firewall Rule</span></span>
```powershell
PS C:\> New-AzMySqlFirewallRule -Name rule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -EndIPAddress 0.0.0.1 -StartIPAddress 0.0.0.0

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="6e6ff-112">Este cmdlets criam uma Regra de Firewall do servidor MySql.</span><span class="sxs-lookup"><span data-stu-id="6e6ff-112">This cmdlets create a MySql server Firewall Rule.</span></span>

### <span data-ttu-id="6e6ff-113">Exemplo 2: Criar uma nova Regra de Firewall MySql usando -ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="6e6ff-113">Example 2: Create a new MySql Firewall Rule using -ClientIPAddress.</span></span>
```powershell
PS C:\> New-AzMySqlFirewallRule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -ClientIPAddress 0.0.0.1

Name                                StartIPAddress EndIPAddress
----                                -------------- ------------
ClientIPAddress_2020-08-11_18-19-27 0.0.0.1        0.0.0.1
```

<span data-ttu-id="6e6ff-114">Este cmdlets criam uma Regra de Firewall MySql usando -ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="6e6ff-114">This cmdlets create a MySql Firewall Rule using -ClientIPAddress.</span></span>

### <span data-ttu-id="6e6ff-115">Exemplo 3: Criar uma nova Regra de Firewall MySql para permitir todos os IPs</span><span class="sxs-lookup"><span data-stu-id="6e6ff-115">Example 3: Create a new MySql Firewall Rule to allow all IPs</span></span>
```powershell
PS C:\> New-AzMySqlFirewallRule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -AllowAll

Name                         StartIPAddress EndIPAddress
----                         -------------- ------------
AllowAll_2020-08-11_18-19-27 0.0.0.0        255.255.255.255
```

<span data-ttu-id="6e6ff-116">Esses cmdlets criam uma nova Regra de Firewall MySql para permitir todos os IPs.</span><span class="sxs-lookup"><span data-stu-id="6e6ff-116">This cmdlets create a new MySql Firewall Rule to allow all IPs.</span></span>

## <span data-ttu-id="6e6ff-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="6e6ff-117">PARAMETERS</span></span>

### <span data-ttu-id="6e6ff-118">-AllowAll</span><span class="sxs-lookup"><span data-stu-id="6e6ff-118">-AllowAll</span></span>
<span data-ttu-id="6e6ff-119">Presente para permitir todos os IPs de intervalo, de 0,0.0.0 a 255.255.255.255.</span><span class="sxs-lookup"><span data-stu-id="6e6ff-119">Present to allow all range IPs, from 0.0.0.0 to 255.255.255.255.</span></span>

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

### <span data-ttu-id="6e6ff-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6e6ff-120">-AsJob</span></span>
<span data-ttu-id="6e6ff-121">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="6e6ff-121">Run the command as a job</span></span>

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

### <span data-ttu-id="6e6ff-122">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="6e6ff-122">-ClientIPAddress</span></span>
<span data-ttu-id="6e6ff-123">IP único especificado pelo cliente da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="6e6ff-123">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="6e6ff-124">Deve ser formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="6e6ff-124">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="6e6ff-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e6ff-125">-DefaultProfile</span></span>
<span data-ttu-id="6e6ff-126">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6e6ff-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e6ff-127">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="6e6ff-127">-EndIPAddress</span></span>
<span data-ttu-id="6e6ff-128">O endereço IP final da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="6e6ff-128">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="6e6ff-129">Deve ser formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="6e6ff-129">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="6e6ff-130">-Name</span><span class="sxs-lookup"><span data-stu-id="6e6ff-130">-Name</span></span>
<span data-ttu-id="6e6ff-131">O nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="6e6ff-131">The name of the server firewall rule.</span></span>
<span data-ttu-id="6e6ff-132">Se não for especificado, o padrão será indefinido.</span><span class="sxs-lookup"><span data-stu-id="6e6ff-132">If not specified, the default is undefined.</span></span>
<span data-ttu-id="6e6ff-133">Se AllowAll estiver presente, o nome padrão será AllowAll_yyyy-MM-dd_HH-mm-ss.</span><span class="sxs-lookup"><span data-stu-id="6e6ff-133">If AllowAll is present, the default name is AllowAll_yyyy-MM-dd_HH-mm-ss.</span></span>

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

### <span data-ttu-id="6e6ff-134">-NoWait</span><span class="sxs-lookup"><span data-stu-id="6e6ff-134">-NoWait</span></span>
<span data-ttu-id="6e6ff-135">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="6e6ff-135">Run the command asynchronously</span></span>

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

### <span data-ttu-id="6e6ff-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e6ff-136">-ResourceGroupName</span></span>
<span data-ttu-id="6e6ff-137">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6e6ff-137">The name of the resource group.</span></span>
<span data-ttu-id="6e6ff-138">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="6e6ff-138">The name is case insensitive.</span></span>

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

### <span data-ttu-id="6e6ff-139">-ServerName</span><span class="sxs-lookup"><span data-stu-id="6e6ff-139">-ServerName</span></span>
<span data-ttu-id="6e6ff-140">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="6e6ff-140">The name of the server.</span></span>

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

### <span data-ttu-id="6e6ff-141">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="6e6ff-141">-StartIPAddress</span></span>
<span data-ttu-id="6e6ff-142">O endereço IP inicial da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="6e6ff-142">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="6e6ff-143">Deve ser formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="6e6ff-143">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="6e6ff-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6e6ff-144">-SubscriptionId</span></span>
<span data-ttu-id="6e6ff-145">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="6e6ff-145">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="6e6ff-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6e6ff-146">-Confirm</span></span>
<span data-ttu-id="6e6ff-147">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6e6ff-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e6ff-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e6ff-148">-WhatIf</span></span>
<span data-ttu-id="6e6ff-149">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6e6ff-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e6ff-150">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6e6ff-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e6ff-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e6ff-151">CommonParameters</span></span>
<span data-ttu-id="6e6ff-152">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e6ff-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e6ff-153">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6e6ff-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e6ff-154">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6e6ff-154">INPUTS</span></span>

## <span data-ttu-id="6e6ff-155">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="6e6ff-155">OUTPUTS</span></span>

### <span data-ttu-id="6e6ff-156">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="6e6ff-156">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="6e6ff-157">NOTES</span><span class="sxs-lookup"><span data-stu-id="6e6ff-157">NOTES</span></span>

<span data-ttu-id="6e6ff-158">ALIASES</span><span class="sxs-lookup"><span data-stu-id="6e6ff-158">ALIASES</span></span>

## <span data-ttu-id="6e6ff-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6e6ff-159">RELATED LINKS</span></span>

