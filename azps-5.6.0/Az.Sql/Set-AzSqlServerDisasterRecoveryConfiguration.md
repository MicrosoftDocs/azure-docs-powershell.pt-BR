---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 44F8EFF4-8E3D-4657-9D17-2A3F49CEA515
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: a1f91c01d3183551cbabf58754fbe628e1feea32
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890578"
---
# <span data-ttu-id="81ce4-101">Set-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="81ce4-101">Set-AzSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="81ce4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81ce4-102">SYNOPSIS</span></span>
<span data-ttu-id="81ce4-103">Modifica uma configuração de recuperação de servidor de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="81ce4-103">Modifies a database server recovery configuration.</span></span>

## <span data-ttu-id="81ce4-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="81ce4-104">SYNTAX</span></span>

```
Set-AzSqlServerDisasterRecoveryConfiguration -VirtualEndpointName <String> [-Failover] [-AllowDataLoss]
 [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81ce4-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="81ce4-105">DESCRIPTION</span></span>
<span data-ttu-id="81ce4-106">O cmdlet **Set-AzSqlServerDisasterRecoveryConfiguration** modifica uma configuração de recuperação SQL servidor de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="81ce4-106">The **Set-AzSqlServerDisasterRecoveryConfiguration** cmdlet modifies a SQL database server recovery configuration.</span></span>

## <span data-ttu-id="81ce4-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="81ce4-107">EXAMPLES</span></span>

## <span data-ttu-id="81ce4-108">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="81ce4-108">PARAMETERS</span></span>

### <span data-ttu-id="81ce4-109">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="81ce4-109">-AllowDataLoss</span></span>
<span data-ttu-id="81ce4-110">Indica que a operação de failover permite a perda de dados.</span><span class="sxs-lookup"><span data-stu-id="81ce4-110">Indicates that the failover operation permits data loss.</span></span>

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

### <span data-ttu-id="81ce4-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="81ce4-111">-AsJob</span></span>
<span data-ttu-id="81ce4-112">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="81ce4-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81ce4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81ce4-113">-DefaultProfile</span></span>
<span data-ttu-id="81ce4-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="81ce4-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="81ce4-115">-Failover</span><span class="sxs-lookup"><span data-stu-id="81ce4-115">-Failover</span></span>
<span data-ttu-id="81ce4-116">Indica que essa operação é um failover.</span><span class="sxs-lookup"><span data-stu-id="81ce4-116">Indicates that this operation is a failover.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81ce4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81ce4-117">-ResourceGroupName</span></span>
<span data-ttu-id="81ce4-118">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="81ce4-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="81ce4-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="81ce4-119">-ServerName</span></span>
<span data-ttu-id="81ce4-120">Especifica o nome de um servidor SQL banco de dados.</span><span class="sxs-lookup"><span data-stu-id="81ce4-120">Specifies the name of a SQL database server.</span></span>

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

### <span data-ttu-id="81ce4-121">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="81ce4-121">-VirtualEndpointName</span></span>
<span data-ttu-id="81ce4-122">Especifica o nome de um ponto de extremidade virtual.</span><span class="sxs-lookup"><span data-stu-id="81ce4-122">Specifies the name of a virtual end point.</span></span>

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

### <span data-ttu-id="81ce4-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="81ce4-123">-Confirm</span></span>
<span data-ttu-id="81ce4-124">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81ce4-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81ce4-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81ce4-125">-WhatIf</span></span>
<span data-ttu-id="81ce4-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="81ce4-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81ce4-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="81ce4-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81ce4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81ce4-128">CommonParameters</span></span>
<span data-ttu-id="81ce4-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81ce4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81ce4-130">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="81ce4-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81ce4-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="81ce4-131">INPUTS</span></span>

### <span data-ttu-id="81ce4-132">System.String</span><span class="sxs-lookup"><span data-stu-id="81ce4-132">System.String</span></span>

## <span data-ttu-id="81ce4-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="81ce4-133">OUTPUTS</span></span>

### <span data-ttu-id="81ce4-134">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="81ce4-134">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="81ce4-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="81ce4-135">NOTES</span></span>

## <span data-ttu-id="81ce4-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="81ce4-136">RELATED LINKS</span></span>

[<span data-ttu-id="81ce4-137">Get-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="81ce4-137">Get-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="81ce4-138">New-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="81ce4-138">New-AzSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="81ce4-139">Remove-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="81ce4-139">Remove-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="81ce4-140">SQL documentação do banco de dados</span><span class="sxs-lookup"><span data-stu-id="81ce4-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
