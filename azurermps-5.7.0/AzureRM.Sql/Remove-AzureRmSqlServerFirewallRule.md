---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 251A4546-AC23-4880-B197-773B1B814607
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerFirewallRule.md
ms.openlocfilehash: 6f79d85fd09848f1b6f43e4907565b4989197183
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428728"
---
# <span data-ttu-id="af954-101">Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="af954-101">Remove-AzureRmSqlServerFirewallRule</span></span>

## <span data-ttu-id="af954-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="af954-102">SYNOPSIS</span></span>
<span data-ttu-id="af954-103">Exclui uma regra de firewall de um servidor de banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="af954-103">Deletes a firewall rule from a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af954-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="af954-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerFirewallRule [-FirewallRuleName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="af954-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="af954-105">DESCRIPTION</span></span>
<span data-ttu-id="af954-106">O cmdlet **Remove-AzureRmSqlServerFirewallRule** exclui uma regra de firewall do servidor de banco de dados SQL do Azure especificado.</span><span class="sxs-lookup"><span data-stu-id="af954-106">The **Remove-AzureRmSqlServerFirewallRule** cmdlet deletes a firewall rule from the specified Azure SQL Database server.</span></span>

## <span data-ttu-id="af954-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="af954-107">EXAMPLES</span></span>

### <span data-ttu-id="af954-108">Exemplo 1: excluir uma regra</span><span class="sxs-lookup"><span data-stu-id="af954-108">Example 1: Delete a rule</span></span>
```
PS C:\>Remove-AzureRmSqlServerFirewallRule -FirewallRuleName "Rule01" -ResourceGroupName "RresourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="af954-109">Esse comando exclui uma regra de firewall chamada Rule01 no servidor chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="af954-109">This command deletes a firewall rule named Rule01 on the server named Server01.</span></span>

## <span data-ttu-id="af954-110">OS</span><span class="sxs-lookup"><span data-stu-id="af954-110">PARAMETERS</span></span>

### <span data-ttu-id="af954-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af954-111">-DefaultProfile</span></span>
<span data-ttu-id="af954-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="af954-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af954-113">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="af954-113">-FirewallRuleName</span></span>
<span data-ttu-id="af954-114">Especifica o nome da regra de firewall que este cmdlet exclui.</span><span class="sxs-lookup"><span data-stu-id="af954-114">Specifies the name of the firewall rule that this cmdlet deletes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af954-115">-Force</span><span class="sxs-lookup"><span data-stu-id="af954-115">-Force</span></span>
<span data-ttu-id="af954-116">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="af954-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af954-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af954-117">-ResourceGroupName</span></span>
<span data-ttu-id="af954-118">Especifica o nome de um grupo de recursos ao qual o servidor está atribuído.</span><span class="sxs-lookup"><span data-stu-id="af954-118">Specifies the name of a resource group to which the server is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af954-119">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="af954-119">-ServerName</span></span>
<span data-ttu-id="af954-120">Especifica o nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="af954-120">Specifies the name of the server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af954-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="af954-121">-Confirm</span></span>
<span data-ttu-id="af954-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af954-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af954-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af954-123">-WhatIf</span></span>
<span data-ttu-id="af954-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="af954-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af954-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="af954-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af954-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af954-126">CommonParameters</span></span>
<span data-ttu-id="af954-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af954-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af954-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af954-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af954-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="af954-129">INPUTS</span></span>

### <span data-ttu-id="af954-130">Microsoft. Azure. Commands. Sql. FirewallRule. Model. AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="af954-130">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="af954-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="af954-131">OUTPUTS</span></span>

## <span data-ttu-id="af954-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="af954-132">NOTES</span></span>

## <span data-ttu-id="af954-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="af954-133">RELATED LINKS</span></span>

[<span data-ttu-id="af954-134">Get-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="af954-134">Get-AzureRmSqlServerFirewallRule</span></span>](./Get-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="af954-135">New-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="af954-135">New-AzureRmSqlServerFirewallRule</span></span>](./New-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="af954-136">Set-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="af954-136">Set-AzureRmSqlServerFirewallRule</span></span>](./Set-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="af954-137">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="af954-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


