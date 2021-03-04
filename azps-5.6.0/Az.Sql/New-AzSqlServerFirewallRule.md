---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 51AF8EFB-F0C1-41E0-BBC5-E48FB1B8672C
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerFirewallRule.md
ms.openlocfilehash: 07179b5fb139ba43b341114e2bf597fbbca05ed5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885786"
---
# <span data-ttu-id="87b33-101">New-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="87b33-101">New-AzSqlServerFirewallRule</span></span>

## <span data-ttu-id="87b33-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87b33-102">SYNOPSIS</span></span>
<span data-ttu-id="87b33-103">Cria uma regra de firewall para um servidor SQL Banco de Dados.</span><span class="sxs-lookup"><span data-stu-id="87b33-103">Creates a firewall rule for a SQL Database server.</span></span>

## <span data-ttu-id="87b33-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="87b33-104">SYNTAX</span></span>

### <span data-ttu-id="87b33-105">UserSpecifiedRuleSet</span><span class="sxs-lookup"><span data-stu-id="87b33-105">UserSpecifiedRuleSet</span></span>
```
New-AzSqlServerFirewallRule -FirewallRuleName <String> -StartIpAddress <String> -EndIpAddress <String>
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87b33-106">AzureIpRuleSet</span><span class="sxs-lookup"><span data-stu-id="87b33-106">AzureIpRuleSet</span></span>
```
New-AzSqlServerFirewallRule [-AllowAllAzureIPs] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87b33-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="87b33-107">DESCRIPTION</span></span>
<span data-ttu-id="87b33-108">O cmdlet **New-AzSqlServerFirewallRule** cria uma regra de firewall para o servidor de banco de dados SQL Azure especificado.</span><span class="sxs-lookup"><span data-stu-id="87b33-108">The **New-AzSqlServerFirewallRule** cmdlet creates a firewall rule for the specified Azure SQL Database server.</span></span>

## <span data-ttu-id="87b33-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="87b33-109">EXAMPLES</span></span>

### <span data-ttu-id="87b33-110">Exemplo 1: Criar uma regra de firewall</span><span class="sxs-lookup"><span data-stu-id="87b33-110">Example 1: Create a firewall rule</span></span>
```
PS C:\>New-AzSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -FirewallRuleName "Rule01" -StartIpAddress "192.168.0.198" -EndIpAddress "192.168.0.199"
ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 192.168.0.198
EndIpAddress      : 192.168.0.199
FirewallRuleName  : Rule01
```

<span data-ttu-id="87b33-111">Este comando cria uma regra de firewall chamada Rule01 no servidor chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="87b33-111">This command creates a firewall rule named Rule01 on the server named Server01.</span></span>
<span data-ttu-id="87b33-112">A regra inclui os endereços IP inicial e final especificados.</span><span class="sxs-lookup"><span data-stu-id="87b33-112">The rule includes the specified start and end IP addresses.</span></span>

### <span data-ttu-id="87b33-113">Exemplo 2: Criar uma regra de firewall que permita que todos os endereços IP do Azure acessem o servidor</span><span class="sxs-lookup"><span data-stu-id="87b33-113">Example 2: Create a firewall rule that allows all Azure IP addresses to access the server</span></span>
```
PS C:\>New-AzSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -AllowAllAzureIPs
```

<span data-ttu-id="87b33-114">Este comando cria uma regra de firewall no servidor chamado Server01 que pertence ao grupo de recursos chamado ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="87b33-114">This command creates a firewall rule on the server named Server01 that belongs to the resource group named ResourceGroup01.</span></span>
<span data-ttu-id="87b33-115">Como o *parâmetro AllowAllAzureIPs* é usado, a regra de firewall permite que todos os endereços IP do Azure acessem o servidor.</span><span class="sxs-lookup"><span data-stu-id="87b33-115">Since the *AllowAllAzureIPs* parameter is used, the firewall rule allows all Azure IP addresses to access the server.</span></span>

## <span data-ttu-id="87b33-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="87b33-116">PARAMETERS</span></span>

