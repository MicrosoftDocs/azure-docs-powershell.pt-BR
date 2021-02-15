---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 251A4546-AC23-4880-B197-773B1B814607
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerFirewallRule.md
ms.openlocfilehash: 83a68863b3dce71a091dc5de11377bade7bdc638
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116134"
---
# <span data-ttu-id="55871-101">Remove-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="55871-101">Remove-AzSqlServerFirewallRule</span></span>

## <span data-ttu-id="55871-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="55871-102">SYNOPSIS</span></span>
<span data-ttu-id="55871-103">Exclui uma regra de firewall de um servidor de banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="55871-103">Deletes a firewall rule from a SQL Database server.</span></span>

## <span data-ttu-id="55871-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="55871-104">SYNTAX</span></span>

```
Remove-AzSqlServerFirewallRule [-FirewallRuleName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="55871-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="55871-105">DESCRIPTION</span></span>
<span data-ttu-id="55871-106">O cmdlet **Remove-AzSqlServerFirewallRule** exclui uma regra de firewall do servidor de banco de dados SQL do Azure especificado.</span><span class="sxs-lookup"><span data-stu-id="55871-106">The **Remove-AzSqlServerFirewallRule** cmdlet deletes a firewall rule from the specified Azure SQL Database server.</span></span>

## <span data-ttu-id="55871-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="55871-107">EXAMPLES</span></span>

### <span data-ttu-id="55871-108">Exemplo 1: Excluir uma regra</span><span class="sxs-lookup"><span data-stu-id="55871-108">Example 1: Delete a rule</span></span>
```
PS C:\>Remove-AzSqlServerFirewallRule -FirewallRuleName "Rule01" -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="55871-109">Esse comando exclui uma regra de firewall chamada Rule01 no servidor chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="55871-109">This command deletes a firewall rule named Rule01 on the server named Server01.</span></span>

## <span data-ttu-id="55871-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="55871-110">PARAMETERS</span></span>

### <span data-ttu-id="55871-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55871-111">-DefaultProfile</span></span>
<span data-ttu-id="55871-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="55871-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="55871-113">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="55871-113">-FirewallRuleName</span></span>
<span data-ttu-id="55871-114">Especifica o nome da regra de firewall que este cmdlet exclui.</span><span class="sxs-lookup"><span data-stu-id="55871-114">Specifies the name of the firewall rule that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="55871-115">-Forçar</span><span class="sxs-lookup"><span data-stu-id="55871-115">-Force</span></span>
<span data-ttu-id="55871-116">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="55871-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="55871-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55871-117">-ResourceGroupName</span></span>
<span data-ttu-id="55871-118">Especifica o nome de um grupo de recursos ao qual o servidor é atribuído.</span><span class="sxs-lookup"><span data-stu-id="55871-118">Specifies the name of a resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="55871-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="55871-119">-ServerName</span></span>
<span data-ttu-id="55871-120">Especifica o nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="55871-120">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="55871-121">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="55871-121">-Confirm</span></span>
<span data-ttu-id="55871-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="55871-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55871-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55871-123">-WhatIf</span></span>
<span data-ttu-id="55871-124">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="55871-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55871-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="55871-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55871-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55871-126">CommonParameters</span></span>
<span data-ttu-id="55871-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55871-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55871-128">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="55871-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55871-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="55871-129">INPUTS</span></span>

### <span data-ttu-id="55871-130">System.String</span><span class="sxs-lookup"><span data-stu-id="55871-130">System.String</span></span>

## <span data-ttu-id="55871-131">Saídas</span><span class="sxs-lookup"><span data-stu-id="55871-131">OUTPUTS</span></span>

### <span data-ttu-id="55871-132">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="55871-132">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="55871-133">Notas</span><span class="sxs-lookup"><span data-stu-id="55871-133">NOTES</span></span>

## <span data-ttu-id="55871-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="55871-134">RELATED LINKS</span></span>

[<span data-ttu-id="55871-135">Get-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="55871-135">Get-AzSqlServerFirewallRule</span></span>](./Get-AzSqlServerFirewallRule.md)

[<span data-ttu-id="55871-136">New-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="55871-136">New-AzSqlServerFirewallRule</span></span>](./New-AzSqlServerFirewallRule.md)

[<span data-ttu-id="55871-137">Set-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="55871-137">Set-AzSqlServerFirewallRule</span></span>](./Set-AzSqlServerFirewallRule.md)

[<span data-ttu-id="55871-138">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="55871-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


