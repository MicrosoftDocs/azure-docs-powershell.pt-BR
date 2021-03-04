---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B407CF77-792B-40F8-87AB-49FB3DCEE646
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerFirewallRule.md
ms.openlocfilehash: 2365cb4f6dedeb0620a2bdb1c1549eb0cd25d0c1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890579"
---
# <span data-ttu-id="23da4-101">Set-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="23da4-101">Set-AzSqlServerFirewallRule</span></span>

## <span data-ttu-id="23da4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23da4-102">SYNOPSIS</span></span>
<span data-ttu-id="23da4-103">Modifica uma regra de firewall no servidor de banco de dados do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="23da4-103">Modifies a firewall rule in Azure SQL Database server.</span></span>

## <span data-ttu-id="23da4-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="23da4-104">SYNTAX</span></span>

```
Set-AzSqlServerFirewallRule [-FirewallRuleName] <String> -StartIpAddress <String> -EndIpAddress <String>
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23da4-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="23da4-105">DESCRIPTION</span></span>
<span data-ttu-id="23da4-106">O cmdlet **Set-AzSqlServerFirewallRule** modifica uma regra de firewall em um servidor de banco de dados do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="23da4-106">The **Set-AzSqlServerFirewallRule** cmdlet modifies a firewall rule in an Azure SQL Database server.</span></span>

## <span data-ttu-id="23da4-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="23da4-107">EXAMPLES</span></span>

### <span data-ttu-id="23da4-108">Exemplo 1: Modificar uma regra de firewall</span><span class="sxs-lookup"><span data-stu-id="23da4-108">Example 1: Modify a firewall rule</span></span>
```
PS C:\>Set-AzSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -FirewallRuleName "Rule01" -StartIpAddress "192.168.0.197" -EndIpAddress "192.168.0.199"
ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 192.168.0.199
EndIpAddress      : 192.168.0.200
FirewallRuleName  : Rule01
```

<span data-ttu-id="23da4-109">Este comando modifica uma regra de firewall chamada Rule01 no servidor chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="23da4-109">This command modifies a firewall rule named Rule01 on the server named Server01.</span></span>
<span data-ttu-id="23da4-110">O comando modifica os endereços IP inicial e final.</span><span class="sxs-lookup"><span data-stu-id="23da4-110">The command modifies the start and end IP addresses.</span></span>

## <span data-ttu-id="23da4-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="23da4-111">PARAMETERS</span></span>

### <span data-ttu-id="23da4-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23da4-112">-DefaultProfile</span></span>
<span data-ttu-id="23da4-113">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="23da4-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="23da4-114">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="23da4-114">-EndIpAddress</span></span>
<span data-ttu-id="23da4-115">Especifica o valor final do intervalo de endereços IP para essa regra.</span><span class="sxs-lookup"><span data-stu-id="23da4-115">Specifies the end value of the IP address range for this rule.</span></span>

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

### <span data-ttu-id="23da4-116">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="23da4-116">-FirewallRuleName</span></span>
<span data-ttu-id="23da4-117">Especifica o nome da regra de firewall que este cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="23da4-117">Specifies the name of the firewall rule that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23da4-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23da4-118">-ResourceGroupName</span></span>
<span data-ttu-id="23da4-119">Especifica o nome do grupo de recursos ao qual o servidor é atribuído.</span><span class="sxs-lookup"><span data-stu-id="23da4-119">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="23da4-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="23da4-120">-ServerName</span></span>
<span data-ttu-id="23da4-121">Especifica o nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="23da4-121">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="23da4-122">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="23da4-122">-StartIpAddress</span></span>
<span data-ttu-id="23da4-123">Especifica o valor inicial do intervalo de endereços IP para a regra de firewall.</span><span class="sxs-lookup"><span data-stu-id="23da4-123">Specifies the start value of the IP address range for the firewall rule.</span></span>

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

### <span data-ttu-id="23da4-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="23da4-124">-Confirm</span></span>
<span data-ttu-id="23da4-125">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23da4-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23da4-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23da4-126">-WhatIf</span></span>
<span data-ttu-id="23da4-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="23da4-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23da4-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="23da4-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23da4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23da4-129">CommonParameters</span></span>
<span data-ttu-id="23da4-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23da4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23da4-131">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="23da4-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23da4-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="23da4-132">INPUTS</span></span>

### <span data-ttu-id="23da4-133">System.String</span><span class="sxs-lookup"><span data-stu-id="23da4-133">System.String</span></span>

## <span data-ttu-id="23da4-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="23da4-134">OUTPUTS</span></span>

### <span data-ttu-id="23da4-135">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="23da4-135">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="23da4-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="23da4-136">NOTES</span></span>

## <span data-ttu-id="23da4-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="23da4-137">RELATED LINKS</span></span>

[<span data-ttu-id="23da4-138">Get-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="23da4-138">Get-AzSqlServerFirewallRule</span></span>](./Get-AzSqlServerFirewallRule.md)

[<span data-ttu-id="23da4-139">New-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="23da4-139">New-AzSqlServerFirewallRule</span></span>](./New-AzSqlServerFirewallRule.md)

[<span data-ttu-id="23da4-140">Remove-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="23da4-140">Remove-AzSqlServerFirewallRule</span></span>](./Remove-AzSqlServerFirewallRule.md)

[<span data-ttu-id="23da4-141">SQL documentação do banco de dados</span><span class="sxs-lookup"><span data-stu-id="23da4-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


