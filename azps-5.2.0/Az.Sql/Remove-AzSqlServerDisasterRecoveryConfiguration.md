---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2A74E72B-BD6B-45D7-9C19-B2575C60C43F
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: df3ed9faa96a98b4e94df370bf90161e7baf2b99
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98256662"
---
# <span data-ttu-id="094bf-101">Remove-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="094bf-101">Remove-AzSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="094bf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="094bf-102">SYNOPSIS</span></span>
<span data-ttu-id="094bf-103">Remove uma configuração de recuperação do sistema de servidor de banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="094bf-103">Removes a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="094bf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="094bf-104">SYNTAX</span></span>

```
Remove-AzSqlServerDisasterRecoveryConfiguration [-VirtualEndpointName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="094bf-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="094bf-105">DESCRIPTION</span></span>
<span data-ttu-id="094bf-106">O cmdlet **Remove-AzSqlServerDisasterRecoveryConfiguration** remove uma configuração de recuperação do sistema de servidor de banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="094bf-106">The **Remove-AzSqlServerDisasterRecoveryConfiguration** cmdlet removes a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="094bf-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="094bf-107">EXAMPLES</span></span>

## <span data-ttu-id="094bf-108">OS</span><span class="sxs-lookup"><span data-stu-id="094bf-108">PARAMETERS</span></span>

### <span data-ttu-id="094bf-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="094bf-109">-DefaultProfile</span></span>
<span data-ttu-id="094bf-110">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="094bf-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="094bf-111">-Force</span><span class="sxs-lookup"><span data-stu-id="094bf-111">-Force</span></span>
<span data-ttu-id="094bf-112">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="094bf-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="094bf-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="094bf-113">-ResourceGroupName</span></span>
<span data-ttu-id="094bf-114">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="094bf-114">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="094bf-115">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="094bf-115">-ServerName</span></span>
<span data-ttu-id="094bf-116">Especifica o nome de um servidor de banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="094bf-116">Specifies the name of a SQL database server.</span></span>

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

### <span data-ttu-id="094bf-117">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="094bf-117">-VirtualEndpointName</span></span>
<span data-ttu-id="094bf-118">Especifica o nome de um ponto de extremidade virtual.</span><span class="sxs-lookup"><span data-stu-id="094bf-118">Specifies the name of a virtual end point.</span></span>

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

### <span data-ttu-id="094bf-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="094bf-119">-Confirm</span></span>
<span data-ttu-id="094bf-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="094bf-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="094bf-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="094bf-121">-WhatIf</span></span>
<span data-ttu-id="094bf-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="094bf-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="094bf-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="094bf-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="094bf-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="094bf-124">CommonParameters</span></span>
<span data-ttu-id="094bf-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="094bf-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="094bf-126">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="094bf-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="094bf-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="094bf-127">INPUTS</span></span>

### <span data-ttu-id="094bf-128">System. String</span><span class="sxs-lookup"><span data-stu-id="094bf-128">System.String</span></span>

## <span data-ttu-id="094bf-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="094bf-129">OUTPUTS</span></span>

### <span data-ttu-id="094bf-130">Microsoft. Azure. Commands. Sql. ServerDisasterRecoveryConfiguration. Model. AzureSqlServerDisasterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="094bf-130">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="094bf-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="094bf-131">NOTES</span></span>

## <span data-ttu-id="094bf-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="094bf-132">RELATED LINKS</span></span>

[<span data-ttu-id="094bf-133">Get-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="094bf-133">Get-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="094bf-134">New-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="094bf-134">New-AzSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="094bf-135">Set-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="094bf-135">Set-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="094bf-136">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="094bf-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
