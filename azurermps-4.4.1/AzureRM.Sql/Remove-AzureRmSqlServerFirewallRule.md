---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 251A4546-AC23-4880-B197-773B1B814607
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerFirewallRule.md
ms.openlocfilehash: 1f7f039bb0bba1338fdcc4d5ceb3a403822fba71
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427741"
---
# <span data-ttu-id="eec50-101">Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="eec50-101">Remove-AzureRmSqlServerFirewallRule</span></span>

## <span data-ttu-id="eec50-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="eec50-102">SYNOPSIS</span></span>
<span data-ttu-id="eec50-103">Exclui uma regra de firewall de um servidor de banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="eec50-103">Deletes a firewall rule from a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eec50-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="eec50-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerFirewallRule [-FirewallRuleName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="eec50-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="eec50-105">DESCRIPTION</span></span>
<span data-ttu-id="eec50-106">O cmdlet **Remove-AzureRmSqlServerFirewallRule** exclui uma regra de firewall do servidor de banco de dados SQL do Azure especificado.</span><span class="sxs-lookup"><span data-stu-id="eec50-106">The **Remove-AzureRmSqlServerFirewallRule** cmdlet deletes a firewall rule from the specified Azure SQL Database server.</span></span>

## <span data-ttu-id="eec50-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="eec50-107">EXAMPLES</span></span>

### <span data-ttu-id="eec50-108">Exemplo 1: excluir uma regra</span><span class="sxs-lookup"><span data-stu-id="eec50-108">Example 1: Delete a rule</span></span>
```
PS C:\>Remove-AzureRmSqlServerFirewallRule -FirewallRuleName "Rule01" -ResourceGroupName "RresourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="eec50-109">Esse comando exclui uma regra de firewall chamada Rule01 no servidor chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="eec50-109">This command deletes a firewall rule named Rule01 on the server named Server01.</span></span>

## <span data-ttu-id="eec50-110">OS</span><span class="sxs-lookup"><span data-stu-id="eec50-110">PARAMETERS</span></span>

### <span data-ttu-id="eec50-111">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="eec50-111">-FirewallRuleName</span></span>
<span data-ttu-id="eec50-112">Especifica o nome da regra de firewall que este cmdlet exclui.</span><span class="sxs-lookup"><span data-stu-id="eec50-112">Specifies the name of the firewall rule that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="eec50-113">-Force</span><span class="sxs-lookup"><span data-stu-id="eec50-113">-Force</span></span>
<span data-ttu-id="eec50-114">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="eec50-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eec50-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eec50-115">-ResourceGroupName</span></span>
<span data-ttu-id="eec50-116">Especifica o nome de um grupo de recursos ao qual o servidor está atribuído.</span><span class="sxs-lookup"><span data-stu-id="eec50-116">Specifies the name of a resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="eec50-117">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="eec50-117">-ServerName</span></span>
<span data-ttu-id="eec50-118">Especifica o nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="eec50-118">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="eec50-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="eec50-119">-Confirm</span></span>
<span data-ttu-id="eec50-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eec50-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eec50-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eec50-121">-WhatIf</span></span>
<span data-ttu-id="eec50-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="eec50-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eec50-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="eec50-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eec50-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eec50-124">-DefaultProfile</span></span>
<span data-ttu-id="eec50-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="eec50-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eec50-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eec50-126">CommonParameters</span></span>
<span data-ttu-id="eec50-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eec50-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eec50-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eec50-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eec50-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="eec50-129">INPUTS</span></span>

### <span data-ttu-id="eec50-130">Microsoft. Azure. Commands. Sql. FirewallRule. Model. AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="eec50-130">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="eec50-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="eec50-131">OUTPUTS</span></span>

## <span data-ttu-id="eec50-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="eec50-132">NOTES</span></span>

## <span data-ttu-id="eec50-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="eec50-133">RELATED LINKS</span></span>

[<span data-ttu-id="eec50-134">Get-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="eec50-134">Get-AzureRmSqlServerFirewallRule</span></span>](./Get-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="eec50-135">New-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="eec50-135">New-AzureRmSqlServerFirewallRule</span></span>](./New-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="eec50-136">Set-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="eec50-136">Set-AzureRmSqlServerFirewallRule</span></span>](./Set-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="eec50-137">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="eec50-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


