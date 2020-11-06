---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerDnsAlias.md
ms.openlocfilehash: dc13bdaf737985f6769b3bb326201100204c6495
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428731"
---
# <span data-ttu-id="f4ba7-101">Remove-AzureRmSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="f4ba7-101">Remove-AzureRmSqlServerDnsAlias</span></span>

## <span data-ttu-id="f4ba7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f4ba7-102">SYNOPSIS</span></span>
<span data-ttu-id="f4ba7-103">Remove o alias do DNS do SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="f4ba7-103">Removes Azure SQL Server DNS Alias.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f4ba7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f4ba7-104">SYNTAX</span></span>

### <span data-ttu-id="f4ba7-105">Remover um alias de DNS de servidor de parâmetros de entrada de cmdlet</span><span class="sxs-lookup"><span data-stu-id="f4ba7-105">Remove a Server Dns Alias from cmdlet input parameters</span></span>
```
Remove-AzureRmSqlServerDnsAlias -Name <String> -ServerName <String> [-ResourceGroupName] <String> [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4ba7-106">Remover um alias DNS de servidor da definição de instância AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="f4ba7-106">Remove a Server Dns Alias from AzureSqlServerDnsAliasModel instance definition</span></span>
```
Remove-AzureRmSqlServerDnsAlias -InputObject <AzureSqlServerDnsAliasModel> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4ba7-107">Remover um alias de DNS de servidor de uma ID de recurso do Azure</span><span class="sxs-lookup"><span data-stu-id="f4ba7-107">Remove a Server Dns Alias from an Azure resource id</span></span>
```
Remove-AzureRmSqlServerDnsAlias -ResourceId <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4ba7-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f4ba7-108">DESCRIPTION</span></span>
<span data-ttu-id="f4ba7-109">Esses comandos removem o alias do DNS do SQL Server do Azure do servidor deixando o servidor intacto.</span><span class="sxs-lookup"><span data-stu-id="f4ba7-109">This commands remove Azure SQL Server DNS Alias from the server leaving server intact.</span></span>

## <span data-ttu-id="f4ba7-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f4ba7-110">EXAMPLES</span></span>

### <span data-ttu-id="f4ba7-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f4ba7-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmSqlServerDnsAlias -DnsAliasName aliasName -ServerName serverName -ResourceGroupName rg
```

<span data-ttu-id="f4ba7-112">Remove o alias DNS do SQL Server do Azure com o nome aliasname do servidor com o nome nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="f4ba7-112">Removes Azure SQL Server DNS Alias with the name aliasName from the server with the name serverName</span></span>

## <span data-ttu-id="f4ba7-113">OS</span><span class="sxs-lookup"><span data-stu-id="f4ba7-113">PARAMETERS</span></span>

### <span data-ttu-id="f4ba7-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f4ba7-114">-AsJob</span></span>
<span data-ttu-id="f4ba7-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="f4ba7-115">Run cmdlet in the background</span></span>
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

### <span data-ttu-id="f4ba7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4ba7-116">-DefaultProfile</span></span>
<span data-ttu-id="f4ba7-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f4ba7-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4ba7-118">-Force</span><span class="sxs-lookup"><span data-stu-id="f4ba7-118">-Force</span></span>
<span data-ttu-id="f4ba7-119">Ignorar a mensagem de confirmação para executar a ação</span><span class="sxs-lookup"><span data-stu-id="f4ba7-119">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="f4ba7-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f4ba7-120">-InputObject</span></span>
<span data-ttu-id="f4ba7-121">O objeto de alias de DNS do servidor a ser removido</span><span class="sxs-lookup"><span data-stu-id="f4ba7-121">The Server Dns Alias object to remove</span></span>

```yaml
Type: AzureSqlServerDnsAliasModel
Parameter Sets: Remove a Server Dns Alias from AzureSqlServerDnsAliasModel instance definition
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f4ba7-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="f4ba7-122">-Name</span></span>
<span data-ttu-id="f4ba7-123">Nome do alias DNS do SQL Server do Azure</span><span class="sxs-lookup"><span data-stu-id="f4ba7-123">Azure Sql Server Dns Alias name</span></span>

```yaml
Type: String
Parameter Sets: Remove a Server Dns Alias from cmdlet input parameters
Aliases: DnsAliasName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4ba7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4ba7-124">-ResourceGroupName</span></span>
<span data-ttu-id="f4ba7-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f4ba7-125">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: Remove a Server Dns Alias from cmdlet input parameters
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4ba7-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f4ba7-126">-ResourceId</span></span>
<span data-ttu-id="f4ba7-127">A ID do recurso do objeto de alias DNS do servidor a ser removido</span><span class="sxs-lookup"><span data-stu-id="f4ba7-127">The resource id of Server Dns Alias object to remove</span></span>

```yaml
Type: String
Parameter Sets: Remove a Server Dns Alias from an Azure resource id
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4ba7-128">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="f4ba7-128">-ServerName</span></span>
<span data-ttu-id="f4ba7-129">O nome do SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="f4ba7-129">The Azure Sql Server name.</span></span>

```yaml
Type: String
Parameter Sets: Remove a Server Dns Alias from cmdlet input parameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4ba7-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f4ba7-130">-Confirm</span></span>
<span data-ttu-id="f4ba7-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4ba7-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4ba7-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4ba7-132">-WhatIf</span></span>
<span data-ttu-id="f4ba7-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f4ba7-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4ba7-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f4ba7-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4ba7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4ba7-135">CommonParameters</span></span>
<span data-ttu-id="f4ba7-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4ba7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4ba7-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4ba7-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4ba7-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f4ba7-138">INPUTS</span></span>

### <span data-ttu-id="f4ba7-139">System. String</span><span class="sxs-lookup"><span data-stu-id="f4ba7-139">System.String</span></span>
<span data-ttu-id="f4ba7-140">Microsoft. Azure. Commands. Sql. ServerDnsAlias. Model. AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="f4ba7-140">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="f4ba7-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f4ba7-141">OUTPUTS</span></span>

### <span data-ttu-id="f4ba7-142">Microsoft. Azure. Commands. Sql. ServerDnsAlias. Model. AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="f4ba7-142">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="f4ba7-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f4ba7-143">NOTES</span></span>

## <span data-ttu-id="f4ba7-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f4ba7-144">RELATED LINKS</span></span>