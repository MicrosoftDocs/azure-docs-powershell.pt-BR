---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: C7F3E754-394A-4F93-A621-A07AF281EE45
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: b4cbf71dc4b9a04a3070bab22266ba28f88b2131
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118936"
---
# <span data-ttu-id="66369-101">Get-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="66369-101">Get-AzSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="66369-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="66369-102">SYNOPSIS</span></span>
<span data-ttu-id="66369-103">Obtém uma configuração de recuperação do sistema de servidor de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="66369-103">Gets a database server system recovery configuration.</span></span>

## <span data-ttu-id="66369-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="66369-104">SYNTAX</span></span>

```
Get-AzSqlServerDisasterRecoveryConfiguration [-VirtualEndpointName <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="66369-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="66369-105">DESCRIPTION</span></span>
<span data-ttu-id="66369-106">O cmdlet **Get-AzSqlServerDisasterRecoveryConfiguration** obtém uma configuração de recuperação do sistema do servidor de banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="66369-106">The **Get-AzSqlServerDisasterRecoveryConfiguration** cmdlet gets a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="66369-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="66369-107">EXAMPLES</span></span>

## <span data-ttu-id="66369-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="66369-108">PARAMETERS</span></span>

### <span data-ttu-id="66369-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66369-109">-DefaultProfile</span></span>
<span data-ttu-id="66369-110">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="66369-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="66369-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66369-111">-ResourceGroupName</span></span>
<span data-ttu-id="66369-112">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="66369-112">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="66369-113">-ServerName</span><span class="sxs-lookup"><span data-stu-id="66369-113">-ServerName</span></span>
<span data-ttu-id="66369-114">Especifica o nome do servidor de banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="66369-114">Specifies the name of SQL database server.</span></span>

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

### <span data-ttu-id="66369-115">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="66369-115">-VirtualEndpointName</span></span>
<span data-ttu-id="66369-116">Especifica o nome do ponto de extremidade virtual.</span><span class="sxs-lookup"><span data-stu-id="66369-116">Specifies the name of the virtual end point.</span></span>

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

### <span data-ttu-id="66369-117">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="66369-117">-Confirm</span></span>
<span data-ttu-id="66369-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="66369-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66369-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66369-119">-WhatIf</span></span>
<span data-ttu-id="66369-120">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="66369-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66369-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="66369-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66369-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66369-122">CommonParameters</span></span>
<span data-ttu-id="66369-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66369-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66369-124">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="66369-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66369-125">Entradas</span><span class="sxs-lookup"><span data-stu-id="66369-125">INPUTS</span></span>

### <span data-ttu-id="66369-126">System.String</span><span class="sxs-lookup"><span data-stu-id="66369-126">System.String</span></span>

## <span data-ttu-id="66369-127">Saídas</span><span class="sxs-lookup"><span data-stu-id="66369-127">OUTPUTS</span></span>

### <span data-ttu-id="66369-128">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="66369-128">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="66369-129">Notas</span><span class="sxs-lookup"><span data-stu-id="66369-129">NOTES</span></span>

## <span data-ttu-id="66369-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="66369-130">RELATED LINKS</span></span>

[<span data-ttu-id="66369-131">New-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="66369-131">New-AzSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="66369-132">Remove-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="66369-132">Remove-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="66369-133">Set-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="66369-133">Set-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="66369-134">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="66369-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

