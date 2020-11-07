---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 1D8E8599-113C-4852-8416-1F3359071047
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: a294fd3db4ded19dba2ebd55547ec1c6cbfa9c68
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93954582"
---
# <span data-ttu-id="e62b6-101">New-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="e62b6-101">New-AzSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="e62b6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e62b6-102">SYNOPSIS</span></span>
<span data-ttu-id="e62b6-103">Cria uma configuração de recuperação do sistema de servidor de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e62b6-103">Creates a database server system recovery configuration.</span></span>

## <span data-ttu-id="e62b6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e62b6-104">SYNTAX</span></span>

```
New-AzSqlServerDisasterRecoveryConfiguration -VirtualEndpointName <String> -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-FailoverPolicy <String>] [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e62b6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e62b6-105">DESCRIPTION</span></span>
<span data-ttu-id="e62b6-106">O cmdlet **New-AzSqlServerDisasterRecoveryConfiguration** cria uma configuração de recuperação do sistema de servidor de banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="e62b6-106">The **New-AzSqlServerDisasterRecoveryConfiguration** cmdlet creates a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="e62b6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e62b6-107">EXAMPLES</span></span>

## <span data-ttu-id="e62b6-108">OS</span><span class="sxs-lookup"><span data-stu-id="e62b6-108">PARAMETERS</span></span>

### <span data-ttu-id="e62b6-109">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e62b6-109">-AsJob</span></span>
<span data-ttu-id="e62b6-110">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="e62b6-110">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e62b6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e62b6-111">-DefaultProfile</span></span>
<span data-ttu-id="e62b6-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="e62b6-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e62b6-113">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="e62b6-113">-FailoverPolicy</span></span>
<span data-ttu-id="e62b6-114">Especifica a política de failover.</span><span class="sxs-lookup"><span data-stu-id="e62b6-114">Specifies the failover policy.</span></span>

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

### <span data-ttu-id="e62b6-115">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e62b6-115">-PartnerResourceGroupName</span></span>
<span data-ttu-id="e62b6-116">Especifica o nome do grupo de recursos do parceiro.</span><span class="sxs-lookup"><span data-stu-id="e62b6-116">Specifies the name of the partner resource group.</span></span>

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

### <span data-ttu-id="e62b6-117">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="e62b6-117">-PartnerServerName</span></span>
<span data-ttu-id="e62b6-118">Especifica o nome do servidor parceiro.</span><span class="sxs-lookup"><span data-stu-id="e62b6-118">Specifies the name of the partner server.</span></span>

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

### <span data-ttu-id="e62b6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e62b6-119">-ResourceGroupName</span></span>
<span data-ttu-id="e62b6-120">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e62b6-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="e62b6-121">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="e62b6-121">-ServerName</span></span>
<span data-ttu-id="e62b6-122">Especifica o nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="e62b6-122">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="e62b6-123">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="e62b6-123">-VirtualEndpointName</span></span>
<span data-ttu-id="e62b6-124">Especifica o nome do ponto de extremidade virtual.</span><span class="sxs-lookup"><span data-stu-id="e62b6-124">Specifies the name of the virtual end point.</span></span>

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

### <span data-ttu-id="e62b6-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e62b6-125">-Confirm</span></span>
<span data-ttu-id="e62b6-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e62b6-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e62b6-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e62b6-127">-WhatIf</span></span>
<span data-ttu-id="e62b6-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e62b6-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e62b6-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e62b6-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e62b6-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e62b6-130">CommonParameters</span></span>
<span data-ttu-id="e62b6-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e62b6-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e62b6-132">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e62b6-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e62b6-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e62b6-133">INPUTS</span></span>

### <span data-ttu-id="e62b6-134">System. String</span><span class="sxs-lookup"><span data-stu-id="e62b6-134">System.String</span></span>

## <span data-ttu-id="e62b6-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e62b6-135">OUTPUTS</span></span>

### <span data-ttu-id="e62b6-136">Microsoft. Azure. Commands. Sql. ServerDisasterRecoveryConfiguration. Model. AzureSqlServerDisasterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="e62b6-136">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="e62b6-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e62b6-137">NOTES</span></span>

## <span data-ttu-id="e62b6-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e62b6-138">RELATED LINKS</span></span>

[<span data-ttu-id="e62b6-139">Get-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="e62b6-139">Get-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="e62b6-140">Remove-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="e62b6-140">Remove-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="e62b6-141">Set-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="e62b6-141">Set-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="e62b6-142">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="e62b6-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
