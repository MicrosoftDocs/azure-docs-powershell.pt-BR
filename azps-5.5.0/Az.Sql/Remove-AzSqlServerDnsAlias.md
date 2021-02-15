---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerDnsAlias.md
ms.openlocfilehash: d611f0bc14d657f47881cbdfbb1326111873114a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116136"
---
# <span data-ttu-id="1ae36-101">Remove-AzSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="1ae36-101">Remove-AzSqlServerDnsAlias</span></span>

## <span data-ttu-id="1ae36-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1ae36-102">SYNOPSIS</span></span>
<span data-ttu-id="1ae36-103">Remove o alias DNS do Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="1ae36-103">Removes Azure SQL Server DNS Alias.</span></span>

## <span data-ttu-id="1ae36-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1ae36-104">SYNTAX</span></span>

### <span data-ttu-id="1ae36-105">Remover um Alias Dns do Servidor dos parâmetros de entrada do cmdlet</span><span class="sxs-lookup"><span data-stu-id="1ae36-105">Remove a Server Dns Alias from cmdlet input parameters</span></span>
```
Remove-AzSqlServerDnsAlias -Name <String> -ServerName <String> [-ResourceGroupName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ae36-106">Remover um Alias Dns do Servidor da definição de instância do AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="1ae36-106">Remove a Server Dns Alias from AzureSqlServerDnsAliasModel instance definition</span></span>
```
Remove-AzSqlServerDnsAlias -InputObject <AzureSqlServerDnsAliasModel> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ae36-107">Remover um Alias Dns do Servidor de uma ID de recurso do Azure</span><span class="sxs-lookup"><span data-stu-id="1ae36-107">Remove a Server Dns Alias from an Azure resource id</span></span>
```
Remove-AzSqlServerDnsAlias -ResourceId <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ae36-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="1ae36-108">DESCRIPTION</span></span>
<span data-ttu-id="1ae36-109">Esses comandos removem o Alias DNS do SQL Server do Azure do servidor, deixando o servidor intacto.</span><span class="sxs-lookup"><span data-stu-id="1ae36-109">This commands remove Azure SQL Server DNS Alias from the server leaving server intact.</span></span>

## <span data-ttu-id="1ae36-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1ae36-110">EXAMPLES</span></span>

### <span data-ttu-id="1ae36-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1ae36-111">Example 1</span></span>
```
PS C:\> Remove-AzSqlServerDnsAlias -DnsAliasName aliasName -ServerName serverName -ResourceGroupName rg
```

<span data-ttu-id="1ae36-112">Remove o Alias DNS do Azure SQL Server com o nome aliasName do servidor com o nome serverName</span><span class="sxs-lookup"><span data-stu-id="1ae36-112">Removes Azure SQL Server DNS Alias with the name aliasName from the server with the name serverName</span></span>

## <span data-ttu-id="1ae36-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1ae36-113">PARAMETERS</span></span>

### <span data-ttu-id="1ae36-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1ae36-114">-AsJob</span></span>
<span data-ttu-id="1ae36-115">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="1ae36-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1ae36-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ae36-116">-DefaultProfile</span></span>
<span data-ttu-id="1ae36-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="1ae36-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1ae36-118">-Forçar</span><span class="sxs-lookup"><span data-stu-id="1ae36-118">-Force</span></span>
<span data-ttu-id="1ae36-119">Ignorar a mensagem de confirmação para executar a ação</span><span class="sxs-lookup"><span data-stu-id="1ae36-119">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="1ae36-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1ae36-120">-InputObject</span></span>
<span data-ttu-id="1ae36-121">O objeto Alias dns do servidor a ser removido</span><span class="sxs-lookup"><span data-stu-id="1ae36-121">The Server Dns Alias object to remove</span></span>

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

### <span data-ttu-id="1ae36-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="1ae36-122">-Name</span></span>
<span data-ttu-id="1ae36-123">Nome de alias dns do Azure Sql Server</span><span class="sxs-lookup"><span data-stu-id="1ae36-123">Azure Sql Server Dns Alias name</span></span>

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

### <span data-ttu-id="1ae36-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ae36-124">-ResourceGroupName</span></span>
<span data-ttu-id="1ae36-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1ae36-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="1ae36-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1ae36-126">-ResourceId</span></span>
<span data-ttu-id="1ae36-127">A ID do recurso do objeto Alias dns do servidor a ser removido</span><span class="sxs-lookup"><span data-stu-id="1ae36-127">The resource id of Server Dns Alias object to remove</span></span>

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

### <span data-ttu-id="1ae36-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1ae36-128">-ServerName</span></span>
<span data-ttu-id="1ae36-129">O nome do Sql Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="1ae36-129">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="1ae36-130">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="1ae36-130">-Confirm</span></span>
<span data-ttu-id="1ae36-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ae36-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ae36-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ae36-132">-WhatIf</span></span>
<span data-ttu-id="1ae36-133">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="1ae36-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ae36-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1ae36-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ae36-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ae36-135">CommonParameters</span></span>
<span data-ttu-id="1ae36-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ae36-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ae36-137">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1ae36-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ae36-138">Entradas</span><span class="sxs-lookup"><span data-stu-id="1ae36-138">INPUTS</span></span>

### <span data-ttu-id="1ae36-139">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="1ae36-139">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

### <span data-ttu-id="1ae36-140">System.String</span><span class="sxs-lookup"><span data-stu-id="1ae36-140">System.String</span></span>

## <span data-ttu-id="1ae36-141">Saídas</span><span class="sxs-lookup"><span data-stu-id="1ae36-141">OUTPUTS</span></span>

### <span data-ttu-id="1ae36-142">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="1ae36-142">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="1ae36-143">Notas</span><span class="sxs-lookup"><span data-stu-id="1ae36-143">NOTES</span></span>

## <span data-ttu-id="1ae36-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1ae36-144">RELATED LINKS</span></span>
