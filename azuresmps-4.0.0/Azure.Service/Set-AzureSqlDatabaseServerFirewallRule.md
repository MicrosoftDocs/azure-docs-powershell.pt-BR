---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: F311A7A9-5FE9-4E81-8FF1-8E3A02F2BF4B
online version: ''
schema: 2.0.0
ms.openlocfilehash: ce9d384a5dd7f57fb4444fb173864ec5859b3a81
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945863"
---
# <span data-ttu-id="91734-101">Set-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="91734-101">Set-AzureSqlDatabaseServerFirewallRule</span></span>

## <span data-ttu-id="91734-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="91734-102">SYNOPSIS</span></span>
<span data-ttu-id="91734-103">Modifica uma regra de firewall existente em um servidor de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="91734-103">Modifies an existing firewall rule in an Azure SQL Database Server.</span></span>

## <span data-ttu-id="91734-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="91734-104">SYNTAX</span></span>

```
Set-AzureSqlDatabaseServerFirewallRule -ServerName <String> -RuleName <String> -StartIpAddress <String>
 -EndIpAddress <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91734-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="91734-105">DESCRIPTION</span></span>
<span data-ttu-id="91734-106">O cmdlet **set-AzureSqlDatabaseServerFirewallRule** modifica os valores do endereço IP inicial e do endereço IP final de uma regra de firewall existente na instância especificada do servidor de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="91734-106">The **Set-AzureSqlDatabaseServerFirewallRule** cmdlet modifies the start IP address and end IP address values of an existing firewall rule in the specified instance of Azure SQL Database Server.</span></span>

## <span data-ttu-id="91734-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="91734-107">EXAMPLES</span></span>

### <span data-ttu-id="91734-108">Exemplo 1: modificar uma regra de firewall</span><span class="sxs-lookup"><span data-stu-id="91734-108">Example 1: Modify a firewall rule</span></span>
```
PS C:\> Set-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y" -RuleName "FirewallRule24" -StartIpAddress 10.1.1.2 -EndIpAddress 10.1.1.4
```

<span data-ttu-id="91734-109">Esse comando modifica o endereço IP inicial e o endereço IP final da regra de firewall chamada FirewallRule24 no servidor de banco de dados SQL do Azure chamado lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="91734-109">This command modifies the start IP address and end IP address of the firewall rule named FirewallRule24 on the Azure SQL Database server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="91734-110">OS</span><span class="sxs-lookup"><span data-stu-id="91734-110">PARAMETERS</span></span>

### <span data-ttu-id="91734-111">-Endipaddress</span><span class="sxs-lookup"><span data-stu-id="91734-111">-EndIpAddress</span></span>
<span data-ttu-id="91734-112">Especifica o valor final do intervalo de endereços IP para esta regra.</span><span class="sxs-lookup"><span data-stu-id="91734-112">Specifies the end value of the IP address range for this rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91734-113">-Force</span><span class="sxs-lookup"><span data-stu-id="91734-113">-Force</span></span>
<span data-ttu-id="91734-114">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="91734-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="91734-115">-Perfil</span><span class="sxs-lookup"><span data-stu-id="91734-115">-Profile</span></span>
<span data-ttu-id="91734-116">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="91734-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="91734-117">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="91734-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="91734-118">-RuleName</span><span class="sxs-lookup"><span data-stu-id="91734-118">-RuleName</span></span>
<span data-ttu-id="91734-119">Especifica o nome da regra de firewall que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="91734-119">Specifies the name of the firewall rule that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="91734-120">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="91734-120">-ServerName</span></span>
<span data-ttu-id="91734-121">Especifica o nome de um servidor.</span><span class="sxs-lookup"><span data-stu-id="91734-121">Specifies the name of a server.</span></span>
<span data-ttu-id="91734-122">Esse cmdlet cria uma regra de firewall no servidor que esse cmdlet especifica.</span><span class="sxs-lookup"><span data-stu-id="91734-122">This cmdlet creates a firewall rule on the server that this cmdlet specifies.</span></span>
<span data-ttu-id="91734-123">Especifique o nome do servidor, não o nome DNS totalmente qualificado.</span><span class="sxs-lookup"><span data-stu-id="91734-123">Specify the server name, not the fully qualified DNS name.</span></span>

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

### <span data-ttu-id="91734-124">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="91734-124">-StartIpAddress</span></span>
<span data-ttu-id="91734-125">Especifica o valor inicial do intervalo de endereços IP para a regra de firewall.</span><span class="sxs-lookup"><span data-stu-id="91734-125">Specifies the start value of the IP address range for the firewall rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91734-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="91734-126">-Confirm</span></span>
<span data-ttu-id="91734-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="91734-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91734-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91734-128">-WhatIf</span></span>
<span data-ttu-id="91734-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="91734-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91734-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="91734-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91734-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91734-131">CommonParameters</span></span>
<span data-ttu-id="91734-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91734-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91734-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91734-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91734-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="91734-134">INPUTS</span></span>

### <span data-ttu-id="91734-135">Microsoft. WindowsAzure. Commands. SQLDatabase. Model. SqlDatabaseServerFirewallRuleContext</span><span class="sxs-lookup"><span data-stu-id="91734-135">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerFirewallRuleContext</span></span>

## <span data-ttu-id="91734-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="91734-136">OUTPUTS</span></span>

### <span data-ttu-id="91734-137">Microsoft. WindowsAzure. Commands. SQLDatabase. Model. SqlDatabaseServerFirewallRuleContext</span><span class="sxs-lookup"><span data-stu-id="91734-137">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerFirewallRuleContext</span></span>

## <span data-ttu-id="91734-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="91734-138">NOTES</span></span>

## <span data-ttu-id="91734-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="91734-139">RELATED LINKS</span></span>

[<span data-ttu-id="91734-140">Banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="91734-140">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="91734-141">Operações para bancos de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="91734-141">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="91734-142">Definir regra de firewall</span><span class="sxs-lookup"><span data-stu-id="91734-142">Set Firewall Rule</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505707.aspx)

[<span data-ttu-id="91734-143">Get-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="91734-143">Get-AzureSqlDatabaseServerFirewallRule</span></span>](./Get-AzureSqlDatabaseServerFirewallRule.md)

[<span data-ttu-id="91734-144">New-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="91734-144">New-AzureSqlDatabaseServerFirewallRule</span></span>](./New-AzureSqlDatabaseServerFirewallRule.md)

[<span data-ttu-id="91734-145">Remove-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="91734-145">Remove-AzureSqlDatabaseServerFirewallRule</span></span>](./Remove-AzureSqlDatabaseServerFirewallRule.md)


