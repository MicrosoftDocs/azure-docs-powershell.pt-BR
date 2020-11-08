---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/new-azmariadbfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbFirewallRule.md
ms.openlocfilehash: 00da9023a7ed6607993af3faadccfbddbb784526
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94126040"
---
# <span data-ttu-id="aabc8-101">New-AzMariaDbFirewallRule</span><span class="sxs-lookup"><span data-stu-id="aabc8-101">New-AzMariaDbFirewallRule</span></span>

## <span data-ttu-id="aabc8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="aabc8-102">SYNOPSIS</span></span>
<span data-ttu-id="aabc8-103">Cria uma nova regra de firewall ou atualiza uma regra de firewall existente.</span><span class="sxs-lookup"><span data-stu-id="aabc8-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="aabc8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="aabc8-104">SYNTAX</span></span>

### <span data-ttu-id="aabc8-105">Createexpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="aabc8-105">CreateExpanded (Default)</span></span>
```
New-AzMariaDbFirewallRule -ResourceGroupName <String> -ServerName <String> -EndIPAddress <String>
 -StartIPAddress <String> [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="aabc8-106">AllowAll</span><span class="sxs-lookup"><span data-stu-id="aabc8-106">AllowAll</span></span>
```
New-AzMariaDbFirewallRule -ResourceGroupName <String> -ServerName <String> -AllowAll [-Name <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="aabc8-107">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="aabc8-107">ClientIPAddress</span></span>
```
New-AzMariaDbFirewallRule -ResourceGroupName <String> -ServerName <String> -ClientIPAddress <String>
 [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="aabc8-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="aabc8-108">DESCRIPTION</span></span>
<span data-ttu-id="aabc8-109">Cria uma nova regra de firewall ou atualiza uma regra de firewall existente.</span><span class="sxs-lookup"><span data-stu-id="aabc8-109">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="aabc8-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="aabc8-110">EXAMPLES</span></span>

### <span data-ttu-id="aabc8-111">Exemplo 1: criar uma regra de firewall em um MariaDB</span><span class="sxs-lookup"><span data-stu-id="aabc8-111">Example 1: Create a firewall rule under a MariaDB</span></span>
```powershell
PS C:\> New-AzMariaDbFirewallRule -Name firewall-101 -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-asd-01 -EndIPAddress 0.0.2.255 -StartIPAddress 0.0.2.1

Name         StartIPAddress EndIPAddress
----         -------------- ------------
firewall-101 0.0.2.1        0.0.2.255
```

<span data-ttu-id="aabc8-112">Esse comando cria uma regra de firewall em um MariaDB.</span><span class="sxs-lookup"><span data-stu-id="aabc8-112">This command creates a firewall rule under a MariaDB.</span></span>

### <span data-ttu-id="aabc8-113">Exemplo 2: criar uma nova regra de firewall MariaDB usando-ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="aabc8-113">Example 2: Create a new MariaDB Firewall Rule using -ClientIPAddress.</span></span>
```powershell
PS C:\> New-AzMariaDbFirewallRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-asd-01 -ClientIPAddress 0.0.0.1

Name                                StartIPAddress EndIPAddress
----                                -------------- ------------
ClientIPAddress_2020-08-11_18-19-27 0.0.0.1        0.0.0.1
```

<span data-ttu-id="aabc8-114">Esses cmdlets criam uma regra de firewall MariaDB usando-ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="aabc8-114">This cmdlets create a MariaDB Firewall Rule using -ClientIPAddress.</span></span>

### <span data-ttu-id="aabc8-115">Exemplo 3: criar uma nova regra de firewall MariaDB para permitir todos os IPs</span><span class="sxs-lookup"><span data-stu-id="aabc8-115">Example 3: Create a new MariaDB Firewall Rule to allow all IPs</span></span>
```powershell
PS C:\> New-AzMariaDbFirewallRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-asd-01 -AllowAll

Name                         StartIPAddress EndIPAddress
----                         -------------- ------------
AllowAll_2020-08-11_18-19-27 0.0.0.0        255.255.255.255
```

<span data-ttu-id="aabc8-116">Esses cmdlets criam uma nova regra de firewall MariaDB para permitir que todos os IPs.</span><span class="sxs-lookup"><span data-stu-id="aabc8-116">This cmdlets create a new MariaDB Firewall Rule to allow all IPs.</span></span>

## <span data-ttu-id="aabc8-117">OS</span><span class="sxs-lookup"><span data-stu-id="aabc8-117">PARAMETERS</span></span>

### <span data-ttu-id="aabc8-118">-AllowAll</span><span class="sxs-lookup"><span data-stu-id="aabc8-118">-AllowAll</span></span>
<span data-ttu-id="aabc8-119">Apresentar para permitir todos os IPs de intervalo, de 0.0.0.0 a 255.255.255.255.</span><span class="sxs-lookup"><span data-stu-id="aabc8-119">Present to allow all range IPs, from 0.0.0.0 to 255.255.255.255.</span></span>

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

### <span data-ttu-id="aabc8-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aabc8-120">-AsJob</span></span>
<span data-ttu-id="aabc8-121">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="aabc8-121">Run the command as a job</span></span>

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

### <span data-ttu-id="aabc8-122">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="aabc8-122">-ClientIPAddress</span></span>
<span data-ttu-id="aabc8-123">Único IP especificado pelo cliente da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="aabc8-123">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="aabc8-124">Deve ser o formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="aabc8-124">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="aabc8-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aabc8-125">-DefaultProfile</span></span>
<span data-ttu-id="aabc8-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="aabc8-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aabc8-127">-Endipaddress</span><span class="sxs-lookup"><span data-stu-id="aabc8-127">-EndIPAddress</span></span>
<span data-ttu-id="aabc8-128">O endereço IP final da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="aabc8-128">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="aabc8-129">Deve ser o formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="aabc8-129">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="aabc8-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="aabc8-130">-Name</span></span>
<span data-ttu-id="aabc8-131">O nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="aabc8-131">The name of the server firewall rule.</span></span>
<span data-ttu-id="aabc8-132">Se não for especificado, o padrão será indefinido.</span><span class="sxs-lookup"><span data-stu-id="aabc8-132">If not specified, the default is undefined.</span></span>
<span data-ttu-id="aabc8-133">Se AllowAll estiver presente, o nome padrão será AllowAll_yyyy-MM-dd_HH-mm-SS.</span><span class="sxs-lookup"><span data-stu-id="aabc8-133">If AllowAll is present, the default name is AllowAll_yyyy-MM-dd_HH-mm-ss.</span></span>

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

### <span data-ttu-id="aabc8-134">-Nowait</span><span class="sxs-lookup"><span data-stu-id="aabc8-134">-NoWait</span></span>
<span data-ttu-id="aabc8-135">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="aabc8-135">Run the command asynchronously</span></span>

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

### <span data-ttu-id="aabc8-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aabc8-136">-ResourceGroupName</span></span>
<span data-ttu-id="aabc8-137">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="aabc8-137">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="aabc8-138">Você pode obter esse valor da API do Azure Resource Manager ou do Portal.</span><span class="sxs-lookup"><span data-stu-id="aabc8-138">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="aabc8-139">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="aabc8-139">-ServerName</span></span>
<span data-ttu-id="aabc8-140">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="aabc8-140">The name of the server.</span></span>

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

### <span data-ttu-id="aabc8-141">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="aabc8-141">-StartIPAddress</span></span>
<span data-ttu-id="aabc8-142">O endereço IP inicial da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="aabc8-142">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="aabc8-143">Deve ser o formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="aabc8-143">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="aabc8-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="aabc8-144">-SubscriptionId</span></span>
<span data-ttu-id="aabc8-145">A ID da assinatura que identifica uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="aabc8-145">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="aabc8-146">-Confirme</span><span class="sxs-lookup"><span data-stu-id="aabc8-146">-Confirm</span></span>
<span data-ttu-id="aabc8-147">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aabc8-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aabc8-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aabc8-148">-WhatIf</span></span>
<span data-ttu-id="aabc8-149">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="aabc8-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aabc8-150">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="aabc8-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aabc8-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aabc8-151">CommonParameters</span></span>
<span data-ttu-id="aabc8-152">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aabc8-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aabc8-153">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aabc8-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aabc8-154">SENSORES</span><span class="sxs-lookup"><span data-stu-id="aabc8-154">INPUTS</span></span>

## <span data-ttu-id="aabc8-155">EXIBE</span><span class="sxs-lookup"><span data-stu-id="aabc8-155">OUTPUTS</span></span>

### <span data-ttu-id="aabc8-156">Microsoft. Azure. PowerShell. cmdlets. MariaDb. Models. Api20180601Preview. IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="aabc8-156">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IFirewallRule</span></span>

## <span data-ttu-id="aabc8-157">INFORMA</span><span class="sxs-lookup"><span data-stu-id="aabc8-157">NOTES</span></span>

<span data-ttu-id="aabc8-158">ALIASES</span><span class="sxs-lookup"><span data-stu-id="aabc8-158">ALIASES</span></span>

## <span data-ttu-id="aabc8-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="aabc8-159">RELATED LINKS</span></span>

