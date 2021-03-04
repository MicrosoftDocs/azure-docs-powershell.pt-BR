---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerDnsAlias.md
ms.openlocfilehash: bbc941c260579fb7fdb437f0b30002999635b8eb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887658"
---
# <span data-ttu-id="8f7a5-101">Set-AzSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="8f7a5-101">Set-AzSqlServerDnsAlias</span></span>

## <span data-ttu-id="8f7a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f7a5-102">SYNOPSIS</span></span>
<span data-ttu-id="8f7a5-103">Modifica o servidor para o qual o Azure SQL Server DNS Alias está apontando</span><span class="sxs-lookup"><span data-stu-id="8f7a5-103">Modifies the server to which Azure SQL Server DNS Alias is pointing</span></span>

## <span data-ttu-id="8f7a5-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="8f7a5-104">SYNTAX</span></span>

```
Set-AzSqlServerDnsAlias -Name <String> -TargetServerName <String> [-ResourceGroupName] <String>
 -SourceServerName <String> -SourceServerResourceGroupName <String> -SourceServerSubscriptionId <Guid> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f7a5-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="8f7a5-105">DESCRIPTION</span></span>
<span data-ttu-id="8f7a5-106">Este comando está atualizando o servidor para o qual o alias está apontando.</span><span class="sxs-lookup"><span data-stu-id="8f7a5-106">This command is updating the server to which alias is pointing.</span></span> <span data-ttu-id="8f7a5-107">Esse comando precisa ser emitido enquanto estiver conectado à assinatura onde o novo servidor para o qual o alias apontará está localizado.</span><span class="sxs-lookup"><span data-stu-id="8f7a5-107">This command needs to be issued while logged into subscription where new server to which alias is going to point is located.</span></span>

## <span data-ttu-id="8f7a5-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8f7a5-108">EXAMPLES</span></span>

### <span data-ttu-id="8f7a5-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8f7a5-109">Example 1</span></span>
```
PS C:\> Set-AzSqlServerDnsAlias -ResourceGroupName rg -DnsAliasName aliasName -TargetServerName newServer -SourceServerName oldServer -SourceServerResourceGroupName SourceServerRG -SourceServerSubscriptionId 0000-0000-0000-0000
```

<span data-ttu-id="8f7a5-110">Este comando está atualizando o alias que estava apontando anteriormente para o oldServer para apontar para o servidor newServer</span><span class="sxs-lookup"><span data-stu-id="8f7a5-110">This command is updating alias which was previously pointing to oldServer to point to server newServer</span></span>

## <span data-ttu-id="8f7a5-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="8f7a5-111">PARAMETERS</span></span>

### <span data-ttu-id="8f7a5-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8f7a5-112">-AsJob</span></span>
<span data-ttu-id="8f7a5-113">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="8f7a5-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8f7a5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f7a5-114">-DefaultProfile</span></span>
<span data-ttu-id="8f7a5-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="8f7a5-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8f7a5-116">-Name</span><span class="sxs-lookup"><span data-stu-id="8f7a5-116">-Name</span></span>
<span data-ttu-id="8f7a5-117">O nome alias dns do Azure Sql Server.</span><span class="sxs-lookup"><span data-stu-id="8f7a5-117">The Azure Sql Server Dns Alias name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DnsAliasName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f7a5-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f7a5-118">-ResourceGroupName</span></span>
<span data-ttu-id="8f7a5-119">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8f7a5-119">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TargetResourceGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f7a5-120">-SourceServerName</span><span class="sxs-lookup"><span data-stu-id="8f7a5-120">-SourceServerName</span></span>
<span data-ttu-id="8f7a5-121">O nome do Azure Sql Server para o qual o alias está apontando no momento.</span><span class="sxs-lookup"><span data-stu-id="8f7a5-121">The name of Azure Sql Server to which alias is currently pointing.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f7a5-122">-SourceServerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f7a5-122">-SourceServerResourceGroupName</span></span>
<span data-ttu-id="8f7a5-123">O nome do grupo de recursos do servidor de origem.</span><span class="sxs-lookup"><span data-stu-id="8f7a5-123">The name of resource group of the source server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f7a5-124">-SourceServerSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8f7a5-124">-SourceServerSubscriptionId</span></span>
<span data-ttu-id="8f7a5-125">A id de assinatura do servidor de origem</span><span class="sxs-lookup"><span data-stu-id="8f7a5-125">The subscription id of the source server</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f7a5-126">-TargetServerName</span><span class="sxs-lookup"><span data-stu-id="8f7a5-126">-TargetServerName</span></span>
<span data-ttu-id="8f7a5-127">O nome do Azure Sql Server para o qual o alias deve apontar.</span><span class="sxs-lookup"><span data-stu-id="8f7a5-127">The name of Azure Sql Server to which alias should point.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f7a5-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8f7a5-128">-Confirm</span></span>
<span data-ttu-id="8f7a5-129">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8f7a5-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f7a5-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f7a5-130">-WhatIf</span></span>
<span data-ttu-id="8f7a5-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8f7a5-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f7a5-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8f7a5-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f7a5-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f7a5-133">CommonParameters</span></span>
<span data-ttu-id="8f7a5-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f7a5-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f7a5-135">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8f7a5-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f7a5-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8f7a5-136">INPUTS</span></span>

### <span data-ttu-id="8f7a5-137">System.String</span><span class="sxs-lookup"><span data-stu-id="8f7a5-137">System.String</span></span>

## <span data-ttu-id="8f7a5-138">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="8f7a5-138">OUTPUTS</span></span>

### <span data-ttu-id="8f7a5-139">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="8f7a5-139">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="8f7a5-140">NOTES</span><span class="sxs-lookup"><span data-stu-id="8f7a5-140">NOTES</span></span>

## <span data-ttu-id="8f7a5-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8f7a5-141">RELATED LINKS</span></span>
