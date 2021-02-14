---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 1D8E8599-113C-4852-8416-1F3359071047
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: a294fd3db4ded19dba2ebd55547ec1c6cbfa9c68
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111312"
---
# <span data-ttu-id="48f25-101">New-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="48f25-101">New-AzSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="48f25-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="48f25-102">SYNOPSIS</span></span>
<span data-ttu-id="48f25-103">Cria uma configuração de recuperação do sistema de servidor de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="48f25-103">Creates a database server system recovery configuration.</span></span>

## <span data-ttu-id="48f25-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="48f25-104">SYNTAX</span></span>

```
New-AzSqlServerDisasterRecoveryConfiguration -VirtualEndpointName <String> -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-FailoverPolicy <String>] [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="48f25-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="48f25-105">DESCRIPTION</span></span>
<span data-ttu-id="48f25-106">O cmdlet **New-AzSqlServerDisasterRecoveryConfiguration** cria uma configuração de recuperação do sistema do servidor de banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="48f25-106">The **New-AzSqlServerDisasterRecoveryConfiguration** cmdlet creates a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="48f25-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="48f25-107">EXAMPLES</span></span>

## <span data-ttu-id="48f25-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="48f25-108">PARAMETERS</span></span>

### <span data-ttu-id="48f25-109">-AsJob</span><span class="sxs-lookup"><span data-stu-id="48f25-109">-AsJob</span></span>
<span data-ttu-id="48f25-110">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="48f25-110">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="48f25-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48f25-111">-DefaultProfile</span></span>
<span data-ttu-id="48f25-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="48f25-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="48f25-113">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="48f25-113">-FailoverPolicy</span></span>
<span data-ttu-id="48f25-114">Especifica a política de failover.</span><span class="sxs-lookup"><span data-stu-id="48f25-114">Specifies the failover policy.</span></span>

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

### <span data-ttu-id="48f25-115">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48f25-115">-PartnerResourceGroupName</span></span>
<span data-ttu-id="48f25-116">Especifica o nome do grupo de recursos do parceiro.</span><span class="sxs-lookup"><span data-stu-id="48f25-116">Specifies the name of the partner resource group.</span></span>

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

### <span data-ttu-id="48f25-117">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="48f25-117">-PartnerServerName</span></span>
<span data-ttu-id="48f25-118">Especifica o nome do servidor parceiro.</span><span class="sxs-lookup"><span data-stu-id="48f25-118">Specifies the name of the partner server.</span></span>

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

### <span data-ttu-id="48f25-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48f25-119">-ResourceGroupName</span></span>
<span data-ttu-id="48f25-120">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="48f25-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="48f25-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="48f25-121">-ServerName</span></span>
<span data-ttu-id="48f25-122">Especifica o nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="48f25-122">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="48f25-123">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="48f25-123">-VirtualEndpointName</span></span>
<span data-ttu-id="48f25-124">Especifica o nome do ponto de extremidade virtual.</span><span class="sxs-lookup"><span data-stu-id="48f25-124">Specifies the name of the virtual end point.</span></span>

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

### <span data-ttu-id="48f25-125">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="48f25-125">-Confirm</span></span>
<span data-ttu-id="48f25-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="48f25-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48f25-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48f25-127">-WhatIf</span></span>
<span data-ttu-id="48f25-128">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="48f25-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48f25-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="48f25-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48f25-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48f25-130">CommonParameters</span></span>
<span data-ttu-id="48f25-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48f25-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48f25-132">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="48f25-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48f25-133">Entradas</span><span class="sxs-lookup"><span data-stu-id="48f25-133">INPUTS</span></span>

### <span data-ttu-id="48f25-134">System.String</span><span class="sxs-lookup"><span data-stu-id="48f25-134">System.String</span></span>

## <span data-ttu-id="48f25-135">Saídas</span><span class="sxs-lookup"><span data-stu-id="48f25-135">OUTPUTS</span></span>

### <span data-ttu-id="48f25-136">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="48f25-136">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="48f25-137">Notas</span><span class="sxs-lookup"><span data-stu-id="48f25-137">NOTES</span></span>

## <span data-ttu-id="48f25-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="48f25-138">RELATED LINKS</span></span>

[<span data-ttu-id="48f25-139">Get-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="48f25-139">Get-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="48f25-140">Remove-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="48f25-140">Remove-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="48f25-141">Set-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="48f25-141">Set-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="48f25-142">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="48f25-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
