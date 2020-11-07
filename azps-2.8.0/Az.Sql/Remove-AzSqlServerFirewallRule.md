---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 251A4546-AC23-4880-B197-773B1B814607
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerFirewallRule.md
ms.openlocfilehash: ea3a34b8587b487fad1b0af35c2a50c36748913a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773799"
---
# <span data-ttu-id="be207-101">Remove-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="be207-101">Remove-AzSqlServerFirewallRule</span></span>

## <span data-ttu-id="be207-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="be207-102">SYNOPSIS</span></span>
<span data-ttu-id="be207-103">Exclui uma regra de firewall de um servidor de banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="be207-103">Deletes a firewall rule from a SQL Database server.</span></span>

## <span data-ttu-id="be207-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="be207-104">SYNTAX</span></span>

```
Remove-AzSqlServerFirewallRule [-FirewallRuleName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="be207-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="be207-105">DESCRIPTION</span></span>
<span data-ttu-id="be207-106">O cmdlet **Remove-AzSqlServerFirewallRule** exclui uma regra de firewall do servidor de banco de dados SQL do Azure especificado.</span><span class="sxs-lookup"><span data-stu-id="be207-106">The **Remove-AzSqlServerFirewallRule** cmdlet deletes a firewall rule from the specified Azure SQL Database server.</span></span>

## <span data-ttu-id="be207-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="be207-107">EXAMPLES</span></span>

### <span data-ttu-id="be207-108">Exemplo 1: excluir uma regra</span><span class="sxs-lookup"><span data-stu-id="be207-108">Example 1: Delete a rule</span></span>
```
PS C:\>Remove-AzSqlServerFirewallRule -FirewallRuleName "Rule01" -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="be207-109">Esse comando exclui uma regra de firewall chamada Rule01 no servidor chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="be207-109">This command deletes a firewall rule named Rule01 on the server named Server01.</span></span>

## <span data-ttu-id="be207-110">OS</span><span class="sxs-lookup"><span data-stu-id="be207-110">PARAMETERS</span></span>

### <span data-ttu-id="be207-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be207-111">-DefaultProfile</span></span>
<span data-ttu-id="be207-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="be207-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="be207-113">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="be207-113">-FirewallRuleName</span></span>
<span data-ttu-id="be207-114">Especifica o nome da regra de firewall que este cmdlet exclui.</span><span class="sxs-lookup"><span data-stu-id="be207-114">Specifies the name of the firewall rule that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="be207-115">-Force</span><span class="sxs-lookup"><span data-stu-id="be207-115">-Force</span></span>
<span data-ttu-id="be207-116">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="be207-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="be207-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be207-117">-ResourceGroupName</span></span>
<span data-ttu-id="be207-118">Especifica o nome de um grupo de recursos ao qual o servidor está atribuído.</span><span class="sxs-lookup"><span data-stu-id="be207-118">Specifies the name of a resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="be207-119">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="be207-119">-ServerName</span></span>
<span data-ttu-id="be207-120">Especifica o nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="be207-120">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="be207-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="be207-121">-Confirm</span></span>
<span data-ttu-id="be207-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="be207-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be207-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be207-123">-WhatIf</span></span>
<span data-ttu-id="be207-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="be207-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be207-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="be207-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be207-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be207-126">CommonParameters</span></span>
<span data-ttu-id="be207-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be207-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be207-128">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="be207-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be207-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="be207-129">INPUTS</span></span>

### <span data-ttu-id="be207-130">System. String</span><span class="sxs-lookup"><span data-stu-id="be207-130">System.String</span></span>

## <span data-ttu-id="be207-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="be207-131">OUTPUTS</span></span>

### <span data-ttu-id="be207-132">Microsoft. Azure. Commands. Sql. FirewallRule. Model. AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="be207-132">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="be207-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="be207-133">NOTES</span></span>

## <span data-ttu-id="be207-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="be207-134">RELATED LINKS</span></span>

[<span data-ttu-id="be207-135">Get-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="be207-135">Get-AzSqlServerFirewallRule</span></span>](./Get-AzSqlServerFirewallRule.md)

[<span data-ttu-id="be207-136">New-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="be207-136">New-AzSqlServerFirewallRule</span></span>](./New-AzSqlServerFirewallRule.md)

[<span data-ttu-id="be207-137">Set-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="be207-137">Set-AzSqlServerFirewallRule</span></span>](./Set-AzSqlServerFirewallRule.md)

[<span data-ttu-id="be207-138">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="be207-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

