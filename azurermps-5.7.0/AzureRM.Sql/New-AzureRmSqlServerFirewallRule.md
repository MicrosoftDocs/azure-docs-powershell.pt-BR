---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 51AF8EFB-F0C1-41E0-BBC5-E48FB1B8672C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerFirewallRule.md
ms.openlocfilehash: cc0d7163b9251037f4127d8fc6894f74f103436b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431560"
---
# <span data-ttu-id="87069-101">New-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="87069-101">New-AzureRmSqlServerFirewallRule</span></span>

## <span data-ttu-id="87069-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="87069-102">SYNOPSIS</span></span>
<span data-ttu-id="87069-103">Cria uma regra de firewall para um servidor de banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="87069-103">Creates a firewall rule for a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="87069-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="87069-104">SYNTAX</span></span>

### <span data-ttu-id="87069-105">UserSpecifiedRuleSet</span><span class="sxs-lookup"><span data-stu-id="87069-105">UserSpecifiedRuleSet</span></span>
```
New-AzureRmSqlServerFirewallRule -FirewallRuleName <String> -StartIpAddress <String> -EndIpAddress <String>
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87069-106">AzureIpRuleSet</span><span class="sxs-lookup"><span data-stu-id="87069-106">AzureIpRuleSet</span></span>
```
New-AzureRmSqlServerFirewallRule [-AllowAllAzureIPs] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87069-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="87069-107">DESCRIPTION</span></span>
<span data-ttu-id="87069-108">O cmdlet **New-AzureRmSqlServerFirewallRule** cria uma regra de firewall para o servidor de banco de dados SQL do Azure especificado.</span><span class="sxs-lookup"><span data-stu-id="87069-108">The **New-AzureRmSqlServerFirewallRule** cmdlet creates a firewall rule for the specified Azure SQL Database server.</span></span>

## <span data-ttu-id="87069-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="87069-109">EXAMPLES</span></span>

### <span data-ttu-id="87069-110">Exemplo 1: criar uma regra de firewall</span><span class="sxs-lookup"><span data-stu-id="87069-110">Example 1: Create a firewall rule</span></span>
```
PS C:\>New-AzureRmSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -FirewallRuleName "Rule01" -StartIpAddress "192.168.0.198" -EndIpAddress "192.168.0.199"
ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 192.168.0.198
EndIpAddress      : 192.168.0.199
FirewallRuleName  : Rule01
```

<span data-ttu-id="87069-111">Esse comando cria uma regra de firewall chamada Rule01 no servidor chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="87069-111">This command creates a firewall rule named Rule01 on the server named Server01.</span></span>
<span data-ttu-id="87069-112">A regra inclui os endereços IP de início e término especificados.</span><span class="sxs-lookup"><span data-stu-id="87069-112">The rule includes the specified start and end IP addresses.</span></span>

### <span data-ttu-id="87069-113">Exemplo 2: criar uma regra de firewall que permita que todos os endereços IP do Azure acessem o servidor</span><span class="sxs-lookup"><span data-stu-id="87069-113">Example 2: Create a firewall rule that allows all Azure IP addresses to access the server</span></span>
```
PS C:\>New-AzureRmSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -AllowAllAzureIPs
```

<span data-ttu-id="87069-114">Esse comando cria uma regra de firewall no servidor chamado Server01 que pertence ao grupo de recursos chamado ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="87069-114">This command creates a firewall rule on the server named Server01 that belongs to the resource group named ResourceGroup01.</span></span>
<span data-ttu-id="87069-115">Como o parâmetro *AllowAllAzureIPs* é usado, a regra de firewall permite que todos os endereços IP do Azure acessem o servidor.</span><span class="sxs-lookup"><span data-stu-id="87069-115">Since the *AllowAllAzureIPs* parameter is used, the firewall rule allows all Azure IP addresses to access the server.</span></span>

## <span data-ttu-id="87069-116">OS</span><span class="sxs-lookup"><span data-stu-id="87069-116">PARAMETERS</span></span>

