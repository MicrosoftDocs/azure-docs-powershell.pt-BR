---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 265600b201a6333b8dcd7c14f0cefe429f92619e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113721"
---
# <span data-ttu-id="11cf2-101">Remove-AzSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="11cf2-101">Remove-AzSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="11cf2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="11cf2-102">SYNOPSIS</span></span>
<span data-ttu-id="11cf2-103">Exclui uma Regra de Rede Virtual do SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="11cf2-103">Deletes an Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="11cf2-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="11cf2-104">SYNTAX</span></span>

```
Remove-AzSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> [-AsJob] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="11cf2-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="11cf2-105">DESCRIPTION</span></span>
<span data-ttu-id="11cf2-106">Esse comando exclui uma Regra de Rede Virtual do SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="11cf2-106">This command deletes an Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="11cf2-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="11cf2-107">EXAMPLES</span></span>

### <span data-ttu-id="11cf2-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="11cf2-108">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Remove-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName
```

<span data-ttu-id="11cf2-109">Exclui uma regra de rede virtual existente do Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="11cf2-109">Deletes an existing Azure SQL Server virtual network rule</span></span>

## <span data-ttu-id="11cf2-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="11cf2-110">PARAMETERS</span></span>

### <span data-ttu-id="11cf2-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="11cf2-111">-AsJob</span></span>
<span data-ttu-id="11cf2-112">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="11cf2-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="11cf2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11cf2-113">-DefaultProfile</span></span>
<span data-ttu-id="11cf2-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="11cf2-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="11cf2-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11cf2-115">-ResourceGroupName</span></span>
<span data-ttu-id="11cf2-116">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="11cf2-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="11cf2-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="11cf2-117">-ServerName</span></span>
<span data-ttu-id="11cf2-118">O nome do Sql Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="11cf2-118">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="11cf2-119">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="11cf2-119">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="11cf2-120">Nome da Regra de Rede Virtual do Azure Sql Server</span><span class="sxs-lookup"><span data-stu-id="11cf2-120">Azure Sql Server Virtual Network Rule name</span></span>

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

### <span data-ttu-id="11cf2-121">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="11cf2-121">-Confirm</span></span>
<span data-ttu-id="11cf2-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11cf2-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11cf2-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11cf2-123">-WhatIf</span></span>
<span data-ttu-id="11cf2-124">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="11cf2-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11cf2-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="11cf2-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11cf2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11cf2-126">CommonParameters</span></span>
<span data-ttu-id="11cf2-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11cf2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11cf2-128">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="11cf2-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11cf2-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="11cf2-129">INPUTS</span></span>

### <span data-ttu-id="11cf2-130">System.String</span><span class="sxs-lookup"><span data-stu-id="11cf2-130">System.String</span></span>

## <span data-ttu-id="11cf2-131">Saídas</span><span class="sxs-lookup"><span data-stu-id="11cf2-131">OUTPUTS</span></span>

### <span data-ttu-id="11cf2-132">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="11cf2-132">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="11cf2-133">Notas</span><span class="sxs-lookup"><span data-stu-id="11cf2-133">NOTES</span></span>

## <span data-ttu-id="11cf2-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="11cf2-134">RELATED LINKS</span></span>