### <span data-ttu-id="87b33-117">-AllowAllAzureIPs</span><span class="sxs-lookup"><span data-stu-id="87b33-117">-AllowAllAzureIPs</span></span>
<span data-ttu-id="87b33-118">Indica que essa regra de firewall permite que todos os endereços IP do Azure acessem o servidor.</span><span class="sxs-lookup"><span data-stu-id="87b33-118">Indicates that this firewall rule allows all Azure IP addresses to access the server.</span></span>
<span data-ttu-id="87b33-119">Não será possível usar esse parâmetro se você pretende usar os *parâmetros FirewallRuleName,* *StartIpAddress* e *EndIpAddress.*</span><span class="sxs-lookup"><span data-stu-id="87b33-119">You cannot use this parameter if you intend to use the *FirewallRuleName*, *StartIpAddress*, and *EndIpAddress* parameters.</span></span>
<span data-ttu-id="87b33-120">Se você quiser permitir que os IPs do Azure acessem o servidor, esse parâmetro deve ser usado em uma chamada de cmdlet separada que não use os parâmetros *FirewallRuleName,* *StartIpAddress* e *EndIpAddress.*</span><span class="sxs-lookup"><span data-stu-id="87b33-120">If you want to allow Azure IPs to access the server, this parameter should be used in a separate cmdlet call that does not use the *FirewallRuleName*, *StartIpAddress*, and *EndIpAddress* parameters.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureIpRuleSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87b33-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87b33-121">-DefaultProfile</span></span>
<span data-ttu-id="87b33-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="87b33-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="87b33-123">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="87b33-123">-EndIpAddress</span></span>
<span data-ttu-id="87b33-124">Especifica o valor final do intervalo de endereços IP para essa regra.</span><span class="sxs-lookup"><span data-stu-id="87b33-124">Specifies the end value of the IP address range for this rule.</span></span>

```yaml
Type: System.String
Parameter Sets: UserSpecifiedRuleSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87b33-125">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="87b33-125">-FirewallRuleName</span></span>
<span data-ttu-id="87b33-126">Especifica o nome da nova regra de firewall.</span><span class="sxs-lookup"><span data-stu-id="87b33-126">Specifies the name of the new firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: UserSpecifiedRuleSet
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87b33-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87b33-127">-ResourceGroupName</span></span>
<span data-ttu-id="87b33-128">Especifica o nome de um grupo de recursos ao qual o servidor é atribuído.</span><span class="sxs-lookup"><span data-stu-id="87b33-128">Specifies the name of a resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="87b33-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="87b33-129">-ServerName</span></span>
<span data-ttu-id="87b33-130">Especifica o nome de um servidor.</span><span class="sxs-lookup"><span data-stu-id="87b33-130">Specifies the name of a server.</span></span>
<span data-ttu-id="87b33-131">Especifique o nome do servidor, não o nome DNS totalmente qualificado.</span><span class="sxs-lookup"><span data-stu-id="87b33-131">Specify the server name, not the fully qualified DNS name.</span></span>

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

### <span data-ttu-id="87b33-132">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="87b33-132">-StartIpAddress</span></span>
<span data-ttu-id="87b33-133">Especifica o valor inicial do intervalo de endereços IP para a regra de firewall.</span><span class="sxs-lookup"><span data-stu-id="87b33-133">Specifies the start value of the IP address range for the firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: UserSpecifiedRuleSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87b33-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="87b33-134">-Confirm</span></span>
<span data-ttu-id="87b33-135">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87b33-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87b33-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87b33-136">-WhatIf</span></span>
<span data-ttu-id="87b33-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="87b33-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87b33-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="87b33-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87b33-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87b33-139">CommonParameters</span></span>
<span data-ttu-id="87b33-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87b33-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87b33-141">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="87b33-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87b33-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="87b33-142">INPUTS</span></span>

### <span data-ttu-id="87b33-143">System.String</span><span class="sxs-lookup"><span data-stu-id="87b33-143">System.String</span></span>

## <span data-ttu-id="87b33-144">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="87b33-144">OUTPUTS</span></span>

### <span data-ttu-id="87b33-145">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="87b33-145">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="87b33-146">NOTES</span><span class="sxs-lookup"><span data-stu-id="87b33-146">NOTES</span></span>

## <span data-ttu-id="87b33-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="87b33-147">RELATED LINKS</span></span>

[<span data-ttu-id="87b33-148">Get-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="87b33-148">Get-AzSqlServerFirewallRule</span></span>](./Get-AzSqlServerFirewallRule.md)

[<span data-ttu-id="87b33-149">Remove-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="87b33-149">Remove-AzSqlServerFirewallRule</span></span>](./Remove-AzSqlServerFirewallRule.md)

[<span data-ttu-id="87b33-150">Set-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="87b33-150">Set-AzSqlServerFirewallRule</span></span>](./Set-AzSqlServerFirewallRule.md)

[<span data-ttu-id="87b33-151">SQL documentação do banco de dados</span><span class="sxs-lookup"><span data-stu-id="87b33-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


