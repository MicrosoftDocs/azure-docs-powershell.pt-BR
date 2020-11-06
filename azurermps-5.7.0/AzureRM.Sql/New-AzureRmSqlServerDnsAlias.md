---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerDnsAlias.md
ms.openlocfilehash: 897911a4f13b2453d0e814828000309ad8865ba5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431562"
---
# <span data-ttu-id="77549-101">New-AzureRmSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="77549-101">New-AzureRmSqlServerDnsAlias</span></span>

## <span data-ttu-id="77549-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="77549-102">SYNOPSIS</span></span>
<span data-ttu-id="77549-103">Esse comando cria um novo alias de DNS do SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="77549-103">This command creates a new Azure SQL Server DNS Alias.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="77549-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="77549-104">SYNTAX</span></span>

```
New-AzureRmSqlServerDnsAlias -Name <String> [-AsJob] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77549-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="77549-105">DESCRIPTION</span></span>
<span data-ttu-id="77549-106">Cria um novo alias do DNS do SQL Server do Azure que está apontando para o servidor especificado.</span><span class="sxs-lookup"><span data-stu-id="77549-106">Creates new Azure SQL Server DNS Alias that is pointing to specified server.</span></span>

## <span data-ttu-id="77549-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="77549-107">EXAMPLES</span></span>

### <span data-ttu-id="77549-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="77549-108">Example 1</span></span>
```
PS C:\> $serverDNSAlias = New-AzureRmSqlServerDnsAlias -ResourceGroupName rg -ServerName serverName -DnsAliasName aliasName

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
```

<span data-ttu-id="77549-109">Esse comando cria o alias do DNS do SQL Server do Azure com o nome aliasname que está apontando para Server nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="77549-109">This command creates Azure SQL Server DNS Alias with the name aliasName that is pointing to server serverName</span></span>

## <span data-ttu-id="77549-110">OS</span><span class="sxs-lookup"><span data-stu-id="77549-110">PARAMETERS</span></span>

### <span data-ttu-id="77549-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="77549-111">-AsJob</span></span>
<span data-ttu-id="77549-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="77549-112">Run cmdlet in the background</span></span>
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

### <span data-ttu-id="77549-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77549-113">-DefaultProfile</span></span>
<span data-ttu-id="77549-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="77549-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="77549-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="77549-115">-Name</span></span>
<span data-ttu-id="77549-116">O nome do alias DNS do SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="77549-116">The Azure Sql Server Dns Alias name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: DnsAliasName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77549-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77549-117">-ResourceGroupName</span></span>
<span data-ttu-id="77549-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="77549-118">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77549-119">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="77549-119">-ServerName</span></span>
<span data-ttu-id="77549-120">O nome do SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="77549-120">The Azure Sql Server name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77549-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="77549-121">-Confirm</span></span>
<span data-ttu-id="77549-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="77549-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77549-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77549-123">-WhatIf</span></span>
<span data-ttu-id="77549-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="77549-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77549-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="77549-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77549-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77549-126">CommonParameters</span></span>
<span data-ttu-id="77549-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77549-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77549-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77549-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77549-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="77549-129">INPUTS</span></span>

### <span data-ttu-id="77549-130">System. String</span><span class="sxs-lookup"><span data-stu-id="77549-130">System.String</span></span>

## <span data-ttu-id="77549-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="77549-131">OUTPUTS</span></span>

### <span data-ttu-id="77549-132">Microsoft. Azure. Commands. Sql. ServerDnsAlias. Model. AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="77549-132">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="77549-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="77549-133">NOTES</span></span>

## <span data-ttu-id="77549-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="77549-134">RELATED LINKS</span></span>
