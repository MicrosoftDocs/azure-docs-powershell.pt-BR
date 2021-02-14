---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: AD8BA5CB-D5D4-4C6E-A65F-E7AE69E3B22C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerFirewallRule.md
ms.openlocfilehash: c2157521614375bbdeb06aac9a62320ec1e08c70
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117093"
---
# <span data-ttu-id="8ba5f-101">Get-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="8ba5f-101">Get-AzSqlServerFirewallRule</span></span>

## <span data-ttu-id="8ba5f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8ba5f-102">SYNOPSIS</span></span>
<span data-ttu-id="8ba5f-103">Obtém regras de firewall para um servidor de banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="8ba5f-103">Gets firewall rules for a SQL Database server.</span></span>

## <span data-ttu-id="8ba5f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8ba5f-104">SYNTAX</span></span>

```
Get-AzSqlServerFirewallRule [[-FirewallRuleName] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ba5f-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="8ba5f-105">DESCRIPTION</span></span>
<span data-ttu-id="8ba5f-106">O cmdlet **Get-AzSqlServerFirewallRule obtém** regras de firewall para um servidor de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="8ba5f-106">The **Get-AzSqlServerFirewallRule** cmdlet gets firewall rules for an Azure SQL Database server.</span></span>
<span data-ttu-id="8ba5f-107">Se você especificar o nome de uma regra de firewall, esse cmdlet obterá informações sobre essa regra de firewall específica.</span><span class="sxs-lookup"><span data-stu-id="8ba5f-107">If you specify the name of a firewall rule, this cmdlet gets information about that specific firewall rule.</span></span>

## <span data-ttu-id="8ba5f-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8ba5f-108">EXAMPLES</span></span>

### <span data-ttu-id="8ba5f-109">Exemplo 1: Obter todas as regras para um servidor</span><span class="sxs-lookup"><span data-stu-id="8ba5f-109">Example 1: Get all rules for a server</span></span>
```
PS C:\>Get-AzSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName : ResourceGroup01
ServerName        : server01
StartIpAddress    : 0.0.0.0
EndIpAddress      : 0.0.0.0
FirewallRuleName  : AllowAllWindowsAzureIps

ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 1.2.3.4
EndIpAddress      : 4.3.2.1
FirewallRuleName  : Rule01
```

<span data-ttu-id="8ba5f-110">Esse comando obtém todas as regras de firewall do servidor chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="8ba5f-110">This command gets all the firewall rules for the server named Server01.</span></span>

### <span data-ttu-id="8ba5f-111">Exemplo 2: Obter todas as regras para um servidor usando filtragem</span><span class="sxs-lookup"><span data-stu-id="8ba5f-111">Example 2: Get all rules for a server using filtering</span></span>
```
PS C:\>Get-AzSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -FirewallRuleName "Rule*"
ResourceGroupName : ResourceGroup01
ServerName        : server01
StartIpAddress    : 0.0.0.0
EndIpAddress      : 0.0.0.0
FirewallRuleName  : Rule01

ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 1.2.3.4
EndIpAddress      : 4.3.2.1
FirewallRuleName  : Rule02
```

<span data-ttu-id="8ba5f-112">Esse comando obtém todas as regras de firewall do servidor chamado Server01 que começam com "Regra".</span><span class="sxs-lookup"><span data-stu-id="8ba5f-112">This command gets all the firewall rules for the server named Server01 that start with "Rule".</span></span>

## <span data-ttu-id="8ba5f-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8ba5f-113">PARAMETERS</span></span>

### <span data-ttu-id="8ba5f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ba5f-114">-DefaultProfile</span></span>
<span data-ttu-id="8ba5f-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="8ba5f-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8ba5f-116">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="8ba5f-116">-FirewallRuleName</span></span>
<span data-ttu-id="8ba5f-117">Especifica o nome da regra de firewall.</span><span class="sxs-lookup"><span data-stu-id="8ba5f-117">Specifies the name of the firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ba5f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ba5f-118">-ResourceGroupName</span></span>
<span data-ttu-id="8ba5f-119">Especifica o nome do grupo de recursos ao qual o SQL Server é atribuído.</span><span class="sxs-lookup"><span data-stu-id="8ba5f-119">Specifies the name of the resource group to which the SQL Server is assigned.</span></span>

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

### <span data-ttu-id="8ba5f-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="8ba5f-120">-ServerName</span></span>
<span data-ttu-id="8ba5f-121">Especifica o nome do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="8ba5f-121">Specifies the name of the SQL Server.</span></span>

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

### <span data-ttu-id="8ba5f-122">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="8ba5f-122">-Confirm</span></span>
<span data-ttu-id="8ba5f-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ba5f-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ba5f-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ba5f-124">-WhatIf</span></span>
<span data-ttu-id="8ba5f-125">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="8ba5f-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ba5f-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8ba5f-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ba5f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ba5f-127">CommonParameters</span></span>
<span data-ttu-id="8ba5f-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ba5f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ba5f-129">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8ba5f-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ba5f-130">Entradas</span><span class="sxs-lookup"><span data-stu-id="8ba5f-130">INPUTS</span></span>

### <span data-ttu-id="8ba5f-131">System.String</span><span class="sxs-lookup"><span data-stu-id="8ba5f-131">System.String</span></span>

## <span data-ttu-id="8ba5f-132">Saídas</span><span class="sxs-lookup"><span data-stu-id="8ba5f-132">OUTPUTS</span></span>

### <span data-ttu-id="8ba5f-133">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="8ba5f-133">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="8ba5f-134">Notas</span><span class="sxs-lookup"><span data-stu-id="8ba5f-134">NOTES</span></span>

## <span data-ttu-id="8ba5f-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8ba5f-135">RELATED LINKS</span></span>

[<span data-ttu-id="8ba5f-136">New-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="8ba5f-136">New-AzSqlServerFirewallRule</span></span>](./New-AzSqlServerFirewallRule.md)

[<span data-ttu-id="8ba5f-137">Remove-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="8ba5f-137">Remove-AzSqlServerFirewallRule</span></span>](./Remove-AzSqlServerFirewallRule.md)

[<span data-ttu-id="8ba5f-138">Set-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="8ba5f-138">Set-AzSqlServerFirewallRule</span></span>](./Set-AzSqlServerFirewallRule.md)

[<span data-ttu-id="8ba5f-139">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="8ba5f-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


