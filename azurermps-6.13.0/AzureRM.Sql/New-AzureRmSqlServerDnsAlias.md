---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerDnsAlias.md
ms.openlocfilehash: 3ce18369645705f78722f7505c8dd1e46f2514b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427141"
---
# <span data-ttu-id="ecff8-101">New-AzureRmSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="ecff8-101">New-AzureRmSqlServerDnsAlias</span></span>

## <span data-ttu-id="ecff8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ecff8-102">SYNOPSIS</span></span>
<span data-ttu-id="ecff8-103">Esse comando cria um novo alias de DNS do SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="ecff8-103">This command creates a new Azure SQL Server DNS Alias.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ecff8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ecff8-104">SYNTAX</span></span>

```
New-AzureRmSqlServerDnsAlias -Name <String> [-AsJob] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ecff8-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ecff8-105">DESCRIPTION</span></span>
<span data-ttu-id="ecff8-106">Cria um novo alias do DNS do SQL Server do Azure que está apontando para o servidor especificado.</span><span class="sxs-lookup"><span data-stu-id="ecff8-106">Creates new Azure SQL Server DNS Alias that is pointing to specified server.</span></span>

## <span data-ttu-id="ecff8-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ecff8-107">EXAMPLES</span></span>

### <span data-ttu-id="ecff8-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ecff8-108">Example 1</span></span>
```
PS C:\> $serverDNSAlias = New-AzureRmSqlServerDnsAlias -ResourceGroupName rg -ServerName serverName -DnsAliasName aliasName

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
```

<span data-ttu-id="ecff8-109">Esse comando cria o alias do DNS do SQL Server do Azure com o nome aliasname que está apontando para Server nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="ecff8-109">This command creates Azure SQL Server DNS Alias with the name aliasName that is pointing to server serverName</span></span>

## <span data-ttu-id="ecff8-110">OS</span><span class="sxs-lookup"><span data-stu-id="ecff8-110">PARAMETERS</span></span>

### <span data-ttu-id="ecff8-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ecff8-111">-AsJob</span></span>
<span data-ttu-id="ecff8-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="ecff8-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ecff8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecff8-113">-DefaultProfile</span></span>
<span data-ttu-id="ecff8-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ecff8-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ecff8-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="ecff8-115">-Name</span></span>
<span data-ttu-id="ecff8-116">O nome do alias DNS do SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="ecff8-116">The Azure Sql Server Dns Alias name.</span></span>

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

### <span data-ttu-id="ecff8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecff8-117">-ResourceGroupName</span></span>
<span data-ttu-id="ecff8-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ecff8-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="ecff8-119">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="ecff8-119">-ServerName</span></span>
<span data-ttu-id="ecff8-120">O nome do SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="ecff8-120">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="ecff8-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ecff8-121">-Confirm</span></span>
<span data-ttu-id="ecff8-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ecff8-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ecff8-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ecff8-123">-WhatIf</span></span>
<span data-ttu-id="ecff8-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ecff8-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ecff8-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ecff8-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ecff8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecff8-126">CommonParameters</span></span>
<span data-ttu-id="ecff8-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ecff8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecff8-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ecff8-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecff8-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ecff8-129">INPUTS</span></span>

### <span data-ttu-id="ecff8-130">System. String</span><span class="sxs-lookup"><span data-stu-id="ecff8-130">System.String</span></span>

## <span data-ttu-id="ecff8-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ecff8-131">OUTPUTS</span></span>

### <span data-ttu-id="ecff8-132">Microsoft. Azure. Commands. Sql. ServerDnsAlias. Model. AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="ecff8-132">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="ecff8-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ecff8-133">NOTES</span></span>

## <span data-ttu-id="ecff8-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ecff8-134">RELATED LINKS</span></span>
