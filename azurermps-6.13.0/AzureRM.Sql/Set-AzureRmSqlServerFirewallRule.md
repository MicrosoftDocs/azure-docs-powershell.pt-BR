---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: B407CF77-792B-40F8-87AB-49FB3DCEE646
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerFirewallRule.md
ms.openlocfilehash: e3d2d706a954bf8cbd7359be4ee7a835fdd4f431
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429302"
---
# <span data-ttu-id="8b020-101">Set-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="8b020-101">Set-AzureRmSqlServerFirewallRule</span></span>

## <span data-ttu-id="8b020-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8b020-102">SYNOPSIS</span></span>
<span data-ttu-id="8b020-103">Modifica uma regra de firewall no servidor de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="8b020-103">Modifies a firewall rule in Azure SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8b020-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8b020-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerFirewallRule [-FirewallRuleName] <String> -StartIpAddress <String> -EndIpAddress <String>
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b020-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8b020-105">DESCRIPTION</span></span>
<span data-ttu-id="8b020-106">O cmdlet **set-AzureRmSqlServerFirewallRule** modifica uma regra de firewall em um servidor de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="8b020-106">The **Set-AzureRmSqlServerFirewallRule** cmdlet modifies a firewall rule in an Azure SQL Database server.</span></span>

## <span data-ttu-id="8b020-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8b020-107">EXAMPLES</span></span>

### <span data-ttu-id="8b020-108">Exemplo 1: modificar uma regra de firewall</span><span class="sxs-lookup"><span data-stu-id="8b020-108">Example 1: Modify a firewall rule</span></span>
```
PS C:\>Set-AzureRmSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -FirewallRuleName "Rule01" -StartIpAddress "192.168.0.197" -EndIpAddress "192.168.0.199"
ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 192.168.0.199
EndIpAddress      : 192.168.0.200
FirewallRuleName  : Rule01
```

<span data-ttu-id="8b020-109">Esse comando modifica uma regra de firewall chamada Rule01 no servidor chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="8b020-109">This command modifies a firewall rule named Rule01 on the server named Server01.</span></span>
<span data-ttu-id="8b020-110">O comando modifica os endereços IP de início e término.</span><span class="sxs-lookup"><span data-stu-id="8b020-110">The command modifies the start and end IP addresses.</span></span>

## <span data-ttu-id="8b020-111">OS</span><span class="sxs-lookup"><span data-stu-id="8b020-111">PARAMETERS</span></span>

### <span data-ttu-id="8b020-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b020-112">-DefaultProfile</span></span>
<span data-ttu-id="8b020-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="8b020-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b020-114">-Endipaddress</span><span class="sxs-lookup"><span data-stu-id="8b020-114">-EndIpAddress</span></span>
<span data-ttu-id="8b020-115">Especifica o valor final do intervalo de endereços IP para esta regra.</span><span class="sxs-lookup"><span data-stu-id="8b020-115">Specifies the end value of the IP address range for this rule.</span></span>

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

### <span data-ttu-id="8b020-116">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="8b020-116">-FirewallRuleName</span></span>
<span data-ttu-id="8b020-117">Especifica o nome da regra de firewall que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="8b020-117">Specifies the name of the firewall rule that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="8b020-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b020-118">-ResourceGroupName</span></span>
<span data-ttu-id="8b020-119">Especifica o nome do grupo de recursos ao qual o servidor está atribuído.</span><span class="sxs-lookup"><span data-stu-id="8b020-119">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="8b020-120">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="8b020-120">-ServerName</span></span>
<span data-ttu-id="8b020-121">Especifica o nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="8b020-121">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="8b020-122">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="8b020-122">-StartIpAddress</span></span>
<span data-ttu-id="8b020-123">Especifica o valor inicial do intervalo de endereços IP para a regra de firewall.</span><span class="sxs-lookup"><span data-stu-id="8b020-123">Specifies the start value of the IP address range for the firewall rule.</span></span>

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

### <span data-ttu-id="8b020-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8b020-124">-Confirm</span></span>
<span data-ttu-id="8b020-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b020-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b020-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b020-126">-WhatIf</span></span>
<span data-ttu-id="8b020-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8b020-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b020-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8b020-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b020-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b020-129">CommonParameters</span></span>
<span data-ttu-id="8b020-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b020-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b020-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b020-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b020-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8b020-132">INPUTS</span></span>

### <span data-ttu-id="8b020-133">System. String</span><span class="sxs-lookup"><span data-stu-id="8b020-133">System.String</span></span>

## <span data-ttu-id="8b020-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8b020-134">OUTPUTS</span></span>

### <span data-ttu-id="8b020-135">Microsoft. Azure. Commands. Sql. FirewallRule. Model. AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="8b020-135">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="8b020-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8b020-136">NOTES</span></span>

## <span data-ttu-id="8b020-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8b020-137">RELATED LINKS</span></span>

[<span data-ttu-id="8b020-138">Get-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="8b020-138">Get-AzureRmSqlServerFirewallRule</span></span>](./Get-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="8b020-139">New-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="8b020-139">New-AzureRmSqlServerFirewallRule</span></span>](./New-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="8b020-140">Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="8b020-140">Remove-AzureRmSqlServerFirewallRule</span></span>](./Remove-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="8b020-141">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="8b020-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