### <span data-ttu-id="87069-117">-AllowAllAzureIPs</span><span class="sxs-lookup"><span data-stu-id="87069-117">-AllowAllAzureIPs</span></span>
<span data-ttu-id="87069-118">Indica que essa regra de firewall permite que todos os endereços IP do Azure acessem o servidor.</span><span class="sxs-lookup"><span data-stu-id="87069-118">Indicates that this firewall rule allows all Azure IP addresses to access the server.</span></span>
<span data-ttu-id="87069-119">Não é possível usar esse parâmetro se você pretende usar os parâmetros *FirewallRuleName* , *StartIpAddress* e *endipaddress* .</span><span class="sxs-lookup"><span data-stu-id="87069-119">You cannot use this parameter if you intend to use the *FirewallRuleName* , *StartIpAddress* , and *EndIpAddress* parameters.</span></span>
<span data-ttu-id="87069-120">Se você quiser permitir que o IPs do Azure acesse o servidor, esse parâmetro deve ser usado em uma chamada de cmdlet separada que não use os parâmetros *FirewallRuleName* , *StartIpAddress* e *endipaddress* .</span><span class="sxs-lookup"><span data-stu-id="87069-120">If you want to allow Azure IPs to access the server, this parameter should be used in a separate cmdlet call that does not use the *FirewallRuleName* , *StartIpAddress* , and *EndIpAddress* parameters.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AzureIpRuleSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87069-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87069-121">-DefaultProfile</span></span>
<span data-ttu-id="87069-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="87069-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="87069-123">-Endipaddress</span><span class="sxs-lookup"><span data-stu-id="87069-123">-EndIpAddress</span></span>
<span data-ttu-id="87069-124">Especifica o valor final do intervalo de endereços IP para esta regra.</span><span class="sxs-lookup"><span data-stu-id="87069-124">Specifies the end value of the IP address range for this rule.</span></span>

```yaml
Type: String
Parameter Sets: UserSpecifiedRuleSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87069-125">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="87069-125">-FirewallRuleName</span></span>
<span data-ttu-id="87069-126">Especifica o nome da nova regra de firewall.</span><span class="sxs-lookup"><span data-stu-id="87069-126">Specifies the name of the new firewall rule.</span></span>

```yaml
Type: String
Parameter Sets: UserSpecifiedRuleSet
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87069-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87069-127">-ResourceGroupName</span></span>
<span data-ttu-id="87069-128">Especifica o nome de um grupo de recursos ao qual o servidor está atribuído.</span><span class="sxs-lookup"><span data-stu-id="87069-128">Specifies the name of a resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="87069-129">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="87069-129">-ServerName</span></span>
<span data-ttu-id="87069-130">Especifica o nome de um servidor.</span><span class="sxs-lookup"><span data-stu-id="87069-130">Specifies the name of a server.</span></span>
<span data-ttu-id="87069-131">Especifique o nome do servidor, não o nome DNS totalmente qualificado.</span><span class="sxs-lookup"><span data-stu-id="87069-131">Specify the server name, not the fully qualified DNS name.</span></span>

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

### <span data-ttu-id="87069-132">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="87069-132">-StartIpAddress</span></span>
<span data-ttu-id="87069-133">Especifica o valor inicial do intervalo de endereços IP para a regra de firewall.</span><span class="sxs-lookup"><span data-stu-id="87069-133">Specifies the start value of the IP address range for the firewall rule.</span></span>

```yaml
Type: String
Parameter Sets: UserSpecifiedRuleSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87069-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="87069-134">-Confirm</span></span>
<span data-ttu-id="87069-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87069-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87069-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87069-136">-WhatIf</span></span>
<span data-ttu-id="87069-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="87069-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87069-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="87069-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87069-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87069-139">CommonParameters</span></span>
<span data-ttu-id="87069-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87069-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87069-141">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87069-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87069-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="87069-142">INPUTS</span></span>

### <span data-ttu-id="87069-143">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="87069-143">None</span></span>
<span data-ttu-id="87069-144">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="87069-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="87069-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="87069-145">OUTPUTS</span></span>

### <span data-ttu-id="87069-146">Microsoft. Azure. Commands. Sql. FirewallRule. Model. AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="87069-146">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="87069-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="87069-147">NOTES</span></span>

## <span data-ttu-id="87069-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="87069-148">RELATED LINKS</span></span>

[<span data-ttu-id="87069-149">Get-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="87069-149">Get-AzureRmSqlServerFirewallRule</span></span>](./Get-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="87069-150">Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="87069-150">Remove-AzureRmSqlServerFirewallRule</span></span>](./Remove-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="87069-151">Set-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="87069-151">Set-AzureRmSqlServerFirewallRule</span></span>](./Set-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="87069-152">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="87069-152">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


