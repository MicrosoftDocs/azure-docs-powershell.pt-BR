---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: B407CF77-792B-40F8-87AB-49FB3DCEE646
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerFirewallRule.md
ms.openlocfilehash: e0957e7c68a2332cbd50bbc42d703c41bb277b75
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427412"
---
# <span data-ttu-id="fdcca-101">Set-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="fdcca-101">Set-AzureRmSqlServerFirewallRule</span></span>

## <span data-ttu-id="fdcca-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fdcca-102">SYNOPSIS</span></span>
<span data-ttu-id="fdcca-103">Modifica uma regra de firewall no servidor de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="fdcca-103">Modifies a firewall rule in Azure SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fdcca-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fdcca-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerFirewallRule [-FirewallRuleName] <String> -StartIpAddress <String> -EndIpAddress <String>
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fdcca-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fdcca-105">DESCRIPTION</span></span>
<span data-ttu-id="fdcca-106">O cmdlet **set-AzureRmSqlServerFirewallRule** modifica uma regra de firewall em um servidor de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="fdcca-106">The **Set-AzureRmSqlServerFirewallRule** cmdlet modifies a firewall rule in an Azure SQL Database server.</span></span>

## <span data-ttu-id="fdcca-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fdcca-107">EXAMPLES</span></span>

### <span data-ttu-id="fdcca-108">Exemplo 1: modificar uma regra de firewall</span><span class="sxs-lookup"><span data-stu-id="fdcca-108">Example 1: Modify a firewall rule</span></span>
```
PS C:\>Set-AzureRmSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -FirewallRuleName "Rule01" -StartIpAddress "192.168.0.197" -EndIpAddress "192.168.0.199"
ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 192.168.0.199
EndIpAddress      : 192.168.0.200
FirewallRuleName  : Rule01
```

<span data-ttu-id="fdcca-109">Esse comando modifica uma regra de firewall chamada Rule01 no servidor chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="fdcca-109">This command modifies a firewall rule named Rule01 on the server named Server01.</span></span>
<span data-ttu-id="fdcca-110">O comando modifica os endereços IP de início e término.</span><span class="sxs-lookup"><span data-stu-id="fdcca-110">The command modifies the start and end IP addresses.</span></span>

## <span data-ttu-id="fdcca-111">OS</span><span class="sxs-lookup"><span data-stu-id="fdcca-111">PARAMETERS</span></span>

### <span data-ttu-id="fdcca-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdcca-112">-DefaultProfile</span></span>
<span data-ttu-id="fdcca-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="fdcca-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fdcca-114">-Endipaddress</span><span class="sxs-lookup"><span data-stu-id="fdcca-114">-EndIpAddress</span></span>
<span data-ttu-id="fdcca-115">Especifica o valor final do intervalo de endereços IP para esta regra.</span><span class="sxs-lookup"><span data-stu-id="fdcca-115">Specifies the end value of the IP address range for this rule.</span></span>

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

### <span data-ttu-id="fdcca-116">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="fdcca-116">-FirewallRuleName</span></span>
<span data-ttu-id="fdcca-117">Especifica o nome da regra de firewall que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="fdcca-117">Specifies the name of the firewall rule that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="fdcca-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fdcca-118">-ResourceGroupName</span></span>
<span data-ttu-id="fdcca-119">Especifica o nome do grupo de recursos ao qual o servidor está atribuído.</span><span class="sxs-lookup"><span data-stu-id="fdcca-119">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="fdcca-120">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="fdcca-120">-ServerName</span></span>
<span data-ttu-id="fdcca-121">Especifica o nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="fdcca-121">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="fdcca-122">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="fdcca-122">-StartIpAddress</span></span>
<span data-ttu-id="fdcca-123">Especifica o valor inicial do intervalo de endereços IP para a regra de firewall.</span><span class="sxs-lookup"><span data-stu-id="fdcca-123">Specifies the start value of the IP address range for the firewall rule.</span></span>

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

### <span data-ttu-id="fdcca-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="fdcca-124">-Confirm</span></span>
<span data-ttu-id="fdcca-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fdcca-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fdcca-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fdcca-126">-WhatIf</span></span>
<span data-ttu-id="fdcca-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fdcca-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fdcca-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fdcca-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fdcca-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdcca-129">CommonParameters</span></span>
<span data-ttu-id="fdcca-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fdcca-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdcca-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fdcca-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdcca-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fdcca-132">INPUTS</span></span>

### <span data-ttu-id="fdcca-133">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="fdcca-133">None</span></span>
<span data-ttu-id="fdcca-134">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="fdcca-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fdcca-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fdcca-135">OUTPUTS</span></span>

### <span data-ttu-id="fdcca-136">Microsoft. Azure. Commands. Sql. FirewallRule. Model. AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="fdcca-136">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="fdcca-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fdcca-137">NOTES</span></span>

## <span data-ttu-id="fdcca-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fdcca-138">RELATED LINKS</span></span>

[<span data-ttu-id="fdcca-139">Get-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="fdcca-139">Get-AzureRmSqlServerFirewallRule</span></span>](./Get-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="fdcca-140">New-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="fdcca-140">New-AzureRmSqlServerFirewallRule</span></span>](./New-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="fdcca-141">Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="fdcca-141">Remove-AzureRmSqlServerFirewallRule</span></span>](./Remove-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="fdcca-142">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="fdcca-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


