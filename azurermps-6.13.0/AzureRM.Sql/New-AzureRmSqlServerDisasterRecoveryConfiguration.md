---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 1D8E8599-113C-4852-8416-1F3359071047
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: c583de368f549fdcd2916e7002829fc206350fc9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427138"
---
# <span data-ttu-id="eaaee-101">New-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="eaaee-101">New-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="eaaee-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="eaaee-102">SYNOPSIS</span></span>
<span data-ttu-id="eaaee-103">Cria uma configuração de recuperação do sistema de servidor de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="eaaee-103">Creates a database server system recovery configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eaaee-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="eaaee-104">SYNTAX</span></span>

```
New-AzureRmSqlServerDisasterRecoveryConfiguration -VirtualEndpointName <String>
 -PartnerResourceGroupName <String> -PartnerServerName <String> [-FailoverPolicy <String>] [-AsJob]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eaaee-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="eaaee-105">DESCRIPTION</span></span>
<span data-ttu-id="eaaee-106">O cmdlet **New-AzureRmSqlServerDisasterRecoveryConfiguration** cria uma configuração de recuperação do sistema de servidor de banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="eaaee-106">The **New-AzureRmSqlServerDisasterRecoveryConfiguration** cmdlet creates a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="eaaee-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="eaaee-107">EXAMPLES</span></span>

## <span data-ttu-id="eaaee-108">OS</span><span class="sxs-lookup"><span data-stu-id="eaaee-108">PARAMETERS</span></span>

### <span data-ttu-id="eaaee-109">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eaaee-109">-AsJob</span></span>
<span data-ttu-id="eaaee-110">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="eaaee-110">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="eaaee-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eaaee-111">-DefaultProfile</span></span>
<span data-ttu-id="eaaee-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="eaaee-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eaaee-113">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="eaaee-113">-FailoverPolicy</span></span>
<span data-ttu-id="eaaee-114">Especifica a política de failover.</span><span class="sxs-lookup"><span data-stu-id="eaaee-114">Specifies the failover policy.</span></span>

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

### <span data-ttu-id="eaaee-115">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eaaee-115">-PartnerResourceGroupName</span></span>
<span data-ttu-id="eaaee-116">Especifica o nome do grupo de recursos do parceiro.</span><span class="sxs-lookup"><span data-stu-id="eaaee-116">Specifies the name of the partner resource group.</span></span>

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

### <span data-ttu-id="eaaee-117">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="eaaee-117">-PartnerServerName</span></span>
<span data-ttu-id="eaaee-118">Especifica o nome do servidor parceiro.</span><span class="sxs-lookup"><span data-stu-id="eaaee-118">Specifies the name of the partner server.</span></span>

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

### <span data-ttu-id="eaaee-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eaaee-119">-ResourceGroupName</span></span>
<span data-ttu-id="eaaee-120">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="eaaee-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="eaaee-121">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="eaaee-121">-ServerName</span></span>
<span data-ttu-id="eaaee-122">Especifica o nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="eaaee-122">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="eaaee-123">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="eaaee-123">-VirtualEndpointName</span></span>
<span data-ttu-id="eaaee-124">Especifica o nome do ponto de extremidade virtual.</span><span class="sxs-lookup"><span data-stu-id="eaaee-124">Specifies the name of the virtual end point.</span></span>

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

### <span data-ttu-id="eaaee-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="eaaee-125">-Confirm</span></span>
<span data-ttu-id="eaaee-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eaaee-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eaaee-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eaaee-127">-WhatIf</span></span>
<span data-ttu-id="eaaee-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="eaaee-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eaaee-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="eaaee-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eaaee-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eaaee-130">CommonParameters</span></span>
<span data-ttu-id="eaaee-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eaaee-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eaaee-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eaaee-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eaaee-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="eaaee-133">INPUTS</span></span>

### <span data-ttu-id="eaaee-134">System. String</span><span class="sxs-lookup"><span data-stu-id="eaaee-134">System.String</span></span>

## <span data-ttu-id="eaaee-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="eaaee-135">OUTPUTS</span></span>

### <span data-ttu-id="eaaee-136">Microsoft. Azure. Commands. Sql. ServerDisasterRecoveryConfiguration. Model. AzureSqlServerDisasterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="eaaee-136">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="eaaee-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="eaaee-137">NOTES</span></span>

## <span data-ttu-id="eaaee-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="eaaee-138">RELATED LINKS</span></span>

[<span data-ttu-id="eaaee-139">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="eaaee-139">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="eaaee-140">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="eaaee-140">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="eaaee-141">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="eaaee-141">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="eaaee-142">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="eaaee-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)