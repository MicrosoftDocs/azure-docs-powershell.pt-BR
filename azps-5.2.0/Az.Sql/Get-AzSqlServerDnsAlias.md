---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDnsAlias.md
ms.openlocfilehash: 417bab5679da4607cc42468fc4620cf392323919
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98261053"
---
# <span data-ttu-id="820bc-101">Get-AzSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="820bc-101">Get-AzSqlServerDnsAlias</span></span>

## <span data-ttu-id="820bc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="820bc-102">SYNOPSIS</span></span>
<span data-ttu-id="820bc-103">Obtém ou lista o alias DNS do SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="820bc-103">Gets or lists Azure SQL Server DNS Alias.</span></span>

## <span data-ttu-id="820bc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="820bc-104">SYNTAX</span></span>

```
Get-AzSqlServerDnsAlias [-Name <String>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="820bc-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="820bc-105">DESCRIPTION</span></span>
<span data-ttu-id="820bc-106">Obtenha o alias DNS específico do Azure SQL Server ou liste todos os aliases de servidor DNS do servidor</span><span class="sxs-lookup"><span data-stu-id="820bc-106">Get the specific Azure SQL Server DNS Alias or lists all Server DNS Aliases for the server</span></span>

## <span data-ttu-id="820bc-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="820bc-107">EXAMPLES</span></span>

### <span data-ttu-id="820bc-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="820bc-108">Example 1</span></span>
```
PS C:\> $serverDNSAliases = Get-AzSqlServerDNSAlias -ServerName servername -ResourceGroupName rgname

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
rgname             servername   dnsaliasname2
```

<span data-ttu-id="820bc-109">Lista todos os aliases de servidor DNS para o servidor específico</span><span class="sxs-lookup"><span data-stu-id="820bc-109">Lists all Server DNS Aliases for the specific server</span></span>

### <span data-ttu-id="820bc-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="820bc-110">Example 2</span></span>
```
PS C:\> $serverDNSAliases = Get-AzSqlServerDNSAlias -DnsAliasName dnsaliasname -ServerName servername -ResourceGroupName rgname

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
```

<span data-ttu-id="820bc-111">Obtém o alias DNS do servidor especificado pelo nome do servidor e do alias</span><span class="sxs-lookup"><span data-stu-id="820bc-111">Gets Server DNS Alias specified by server and alias name</span></span>

### <span data-ttu-id="820bc-112">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="820bc-112">Example 3</span></span>
```
PS C:\> $serverDNSAliases = Get-AzSqlServerDNSAlias -ServerName servername -ResourceGroupName rgname -DnsAliasName "dnsaliasname*"

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
rgname             servername   dnsaliasname2
```

<span data-ttu-id="820bc-113">Lista todos os aliases de servidor DNS para o servidor específico que começa com "dnsaliasname".</span><span class="sxs-lookup"><span data-stu-id="820bc-113">Lists all Server DNS Aliases for the specific server that start with "dnsaliasname".</span></span>

## <span data-ttu-id="820bc-114">OS</span><span class="sxs-lookup"><span data-stu-id="820bc-114">PARAMETERS</span></span>

### <span data-ttu-id="820bc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="820bc-115">-DefaultProfile</span></span>
<span data-ttu-id="820bc-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="820bc-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="820bc-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="820bc-117">-Name</span></span>
<span data-ttu-id="820bc-118">O nome do alias DNS do SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="820bc-118">The Azure Sql Server DNS Alias name.</span></span>

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

### <span data-ttu-id="820bc-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="820bc-119">-ResourceGroupName</span></span>
<span data-ttu-id="820bc-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="820bc-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="820bc-121">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="820bc-121">-ServerName</span></span>
<span data-ttu-id="820bc-122">O nome do SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="820bc-122">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="820bc-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="820bc-123">-Confirm</span></span>
<span data-ttu-id="820bc-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="820bc-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="820bc-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="820bc-125">-WhatIf</span></span>
<span data-ttu-id="820bc-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="820bc-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="820bc-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="820bc-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="820bc-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="820bc-128">CommonParameters</span></span>
<span data-ttu-id="820bc-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="820bc-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="820bc-130">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="820bc-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="820bc-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="820bc-131">INPUTS</span></span>

### <span data-ttu-id="820bc-132">System. String</span><span class="sxs-lookup"><span data-stu-id="820bc-132">System.String</span></span>

## <span data-ttu-id="820bc-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="820bc-133">OUTPUTS</span></span>

### <span data-ttu-id="820bc-134">Microsoft. Azure. Commands. Sql. ServerDnsAlias. Model. AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="820bc-134">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="820bc-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="820bc-135">NOTES</span></span>

## <span data-ttu-id="820bc-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="820bc-136">RELATED LINKS</span></span>
