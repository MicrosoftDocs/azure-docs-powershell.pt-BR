---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 44F8EFF4-8E3D-4657-9D17-2A3F49CEA515
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: b3a84fc37e747cb54571bc26563789599fac3a7d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773698"
---
# <span data-ttu-id="014b3-101">Set-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="014b3-101">Set-AzSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="014b3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="014b3-102">SYNOPSIS</span></span>
<span data-ttu-id="014b3-103">Modifica uma configuração de recuperação do servidor de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="014b3-103">Modifies a database server recovery configuration.</span></span>

## <span data-ttu-id="014b3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="014b3-104">SYNTAX</span></span>

```
Set-AzSqlServerDisasterRecoveryConfiguration -VirtualEndpointName <String> [-Failover] [-AllowDataLoss]
 [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="014b3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="014b3-105">DESCRIPTION</span></span>
<span data-ttu-id="014b3-106">O cmdlet **set-AzSqlServerDisasterRecoveryConfiguration** modifica uma configuração de recuperação do servidor de banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="014b3-106">The **Set-AzSqlServerDisasterRecoveryConfiguration** cmdlet modifies a SQL database server recovery configuration.</span></span>

## <span data-ttu-id="014b3-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="014b3-107">EXAMPLES</span></span>

## <span data-ttu-id="014b3-108">OS</span><span class="sxs-lookup"><span data-stu-id="014b3-108">PARAMETERS</span></span>

### <span data-ttu-id="014b3-109">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="014b3-109">-AllowDataLoss</span></span>
<span data-ttu-id="014b3-110">Indica que a operação de failover permite perda de dados.</span><span class="sxs-lookup"><span data-stu-id="014b3-110">Indicates that the failover operation permits data loss.</span></span>

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

### <span data-ttu-id="014b3-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="014b3-111">-AsJob</span></span>
<span data-ttu-id="014b3-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="014b3-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="014b3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="014b3-113">-DefaultProfile</span></span>
<span data-ttu-id="014b3-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="014b3-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="014b3-115">-Failover</span><span class="sxs-lookup"><span data-stu-id="014b3-115">-Failover</span></span>
<span data-ttu-id="014b3-116">Indica que essa operação é um failover.</span><span class="sxs-lookup"><span data-stu-id="014b3-116">Indicates that this operation is a failover.</span></span>

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

### <span data-ttu-id="014b3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="014b3-117">-ResourceGroupName</span></span>
<span data-ttu-id="014b3-118">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="014b3-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="014b3-119">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="014b3-119">-ServerName</span></span>
<span data-ttu-id="014b3-120">Especifica o nome de um servidor de banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="014b3-120">Specifies the name of a SQL database server.</span></span>

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

### <span data-ttu-id="014b3-121">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="014b3-121">-VirtualEndpointName</span></span>
<span data-ttu-id="014b3-122">Especifica o nome de um ponto de extremidade virtual.</span><span class="sxs-lookup"><span data-stu-id="014b3-122">Specifies the name of a virtual end point.</span></span>

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

### <span data-ttu-id="014b3-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="014b3-123">-Confirm</span></span>
<span data-ttu-id="014b3-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="014b3-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="014b3-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="014b3-125">-WhatIf</span></span>
<span data-ttu-id="014b3-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="014b3-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="014b3-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="014b3-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="014b3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="014b3-128">CommonParameters</span></span>
<span data-ttu-id="014b3-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="014b3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="014b3-130">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="014b3-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="014b3-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="014b3-131">INPUTS</span></span>

### <span data-ttu-id="014b3-132">System. String</span><span class="sxs-lookup"><span data-stu-id="014b3-132">System.String</span></span>

## <span data-ttu-id="014b3-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="014b3-133">OUTPUTS</span></span>

### <span data-ttu-id="014b3-134">Microsoft. Azure. Commands. Sql. ServerDisasterRecoveryConfiguration. Model. AzureSqlServerDisasterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="014b3-134">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="014b3-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="014b3-135">NOTES</span></span>

## <span data-ttu-id="014b3-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="014b3-136">RELATED LINKS</span></span>

[<span data-ttu-id="014b3-137">Get-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="014b3-137">Get-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="014b3-138">New-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="014b3-138">New-AzSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="014b3-139">Remove-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="014b3-139">Remove-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="014b3-140">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="014b3-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
