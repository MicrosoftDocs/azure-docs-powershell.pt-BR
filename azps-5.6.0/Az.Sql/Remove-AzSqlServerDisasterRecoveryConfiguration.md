---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2A74E72B-BD6B-45D7-9C19-B2575C60C43F
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: 10da2a625eb3858e77343275246d8a142fefc504
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890975"
---
# <span data-ttu-id="28de1-101">Remove-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="28de1-101">Remove-AzSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="28de1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28de1-102">SYNOPSIS</span></span>
<span data-ttu-id="28de1-103">Remove uma configuração de recuperação do sistema SQL servidor de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="28de1-103">Removes a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="28de1-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="28de1-104">SYNTAX</span></span>

```
Remove-AzSqlServerDisasterRecoveryConfiguration [-VirtualEndpointName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="28de1-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="28de1-105">DESCRIPTION</span></span>
<span data-ttu-id="28de1-106">O cmdlet **Remove-AzSqlServerDisasterRecoveryConfiguration** remove uma configuração SQL recuperação do sistema do servidor de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="28de1-106">The **Remove-AzSqlServerDisasterRecoveryConfiguration** cmdlet removes a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="28de1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="28de1-107">EXAMPLES</span></span>

## <span data-ttu-id="28de1-108">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="28de1-108">PARAMETERS</span></span>

### <span data-ttu-id="28de1-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28de1-109">-DefaultProfile</span></span>
<span data-ttu-id="28de1-110">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="28de1-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="28de1-111">-Force</span><span class="sxs-lookup"><span data-stu-id="28de1-111">-Force</span></span>
<span data-ttu-id="28de1-112">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="28de1-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="28de1-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28de1-113">-ResourceGroupName</span></span>
<span data-ttu-id="28de1-114">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="28de1-114">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="28de1-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="28de1-115">-ServerName</span></span>
<span data-ttu-id="28de1-116">Especifica o nome de um servidor SQL banco de dados.</span><span class="sxs-lookup"><span data-stu-id="28de1-116">Specifies the name of a SQL database server.</span></span>

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

### <span data-ttu-id="28de1-117">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="28de1-117">-VirtualEndpointName</span></span>
<span data-ttu-id="28de1-118">Especifica o nome de um ponto de extremidade virtual.</span><span class="sxs-lookup"><span data-stu-id="28de1-118">Specifies the name of a virtual end point.</span></span>

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

### <span data-ttu-id="28de1-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="28de1-119">-Confirm</span></span>
<span data-ttu-id="28de1-120">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="28de1-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28de1-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28de1-121">-WhatIf</span></span>
<span data-ttu-id="28de1-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="28de1-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28de1-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="28de1-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28de1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28de1-124">CommonParameters</span></span>
<span data-ttu-id="28de1-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28de1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28de1-126">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="28de1-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28de1-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="28de1-127">INPUTS</span></span>

### <span data-ttu-id="28de1-128">System.String</span><span class="sxs-lookup"><span data-stu-id="28de1-128">System.String</span></span>

## <span data-ttu-id="28de1-129">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="28de1-129">OUTPUTS</span></span>

### <span data-ttu-id="28de1-130">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="28de1-130">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="28de1-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="28de1-131">NOTES</span></span>

## <span data-ttu-id="28de1-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="28de1-132">RELATED LINKS</span></span>

[<span data-ttu-id="28de1-133">Get-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="28de1-133">Get-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="28de1-134">New-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="28de1-134">New-AzSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="28de1-135">Set-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="28de1-135">Set-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="28de1-136">SQL documentação do banco de dados</span><span class="sxs-lookup"><span data-stu-id="28de1-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
