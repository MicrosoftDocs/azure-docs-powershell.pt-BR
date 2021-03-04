---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDnsAlias.md
ms.openlocfilehash: 49a175606526979acb4c44ddc4cb23ca7bbc33ff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888646"
---
# <span data-ttu-id="1fba2-101">Get-AzSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="1fba2-101">Get-AzSqlServerDnsAlias</span></span>

## <span data-ttu-id="1fba2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1fba2-102">SYNOPSIS</span></span>
<span data-ttu-id="1fba2-103">Obtém ou lista o Azure SQL Server DNS Alias.</span><span class="sxs-lookup"><span data-stu-id="1fba2-103">Gets or lists Azure SQL Server DNS Alias.</span></span>

## <span data-ttu-id="1fba2-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="1fba2-104">SYNTAX</span></span>

```
Get-AzSqlServerDnsAlias [-Name <String>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1fba2-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="1fba2-105">DESCRIPTION</span></span>
<span data-ttu-id="1fba2-106">Obter o Alias DNS específico do Azure SQL Server lista todos os Aliases DNS do Servidor para o servidor</span><span class="sxs-lookup"><span data-stu-id="1fba2-106">Get the specific Azure SQL Server DNS Alias or lists all Server DNS Aliases for the server</span></span>

## <span data-ttu-id="1fba2-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1fba2-107">EXAMPLES</span></span>

### <span data-ttu-id="1fba2-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1fba2-108">Example 1</span></span>
```
PS C:\> $serverDNSAliases = Get-AzSqlServerDNSAlias -ServerName servername -ResourceGroupName rgname

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
rgname             servername   dnsaliasname2
```

<span data-ttu-id="1fba2-109">Lista todos os Aliases DNS do Servidor para o servidor específico</span><span class="sxs-lookup"><span data-stu-id="1fba2-109">Lists all Server DNS Aliases for the specific server</span></span>

### <span data-ttu-id="1fba2-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="1fba2-110">Example 2</span></span>
```
PS C:\> $serverDNSAliases = Get-AzSqlServerDNSAlias -DnsAliasName dnsaliasname -ServerName servername -ResourceGroupName rgname

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
```

<span data-ttu-id="1fba2-111">Obtém Alias DNS do servidor especificado pelo nome de servidor e alias</span><span class="sxs-lookup"><span data-stu-id="1fba2-111">Gets Server DNS Alias specified by server and alias name</span></span>

### <span data-ttu-id="1fba2-112">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="1fba2-112">Example 3</span></span>
```
PS C:\> $serverDNSAliases = Get-AzSqlServerDNSAlias -ServerName servername -ResourceGroupName rgname -DnsAliasName "dnsaliasname*"

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
rgname             servername   dnsaliasname2
```

<span data-ttu-id="1fba2-113">Lista todos os Aliases DNS do Servidor para o servidor específico que começa com "dnsaliasname".</span><span class="sxs-lookup"><span data-stu-id="1fba2-113">Lists all Server DNS Aliases for the specific server that start with "dnsaliasname".</span></span>

## <span data-ttu-id="1fba2-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="1fba2-114">PARAMETERS</span></span>

### <span data-ttu-id="1fba2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fba2-115">-DefaultProfile</span></span>
<span data-ttu-id="1fba2-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="1fba2-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1fba2-117">-Name</span><span class="sxs-lookup"><span data-stu-id="1fba2-117">-Name</span></span>
<span data-ttu-id="1fba2-118">O nome alias DNS do Azure Sql Server.</span><span class="sxs-lookup"><span data-stu-id="1fba2-118">The Azure Sql Server DNS Alias name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DnsAliasName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fba2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1fba2-119">-ResourceGroupName</span></span>
<span data-ttu-id="1fba2-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1fba2-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="1fba2-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1fba2-121">-ServerName</span></span>
<span data-ttu-id="1fba2-122">O nome do Sql Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="1fba2-122">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="1fba2-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1fba2-123">-Confirm</span></span>
<span data-ttu-id="1fba2-124">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1fba2-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1fba2-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1fba2-125">-WhatIf</span></span>
<span data-ttu-id="1fba2-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1fba2-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1fba2-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1fba2-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1fba2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fba2-128">CommonParameters</span></span>
<span data-ttu-id="1fba2-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1fba2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fba2-130">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1fba2-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fba2-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1fba2-131">INPUTS</span></span>

### <span data-ttu-id="1fba2-132">System.String</span><span class="sxs-lookup"><span data-stu-id="1fba2-132">System.String</span></span>

## <span data-ttu-id="1fba2-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="1fba2-133">OUTPUTS</span></span>

### <span data-ttu-id="1fba2-134">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="1fba2-134">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="1fba2-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="1fba2-135">NOTES</span></span>

## <span data-ttu-id="1fba2-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1fba2-136">RELATED LINKS</span></span>
