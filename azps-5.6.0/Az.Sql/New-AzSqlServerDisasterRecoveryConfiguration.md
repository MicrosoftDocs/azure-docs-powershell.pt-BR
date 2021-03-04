---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 1D8E8599-113C-4852-8416-1F3359071047
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: e9fd76953d4cf760c501370b77be3301cb043524
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887950"
---
# <span data-ttu-id="99ff9-101">New-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="99ff9-101">New-AzSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="99ff9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99ff9-102">SYNOPSIS</span></span>
<span data-ttu-id="99ff9-103">Cria uma configuração de recuperação do sistema do servidor de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="99ff9-103">Creates a database server system recovery configuration.</span></span>

## <span data-ttu-id="99ff9-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="99ff9-104">SYNTAX</span></span>

```
New-AzSqlServerDisasterRecoveryConfiguration -VirtualEndpointName <String> -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-FailoverPolicy <String>] [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="99ff9-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="99ff9-105">DESCRIPTION</span></span>
<span data-ttu-id="99ff9-106">O cmdlet **New-AzSqlServerDisasterRecoveryConfiguration** cria uma configuração SQL recuperação do sistema do servidor de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="99ff9-106">The **New-AzSqlServerDisasterRecoveryConfiguration** cmdlet creates a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="99ff9-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="99ff9-107">EXAMPLES</span></span>

## <span data-ttu-id="99ff9-108">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="99ff9-108">PARAMETERS</span></span>

### <span data-ttu-id="99ff9-109">-AsJob</span><span class="sxs-lookup"><span data-stu-id="99ff9-109">-AsJob</span></span>
<span data-ttu-id="99ff9-110">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="99ff9-110">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="99ff9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99ff9-111">-DefaultProfile</span></span>
<span data-ttu-id="99ff9-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="99ff9-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="99ff9-113">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="99ff9-113">-FailoverPolicy</span></span>
<span data-ttu-id="99ff9-114">Especifica a política de failover.</span><span class="sxs-lookup"><span data-stu-id="99ff9-114">Specifies the failover policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99ff9-115">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99ff9-115">-PartnerResourceGroupName</span></span>
<span data-ttu-id="99ff9-116">Especifica o nome do grupo de recursos do parceiro.</span><span class="sxs-lookup"><span data-stu-id="99ff9-116">Specifies the name of the partner resource group.</span></span>

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

### <span data-ttu-id="99ff9-117">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="99ff9-117">-PartnerServerName</span></span>
<span data-ttu-id="99ff9-118">Especifica o nome do servidor parceiro.</span><span class="sxs-lookup"><span data-stu-id="99ff9-118">Specifies the name of the partner server.</span></span>

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

### <span data-ttu-id="99ff9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99ff9-119">-ResourceGroupName</span></span>
<span data-ttu-id="99ff9-120">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="99ff9-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="99ff9-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="99ff9-121">-ServerName</span></span>
<span data-ttu-id="99ff9-122">Especifica o nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="99ff9-122">Specifies the name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99ff9-123">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="99ff9-123">-VirtualEndpointName</span></span>
<span data-ttu-id="99ff9-124">Especifica o nome do ponto de extremidade virtual.</span><span class="sxs-lookup"><span data-stu-id="99ff9-124">Specifies the name of the virtual end point.</span></span>

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

### <span data-ttu-id="99ff9-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="99ff9-125">-Confirm</span></span>
<span data-ttu-id="99ff9-126">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="99ff9-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99ff9-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99ff9-127">-WhatIf</span></span>
<span data-ttu-id="99ff9-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="99ff9-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99ff9-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="99ff9-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99ff9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99ff9-130">CommonParameters</span></span>
<span data-ttu-id="99ff9-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99ff9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99ff9-132">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="99ff9-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99ff9-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="99ff9-133">INPUTS</span></span>

### <span data-ttu-id="99ff9-134">System.String</span><span class="sxs-lookup"><span data-stu-id="99ff9-134">System.String</span></span>

## <span data-ttu-id="99ff9-135">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="99ff9-135">OUTPUTS</span></span>

### <span data-ttu-id="99ff9-136">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="99ff9-136">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="99ff9-137">NOTES</span><span class="sxs-lookup"><span data-stu-id="99ff9-137">NOTES</span></span>

## <span data-ttu-id="99ff9-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="99ff9-138">RELATED LINKS</span></span>

[<span data-ttu-id="99ff9-139">Get-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="99ff9-139">Get-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="99ff9-140">Remove-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="99ff9-140">Remove-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="99ff9-141">Set-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="99ff9-141">Set-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="99ff9-142">SQL documentação do banco de dados</span><span class="sxs-lookup"><span data-stu-id="99ff9-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
