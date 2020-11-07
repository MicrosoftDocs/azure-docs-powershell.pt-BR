---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 383DD041-78DC-4170-9529-1FD6F13BC178
online version: ''
schema: 2.0.0
ms.openlocfilehash: 29cbf01629ef772fc41436f3916a2077c1535329
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946106"
---
# <span data-ttu-id="c3e10-101">Remove-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="c3e10-101">Remove-AzureSqlDatabaseServerFirewallRule</span></span>

## <span data-ttu-id="c3e10-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c3e10-102">SYNOPSIS</span></span>
<span data-ttu-id="c3e10-103">Remove uma regra de firewall de um servidor de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="c3e10-103">Removes a firewall rule from an Azure SQL Database server.</span></span>

## <span data-ttu-id="c3e10-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c3e10-104">SYNTAX</span></span>

```
Remove-AzureSqlDatabaseServerFirewallRule -ServerName <String> -RuleName <String> [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3e10-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c3e10-105">DESCRIPTION</span></span>
<span data-ttu-id="c3e10-106">O cmdlet **Remove-AzureSqlDatabaseServerFirewallRule** remove uma regra de firewall de uma instância do servidor de banco de dados SQL do Azure na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="c3e10-106">The **Remove-AzureSqlDatabaseServerFirewallRule** cmdlet removes a firewall rule from an instance of Azure SQL Database Server in the current subscription.</span></span>

## <span data-ttu-id="c3e10-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c3e10-107">EXAMPLES</span></span>

### <span data-ttu-id="c3e10-108">Exemplo 1: remover uma regra</span><span class="sxs-lookup"><span data-stu-id="c3e10-108">Example 1: Remove a rule</span></span>
```
PS C:\>Remove-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y" -RuleName "FirewallRule24"
```

<span data-ttu-id="c3e10-109">Esse comando Remove a regra de firewall chamada FirewallRule24 do servidor de banco de dados SQL do Azure chamado lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="c3e10-109">This command removes the firewall rule named FirewallRule24 from the Azure SQL Database server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="c3e10-110">OS</span><span class="sxs-lookup"><span data-stu-id="c3e10-110">PARAMETERS</span></span>

### <span data-ttu-id="c3e10-111">-Force</span><span class="sxs-lookup"><span data-stu-id="c3e10-111">-Force</span></span>
<span data-ttu-id="c3e10-112">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="c3e10-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c3e10-113">-Perfil</span><span class="sxs-lookup"><span data-stu-id="c3e10-113">-Profile</span></span>
<span data-ttu-id="c3e10-114">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="c3e10-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c3e10-115">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="c3e10-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3e10-116">-RuleName</span><span class="sxs-lookup"><span data-stu-id="c3e10-116">-RuleName</span></span>
<span data-ttu-id="c3e10-117">Especifica o nome da regra de firewall que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="c3e10-117">Specifies the name of the firewall rule that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3e10-118">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="c3e10-118">-ServerName</span></span>
<span data-ttu-id="c3e10-119">Especifica o nome de um servidor.</span><span class="sxs-lookup"><span data-stu-id="c3e10-119">Specifies the name of a server.</span></span>
<span data-ttu-id="c3e10-120">Esse cmdlet Remove uma regra de firewall do servidor que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="c3e10-120">This cmdlet removes a firewall rule from the server that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3e10-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c3e10-121">-Confirm</span></span>
<span data-ttu-id="c3e10-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c3e10-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3e10-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3e10-123">-WhatIf</span></span>
<span data-ttu-id="c3e10-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c3e10-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3e10-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c3e10-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3e10-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3e10-126">CommonParameters</span></span>
<span data-ttu-id="c3e10-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3e10-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3e10-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3e10-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3e10-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c3e10-129">INPUTS</span></span>

### <span data-ttu-id="c3e10-130">Microsoft. WindowsAzure. Commands. SQLDatabase. Model. SqlDatabaseServerFirewallRuleContext</span><span class="sxs-lookup"><span data-stu-id="c3e10-130">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerFirewallRuleContext</span></span>

## <span data-ttu-id="c3e10-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c3e10-131">OUTPUTS</span></span>

## <span data-ttu-id="c3e10-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c3e10-132">NOTES</span></span>

## <span data-ttu-id="c3e10-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c3e10-133">RELATED LINKS</span></span>

[<span data-ttu-id="c3e10-134">Banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="c3e10-134">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="c3e10-135">Excluir regra de firewall</span><span class="sxs-lookup"><span data-stu-id="c3e10-135">Delete Firewall Rule</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505706.aspx)

[<span data-ttu-id="c3e10-136">Operações para bancos de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="c3e10-136">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="c3e10-137">Get-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="c3e10-137">Get-AzureSqlDatabaseServerFirewallRule</span></span>](./Get-AzureSqlDatabaseServerFirewallRule.md)

[<span data-ttu-id="c3e10-138">New-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="c3e10-138">New-AzureSqlDatabaseServerFirewallRule</span></span>](./New-AzureSqlDatabaseServerFirewallRule.md)

[<span data-ttu-id="c3e10-139">Set-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="c3e10-139">Set-AzureSqlDatabaseServerFirewallRule</span></span>](./Set-AzureSqlDatabaseServerFirewallRule.md)


