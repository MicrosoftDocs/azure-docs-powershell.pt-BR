---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 41D63CC1-5E9F-48D3-89DE-0F753C7475F2
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverdisasterrecoveryconfigurationactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDisasterRecoveryConfigurationActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDisasterRecoveryConfigurationActivity.md
ms.openlocfilehash: ad3c257366513a5cc9998b4e4edea8879dc38545
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110822"
---
# <span data-ttu-id="b0390-101">Get-AzSqlServerDisasterRecoveryConfigurationActivity</span><span class="sxs-lookup"><span data-stu-id="b0390-101">Get-AzSqlServerDisasterRecoveryConfigurationActivity</span></span>

## <span data-ttu-id="b0390-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b0390-102">SYNOPSIS</span></span>
<span data-ttu-id="b0390-103">Obtém a atividade para uma configuração de recuperação do sistema do servidor de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="b0390-103">Gets activity for a database server system recovery configuration.</span></span>

## <span data-ttu-id="b0390-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b0390-104">SYNTAX</span></span>

```
Get-AzSqlServerDisasterRecoveryConfigurationActivity [-ServerName] <String>
 -ServerDisasterRecoveryConfigurationName <String> [-OperationId <Guid>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0390-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b0390-105">DESCRIPTION</span></span>
<span data-ttu-id="b0390-106">O cmdlet **Get-AzSqlServerDisasterRecoveryConfigurationActivity** Obtém atividade para uma configuração de recuperação do sistema de servidor de banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="b0390-106">The **Get-AzSqlServerDisasterRecoveryConfigurationActivity** cmdlet gets activity for a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="b0390-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b0390-107">EXAMPLES</span></span>

## <span data-ttu-id="b0390-108">OS</span><span class="sxs-lookup"><span data-stu-id="b0390-108">PARAMETERS</span></span>

### <span data-ttu-id="b0390-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0390-109">-DefaultProfile</span></span>
<span data-ttu-id="b0390-110">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="b0390-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b0390-111">-OperationId</span><span class="sxs-lookup"><span data-stu-id="b0390-111">-OperationId</span></span>
<span data-ttu-id="b0390-112">Especifica a ID da operação.</span><span class="sxs-lookup"><span data-stu-id="b0390-112">Specifies the operation ID.</span></span>

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

### <span data-ttu-id="b0390-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0390-113">-ResourceGroupName</span></span>
<span data-ttu-id="b0390-114">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b0390-114">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="b0390-115">-ServerDisasterRecoveryConfigurationName</span><span class="sxs-lookup"><span data-stu-id="b0390-115">-ServerDisasterRecoveryConfigurationName</span></span>
<span data-ttu-id="b0390-116">Especifica o nome da configuração de recuperação do sistema do servidor.</span><span class="sxs-lookup"><span data-stu-id="b0390-116">Specifies the name of the server system recovery configuration.</span></span>

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

### <span data-ttu-id="b0390-117">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="b0390-117">-ServerName</span></span>
<span data-ttu-id="b0390-118">Especifica o nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="b0390-118">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="b0390-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b0390-119">-Confirm</span></span>
<span data-ttu-id="b0390-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b0390-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0390-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0390-121">-WhatIf</span></span>
<span data-ttu-id="b0390-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b0390-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0390-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b0390-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0390-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0390-124">CommonParameters</span></span>
<span data-ttu-id="b0390-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0390-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0390-126">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b0390-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0390-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b0390-127">INPUTS</span></span>

### <span data-ttu-id="b0390-128">System. String</span><span class="sxs-lookup"><span data-stu-id="b0390-128">System.String</span></span>

### <span data-ttu-id="b0390-129">System. Nullable ' 1 [[System. GUID, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="b0390-129">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="b0390-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b0390-130">OUTPUTS</span></span>

### <span data-ttu-id="b0390-131">Microsoft. Azure. Commands. Sql. ServerDisasterRecoveryConfiguration. Model. AzureSqlServerDisasterRecoveryConfigurationActivityModel</span><span class="sxs-lookup"><span data-stu-id="b0390-131">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationActivityModel</span></span>

## <span data-ttu-id="b0390-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b0390-132">NOTES</span></span>

## <span data-ttu-id="b0390-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b0390-133">RELATED LINKS</span></span>

[<span data-ttu-id="b0390-134">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="b0390-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
