---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerDnsAlias.md
ms.openlocfilehash: 4a2b7de83036e274b9d53b701615e3c348c5f4df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426563"
---
# <span data-ttu-id="9494c-101">Get-AzureRmSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="9494c-101">Get-AzureRmSqlServerDnsAlias</span></span>

## <span data-ttu-id="9494c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9494c-102">SYNOPSIS</span></span>
<span data-ttu-id="9494c-103">Obtém ou lista o alias DNS do SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="9494c-103">Gets or lists Azure SQL Server DNS Alias.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9494c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9494c-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerDnsAlias [-Name <String>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9494c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9494c-105">DESCRIPTION</span></span>
<span data-ttu-id="9494c-106">Obtenha o alias DNS específico do Azure SQL Server ou liste todos os aliases de servidor DNS do servidor</span><span class="sxs-lookup"><span data-stu-id="9494c-106">Get the specific Azure SQL Server DNS Alias or lists all Server DNS Aliases for the server</span></span>

## <span data-ttu-id="9494c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9494c-107">EXAMPLES</span></span>

### <span data-ttu-id="9494c-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9494c-108">Example 1</span></span>
```
PS C:\> $serverDNSAliases = Get-AzureRmSqlServerDNSAlias -ServerName servername -ResourceGroupName rgname

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
rgname             servername   dnsaliasname2
```

<span data-ttu-id="9494c-109">Lista todos os aliases de servidor DNS para o servidor específico</span><span class="sxs-lookup"><span data-stu-id="9494c-109">Lists all Server DNS Aliases for the specific server</span></span>

### <span data-ttu-id="9494c-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="9494c-110">Example 2</span></span>
```
PS C:\> $serverDNSAliases = Get-AzureRmSqlServerDNSAlias -DnsAliasName dnsaliasname -ServerName servername -ResourceGroupName rgname

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
```

<span data-ttu-id="9494c-111">Obtém o alias DNS do servidor especificado pelo nome do servidor e do alias</span><span class="sxs-lookup"><span data-stu-id="9494c-111">Gets Server DNS Alias specified by server and alias name</span></span>

## <span data-ttu-id="9494c-112">OS</span><span class="sxs-lookup"><span data-stu-id="9494c-112">PARAMETERS</span></span>

### <span data-ttu-id="9494c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9494c-113">-DefaultProfile</span></span>
<span data-ttu-id="9494c-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9494c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9494c-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="9494c-115">-Name</span></span>
<span data-ttu-id="9494c-116">O nome do alias DNS do SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="9494c-116">The Azure Sql Server DNS Alias name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: DnsAliasName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9494c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9494c-117">-ResourceGroupName</span></span>
<span data-ttu-id="9494c-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9494c-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="9494c-119">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="9494c-119">-ServerName</span></span>
<span data-ttu-id="9494c-120">O nome do SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="9494c-120">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="9494c-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9494c-121">-Confirm</span></span>
<span data-ttu-id="9494c-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9494c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9494c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9494c-123">-WhatIf</span></span>
<span data-ttu-id="9494c-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9494c-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9494c-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9494c-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9494c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9494c-126">CommonParameters</span></span>
<span data-ttu-id="9494c-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9494c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9494c-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9494c-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9494c-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9494c-129">INPUTS</span></span>

### <span data-ttu-id="9494c-130">System. String</span><span class="sxs-lookup"><span data-stu-id="9494c-130">System.String</span></span>

## <span data-ttu-id="9494c-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9494c-131">OUTPUTS</span></span>

### <span data-ttu-id="9494c-132">Microsoft. Azure. Commands. Sql. ServerDnsAlias. Model. AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="9494c-132">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="9494c-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9494c-133">NOTES</span></span>

## <span data-ttu-id="9494c-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9494c-134">RELATED LINKS</span></span>
