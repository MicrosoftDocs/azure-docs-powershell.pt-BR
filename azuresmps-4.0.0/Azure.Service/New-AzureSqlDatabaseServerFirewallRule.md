---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: A723D12D-DCF5-4F0C-AAC2-8BADFBAC3328
online version: ''
schema: 2.0.0
ms.openlocfilehash: a0383e451d8346d4b6465390cc78850b270f6ac3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945969"
---
# <span data-ttu-id="d9782-101">New-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d9782-101">New-AzureSqlDatabaseServerFirewallRule</span></span>

## <span data-ttu-id="d9782-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d9782-102">SYNOPSIS</span></span>
<span data-ttu-id="d9782-103">Cria uma regra de firewall no servidor de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="d9782-103">Creates a firewall rule in Azure SQL Database Server.</span></span>

## <span data-ttu-id="d9782-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d9782-104">SYNTAX</span></span>

### <span data-ttu-id="d9782-105">IpRange (padrão)</span><span class="sxs-lookup"><span data-stu-id="d9782-105">IpRange (Default)</span></span>
```
New-AzureSqlDatabaseServerFirewallRule -ServerName <String> -RuleName <String> -StartIpAddress <String>
 -EndIpAddress <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9782-106">AllowAllAzureServices</span><span class="sxs-lookup"><span data-stu-id="d9782-106">AllowAllAzureServices</span></span>
```
New-AzureSqlDatabaseServerFirewallRule -ServerName <String> [-RuleName <String>] [-AllowAllAzureServices]
 [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9782-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d9782-107">DESCRIPTION</span></span>
<span data-ttu-id="d9782-108">O cmdlet **New-AzureSqlDatabaseServerFirewallRule** cria uma regra de firewall na instância especificada do servidor de banco de dados SQL do Azure na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="d9782-108">The **New-AzureSqlDatabaseServerFirewallRule** cmdlet creates a firewall rule in the specified instance of Azure SQL Database Server in the current subscription.</span></span>

<span data-ttu-id="d9782-109">Use os parâmetros *StartIpAddress* e *endipaddress* para especificar um intervalo de endereços IP que essa regra permite para se conectar ao servidor de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="d9782-109">Use the *StartIpAddress* and *EndIpAddress* parameters to specify a range of IP addresses that this rule allows to connect to the Azure SQL Database server.</span></span>

<span data-ttu-id="d9782-110">Especifique o parâmetro *AllowAllAzureServices* para criar uma regra que permita a conexão do Azure com o servidor.</span><span class="sxs-lookup"><span data-stu-id="d9782-110">Specify the *AllowAllAzureServices* parameter to create a rule that allows Azure connections to the server.</span></span>
<span data-ttu-id="d9782-111">A regra tem valores de endereço IP inicial e final de 0.0.0.0.</span><span class="sxs-lookup"><span data-stu-id="d9782-111">The rule has starting and ending IP address values of 0.0.0.0.</span></span>
<span data-ttu-id="d9782-112">Se você não especificar um nome de regra de firewall, esse cmdlet atribuirá o nome padrão AllowAllAzureServices.</span><span class="sxs-lookup"><span data-stu-id="d9782-112">If you do not specify a firewall rule name, this cmdlet assigns the default name AllowAllAzureServices.</span></span>

## <span data-ttu-id="d9782-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d9782-113">EXAMPLES</span></span>

### <span data-ttu-id="d9782-114">Exemplo 1: criar uma regra de firewall</span><span class="sxs-lookup"><span data-stu-id="d9782-114">Example 1: Create a firewall rule</span></span>
```
PS C:\>New-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y" -RuleName "FirewallRule24" -StartIpAddress 10.1.1.1 -EndIpAddress 10.1.1.2
```

<span data-ttu-id="d9782-115">Esse comando cria uma regra de firewall FirewallRule24 no servidor de banco de dados SQL do Azure chamado lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="d9782-115">This command creates a firewall rule FirewallRule24 on the Azure SQL Database server named lpqd0zbr8y.</span></span>
<span data-ttu-id="d9782-116">O comando especifica um intervalo de endereços IP.</span><span class="sxs-lookup"><span data-stu-id="d9782-116">The command specifies an IP address range.</span></span>

### <span data-ttu-id="d9782-117">Exemplo 2: criar uma regra que permita todos os serviços do Azure</span><span class="sxs-lookup"><span data-stu-id="d9782-117">Example 2: Create a rule that allows all Azure services</span></span>
```
PS C:\>New-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y" -AllowAllAzureServices -RuleName "AzureConnections"
```

<span data-ttu-id="d9782-118">Esse comando cria uma regra de firewall chamada AzureConnections no servidor chamado lpqd0zbr8y que permite conexões do Azure.</span><span class="sxs-lookup"><span data-stu-id="d9782-118">This command creates a firewall rule named AzureConnections on the server named lpqd0zbr8y that allows Azure connections.</span></span>

### <span data-ttu-id="d9782-119">Exemplo 3: criar uma regra que permita que todos os serviços do Azure que usam o nome padrão criem uma regra que permita todos os serviços do Azure que usam o nome padrão</span><span class="sxs-lookup"><span data-stu-id="d9782-119">Example 3: Create a rule that allows all Azure services that uses the default name Create a rule that allows all Azure services that uses the default name</span></span>
```
PS C:\>New-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y" -AllowAllAzureServices
```

<span data-ttu-id="d9782-120">Esse comando cria uma regra de firewall no servidor especificado chamado lpqd0zbr8y, que permite conexões do Azure.</span><span class="sxs-lookup"><span data-stu-id="d9782-120">This command creates a firewall rule on the specified server named lpqd0zbr8y that allows Azure connections.</span></span>
<span data-ttu-id="d9782-121">O comando atribui o nome de regra padrão AllowAllAzureServices.</span><span class="sxs-lookup"><span data-stu-id="d9782-121">The command assigns the default rule name AllowAllAzureServices.</span></span>

## <span data-ttu-id="d9782-122">OS</span><span class="sxs-lookup"><span data-stu-id="d9782-122">PARAMETERS</span></span>

### <span data-ttu-id="d9782-123">-AllowAllAzureServices</span><span class="sxs-lookup"><span data-stu-id="d9782-123">-AllowAllAzureServices</span></span>
<span data-ttu-id="d9782-124">Indica que essa regra de firewall permite que todos os endereços IP do Azure acessem o servidor.</span><span class="sxs-lookup"><span data-stu-id="d9782-124">Indicates that this firewall rule enables all Azure IP addresses to access the server.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AllowAllAzureServices
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9782-125">-Endipaddress</span><span class="sxs-lookup"><span data-stu-id="d9782-125">-EndIpAddress</span></span>
<span data-ttu-id="d9782-126">Especifica o valor final do intervalo de endereços IP para esta regra.</span><span class="sxs-lookup"><span data-stu-id="d9782-126">Specifies the end value of the IP address range for this rule.</span></span>

```yaml
Type: String
Parameter Sets: IpRange
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9782-127">-Force</span><span class="sxs-lookup"><span data-stu-id="d9782-127">-Force</span></span>
<span data-ttu-id="d9782-128">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="d9782-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d9782-129">-Perfil</span><span class="sxs-lookup"><span data-stu-id="d9782-129">-Profile</span></span>
<span data-ttu-id="d9782-130">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="d9782-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d9782-131">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="d9782-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d9782-132">-RuleName</span><span class="sxs-lookup"><span data-stu-id="d9782-132">-RuleName</span></span>
<span data-ttu-id="d9782-133">Especifica o nome da nova regra de firewall.</span><span class="sxs-lookup"><span data-stu-id="d9782-133">Specifies the name of the new firewall rule.</span></span>

```yaml
Type: String
Parameter Sets: IpRange
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: AllowAllAzureServices
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9782-134">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="d9782-134">-ServerName</span></span>
<span data-ttu-id="d9782-135">Especifica o nome de um servidor.</span><span class="sxs-lookup"><span data-stu-id="d9782-135">Specifies the name of a server.</span></span>
<span data-ttu-id="d9782-136">Esse cmdlet cria uma regra de firewall no servidor que esse cmdlet especifica.</span><span class="sxs-lookup"><span data-stu-id="d9782-136">This cmdlet creates a firewall rule on the server that this cmdlet specifies.</span></span>
<span data-ttu-id="d9782-137">Especifique o nome do servidor, não o nome DNS totalmente qualificado.</span><span class="sxs-lookup"><span data-stu-id="d9782-137">Specify the server name, not the fully qualified DNS name.</span></span>

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

### <span data-ttu-id="d9782-138">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="d9782-138">-StartIpAddress</span></span>
<span data-ttu-id="d9782-139">Especifica o valor inicial do intervalo de endereços IP para a regra de firewall.</span><span class="sxs-lookup"><span data-stu-id="d9782-139">Specifies the start value of the IP address range for the firewall rule.</span></span>

```yaml
Type: String
Parameter Sets: IpRange
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9782-140">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d9782-140">-Confirm</span></span>
<span data-ttu-id="d9782-141">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d9782-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9782-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9782-142">-WhatIf</span></span>
<span data-ttu-id="d9782-143">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d9782-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9782-144">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d9782-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9782-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9782-145">CommonParameters</span></span>
<span data-ttu-id="d9782-146">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9782-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9782-147">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9782-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9782-148">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d9782-148">INPUTS</span></span>

## <span data-ttu-id="d9782-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d9782-149">OUTPUTS</span></span>

### <span data-ttu-id="d9782-150">Microsoft. WindowsAzure. Commands. SQLDatabase. Model. SqlDatabaseServerFirewallRuleContext</span><span class="sxs-lookup"><span data-stu-id="d9782-150">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerFirewallRuleContext</span></span>

## <span data-ttu-id="d9782-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d9782-151">NOTES</span></span>

## <span data-ttu-id="d9782-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d9782-152">RELATED LINKS</span></span>

[<span data-ttu-id="d9782-153">Banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="d9782-153">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="d9782-154">Criar regra de firewall</span><span class="sxs-lookup"><span data-stu-id="d9782-154">Create Firewall Rule</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505712.aspx)

[<span data-ttu-id="d9782-155">Operações para bancos de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="d9782-155">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="d9782-156">Get-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d9782-156">Get-AzureSqlDatabaseServerFirewallRule</span></span>](./Get-AzureSqlDatabaseServerFirewallRule.md)

[<span data-ttu-id="d9782-157">Remove-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d9782-157">Remove-AzureSqlDatabaseServerFirewallRule</span></span>](./Remove-AzureSqlDatabaseServerFirewallRule.md)

[<span data-ttu-id="d9782-158">Set-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d9782-158">Set-AzureSqlDatabaseServerFirewallRule</span></span>](./Set-AzureSqlDatabaseServerFirewallRule.md)


