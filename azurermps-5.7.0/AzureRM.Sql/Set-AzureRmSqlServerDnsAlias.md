---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerDnsAlias.md
ms.openlocfilehash: 78ffcb50b47b315426998825232348dd41c23f97
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427417"
---
# <span data-ttu-id="946d5-101">Set-AzureRmSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="946d5-101">Set-AzureRmSqlServerDnsAlias</span></span>

## <span data-ttu-id="946d5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="946d5-102">SYNOPSIS</span></span>
<span data-ttu-id="946d5-103">Modifica o servidor para o qual o alias DNS do SQL Server do Azure está apontando</span><span class="sxs-lookup"><span data-stu-id="946d5-103">Modifies the server to which Azure SQL Server DNS Alias is pointing</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="946d5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="946d5-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerDnsAlias -Name <String> -TargetServerName <String> [-ResourceGroupName] <String>
 -SourceServerName <String> -SourceServerResourceGroupName <String> -SourceServerSubscriptionId <Guid> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="946d5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="946d5-105">DESCRIPTION</span></span>
<span data-ttu-id="946d5-106">Este comando está atualizando o servidor ao qual o alias está apontando.</span><span class="sxs-lookup"><span data-stu-id="946d5-106">This command is updating the server to which alias is pointing.</span></span> 

<span data-ttu-id="946d5-107">Esse comando precisa ser emitido enquanto estiver conectado em uma assinatura em que o novo servidor ao qual o alias está indo se encontra.</span><span class="sxs-lookup"><span data-stu-id="946d5-107">This command needs to be issued while logged into subscription where new server to which alias is going to point is located.</span></span>

## <span data-ttu-id="946d5-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="946d5-108">EXAMPLES</span></span>

### <span data-ttu-id="946d5-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="946d5-109">Example 1</span></span>
```
PS C:\> Set-AzureRmSqlServerDnsAlias -ResourceGroupName rg -DnsAliasName aliasName -TargetServerName newServer -SourceServerName oldServer -SourceServerResourceGroupName SourceServerRG -SourceServerSubscriptionId 0000-0000-0000-0000
```

<span data-ttu-id="946d5-110">Este comando está atualizando o alias que estava apontando anteriormente para oldServer para apontar para o servidor newServer</span><span class="sxs-lookup"><span data-stu-id="946d5-110">This command is updating alias which was previously pointing to oldServer to point to server newServer</span></span>

## <span data-ttu-id="946d5-111">OS</span><span class="sxs-lookup"><span data-stu-id="946d5-111">PARAMETERS</span></span>

### <span data-ttu-id="946d5-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="946d5-112">-AsJob</span></span>
<span data-ttu-id="946d5-113">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="946d5-113">Run cmdlet in the background</span></span>
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

### <span data-ttu-id="946d5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="946d5-114">-DefaultProfile</span></span>
<span data-ttu-id="946d5-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="946d5-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="946d5-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="946d5-116">-Name</span></span>
<span data-ttu-id="946d5-117">O nome do alias DNS do SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="946d5-117">The Azure Sql Server Dns Alias name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: DnsAliasName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="946d5-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="946d5-118">-ResourceGroupName</span></span>
<span data-ttu-id="946d5-119">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="946d5-119">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TargetResourceGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="946d5-120">-SourceServerName</span><span class="sxs-lookup"><span data-stu-id="946d5-120">-SourceServerName</span></span>
<span data-ttu-id="946d5-121">O nome do Azure SQL Server ao qual o alias está atualmente apontando.</span><span class="sxs-lookup"><span data-stu-id="946d5-121">The name of Azure Sql Server to which alias is currently pointing.</span></span>

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

### <span data-ttu-id="946d5-122">-SourceServerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="946d5-122">-SourceServerResourceGroupName</span></span>
<span data-ttu-id="946d5-123">O nome do grupo de recursos do servidor de origem.</span><span class="sxs-lookup"><span data-stu-id="946d5-123">The name of resource group of the source server.</span></span>

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

### <span data-ttu-id="946d5-124">-SourceServerSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="946d5-124">-SourceServerSubscriptionId</span></span>
<span data-ttu-id="946d5-125">A ID da assinatura do servidor de origem</span><span class="sxs-lookup"><span data-stu-id="946d5-125">The subscription id of the source server</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="946d5-126">-TargetServerName</span><span class="sxs-lookup"><span data-stu-id="946d5-126">-TargetServerName</span></span>
<span data-ttu-id="946d5-127">O nome do Azure SQL Server ao qual o alias deve apontar.</span><span class="sxs-lookup"><span data-stu-id="946d5-127">The name of Azure Sql Server to which alias should point.</span></span>

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

### <span data-ttu-id="946d5-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="946d5-128">-Confirm</span></span>
<span data-ttu-id="946d5-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="946d5-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="946d5-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="946d5-130">-WhatIf</span></span>
<span data-ttu-id="946d5-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="946d5-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="946d5-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="946d5-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="946d5-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="946d5-133">CommonParameters</span></span>
<span data-ttu-id="946d5-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="946d5-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="946d5-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="946d5-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="946d5-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="946d5-136">INPUTS</span></span>

### <span data-ttu-id="946d5-137">System. String</span><span class="sxs-lookup"><span data-stu-id="946d5-137">System.String</span></span>

## <span data-ttu-id="946d5-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="946d5-138">OUTPUTS</span></span>

### <span data-ttu-id="946d5-139">Microsoft. Azure. Commands. Sql. ServerDnsAlias. Model. AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="946d5-139">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="946d5-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="946d5-140">NOTES</span></span>

## <span data-ttu-id="946d5-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="946d5-141">RELATED LINKS</span></span>
