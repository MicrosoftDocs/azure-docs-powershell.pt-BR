---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: C7F3E754-394A-4F93-A621-A07AF281EE45
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: b4cbf71dc4b9a04a3070bab22266ba28f88b2131
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943912"
---
# <span data-ttu-id="ebeb1-101">Get-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="ebeb1-101">Get-AzSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="ebeb1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ebeb1-102">SYNOPSIS</span></span>
<span data-ttu-id="ebeb1-103">Obtém uma configuração de recuperação do sistema de servidor de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="ebeb1-103">Gets a database server system recovery configuration.</span></span>

## <span data-ttu-id="ebeb1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ebeb1-104">SYNTAX</span></span>

```
Get-AzSqlServerDisasterRecoveryConfiguration [-VirtualEndpointName <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ebeb1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ebeb1-105">DESCRIPTION</span></span>
<span data-ttu-id="ebeb1-106">O cmdlet **Get-AzSqlServerDisasterRecoveryConfiguration** Obtém uma configuração de recuperação do sistema de servidor de banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="ebeb1-106">The **Get-AzSqlServerDisasterRecoveryConfiguration** cmdlet gets a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="ebeb1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ebeb1-107">EXAMPLES</span></span>

## <span data-ttu-id="ebeb1-108">OS</span><span class="sxs-lookup"><span data-stu-id="ebeb1-108">PARAMETERS</span></span>

### <span data-ttu-id="ebeb1-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebeb1-109">-DefaultProfile</span></span>
<span data-ttu-id="ebeb1-110">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="ebeb1-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ebeb1-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ebeb1-111">-ResourceGroupName</span></span>
<span data-ttu-id="ebeb1-112">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ebeb1-112">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="ebeb1-113">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="ebeb1-113">-ServerName</span></span>
<span data-ttu-id="ebeb1-114">Especifica o nome do servidor de banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="ebeb1-114">Specifies the name of SQL database server.</span></span>

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

### <span data-ttu-id="ebeb1-115">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="ebeb1-115">-VirtualEndpointName</span></span>
<span data-ttu-id="ebeb1-116">Especifica o nome do ponto de extremidade virtual.</span><span class="sxs-lookup"><span data-stu-id="ebeb1-116">Specifies the name of the virtual end point.</span></span>

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

### <span data-ttu-id="ebeb1-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ebeb1-117">-Confirm</span></span>
<span data-ttu-id="ebeb1-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ebeb1-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ebeb1-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ebeb1-119">-WhatIf</span></span>
<span data-ttu-id="ebeb1-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ebeb1-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ebeb1-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ebeb1-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ebeb1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebeb1-122">CommonParameters</span></span>
<span data-ttu-id="ebeb1-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ebeb1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebeb1-124">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ebeb1-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebeb1-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ebeb1-125">INPUTS</span></span>

### <span data-ttu-id="ebeb1-126">System. String</span><span class="sxs-lookup"><span data-stu-id="ebeb1-126">System.String</span></span>

## <span data-ttu-id="ebeb1-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ebeb1-127">OUTPUTS</span></span>

### <span data-ttu-id="ebeb1-128">Microsoft. Azure. Commands. Sql. ServerDisasterRecoveryConfiguration. Model. AzureSqlServerDisasterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="ebeb1-128">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="ebeb1-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ebeb1-129">NOTES</span></span>

## <span data-ttu-id="ebeb1-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ebeb1-130">RELATED LINKS</span></span>

[<span data-ttu-id="ebeb1-131">New-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="ebeb1-131">New-AzSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="ebeb1-132">Remove-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="ebeb1-132">Remove-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="ebeb1-133">Set-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="ebeb1-133">Set-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="ebeb1-134">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="ebeb1-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

