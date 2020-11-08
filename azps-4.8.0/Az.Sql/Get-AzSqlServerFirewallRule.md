---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: AD8BA5CB-D5D4-4C6E-A65F-E7AE69E3B22C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerFirewallRule.md
ms.openlocfilehash: c2157521614375bbdeb06aac9a62320ec1e08c70
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94112122"
---
# <span data-ttu-id="38dd1-101">Get-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="38dd1-101">Get-AzSqlServerFirewallRule</span></span>

## <span data-ttu-id="38dd1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="38dd1-102">SYNOPSIS</span></span>
<span data-ttu-id="38dd1-103">Obtém regras de firewall para um servidor de banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="38dd1-103">Gets firewall rules for a SQL Database server.</span></span>

## <span data-ttu-id="38dd1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="38dd1-104">SYNTAX</span></span>

```
Get-AzSqlServerFirewallRule [[-FirewallRuleName] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38dd1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="38dd1-105">DESCRIPTION</span></span>
<span data-ttu-id="38dd1-106">O cmdlet **Get-AzSqlServerFirewallRule** Obtém regras de firewall para um servidor de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="38dd1-106">The **Get-AzSqlServerFirewallRule** cmdlet gets firewall rules for an Azure SQL Database server.</span></span>
<span data-ttu-id="38dd1-107">Se você especificar o nome de uma regra de firewall, esse cmdlet obterá informações sobre essa regra de firewall específica.</span><span class="sxs-lookup"><span data-stu-id="38dd1-107">If you specify the name of a firewall rule, this cmdlet gets information about that specific firewall rule.</span></span>

## <span data-ttu-id="38dd1-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="38dd1-108">EXAMPLES</span></span>

### <span data-ttu-id="38dd1-109">Exemplo 1: obter todas as regras para um servidor</span><span class="sxs-lookup"><span data-stu-id="38dd1-109">Example 1: Get all rules for a server</span></span>
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

<span data-ttu-id="38dd1-110">Esse comando obtém todas as regras de firewall do servidor chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="38dd1-110">This command gets all the firewall rules for the server named Server01.</span></span>

### <span data-ttu-id="38dd1-111">Exemplo 2: obter todas as regras de um servidor usando a filtragem</span><span class="sxs-lookup"><span data-stu-id="38dd1-111">Example 2: Get all rules for a server using filtering</span></span>
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

<span data-ttu-id="38dd1-112">Esse comando obtém todas as regras de firewall do servidor chamado Server01 que começam com "regra".</span><span class="sxs-lookup"><span data-stu-id="38dd1-112">This command gets all the firewall rules for the server named Server01 that start with "Rule".</span></span>

## <span data-ttu-id="38dd1-113">OS</span><span class="sxs-lookup"><span data-stu-id="38dd1-113">PARAMETERS</span></span>

### <span data-ttu-id="38dd1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38dd1-114">-DefaultProfile</span></span>
<span data-ttu-id="38dd1-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="38dd1-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="38dd1-116">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="38dd1-116">-FirewallRuleName</span></span>
<span data-ttu-id="38dd1-117">Especifica o nome da regra de firewall.</span><span class="sxs-lookup"><span data-stu-id="38dd1-117">Specifies the name of the firewall rule.</span></span>

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

### <span data-ttu-id="38dd1-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38dd1-118">-ResourceGroupName</span></span>
<span data-ttu-id="38dd1-119">Especifica o nome do grupo de recursos ao qual o SQL Server está atribuído.</span><span class="sxs-lookup"><span data-stu-id="38dd1-119">Specifies the name of the resource group to which the SQL Server is assigned.</span></span>

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

### <span data-ttu-id="38dd1-120">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="38dd1-120">-ServerName</span></span>
<span data-ttu-id="38dd1-121">Especifica o nome do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="38dd1-121">Specifies the name of the SQL Server.</span></span>

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

### <span data-ttu-id="38dd1-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="38dd1-122">-Confirm</span></span>
<span data-ttu-id="38dd1-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38dd1-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38dd1-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38dd1-124">-WhatIf</span></span>
<span data-ttu-id="38dd1-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="38dd1-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38dd1-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="38dd1-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38dd1-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38dd1-127">CommonParameters</span></span>
<span data-ttu-id="38dd1-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38dd1-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38dd1-129">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="38dd1-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38dd1-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="38dd1-130">INPUTS</span></span>

### <span data-ttu-id="38dd1-131">System. String</span><span class="sxs-lookup"><span data-stu-id="38dd1-131">System.String</span></span>

## <span data-ttu-id="38dd1-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="38dd1-132">OUTPUTS</span></span>

### <span data-ttu-id="38dd1-133">Microsoft. Azure. Commands. Sql. FirewallRule. Model. AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="38dd1-133">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="38dd1-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="38dd1-134">NOTES</span></span>

## <span data-ttu-id="38dd1-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="38dd1-135">RELATED LINKS</span></span>

[<span data-ttu-id="38dd1-136">New-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="38dd1-136">New-AzSqlServerFirewallRule</span></span>](./New-AzSqlServerFirewallRule.md)

[<span data-ttu-id="38dd1-137">Remove-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="38dd1-137">Remove-AzSqlServerFirewallRule</span></span>](./Remove-AzSqlServerFirewallRule.md)

[<span data-ttu-id="38dd1-138">Set-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="38dd1-138">Set-AzSqlServerFirewallRule</span></span>](./Set-AzSqlServerFirewallRule.md)

[<span data-ttu-id="38dd1-139">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="38dd1-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


