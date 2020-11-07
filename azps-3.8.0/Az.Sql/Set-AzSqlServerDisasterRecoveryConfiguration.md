---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 44F8EFF4-8E3D-4657-9D17-2A3F49CEA515
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: c49eb386265dff2650ba9bdb0882d25be98fca0c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93778002"
---
# <span data-ttu-id="25841-101">Set-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="25841-101">Set-AzSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="25841-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="25841-102">SYNOPSIS</span></span>
<span data-ttu-id="25841-103">Modifica uma configuração de recuperação do servidor de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="25841-103">Modifies a database server recovery configuration.</span></span>

## <span data-ttu-id="25841-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="25841-104">SYNTAX</span></span>

```
Set-AzSqlServerDisasterRecoveryConfiguration -VirtualEndpointName <String> [-Failover] [-AllowDataLoss]
 [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25841-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="25841-105">DESCRIPTION</span></span>
<span data-ttu-id="25841-106">O cmdlet **set-AzSqlServerDisasterRecoveryConfiguration** modifica uma configuração de recuperação do servidor de banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="25841-106">The **Set-AzSqlServerDisasterRecoveryConfiguration** cmdlet modifies a SQL database server recovery configuration.</span></span>

## <span data-ttu-id="25841-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="25841-107">EXAMPLES</span></span>

## <span data-ttu-id="25841-108">OS</span><span class="sxs-lookup"><span data-stu-id="25841-108">PARAMETERS</span></span>

### <span data-ttu-id="25841-109">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="25841-109">-AllowDataLoss</span></span>
<span data-ttu-id="25841-110">Indica que a operação de failover permite perda de dados.</span><span class="sxs-lookup"><span data-stu-id="25841-110">Indicates that the failover operation permits data loss.</span></span>

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

### <span data-ttu-id="25841-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="25841-111">-AsJob</span></span>
<span data-ttu-id="25841-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="25841-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="25841-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25841-113">-DefaultProfile</span></span>
<span data-ttu-id="25841-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="25841-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="25841-115">-Failover</span><span class="sxs-lookup"><span data-stu-id="25841-115">-Failover</span></span>
<span data-ttu-id="25841-116">Indica que essa operação é um failover.</span><span class="sxs-lookup"><span data-stu-id="25841-116">Indicates that this operation is a failover.</span></span>

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

### <span data-ttu-id="25841-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25841-117">-ResourceGroupName</span></span>
<span data-ttu-id="25841-118">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="25841-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="25841-119">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="25841-119">-ServerName</span></span>
<span data-ttu-id="25841-120">Especifica o nome de um servidor de banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="25841-120">Specifies the name of a SQL database server.</span></span>

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

### <span data-ttu-id="25841-121">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="25841-121">-VirtualEndpointName</span></span>
<span data-ttu-id="25841-122">Especifica o nome de um ponto de extremidade virtual.</span><span class="sxs-lookup"><span data-stu-id="25841-122">Specifies the name of a virtual end point.</span></span>

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

### <span data-ttu-id="25841-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="25841-123">-Confirm</span></span>
<span data-ttu-id="25841-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="25841-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25841-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25841-125">-WhatIf</span></span>
<span data-ttu-id="25841-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="25841-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25841-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="25841-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25841-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25841-128">CommonParameters</span></span>
<span data-ttu-id="25841-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25841-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25841-130">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="25841-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25841-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="25841-131">INPUTS</span></span>

### <span data-ttu-id="25841-132">System. String</span><span class="sxs-lookup"><span data-stu-id="25841-132">System.String</span></span>

## <span data-ttu-id="25841-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="25841-133">OUTPUTS</span></span>

### <span data-ttu-id="25841-134">Microsoft. Azure. Commands. Sql. ServerDisasterRecoveryConfiguration. Model. AzureSqlServerDisasterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="25841-134">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="25841-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="25841-135">NOTES</span></span>

## <span data-ttu-id="25841-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="25841-136">RELATED LINKS</span></span>

[<span data-ttu-id="25841-137">Get-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="25841-137">Get-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="25841-138">New-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="25841-138">New-AzSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="25841-139">Remove-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="25841-139">Remove-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="25841-140">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="25841-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
