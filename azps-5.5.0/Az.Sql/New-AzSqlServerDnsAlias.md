---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDnsAlias.md
ms.openlocfilehash: 66f8c3acc178a922868177200e6d4f1f8f50931f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100110930"
---
# <span data-ttu-id="6b85e-101">New-AzSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="6b85e-101">New-AzSqlServerDnsAlias</span></span>

## <span data-ttu-id="6b85e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6b85e-102">SYNOPSIS</span></span>
<span data-ttu-id="6b85e-103">Esse comando cria um novo Alias DNS do Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="6b85e-103">This command creates a new Azure SQL Server DNS Alias.</span></span>

## <span data-ttu-id="6b85e-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6b85e-104">SYNTAX</span></span>

```
New-AzSqlServerDnsAlias -Name <String> [-AsJob] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b85e-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="6b85e-105">DESCRIPTION</span></span>
<span data-ttu-id="6b85e-106">Cria um novo Alias DNS do Azure SQL Server que aponta para o servidor especificado.</span><span class="sxs-lookup"><span data-stu-id="6b85e-106">Creates new Azure SQL Server DNS Alias that is pointing to specified server.</span></span>

## <span data-ttu-id="6b85e-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6b85e-107">EXAMPLES</span></span>

### <span data-ttu-id="6b85e-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6b85e-108">Example 1</span></span>
```
PS C:\> $serverDNSAlias = New-AzSqlServerDnsAlias -ResourceGroupName rg -ServerName serverName -DnsAliasName aliasName

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
```

<span data-ttu-id="6b85e-109">Esse comando cria Alias DNS do Azure SQL Server com o nome aliasName que aponta para serverName</span><span class="sxs-lookup"><span data-stu-id="6b85e-109">This command creates Azure SQL Server DNS Alias with the name aliasName that is pointing to server serverName</span></span>

## <span data-ttu-id="6b85e-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6b85e-110">PARAMETERS</span></span>

### <span data-ttu-id="6b85e-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6b85e-111">-AsJob</span></span>
<span data-ttu-id="6b85e-112">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="6b85e-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6b85e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b85e-113">-DefaultProfile</span></span>
<span data-ttu-id="6b85e-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="6b85e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6b85e-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="6b85e-115">-Name</span></span>
<span data-ttu-id="6b85e-116">O nome alias dns do Azure Sql Server.</span><span class="sxs-lookup"><span data-stu-id="6b85e-116">The Azure Sql Server Dns Alias name.</span></span>

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

### <span data-ttu-id="6b85e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b85e-117">-ResourceGroupName</span></span>
<span data-ttu-id="6b85e-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6b85e-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="6b85e-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="6b85e-119">-ServerName</span></span>
<span data-ttu-id="6b85e-120">O nome do Sql Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="6b85e-120">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="6b85e-121">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="6b85e-121">-Confirm</span></span>
<span data-ttu-id="6b85e-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6b85e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b85e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b85e-123">-WhatIf</span></span>
<span data-ttu-id="6b85e-124">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="6b85e-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b85e-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6b85e-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b85e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b85e-126">CommonParameters</span></span>
<span data-ttu-id="6b85e-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b85e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b85e-128">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6b85e-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b85e-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="6b85e-129">INPUTS</span></span>

### <span data-ttu-id="6b85e-130">System.String</span><span class="sxs-lookup"><span data-stu-id="6b85e-130">System.String</span></span>

## <span data-ttu-id="6b85e-131">Saídas</span><span class="sxs-lookup"><span data-stu-id="6b85e-131">OUTPUTS</span></span>

### <span data-ttu-id="6b85e-132">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="6b85e-132">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="6b85e-133">Notas</span><span class="sxs-lookup"><span data-stu-id="6b85e-133">NOTES</span></span>

## <span data-ttu-id="6b85e-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6b85e-134">RELATED LINKS</span></span>
