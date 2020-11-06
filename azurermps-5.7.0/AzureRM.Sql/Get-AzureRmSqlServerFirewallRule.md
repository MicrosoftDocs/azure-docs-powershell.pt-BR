---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: AD8BA5CB-D5D4-4C6E-A65F-E7AE69E3B22C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerFirewallRule.md
ms.openlocfilehash: eb514075bd366a0360f29c65455805be5f85569f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426564"
---
# <span data-ttu-id="ad6fb-101">Get-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ad6fb-101">Get-AzureRmSqlServerFirewallRule</span></span>

## <span data-ttu-id="ad6fb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ad6fb-102">SYNOPSIS</span></span>
<span data-ttu-id="ad6fb-103">Obtém regras de firewall para um servidor de banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="ad6fb-103">Gets firewall rules for a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad6fb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ad6fb-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerFirewallRule [[-FirewallRuleName] <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ad6fb-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ad6fb-105">DESCRIPTION</span></span>
<span data-ttu-id="ad6fb-106">O cmdlet **Get-AzureRmSqlServerFirewallRule** Obtém regras de firewall para um servidor de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="ad6fb-106">The **Get-AzureRmSqlServerFirewallRule** cmdlet gets firewall rules for an Azure SQL Database server.</span></span>
<span data-ttu-id="ad6fb-107">Se você especificar o nome de uma regra de firewall, esse cmdlet obterá informações sobre essa regra de firewall específica.</span><span class="sxs-lookup"><span data-stu-id="ad6fb-107">If you specify the name of a firewall rule, this cmdlet gets information about that specific firewall rule.</span></span>

## <span data-ttu-id="ad6fb-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ad6fb-108">EXAMPLES</span></span>

### <span data-ttu-id="ad6fb-109">Exemplo 1: obter todas as regras para um servidor</span><span class="sxs-lookup"><span data-stu-id="ad6fb-109">Example 1: Get all rules for a server</span></span>
```
PS C:\>Get-AzureRmSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
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

<span data-ttu-id="ad6fb-110">Esse comando obtém todas as regras de firewall do servidor chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="ad6fb-110">This command gets all the firewall rules for the server named Server01.</span></span>

## <span data-ttu-id="ad6fb-111">OS</span><span class="sxs-lookup"><span data-stu-id="ad6fb-111">PARAMETERS</span></span>

### <span data-ttu-id="ad6fb-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad6fb-112">-DefaultProfile</span></span>
<span data-ttu-id="ad6fb-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="ad6fb-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ad6fb-114">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="ad6fb-114">-FirewallRuleName</span></span>
<span data-ttu-id="ad6fb-115">Especifica o nome da regra de firewall.</span><span class="sxs-lookup"><span data-stu-id="ad6fb-115">Specifies the name of the firewall rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad6fb-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad6fb-116">-ResourceGroupName</span></span>
<span data-ttu-id="ad6fb-117">Especifica o nome do grupo de recursos ao qual o SQL Server está atribuído.</span><span class="sxs-lookup"><span data-stu-id="ad6fb-117">Specifies the name of the resource group to which the SQL Server is assigned.</span></span>

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

### <span data-ttu-id="ad6fb-118">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="ad6fb-118">-ServerName</span></span>
<span data-ttu-id="ad6fb-119">Especifica o nome do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ad6fb-119">Specifies the name of the SQL Server.</span></span>

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

### <span data-ttu-id="ad6fb-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ad6fb-120">-Confirm</span></span>
<span data-ttu-id="ad6fb-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad6fb-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad6fb-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad6fb-122">-WhatIf</span></span>
<span data-ttu-id="ad6fb-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ad6fb-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad6fb-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ad6fb-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad6fb-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad6fb-125">CommonParameters</span></span>
<span data-ttu-id="ad6fb-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad6fb-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad6fb-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad6fb-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad6fb-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ad6fb-128">INPUTS</span></span>

### <span data-ttu-id="ad6fb-129">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="ad6fb-129">None</span></span>
<span data-ttu-id="ad6fb-130">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="ad6fb-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ad6fb-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ad6fb-131">OUTPUTS</span></span>

### <span data-ttu-id="ad6fb-132">Microsoft. Azure. Commands. Sql. FirewallRule. Model. AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="ad6fb-132">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="ad6fb-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ad6fb-133">NOTES</span></span>

## <span data-ttu-id="ad6fb-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ad6fb-134">RELATED LINKS</span></span>

[<span data-ttu-id="ad6fb-135">New-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ad6fb-135">New-AzureRmSqlServerFirewallRule</span></span>](./New-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="ad6fb-136">Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ad6fb-136">Remove-AzureRmSqlServerFirewallRule</span></span>](./Remove-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="ad6fb-137">Set-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ad6fb-137">Set-AzureRmSqlServerFirewallRule</span></span>](./Set-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="ad6fb-138">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="ad6fb-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


