---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B407CF77-792B-40F8-87AB-49FB3DCEE646
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerFirewallRule.md
ms.openlocfilehash: 5c079adea8079807374d4538f6259cd995103694
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598755"
---
# <span data-ttu-id="9fad0-101">Set-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="9fad0-101">Set-AzSqlServerFirewallRule</span></span>

## <span data-ttu-id="9fad0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9fad0-102">SYNOPSIS</span></span>
<span data-ttu-id="9fad0-103">Modifica uma regra de firewall no servidor de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="9fad0-103">Modifies a firewall rule in Azure SQL Database server.</span></span>

## <span data-ttu-id="9fad0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9fad0-104">SYNTAX</span></span>

```
Set-AzSqlServerFirewallRule [-FirewallRuleName] <String> -StartIpAddress <String> -EndIpAddress <String>
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9fad0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9fad0-105">DESCRIPTION</span></span>
<span data-ttu-id="9fad0-106">O cmdlet **set-AzSqlServerFirewallRule** modifica uma regra de firewall em um servidor de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="9fad0-106">The **Set-AzSqlServerFirewallRule** cmdlet modifies a firewall rule in an Azure SQL Database server.</span></span>

## <span data-ttu-id="9fad0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9fad0-107">EXAMPLES</span></span>

### <span data-ttu-id="9fad0-108">Exemplo 1: modificar uma regra de firewall</span><span class="sxs-lookup"><span data-stu-id="9fad0-108">Example 1: Modify a firewall rule</span></span>
```
PS C:\>Set-AzSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -FirewallRuleName "Rule01" -StartIpAddress "192.168.0.197" -EndIpAddress "192.168.0.199"
ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 192.168.0.199
EndIpAddress      : 192.168.0.200
FirewallRuleName  : Rule01
```

<span data-ttu-id="9fad0-109">Esse comando modifica uma regra de firewall chamada Rule01 no servidor chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="9fad0-109">This command modifies a firewall rule named Rule01 on the server named Server01.</span></span>
<span data-ttu-id="9fad0-110">O comando modifica os endereços IP de início e término.</span><span class="sxs-lookup"><span data-stu-id="9fad0-110">The command modifies the start and end IP addresses.</span></span>

## <span data-ttu-id="9fad0-111">OS</span><span class="sxs-lookup"><span data-stu-id="9fad0-111">PARAMETERS</span></span>

### <span data-ttu-id="9fad0-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fad0-112">-DefaultProfile</span></span>
<span data-ttu-id="9fad0-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="9fad0-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9fad0-114">-Endipaddress</span><span class="sxs-lookup"><span data-stu-id="9fad0-114">-EndIpAddress</span></span>
<span data-ttu-id="9fad0-115">Especifica o valor final do intervalo de endereços IP para esta regra.</span><span class="sxs-lookup"><span data-stu-id="9fad0-115">Specifies the end value of the IP address range for this rule.</span></span>

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

### <span data-ttu-id="9fad0-116">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="9fad0-116">-FirewallRuleName</span></span>
<span data-ttu-id="9fad0-117">Especifica o nome da regra de firewall que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="9fad0-117">Specifies the name of the firewall rule that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="9fad0-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9fad0-118">-ResourceGroupName</span></span>
<span data-ttu-id="9fad0-119">Especifica o nome do grupo de recursos ao qual o servidor está atribuído.</span><span class="sxs-lookup"><span data-stu-id="9fad0-119">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="9fad0-120">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="9fad0-120">-ServerName</span></span>
<span data-ttu-id="9fad0-121">Especifica o nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="9fad0-121">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="9fad0-122">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="9fad0-122">-StartIpAddress</span></span>
<span data-ttu-id="9fad0-123">Especifica o valor inicial do intervalo de endereços IP para a regra de firewall.</span><span class="sxs-lookup"><span data-stu-id="9fad0-123">Specifies the start value of the IP address range for the firewall rule.</span></span>

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

### <span data-ttu-id="9fad0-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9fad0-124">-Confirm</span></span>
<span data-ttu-id="9fad0-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9fad0-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9fad0-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9fad0-126">-WhatIf</span></span>
<span data-ttu-id="9fad0-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9fad0-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9fad0-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9fad0-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9fad0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fad0-129">CommonParameters</span></span>
<span data-ttu-id="9fad0-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9fad0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fad0-131">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9fad0-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fad0-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9fad0-132">INPUTS</span></span>

### <span data-ttu-id="9fad0-133">System. String</span><span class="sxs-lookup"><span data-stu-id="9fad0-133">System.String</span></span>

## <span data-ttu-id="9fad0-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9fad0-134">OUTPUTS</span></span>

### <span data-ttu-id="9fad0-135">Microsoft. Azure. Commands. Sql. FirewallRule. Model. AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="9fad0-135">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="9fad0-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9fad0-136">NOTES</span></span>

## <span data-ttu-id="9fad0-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9fad0-137">RELATED LINKS</span></span>

[<span data-ttu-id="9fad0-138">Get-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="9fad0-138">Get-AzSqlServerFirewallRule</span></span>](./Get-AzSqlServerFirewallRule.md)

[<span data-ttu-id="9fad0-139">New-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="9fad0-139">New-AzSqlServerFirewallRule</span></span>](./New-AzSqlServerFirewallRule.md)

[<span data-ttu-id="9fad0-140">Remove-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="9fad0-140">Remove-AzSqlServerFirewallRule</span></span>](./Remove-AzSqlServerFirewallRule.md)

[<span data-ttu-id="9fad0-141">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="9fad0-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


