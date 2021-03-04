---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerDnsAlias.md
ms.openlocfilehash: 07065c18b9e06f75863ddd41f8a6f0155a3699f9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887309"
---
# <span data-ttu-id="b4a32-101">Remove-AzSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="b4a32-101">Remove-AzSqlServerDnsAlias</span></span>

## <span data-ttu-id="b4a32-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4a32-102">SYNOPSIS</span></span>
<span data-ttu-id="b4a32-103">Remove o Azure SQL Server DNS Alias.</span><span class="sxs-lookup"><span data-stu-id="b4a32-103">Removes Azure SQL Server DNS Alias.</span></span>

## <span data-ttu-id="b4a32-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b4a32-104">SYNTAX</span></span>

### <span data-ttu-id="b4a32-105">Remover um Alias dns do servidor dos parâmetros de entrada do cmdlet</span><span class="sxs-lookup"><span data-stu-id="b4a32-105">Remove a Server Dns Alias from cmdlet input parameters</span></span>
```
Remove-AzSqlServerDnsAlias -Name <String> -ServerName <String> [-ResourceGroupName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4a32-106">Remover um Alias dns do servidor da definição de instância do AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="b4a32-106">Remove a Server Dns Alias from AzureSqlServerDnsAliasModel instance definition</span></span>
```
Remove-AzSqlServerDnsAlias -InputObject <AzureSqlServerDnsAliasModel> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4a32-107">Remover um Alias dns do servidor de uma id de recurso do Azure</span><span class="sxs-lookup"><span data-stu-id="b4a32-107">Remove a Server Dns Alias from an Azure resource id</span></span>
```
Remove-AzSqlServerDnsAlias -ResourceId <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4a32-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b4a32-108">DESCRIPTION</span></span>
<span data-ttu-id="b4a32-109">Esses comandos removem o Azure SQL Server Dns Alias do servidor deixando o servidor intacto.</span><span class="sxs-lookup"><span data-stu-id="b4a32-109">This commands remove Azure SQL Server DNS Alias from the server leaving server intact.</span></span>

## <span data-ttu-id="b4a32-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b4a32-110">EXAMPLES</span></span>

### <span data-ttu-id="b4a32-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b4a32-111">Example 1</span></span>
```
PS C:\> Remove-AzSqlServerDnsAlias -DnsAliasName aliasName -ServerName serverName -ResourceGroupName rg
```

<span data-ttu-id="b4a32-112">Remove o Azure SQL Server DNS Alias com o nome aliasName do servidor com o nome serverName</span><span class="sxs-lookup"><span data-stu-id="b4a32-112">Removes Azure SQL Server DNS Alias with the name aliasName from the server with the name serverName</span></span>

## <span data-ttu-id="b4a32-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b4a32-113">PARAMETERS</span></span>

### <span data-ttu-id="b4a32-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b4a32-114">-AsJob</span></span>
<span data-ttu-id="b4a32-115">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="b4a32-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b4a32-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4a32-116">-DefaultProfile</span></span>
<span data-ttu-id="b4a32-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="b4a32-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4a32-118">-Force</span><span class="sxs-lookup"><span data-stu-id="b4a32-118">-Force</span></span>
<span data-ttu-id="b4a32-119">Ignorar mensagem de confirmação para executar a ação</span><span class="sxs-lookup"><span data-stu-id="b4a32-119">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="b4a32-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b4a32-120">-InputObject</span></span>
<span data-ttu-id="b4a32-121">O objeto Alias dns do servidor a ser removido</span><span class="sxs-lookup"><span data-stu-id="b4a32-121">The Server Dns Alias object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel
Parameter Sets: Remove a Server Dns Alias from AzureSqlServerDnsAliasModel instance definition
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b4a32-122">-Name</span><span class="sxs-lookup"><span data-stu-id="b4a32-122">-Name</span></span>
<span data-ttu-id="b4a32-123">Nome do Alias dns do Azure Sql Server</span><span class="sxs-lookup"><span data-stu-id="b4a32-123">Azure Sql Server Dns Alias name</span></span>

```yaml
Type: System.String
Parameter Sets: Remove a Server Dns Alias from cmdlet input parameters
Aliases: DnsAliasName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4a32-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4a32-124">-ResourceGroupName</span></span>
<span data-ttu-id="b4a32-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b4a32-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Remove a Server Dns Alias from cmdlet input parameters
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4a32-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b4a32-126">-ResourceId</span></span>
<span data-ttu-id="b4a32-127">A id de recurso do objeto Dns Alias do Servidor a ser removido</span><span class="sxs-lookup"><span data-stu-id="b4a32-127">The resource id of Server Dns Alias object to remove</span></span>

```yaml
Type: System.String
Parameter Sets: Remove a Server Dns Alias from an Azure resource id
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4a32-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b4a32-128">-ServerName</span></span>
<span data-ttu-id="b4a32-129">O nome do Sql Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="b4a32-129">The Azure Sql Server name.</span></span>

```yaml
Type: System.String
Parameter Sets: Remove a Server Dns Alias from cmdlet input parameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4a32-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b4a32-130">-Confirm</span></span>
<span data-ttu-id="b4a32-131">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4a32-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4a32-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4a32-132">-WhatIf</span></span>
<span data-ttu-id="b4a32-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b4a32-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4a32-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b4a32-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4a32-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4a32-135">CommonParameters</span></span>
<span data-ttu-id="b4a32-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4a32-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4a32-137">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b4a32-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4a32-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b4a32-138">INPUTS</span></span>

### <span data-ttu-id="b4a32-139">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="b4a32-139">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

### <span data-ttu-id="b4a32-140">System.String</span><span class="sxs-lookup"><span data-stu-id="b4a32-140">System.String</span></span>

## <span data-ttu-id="b4a32-141">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b4a32-141">OUTPUTS</span></span>

### <span data-ttu-id="b4a32-142">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="b4a32-142">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="b4a32-143">NOTES</span><span class="sxs-lookup"><span data-stu-id="b4a32-143">NOTES</span></span>

## <span data-ttu-id="b4a32-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b4a32-144">RELATED LINKS</span></span>
