---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/new-azmysqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFirewallRule.md
ms.openlocfilehash: 67ef03656b97514d1d39ae72f0f0d52d5b302619
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98258768"
---
# <span data-ttu-id="707f3-101">New-AzMySqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="707f3-101">New-AzMySqlFirewallRule</span></span>

## <span data-ttu-id="707f3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="707f3-102">SYNOPSIS</span></span>
<span data-ttu-id="707f3-103">Cria uma nova regra de firewall ou atualiza uma regra de firewall existente.</span><span class="sxs-lookup"><span data-stu-id="707f3-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="707f3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="707f3-104">SYNTAX</span></span>

### <span data-ttu-id="707f3-105">Createexpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="707f3-105">CreateExpanded (Default)</span></span>
```
New-AzMySqlFirewallRule -ResourceGroupName <String> -ServerName <String> -EndIPAddress <String>
 -StartIPAddress <String> [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="707f3-106">AllowAll</span><span class="sxs-lookup"><span data-stu-id="707f3-106">AllowAll</span></span>
```
New-AzMySqlFirewallRule -ResourceGroupName <String> -ServerName <String> -AllowAll [-Name <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="707f3-107">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="707f3-107">ClientIPAddress</span></span>
```
New-AzMySqlFirewallRule -ResourceGroupName <String> -ServerName <String> -ClientIPAddress <String>
 [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="707f3-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="707f3-108">DESCRIPTION</span></span>
<span data-ttu-id="707f3-109">Cria uma nova regra de firewall ou atualiza uma regra de firewall existente.</span><span class="sxs-lookup"><span data-stu-id="707f3-109">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="707f3-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="707f3-110">EXAMPLES</span></span>

### <span data-ttu-id="707f3-111">Exemplo 1: criar uma nova regra de firewall do servidor MySql</span><span class="sxs-lookup"><span data-stu-id="707f3-111">Example 1: Create a new MySql server Firewall Rule</span></span>
```powershell
PS C:\> New-AzMySqlFirewallRule -Name rule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -EndIPAddress 0.0.0.1 -StartIPAddress 0.0.0.0

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="707f3-112">Estes cmdlets criam uma regra de firewall do servidor MySql.</span><span class="sxs-lookup"><span data-stu-id="707f3-112">This cmdlets create a MySql server Firewall Rule.</span></span>

### <span data-ttu-id="707f3-113">Exemplo 2: criar uma nova regra de firewall do MySql usando-ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="707f3-113">Example 2: Create a new MySql Firewall Rule using -ClientIPAddress.</span></span>
```powershell
PS C:\> New-AzMySqlFirewallRule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -ClientIPAddress 0.0.0.1

Name                                StartIPAddress EndIPAddress
----                                -------------- ------------
ClientIPAddress_2020-08-11_18-19-27 0.0.0.1        0.0.0.1
```

<span data-ttu-id="707f3-114">Estes cmdlets criam uma regra de firewall MySql usando-ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="707f3-114">This cmdlets create a MySql Firewall Rule using -ClientIPAddress.</span></span>

### <span data-ttu-id="707f3-115">Exemplo 3: criar uma nova regra de firewall MySql para permitir todos os IPs</span><span class="sxs-lookup"><span data-stu-id="707f3-115">Example 3: Create a new MySql Firewall Rule to allow all IPs</span></span>
```powershell
PS C:\> New-AzMySqlFirewallRule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -AllowAll

Name                         StartIPAddress EndIPAddress
----                         -------------- ------------
AllowAll_2020-08-11_18-19-27 0.0.0.0        255.255.255.255
```

<span data-ttu-id="707f3-116">Esses cmdlets criam uma nova regra de firewall MySql para permitir todos os IPs.</span><span class="sxs-lookup"><span data-stu-id="707f3-116">This cmdlets create a new MySql Firewall Rule to allow all IPs.</span></span>

## <span data-ttu-id="707f3-117">OS</span><span class="sxs-lookup"><span data-stu-id="707f3-117">PARAMETERS</span></span>

### <span data-ttu-id="707f3-118">-AllowAll</span><span class="sxs-lookup"><span data-stu-id="707f3-118">-AllowAll</span></span>
<span data-ttu-id="707f3-119">Apresentar para permitir todos os IPs de intervalo, de 0.0.0.0 a 255.255.255.255.</span><span class="sxs-lookup"><span data-stu-id="707f3-119">Present to allow all range IPs, from 0.0.0.0 to 255.255.255.255.</span></span>

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

### <span data-ttu-id="707f3-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="707f3-120">-AsJob</span></span>
<span data-ttu-id="707f3-121">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="707f3-121">Run the command as a job</span></span>

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

### <span data-ttu-id="707f3-122">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="707f3-122">-ClientIPAddress</span></span>
<span data-ttu-id="707f3-123">Único IP especificado pelo cliente da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="707f3-123">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="707f3-124">Deve ser o formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="707f3-124">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="707f3-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="707f3-125">-DefaultProfile</span></span>
<span data-ttu-id="707f3-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="707f3-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="707f3-127">-Endipaddress</span><span class="sxs-lookup"><span data-stu-id="707f3-127">-EndIPAddress</span></span>
<span data-ttu-id="707f3-128">O endereço IP final da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="707f3-128">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="707f3-129">Deve ser o formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="707f3-129">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="707f3-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="707f3-130">-Name</span></span>
<span data-ttu-id="707f3-131">O nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="707f3-131">The name of the server firewall rule.</span></span>
<span data-ttu-id="707f3-132">Se não for especificado, o padrão será indefinido.</span><span class="sxs-lookup"><span data-stu-id="707f3-132">If not specified, the default is undefined.</span></span>
<span data-ttu-id="707f3-133">Se AllowAll estiver presente, o nome padrão será AllowAll_yyyy-MM-dd_HH-mm-SS.</span><span class="sxs-lookup"><span data-stu-id="707f3-133">If AllowAll is present, the default name is AllowAll_yyyy-MM-dd_HH-mm-ss.</span></span>

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

### <span data-ttu-id="707f3-134">-Nowait</span><span class="sxs-lookup"><span data-stu-id="707f3-134">-NoWait</span></span>
<span data-ttu-id="707f3-135">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="707f3-135">Run the command asynchronously</span></span>

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

### <span data-ttu-id="707f3-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="707f3-136">-ResourceGroupName</span></span>
<span data-ttu-id="707f3-137">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="707f3-137">The name of the resource group.</span></span>
<span data-ttu-id="707f3-138">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="707f3-138">The name is case insensitive.</span></span>

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

### <span data-ttu-id="707f3-139">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="707f3-139">-ServerName</span></span>
<span data-ttu-id="707f3-140">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="707f3-140">The name of the server.</span></span>

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

### <span data-ttu-id="707f3-141">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="707f3-141">-StartIPAddress</span></span>
<span data-ttu-id="707f3-142">O endereço IP inicial da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="707f3-142">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="707f3-143">Deve ser o formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="707f3-143">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="707f3-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="707f3-144">-SubscriptionId</span></span>
<span data-ttu-id="707f3-145">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="707f3-145">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="707f3-146">-Confirme</span><span class="sxs-lookup"><span data-stu-id="707f3-146">-Confirm</span></span>
<span data-ttu-id="707f3-147">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="707f3-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="707f3-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="707f3-148">-WhatIf</span></span>
<span data-ttu-id="707f3-149">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="707f3-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="707f3-150">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="707f3-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="707f3-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="707f3-151">CommonParameters</span></span>
<span data-ttu-id="707f3-152">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="707f3-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="707f3-153">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="707f3-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="707f3-154">SENSORES</span><span class="sxs-lookup"><span data-stu-id="707f3-154">INPUTS</span></span>

## <span data-ttu-id="707f3-155">EXIBE</span><span class="sxs-lookup"><span data-stu-id="707f3-155">OUTPUTS</span></span>

### <span data-ttu-id="707f3-156">Microsoft. Azure. PowerShell. cmdlets. MySql. Models. Api20171201. IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="707f3-156">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="707f3-157">INFORMA</span><span class="sxs-lookup"><span data-stu-id="707f3-157">NOTES</span></span>

<span data-ttu-id="707f3-158">ALIASES</span><span class="sxs-lookup"><span data-stu-id="707f3-158">ALIASES</span></span>

## <span data-ttu-id="707f3-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="707f3-159">RELATED LINKS</span></span>

