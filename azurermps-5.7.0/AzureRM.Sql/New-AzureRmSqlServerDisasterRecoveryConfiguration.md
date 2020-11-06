---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 1D8E8599-113C-4852-8416-1F3359071047
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: 1fb3f802971f6724545c7006ed67ff01da4d7842
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431566"
---
# <span data-ttu-id="0e393-101">New-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="0e393-101">New-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="0e393-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0e393-102">SYNOPSIS</span></span>
<span data-ttu-id="0e393-103">Cria uma configuração de recuperação do sistema de servidor de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="0e393-103">Creates a database server system recovery configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0e393-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0e393-104">SYNTAX</span></span>

```
New-AzureRmSqlServerDisasterRecoveryConfiguration -VirtualEndpointName <String>
 -PartnerResourceGroupName <String> -PartnerServerName <String> [-FailoverPolicy <String>] [-AsJob]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e393-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0e393-105">DESCRIPTION</span></span>
<span data-ttu-id="0e393-106">O cmdlet **New-AzureRmSqlServerDisasterRecoveryConfiguration** cria uma configuração de recuperação do sistema de servidor de banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="0e393-106">The **New-AzureRmSqlServerDisasterRecoveryConfiguration** cmdlet creates a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="0e393-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0e393-107">EXAMPLES</span></span>

## <span data-ttu-id="0e393-108">OS</span><span class="sxs-lookup"><span data-stu-id="0e393-108">PARAMETERS</span></span>

### <span data-ttu-id="0e393-109">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0e393-109">-AsJob</span></span>
<span data-ttu-id="0e393-110">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="0e393-110">Run cmdlet in the background</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e393-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e393-111">-DefaultProfile</span></span>
<span data-ttu-id="0e393-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="0e393-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e393-113">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="0e393-113">-FailoverPolicy</span></span>
<span data-ttu-id="0e393-114">Especifica a política de failover.</span><span class="sxs-lookup"><span data-stu-id="0e393-114">Specifies the failover policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e393-115">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e393-115">-PartnerResourceGroupName</span></span>
<span data-ttu-id="0e393-116">Especifica o nome do grupo de recursos do parceiro.</span><span class="sxs-lookup"><span data-stu-id="0e393-116">Specifies the name of the partner resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e393-117">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="0e393-117">-PartnerServerName</span></span>
<span data-ttu-id="0e393-118">Especifica o nome do servidor parceiro.</span><span class="sxs-lookup"><span data-stu-id="0e393-118">Specifies the name of the partner server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e393-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e393-119">-ResourceGroupName</span></span>
<span data-ttu-id="0e393-120">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0e393-120">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e393-121">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="0e393-121">-ServerName</span></span>
<span data-ttu-id="0e393-122">Especifica o nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="0e393-122">Specifies the name of the server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e393-123">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="0e393-123">-VirtualEndpointName</span></span>
<span data-ttu-id="0e393-124">Especifica o nome do ponto de extremidade virtual.</span><span class="sxs-lookup"><span data-stu-id="0e393-124">Specifies the name of the virtual end point.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e393-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0e393-125">-Confirm</span></span>
<span data-ttu-id="0e393-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0e393-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e393-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e393-127">-WhatIf</span></span>
<span data-ttu-id="0e393-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0e393-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e393-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0e393-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e393-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e393-130">CommonParameters</span></span>
<span data-ttu-id="0e393-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e393-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e393-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e393-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e393-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0e393-133">INPUTS</span></span>

### <span data-ttu-id="0e393-134">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="0e393-134">None</span></span>
<span data-ttu-id="0e393-135">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="0e393-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0e393-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0e393-136">OUTPUTS</span></span>

## <span data-ttu-id="0e393-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0e393-137">NOTES</span></span>

## <span data-ttu-id="0e393-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0e393-138">RELATED LINKS</span></span>

[<span data-ttu-id="0e393-139">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="0e393-139">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="0e393-140">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="0e393-140">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="0e393-141">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="0e393-141">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="0e393-142">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="0e393-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
