---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: BE00A25D-3ECE-4B27-9D79-78128CFEBDB0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 100202df1871610aff3af1fe90bb7d603c141d62
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945572"
---
# <span data-ttu-id="ed218-101">Get-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ed218-101">Get-AzureSqlDatabaseServerFirewallRule</span></span>

## <span data-ttu-id="ed218-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ed218-102">SYNOPSIS</span></span>
<span data-ttu-id="ed218-103">Obtém regras de firewall para o servidor do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="ed218-103">Gets firewall rules for Azure SQL Database Server.</span></span>

## <span data-ttu-id="ed218-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ed218-104">SYNTAX</span></span>

```
Get-AzureSqlDatabaseServerFirewallRule -ServerName <String> [-RuleName <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="ed218-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ed218-105">DESCRIPTION</span></span>
<span data-ttu-id="ed218-106">O cmdlet **Get-AzureSqlDatabaseServerFirewallRule** Obtém regras de firewall para uma instância do servidor de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="ed218-106">The **Get-AzureSqlDatabaseServerFirewallRule** cmdlet gets firewall rules for an instance of Azure SQL Database Server.</span></span>
<span data-ttu-id="ed218-107">Se você especificar uma regra de firewall por nome, esse cmdlet retornará informações sobre essa regra de firewall.</span><span class="sxs-lookup"><span data-stu-id="ed218-107">If you specify a firewall rule by name, this cmdlet returns information about that firewall rule.</span></span>
<span data-ttu-id="ed218-108">Caso contrário, o cmdlet retorna informações sobre todas as regras de firewall no servidor de banco de dados SQL do Azure especificado.</span><span class="sxs-lookup"><span data-stu-id="ed218-108">Otherwise, the cmdlet returns information about all the firewall rules on the specified Azure SQL Database server.</span></span>

## <span data-ttu-id="ed218-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ed218-109">EXAMPLES</span></span>

### <span data-ttu-id="ed218-110">Exemplo 1: obter todas as regras de firewall em um servidor</span><span class="sxs-lookup"><span data-stu-id="ed218-110">Example 1: Get all firewall rules on a server</span></span>
```
PS C:\> Get-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y"
```

<span data-ttu-id="ed218-111">Esse comando obtém todas as regras de firewall no servidor de banco de dados SQL do Azure chamado lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="ed218-111">This command gets all the firewall rules on the Azure SQL Database server named lpqd0zbr8y.</span></span>

### <span data-ttu-id="ed218-112">Exemplo 2: obter uma regra de firewall usando seu nome</span><span class="sxs-lookup"><span data-stu-id="ed218-112">Example 2: Get a firewall rule by using its name</span></span>
```
PS C:\> Get-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y" -RuleName "FirewallRule24"
```

<span data-ttu-id="ed218-113">Esse comando obtém a regra de firewall chamada FirewallRule24 no servidor chamado lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="ed218-113">This command gets the firewall rule named FirewallRule24 on the server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="ed218-114">OS</span><span class="sxs-lookup"><span data-stu-id="ed218-114">PARAMETERS</span></span>

### <span data-ttu-id="ed218-115">-Perfil</span><span class="sxs-lookup"><span data-stu-id="ed218-115">-Profile</span></span>
<span data-ttu-id="ed218-116">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="ed218-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ed218-117">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="ed218-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ed218-118">-RuleName</span><span class="sxs-lookup"><span data-stu-id="ed218-118">-RuleName</span></span>
<span data-ttu-id="ed218-119">Especifica o nome da regra de firewall que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="ed218-119">Specifies the name of the firewall rule that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed218-120">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="ed218-120">-ServerName</span></span>
<span data-ttu-id="ed218-121">Especifica o nome de um servidor.</span><span class="sxs-lookup"><span data-stu-id="ed218-121">Specifies the name of a server.</span></span>
<span data-ttu-id="ed218-122">Este cmdlet obtém regras de firewall do servidor que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="ed218-122">This cmdlet gets firewall rules from the server that this parameter specifies.</span></span>
<span data-ttu-id="ed218-123">Especifique o nome do servidor, não o nome DNS totalmente qualificado.</span><span class="sxs-lookup"><span data-stu-id="ed218-123">Specify the server name, not the fully qualified DNS name.</span></span>

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

### <span data-ttu-id="ed218-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed218-124">CommonParameters</span></span>
<span data-ttu-id="ed218-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed218-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed218-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed218-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed218-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ed218-127">INPUTS</span></span>

### <span data-ttu-id="ed218-128">Microsoft. WindowsAzure. Commands. SQLDatabase. Model. SqlDatabaseServerFirewallRuleContext</span><span class="sxs-lookup"><span data-stu-id="ed218-128">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerFirewallRuleContext</span></span>

## <span data-ttu-id="ed218-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ed218-129">OUTPUTS</span></span>

### <span data-ttu-id="ed218-130">IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerFirewallRuleContext\></span><span class="sxs-lookup"><span data-stu-id="ed218-130">IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerFirewallRuleContext\></span></span>

## <span data-ttu-id="ed218-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ed218-131">NOTES</span></span>

## <span data-ttu-id="ed218-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ed218-132">RELATED LINKS</span></span>

[<span data-ttu-id="ed218-133">Banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="ed218-133">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="ed218-134">Regras de firewall de lista</span><span class="sxs-lookup"><span data-stu-id="ed218-134">List Firewall Rules</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505715.aspx)

[<span data-ttu-id="ed218-135">Operações para bancos de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="ed218-135">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="ed218-136">New-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ed218-136">New-AzureSqlDatabaseServerFirewallRule</span></span>](./New-AzureSqlDatabaseServerFirewallRule.md)

[<span data-ttu-id="ed218-137">Remove-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ed218-137">Remove-AzureSqlDatabaseServerFirewallRule</span></span>](./Remove-AzureSqlDatabaseServerFirewallRule.md)

[<span data-ttu-id="ed218-138">Set-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ed218-138">Set-AzureSqlDatabaseServerFirewallRule</span></span>](./Set-AzureSqlDatabaseServerFirewallRule.md)


