---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: AD8BA5CB-D5D4-4C6E-A65F-E7AE69E3B22C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerFirewallRule.md
ms.openlocfilehash: 27715ee03871c08c53380861e2cd54d843b2ba51
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609546"
---
# <span data-ttu-id="5687c-101">Get-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="5687c-101">Get-AzureRmSqlServerFirewallRule</span></span>

## <span data-ttu-id="5687c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5687c-102">SYNOPSIS</span></span>
<span data-ttu-id="5687c-103">Obtém regras de firewall para um servidor de banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="5687c-103">Gets firewall rules for a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5687c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5687c-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerFirewallRule [[-FirewallRuleName] <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5687c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5687c-105">DESCRIPTION</span></span>
<span data-ttu-id="5687c-106">O cmdlet **Get-AzureRmSqlServerFirewallRule** Obtém regras de firewall para um servidor de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="5687c-106">The **Get-AzureRmSqlServerFirewallRule** cmdlet gets firewall rules for an Azure SQL Database server.</span></span>
<span data-ttu-id="5687c-107">Se você especificar o nome de uma regra de firewall, esse cmdlet obterá informações sobre essa regra de firewall específica.</span><span class="sxs-lookup"><span data-stu-id="5687c-107">If you specify the name of a firewall rule, this cmdlet gets information about that specific firewall rule.</span></span>

## <span data-ttu-id="5687c-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5687c-108">EXAMPLES</span></span>

### <span data-ttu-id="5687c-109">Exemplo 1: obter todas as regras para um servidor</span><span class="sxs-lookup"><span data-stu-id="5687c-109">Example 1: Get all rules for a server</span></span>
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

<span data-ttu-id="5687c-110">Esse comando obtém todas as regras de firewall do servidor chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="5687c-110">This command gets all the firewall rules for the server named Server01.</span></span>

## <span data-ttu-id="5687c-111">OS</span><span class="sxs-lookup"><span data-stu-id="5687c-111">PARAMETERS</span></span>

### <span data-ttu-id="5687c-112">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="5687c-112">-FirewallRuleName</span></span>
<span data-ttu-id="5687c-113">Especifica o nome da regra de firewall.</span><span class="sxs-lookup"><span data-stu-id="5687c-113">Specifies the name of the firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5687c-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5687c-114">-ResourceGroupName</span></span>
<span data-ttu-id="5687c-115">Especifica o nome do grupo de recursos ao qual o SQL Server está atribuído.</span><span class="sxs-lookup"><span data-stu-id="5687c-115">Specifies the name of the resource group to which the SQL Server is assigned.</span></span>

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

### <span data-ttu-id="5687c-116">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="5687c-116">-ServerName</span></span>
<span data-ttu-id="5687c-117">Especifica o nome do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="5687c-117">Specifies the name of the SQL Server.</span></span>

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

### <span data-ttu-id="5687c-118">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5687c-118">-Confirm</span></span>
<span data-ttu-id="5687c-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5687c-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5687c-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5687c-120">-WhatIf</span></span>
<span data-ttu-id="5687c-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5687c-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5687c-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5687c-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5687c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5687c-123">-DefaultProfile</span></span>
<span data-ttu-id="5687c-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5687c-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5687c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5687c-125">CommonParameters</span></span>
<span data-ttu-id="5687c-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5687c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5687c-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5687c-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5687c-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5687c-128">INPUTS</span></span>

## <span data-ttu-id="5687c-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5687c-129">OUTPUTS</span></span>

### <span data-ttu-id="5687c-130">Microsoft. Azure. Commands. Sql. FirewallRule. Model. AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="5687c-130">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="5687c-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5687c-131">NOTES</span></span>

## <span data-ttu-id="5687c-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5687c-132">RELATED LINKS</span></span>

[<span data-ttu-id="5687c-133">New-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="5687c-133">New-AzureRmSqlServerFirewallRule</span></span>](./New-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="5687c-134">Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="5687c-134">Remove-AzureRmSqlServerFirewallRule</span></span>](./Remove-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="5687c-135">Set-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="5687c-135">Set-AzureRmSqlServerFirewallRule</span></span>](./Set-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="5687c-136">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="5687c-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


