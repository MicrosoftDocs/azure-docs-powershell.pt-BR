---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 41D63CC1-5E9F-48D3-89DE-0F753C7475F2
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlserverdisasterrecoveryconfigurationactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDisasterRecoveryConfigurationActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDisasterRecoveryConfigurationActivity.md
ms.openlocfilehash: 68e81a7f51ca385d5671698ad8624f523ae98c53
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886714"
---
# <span data-ttu-id="e1238-101">Get-AzSqlServerDisasterRecoveryConfigurationActivity</span><span class="sxs-lookup"><span data-stu-id="e1238-101">Get-AzSqlServerDisasterRecoveryConfigurationActivity</span></span>

## <span data-ttu-id="e1238-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1238-102">SYNOPSIS</span></span>
<span data-ttu-id="e1238-103">Obtém atividade para uma configuração de recuperação do sistema do servidor de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e1238-103">Gets activity for a database server system recovery configuration.</span></span>

## <span data-ttu-id="e1238-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e1238-104">SYNTAX</span></span>

```
Get-AzSqlServerDisasterRecoveryConfigurationActivity [-ServerName] <String>
 -ServerDisasterRecoveryConfigurationName <String> [-OperationId <Guid>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1238-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e1238-105">DESCRIPTION</span></span>
<span data-ttu-id="e1238-106">O cmdlet **Get-AzSqlServerDisasterRecoveryConfigurationActivity** obtém atividade para uma configuração de recuperação do sistema SQL servidor de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e1238-106">The **Get-AzSqlServerDisasterRecoveryConfigurationActivity** cmdlet gets activity for a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="e1238-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e1238-107">EXAMPLES</span></span>

## <span data-ttu-id="e1238-108">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e1238-108">PARAMETERS</span></span>

### <span data-ttu-id="e1238-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1238-109">-DefaultProfile</span></span>
<span data-ttu-id="e1238-110">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="e1238-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e1238-111">-OperationId</span><span class="sxs-lookup"><span data-stu-id="e1238-111">-OperationId</span></span>
<span data-ttu-id="e1238-112">Especifica a ID da operação.</span><span class="sxs-lookup"><span data-stu-id="e1238-112">Specifies the operation ID.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1238-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1238-113">-ResourceGroupName</span></span>
<span data-ttu-id="e1238-114">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e1238-114">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="e1238-115">-ServerDisasterRecoveryConfigurationName</span><span class="sxs-lookup"><span data-stu-id="e1238-115">-ServerDisasterRecoveryConfigurationName</span></span>
<span data-ttu-id="e1238-116">Especifica o nome da configuração de recuperação do sistema do servidor.</span><span class="sxs-lookup"><span data-stu-id="e1238-116">Specifies the name of the server system recovery configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1238-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e1238-117">-ServerName</span></span>
<span data-ttu-id="e1238-118">Especifica o nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="e1238-118">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="e1238-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e1238-119">-Confirm</span></span>
<span data-ttu-id="e1238-120">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1238-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1238-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1238-121">-WhatIf</span></span>
<span data-ttu-id="e1238-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e1238-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1238-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e1238-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1238-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1238-124">CommonParameters</span></span>
<span data-ttu-id="e1238-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1238-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1238-126">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e1238-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1238-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e1238-127">INPUTS</span></span>

### <span data-ttu-id="e1238-128">System.String</span><span class="sxs-lookup"><span data-stu-id="e1238-128">System.String</span></span>

### <span data-ttu-id="e1238-129">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="e1238-129">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="e1238-130">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e1238-130">OUTPUTS</span></span>

### <span data-ttu-id="e1238-131">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationActivityModel</span><span class="sxs-lookup"><span data-stu-id="e1238-131">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationActivityModel</span></span>

## <span data-ttu-id="e1238-132">NOTES</span><span class="sxs-lookup"><span data-stu-id="e1238-132">NOTES</span></span>

## <span data-ttu-id="e1238-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e1238-133">RELATED LINKS</span></span>

[<span data-ttu-id="e1238-134">SQL documentação do banco de dados</span><span class="sxs-lookup"><span data-stu-id="e1238-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
