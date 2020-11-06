---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 1D8E8599-113C-4852-8416-1F3359071047
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: 06d0b7eae38459943872926b640a0f48b2e28b08
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427747"
---
# <span data-ttu-id="dff78-101">New-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="dff78-101">New-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="dff78-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dff78-102">SYNOPSIS</span></span>
<span data-ttu-id="dff78-103">Cria uma configuração de recuperação do sistema de servidor de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="dff78-103">Creates a database server system recovery configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dff78-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dff78-104">SYNTAX</span></span>

```
New-AzureRmSqlServerDisasterRecoveryConfiguration -VirtualEndpointName <String>
 -PartnerResourceGroupName <String> -PartnerServerName <String> [-FailoverPolicy <String>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dff78-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dff78-105">DESCRIPTION</span></span>
<span data-ttu-id="dff78-106">O cmdlet **New-AzureRmSqlServerDisasterRecoveryConfiguration** cria uma configuração de recuperação do sistema de servidor de banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="dff78-106">The **New-AzureRmSqlServerDisasterRecoveryConfiguration** cmdlet creates a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="dff78-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dff78-107">EXAMPLES</span></span>

## <span data-ttu-id="dff78-108">OS</span><span class="sxs-lookup"><span data-stu-id="dff78-108">PARAMETERS</span></span>

### <span data-ttu-id="dff78-109">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="dff78-109">-FailoverPolicy</span></span>
<span data-ttu-id="dff78-110">Especifica a política de failover.</span><span class="sxs-lookup"><span data-stu-id="dff78-110">Specifies the failover policy.</span></span>

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

### <span data-ttu-id="dff78-111">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dff78-111">-PartnerResourceGroupName</span></span>
<span data-ttu-id="dff78-112">Especifica o nome do grupo de recursos do parceiro.</span><span class="sxs-lookup"><span data-stu-id="dff78-112">Specifies the name of the partner resource group.</span></span>

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

### <span data-ttu-id="dff78-113">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="dff78-113">-PartnerServerName</span></span>
<span data-ttu-id="dff78-114">Especifica o nome do servidor parceiro.</span><span class="sxs-lookup"><span data-stu-id="dff78-114">Specifies the name of the partner server.</span></span>

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

### <span data-ttu-id="dff78-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dff78-115">-ResourceGroupName</span></span>
<span data-ttu-id="dff78-116">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="dff78-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="dff78-117">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="dff78-117">-ServerName</span></span>
<span data-ttu-id="dff78-118">Especifica o nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="dff78-118">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="dff78-119">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="dff78-119">-VirtualEndpointName</span></span>
<span data-ttu-id="dff78-120">Especifica o nome do ponto de extremidade virtual.</span><span class="sxs-lookup"><span data-stu-id="dff78-120">Specifies the name of the virtual end point.</span></span>

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

### <span data-ttu-id="dff78-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="dff78-121">-Confirm</span></span>
<span data-ttu-id="dff78-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dff78-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dff78-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dff78-123">-WhatIf</span></span>
<span data-ttu-id="dff78-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="dff78-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dff78-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="dff78-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dff78-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dff78-126">-DefaultProfile</span></span>
<span data-ttu-id="dff78-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dff78-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dff78-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dff78-128">CommonParameters</span></span>
<span data-ttu-id="dff78-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dff78-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dff78-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dff78-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dff78-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dff78-131">INPUTS</span></span>

## <span data-ttu-id="dff78-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dff78-132">OUTPUTS</span></span>

## <span data-ttu-id="dff78-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dff78-133">NOTES</span></span>

## <span data-ttu-id="dff78-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dff78-134">RELATED LINKS</span></span>

[<span data-ttu-id="dff78-135">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="dff78-135">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="dff78-136">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="dff78-136">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="dff78-137">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="dff78-137">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="dff78-138">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="dff78-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)