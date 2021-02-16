---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2A74E72B-BD6B-45D7-9C19-B2575C60C43F
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: df3ed9faa96a98b4e94df370bf90161e7baf2b99
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118605"
---
# <span data-ttu-id="af49b-101">Remove-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="af49b-101">Remove-AzSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="af49b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="af49b-102">SYNOPSIS</span></span>
<span data-ttu-id="af49b-103">Remove uma configuração de recuperação do sistema do servidor de banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="af49b-103">Removes a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="af49b-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="af49b-104">SYNTAX</span></span>

```
Remove-AzSqlServerDisasterRecoveryConfiguration [-VirtualEndpointName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="af49b-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="af49b-105">DESCRIPTION</span></span>
<span data-ttu-id="af49b-106">O cmdlet **Remove-AzSqlServerDisasterRecoveryConfiguration** remove uma configuração de recuperação do sistema do servidor de banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="af49b-106">The **Remove-AzSqlServerDisasterRecoveryConfiguration** cmdlet removes a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="af49b-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="af49b-107">EXAMPLES</span></span>

## <span data-ttu-id="af49b-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="af49b-108">PARAMETERS</span></span>

### <span data-ttu-id="af49b-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af49b-109">-DefaultProfile</span></span>
<span data-ttu-id="af49b-110">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="af49b-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="af49b-111">-Forçar</span><span class="sxs-lookup"><span data-stu-id="af49b-111">-Force</span></span>
<span data-ttu-id="af49b-112">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="af49b-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="af49b-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af49b-113">-ResourceGroupName</span></span>
<span data-ttu-id="af49b-114">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="af49b-114">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="af49b-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="af49b-115">-ServerName</span></span>
<span data-ttu-id="af49b-116">Especifica o nome de um servidor de banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="af49b-116">Specifies the name of a SQL database server.</span></span>

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

### <span data-ttu-id="af49b-117">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="af49b-117">-VirtualEndpointName</span></span>
<span data-ttu-id="af49b-118">Especifica o nome de um ponto de extremidade virtual.</span><span class="sxs-lookup"><span data-stu-id="af49b-118">Specifies the name of a virtual end point.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af49b-119">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="af49b-119">-Confirm</span></span>
<span data-ttu-id="af49b-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af49b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af49b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af49b-121">-WhatIf</span></span>
<span data-ttu-id="af49b-122">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="af49b-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af49b-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="af49b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af49b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af49b-124">CommonParameters</span></span>
<span data-ttu-id="af49b-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af49b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af49b-126">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="af49b-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af49b-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="af49b-127">INPUTS</span></span>

### <span data-ttu-id="af49b-128">System.String</span><span class="sxs-lookup"><span data-stu-id="af49b-128">System.String</span></span>

## <span data-ttu-id="af49b-129">Saídas</span><span class="sxs-lookup"><span data-stu-id="af49b-129">OUTPUTS</span></span>

### <span data-ttu-id="af49b-130">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="af49b-130">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="af49b-131">Notas</span><span class="sxs-lookup"><span data-stu-id="af49b-131">NOTES</span></span>

## <span data-ttu-id="af49b-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="af49b-132">RELATED LINKS</span></span>

[<span data-ttu-id="af49b-133">Get-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="af49b-133">Get-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="af49b-134">New-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="af49b-134">New-AzSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="af49b-135">Set-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="af49b-135">Set-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="af49b-136">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="af49b-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
