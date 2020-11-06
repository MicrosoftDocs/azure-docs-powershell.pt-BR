---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 44F8EFF4-8E3D-4657-9D17-2A3F49CEA515
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: 19f7d8adf7e8eae48bb85c19c9f01c61dc741da0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429307"
---
# <span data-ttu-id="4040c-101">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="4040c-101">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="4040c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4040c-102">SYNOPSIS</span></span>
<span data-ttu-id="4040c-103">Modifica uma configuração de recuperação do servidor de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="4040c-103">Modifies a database server recovery configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4040c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4040c-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerDisasterRecoveryConfiguration -VirtualEndpointName <String> [-Failover] [-AllowDataLoss]
 [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4040c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4040c-105">DESCRIPTION</span></span>
<span data-ttu-id="4040c-106">O cmdlet **set-AzureRmSqlServerDisasterRecoveryConfiguration** modifica uma configuração de recuperação do servidor de banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="4040c-106">The **Set-AzureRmSqlServerDisasterRecoveryConfiguration** cmdlet modifies a SQL database server recovery configuration.</span></span>

## <span data-ttu-id="4040c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4040c-107">EXAMPLES</span></span>

## <span data-ttu-id="4040c-108">OS</span><span class="sxs-lookup"><span data-stu-id="4040c-108">PARAMETERS</span></span>

### <span data-ttu-id="4040c-109">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="4040c-109">-AllowDataLoss</span></span>
<span data-ttu-id="4040c-110">Indica que a operação de failover permite perda de dados.</span><span class="sxs-lookup"><span data-stu-id="4040c-110">Indicates that the failover operation permits data loss.</span></span>

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

### <span data-ttu-id="4040c-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4040c-111">-AsJob</span></span>
<span data-ttu-id="4040c-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="4040c-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4040c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4040c-113">-DefaultProfile</span></span>
<span data-ttu-id="4040c-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="4040c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4040c-115">-Failover</span><span class="sxs-lookup"><span data-stu-id="4040c-115">-Failover</span></span>
<span data-ttu-id="4040c-116">Indica que essa operação é um failover.</span><span class="sxs-lookup"><span data-stu-id="4040c-116">Indicates that this operation is a failover.</span></span>

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

### <span data-ttu-id="4040c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4040c-117">-ResourceGroupName</span></span>
<span data-ttu-id="4040c-118">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4040c-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="4040c-119">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="4040c-119">-ServerName</span></span>
<span data-ttu-id="4040c-120">Especifica o nome de um servidor de banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="4040c-120">Specifies the name of a SQL database server.</span></span>

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

### <span data-ttu-id="4040c-121">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="4040c-121">-VirtualEndpointName</span></span>
<span data-ttu-id="4040c-122">Especifica o nome de um ponto de extremidade virtual.</span><span class="sxs-lookup"><span data-stu-id="4040c-122">Specifies the name of a virtual end point.</span></span>

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

### <span data-ttu-id="4040c-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4040c-123">-Confirm</span></span>
<span data-ttu-id="4040c-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4040c-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4040c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4040c-125">-WhatIf</span></span>
<span data-ttu-id="4040c-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4040c-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4040c-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4040c-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4040c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4040c-128">CommonParameters</span></span>
<span data-ttu-id="4040c-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4040c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4040c-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4040c-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4040c-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4040c-131">INPUTS</span></span>

### <span data-ttu-id="4040c-132">System. String</span><span class="sxs-lookup"><span data-stu-id="4040c-132">System.String</span></span>

## <span data-ttu-id="4040c-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4040c-133">OUTPUTS</span></span>

### <span data-ttu-id="4040c-134">Microsoft. Azure. Commands. Sql. ServerDisasterRecoveryConfiguration. Model. AzureSqlServerDisasterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="4040c-134">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="4040c-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4040c-135">NOTES</span></span>

## <span data-ttu-id="4040c-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4040c-136">RELATED LINKS</span></span>

[<span data-ttu-id="4040c-137">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="4040c-137">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="4040c-138">New-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="4040c-138">New-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="4040c-139">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="4040c-139">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="4040c-140">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="4040c-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
