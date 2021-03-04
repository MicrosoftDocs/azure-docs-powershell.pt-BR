---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 251A4546-AC23-4880-B197-773B1B814607
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerFirewallRule.md
ms.openlocfilehash: 0b76faf383e8cd3c70d6ff1e7e38de367850ac8b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887305"
---
# <span data-ttu-id="cf719-101">Remove-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="cf719-101">Remove-AzSqlServerFirewallRule</span></span>

## <span data-ttu-id="cf719-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf719-102">SYNOPSIS</span></span>
<span data-ttu-id="cf719-103">Exclui uma regra de firewall de um servidor SQL Banco de Dados.</span><span class="sxs-lookup"><span data-stu-id="cf719-103">Deletes a firewall rule from a SQL Database server.</span></span>

## <span data-ttu-id="cf719-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="cf719-104">SYNTAX</span></span>

```
Remove-AzSqlServerFirewallRule [-FirewallRuleName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cf719-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="cf719-105">DESCRIPTION</span></span>
<span data-ttu-id="cf719-106">O cmdlet **Remove-AzSqlServerFirewallRule** exclui uma regra de firewall do servidor de banco de dados SQL Azure especificado.</span><span class="sxs-lookup"><span data-stu-id="cf719-106">The **Remove-AzSqlServerFirewallRule** cmdlet deletes a firewall rule from the specified Azure SQL Database server.</span></span>

## <span data-ttu-id="cf719-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cf719-107">EXAMPLES</span></span>

### <span data-ttu-id="cf719-108">Exemplo 1: Excluir uma regra</span><span class="sxs-lookup"><span data-stu-id="cf719-108">Example 1: Delete a rule</span></span>
```
PS C:\>Remove-AzSqlServerFirewallRule -FirewallRuleName "Rule01" -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="cf719-109">Este comando exclui uma regra de firewall chamada Rule01 no servidor chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="cf719-109">This command deletes a firewall rule named Rule01 on the server named Server01.</span></span>

## <span data-ttu-id="cf719-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="cf719-110">PARAMETERS</span></span>

### <span data-ttu-id="cf719-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf719-111">-DefaultProfile</span></span>
<span data-ttu-id="cf719-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="cf719-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cf719-113">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="cf719-113">-FirewallRuleName</span></span>
<span data-ttu-id="cf719-114">Especifica o nome da regra de firewall que esse cmdlet exclui.</span><span class="sxs-lookup"><span data-stu-id="cf719-114">Specifies the name of the firewall rule that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="cf719-115">-Force</span><span class="sxs-lookup"><span data-stu-id="cf719-115">-Force</span></span>
<span data-ttu-id="cf719-116">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="cf719-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="cf719-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf719-117">-ResourceGroupName</span></span>
<span data-ttu-id="cf719-118">Especifica o nome de um grupo de recursos ao qual o servidor é atribuído.</span><span class="sxs-lookup"><span data-stu-id="cf719-118">Specifies the name of a resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="cf719-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="cf719-119">-ServerName</span></span>
<span data-ttu-id="cf719-120">Especifica o nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="cf719-120">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="cf719-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cf719-121">-Confirm</span></span>
<span data-ttu-id="cf719-122">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf719-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf719-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf719-123">-WhatIf</span></span>
<span data-ttu-id="cf719-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cf719-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf719-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cf719-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf719-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf719-126">CommonParameters</span></span>
<span data-ttu-id="cf719-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf719-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf719-128">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cf719-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf719-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cf719-129">INPUTS</span></span>

### <span data-ttu-id="cf719-130">System.String</span><span class="sxs-lookup"><span data-stu-id="cf719-130">System.String</span></span>

## <span data-ttu-id="cf719-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="cf719-131">OUTPUTS</span></span>

### <span data-ttu-id="cf719-132">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="cf719-132">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="cf719-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="cf719-133">NOTES</span></span>

## <span data-ttu-id="cf719-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cf719-134">RELATED LINKS</span></span>

[<span data-ttu-id="cf719-135">Get-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="cf719-135">Get-AzSqlServerFirewallRule</span></span>](./Get-AzSqlServerFirewallRule.md)

[<span data-ttu-id="cf719-136">New-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="cf719-136">New-AzSqlServerFirewallRule</span></span>](./New-AzSqlServerFirewallRule.md)

[<span data-ttu-id="cf719-137">Set-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="cf719-137">Set-AzSqlServerFirewallRule</span></span>](./Set-AzSqlServerFirewallRule.md)

[<span data-ttu-id="cf719-138">SQL documentação do banco de dados</span><span class="sxs-lookup"><span data-stu-id="cf719-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


