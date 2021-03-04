---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDnsAlias.md
ms.openlocfilehash: 46a3476d5ae4cead17eba0d03412ad2db57b01a4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885787"
---
# <span data-ttu-id="9075f-101">New-AzSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="9075f-101">New-AzSqlServerDnsAlias</span></span>

## <span data-ttu-id="9075f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9075f-102">SYNOPSIS</span></span>
<span data-ttu-id="9075f-103">Este comando cria um novo Alias DNS do Azure SQL Server DNS.</span><span class="sxs-lookup"><span data-stu-id="9075f-103">This command creates a new Azure SQL Server DNS Alias.</span></span>

## <span data-ttu-id="9075f-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="9075f-104">SYNTAX</span></span>

```
New-AzSqlServerDnsAlias -Name <String> [-AsJob] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9075f-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="9075f-105">DESCRIPTION</span></span>
<span data-ttu-id="9075f-106">Cria um novo Alias dns do Azure SQL Server que está apontando para o servidor especificado.</span><span class="sxs-lookup"><span data-stu-id="9075f-106">Creates new Azure SQL Server DNS Alias that is pointing to specified server.</span></span>

## <span data-ttu-id="9075f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9075f-107">EXAMPLES</span></span>

### <span data-ttu-id="9075f-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9075f-108">Example 1</span></span>
```
PS C:\> $serverDNSAlias = New-AzSqlServerDnsAlias -ResourceGroupName rg -ServerName serverName -DnsAliasName aliasName

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
```

<span data-ttu-id="9075f-109">Este comando cria o Azure SQL Server DNS Alias com o nome aliasName que está apontando para serverName do servidor</span><span class="sxs-lookup"><span data-stu-id="9075f-109">This command creates Azure SQL Server DNS Alias with the name aliasName that is pointing to server serverName</span></span>

## <span data-ttu-id="9075f-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="9075f-110">PARAMETERS</span></span>

### <span data-ttu-id="9075f-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9075f-111">-AsJob</span></span>
<span data-ttu-id="9075f-112">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="9075f-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9075f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9075f-113">-DefaultProfile</span></span>
<span data-ttu-id="9075f-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="9075f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9075f-115">-Name</span><span class="sxs-lookup"><span data-stu-id="9075f-115">-Name</span></span>
<span data-ttu-id="9075f-116">O nome alias dns do Azure Sql Server.</span><span class="sxs-lookup"><span data-stu-id="9075f-116">The Azure Sql Server Dns Alias name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DnsAliasName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9075f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9075f-117">-ResourceGroupName</span></span>
<span data-ttu-id="9075f-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9075f-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="9075f-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="9075f-119">-ServerName</span></span>
<span data-ttu-id="9075f-120">O nome do Sql Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="9075f-120">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="9075f-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9075f-121">-Confirm</span></span>
<span data-ttu-id="9075f-122">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9075f-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9075f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9075f-123">-WhatIf</span></span>
<span data-ttu-id="9075f-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9075f-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9075f-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9075f-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9075f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9075f-126">CommonParameters</span></span>
<span data-ttu-id="9075f-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9075f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9075f-128">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9075f-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9075f-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9075f-129">INPUTS</span></span>

### <span data-ttu-id="9075f-130">System.String</span><span class="sxs-lookup"><span data-stu-id="9075f-130">System.String</span></span>

## <span data-ttu-id="9075f-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="9075f-131">OUTPUTS</span></span>

### <span data-ttu-id="9075f-132">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="9075f-132">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="9075f-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="9075f-133">NOTES</span></span>

## <span data-ttu-id="9075f-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9075f-134">RELATED LINKS</span></span>
