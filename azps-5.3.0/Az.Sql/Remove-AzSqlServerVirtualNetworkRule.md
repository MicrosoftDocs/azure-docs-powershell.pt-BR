---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 265600b201a6333b8dcd7c14f0cefe429f92619e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98426818"
---
# <span data-ttu-id="12172-101">Remove-AzSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="12172-101">Remove-AzSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="12172-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="12172-102">SYNOPSIS</span></span>
<span data-ttu-id="12172-103">Exclui uma regra de rede virtual do Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="12172-103">Deletes an Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="12172-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="12172-104">SYNTAX</span></span>

```
Remove-AzSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> [-AsJob] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="12172-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="12172-105">DESCRIPTION</span></span>
<span data-ttu-id="12172-106">Esse comando exclui uma regra de rede virtual do SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="12172-106">This command deletes an Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="12172-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="12172-107">EXAMPLES</span></span>

### <span data-ttu-id="12172-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="12172-108">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Remove-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName
```

<span data-ttu-id="12172-109">Exclui uma regra de rede virtual do Azure SQL Server existente</span><span class="sxs-lookup"><span data-stu-id="12172-109">Deletes an existing Azure SQL Server virtual network rule</span></span>

## <span data-ttu-id="12172-110">OS</span><span class="sxs-lookup"><span data-stu-id="12172-110">PARAMETERS</span></span>

### <span data-ttu-id="12172-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="12172-111">-AsJob</span></span>
<span data-ttu-id="12172-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="12172-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="12172-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12172-113">-DefaultProfile</span></span>
<span data-ttu-id="12172-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="12172-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="12172-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12172-115">-ResourceGroupName</span></span>
<span data-ttu-id="12172-116">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="12172-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="12172-117">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="12172-117">-ServerName</span></span>
<span data-ttu-id="12172-118">O nome do SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="12172-118">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="12172-119">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="12172-119">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="12172-120">Nome da regra de rede virtual do SQL Server do Azure</span><span class="sxs-lookup"><span data-stu-id="12172-120">Azure Sql Server Virtual Network Rule name</span></span>

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

### <span data-ttu-id="12172-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="12172-121">-Confirm</span></span>
<span data-ttu-id="12172-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12172-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12172-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12172-123">-WhatIf</span></span>
<span data-ttu-id="12172-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="12172-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12172-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="12172-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12172-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12172-126">CommonParameters</span></span>
<span data-ttu-id="12172-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12172-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12172-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="12172-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12172-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="12172-129">INPUTS</span></span>

### <span data-ttu-id="12172-130">System. String</span><span class="sxs-lookup"><span data-stu-id="12172-130">System.String</span></span>

## <span data-ttu-id="12172-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="12172-131">OUTPUTS</span></span>

### <span data-ttu-id="12172-132">Microsoft. Azure. Commands. Sql. VirtualNetworkRule. Model. AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="12172-132">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="12172-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="12172-133">NOTES</span></span>

## <span data-ttu-id="12172-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="12172-134">RELATED LINKS</span></span>
